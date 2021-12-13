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

Para crear la lista de números utilizaremos la función range, que puede ejecutarse de tres formas diferentes:

```
range(mayor)
range(menor,mayor)
range(menor,mayor,incremento)
```

En el primer caso la lista se iniciará en 0 y llegará hasta el número mayor sin incluirlo. Es decir, si pasamos el número 5 la lista sería: 0, 1, 2, 3, 4.

En el segundo caso determinamos el número en el que se empieza (menor). La función creará la lista sin incluir al número mayor. Así, range(25,31) devolvería la siguiente lista: 25, 26, 27, 28, 29, 30.

En el último caso se establece el incremento que habrá entre cada elemento de la lista y el siguiente. Si no se especifica, Python entenderá que este incremento es 1. Por ejemplo, range(2,7,2) devolvería la siguiente lista: 2, 4, 6.

Por lo tanto, lo que debe quedar claro de esta función es lo siguiente:

1. Si sólo pasamos un úmero, la lista empezará en 0, se incrementará de 1 en 1 y llegará hasta el número especificado menos 1.
1. Si ponemos dos números la lista empezará en el primero, se irá incrementando de 1 en 1 y llegará hasta el segundo número menos 1.
1. Si ponemos 3 números, empezará en el primero, se irá incrementando en lo especificado por el tercer número y llegará hasta el segundo menos 1.


## El código

```
tabla=int(input("Número: "))
for i in range(1,11):
	print("{} por {} da {}.".format(tabla,i,tabla*i))
```