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
-