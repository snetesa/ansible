### Day 2
[1] Создайте плэйбук uninstall-httpd.yml, который удалит httpd с управляемых хостов, удалит файл /var/www/html/index.html и закроет на фаерволе порты, используемые веб-сервером.
!Задание на условия - https://docs.ansible.com/ansible/latest/user_guide/playbooks_conditionals.html. https://docs.ansible.com/ansible/latest/modules/stat_module.html
[2] На одной из управляемых нод создайте файл /tmp/database и напишите плэйбук, который будет устанавливать mariadb-server, если такой файл существует.
!Задание на Jinja2 темплейты - https://docs.ansible.com/ansible/latest/modules/template_module.html
[3] Напишите плэйбук, который устанавливает и включает FTP (пакет vsftpd), открывает необходимые порты. Определите в переменных необходимые параметры конфигурации ftp-сервера и используйте их в j2-шаблоне для конфига vsftpd.conf:
    - разрешен анонимный доступ и аплоад файлов
    - /var/ftp/pub - настроены необходимые разрешения и соответствующий SELinux контекст
    - SELinux "ftpd_anon_write" boolean - значение "on"