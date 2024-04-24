# Instalando requisitos

La instalación suele ser muy sencilla y solo requiere unos pocos pasos, pero podríamos probar diferentes opciones.

Debemos tener en cuenta que HarperDB **funciona con NodeJS**, por lo que si no lo tenemos instalado, necesitaríamos instalarlo primero.

### Instalar y empezar HarperBD

Luego puedes instalar HarperDB con NPM e iniciarlo:

``$ npm install -g harperdb``\
``$ harperdb``

HarperDB se iniciará automáticamente después de la instalación.

### Instalación sin conexión

Podemos instalar HarperDB compilando desde el código fuente o usando npm para instalar HarperDB.

**Usando npm:**
``npm install -g harperdb-X.X.X.tgz harperdb install``

**Instalando desde el código fuente:**

Primero, necesitamos descargar el paquete [paquete de instalación](https://products-harperdb-io.s3.us-east-2.amazonaws.com/index.html)

**Nota:** si queremos compilar desde el código fuente, necesitamos las siguientes dependencias:

- Go: versión 1.19.1
- GCC
- Make
- Python v3.7, v3.8, v3.9, o v3.10