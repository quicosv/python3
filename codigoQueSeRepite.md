---
title: Código que se repite
---

Imaginemos que queremos hacer un programa que imprima la tabla de multiplicar del número que se le solicita. Con lo que sabemos hasta ahora podríamos resolverlo, pero tendríamos que hacer muchas líneas dedicadas a hacer las distintas multiplicaciones (una para multiplicar por uno, otra para multiplicar por dos, etcétera). Afortunadamente, existe una manera de ahorrarnos trabajo consistente en hacer que un determinado bloque se repita un número de veces.


## El bloque for

La estructura repetitiva que usaremos en este problema será la siguiente:

```
for elemento in lista:
	bloque de instrucciones que se repiten
```

Lo que ocurrirá será que se creará una variable que se va a llamar elemento. Su primer valor será el primer elemento de la lista. Entonces se ejecutará el bloque de instrucciones que se repiten. Cuando termine, elemento pasará a valer el siguiente elemento de la lista y las instrucciones del bloque se repetirán nuevamente. Esto sucederá hasta que nuestra variable elemento tenga como valor el último elemento de la lista. En ese momento, cuando se terminen de repetir las instrucciones del bloque se seguirá con la ejecución del resto del programa.


## La tabla de multiplicar

Una tabla de multiplicar consiste en conocer el resultado de multiplicar un determinado número por los números del 1 al 10. Por lo tanto, la lista con la que deberemos trabajar será la de los números del 1 al 10. Dentro del bucle (así es como se llama a la estructura repetitiva) sólo tendremos que imprimir el valor de multiplicar el número que ha proporcionado el usuario por el valor que tenga la variable elemento en ese instante. Este programa también nos servirá para comprobar que cuando formateamos el texto que imprimimos, no sólo podemos imprimir el contenido de una variable, sino también el resultado de una operación.


## El código

```
tabla=int(input("Número: "))
for i in range(1,11):
	print("{} por {} da {}.".format(tabla,i,tabla*i))
```