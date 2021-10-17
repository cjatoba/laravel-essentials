#Tutorial para configuração do bootstrap 5 em um projeto Laravel 8

You can install bootstrap manually and compile sass.

First, add it to npm with compilers:

```npm
npm install bootstrap
npm install sass
npm install sass-loader
```
Second, create (if not created) resources/sass/app.scss and add this:
```Javascript
@import '~bootstrap';
```

Third, add compilation in webpack.mix.js:

mix.sass('resources/sass/app.scss', 'public/css')

Than, compile it with npm dev - you see compiled file public/css/app.css

Now you can use it in templates with asset:

```php
<link href="{{ asset('css/app.css') }}" rel="stylesheet">
```

##Fonte

https://stackoverflow.com/questions/68393652/how-to-install-bootstrap-in-laravel-8