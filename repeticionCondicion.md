---
title: Repetición con condición
---

Una empresa fabrica tubos. Conforme los tubos están hechos, una persona va introduciendo sus medidas en un programa. Queremos saber el número de tubos que se han fabricado hoy.

Por el enunciado del problema deducimos que necesitamos una estructura que se repite, ya que se deben poder introducir los datos de todos los tubos. El problema es que no tenemos forma de crear una lista ni de usar la función range, porque precisamente es la cantidad de tubos lo que necesitamos hallar. Por ello, no podemos usar el bloque for como hasta ahora, sino que debemos usar el bloque while, cuya estructura es la siguiente:

```
while(condicion):
	bloque
```

Esto significa que se evaluará una condición y, si se cumple, el bloque se ejecutará. Al terminar se volverá a evaluar la condición y, en caso de cumplirse, volverá a ejecutarse el bloque. En el momento en el que no se cumpla la condición el bloque no se ejecutará.


## Resolución del problema

Primero creamos la variable que llevará la cuenta de los tubos con el valor 0 (porque aún no hemos fabricado ninguno) y hacemos que el usuario escriba la longitud de un tubo. En el mismo mensaje le indicamos que escriba el 0 para salir. Si la longitud del tubo es distinta a 0 entraremos en el bucle, aumentará en 1 el número de tubos y se pedirá la longitud de otro tubo. En cuanto el usuario escriba el número 0 se saldrá del bucle y se imprimirá el mensaje adecuado según el número de tubos fabricados.

```
tubos=0
medida=float(input("Longitud del tubo (0 para salir): "))
while(medida!=0):
	tubos=tubos+1
	medida=float(input("Longitud del tubo (0 para salir): "))
if(tubos==0):
	print("Hoy no hemos tenido actividad.")
elif(tubos==1):
	print("Sólo hemos fabricado un tubo.")
else:
	print("Hemos fabricado {} tubos.".format(tubos))
```