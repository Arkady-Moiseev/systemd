# Инициализация системы. Systemd

1. Написать service, который раз в 30 секунд мониторит лог на предмет наличия ключевого слова.
2. Установить spawn-fcgi и переписать init-скрипт на unit-файл.
3. Дополнить unit-файл httpd возможностью запустить несколько инстансов сервера с разными конфигурационными файлами.
____________________________________________________

<b>1. Написать service, который раз в 30 секунд мониторит лог на предмет наличия ключевого слова.</b>

Создаем файлы со следующим содержанием

<p><a href="https://github.com/Arkady1996/systemd/blob/main/watchlog">watchlog</a> - /etc/sysconfig/watchlog</p>
<p><a href="https://github.com/Arkady1996/systemd/blob/main/watchlog.sh">watchlog.sh</a> - /opt/watchlog.sh</p>
<p><a href="https://github.com/Arkady1996/systemd/blob/main/watchlog.service">watchlog.service</a> - /etc/systemd/system/</p>
<p><a href="https://github.com/Arkady1996/systemd/blob/main/watchlog.timer">watchlog.timer</a> - /etc/systemd/system/</p>

После запуска <b>systemctl start watchlog.timer</b> можно проверить журнал <b>/var/log/messages</b>

![img_1](https://github.com/Arkady1996/systemd/blob/main/images/1.png)

<b>2. Установить spawn-fcgi и переписать init-скрипт на unit-файл.</b>

![img_2](https://github.com/Arkady1996/systemd/blob/main/images/2.png)

<b>3. Дополнить unit-файл httpd возможностью запустить несколько инстансов сервера с разными конфигурационными файлами.</b>

![img_3](https://github.com/Arkady1996/systemd/blob/main/images/3.png)

![img_31](https://github.com/Arkady1996/systemd/blob/main/images/31.png)

![img_32](https://github.com/Arkady1996/systemd/blob/main/images/32.png)
