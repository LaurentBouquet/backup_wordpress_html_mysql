# backup_wordpress_html_mysql

## Docker run

docker run -d --name demo-wordpress-backup --hostname demo-backup --link demo-mysql --restart=always -v demo_wordpress_html:/var/www/html -v demo_wordpress_docs:/var/www/documents -v demo_wordpress_custom:/var/www/html/custom -v demo_wordpress_conf:/var/www/html/conf -v /etc/localtime:/etc/localtime:ro -v /home/backup:/backup -e "MYSQL_ROOT_PASSWORD=aSecurePassword" -e "MYSQL_DATABASE=wordpress" -e "DOLIBARR_CONTAINER_NAME=demo-wordpress" -e "MYSQL_CONTAINER_NAME=demo-mysql" lbouquet/backup_wordpress_html_mysql:latest crond -f -d 8 

## Docker compose

TODO

