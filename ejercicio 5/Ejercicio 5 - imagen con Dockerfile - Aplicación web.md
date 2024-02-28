# Ejercicio 5 - imagen con Dockerfile - Aplicación web

> Realizado por Ángel Durántez, Sergio Álvarez y Adrián Vega

1. Arranca un contenedor que ejecute una instancia de la imagen php:7.4-apache , que se llame web y que sea accesible desde un navegador en el puerto 8000.

`docker run -d -p 8000:80 --name web php:7.4-apache`

![image-20240221105617135](./Ejercicio%205%20-%20imagen%20con%20Dockerfile%20-%20Aplicaci%C3%B3n%20web.assets/image-20240221105617135.png)

2. Coloca en el directorio raíz del servicio web ( /var/www/html ) un sitio web donde figure el nombre de los componentes del grupo - el sitio deberá tener al menos un archivo index.html y un archivo .css

`Subimos los archivos al servidor`

![image-20240221110714146](./Ejercicio%205%20-%20imagen%20con%20Dockerfile%20-%20Aplicaci%C3%B3n%20web.assets/image-20240221110714146.png)

`Ahora los copiamos al contenedor`

![image-20240221110810665](./Ejercicio%205%20-%20imagen%20con%20Dockerfile%20-%20Aplicaci%C3%B3n%20web.assets/image-20240221110810665.png)

3. Coloca en ese mismo directorio raíz un archivo llamado mes.php que muestre el nombre del mes actual. Ver la salida del script en el navegador

`creamos el archivo mes.php`

![image-20240221110943769](./Ejercicio%205%20-%20imagen%20con%20Dockerfile%20-%20Aplicaci%C3%B3n%20web.assets/image-20240221110943769.png)

`Lo copiamos al contenedor`

![image-20240221111005713](./Ejercicio%205%20-%20imagen%20con%20Dockerfile%20-%20Aplicaci%C3%B3n%20web.assets/image-20240221111005713.png)

![image-20240221115322949](./Ejercicio%205%20-%20imagen%20con%20Dockerfile%20-%20Aplicaci%C3%B3n%20web.assets/image-20240221115322949.png)

4. Borrar el contenedor

![image-20240226084046414](./Ejercicio%205%20-%20imagen%20con%20Dockerfile%20-%20Aplicaci%C3%B3n%20web.assets/image-20240226084046414.png)

5. Automatizar estas operaciones creando un fichero Dockerfile

![image-20240226084522544](./Ejercicio%205%20-%20imagen%20con%20Dockerfile%20-%20Aplicaci%C3%B3n%20web.assets/image-20240226084522544.png)

![image-20240226084455192](./Ejercicio%205%20-%20imagen%20con%20Dockerfile%20-%20Aplicaci%C3%B3n%20web.assets/image-20240226084455192.png)

![image-20240226085448977](./Ejercicio%205%20-%20imagen%20con%20Dockerfile%20-%20Aplicaci%C3%B3n%20web.assets/image-20240226085448977.png)

![image-20240226085429266](./Ejercicio%205%20-%20imagen%20con%20Dockerfile%20-%20Aplicaci%C3%B3n%20web.assets/image-20240226085429266.png)

![image-20240226085502370](./Ejercicio%205%20-%20imagen%20con%20Dockerfile%20-%20Aplicaci%C3%B3n%20web.assets/image-20240226085502370.png)

![image-20240226091036244](./Ejercicio%205%20-%20imagen%20con%20Dockerfile%20-%20Aplicaci%C3%B3n%20web.assets/image-20240226091036244.png)

