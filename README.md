# Implementing Spatie's Permissions package into Inertia Laravel project (React).

Easy to use package to implement Spatie's Permissions package into Inertia Laravel project.

## Installation

You can install the package via composer:

```bash
composer require toohard2explain/laravel-inertia-permissions-react
```

You can publish and run the migrations with

```bash
php artisan migrate
```

Add the following to your vite.config.js file

```js
resolve: {
    alias: {
        '@laravel-inertia-permissions-react': 'vendor/toohard2explain/laravel-inertia-permissions-react/resources/js'
    }
}
```

Optionally, you can add the following to your jsconfig.json file:
```json
{
    "compilerOptions": {
        "paths": {
            "@laravel-inertia-permissions-react/*": ["./vendor/toohard2explain/laravel-inertia-permissions-react/resources/js/*"]
        }
    }
}
```

[//]: # (Optionally, you can publish the views using)

[//]: # ()
[//]: # (```bash)

[//]: # (php artisan vendor:publish --tag=":package_slug-views")

[//]: # (```)

## Usage

Permissions and Roles are automatically Shared with Inertia.
You can access them in your Vue components like this:

```js
import usePermissions from '@laravel-inertia-permissions-react/hooks/usePermissions.js';

const { can, is } = usePermissions()

if (can('edit articles')) {
    // do something
}

if (is('writer')) {
    // do something
}
```


## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.
