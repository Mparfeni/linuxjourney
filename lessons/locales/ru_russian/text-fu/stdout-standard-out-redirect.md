# stdout (Standard Out)

## Содержание урока

Сейчас мы знакомы с многими командами и их выводом, и теперь нам предстоит перейти в следующую тему I/O (input/output, ввод/вывод) потоков. Давайте запустим следующую команду и обсудим, как она работает.

<pre>$ echo Hello World > peanuts.txt</pre>

Что только что произошло? Давайте проверим директорию, откуда вы запустили эту команду, и вот вы должны увидеть файл, названный peanuts.txt, посмотрим внутрь этого файла и увидим строку Hello World. В этой команде произошло множество вещей, давайте разберем их.

Во-первых, разберем эту часть:

<pre>$ echo Hello World</pre>

Мы знаем, что эта команда выведет на экран Hello World, но как? Процессы используют I/O потоки, чтобы получить или вернуть вывод. По-умолчанию команда echo берет ввод (стандартный ввод или stdin (standard input)) с клавиатуры и возвращает вывод (стандартный вывод или stdout(standard output)) на экран. Так вот, это то, почему когда вы вводите echo Hello World в вашей консоли, вы получаете Hello World на вашем экране. Однако, перенаправление I/O позволяет нам изменить это поведение по-умолчанию, давая нам большую гибкость при манипуляции с файлами.

Давайте перейдем к следующей части нашей команды:

<pre> > </pre>

\> - оператор перенаправления, который позволяет нам изменять направление стандартного вывода. Он позволяет нам направить вывод echo Hello World в файл, вместо экрана. Если файл не существуют, то таковой будет создан. Однако, если он существует, то он будет перезаписан (вы можете добавить флаг для предотвращения этой ситуации в зависимости от оболочки, которую вы используете).

Вот так работает перенаправление stdout!

Давайте скажем, что мы не хотим перезаписывать наш peanuts.txt, к счастью, существует оператор перенаправления, такой как >>:

<pre>$ echo Hello World >> peanuts.txt</pre>

Это добавит Hello World в конец файла peanuts.txt, если файла еще не существует, то он будет создан, также как и в случае с оператором >!


## Задание

Попробуйте пару команд:

<pre>
$ ls -l /var/log > myoutput.txt
$ echo Hello World > rm
$ > somefile.txt 
</pre>

## Вопрос

Какой оператор перенаправляет вывод в файл?

## Ответ

>>