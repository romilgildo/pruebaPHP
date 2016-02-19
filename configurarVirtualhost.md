# Configuración del Virtualhost

Creamos el siguiente fichero:

`sudo nano /etc/apache2/sites-available/coches.com.conf`

Y le metemos el siguiente contenido:

```
<VirtualHost *:80>

	ServerAdmin admin@coches.com
	ServerName coches.com
	ServerAlias www.coches.com
	DocumentRoot /home/romilgildo/PHP/prueba-coches/web/

	<Directory />
    Options FollowSymLinks
    AllowOverride None
		Require all granted
	</Directory>

	ErrorLog ${APACHE_LOG_DIR}/error.log
	CustomLog ${APACHE_LOG_DIR}/access.log combined

</VirtualHost>
```

Habilitamos el virtualhost con este comando:

`sudo a2ensite coches.com.conf`

Editamos el fichero hosts:

`sudo nano /etc/hosts`

Añadiendo la siguiente línea:

`192.168.1.105   coches.com`

Donde la IP deberá ser la vuestra de cada una obtenida con `ifconfig`.

Reiniciamos el servidor Apache:

`sudo service apache2 restart`

Creamos un fichero de prueba html dentro del directorio root, es decir, en web:

```
<html>
  <head>
    <title>Bienvenido a Coches.com</title>
  </head>
  <body>
    <h1>Correcto! El Virtual Host esta funcionando!</h1>
  </body>
</html>
```

Ya solo nos queda comprobar que funciona introduciendo nuestro nombre de dominio "coches.com" en el navegador web:

![Virtual funcionando](http://i628.photobucket.com/albums/uu6/romilgildo/VirtualHost_zpslj4wedm1.png)
