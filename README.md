Keeper
======

Asset Manager for Laravel 4


Setup
-------------------

composer.json:

Add `"turtlebits/keeper": "dev-master"` to the `require` section of `composer.json`

Register the service provider by adding `'TurtleBits\Keeper\KeeperServiceProvider',` to the `providers` section of the `app/config/app.php` file

If you use [TwigBridge](https://github.com/rcrowe/TwigBridge), add `'TurtleBits\Keeper\Extensions\KeeperTwigExtension'` to the `extensions` section of the `app/config/packages/rcrowe/twigbridge/config.php` file.


Requirements
-------------------

This package uses [lessphp](https://github.com/leafo/lessphp) as a `less` compiler, and installs it automatically.


Usage
-------------------

In Blade views:

{{ Keeper::style(array('application', 'structure')) }}
{{ Keeper::script(array('jquery', 'application')) }}
{{ Keeper::image('logo.jpg') }}

In Twig views:

```
{{ keeper_style(['application', 'structure'])|raw }}
{{ keeper_script(['jquery', 'application'])|raw }}
{{ keeper_image('logo.jpg') }}
```


TODO
-------------------
* Add css minification
* Add js minification
* Add css groups
* Add js groups
* Add basic image filters
* Add basic image transforms