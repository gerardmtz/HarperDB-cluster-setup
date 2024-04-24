## Operaciones básicas de SQL CRUD

El analizador de SQL todavía está en desarrollo activo, muchas características de SQL pueden no estar optimizadas o utilizar índices. Este documento se actualizará a medida que estén disponibles más características y funcionalidades. En general, la **interfaz REST** proporciona una interfaz más estable, segura y de alto rendimiento para la interacción de datos, pero la funcionalidad de SQL puede ser útil para consultas administrativas ad-hoc y para utilizar sentencias SQL existentes.

HarperDB se adhiere al concepto de base de datos y tablas. Esto permite a los desarrolladores aislar las estructuras de las tablas entre sí, todo dentro de una misma base de datos.

Las operaciones básicas de SQL CRUD que podrían utilizarse son:

- **Crear (Insertar):** Para insertar un nuevo registro en una tabla, puedes usar la sentencia INSERT

```json
{
  "operation": "sql",
  "sql": "INSERT INTO dev.dog (id, dog_name) VALUES (22, 'Simon')"
}
```

- **Leer (Seleccionar):** Para consultar datos de la base de datos, puedes usar la sentencia SELECT

```json
{
  "operation": "sql",
  "sql": "SELECT * FROM dev.dog WHERE id = 1"
}
```

- **Actualizar:** Para cambiar los valores de los atributos especificados en una o más filas de una tabla de la base de datos, puedes usar la sentencia UPDATE

```json 
{
  "operation": "sql",
  "sql": "UPDATE dev.dog SET dog_name = 'penelope' WHERE id = 1"
}
```

- **Eliminar:** Para eliminar una o más filas de datos de una tabla de la base de datos, puedes usar la sentencia DELETE

```json
{
  "operation": "sql",
  "sql": "DELETE FROM dev.dog WHERE id = 1"
}
```
