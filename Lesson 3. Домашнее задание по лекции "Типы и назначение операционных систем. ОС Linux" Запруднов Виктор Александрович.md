# Задание 1
Кейс:
Компания ООО "Рога и Копыта" решила автоматизировать свою работу и централизировать управление учетными записями. Руководством было принято решение развернуть пять новых серверов:
систему контроля доступа пользователей и управления учетными записями;
терминальный сервер;
два сервера для веб-приложений и прокси сервер.
Какие ОС вы выберете для каких серверов? Почему?
# Ответ на задание 1:
Для серверов контроля доступа и управления учетными записями пользуюсь WindowsServer версия 2016.Из плюсов: удобный интерфейс при добавлении удалении пользователей,контроль безопасности по группам пользователей которых ты сам определяешь.

Для терминального сервера всё тот же  WindowsServer версия 2016 с программной ОС для тонких клиентов  WTware. Опять же простой и понятный интерфейс настройки. Авторизации все можно смотреть в отдельном файлике-логе.

Для серверов веб-приложений и прокси сервера скорее всего воспользовался бы CentOS от 8 версии. Настраивал на этой системе ngnix сервер для мониторинга. Так же на на аналогичной ОС сейчас работает OVPN сервер, паралельно  которому можно установить прокси. Так что я за CentOS в этом пункте.)

# Задание 2
На каких уровнях системы работают следующие службы или приложения?
оконный менеджер;
файловый менеджер;
веб-браузер;
текстовый редактор;
калькулятор.
# Ответ на задание 2:
оконный менеджер - это уровень службы операционной системы,

файловый менеджер - это  уровень пользовательских программ как например Midnight Commander,

веб-браузер,текстовый редактор и калькулятор  - так же уровень пользовательских программ
# Задание 3.
Назовите по два DEB и RPM дистрибутива.
# Ответ на задание 3:
DEB -  Astra Linux и Linux Mint,

RPM -  CentOS и Fedora
