---
title: Argumentos
---

Los programas que hemos estado desarrollando hasta ahora están hechos para que se ejecuten en una terminal. En este sistema es muy común que se ejecuten programas especificando opciones antes de pulsar enter: estas opciones se llaman argumentos.

Para procesar los argumentos en Python necesitamos una lista que se llama `argv`. Esta lista no está disponible directamente en Python, sino que habrá que importarla desde el módulo `sys`.

Vamos a hacer un programa que simplemente nos diga cuáles son los argumentos que teclea el usuario. El resultado será que el primer argumento siempre es el nombre del programa y, a partir de ahí, el espacio en blanco separa unos argumentos de otros.

```
from sys import argv
contador=1
for argumento in argv:
	print("Argumento {}: {}.".format(contador,argumento))
	contador=contador+1
```

Vamos a hacer un programa que calcule el sueldo que debe cobrar una persona conociendo las horas trabajadas y el pago por hora. Pero vamos a hacer que el usuario pase los datos como argumentos, de forma que escribiría el nombre del programa, las horas trabajadas y el pago por hora. Luego pulsaría enter y se ejecutaría.

Primero debemos saber si el usuario escribe correctamente los argumentos. Si lo hace tendríamos la siguiente situación:

- `argv[0]` almacena el nombre del programa.
- `argv[1]` almacena las horas trabajadas.
- `argv[2]` almacena el pago por hora.


Por lo tanto, lo que nos debe preocupar es si existe `argv[2]`. Si no existe debemos imprimir un mensaje indicando la forma correcta de ejecutar el programa y hacer que termine. Para salir de un programa de Python tenemos que ejecutar la función `exit` que también está en el módulo `sys`.

En caso de que el usuario haya escrito los argumentos correctos, como éstos son tratados como texto haremos las conversiones apropiadas (las horas a número entero y el coste a número decimal). Después sólo hay que calcular el sueldo e imprimilo.

```
from sys import argv,exit
if(not argv[2]):
	print("Escriba, separados por un espacio, el nombre del programa, las horas trabajadas y el pago por hora.")
	exit()
else:
	horasTrabajadas=int(argv[1])
	costeHora=float(argv[2])
sueldo=horasTrabajadas*costeHora
print("Esta persona cobrará {} unidades monetarias.".format(sueldo))
```

A partir de ahora, cuando hagamos un programa deberemos decidir qué datos podemos recibir como argumentos y qué datos es más conveniente recibir en la ejecución del programa con la función `input`.