
## Insalll Yii2

- Install following tools

    https://git-scm.com/download/win\
    https://docs.docker.com/desktop/windows/install/

- `git clone https://github.com/royalscouts/yii2-app-advanced`

- `docker-compose up -d`

- `docker-compose logs -f`

- `docker-compose run --rm backend composer install`

- `docker-compose run --rm backend php ./init`

- edit ./common/config/main-local.php

         'dsn' => 'mysql:host=mysql;dbname=yii2advanced',
         'username' => 'yii2advanced',
         'password' => 'secret',

- `docker-compose run --rm backend yii migrate`

____



- to create new migration script:\
`docker-compose run --rm backend yii migrate/create migration_script_name`


-  Yii2/Docker guide\
    https://www.yiiframework.com/doc/guide/2.0/en/tutorial-docker