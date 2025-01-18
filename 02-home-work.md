1) Создать пользователей user_{1,2,3,4,5}
2) Вывести из файла /etc/passwd только имена созданных пользователей (grep)
3) Добавить группы workers; teachers; students
4) Вывести из файла /etc/group только названия добавленных групп
5) Пользователей user_1 и user_2 добавить в группу workers
6) Пользователей user_3, user_4, user_5 добавить в группу students
7) Создать пользователя mentor3 и добавить в группу teachers
8) Вывести на экран состав групп workers; teachers; students
9) Задать пароли для всех пользователей
10) С помощью команды id вывести информацию о пользователе mentor3 и вывести только список его групп
11) Создать группы developers, designers, managers и admins
12) Создать пользователей jdoe, asmith, mjackson, kchen, rgarcia
13) Добавить пользователей
- mjackson в группу admins
- jdoe, kchen, rgarcia в группу developers
- asmith - в группу designers
14) Вывести из файла /etc/passwd только имена созданных пользователей
15) Вывести из файла /etc/group названия и состав добавленных групп
16) Задать пользователям пароли
17) Добавить пользователя asmith в группу managers
18) С помощью команды id получить информацию о пользователе asmith и вывести его первичную группу
19) Выполнить команду ```sudo getent shadow``` и из ее вывода получить имена добавленных в п2 пользователей и хеши их паролей
   В домашней директории создать директорию magento
20) В директории magento создать директории media, code и styles
21) В директории code создать файл index.php с содержимым
```
<?php
phpinfo();
?>
```
22) В директории styles создать файл main.css с содержимым
```
h1 {
    color: #333; /* Цвет текста */
    text-align: center; /* Выравнивание по центру */
}
```
23) В директории magento создать файл index.html с содержимым
```
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>E-commerce page</title>
    <link rel="stylesheet" href="styles.css"> <!-- Подключаем CSS -->
</head>
<body>
    <header>
        <h1>Welcome!</h1>
        <h2>e-commerce site</h2>
    </header>
```
24) Сделать владельцем файла index.html пользователя mjackson, а группой владельцев - группу developers
25) Сделать владельцем файла styles/main.css пользователя asmith, а группой владельцев - группу designers
26) Сделать владельцем файла code/index.php пользователя rgarcia, а группой владельцев - группу admins
