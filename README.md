
# laravel-sendgrid-driver

A mail driver with support for Sendgrid Web API, using the original Laravel API. This library extends the original Laravel classes, so it uses exactly the same methods.

Using this package requires a Sendgrid API key which may be generated [here](https://app.sendgrid.com/settings/api_keys).

# Install

Add the package to your `composer.json` and run `composer update`:

```json
"require": {
    "io-digital/laravel-sendgrid-driver": "^1.0"
},
```

Alternatively, install directly with composer:

```
$ composer require io-digital/laravel-sendgrid-driver
```

Remove the default service provider and add the sendgrid service provider in `app/config/app.php`:

```php
'providers' => [
    // Illuminate\Mail\MailServiceProvider::class,
    IoDigital\SendGridDriver\MailServiceProvider::class,
];
```

# Configure

Edit your `.env` file to include the following:

```
MAIL_DRIVER=sendgrid
SENDGRID_API_KEY='YOUR_SENDGRID_API_KEY'
```

And finally, edit your `config/service.php` file to include the following:

```php
'sendgrid' => [
    'api_key' => env('SENDGRID_API_KEY')
]
```
