mysql things


    docker exec -it mariadb /bin/bash

    root@51456cc41fb2:/# mysql -p$MYSQL_ROOT_PASSWORD -u root

    MariaDB [(none)]> CREATE DATABASE blog; CREATE DATABASE blog2;

    MariaDB [(none)]> CREATE USER 'blog' IDENTIFIED BY 'hallo123';

    MariaDB [(none)]> CREATE USER 'blog2' IDENTIFIED BY 'hallo123';

    docker run --name blog2-wordpress -e WORDPRESS_DB_HOST=mariadb -e WORDPRESS_DB_USER=blog2 -e WORDPRESS_DB_PASSWORD=hallo123 -e    WORDPRESS_DB_CHARSET=utf8mb4 -e   WORDPRESS_DB_COLLATE=utf8mb4_unicode_ci -e WORDPRESS_DB_NAME=blog2 -p    127.0.0.1:10001:80 --link mariadb:mariadb -v /var/www/blog2.local/  public:/var/www/html --restart=always -d wordpress:5.1.1