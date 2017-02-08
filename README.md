# mix-funciton
Mix function to render versioned assetes outside Laravel project

## Instalation
First install Laravel Mix [https://github.com/JeffreyWay/laravel-mix](https://github.com/JeffreyWay/laravel-mix)

Then add this this line in your require section

```
"require": {
    "ibox/mix-function": "~1.0"
}
```
Then run:
```
composer install
```

Optionally you can run

```
composer dump-autoload
```

## Configuration
If you you have a public directory, you can configure laravel mix as follow
```
mix.setPublicPath('public');
mix.sass('resources/assets/sass/app.sass', 'public/css').version();
```

## Usage
Require composer autoload

```
require '../vendor/autoload.php';
```

Then in your HTML you can use mix function like this:

```
<link href="<?= mix('/css/app.css', __DIR__) ?>" rel="stylesheet">
```




