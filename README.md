# website.cz

https://www.website.cz

## Requirements

- PHP 7.0.0.
- MySQL 5.7.x or compatible MariaDb.

Run `php -v`. When it prints some version higher then 7.0.0 it is Ok. Otherwise check tutorial:

http://blog.vojtasvoboda.cz/instalace-php-na-mac-os-x-mountain-lion

## Installation

1. Create .env file as copy of .env.dist and fill each line. Ask me for encryption key and cipher!
2. Run `composer install`.
3. Create file `/config/dev/app.php` with content `<?php return ['debug' => true];` to set up debug mode.
4. Create database and run database migrations by `php artisan october:up`.

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
