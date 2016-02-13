# Instalación

Actualizar repositorio:

`sudo apt-get update`

Instalar **Apache**:

`sudo apt-get install apache2`

Comprobar funcionamiento Apache, introduciendo `localhost` en el navegador web:

![Funcionamiento Apache](http://i628.photobucket.com/albums/uu6/romilgildo/Apache_zpsx2vyhcsx.png)

Instalar **MySQL**:

`sudo apt-get install mysql-server php5-mysql`

Te pedirá una clave para el usuario root.

Asegurar MySQL:

```
sudo mysql_install_db
sudo mysql_secure_installation
```

Introduces la contraseña de usuario root, eliges si deseas cambiarla, y luego aceptas las siguientes preguntas pulsando ENTER.

Comprobar acceso a MySQL:

`mysql -u root -p`

![Funcionamiento MySQL](http://i628.photobucket.com/albums/uu6/romilgildo/MySQL_zpsdkydpois.png)

Instalar **PHP**:

```
sudo apt-get install php5 libapache2-mod-php5 php5-mcrypt
sudo php5enmod mcrypt
```

Crear fichero PHP de prueba:

`sudo nano /var/www/html/info.php`

Con el siguiente contenido:

```
<?php
phpinfo();
?>
```

Reiniciar Apache:

`sudo service apache2 restart`

Comprobar funcionamiento PHP, añadiendo `/info.php` al localhost en el navegador:

![Funcionamiento PHP](http://i628.photobucket.com/albums/uu6/romilgildo/PHP_zpsnpxptuzb.png)

Instalar **phpMyAdmin**:

`sudo apt-get install phpmyadmin`

Durante la instalación, elegimos apache2 como servidor, y configuramos la base de datos con dbconfig-common, introduciendo la password MySQL y la nueva para phpMyAdmin.

Reiniciar de nuevo Apache.

Comprobar funcionamiento phpMyAdmin, añadiendo `/phpmyadmin` al localhost en el navegador:

![Funcionamiento phpMyAdmin](http://i628.photobucket.com/albums/uu6/romilgildo/phpMyAdmin_zpsjkse9oml.png)

Instalar **Symfony**:

```
sudo curl -LsS https://symfony.com/installer -o /usr/local/bin/symfony`
sudo chmod a+x /usr/local/bin/symfony
```

En el directorio de proyectos PHP:

`sudo cp /usr/local/bin/symfony .`

Comprobar funcionamiento Symfony, ejecutando `php symfony`:

![Funcionamiento Symfony](http://i628.photobucket.com/albums/uu6/romilgildo/Symfony_zpsx7c4ecrl.png)
