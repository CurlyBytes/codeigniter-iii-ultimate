Composer --dev ======== is for installation as not requried when somebody else is using your code or library
Composer --no-dev ========= remove the library as part of required dependency

composer create-project kenjis/codeigniter-composer-installer --no-dev --remove-vcs // need to add no-dev to not install the dependency of the project from kenji and remove vcs its because i have already existing app

php composer.phar validate --with-dependencies //before you tag a release. It will check if your composer.json is valid: Also validate the composer.json of all installed dependencies.

for CI3 phpunit best setup use the following:
composer require kenjis/ci-phpunit-test --dev
php vendor/kenjis/ci-phpunit-test/install.php --from-composer //https://github.com/kenjis/ci-phpunit-test


composer dump-autoload
php composer.phar status
php composer.phar self-update



major installation or first
composer create-project laravel/laravel --prefer-dist --profile --verbose

major changes or update
composer update --dry-run --profile --verbose


patch only
$ composer require monolog/monolog:>1.18.0 -o

stable minor or 1 up higher of the current
composer require monolog/monolog:~1.18.0 -o

latest stable minor
composer require monolog/monolog:^1.18.0 -o
referrence
https://nomadphp.com/blog/11/Five-Composer-Tips-Every-PHP-Developer-Should-Know
https://www.droptica.com/blog/10-tricks-work-efficiently-composer-drupal-8/


CI should have everyday build per application , and the library should be install specific version



search about https://packagist.org/packages/phpcompatibility/php-compatibility this package on proper usage
--
 show                   Shows information about packages.
  status                 Shows a list of locally modified packages, for packages installed from source.
  suggests               Shows package suggestions.
  test                   Launches the preconfigured PHPUnit
  update-package         Runs the update-package script as defined in composer.json.
  upgrade                Upgrades your dependencies to the latest version according to composer.json, and updates the composer.lock file.
  validate               Validates a composer.json and composer.lock.
  why                    Shows which packages cause the given package to be installed.
  why-not                Shows which packages prevent the given package from being installed.
  run-script             Runs the scripts defined in composer.json.
  search                 Searches for packages.
  self-update            Updates composer.phar to the latest version.
  selfupdate             Updates composer.phar to the latest version.
    about                  Shows the short information about Composer.
  archive                Creates an archive of this composer package.

search position it job works
-- if else statement in CI ( azure yaml or travis CI)
   "phpcs-src": "vendor\\bin\\phpcs",
    "phpcs-tests": "vendor\\bin\\phpcs --runtime-set testVersion 5.6 tests\\phpunit\\",
    "phpcs": [
      "@phpcs-src",
      "@phpcs-tests"
    ],
    "test-unit": "vendor\\bin\\phpunit --testsuite unit",
    "test-integration": "vendor\\bin\\phpunit --testsuite integration"


pattern to create new project on composer composer create-project laravel/laravel --prefer-dist --profile --verbose

---
To install phpunit
- https://phpunit.de/getting-started-with-phpunit.html
- to resolve issue in phpunit to run in CI3  https://stackoverflow.com/questions/43188374/update-phpunit-xampp
- composer filename php -s localhost:2004
- review the phpunit setup and the comment tags for proper execution
https://phpunit.readthedocs.io/en/8.5/textui.html
- add markdown magics tips and tricks https://github.com/davidwells/markdown-magic
- add unit test, integration test, load test , api test and ui test
- fix the suggest scripts in the composer
- refactor composer to compliant to all os(linux, windows and mac)
--- Future check
must check doctrine implementation
https://github.com/FriendsOfPHP/security-advisories/tree/master/codeigniter/framework
https://github.com/kenjis/php-code-benchmarks
https://packagist.org/packages/phpbench/phpbench
https://github.com/webdevops/php-docker-boilerplate
https://github.com/VisualPHPUnit/VisualPHPUnit
https://github.com/chriskacerguis/codeigniter-restserver
https://github.com/siriusphp/validation
https://packagist.org/packages/tan5en5/codeigniter-debugbar
https://packagist.org/packages/fzaninotto/faker
https://github.com/kenjis/codeigniter-composer-installer/blob/master/composer.json
https://packagist.org/packages/kriswallsmith/assetic
https://github.com/Tan5en5/codeigniter-debugbar
https://github.com/php-middleware/phpdebugbar
https://github.com/avenirer/codeigniter-matches-cli
https://www.alibabacloud.com/blog/automating-your-php-application-deployment-with-php-deployer_594654
https://github.com/bcit-ci/codeigniter3-translations