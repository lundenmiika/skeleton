## Install Skeleton files

composer clearcache && COMPOSER_MEMORY_LIMIT=-1 composer update pimcore/pimcore

## Run install script

rm -rf my-project && composer clearcache && COMPOSER_MEMORY_LIMIT=-1 composer create-project --repository-url=./packages.json pimcore/skeleton my-project
cd ./my-project
./vendor/bin/pimcore-install

## Add installer.yml to my-project/app/config/installer.yml

```
pimcore_install:
  parameters:
    database_credentials:
      user: "project_user"
      password: "PASSWORD"
      dbname: "project_database"
      host: "127.0.0.1"
      port: "3305"
```
