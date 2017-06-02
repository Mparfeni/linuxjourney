# Samba

## Содержание урока

В первые дни вычислений стало необходимо, чтобы машины Windows обменивались файлами с машинами Linux, поэтому был создан протокол сообщений сервера (SMB). SMB использовался для обмена файлами между операционными системами Windows (у Mac также есть совместное использование файлов с SMB), а затем он был очищен и оптимизирован в виде протокола общей интернет-файловой системы (CIFS).

Samba - это то, что мы называем утилитами Linux для работы с CIFS в Linux. В дополнение к совместному использованию файлов вы также можете обмениваться ресурсами, такими как принтеры.

<b>Создайте сетевой ресурс с помощью Samba</b>

Давайте рассмотрим основные шаги по созданию сетевого ресурса, доступ к которому может получить компьютер Windows:

<b>Установка Samba</b>

<pre>$ sudo apt update
$ sudo apt install samba</pre>

<b>Настройка smb.conf</b>

Файл конфигурации для Samba находится в /etc/samba/smb.conf, этот файл должен сообщить системе, какие каталоги должны быть доступны для общего доступа, их разрешения доступа и другие параметры. По умолчанию smb.conf поставляется с большим количеством кода с комментариями, и вы можете использовать их в качестве примера для написания своих собственных конфигураций.

<pre>$ sudo vi /etc/samba/smb.conf</pre>

<b>Настройка пароля для Samba</b>

<pre>$ sudo smbpasswd -a [username]</pre>

<b>Создание общего каталога</b>

<pre>$ mkdir /my/directory/to/share</pre>

<b>Перезапуск сервисов Samba</b>

<pre>$ sudo service smbd restart</pre>

<b>Доступ к ресурсу Samba через Windows</b>

В Windows просто введите сетевое соединение в командной строке: \\HOST\sharename.

<b>Доступ к ресурсу Samba / Windows через Linux</b>

<pre>$ smbclient //HOST/directory -U user</pre>

Пакет Samba включает инструмент командной строки, называемый <b> smbclient </ b>, который вы можете использовать для доступа к любому серверу Windows или Samba. Как только вы подключитесь к общему ресурсу, вы можете перемещаться и передавать файлы.

<b>Присоедините ресурс Samba к вашей системе</b>

Вместо передачи файлов один за другим вы можете просто подключить сетевой ресурс в своей системе.

<pre>$ sudo mount -t cifs servername:directory mountpount -o user=username,pass=password</pre>

## Задание

Настройте общий ресурс Samba, если у вас его нет, откройте smb.conf и ознакомьтесь с параметрами в файле конфигурации.

## Вопрос

Каков последний протокол, используемый для передачи файлов между Windows и Linux?

## Ответ

CIFS