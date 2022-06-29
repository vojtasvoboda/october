# website.com

https://www.website.com

## Requirements

- PHP 7.4 (max PHP 8.0)
- MySQL 5.7 or MariaDB 10.2

Run `php -v`. When it prints some version higher than 7.4 it is Ok. Otherwise check tutorial:

http://blog.vojtasvoboda.cz/instalace-php-na-mac-os-x-mountain-lion

## Installation

1. Create .env file as copy of .env.example and fill each line.
2. Run `composer install`.
3. Create database and run database migrations by `php artisan october:migrate`.

## Run on localhost

1. Run local server by `php artisan serve`. Project should works at `http://localhost:8000/`.
2. Login to backend at `http://localhost:8000/backend` with admin/admin credentials.

## Run on production

1. Set environment to production at .env file (APP_ENV=production).
2. Set Error Logger plugin at backend.
3. Remove admin account and create your own.
4. Set mailing at Backend > Mail configuration.
5. Set mail templates text at Backend > Mail templates
    - **rainlab.user::mail.activate** is sent after registration
    - **rainlab.user::mail.welcome** after successfull account confirmation
