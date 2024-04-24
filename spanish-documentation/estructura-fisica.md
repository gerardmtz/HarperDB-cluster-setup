## Estructura física y almacenamiento de DB
Las bases de datos y las tablas de datos de HarperDB se almacenan en el directorio `~/hdb`.

**Nota:** puedes cambiar la ubicación del directorio de datos de HarperDB actualizando el **rootPath** en el archivo de configuración (que especificaste durante la instalación) a una nueva ubicación. Luego, edita el archivo `hdb_boot_properties.file` para dirigir HarperDB a la nueva ubicación actualizando la variable `settings_path`.

Es importante mencionar que HarperDB utiliza *LMDB (Lightning Memory-Mapped Database)* como el almacén de clave-valor subyacente.

Los datos están **mapeados en memoria**, lo que permite un acceso rápido a los datos sin duplicación. Todas las operaciones de escritura están completamente serializadas, lo que hace que las escrituras estén libres de interbloqueos.