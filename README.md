![Slynova](https://cloud.githubusercontent.com/assets/2793951/8206037/35841f80-14f6-11e5-8538-b378cd632d28.png)


# unmaintained fork of slynova-org/laravel-commentable
### v1.0.1 hash in composer.lock was at e6717ea12d74d02d7b8389b24a9631d932035000 when downloaded

to **Override the Repo** which composer pulls from you will need to add the repository override to your projects composer.json file:

```
"repositories": [
        {
            "type": "vcs",
            "url": "https://github.com/gitBC/laravel-commentable"
        }
    ],
```
then run

```
	$composer update slynova/laravel-commentable
```

# Laravel-Commentable

[![License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](https://tldrlegal.com/license/mit-license)
[![Total Downloads](https://img.shields.io/packagist/dt/slynova/laravel-commentable.svg?style=flat-square)](https://packagist.org/packages/slynova/laravel-commentable)

Laravel Commentable adds polymorphic threaded comments to Laravel 5.1 and above.

This package use Nested Set pattern with [Baum](https://github.com/etrepat/baum).<br>
[More information about Nested Set](http://en.wikipedia.org/wiki/Nested_set_model)

# Table of Contents

* [Requirements](#requirements)
* [Getting Started](#getting-started)
* [Example](#example)
* [Change Logs](#change-logs)
* [Contribution Guidelines](#contribution-guidelines)

# <a name="requirements"></a>Requirements

* As Laravel 5.1 require PHP 5.5.9+, we required the same version.

# <a name="getting-started"></a>Getting Started

0. PLEASE NOTE, this is a fork for version 1.0.1

	```
    "require": {
        "slynova/laravel-commentable": "^1.0.1"
	}
	```

1. Require the package with [Composer](https://getcomposer.org).
    ```shell
    $ composer require slynova/laravel-commentable
    ```


2. Add the package to your application service providers in `config/app.php`.
    ```php
    'providers' => [

        Illuminate\Foundation\Providers\ArtisanServiceProvider::class,
        Illuminate\Auth\AuthServiceProvider::class,
        ...
        Slynova\Commentable\ServiceProvider::class,

    ],
    ```

3. Publish the package's migrations to your application and migrate.
    ```shell
    $ php artisan vendor:publish --provider="Slynova\Commentable\ServiceProvider" --tag="migrations"
    $ php artisan migrate
    ```

# <a name="example"></a>Example

You can find an usage example of this package in the [laravel-commentable-example](https://github.com/Slynova-Org/laravel-commentable-example) repository.

# <a name="change-logs"></a>Change Logs

Nothing has been changed from the first release.

# <a name="contribution-guidelines"></a>Contribution Guidelines

Support follows PSR-2 PHP coding standards, and semantic versioning.

-- Please report any issue you find in the issues page.
Pull requests are welcome. --
