# laravel-sendgrid-driver
====

A Mail Driver with support for Sendgrid Web API, using the original Laravel API.
This library extends the original Laravel classes, so it uses exactly the same methods.

To use this package required your [Sendgrid Api Key](https://sendgrid.com/docs/User_Guide/Settings/api_keys.html).
Please make it [Here](https://app.sendgrid.com/settings/api_keys).

# Install (Laravel5.2~)

Add the package to your composer.json and run composer update.
```json
"require": {
    "io-digital/laravel-sendgrid-driver": "^1.0"
},
```

or installed with composer
```
$ composer require io-digital/laravel-sendgrid-driver
```

Remove the default service provider and add the sendgrid service provider in app/config/app.php:
```php
'providers' => [
//  Illuminate\Mail\MailServiceProvider::class,

    IoDigital\SendGridDriver\MailServiceProvider::class,
];
```

#Configure

.env
```
MAIL_DRIVER=sendgrid
SENDGRID_API_KEY='YOUR_SENDGRID_API_KEY'
```

config/service.php
```
    'sendgrid' => [
        'api_key' => env('SENDGRID_API_KEY')
    ]
```