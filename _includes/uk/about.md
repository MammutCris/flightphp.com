# Що таке Flight?

Flight це швидкий, простий і гнучкий фреймворк на PHP.
Flight дозволяє швидко та легко створювати веб-додатки з використанням RESTful.

``` php?start_inline=1
require 'flight/Flight.php';

Flight::route('/', function(){
  echo 'hello world!';
});

Flight::start();
```

[Детальніше]({{page.lang|prepend:'/'|replace:'/.',''}}/learn)

# Вимоги

Flight потребує PHP 5.3 чи вище.

# Ліцензія

Flight створений під ліцензією [MIT](https://github.com/mikecao/flight/blob/master/LICENSE).

# Допомога у розвитку

Цей сайт знаходиться у [Github](https://github.com/mikecao/flightphp.com).
Запрошуємо вас допомогти у розвитку та перекладі.