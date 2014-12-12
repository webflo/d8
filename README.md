Drupal 8 Composer Example
=========================

- Drupal Core (/core without vendor)
- Drush

```
{
  "minimum-stability": "dev",
  "prefer-stable": true,
  "require": {
    "composer/installers": "dev-drupal-core",
    "drush/drush": "dev-master",
    "webflo/drupal": "*",

    "drupal/drupal-core": "dev-8.0.x-composer",
    "drupal/devel": "dev-8.x-1.x",
    "drupal/name": "dev-8.x-1.x"
  },
  "require-dev": {

  },
  "config": {
    "bin-dir": "bin/",
    "autoloader-suffix": "Drupal8"
  },
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/tstoeckler/installers.git"
    },
    {
      "type": "vcs",
      "url": "https://github.com/webflo/d8.git"
    },
    {
      "type": "vcs",
      "url": "https://github.com/webflo/drupal-core.git"
    },
        {
      "type": "vcs",
      "url": "https://github.com/webflo/drush.git"
    },
    {
      "type": "composer",
      "url": "http://drupal-packagist.webflo.io"
    }
  ],
  "extra": {
    "installer-paths": {
      "src/core": [
        "type:drupal-core"
      ],
      "src/modules/contrib/{$name}": [
        "type:drupal-module"
      ]
    }
  }
}
```
