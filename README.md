# [JSON Pretty Print Formatter for Monolog](http://github.com/skyzyx/monolog-json-pretty-print-formatter)

A variation of the [Monolog](https://github.com/Seldaek/monolog) `JsonFormatter` class which pretty-prints the JSON output. The API for this class is 100% backwards-compatible with `JsonFormatter`.


## Requirements
### Required
The following software is **required** for JSON Pretty Print Formatter for Monolog to run:

* [PHP] 5.4.0+


## Examples

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

### Bundle with Composer (recommended!)
To add JSON Pretty Print Formatter for Monolog as a [Composer] dependency in your `composer.json` file:

```json
{
    "require": {
        "skyzyx/monolog-json-pretty-print-formatter": ">=1.0"
    }
}
```

And include it in your scripts:

```php
require_once 'vendor/autoload.php';
```

## Contributing
To view the list of existing [contributors](/skyzyx/monolog-json-pretty-print-formatter/graphs/contributors), run the following command from the Terminal:

```bash
git shortlog -sne --no-merges
```

### How?
Here's the process for contributing:

1. Fork JSON Pretty Print Formatter for Monolog to your GitHub account.
2. Clone your GitHub copy of the repository into your local workspace.
3. Write code, fix bugs, and add tests with 100% code coverage.
4. Commit your changes to your local workspace and push them up to your GitHub copy.
5. You submit a GitHub pull request with a description of what the change is.
6. The contribution is reviewed. Maybe there will be some banter back-and-forth in the comments.
7. If all goes well, your pull request will be accepted and your changes are merged in.


## Authors, Copyright & Licensing

* Copyright (c) 2014 [Ryan Parman](http://ryanparman.com).

See also the list of [contributors](/skyzyx/monolog-json-pretty-print-formatter/contributors) who participated in this project.

Licensed for use under the terms of the [MIT] license.

  [PHP]: http://php.net
  [Composer]: https://getcomposer.org
  [MIT]: http://www.opensource.org/licenses/mit-license.php
  [Apache 2.0]: http://opensource.org/licenses/Apache-2.0
