# Ответ на задание №1:

Чем частное облако отличается от общедоступного, публичного и гибридного?

В отличие от частного облака, общедоступное облако позволяет компании сэкономить на приобретении, администрировании и обслуживании локального оборудования и инфраструктуры приложений, так как ответственность за обслуживание системы и управление ею несет  поставщик облачных служб.  Общедоступные облака также можно развернуть быстрее, чем локальные инфраструктуры. Кроме того, они предоставляют практически бесконечно масштабируемую платформу. Каждый сотрудник компании может использовать одно и то же приложение из любого офиса или филиала на любом устройстве, имеющем доступ к Интернету. Хотя общедоступные облачные среды вызывают сомнения в плане безопасности, при правильной реализации общедоступное облако может быть таким же безопасным, как самое эффективно управляемое частное облако, если поставщик использует надлежащие методы защиты, например системы обнаружения и предотвращения вторжений.

Виртуальное частное облако (VPC, virtual private cloud) — инфраструктура, которая используется только одной компанией.Частные облака чаще представляют собой полноценную инфраструктуру, то есть IaaS.

Публичное или общедоступное облако (public cloud) — решение, при котором провайдер предоставляет доступ к сервису сразу нескольким клиентам. Каждый пользователь создает столько виртуальных серверов, сколько ему нужно, и управляет ими, но физического доступа к оборудованию у них нет.
Гибридная модель подходит компаниям, у которых есть свое частное облако, но ее недостаточно для запуска и тестирования новых сервисов.

Мультиоблачные системы тоже сочетают в себе частные и публичные облака, но последние размещены не у одного провайдера, а у нескольких. Например, почта — у одного, а резервное хранилище данных — у другого.

# Ответ на задание №2:
Что обозначают:IaaS , PaaS, SaaS, CaaS, DRaaS, BaaS, DBaaS, MaaS, DaaS, NaaS, STaaS?

IaaS - облачная инфраструктура как услуга, к инфраструктуре относят вычислительные ресурсы: виртуальные серверы, хранилища, сети.

PaaS - это Platform as a Service, платформа как услуга.Ключевое отличие PaaS от IaaS в том, что здесь у вас есть определенные инструменты, например: система управления базами данных, среда машинного обучения или обработки big data, промышленный IoT. Их нужно настроить под потребности компании, но не надо строить с нуля. Это позволяет экономить время разработчиков — например, им не нужно возиться с разработкой базы данных, можно просто загрузить в нее информацию и работать.


SaaS — это Software as a Service, программное обеспечение как сервис.Примеры SaaS — это большинство сервисов в интернете: электронная почта, CRM-системы, планировщики задач, веб-конструкторы для создания сайтов, платформы для ведения блогов. То есть все облачные программы, которые позволяют решать конкретные задачи.

CaaS (Communication as a Service)
«Коммуникация как услуга» — решение ИТ-аутсорсинга для корпоративной связи, арендованной у одного провайдера. В неё входит сервис интернет-телефонии (передача голоса по IP, то есть VoIP), мессенджеры (IM-приложения), интерфейсы совместной работы или синхронизации изменений в рабочих документах, видеоконференции.


Аварийное восстановление как услуга (DRaaS) — это модель сервиса облачных вычислений, которая позволяет организации выполнять резервное копирование данных и ИТ-инфраструктуры в стороннюю среду облачных вычислений.


BaaS (англ. banking as a service — банк как услуга) — инновационная B2B-услуга сдачи банками в аренду своей инфраструктуры.

DBaaS (Database-as-a-service)

MaaS (Monitoring as a Service)
«Мониторинг как услуга» — позволяет отслеживать ключевые параметры инфраструктуры и программного обеспечения, которые вы задаёте через центральную панель управления в веб-интерфейсе онлайн. 

Data as a Service (DaaS) – относительно новая модель дистрибуции данных, которая подразумевает, что информация сбором, управлением и хранением нужной информации компании и пользователи занимаются не самостоятельно, а делегируют эту задачу специализированным провайдерам.

Network as a Service (NaaS) — обеспечение новейшими сетевыми технологиями и решениями с максимальной стабильностью, масштабируемостью и гибкостью.

STaaS — это аренда у поставщика облачных услуг места для хранения информации в облаке.

# Ответ на задание №3:

Напишите, какой вид сервиса предоставляется пользователю, когда:

Управляет всеми процессами провайдер; - SaaS

Вы управляете приложением и данными, остальным управляет провайдер; PaaS

Вы управляете операционной системой, средой исполнения, данными, приложениями, остальными управляет провайдер; IaaS

Вы управляете сетью, хранилищами, серверами, виртуализацией, операционной системой, средой исполнения, данными, приложениями; Своя реальная инфраструктура.

# Ответ на задание №3:

![image](https://user-images.githubusercontent.com/107581500/202901378-d616c32f-f58b-4323-ba83-6c834ebc0c8b.png)

![image](https://user-images.githubusercontent.com/107581500/202901440-b8e908e8-a4f8-4d5a-85e5-8406848c4931.png)

Ответьте на следующие вопросы:

Какие ОС можно выбрать? - Любую из представленных в списке. Всё зависит от задач.

Какие параметры сервера можно выбрать? Платформу с связке процессор-графически процессор, уровень производительности vCPU, Гарантированная доля vCPU,колличество оперативной памяти.

Какие компоненты мониторинга можно создать?

Дашборды
Комбинируйте свои графики, выстраивайте в нужном порядке

Алерты
Получайте уведомления об изменении в ваших метриках

Какие системы безопасности предусмотрены? Авторизация по ключу созданному при помощи ssh-keygen

Как меняется цена от выбранных характеристик? 
Приведите пример самой дорогой конфигурации и самой дешевой.

Мощная платформа с большим колличество ОЗУ и при хорошем GPU будет стоить дороже  чем  просто процессор к ограниченным использованием vCPU и меньшим колличеством ОЗУ.В общем всё как в простой жизни с обычным физическим железом для ПК


 # Ответ на задание №4:
 
 ![1](https://user-images.githubusercontent.com/107581500/202907042-7d103ec6-f2cf-4343-8e7e-de1c455ec92c.JPG)
 
 Поставил из оф. репозитория nginx на неё и проверил. Всё работает.

 
