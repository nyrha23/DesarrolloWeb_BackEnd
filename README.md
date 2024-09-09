[![Web](https://img.shields.io/badge/GitHub-Nyrha23-9C27B0?style=flat-square&logo=github&logoColor=white&labelColor=101010)](https://github.com/nyrha23) 
[![Web](https://img.shields.io/badge/LinkedIn-Trinidad_Pasi-0e76a8?style=flat-square&logo=linkedin&logoColor=white&labelColor=101010)](https://www.linkedin.com/in/trinidad-pasi/) 

# Desarrollo de Sistemas Web | Back End 
> Este desafío nos acerca más al área de desarrollo y nos prepara para los próximos ejercicios.

## Consigna del ejercicio

Desarrollar un sistema de gestión de pedidos que simula la creación, procesamiento y seguimiento de pedidos. El sistema debe actualizar y mostrar el estado de cada pedido y simular retrasos en el procesamiento y en la realización del pedido. Utiliza funciones de generación aleatoria para simular variaciones en el procesamiento de pedidos. El enfoque debe estar en el backend y se utilizará la consola para la salida de datos. El ingreso de datos será simulado por randoms.

## Instrucciones
1. Definición de la Clase Pedido:
  + Crea una *clase* `Pedido` que represente un pedido con las siguientes propiedades:
    - `nombre`: nombre del pedido.
    - `contenido`: descripción del contenido del pedido.
    - `precio`: precio del pedido.
  + Implementa el *constructor* de la clase para inicializar estas propiedades.

2. Datos de los Objetos:
  + Define tres *arrays* para representar los datos de los pedidos:
    - `nombres`: Contiene los nombres de diferentes productos (ej. 'Burger Clásica', 'Burger BBQ', 'Burger Veggie').
    - `tipos`: Contiene los tipos de ingredientes o materiales (ej. 'salsa especial', 'cebolla, tomate y lechuga', 'salsa 1000 islas').
    - `precios`: Contiene los precios de los productos en pesos (ej. [8.990, 10.490, 9.790]).

3. Funciones Auxiliares:
  + Implementa la función `seleccionarAleatorio(array)` que devuelve un elemento aleatorio de un array proporcionado.
  + Implementa la función `esperar(ms)` que devuelve una *promesa* que se resuelve después de un tiempo específico en milisegundos. Utiliza `setTimeout` dentro de la promesa para simular la espera.

4. Actualización del Estado del Pedido:
  + Implementa la función `actualizarEstadoPedido(pedido, estado)` que actualiza el estado del pedido. Esta función debe imprimir en la consola el nombre del pedido junto con el nuevo estado (ej. 'Pedido X: Recibido').

5. Seguimiento del Proceso del Pedido:
  + Implementa una función *asincrónica* `seguirProcesoPedido(pedido)` que simule el seguimiento del pedido. La función debe actualizar el estado del pedido en intervalos específicos:
    - 'Recibido' después de 1 segundo.
    - 'Preparando' después de 3 segundos.
    - 'Finalizado' después de 1 segundo.
    - 'Entregado' después de 1 segundo.
  + Utiliza la función `esperar(ms)` para las esperas entre cambios de estado.

6. Realización del Pedido:
  + Implementa una función asincrónica `realizarPedido(pedido)` que simula el envío del pedido con un retraso aleatorio. La función debe devolver una promesa que se resuelva con un mensaje indicando el éxito del pedido y el tiempo de retraso en segundos. El retraso debe ser un valor aleatorio entre 1 y 10 segundos.

7. Generación de Pedidos Aleatorios:
  + Implementa la función `generarPedidoAleatorio(i)` que crea un nuevo objeto Pedido con datos aleatorios. La función debe:
    - Generar un nombre de pedido (ej. 'Pedido 1').
    - Seleccionar un contenido aleatorio de los arrays nombres y tipos.
    - Seleccionar un precio aleatorio del array precios.

8. Manejo de Pedidos:
  + Implementa la función asincrónica `manejarPedido(i)` que realice las siguientes tareas:
    - Crear un pedido aleatorio usando `generarPedidoAleatorio(i)`.
    - Simular la realización del pedido con `realizarPedido(pedido)`.
    - Simular el seguimiento del proceso del pedido con `seguirProcesoPedido(pedido)`.

9. Generación Continua de Pedidos:
  + Implementa la función `generarPedidosContinuamente()` que genere pedidos aleatorios de manera continua. La función debe:
    - Generar un nuevo pedido con un retraso aleatorio entre 1 y 10 segundos.
    - Llamar a `manejarPedido(i)` para procesar cada nuevo pedido.
    - Incrementar el contador `i` para crear pedidos únicos.

10. Inicialización:
  + Configura el script para que se inicie la generación continua de pedidos llamando a `generarPedidosContinuamente()` cuando el script se ejecute.

### Ejemplo de Ejecución en Consola:
1. El script comienza generando pedidos aleatorios con un retraso aleatorio.
2. Cada pedido es creado, enviado y seguido con tiempos simulados.
3. Los estados de los pedidos se imprimen en la consola a medida que cambian.

> [!Note]
> Solo se requiere la implementación del backend, por lo que la salida se deben manejar a través de la consola. Asegúrate de que el código esté correctamente comentado para explicar la lógica y el flujo de cada función.
