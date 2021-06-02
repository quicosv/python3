---
title: Listas y tuplas
---

Cuando hemos hablado del bucle `for` hemos creado una lista de números usando la función `range`. Sin embargo, las listas también pueden contener cadenas y, además, no es obligatorio que todos los datos sean de un mismo tipo.

Para crear una lista escribiremos el nombre que le vamos a dar y le asignaremos el conjunto de datos que contendrá. Éste irá encerrado entre corchetes y cada dato se separará del siguiente con una coma.

Existe otro tipo de dato que podemos crear, denominado tupla. Las tuplas se crean igual que las listas, exceptuando que en vez de encerrar los datos entre corchetes lo haremos entre paréntesis:

```
lista=["avión","coche","bicilceta"]
tupla=(5,7,9,11)
```


Tanto las listas como las tuplas se pueden recorrer de la misma manera, pero existe una diferencia muy importante entre ellas: las tuplas no se pueden modificar.


## Acceder a los elementos

Una de las cosas más importantes que hay que aprender (y que suele confundir a los principiantes) es la forma en la que accedemos a un elemento de una lista o tupla. Consiste en escribir el nombre y, entre corchetes, el índice que le corresponde.

Tomemos como ejemplo la lista que hemos creado. Esta lista corresponde a la clasificación final de una carrera celebrada entre distintos medios de transporte. Si quisiéramos contarle a alguien el resultado de la carrera le diríamos que el avión llegó primero, el coche segundo y la bicicleta en tercera posición. Esto hace referencia al orden. Sin embargo, como las matemáticas demuestran que es más fácil realizar los cálculos si nos referimos al primer elemento con el número 0 que si lo hiciéramos con el 1, el primer elemento de cualquier lista o tupla tendrá el índice 0.

Por lo tanto, para conocer el índice de un elemento restaremos 1 a la posición que ocupa (orden). En cambio, si conocemos el índice de un elemento podremos sumarle 1 para saber qué psoición ocupa dentro de la lista. En la siguiente tabla se muestra el orden y el índice de cada medio de transporte:

| Orden | Índice | Elemento |
| --- | --- | --- |
| 1 | 0 | Avión |
| 2 | 1 | Coche |
| 3 | 2 | Bicicleta |


Para poder afianzar este concepto es recomendable practicar en los ratos libres construyendo frases como las siguientes:

- El elemento que está en el lugar 5 tiene índice 4.
- El elemento cuyo índice es 32 ocupa el lugar 33.