# laravel-backend-app

This project was maded to test Laravel backend api to manage `Clientes` model and consume it from React front-end project.

## Prerequisites

You need next things in your machine:
* LAMP (Apache2 and PHP8)
* PostgreSQL Driver for PHP (`php-pgsql` package, enable it in php.ini with this line: `extension=php_pgsql.so`)
* Run an instance of PostgreSQL with docker runnig next command:
    ```bash
    docker run -d --name postgresql -e POSTGRES_USER=pgsql -e POSTGRES_PASSWORD=s3cr3t -e POSTGRES_DB=example -p 5432:5432 postgres:14
    ```


## How to Scaffold this Project?

To generate the basic project structure and initial configuration, run next command:
```bash
composer create-project --prefer-dist laravel/laravel laravel-backend-app
```

## How to execute this project?

To execute this project, once PHP is configured with PostgreSQL... you need to make the database migrations and start up the server running next commands:
```bash
php artisan migrate
php artisan serve
```

> **NOTE:** a couple of commands was used to create the controller and the model for the `Clientes` entity such as:
> * model: `php artisan make:model Cliente -m`
> * controller: `php artisan make:controller ClienteController`