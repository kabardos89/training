# Ответ на задание №1:
Загрузчиков будет всего один и возможно GRUB/GRUB2. Важной особенностью остается, то что все операционные системы должны быть в разных разделах и с опредленными для них файловыми системами, для Windows это ntfs или far32, а для Linux ext4 или любая другая подходящая. Есть cпособы для обмена файлами между этими системами создавая отдельный раздел и каталог в формате fat32 которые обе ОС смогут легко читать.
# Ответ на задание №2:
В initrd находятся модули для  понимания корневой файловой системы, в последствии загрузки мы получаем доступ к нормальному хранилищу модулей ядра.Если  ядро скомпилировано со всем встроенным кодом, а не как с модулями, то initrd не требуется.
# Ответ на задание №3:
В каждом разделе диска может храниться собственный вторичный загрузчик, однако главная загрузочная запись только одна. Поэтому необходимо решить, какой из загрузчиков будет “главным”.
# Ответ на задание №4:
Особой информации про это не нашёл. В Debian по умолчанию  хранятся старые версии ядра. Их можно запускать выбирая .Все пользователи запущены в одной системе и соответственно с одного ядра. Такие вещи наверно можно сделать, но в каком то виртуальном пространстве аля virtualbox.
# Ответ на задание №5:
Благодаря виртуализации мы получаем возможность более полно утилизировать ресурсы железа. Но при этом речь идёт о полной изоляции: в виртуальной машине полностью изолированное ядро, все библиотеки, строго ограниченные ресурсы по процессору и памяти.Соответственно  ничего не произойдет если в хосте и в контейнере разные системы инициализации. При этом в одной статье написано что upstart работает благодаря интеграции  systemd.
