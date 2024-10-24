# Система мониторинга Zabbix`" - `Кантемиров Роман`


### Задание 1
```
Поле для вставки кода...

 apt install posgesql -y
 wget https://repo.zabbix.com/zabbix/6.4/debian/pool/main/z/zabbix-release/zabbix-release_latest+debian11_all.deb
 dpkg -i zabbix-release_latest+debian11_all.deb
 apt update 
 
 apt install zabbix-server-pgsql zabbix-frontend-php php7.4-pgsql zabbix-apache-conf zabbix-sql-scripts zabbix-agent
 
 sudo -u postgres createuser --pwprompt zabbix
 sudo -u postgres createdb -O zabbix zabbix 

 zcat /usr/share/zabbix-sql-scripts/postgresql/server.sql.gz | sudo -u zabbix psql zabbix 
 sudo nano /etc/zabbix/zabbix_server.conf

 systemctl restart zabbix-server zabbix-agent apache2
 systemctl enable zabbix-server zabbix-agent apache2

zabbix server: 
kantemirov_rs@debian11:~$ ip a
1: lo: <LOOPBACK,UP,LOWER_UP> mtu 65536 qdisc noqueue state UNKNOWN group default qlen 1000
    link/loopback 00:00:00:00:00:00 brd 00:00:00:00:00:00
    inet 127.0.0.1/8 scope host lo
       valid_lft forever preferred_lft forever
    inet6 ::1/128 scope host 
       valid_lft forever preferred_lft forever
2: enp0s3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc pfifo_fast state UP group default qlen 1000
    link/ether 08:00:27:a0:56:b4 brd ff:ff:ff:ff:ff:ff
    inet 192.168.0.108/24 brd 192.168.0.255 scope global dynamic noprefixroute enp0s3
       valid_lft 2180sec preferred_lft 2180sec
    inet6 fe80::a00:27ff:fea0:56b4/64 scope link noprefixroute 
       valid_lft forever preferred_lft forever
kantemirov_rs@debian11:~$ 


`При необходимости прикрепитe сюда скриншоты`

[autoresation admin](https://github.com/kantemirovrs/zabbix1/blob/main/img/zabbix0.png)


---

### Задание 2
```
Поле для вставки кода...
 wget https://repo.zabbix.com/zabbix/6.4/debian/pool/main/z/zabbix-release/zabbix-release_latest+debian11_all.deb
 dpkg -i zabbix-release_latest+debian11_all.deb
 apt update 
 
 apt install zabbix-agent
 systemctl restart zabbix-agent
 systemctl enable  zabbix-agent

`При необходимости прикрепитe сюда скриншоты
![Название скриншота 2](ссылка на скриншот 2)`
![Configuration](https://github.com/kantemirovrs/zabbix1/blob/main/img/zabbix1.png)`
![Last data](https://github.com/kantemirovrs/zabbix1/blob/main/img/zabbix2.png)`
![Log](https://github.com/kantemirovrs/zabbix1/blob/main/img/zabbix3.png)`


---
1
