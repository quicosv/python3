---
title: Más sobre repetición de código
---

Existe otra forma de hacer que el código se reptia. Se hace utilizando el bloque while, que se define de la siguiente forma:

```
while(expresión):
	bloque
```

La estructura es más parecida a la de las condiciones. En este caso, el bloque de código se repetirá mientras sea cierta la expresión.

Supongamos que queremos crear un programa que imprima los números del 1 al 5. Si usásemos un for nos quedaría así:

```
for numero in range(1,6):
	print("{} ".format(numero))
```

Haciéndolo con un while primero tenemos que crear la variable que alamcene el número. Luego se entra en el bloque while, donde se imprime la variable y luego se incrementa.

```
numero=1
while(numero<=5):
	print("{} ".format(numero))
	numero=numero+1
```


## Repetir sin definir la condición

Es posible que no sea muy fácil definir la expresión que se debe cumplir para que se repita el bloque de código. En este caso podemos poner ente los paréntesis de definición del while la palabra True (con la T mayúscula), que significa verdadero en inglés. Si hacemos esto deberemos tener mucho cuidado y utilizar en algún punto la palabra clave break. De lo contrario, el código se repetiría eternamente y el programa no terminaría nunca.

Resolveremos ahora el problema anterior con esta herramienta, dejando a la imaginación y la práctica de cada quién los casos en los que crea que la debe utilizar.

```
numero=1
while(True):
	print("{} ".format(numero))
	numero=numero+1
	if(numero>5):
		break
```