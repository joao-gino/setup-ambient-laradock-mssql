# setup-ambient-laradock-mssql
In this repository exists a tutorial that teach how to setup a dev ambient with laradock and SQL Server

# Laradock with SQL Server!

Start the container with the images what you want

    docker-compose up -d nginx mssql

After this, enter the workspace bash

    docker-compose exec workspace bash

Create your project with 'composer create-project' and edit your .env file

    DB_CONNECTION=sqlsrv
    DB_HOST=mssql
    DB_PORT=1433
    DB_DATABASE=your-database-name
    DB_USERNAME=sa
    DB_PASSWORD=your-password

Ok, now you need to install sudo and sqlsrv drivers

    apt-get update
    apt-get -y install sudo

    sudo apt-get install freetds-common freetds-bin unixodbc php-sybase

> (if you have other version of php, use 'php7.1-sybase' and switch the
> '7.1' to your version.

Now you have access to your database, congrats!
