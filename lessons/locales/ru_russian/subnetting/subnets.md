# Подсети

## Содержание урока

Как я могу узнать, нахожусь ли я в той же сети, что и Пэтти? Ну, мы можем просто посмотреть на подсеть, короткую для подсети. Подсеть представляет собой группу хостов с IP-адресами, которые подобным образом определенным образом. Эти хосты обычно находятся в непосредственной близости друг от друга, и вы можете легко отправлять данные на хосты и из них в одной и той же подсети. Думайте об этом как о отправке почты в том же почтовом индексе, это намного проще, чем отправка почты в другое состояние.

Например, все хосты с IP-адресом, который начинается с 123.45.67, будут находиться в одной подсети. Мой хост имеет IP-адрес 123.45.67.8, а Patty's имеет IP-адрес 123.45.67.9. Общие номера - это мой сетевой префикс, а 8 и 9 - наши хосты, поэтому моя сеть такая же, как и у Patty's. Подсете делится на сетевой префикс, такой как 123.45.67.0 и маска подсети.

<b>Маски подсети</b>

Маски подсети определяют, какая часть вашего IP-адреса является частью сети и какая часть является частью хоста.

Типичная маска подсети может выглядеть примерно так:

<pre> 255.255.255.0 </pre>

Часть 255 на самом деле является нашей маской. Чтобы сделать это немного легче понять, помните, как мы обращаемся к каждому октету как к восьми битам? В информатике бит обозначается 0 или 1 в двоичной форме. Когда используются двоичные числа, 1 означает, что вкл., А 0 означает выключение. Итак, что равняется 8 0 или 1?

Перенесите в Google «двоичный в десятичный калькулятор» и преобразуйте 11111111 в десятичную форму. Что вы получаете? 255! Таким образом, октет находится в диапазоне от 0 до 255. Итак, если мы имели маску подсети 255.255.255.0 и IP-адрес 192.168.1.0, сколько хостов находится в этой подсети? Мы найдем ответ на этот вопрос в нашем уроке математики в подсети.

Также, когда мы говорим о нашей подсети, мы обычно обозначаем ее сетевым префиксом, за которым следует маска подсети:

<pre>123.234.0.0/255.255.0.0</pre>

<b>Почему?</b>

Зачем нам нужны подсети? Подсети используются для сегментирования сетей и управления потоком трафика в этой сети. Таким образом, хост в одной подсети не может взаимодействовать с другим хостом в другой подсети.

Но подождите минуту, что, если я хочу подключиться к другим хостам, таким как yahoo.com? Затем вам нужно соединить подсетей вместе. Для подключения подсетей вам просто нужно найти хосты, которые подключены к нескольким подсетям. Например, если мой хост на 192.168.1.129 подключен к локальной сети 192.168.1.129/24, он может достигнуть любого хоста в этой сети. Чтобы добраться до хостов в остальной части Интернета, ему необходимо связаться через маршрутизатор. Традиционно в большинстве сетей с маской подсети 255.255.255.0 маршрутизатор обычно находится по адресу 1 подсети, поэтому 192.168.1.1. Теперь маршрутизатор будет иметь порт, который соединяет его с другой подсетью (больше в курсе маршрутизации). Некоторые IP-адреса (частные сети) не видны в Интернете, и у нас есть такие вещи, как NAT (подробнее об этом позже).

## Задание

Используйте ifconfig для просмотра маски подсети.

## Вопрос

Правда или неправда, что подсеть состоит из маски подсети и сетевого префикса.

## Опросник

Правда
