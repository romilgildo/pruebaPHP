# Ejecución app

Para empezar, vamos a trabajar con la demo de Symfony. Descargar con:

`symfony demo`

Entrar al directorio symfony_demo y ejecutar la aplicación con:

`php app/console server:run`

Comprobar su funcionamiento en la dirección `localhost:8000`:

![Funcionamiento servidor PHP](http://i628.photobucket.com/albums/uu6/romilgildo/runDemo_zpsug9my1q2.png)

Para parar la ejecución, basta con pulsar `Ctrl + C` en la terminal.

Debemos añadir también el siguiente paquete para que funcione correctamente:

```
sudo apt-get install php5-sqlite
sudo service apache2 restart
```

Para gestionar usuarios admins:

```
php app/console app:list-users
php app/console app:add-use
```
