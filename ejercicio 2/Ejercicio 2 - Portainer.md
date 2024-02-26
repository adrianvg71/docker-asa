# Ejercicio 2 - Portainer

> Realizado por Ángel Durántez, Sergio Álvarez y Adrián Vega

## **Utiliza una imagen de 'Portainer' para gestionar Docker. **

**Documenta la aplicación, su puesta en funcionamiento y realiza capturas de varias operaciones, por ejemplo:**

Lo primero que haremos será descargar la imagen de portainer con el siguiente comando.

```bash
$docker pull portainer/portainer
```

![image-20240223094904449](./Ejercicio 2 - Portainer.assets/image-20240223094904449.png)

Seguidamente, crearemos un contenedor de docker con la imagen que acabamos de descargar.

```bash
$docker run -d -p 9000:9000 --name portainer --restart always -v /var/run/docker.sock:/var/run/docker.sock portainer/portainer
```

![image-20240223095127527](./Ejercicio 2 - Portainer.assets/image-20240223095127527.png)

![image-20240223095302036](./Ejercicio 2 - Portainer.assets/image-20240223095302036.png)

**Muestra contenedores activos, para un contenedor, borra un contenedor**

![image-20240226084728220](./Ejercicio 2 - Portainer.assets/image-20240226084728220.png)

El contenedor que borre fue el 'guestbook'.![image-20240226084832100](./Ejercicio 2 - Portainer.assets/image-20240226084832100.png)

**Muestra alguna operación con redes Docker**

![image-20240226085000904](./Ejercicio 2 - Portainer.assets/image-20240226085000904.png)

La operación que hice con las redes, fue la de borrado de la red que utilizaba el contenedor guestbook ya que antes he borrado ese contenedor y ya no la necesito.

**Muestra alguna operación con volúmenes Docker**

![image-20240226085337768](./Ejercicio 2 - Portainer.assets/image-20240226085337768.png)

Cree un volumen --> 'dockerVolumen' como operación con los volúmenes.