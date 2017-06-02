# ICMP

## Содержание урока

Протокол управляющих сообщений Интернета (ICMP) является частью набора протоколов TCP/IP, он используется для отправки обновлений и сообщений об ошибках и является чрезвычайно полезным протоколом, используемым для отладки сетевых проблем, таких как сбой доставки пакетов.

Каждое сообщение ICMP содержит поле типа, кода и контрольной суммы. Поле типа является типом сообщения ICMP, код является подтипом и описывает дополнительную информацию о сообщении, а контрольная сумма используется для обнаружения любых проблем с целостностью сообщения.

Давайте рассмотрим некоторые общие типы ICMP:

<ul>
<li>Type 0 - Echo ответ</li>
<li>Type 3 - Пункт назначения недоступен</li>
<li>Type 8 - Echo запрос</li>
<li>Type 11 - Превышено время</li>
</ul>

Когда пакет не может добраться до адресата, генерируется сообщение 3 типа ICMP, в типе 3 есть 16 кодовых значений, которые далее описывают, почему он не может добраться до адресата:

<ul>
<li>Code 0 - Сеть недоступна</li>
<li>Code 1 - Хост недоступен</li>
и так далее...
</ul>

Эти сообщения будут иметь больший смысл, поскольку мы используем некоторые средства устранения сетевых неполадок.

## Задание

Нет задания для этого урока.

## Вопрос

Какой ICMP тип используется для echo запросов?

## Ответ

8