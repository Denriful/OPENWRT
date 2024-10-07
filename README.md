# Установка XRAY Reality клиента на OpenWRT

## Подготовительные шаги

1. Карта VISA выпущенная не в РФ

2. Оплатить зарубежный VPS хостинг

3. Установить на vps сервер XRAY и GUI (3x-ui самый популярный)

Некоторые хостинги предлагают 3x-ui в качестве дополнения (просто ставим галочку и будет установлен автоматически). Например - [my.friendhosting.net](https://my.friendhosting.net)

Инструкция по ручной установке - https://pikabu.ru/story/ne_wireguardom_edinyim_10649152?utm_source=linkshare&utm_medium=sharing&utm_campaign=mobile_native_share

### Дополнительные шаги после установки 3x-ui

Необходимо выбрать домен расположенный на вашем хостинге, под который будет маскироваться траффик. Для этого подключаемся к консоли vps и скачиваем утилиту - https://github.com/XTLS/RealiTLScanner

Далее с помощью этой утилиты сканируем подсеть и выбираем себе какой нибудь домен и прописываем его в настройках подключения клиента в 3x-ui (взамен дефолтного yahoo.com)

## Установка OpenWRT на роутер ASUS AX4200

https://openwrt.org/toh/asus/tuf-ax4200

прошивка - https://drive.google.com/drive/folders/1p8-cse5ZXldra5YbcHG5TddI8X-eZxNY

https://forum.openwrt.org/t/asus-tuf-ax4200-support/155738/241

## Установка клиента sing-box

opkg update && opkg install sing-box

## Правка конфигураций

Файлы приведены в каталоге etc

После правки необходимо включить сервис sing-box в автозагрузку и рестартануть сеть и файрфол:

service sing-box enable

service sing-box restart

service network restart

service firewall restart

## Полезные ссылки

https://habr.com/ru/articles/767458/

https://habr.com/ru/articles/767464/

https://krasovs.ky/2024/08/05/sing-box-bypass.html

https://github.com/savely-krasovsky/antizapret-sing-box

https://4pda.to/forum

