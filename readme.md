# Config

Simple package to handle PHP based configuration files.

### Install

```sh
composer require exan/config
```

### Usage

```php

/**
 * -- src
 * ---- config
 * ------ database.php
 * ---- index.php
 */

# src/config/database.php

return [
    'host' => 'localhost',
    'name' => 'my_database',
    'port' => 1337,
];

# src/index.php

$config = new Exan\Config\Config(__DIR__ . '/config');

$config->get('database.host', 'my-default-value'); // 'localhost'
```
