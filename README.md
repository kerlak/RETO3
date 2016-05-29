# RETO 3 - Procesamiento

## ¿Qué hay que hacer?

Obtener información (resumida) sobre un flujo de datos que supera la capacidad de almacenamiento en disco del sistema.

La información que tenemos de los retos anteriores, parece decir que podemos almacenar varios cientos de líneas por segundo en nuestra base de datos MySQL. En este reto, el objetivo será procesar 5000 HTTP request por segundo y obtener el número de mensajes recibidos por el sistema cada 10 milisegundos, cada segundo y cada minuto. El resultado de esas estadísticas se podrá obtener por consola ejecutando un comando distinto para cada uno de los tres periodos de tiempo.

## ¿Cómo hacerlo?

Nuestra propuesta inicial será utilizar un Cassandra para las insercciones, realizándolas en modo batch cada 10 milisegundos, y evaluar si alcanza el rendimiento exigido. En caso de no llegar a dicho rendimiento, almacenar solo el resumen.

Nos basaremos en el servidor java del primer reto https://github.com/germanblanco/RETO1/tree/master/server_java
