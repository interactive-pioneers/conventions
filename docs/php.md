# PHP Coding Conventions

## Coding Style

We follow the [PSR-2](http://www.php-fig.org/psr/psr-2/) coding standard and the [PSR-4](http://www.php-fig.org/psr/psr-4/) autoloading standard.

## Linters

Use `$ php -l FILENAME` ([more](http://www.php.net/manual/en/features.commandline.options.php)) and [PHPCS](https://github.com/squizlabs/PHP_CodeSniffer) with PSR-2 configuration:
```
$ phpcs --standard=PSR2 FILENAME
```

### Linter Plugins

__Sublime Text:__
- [SublimeLinter-php](https://github.com/SublimeLinter/SublimeLinter-php)
- [SublimeLinter-phpcs](https://github.com/SublimeLinter/SublimeLinter-phpcs)

__Atom:__
- [AtomLinter/linter-php](https://github.com/AtomLinter/linter-php)
- [AtomLinter/linter-phpcs](https://github.com/AtomLinter/linter-phpcs)

## Documentation

There is no need for code documentation as long as descriptive method names are used in combination with parameter and output type hinting.
