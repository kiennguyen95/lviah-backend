# Lviah
Let's make Haivl great again.

## Setup
- Download and install a local server environment such as [XAMPP](https://www.apachefriends.org/) or [MAMP](https://www.mamp.info/)
- Setting [a virtual host](https://dev.to/crankysparrow/configuring-virtual-hosts-with-mamp-f3i) if you want a prettier local domain

## Installation
1. Clone project

2. Run `composer install` to install all dependencies

3. Change database info at the end of `web/sites/default/settings.php` to yours

4. Access the site in your browser and follow the setup instructions

5. Synchronize configuration by running the following commands:
    - `./vendor/bin/drush cset system.site uuid "fbd76dc7-4c21-4df4-8158-b88ac63678ee" `
    - `./vendor/bin/drush ev '\Drupal::entityTypeManager()->getStorage("shortcut_set")->load("default")->delete();'`
    - `./vendor/bin/drush cim`

