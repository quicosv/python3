---
title: Condicionales complejos
---

Según lo que hemos visto hasta ahora sobre condicionales, tenemos un bloque que se inicia con la línea del `if` en la que expresamos la condición que queremos evaluar y lo que hará el programa si se cumple. Luego se define un bloque que empieza con la palabra clave `else` que indica lo que se va a hacer en caso de que la condición no se cumpla. En medio de estos dos bloques podemos definir tantos bloques como necesitemos para evaluar otras condiciones. Estos bloques se inician con la palabra clave `elif` y la estructura ahora quedaría así:

```
if(condición):
	Lo que pasa si se cumple
elif(otra condición):
	Se cumple la otra condición
elif(una condición más:
	Se cumple esta condición
else:
	No se cumple ninguna condición
```


## Problema

Conociendo la cantidad de preguntas de un examen y las respuestas acertadas informar de la nota de acuerdo con estos criterios:

- Si el acierto es del 100% impimiremos matrícula de honor.
- Si el acierto no llega al 100%, pero es como mínimo del 90% imprimiremos excelente.
- Si el acierto no llega al 90%, pero es como mínimo del 70% imprimiremos notable.
- Si el acierto no llega al 70%, pero es como mínimo del 60% imprimiremos bien.
- Si el acierto no llega al 60%, pero es como mínimo del 50% imprimiremos aprobado.
- Si el acierto no llega al 50% imprimiremos suspendido.


## Planteamiento

1. Guardaremos en variables el total de preguntas y la cantidad de aciertos, que nos los dará el usuario.
1. Calcularemos el porcentaje de acierto dividendo los aciertos entre el total de preguntas y multiplicándolo por 100.
1. Primero podríamos averiguar si el acierto es exactamente igual a 100. Si lo es imprimimos matrícula de honor.
1. Si esta condición no se cumple el acierto ya no llegará al 100%, por lo que para saber si debemos imprimir excelente sólo habría que comprobar si el acierto es igual o superior (como mínimo) al 90%.
1. Así seguimos razonando el resto de condiciones hasta llegar a la del aprobado. Si no es matrícula de honor, excelente, notable, bien ni aprobado sólo puede ser suspendido.


## El código

```
total=int(input("Cantidad de preguntas: "))
aciertos=int(input("Respuestas correctas: "))
porcentaje=100*(aciertos/total)
if(porcentaje==100):
	print("Matrícula de honor.")
elif(porcentaje>=90):
	print("Excelente.")
elif(porcentaje>=70):
	print("Notable.")
elif(porcentaje>=60):
	print("Bien.")
elif(porcentaje>=50):
	print("Aprobado.")
else:
	print("Suspendido.")
```