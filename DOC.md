
## Insalll Yii2

- Install following tools

    - https://git-scm.com/download/win  
    - https://docs.docker.com/desktop/windows/install/
  - 

Execute these in command prompt to 

  - to download (clone) the project
  
     `git clone https://github.com/royalscouts/yii2-app-advanced`

  - to change the directory to 
   `yii-app-advanced` 

    `cd yii-app-advanced` 
  
  - to build and start docker container 
  
    `docker-compose up -d`

  - to view docker container logs 
    `docker-compose logs -f`

  - to install the dependancies   
    `docker-compose run --rm backend composer install`

  - to initiate the php project 
  
    //Important: select the `developer mode` .
    
    `docker-compose run --rm backend php ./init`

  - to set up to the SQL connection 
  
    `edit ./common/config/main-local.php`

         'dsn' => 'mysql:host=mysql;dbname=yii2advanced',
         'username' => 'yii2advanced',
         'password' => 'secret',

- to migrate the db and create database
  
   `docker-compose run --rm backend php ./yii migrate`

____
For reference only :
----

- to create new migration script:\
`docker-compose run --rm backend php ./yii migrate/create migration_script_name`


-  Yii2/Docker guide\
    https://www.yiiframework.com/doc/guide/2.0/en/tutorial-docker