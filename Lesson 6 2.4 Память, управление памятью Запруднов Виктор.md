# Ответ на задание №1:
Сон  (suspend) или как его называют простой режим сна это когда происходит отключение основного питания компьютера с сохранением питание оперативной памяти.
В системной отключении питания в Linux этот режим включен по умолчанию.
Гибернацию (hibernate) это тоже режим сна только с сохранением состояние компьютера в его  жестком диске в файле подкачки(swap).Он должен превышать или быть
равен оперативной памяти компьютера для корректной работы.Данный режим считается не совсем надежным в зависимости от производителей материнских плат и выключен
по умолчанию. Что бы его включить требуются некоторые манипуляции с ядром системы и отдельными утилитами.

# Ответ на задание №2:
Данная программа называется vmstat. Она выгружает информацию о процессах,памяти, виртуальной памяти, вводе-выводе и активности процессора.
Cтолбцы si и so это память которую потребляет swap  с диска.
Swap
si: объем памяти, выгруженный с диска (/s).
so: объем памяти, перенесенный на диск (/s).
Inactive:
# Ответ на задание №3:
Добавил для себя сразу 
1. lscpu | grep Архитектура
2. cat /proc/cpuinfo | grep model, почему то не работает поиск по словам "model name" хотя они в файлике есть.
3. cat /proc/meminfo | grep Inactive
# Ответ на задание №4:
![Screenshot_20220712_142928](https://user-images.githubusercontent.com/107581500/178482787-ea4be3b4-222d-4ab3-9016-ec3cdd54db98.jpg)
![Screenshot_20220712_143140](https://user-images.githubusercontent.com/107581500/178482791-e8d4bc74-a1ce-46bd-a9f1-ee00c44ce281.jpg)
![Screenshot_20220712_143330](https://user-images.githubusercontent.com/107581500/178482794-bece38de-3c0d-423b-a48e-3189762dee51.jpg)

Сделал, но мне никто не ответил почему это не работает на Федоре. 
При активации sudo swapon /swapfile пишет:
sudo swapon /swapfile
swapon: /swapfile: swapon failed: Недопустимый аргумент

Возможно ли это что у меня Fedora и - btrfs файловая система?

Нашёл статью что без бубна тут не обойтись…
https://zen.yandex.ru/media/id/5db841f6ec575b00ad9fe361/kak-sozdat-swapfail-v-fedora-33-60473a009e9a5735c1893e75
Не стал так делать, а просто переустановил систему с ext4.



