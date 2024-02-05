# docker engin

# Apache
sudo docker run --name apa000ex2 -d -p 80:80 httpd


# Mariadb
sudo docker run --name mariadb000ex1 -p 8080:3306 -e MYSQL_ROOT_PASSWORD=myrootpass mariadb
sudo docker exec -i mariadb000ex1

