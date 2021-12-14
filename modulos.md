---
title: Módulos
---

Hasta ahora hemos estado trabajando con componentes que ya tiene Python. Pero Python no tiene todos los componentes que podemos necesitar para todos nuestros programas. La mayoría de ellos están agrupados en módulos. Podemos asimilar los módulos a cajas de herramientas que contienen variables y funciones que nos pueden interesar. Algunos de ellos han sido creados por Python y otros por otros usuarios. De hecho, en un futuro veremos que nosotros también podemos crear nuestros proios módulos.

Para poder utilizar las funciones y variables que hay en un módulo, lo primero que tenemos que hacer es importarlo. Esto se hace en las primeras líneas del programa y, para ello tenemos cuatro opciones:

- `import módulo`
- `from módulo import cosa`
- `from módulo import cosa,algo`
- `from módulo import *`


si usamos la primera opción estamos indicando que vamos a utilizar algo que está en ese módulo. En el momento en el que lo necesitemos indicaremos el nombre del módulo, un punto y lo que vayamos a utilizar.

```
import módulo
módulo.cosa
```

Con la segunda opción estamos diciendo que queremos usar cosa, pero como sabemos que está dentro de módulo le pedimos que nos la prepara para usarla como si ya hubiera venido con Python.

```
from módulo import cosa
cosa
```

Con la tercera opción ejemplificamos que si necesitamos importar varias variables o funciones podemos separarlas con comas.

```
from módulo import cosa,algo
cosa
algo
```

Con la última opción, al especificar un asterisco estamos pidiendo que nos prepara no sólo cosa sino todo el resto de variables y funciones que haya en módulo.

```
from módulo import *
cosa
```

De todas estas opciones, la primera es la más segura de utilizar, debido a que si un nombre de variable o función se repite en dos módulos diferentes, al obligarnos a especificar de qué módulo se debe obtener no habrá ningún problema durante la ejecución.


## Un ejemplo

Supongamos que queremos calcular la longitud de una circunferencia. Para que nuestro programa sea todo lo preciso que puede, vamos a aprovechar que en el módulo `math` está definido el valor de `pi`.

```
from math import pi
radio=float(input("Radio: "))
longitud=2*pi*radio
print("La longitud de la circunferencia es {}.".format(longitud))
```


## Crear mnemotécnicos

Podemos asignar un nombre corto o comprensible que nos interese a una función ue esté contenida en un módulo. Esto facilitará la comprensión del código, porque se supone que entendemos mejor el nombre que le hemos asignado que el nombre original de la función.

Supongamos que queremos calcular la raíz cuadrada de un número. Para esto deberíamos utilizar la función sqrt que se encuentra en el módulo math. Con lo que sabemos hasta ahora podríamos hacer un programa como el siguiente:

```
import math
print("Voy a calcular la raíz cuadrada de 100.")
resultado=math.sqrt(100)
print(resultado)
```

Imaginemos ahora que se nos complica recordar el nombre de la función sqrt y que entendemos mucho mejor el nombre en nuestro diioma (raíz cuadrada). De la misma forma en la que asignamos una variable podríamos asignar un mnemotécnico a esa parte de código tan difícil y Python lo ejecutará sin problemas. El código quedaría así:

```
import math
raizCuadrada=math.sqrt
print("Voy a calcular la raíz cuadrada de 100.")
resultado=raizCuadrada(100)
print(resultado)
```