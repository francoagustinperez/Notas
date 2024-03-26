# Asi se ve los atributos de un directorio
```bash
lsattr directorio
```

# Entre todos los atributos que podemos agregar esta el atributo inmutable el cual se usa para que un archivo no puedo ser destruido ni modificado
```bash 
muchas maquinas de hack the box usan este atributo para que nadie pueda tocar nada de sus maquinas, igualmente hasta el dia de hoy se saben varios metodos para saltearse esto.
```

# Asi se quita el inmutable cuando tu eres el root.
```bash
chattr -i -V directorio 
```

# Atributos:
#### A:El tiempo (tiempo de acceso) del archivo no se puede modificar, lo que puede reducir la cantidad de E / S de disco, lo que es beneficioso para la computadora portátil al mejorar la duración de la batería.
#### S:Opción de sincronización de E / S del disco duro, función similar a la sincronización
#### a:Es decir, después de configurar este parámetro, solo puede agregar datos al archivo, pero no eliminarlo. Se utiliza principalmente para la seguridad del archivo de registro del servidor. Solo el root puede establecer este atributo.
#### i:El archivo no se puede eliminar, renombrar ni vincular, y el contenido no se puede escribir ni agregar (incluso si es un usuario root). Solo root puede establecer esta propiedad
#### c:Comprimir, el archivo se comprimirá automáticamente y luego se almacenará, y se descomprimirá automáticamente cuando se lea
#### d:Eso no es un volcado, el archivo de configuración no puede ser el objetivo de respaldo del programa de volcado
#### j:Es decir, diario, establezca este parámetro para que cuando el sistema de archivos se monte con el parámetro de montaje "datos = ordenados" o "datos = reescritura", el archivo se grabará primero cuando se escriba (en el diario). Si el parámetro del sistema de archivos se establece en data = journal, el parámetro es automáticamente inválido
#### s:Esa es una opción segura y confidencial. Cuando se elimina el archivo con el conjunto de atributos s, todos sus bloques de datos se escribirán en 0
#### u:Esa es la opción recuperar, recuperar. Al contrario de s, cuando se elimina un archivo, se conservan todos sus bloques de datos y el usuario puede restaurar el archivo en el futuro

# LSATTR

# utilizar lsattr El comando enumera los atributos ocultos del archivo. El formato de sintaxis es:
```bash
lsattr [ -RVadv ] [ files… ]
```

# Aca están los significados de varias opciones:

#### Opciones	sentido
#### -R	Visualice recursivamente los atributos de todos los subdirectorios y archivos en el directorio
#### -V	Mostrar información de la versión del programa lsattr
#### -a	Mostrar información de atributos de todos los archivos, incluidos los archivos que comienzan con.
#### -d	Mostrar los atributos del directorio, no los atributos de los archivos en el directorio
#### -v	Mostrar el número de archivo del documento

# Por ejemplo, el siguiente comando muestra los atributos ocultos del directorio directoriosecreto:
```bash
lsattr -Rd directoriosecreto/
```

# Vamos a practicar copiando un archivo.

```bash
cp/etc/hosts prueba
```

# Acabamos de crear una copia del directorio etc host la cual podemos manipular pero tranquilo sin alterar el fichero original.

```bash
chattr +i +e +v
```

# Asi estamos agregando los atributos al directorio +i para hacerlo inmutable y nadie pueda alterarlo ni borrar
#### +e para
#### y +V para hacerlo en modo vervose y que la consola nos valla mostrando el progreso en pantalla y ir adelantando trabajo


##### Fuentes
[Comandos CHATTR & LSATTR En Linux](https://programmerclick.com/article/5604675172/)
[CHATTR y LSATTR: control de atributos de ficheros Linux](https://rm-rf.es/chattr-y-lsattr-visualizar-y-modificar-atributos-en-sistemas-de-ficheros-linux/#:~:text=El%20primer%20comando%2C%20lsattr%20permite,chmod%2C%20chown%2Csetfacl…)

