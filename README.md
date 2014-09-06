# JSON Pretty Print Formatter for Monolog

A variation of the [Monolog](https://github.com/Seldaek/monolog) `LineFormatter` class which pretty-prints the JSON output.

## Usage

```php
use Monolog\Handler\StreamHandler;
use Monolog\Logger;
use Skyzyx\Monolog\Formatter\JsonPrettyPrintFormatter;

$logger = new Logger('AwesomeSauce');
$handler = new StreamHandler('/var/log/awesomesauce.log', Logger::DEBUG);
$formatter = new JsonPrettyPrintFormatter(null, null, true, true);
$handler->setFormatter($formatter);
$logger->pushHandler($handler);
```

## Installation

https://packagist.org/packages/skyzyx/monolog-json-pretty-print-formatter
