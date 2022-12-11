# Ответ на задание №1:
Docker Compose нужен для того что бы несколько контейнеров Docker каждый например с отдельно функционирующим языком,базой данных,веб сервером обьединялись  в одно работающее приложение например Zabbix. Отвечая  немного на последнее задание со звездочкой работа с Docker Compose в выше описанной задаче  занимает в разы меньше времени  и позволяет так же экономить это время при переездах или маштабированиях.

# Ответ на задание №2:
![DC2](https://user-images.githubusercontent.com/107581500/206919421-6399c642-ad96-40ed-a08a-ea68be9bba09.JPG)

# Ответ на задание №3:
![DC3](https://user-images.githubusercontent.com/107581500/206919433-d7ce55e9-871c-4de0-b0f7-a98d23eaf501.JPG)

# Ответ на задание №4:
![DC4](https://user-images.githubusercontent.com/107581500/206919460-0dbe9079-4fa2-4eb7-97a5-aa8e9dee58b9.JPG)

# Ответ на задание №5-№6:

![DC5-6](https://user-images.githubusercontent.com/107581500/206919496-ecb516e8-5701-4c04-a86e-262afaa30c10.JPG)

# Ответ на задание №7:





```version: "3"
services:

 zaprudnovva-netology-db:
  image: postgres:latest
  container_name: zaprudnovva-netology-db
  ports:
   - 5432:5432
  volumes:
   - ./pg_data:/var/lib/postgresql/data/pgdata
  environment:
   POSTGRES_PASSWORD: zaprudnovva12!3!!
   POSTGRES_DB: zaprudnovva-netology-db
   PGDATA: /var/lib/postgresql/data/pgdata
  networks:
   zaprudnovva-my-netology-hw:
    ipv4_address: 172.22.0.2
  restart: always

 pgadmin:
  image: dpage/pgadmin4
  links:
   - zaprudnovva-netology-db
  container_name: zaprudnovva-netology-pgadmin
  environment:
   PGADMIN_DEFAULT_EMAIL: zaprudnovva-@ilove-netology.com
   PGADMIN_DEFAULT_PASSWORD: 123
  ports:
   - "61231:80"
  networks:
   zaprudnovva-my-netology-hw:
    ipv4_address: 172.22.0.3
  restart: always

 zaprudnovva-zabbix-server:
  image: zabbix/zabbix-server-pgsql
  links:
   - zaprudnovva-netology-db
  container_name: zaprudnovva-netology-zabbix
  environment:
   DB_SERVER_HOST: '172.22.0.2'
   POSTGRES_USER: postgres
   POSTGRES_PASSWORD: zaprudnovva12!3!!
  ports:
   - "10051:10051"
  networks:
   zaprudnovva-my-netology-hw:
    ipv4_address: 172.22.0.4
  restart: always

 zaprudnov-zabbix-frontend:
  image: zabbix/zabbix-web-apache-pgsql
  links:
   - zaprudnovva-netology-db
   - zaprudnovva-zabbix-server
  container_name: zaprudnov-netology-zabbix-frontend
  environment:
   DB_SERVER_HOST: '172.22.0.2'
   POSTGRES_USER: 'postgres'
   POSTGRES_PASSWORD: zaprudnovva12!3!!
   ZBX_SERVER_HOST: "zaprudnov-zabbix-frontend"
   PHP_TZ: "Europe/Moscow"
  ports:
   - "80:8080"
   - "443:8443"
  networks:
   zaprudnovva-my-netology-hw:
    ipv4_address: 172.22.0.5
  restart: always

networks:
 zaprudnovva-my-netology-hw:
  driver: bridge
  ipam:
   config:
   - subnet: 172.22.0.0/24


