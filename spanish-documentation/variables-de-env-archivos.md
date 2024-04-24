Por supuesto, aquí está la traducción al español del texto que proporcionaste, manteniendo la sintaxis en Markdown:

# Archivos de configuración y variables de entorno

HarperDB se configura a través de un archivo **YAML** llamado **harperdb-config.yaml** ubicado en el directorio raíz de HarperDB; por defecto, este es un directorio llamado **hdb** ubicado en el directorio home del usuario actual.

## Archivo de configuración y uso

Para cambiar los valores de configuración necesitamos editar el archivo **harperdb-config.yaml** y guardar cualquier cambio. Este archivo puede estar ubicado en el directorio **hdb**.

**HarperDB necesita ser reiniciado para que los cambios surtan efecto**

Algunas secciones importantes en este archivo son:

- `http sessionAffinity`: Esta sección se utiliza para mejorar la eficiencia y equidad en la utilización de hilos al dirigir múltiples solicitudes del mismo cliente al mismo hilo.

- `clustering`: Esta sección configura el motor de agrupamiento, que se utiliza para replicar datos entre instancias de HarperDB

Alternativamente, la configuración se puede cambiar a través de variables de entorno y/o de línea de comandos o a través de la API

## Variables de entorno

Estas son las variables importantes de HarperDB:

- `TC_AGREEMENT`: Esta variable se utiliza para aceptar los términos y condiciones
- `HDB_ADMIN_USERNAME`: Esta variable se utiliza para establecer el nombre de usuario del administrador
- `HDB_ADMIN_PASSWORD`: Esta variable se utiliza para establecer la contraseña del administrador
- `ROOTPATH`: Esta variable se utiliza para establecer la ruta raíz
- `OPERATIONSAPI_NETWORK_PORT`: Esta variable se utiliza para establecer el puerto de red

Estas variables de entorno se pueden utilizar para automatizar las instalaciones de HarperDB