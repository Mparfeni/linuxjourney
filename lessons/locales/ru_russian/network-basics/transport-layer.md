# Транспортный уровень

## Содержание урока

Уровень транспорта помогает нам передавать наши данные таким образом, чтобы сети могли их читать. Это разбивает наши данные на куски, которые будут транспортироваться и складываться вместе в правильном порядке. Эти куски известны как сегменты. Сегменты упрощают передачу данных по сетям.

<b>Порты</b>

Несмотря на то, что мы знаем, куда мы отправляем наши данные по IP-адресам, они недостаточно специфичны для отправки наших данных в определенные процессы или службы. Такие службы, как HTTP, используют канал связи через порты. Если мы хотим отправить данные веб-страницы, нам нужно отправить их через порт HTTP (порт 80). В дополнение к формированию сегментов, транспортный уровень также будет присоединять исходный и целевой порты к сегменту, поэтому, когда получатель получит окончательный пакет, он будет знать, какой порт использовать.

<b>UDP</b>

Существует два популярных транспортных протокола UDP и TCP. Мы кратко обсудим UDP и проведем большую часть времени на TCP, так как он наиболее часто используется.

Протокол UDP не является надежным методом транспортировки данных, на самом деле неважно, получаете ли вы все свои исходные данные. Это может звучать ужасно, но у него есть свои возможности, например, для потоковой передачи мультимедиа, это нормально, если вы потеряете несколько кадров взамен, вы получите ваши данные немного быстрее.

<b>TCP</b>

TCP обеспечивает надежный поток данных, ориентированный на соединение. TCP использует порты для отправки данных на хосты и обратно. Приложение открывает соединение с одного порта на своем хосте на другой порт на удаленном хосте. Чтобы установить соединение, мы используем рукопожатие TCP.

<ul>
<li>Клиент (процесс подключения) отправляет сегмент SYN на сервер, чтобы запросить подключение</li>
<li>Сервер отправляет клиенту сегмент SYN-ACK, чтобы подтвердить запрос на соединение с клиентом</li>
<li>Клиент отправляет ACK на сервер, чтобы подтвердить запрос на подключение к серверу</li>
</ul>

Как только это соединение установлено, данные можно обменивать через TCP-соединение. Данные отправляются в разных сегментах и отслеживаются с порядковыми номерами TCP, чтобы они могли быть упорядочены в правильном порядке, когда они доставляются. В нашем примере электронной почты транспортный уровень присоединяет порт назначения (25) к исходному порту исходного узла.

## Задание

Нет задания для этого урока.

## Вопрос

Какой транспортный протокол считают надежным?

## Ответ

TCP
