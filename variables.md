---
title: Variables
---

Una variable es un lugar en el que poder almacenar un valor (como un texto o unnúmero). Su ventaja es que las operaciones que hagamos no se pierden y que si cambiamos su valor inicial podremos saber cómo afecta al resto del programa.

Supongamos que tenemos unas gallinas que han puesto 36 huevos. De ellos vendemos 24 y queremos saber cuántos huevos nos quedan. Aquí entran en juego tres variables.

- `puestos` almacenaría los huevos que han puesto las gallinas.
- `vendidos` almacenaría los huevos que hemos vendido.
- `restantes` almacenaría el resultado de la resta con la que calculamos los huevos que nos quedan.


las variables `puestos` y `vendidos` nos permiten hacer la resta que resuelve el problema. La variable `restantes` permite almacenar el resultado. Además, si las gallinas hubiesen puesto 55 huevos, sólo tendríamos que cambiar un 36 por un 55 en el lugar en el que le decimos el valor de `puestos` y el programa seguiría funcionando.

Los caracteres admitidos en nombres de variables son letras, números y el guión bajo (`.`). Es una buena práctica que el nombre de la variable nos dé una idea de lo que va a almacenar. Una buena forma de construir nombres de variables es escribirlos como si fueran una palabra (ya que no se admite el espacio en blanco) pero si en realidad son varias palabras podemos poner la pimera en minúscula y la inicial de las restantes en mayúscula.

Por ejemplo, si queremos almacenar la cantidad de usuarios que han comprado un programa, `usuariosConLicencia` podría ser un buen nombre para esa variable.