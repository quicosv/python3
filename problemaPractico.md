---
title: Un problema práctico
---

Una tienda de deportes vende balones de fútbol. Calcular lo que debe pagar un cliente sabiendo la cantidad de balones que se lleva y el precio de cada balón.

## Planteamiento

Cuando nos planteamos resolver un problema así debemos construir un procedimiento ue resuelva el problema. A este procedimiento le llamaremos algoritmo. Posteriormente, codificaremos el algoritmo en el lenguaje de programación con el que estamos trabajando (Python en nuestro caso).


Veamos esto como si fuera un probelma para niños que tienen que aprender a multiplicar. El enunciado sería algo así: si compramos 5 balones y cada balón cuesta 3 euros, ¿cuánto tendremos que pagar? Aquí identificaríamos los datos conocidos (cantidad de balones y el precio), la incógnita (el total a pagar) y la operación que lo resuelve (la multiplicación). Entonces multiplicaríamos 3 por 5 y nos daría 15 euros.

La diferencia está en que en el momento de ejecutar el programa seremos nosotrosquienes escribamos el precio y la cantidad para que el ordenador haga el cálculo. La cantidad de balones será un número entero (con medio balón no se puede jugar) y el precio será un número decimal porque algunas unidades monetarias contemplan los céntimos. Obviamente, es razonable pensar que no todos los clientes se llevarán siempre lamisma cantidad de balones. En cuanto al precio, éste puede cambiar. Además, en este caso concreto nos estamos centrando en los balones, pero si alguien va a comprar cualquier otro artículo el total a pagar también se hallará multiplicando la cantidad por el precio. Una vez hecho el cálculo, es importante que el ordenador nos muestre el resultado obtenido para que lo conozcamos.

Este razonamiento nos lleva un algoritmo como el siguiente:

1. Se nos pide la cantidad de balones. La escribimos y se almacenará como número entero.
1. Se nos pide el precio de cada balón. Lo escribimos y se almacenará como número decimal.
1. El programa multiplica el precio por la cantidad y lo almacena como número decimal.
1. Se imprime un texto en la pantalla diciéndonos cuál es el total.


Por último, sólo nos queda traducir este algoritmo a código Python.

```
cantidad=int(input("Cantidad de balones: "))
precio=float(input("Precio de cada balón: "))
resultado=precio*cantidad
print("Hay que pagar un total de {} unidades monetarias.".format(resultado))
```