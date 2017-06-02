# /etc/hosts

## Cодержание урока

Прежде чем наша машина обратиться к DNS для выполнения запроса, она сначала ищет локально на наших машинах.

<b>/etc/hosts</b>

Файл /etc/hosts содержит сопоставления некоторых имен хостов с IP-адресами. Поля довольно понятны, есть одно для IP-адреса, имя хоста, а затем любой псевдоним для хоста.

<pre>
pete@icebox:~$ cat /etc/hosts
127.0.0.1       localhost
127.0.1.1       icebox
</pre>

Обычно в этом файле вы видите свой локальный адрес, указанный по умолчанию. Вы также можете управлять доступом к хостам, изменяя файлы /etc/hosts.deny или /etc/hosts.allow. Однако, если вы бережете свою безопасность, это не будет лучшим решением, и вам следует вместо этого изменить правила брандмауэра.

Давайте посмотрим на забавный пример /etc/hosts. Измените файл и добавьте строку для:

<pre>
123.45.6.7  www.google.com
</pre>

Сохраните файл и перейдите на сайт www.google.com. Возникли проблемы, не так ли? Это потому, что мы просто сопоставили www.google.com с совершенно неправильным IP-адресом. Поскольку наши хосты сначала просматривают локально для сопоставления IP-адресов, он никогда не достигает DNS, чтобы найти google.com.

<b>/etc/resolv.conf</b>

Традиционно мы использовали файл /etc/resolv.conf для сопоставления DNS-серверов имен для более эффективного поиска, однако с улучшениями, внесенными в DNS, этот файл часто не имеет значения, по сути, вы можете увидеть в моем примере ниже, что /etc/resolv.conf не управляется вручную. Для управления сопоставлениями имен DNS-серверов см. Специальные настройки для распределения.

<pre>
conf(5) file for glibc resolver(3) generated by resolvconf(8)
#     DO NOT EDIT THIS FILE BY HAND -- YOUR CHANGES WILL BE OVERWRITTEN
nameserver 127.0.1.1
search localdomain
</pre>

## Задание

Нет задания для этого урока.

## Вопрос

Какой файл используется для сопоставления имен хостов с IP-адресами на наших компьютерах?

## Ответ

/etc/hosts