1) Выполнить команду ```top &> /dev/null &```
2) С помощью ps найти процесс top
3) В директории /proc найти каталог, который соответствует найденному выше процессу top
4) Убить процесс top
5) В домашней директории диреткорию servers и в ней создать файл web_server с содержимым
```
#!/bin/bash
LOG_FILE="$HOME/web_server.log"
log_levels=("ERROR" "INFO" "WARNING" "DEBUG")
methods=("GET" "POST" "PUT" "PATCH" "OPTIONS" "DELETE")
echo "Starting web-server on $(hostname)" >> $LOG_FILE
while true
do
  sleep 5
  random_method=${methods[$RANDOM % ${#methods[@]}]}
  random_level=${log_levels[$RANDOM % ${#log_levels[@]}]}
  echo "$(date +"%Y-%d-%m [%H:%M:%S]") $random_level $random_method" >> $LOG_FILE
  sleep 5
done
```
6) Сделать файл web_server исполняемым для всех
7) Выполнить команду ```./web_server &> /dev/null &```
8) Найти id процесса web_server
9) В домашней директории найти файл web_server.log и посмотреть его содержимое
10) В директории /proc найти каталог, который соответствует найденному выше процессу web_server
11) Запустить top и найти в нем процесс web_server. Сколько CPU и MEM он потребляет?
12) Приостановить процесс web_server (поставить на паузу, а не убить)
13) Вернуть из паузы процесс web_server
14) Убить процесс web_server
15) В директории servers создать файл simple-server с содержимым
```
#!/bin/bash
LOG_FILE="simple_server.log"

log() {
    echo "$(date '+%Y-%m-%d %H:%M:%S') - $1" >> "$LOG_FILE"
}

if command -v nc >/dev/null 2>&1; then
  log "Skipping..."
else
  if sudo apt-get update && sudo apt-get install -y netcat; then
    log "Succees"
  else
    log "Error when install netcat"
  fi
fi

PORT=8082
while :; do
  { echo -ne "HTTP/1.1 200 OK\r\nContent-Length: $(echo -n "Hello, World!")\r\n\r\nHello, World!"; } | nc -l -p "$PORT" >> simple_server.log 2>&1
done
```
16) Выполнить команду ```./simple-server &> /dev/null &```
17) Найти id процесса simple-server
18) Выполнить команду curl 127.0.0.1:8082
19) Проверить, появился ли в директории servers файл simple_server.log, посмотреть его содержимое
20) В директории /proc найти каталог, который соответствует найденному выше процессу simple-server
21) Запустить top и найти в нем процесс simple-server
22) Приостановить процесс simple-server
23) Вернуть из паузы процесс simple-server
24) Убить процесс simple-server
