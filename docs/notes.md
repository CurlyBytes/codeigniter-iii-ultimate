Composer --dev ======== is for installation as not requried when somebody else is using your code or library
Composer --no-dev ========= remove the library as part of required dependency

composer create-project kenjis/codeigniter-composer-installer --no-dev --remove-vcs // need to add no-dev to not install the dependency of the project from kenji and remove vcs its because i have already existing app

php composer.phar validate --with-dependencies //before you tag a release. It will check if your composer.json is valid: Also validate the composer.json of all installed dependencies.

for CI3 phpunit best setup use the following:
composer require kenjis/ci-phpunit-test --dev
php vendor/kenjis/ci-phpunit-test/install.php --from-composer


composer dump-autoload
php composer.phar status
php composer.phar self-update