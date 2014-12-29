# camunda-bpm-dropwizard-examples

## Log - what happened so far

### mysql instead of h2

Since I had trouble running multiple instances against a h2-server db, the example setup now uses mysql. To set up
the local instance, you can use the [EasyMysql](https://github.com/nkratzke/EasyMySQL) docker setup. On OSX and Windows, 
follow the installation directions of boot2docker, see EasyMysql/README.md.

Afterwards, before running the examples, start the mysql-db using


    cd camunda-bpm-dropwizard/examples
    docker run -d -p 3306:3306 -e user="camunda" -e password="camunda" -e right="WRITE" mysqldb


To admin the database without installing any additional software use [Adminer](http://www.adminer.org/de/), just
start a local php server running:

`php -S localhost:8000 adminer-4.1.0.php` 

and open the page in your browser. Connect with your `boot2docker ip` address and `user=camunda, password=camunda, db=camunda`. 


