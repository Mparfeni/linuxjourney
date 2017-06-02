# Сетевой менеджер

## Содержание урока

Конечно, если вы хотите, чтобы ваша система автоматически работала и работала, в системе для этого уже есть что-то. Большинство дистрибутивов используют демона NetworkManager для автоматической настройки своих сетей.

Вы увидите NetworkManager в виде апплета где-то на панели задач вашего рабочего стола, если вы используете графический интерфейс. Как вы можете видеть, он управляет оборудованием и информацией о вашем подключении. Например, при запуске NetworkManager будет собирать информацию о сетевом оборудовании, искать подключения к беспроводной сети, проводной и т. Д., А затем активировать ее.

Есть также инструменты командной строки для взаимодействия с NetworkManager:

<b>nm-tool</b>

Отчеты nm-tools сообщают о состоянии NetworkManager и его устройствах

<pre>
pete@icebox:/$ nm-tool
NetworkManager Tool

State: connected (global)

- Device: eth0  [Wired connection 1] -------------------------------------------
  Type:              Wired
  Driver:            pcnet32
  State:             connected
  Default:           yes
  HW Address:        12:3D:45:56:7D:CC

  Capabilities:
    Carrier Detect:  yes

  Wired Properties
    Carrier:         on

  IPv4 Settings:
    Address:         192.168.22.1
    Prefix:          24 (255.255.255.0)
    Gateway:         192.168.22.2

    DNS:             192.168.22.2
</pre>

<b>nmcli</b>

Команда nmcli позволяет вам управлять и изменять NetworkManager, см. Man-страницу для получения дополнительной информации.

## Задание

Нет задания для этого урока.

## Вопрос

Какова команда для просмотра информации NetworkManager?

## Ответ

nm-tool