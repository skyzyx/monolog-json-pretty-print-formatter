# JSON Pretty Print Formatter for Monolog

A variation of the [Monolog](https://github.com/Seldaek/monolog) `LineFormatter` class which pretty-prints the JSON output. The API for this class is 100% backwards-compatible with `LineFormatter`.

## Usage

```php
use Monolog\Handler\StreamHandler;
use Monolog\Logger;
use Skyzyx\Monolog\Formatter\JsonPrettyPrintFormatter;

$logger = new Logger('AwesomeSauce');
$handler = new StreamHandler('/var/log/awesomesauce.log', Logger::DEBUG);
$handler->setFormatter(new JsonPrettyPrintFormatter());
$logger->pushHandler($handler);
```

## Installation

https://packagist.org/packages/skyzyx/monolog-json-pretty-print-formatter

## Requirements

Since this leverages the `JSON_PRETTY_PRINT` constant as a parameter for the `json_encode()` function made available in PHP 5.4+, you cannot use this with earlier versions.
