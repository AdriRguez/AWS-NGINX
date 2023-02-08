## Crear carpetas de los sitios web
Accedemos con el usuario root y nos vamos al usuario EC2 y creamos las carpetas html,sitios, sitio1 y sitio2. Despues creamos los index.html que sera a donde apunten nuestros alias.

## Configuracion Nginx
Nos iremos a la carpeta Conf.d y crearemos el fichero server1.conf

~~~
server {
    #root home/ec2-user/html/sitios/;

    location /fantasticas {  
    alias /home/ec2-user/html/sitios/sitio1;
    }

    location /fabulosas {  
    alias /home/ec2-user/html/sitios/sitio2;
    }
}
~~~

Pondremos los nombres de nuestros alias, y en donde pone alias le indicaremos donde se encuentra los index.html

