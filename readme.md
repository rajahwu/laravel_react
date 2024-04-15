# Laravel React

[laravel docs inertia](https://laravel.com/docs/11.x/frontend#inertia)

[inertia js](https://inertiajs.com/)

[inertia laravel react demo](https://github.com/Landish/pingcrm-react)

## [Installation](https://bootcamp.laravel.com/inertia/installation)

Create new laravel project

```bash
    composer create-project laravel/laravel chirper
```

Update database credentials and config

```txt
DB_CONNECTION=pgsql
DB_HOST=127.0.0.1
DB_PORT=5433
DB_DATABASE=laravel
DB_SCHEMA=react
DB_USERNAME=[username]
DB_PASSWORD=[password]
```

```php
# config/database.php

...
   'pgsql' => [
            'driver' => 'pgsql',
            'url' => env('DB_URL'),
            'host' => env('DB_HOST', '127.0.0.1'),
            'port' => env('DB_PORT', '5432'),
            'database' => env('DB_DATABASE', 'laravel'),
            'username' => env('DB_USERNAME', 'root'),
            'password' => env('DB_PASSWORD', ''),
            'charset' => env('DB_CHARSET', 'utf8'),
            'prefix' => '',
            'prefix_indexes' => true,
            'search_path' => env('DB_SCHEMA', 'public'), # <-- Change this line
            'sslmode' => 'prefer',
        ],

...

```

Run migrations and start server

```bash
    cd chirper
    php artisan migrate: fresh
    php artisan serve
```

View site at [http://127.0.0.1:8000/](http://127.0.0.1:8000/)

![laravel installation home page](./assets/images/laravel-installation.png)

## User Authentications with Breeze

```bash
    composer require laravel/breeze --dev
 
    node --version # use node version 18+

    php artisan breeze:install react

    npm run dev
```

Visit [http://127.0.0.1:8000/register](http://127.0.0.1:8000/register)
Register a new user

[breeze registration page](./assets/images/breeze-registration.png)

## crud

### [create](https://bootcamp.laravel.com/inertia/creating-chirps)

### [read](https://bootcamp.laravel.com/inertia/showing-chirps)

### [update](https://bootcamp.laravel.com/inertia/editing-chirps)

### [delete](https://bootcamp.laravel.com/inertia/deleting-chirps)

## [notification and events](https://bootcamp.laravel.com/inertia/notifications-and-events)
