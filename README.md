PHP SDK для работы с XML API Mobile Active
==========================================

Для работы с XML API сервиса СМС-рассылок Mobile Active
вам необходимо иметь логин и пароль в указанном сервисе, 
для получения логина и пароля пройдите регистрацию на сайте [компании Мобильный Актив](http://mobak.ru)

Установка
-----------------

Для установки пакета используйте composer:

`composer require "grigorieff/mobak-php-xml-sdk" "1.0.*"`

или в файле composer.json в require-зависимости добавить:

```
{
  "require" : {
    "grigorieff/mobak-php-xml-sdk" : "1.0.*"
  }
}
```

Использование
----------------------------

Пример отправки СМС-сообщения:

```php
use Mobak;

$smsSender = new Mobak([
    'login' => 'YOUR_LOGIN',
    'password' => 'YOUR_PASSWORD',
])

$smsSender->send([
    'message' => "Your message text",
    'sender' => "Info",
    'phone' => '79194839xxx'
]);

```










