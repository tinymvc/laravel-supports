# Laravel Supports for TinyMVC/Spark

Laravel-inspired support classes and helpers, fine-tuned for
[TinyMVC / Spark](https://github.com/tinymvc).

## Installation

```bash
composer require tinymvc/laravel-supports
```

Requires PHP 8.2 or newer.

## Usage

```php
use Spark\Support\Arr;
use Spark\Support\Str;

$names = collect(['taylor', 'laravel'])
    ->map(fn (string $name) => Str::studly($name))
    ->all();

$value = Arr::get(['user' => ['name' => 'Taylor']], 'user.name');
```

The package provides:

- `Arr`, `Str`, `Number`, and `Pluralizer` utilities
- `Collection` and `LazyCollection`
- `Stringable`, `HtmlString`, and `Js`
- common helpers such as `collect`, `data_get`, `data_set`, `value`, and `tap`
- support contracts and reusable traits

Optional integrations are available for Markdown, ASCII conversion, UUIDs,
and pluralization. See `composer.json` for the supported packages.

## License

Released under the [MIT License](LICENSE.md).
