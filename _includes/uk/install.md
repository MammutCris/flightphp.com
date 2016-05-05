# Установка

### 1. Завантаження файлів.

Якщо ви використовуєте [Composer](https://getcomposer.org/), ви можете завантажити командою:

```
composer require mikecao/flight
```

АБО ви можете [завантажити](https://github.com/mikecao/flight/archive/master.zip) архів.

### 2. Налаштування веб-сервера.

Для _Apache_, пропишіть у ваш `.htaccess` файл ці рядки:

``` apache
RewriteEngine On
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule ^(.*)$ index.php [QSA,L]
```

Для _Nginx_, добавте цей текст у файл налаштування сервера:

``` nginx
server {
    location / {
        try_files $uri $uri/ /index.php;
    }
}
```

### 3. Створіть`index.php` файл.

Спочатку підключаємо фреймворк.

``` php?start_inline=1
require 'flight/Flight.php';
```

Якщо ви використовуєте Composer, підключіть автозапуск.

``` php?start_inline=1
require 'vendor/autoload.php';
```

Потім пропишіть маршрут та напишіть просту функцію яка буде виконуватись при переході за адресою.

``` php?start_inline=1
Flight::route('/', function(){
    echo 'hello world!';
});
```

І на завершення запустіть фреймворк.

```php
Flight::start();
```