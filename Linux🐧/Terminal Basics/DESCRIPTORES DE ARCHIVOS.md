# Vamos a estar hablando de las redirecciones en bash empleando Descriptores de Archivos
# Esto no se utliza mucho pero a nivel de cultura general hay que saberlo es basico de linux.

# Jugamos con exec y un numero cualquiera para crear un Descriptor
# Con menor que < indicamos que queremos que tenga permiso de Lectura
# Con mayor que > indicamos que queremos que tenga un permiso de Escritura

# De esta forma podemos crear un descriptor de archivos.
```bash
exec 3<> file
```

# Si nosotros escribimos un comando en este caso whoami y usamos el siguiente redirector
# podemos hacer que el output (la respuesta del comando) se vea solo dentro de ese Descriptor que creamos.

# Esta es una manera de enviar output a el descriptor de archivo &>3.
```bash
whoami >&3
```

# Entonces si ahora abrimos file, el output estara en ese archivo.
```bash
cat file
```

# Todo lo adicional qe metamos despues lo almacenara por debajo en formato apent sin sobre escribir lo que ya existe por ej.
```bash
pwd >&3
```

# Lo comprobamos
```bash
cat file
```

# Cuando quieras cerrar un descriptor de archivo podemos jugar con exe, esto no quiere decir que pierdas el contenido.
```bash
exec 3>&-
```

# Comprobamos
```bash
cat file
```

# Ahora imaginemos nos creamos un archivo descriptor de archivo 5 con capacidad de lectura y escritura en el archivo data.
```bash
exec 5<> data
```

# Por ejemplo podemos crearnos copias entre descriptores de archivos

# De esta forma le indicamos que queremos hacer una copia del Descriptor de Archivo 5 en el Descriptor de Archivo 8 que estamos creando sobre la marcha.
```bash
exec 8>&5
```

# De esta forma vas a poder cerrar lo que quieras y hacer otras cosas sobre la marcha.



