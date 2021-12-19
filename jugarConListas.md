---
title: Jugar con listas
---

Aquí veremos distintas operaciones que podemos hacer con las listas. Para eso vamos a crear una lista de ejemplo con frutas:

```
frutas=["Manzana","fresa","plátano","naranja"]
```

Podemos imprimir un elemento de la lista. Para eso hay que pasar como parámetro en la función print el nombre de la lista y, entre corchetes, el índice del leemento que nos interesa:

```
print(frutas[1])
```

Como las listas pueden modificarse, existe una forma de modificar uno de sus elementos. Sólo hay que acceder a él y asignarle otro valor (como si fuera una variable).

```
frutas[2]="pera"
```

La función len nos devolverá el número de elementos que tiene la lista.

```
len(frutas)
```

Se puede borrar cualquier elemento de la lista con la función del, que recibe como parámetro el elemento a borrar.

```
del(frutas[1]
```

## Métodos de las listas

Lo que vamos a ver ahora son funciones que operan sobre las listas. Al llamarlos métodos, tenemos que recordar que para usarlos deberemos poner el nombre de lalista, un punto y el método que deseamos ejecutar.

Podemos añadir elementos al final de la lista con el método append:

```
frutas.append("piña")
```

También podemos averiguar el índice de la primera aparición de un elemento en la lista con el método index.

```
frutas.index("piña")
```

Podemos borrar la primera aparición de un elemento con el método remove.

```
frutas.remove("piña")
```

Por último, si todos los elementos son del mismo tipo, podemos ordenar la lista con el método sorted:

```
ordenAscendente=sorted(frutas)
```

La función devuelve una lista nueva con los elementos ordenados de forma ascendente. Si quisiéramosun orden descendente añadiríamos un parámetro:

```
ordenDescendente=sorted(frutas,reverse=True)
```