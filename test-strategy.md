PLAN DE ATAQUE - TEST STRATEGY

A continuación se detalla el plan de pruebas llevado a cabo para el proyecto "Adivina tu número", un juego desarrollado para un banco financiero. El objetivo era asegurar que la lógica del juego funcione correctamente según los requerimientos.

1. Corrección en la generación de número aleatorio.

- Descripción del error: Se estaba utilizando Math.random() * 10, lo cual generaba un número decimal entre 0 y 10 en lugar de un número entero entre 1 y 100.
- Solución implementada: Se cambió el código a Math.floor(Math.random() * 100) + 1 para generar correctamente un número entero entre 1 y 100. - LINE 45

2. Corrección en la cantidad de intentos

- Descripción del error: La cantidad de intentos permitidos estaba definida como 5, en lugar de los 10 requeridos.
- Solución implementada: Se actualizó la constante ATTEMPS a 10. - LINE 47

3. Corrección en el elemento lowOrHi

- Descripción del error: El elemento lowOrHi no se seleccionaba correctamente. 
- Solución implementada: Se corrigió la selección utilizando document.querySelector('.lowOrHi'). - LINE 50

4. Validación del número ngresado por el jugador

- Descripción del error: En el código no se estaba validando si el número ingresado por el jugador era un entero, lo que permitía entradas no válidas según el requerimiento.
- Solución implementada: Se agrego una validación para asegurarse que el número ingresadi fera un entero entre 1 y 100. En caso contrario, se muestra una alerta y no se incrementa el contador de intentos. - LINE 60

5. Corrección en los mensajes de éxito y fracaso

- Descripción del error: Al adivinar el número, se mostraba el mensaje de fracaso, y viceversa.
- Solución implementada: Se intercambiaron los mensajes para que correspondan con las condiciones de éxito y fracaso.  - LINE 72

6. Corrección en el metodo addEventListener

- Descripción del error: El método addeventListener estaba mal escrito
- Solución implementada: Se corrigió a addEventListener en todas las instancias. - LINE 96


7. Corrección en la función resetGame:

- Descripción del error: En la función resetGame, el número aleatorio se generaba incorrectamente utilizando Math.floor(Math.random()) + 1, lo que siempre generaba 1.
- Solución implementada: Se corrigió utilizando Math.floor(Math.random() * 100) + 1. - LINE 123


CONCLUSIÓN: con la correcciones implementadas el juego funciona de acuerdo a los requisitos solicitados, asegurando la funcionalidad del proyecto.
