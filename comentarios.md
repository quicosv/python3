---
title: Comentarios
---

De todas las acepciones que tiene la palabra comentario en el diccionario, la que más puede interesarnos es la siguiente:

> Explicación de un texto para su mejor intelección.

Precisamente, uno de los principales usos que se le da a los comentarios es explicar lo que hace nuestro código, bien para que quien quiera colaborar con nosotros entienda lo que está hecho y pueda realizar sus aportaciones o bien para que a nosotros mismos se nos haga más fácil la revisión y modificación de nuestros programas cuando vayamos a implementar futuras actualizaciones.

Los comentarios se inician con el carácter `#` y se terminan cuando finaliza la línea. Si este carácter está dentro de un texto entre comillas no se comportará como un comentario, sino que se considerará como parte del texto.

Todo lo que forme parte de un comentario será ignorado por el intérprete de python. Esto hace que también se usen los comentarios para que el intérprete ignore alguna parte que tiene algún problema. A continuación se presenta un ejemplo:

```
# Programa de prueba
# Imprimimos una línea
print("Esto se imprime.")
# print("Esto no se ejecuta.")
print("Esto sí que sale en la pantalla.")
print("# Esto no es un comentario.")
```

Por último, se propone un ejercicio que se recomienda hacer con cada ejemplo para que cada uno sepa la medida en la que va comprendiendo los conceptos. Consiste en escribir encima de cada línea un comentario explicando lo que hace esa línea.