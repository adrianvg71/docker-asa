# Ejercicio 3 - Contenedores en red: Adminer y MariaDB

> Realizado por Ángel Durántez, Sergio Álvarez y Adrián Vega

1. Crea una red bridge redbd.

   ```bash
   $docker network create redbd
   $docker network ls
   ```

![image-20240223092455629](./Ejercicio 3 - Contenedores en red Adminer y MariaDB.assets/image-20240223092455629.png)

![image-20240223092444013](./Ejercicio 3 - Contenedores en red Adminer y MariaDB.assets/image-20240223092444013.png)



2. Crea un contenedor con una imagen de mariaDB que estará en la red redbd . Este contenedor se ejecutará en segundo plano, y será accesible a través del puerto 3306. (Es necesario definir la contraseña del usuario root y un volumen de datos persistente)

   ```bash
   $docker run -d --name contenedorMariaDB --network=redbd -p 3306:3306 -e MYSQL_ROOTPASSWORD=1234 -v /home/cliente mariadb
   ```

![image-20240223092419694](./Ejercicio 3 - Contenedores en red Adminer y MariaDB.assets/image-20240223092419694.png)



3. Crear un contenedor con Adminer que se pueda conectar al contenedor de la BD

   ```bash
   $docker run -d --name contenedorAdminer --network=redbd -p 8080:8080 adminer
   ```

![image-20240223092721573](./Ejercicio 3 - Contenedores en red Adminer y MariaDB.assets/image-20240223092721573.png)



4. Comprobar que el contenedor Adminer puede conectar con el contenedor mysql abriendo un navegador web y accediendo a la URL: http://localhost:8080

![image-20240223094752821](./Ejercicio 3 - Contenedores en red Adminer y MariaDB.assets/image-20240223094752821.png)

![image-20240223094708814](./Ejercicio 3 - Contenedores en red Adminer y MariaDB.assets/image-20240223094708814.png)



Captura de pantalla y documento donde se vean los contenedores creados y en ejecución.

```bash
$docker ps -a
```

![image-20240223094837748](./Ejercicio 3 - Contenedores en red Adminer y MariaDB.assets/image-20240223094837748.png)

Captura de pantalla y documento donde se vea el acceso a la BD a través de la interfaz web de Adminer

![image-20240223094752821](./Ejercicio 3 - Contenedores en red Adminer y MariaDB.assets/image-20240223094752821.png)

![image-20240223094708814](./Ejercicio 3 - Contenedores en red Adminer y MariaDB.assets/image-20240223094708814.png)

Captura de pantalla y documento donde se vea la creación de una BD con la interfaz web Adminer

![image-20240223094931589](./Ejercicio 3 - Contenedores en red Adminer y MariaDB.assets/image-20240223094931589.png)

![image-20240223095030061](./Ejercicio 3 - Contenedores en red Adminer y MariaDB.assets/image-20240223095030061.png)

Captura de pantalla y documento donde se entre a la consola del servidor web en modo texto y se compruebe que se ha creado la BD

```bash
$docker exec -it contenedorMariaDB bash
/# mariadb -u root -p
MariaDB [(none)]> SHOW DATABASES;
```

![image-20240223095946964](./Ejercicio 3 - Contenedores en red Adminer y MariaDB.assets/image-20240223095946964.png)

Borrar los contenedores la red y los volúmenes utilizados

```bash
$docker stop contenedorAdminer
$docker stop contenedorMariaDB
$docker rm contenedorAdminer
$docker rm contenedorMariaDB
```

![image-20240223100155619](./Ejercicio 3 - Contenedores en red Adminer y MariaDB.assets/image-20240223100155619.png)