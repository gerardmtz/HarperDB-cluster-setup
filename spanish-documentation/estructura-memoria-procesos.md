# Procesos de memoria e hilos en HarperDB

**Procesos de Memoria:** HarperDB está construido sobre la base de la Base de Datos Mapeada en Memoria Lightning (LMDB), un almacén de clave-valor que ofrece un rendimiento y funcionalidad líderes en la industria.

Esto permite que el algoritmo de almacenamiento de HarperDB almacene datos en tablas como filas/objetos.

Las operaciones de HarperDB son atómicas, consistentes y aisladas por instancia. Esto significa que cualquier consulta proporcionará una vista de instantánea consistente y aislada de la base de datos.

**Hilos:** A partir de la versión 4.1, HarperDB introdujo la capacidad de usar hilos de trabajo para manejar concurrentemente las solicitudes HTTP. Esto fue un cambio del modelo anterior donde los procesos manejaban estas solicitudes. El uso de hilos proporciona varios beneficios:

- Mejor control de la delegación de tráfico con soporte para seguimiento de carga optimizado y afinidad de sesión.
- Mejor capacidad de depuración.
- Soporte para modelos de almacenamiento alternativos.
- Mejor utilización de memoria/recursos.

En términos de uso de recursos, los hilos requieren menos recursos que los procesos. Cada aspecto del tiempo de ejecución de Node.js debe duplicarse en cada proceso adicional. Sin embargo, los hilos de trabajo pueden reutilizar partes importantes del tiempo de ejecución, incluyendo las funciones básicas del tiempo de ejecución de JS, la instancia central de lmdb-js, y quizás lo más importante, el grupo de trabajadores para tareas asíncronas.

Cada tabla de HarperDB tiene un solo proceso de escritura, evitando interbloqueos y asegurando que las escrituras se ejecuten en el orden en que fueron recibidas. Las tablas de HarperDB pueden tener múltiples procesos de lectura operando al mismo tiempo para lecturas consistentes y de alta escala.