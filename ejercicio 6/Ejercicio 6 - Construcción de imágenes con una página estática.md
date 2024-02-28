# Ejercicio 6 - Construcción de imágenes con una página estática

> Realizado por Ángel Durántez, Sergio Álvarez y Adrián Vega

## Version 1: Desde una imagen base

Tenemos un directorio, que en Docker se denomina contexto, donde tenemos el fichero 
Dockerfile y un directorio, llamado public_html con nuestra página web:

![image-20240226092459644](./Ejercicio%206%20-%20Construcci%C3%B3n%20de%20im%C3%A1genes%20con%20una%20p%C3%A1gina%20est%C3%A1tica.assets/image-20240226092459644.png)

![image-20240226092620872](./Ejercicio%206%20-%20Construcci%C3%B3n%20de%20im%C3%A1genes%20con%20una%20p%C3%A1gina%20est%C3%A1tica.assets/image-20240226092620872.png)

Comprobamos que se ha creado la imagen

![image-20240226094857633](./Ejercicio%206%20-%20Construcci%C3%B3n%20de%20im%C3%A1genes%20con%20una%20p%C3%A1gina%20est%C3%A1tica.assets/image-20240226094857633.png)

Creamos el contenedor con la imagen

![image-20240226094938521](./Ejercicio%206%20-%20Construcci%C3%B3n%20de%20im%C3%A1genes%20con%20una%20p%C3%A1gina%20est%C3%A1tica.assets/image-20240226094938521.png)

![image-20240226094950797](./Ejercicio%206%20-%20Construcci%C3%B3n%20de%20im%C3%A1genes%20con%20una%20p%C3%A1gina%20est%C3%A1tica.assets/image-20240226094950797.png)

## Version 2: Desde una imagen con apache2

Ahora el dockerfile será el siguiente

![image-20240226095112633](./Ejercicio%206%20-%20Construcci%C3%B3n%20de%20im%C3%A1genes%20con%20una%20p%C3%A1gina%20est%C3%A1tica.assets/image-20240226095112633.png)

Ahora creamos la imagen y el contenedor

![image-20240226095547587](./Ejercicio%206%20-%20Construcci%C3%B3n%20de%20im%C3%A1genes%20con%20una%20p%C3%A1gina%20est%C3%A1tica.assets/image-20240226095547587.png)

![image-20240226095630609](./Ejercicio%206%20-%20Construcci%C3%B3n%20de%20im%C3%A1genes%20con%20una%20p%C3%A1gina%20est%C3%A1tica.assets/image-20240226095630609.png)

![image-20240226101450854](./Ejercicio%206%20-%20Construcci%C3%B3n%20de%20im%C3%A1genes%20con%20una%20p%C3%A1gina%20est%C3%A1tica.assets/image-20240226101450854.png)

## Version 3: Desde una imagen con nginx

En este caso el Dockefile seria este

![image-20240226101554146](./Ejercicio%206%20-%20Construcci%C3%B3n%20de%20im%C3%A1genes%20con%20una%20p%C3%A1gina%20est%C3%A1tica.assets/image-20240226101554146.png)

Y realizamos lo mismo que antes

![image-20240226101642675](./Ejercicio%206%20-%20Construcci%C3%B3n%20de%20im%C3%A1genes%20con%20una%20p%C3%A1gina%20est%C3%A1tica.assets/image-20240226101642675.png)

![image-20240226101721914](./Ejercicio%206%20-%20Construcci%C3%B3n%20de%20im%C3%A1genes%20con%20una%20p%C3%A1gina%20est%C3%A1tica.assets/image-20240226101721914.png)

![image-20240226101729758](./Ejercicio%206%20-%20Construcci%C3%B3n%20de%20im%C3%A1genes%20con%20una%20p%C3%A1gina%20est%C3%A1tica.assets/image-20240226101729758.png)

