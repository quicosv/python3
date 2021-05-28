---
title: Mensajes en la pantalla
---

Lo primero que se aprende en un lenguaje de programación es cómo hacer que el ordenador muestre un mensaje por pantalla. En el caso de Python esto se hace de la siguiente manera:

```
print("Esto sale en la pantalla.")
```

En este caso estamos utilizando una función que se llama `print`. Como se puede comprender fácilmente, esta función necesita información (el texto que se debe mostrar). Esta información que se pasa a las funciones se llama parámetros.

La forma de ejecutar una función siempre es la misma. Escribimos el nombre y, entre paréntesis, los parámetros. Si necesitamos escribir más de un parámetro, éstos se separarán por comas:

```
funcion(parametro)
funcion(parametro1,parametro2,parametro3)
```

En el caso de `print` deberemos escribir como parámetro un texto entre comillas.


## Otras formas de usar print

Si el texto se encierra entre tres comillas Python respeta los saltos de línea:

```
print("""Línea 1.
Línea 2.
Línea 3.""")
```

Si se pasan varios textos como parámetors a print, en la pantalla se separarán unos de otros con un espacio en blanco.

```
print("Este","texto","sale","bien.")
```