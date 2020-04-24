# Модуль оплаты beGateway для ReadyScript

## Системные требования

* PHP 5.4+
* [cURL](http://php.net/manual/en/book.curl.php)
* [ReadyScript](https://readyscript.ru/) (модуль совместим ReadyScript 3/4/5)

## Установка

1. [Скачайте begateway.zip](https://github.com/beGateway/readyscript-payment-module/blob/master/begateway.zip?raw=true)
2. Зайдите в панель администратора ReadyScript
3. Через меню _Веб-сайт_ перейдите в _Настройка модулей_
4. Установите модуль
  1. Нажмите кнопку _добавить модуль_
  2. Выберите файл архива модуля, скаченного на шаге 1
  3. Нажмите _Далее_ и наследующей странице _Установить_, чтобы установить модуль
  4. Перейдите в настройки модуля _BeGateway_ и включите его

## Настройка модуля

1. Зайдите в панель администратора ReadyScript
2. Зайдите в настройки способов оплаты _Магазин_ -> _Способы оплаты_
3. Нажмите _Добавить способ оплаты_ и перейдите к добавлению нового способа оплаты
4. Настройте модуль
  1. Задайте название способа оплаты
  2. Найдите параметр _Расчетный класс (тип оплаты)_
  3. Выберите _BeGateway_ в выпадающем списке
  4. Нажмите _сохранить и закрыть_
5. Опубликуйте способ оплаты
  1. Выберите настроенный способ оплаты в списке доступных способов оплаты
  2. Опубликуйте его, кликнув на переключатель в колонке _Видим_

## Тестовые данные

Если вы настроите модуль со следующими значениями

  * Домен страницы оплаты __checkout.begateway.com__
  * Id магазина __361__
  * Секретный ключ магазина __b8647b68898b084b836474ed8d61ffe117c9a01168d867f24953b776ddcb134d__

то вы сможете уже осуществить тестовый платеж в вашем магазине.

Используйте следующие данные тестовой карты:

  * номер карты __4200000000000000__
  * имя на карте __JOHN DOE__
  * срок действия карты __01/30__, чтобы получить успешный платеж
  * срок действия карты __10/30__, чтобы получить неуспешный платеж
  * CVC __123__

## Для разработчиков

Для запуска docker-контейнера и установки ReadyScript создайте в hosts-файле машины docker-хоста запись:

```
0.0.0.0 readyscript5.local
```
