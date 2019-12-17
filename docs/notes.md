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


---
To install phpunit
- https://phpunit.de/getting-started-with-phpunit.html
- to resolve issue in phpunit to run in CI3  https://stackoverflow.com/questions/43188374/update-phpunit-xampp
- composer filename php -s localhost:2004
- review the phpunit setup and the comment tags for proper execution
https://phpunit.readthedocs.io/en/8.5/textui.html   
- add markdown magics tips and tricks https://github.com/davidwells/markdown-magic

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