##### Fuentes
[Chuleta Comandos](https://ciberninjas.com/chuleta-comandos-linux/)
[Bash Redirection Chuleta](https://hack4u.io/wp-content/uploads/2022/05/bash-redirections-cheat-sheet.pdf)

# Aclarar que donde utilizo corchetes es porque va tu informacion personalizada los corchetes no van en ninguno de los comandos
# Comandos basicos para moverte dentro de los directorios:

# Crear carpeta (directorio)
```bash
mkdir [nombredirectorio]
```

# Para moverte a esa carpeta.
```bash
cd [directorio]
```

# Para eliminar esa carpeta.
```bash
rm -r [directorio]
```

# Para eliminar todos los archivos terminados igual .sh .py etc
```bash
rm *.odt
```

# Si usamos asterisco al empezar y terminar una palabra clave borraremos todos los archivos qe contenga esa palabra en su titulo
```bash
rm -r *Borrar-eliminar*
```

# Eliminar todos los archivos de una carpeta determinada nos situamos en ella y aplicamos
```bash
rm -r *
```

# Eliminar varios a la vez sin necesidad de que se llamen parecido usamos rm y espacios
```bash
rm eliminame1.odt eliminame2.odt
```

# Listar el contenido del directorio.
```bash
ls
ll
```

# Listar permisos avanzados de cada directorio.
```bash
ls -l
ll
```

# Listar mediante ruta absoluta.
```bash
ls /bin/
```


# Ver ruta actual.
```bash
pwd
```

# Volver un directorio atras.
```bash
../
cd ..
```

# Para volver al directorio home de tu usuario usamos
```bash
cd
```

# Para crear un archivo de texto con el editor nano que viene por defecto
```bash
nano [elnombreyextensionquequeramos]
```

# Eliminar el contenido de un archivo sin borrarlo
```bash
truncate -s 0 nombredelarchivo
```

# Abrir programa de linux desde terminal
```bash
nohup nombreapp &
```

