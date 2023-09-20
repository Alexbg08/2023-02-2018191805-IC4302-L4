# 2023-02-2018191805-IC4302-L4

Alexander Brenes Garita - 2018191805

---------------------------------------------------------------------------------------------

1. ¿Cómo se diferencia el modelo de datos de Big Tables de una base de datos SQL?

Una de las diferencias es en el tipo de datos, en el Bigtable es una base de datos NoSQL que está diseñada para manejar grandes cantidades de datos estructurados y semi-estructurados. Maneja datos tipo texto, numeros y binarios.
En las Base de datos SQL almacenan datos en tablas con un esquema fijo y relaciones definidas entre las tablas. Son diseñadas para datos estructurados y manipular datos.

2. ¿Cuáles decisiones de diseño en Big Table aumenta el rendimiento del sistema? Explique.

- Uso de cache: Bigtable ofrece opciones de almacenamiento en caché que permiten mejorar el rendimiento de lectura. Ya que se puede configurar la caché de bloques y la caché de resultados de consultas para acelerar el acceso a los datos más frecuentes.

- Escabilidad: En Bigtable se puede escalar horizontalmente y el número de nodos de Bigtable puede optimizar el rendimiento en función de la carga de trabajo.

- Diseño de esquema de columnas: Organizar los datos en columnas, qué columnas indexar y qué columnas compuestas utilizar pueden tener un impacto significativo en el rendimiento.

3. ¿Considera que Big Table podría cumplir el papel de Prometheus en un sistema de Observabilidad? En caso de responder No, explique detalladamente, en caso de responder si, ¿utilizarían versiones de timestamps para cada métrica y recolectarían cada métrica como un row separado?

El BigTable NO podria cumplir el papel de Prometheus ya que almacena datos en un modelo de datos de pares, lo que hace no es nativamente adecuado para almacenar series temporales de métricas, como lo hace Prometheus

4. Explique en detalle la organización de tablets en Big Table.

La organización de las tabletas en Bigtable es un componente crítico de su arquitectura y permite una distribución eficiente, escalabilidad y rendimiento de datos. Cada tablet representa un rango de claves de fila y se distribuye geográficamente según las necesidades de la aplicación y la configuración. Esto permite que Bigtable sea una solución altamente escalable y distribuida para el almacenamiento y la recuperación de datos a gran escala.

5. Comente los tipos de fallas de sistemas distribuidos en bases de datos que se mencionan en la lectura.

- Fallas de hardware: Estas fallas se refieren a problemas en los componentes físicos de los servidores, como discos duros, memoria RAM, CPU, etc.

- Fallas de software: Las fallas de software incluyen errores en el sistema operativo, en el software de Bigtable o en las aplicaciones que interactúan con Bigtable

- Fallas de red: Las fallas de red son problemas de conectividad entre los nodos del sistema distribuido.

- Fallas de seguridad:Las fallas de seguridad incluyen violaciones de seguridad como accesos no autorizados, ataques de denegación de servicio entre otros.
