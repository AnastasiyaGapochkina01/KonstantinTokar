1) Создать в домашней директории папку home_works
2) В директории home_works создать директорию text_processing
3) В директории text_processing создать файл info.csv с таким содержимым
```
Name:Company:Price:Ganre:Multiplayer
Item1:Company1:60000$:Ganre1:Yes
Item2:Company2:70000$:Ganre2:Yes
Item3:Company3:90000$:Ganre1:Yes
Item4:Company4:90000$:Ganre1:No
Item5:Company5:110000$:Ganre1:Yes
Item6:Company6:410000$:Ganre2:Yes
Item7:Company1:60000$:Ganre1:Yes
Item8:Company4:40000$:Ganre2:No
Item9:Company3:90000$:Ganre1:Yes
```
4) В файле info.csv с помощью grep найти строки, которые содержат слово No
5) В файле info.csv найти все строки, в которых встречается слово Ganre2
6) В файле info.csv найти все строки, в которых встречается слово Ganre2 и вывести только 3 поле
7) В директории text_processing создат файл metrics с содержимым
```
metric_name:metric_type:interval
cache_disk_use:gauge:1
cache_use:gauge:0
key_buffer_bytes_used:byte:3
table.rows.read:count:10
disk_use:gauge:10
data_size:gauge:1
rows_deleted:count:1
bytes_received:byte:1
```
8) В файле metrics найти все строки, в которых встречается слово gauge и вывести только первое поле
9) В файле metrics найти все строки, в которых встречается слово byte и вывести только 3 поле
10) В файле metrics найти все строки, в которых встречается слово disk и вывести только 2 поле
11) В файле metrics найти все строки, которые начинаются с cache
12) В файле info.csv найти все строки, которые содержат слово Company4
13) В директории text_processing создать файл products с содержимым
```
Handle:Title:SKU:Location:On hand:Available:Count
product-1:Product A:PROD-A:Warehouse A:100
product-1:Product A:PROD-A:Warehouse A:50
product-2:Product B:PROD-B:Warehouse B:200
product-2:Product B:PROD-B:Warehouse B:150
product-3:Product C:PROD-C:Warehouse C:300
product-4:Product D:PROD-D:Warehouse A:400
product-4:Product D:PROD-D:Warehouse A:250
product-5:Product E:PROD-E:Warehouse B:500
product-5:Product E:PROD-E:Warehouse B:300
product-6:Product F:PROD-F:Warehouse C:600
product-6:Product F:PROD-F:Warehouse C:400
```
14) С помощью grep найти в файле products все строки, содержащие слово PROD-C
15) С помощью grep найти в файле products все строки, содержащие слово product-3 и вывести для них последний столбец
16) С помощью grep найти в файле products все строки, у которых столбец Available равен C и для них вывести первый и последний столбец
17) В директории text_processing создать файл hosts с содержимым
```
hostname,interval,timestamp,%user,%system,%memory
sel-srv1,600,2023-10-08 00:00:01 UTC,30.01,20.77,96.21
sel-srv1,600,2023-10-08 00:05:01 UTC,40.07,13.00,84.55
sel-srv1,600,2023-10-08 00:10:01 UTC,5.00,90.55,89.23
sel-srv2,600,2023-10-09 00:15:01 UTC,25.01,15.77,92.21
sel-srv3,600,2023-10-09 00:20:01 UTC,35.07,10.00,80.55
sel-srv3,600,2023-10-09 00:25:01 UTC,10.00,85.55,88.23
sel-srv2,600,2023-10-09 00:30:01 UTC,20.01,25.77,95.21
sel-srv2,600,2023-10-09 00:35:01 UTC,45.07,12.00,82.55
sel-srv3,600,2023-10-09 00:40:01 UTC,15.00,80.55,87.23
```
18) С помощью grep найти в файле hosts строки, содержащие sel-srv2 и вывести 3 столбец
19) С помощью grep найти в файле hosts строки, содержащие дату 2023-10-08
20)  В директории text_processing создать файл inventory с содержимым
```
[Compute1]
IP_Address = 192.168.1.100
Location = Datacenter A
Service_Name = Web Server

[Compute2]
IP_Address = 192.168.1.101
Location = Datacenter B
Service_Name = Database Server

[Compute3]
IP_Address = 192.168.1.102
Location = Datacenter C
Service_Name = Application Server

[Compute4]
IP_Address = 192.168.1.103
Location = Datacenter A
Service_Name = File Server

[Compute5]
IP_Address = 192.168.1.104
Location = Datacenter B
Service_Name = Mail Server
```
21) С помощью grep в файле inventory найти все хосты, которые относятся к Datacenter B
22) С помощью grep в файле inventory найти все хосты, которые относятся к Datacenter C и вывести только их ip
23) Отфильровать вывод команды lscpu так, чтобы получить значение CPU MHz
24) Отфильровать вывод команды lscpu так, чтобы получить значение Hypervisor vendor
25) Из файла /proc/meminfo получить все строки. относящиеся к HugePages
26) Отфильтровать вывод команды lsblk так, чтобы получить все разделы (раздел это та строка, где 6 поле имеет значение part)
27) Для полученных в предыдущем задании разделов вывести их имена
28) С помощью awk вывести из файла /etc/passwd имена всех пользователей (первое поле)
29) С помощью awk вывести из файла /etc/passwd последнее поле
30) Отфильтровать вывод команды free -h так, чтобы получить размер Mem
31) В директории text_processing создать файл logs с содержимым
```
# Cron logs
Oct 20 06:24:01 server1 CRON[1349677]: (user1) CMD (   /usr/bin/python3 /home/user1/update.py)
Oct 20 06:25:01 server3 CRON[1349678]: (user2) CMD (   /usr/bin/python3 /home/user2/report.py)
Oct 20 06:26:01 server2 CRON[1349679]: (root) CMD (   /usr/bin/cleanup.sh)
Oct 20 06:27:01 server3 CRON[1349680]: (user3) CMD (   /usr/bin/backup.sh)
Oct 20 06:28:01 server1 CRON[1349681]: (user4) CMD (   /usr/bin/monitor.sh)

# Error logs
Oct 20 06:30:00 server1 sshd[12345]: Failed password for invalid user admin from 192.168.0.10 port 22 ssh2
Oct 20 06:31:00 server3 sshd[12346]: Failed password for invalid user guest from 192.168.0.11 port 22 ssh2
Oct 20 06:32:00 server1 sshd[12347]: Accepted password for user2 from 192.168.0.12 port 22 ssh2
Oct 20 06:33:00 server1 sshd[12348]: Failed password for invalid user test from 192.168.0.13 port 22 ssh2

# Warning logs
Oct 20 06:35:00 server1 kernel: [123456] Warning! CPU temperature is high.
Oct 21 09:10:00 server2 kernel: [123458] Warning! High CPU usage detected on process ID 5678.
Oct 21 09:11:00 server2 systemd[1]: Warning! Service myservice.service is taking too long to start.
Oct 21 09:12:00 server2 sshd[23461]: Warning! Multiple failed login attempts from 192.168.0.25.
Oct 21 09:13:00 server2 application[34571]: Warning! Disk space on /home is below 10% remaining.

# Info logs
Oct 21 09:02:00 server2 application[34569]: INFO User1 logged in successfully.
Oct 21 09:03:00 server2 application[34570]: INFO User3 logged out.
Oct 21 09:14:00 server2 application[34572]: INFO User4 logged in successfully from 192.168.0.26.
Oct 21 09:15:00 server2 application[34573]: INFO Backup completed successfully at /backup/user4_backup.tar.gz.
Oct 21 09:16:00 server2 systemd[1]: INFO Service myservice.service started successfully.
Oct 21 09:17:00 server2 sshd[23462]: INFO User1 logged out from session on terminal pts/0.
```
32) В файле logs.txt найти все записи, которые содержат application
33) В файле logs найти записи о запусках cron на сервере server3 и вывести команду, которая запускалась (это то, что в скобках в конце)

<img width="928" alt="image" src="https://github.com/user-attachments/assets/c61ff7c3-5346-45ff-a45e-c6511dde87a1">

34) В файле logs найти запись о сервисе myservice
35) В файле logs найти все записи, содержащие ssh и вывести для них название сервера (третье поле)

<img width="714" alt="image" src="https://github.com/user-attachments/assets/b13e56a0-1b74-438f-b910-55b9d4e1e4fa">

36) В файле logs найти все записи, содержащие kernel и вывести для них шестое поле
37) В файле logs найти все записи, содержащие "Failed password" и вывести только ip

<img width="699" alt="image" src="https://github.com/user-attachments/assets/da09364f-353d-4bd5-8563-423402547b1b">

38) В файле logs.txt найти записи, содержащие "Accepted password" и вывести имя пользователя и ip

<img width="688" alt="image" src="https://github.com/user-attachments/assets/1d36804e-31b3-4257-9b1d-97c0130a3acc">

39) В файле logs.txt найти записи, содержащие "Disk space" и вывести название сервера
40) Из файла /etc/os-release получить версию установленного Linux
