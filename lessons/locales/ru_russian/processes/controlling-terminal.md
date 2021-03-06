# Управлящий терминал

## Содержание урока

Мы обсудили, какие есть поле TTY в выводе ps. TTY - это терминал, который выполнил команду.

Существует два типа терминалов, обычные <b>терминальные устройства</b> и <b>псевдотерминальные устройства</b>. Обычное терминальное устройство - это собственное терминальное устройство, в которое вы можете ввести и отправить вывод в вашу систему. Это похоже на приложение, которое вы запускали для запуска терминала, но это не так.

Чтобы вы могли увидеть все в действии, наберите Ctrl-Alt-F1, чтобы попасть в TTY1 (первая виртуальная консоль), вы заметите, что у вас нет ничего, кроме терминала и т.п. Это считается обычным терминальным устройством, вы можете выйти из него с помощью Ctrl-Alt-F7.

Псевдотерминал - это то, с чем вы привыкли работать, они эмулируют терминалы с терминальным окном оболочки и обозначаются PTS. Если вы посмотрите на ps снова, вы увидите, что ваш процесс оболочки находится под pts/*, например:

<pre>
ps -e | grep pts
11477 pts/0    00:00:00 tmux
11510 pts/2    00:00:00 bash
11612 pts/2    00:00:00 sudo
11672 pts/2    00:00:00 bash
11720 pts/1    00:00:00 bash
16012 pts/1    00:00:00 man
16024 pts/1    00:00:00 pager
16750 pts/5    00:00:00 bash
27323 pts/5    00:00:00 ps
27324 pts/5    00:00:00 grep
32565 pts/3    00:00:00 ssh
32598 pts/4    00:00:00 ssh
</pre>

Теперь, возвращаясь к управляющему терминалу, процессы обычно привязаны к управляющему терминалу. Например, если вы запускали программу в своем окне оболочки, такую как Поиск, и закрыли окно, ваш процесс также будет закрыт вместе с окном.

Существуют такие процессы, как deamon-processes. Они являются особыми процессами, которые поддерживают работу системы. Они часто запускаются при загрузке системы и обычно завершаются при завершении работы системы. Они работают в фоновом режиме, и поскольку мы не хотим, чтобы эти специальные процессы завершались, они не привязаны к управляющему терминалу. В выходных данных ps TTY указан как <b>?</b>, что означает, что у него нет управляющего терминала.

## Задание

Посмотрите на свой вывод ps и перечислите все уникальные значения TTY.

## Вопрос

Какое значение у процесса,который не имеет контрольного терминала?

## Ответ

?