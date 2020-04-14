# monolog-discord-handler

A simple monolog handler for support Discord webhooks

-------------------------------------------------

### Dependecies

- PHP ^7.2
- Monolog ~2

-------------------------------------------------

## 1. Installing

Easy install via composer. Still no idea what composer is? Inform yourself [here](http://getcomposer.org).

```composer require den1008/monolog-discord-handler```

-------------------------------------------------

## 2. Usage

Push this handler to your monlog instance:

### Only one webhooks url

```php
<?php
require 'vendor/autoload.php';

$log = new Monolog\Logger('your name');

$log->pushHandler(new DiscordHandler\DiscordHandler('Discord Webhook url', 'name', 'subname', 'DEBUG'));

```

### Many webhooks url


```php
<?php
require 'vendor/autoload.php';

$log = new Monolog\Logger('your name');

$log->pushHandler(new DiscordHandler\DiscordHandler([
'Discord Webhook url 1',
'Discord Webhook url 2',
], 'name', 'subname', 'DEBUG'));

```
