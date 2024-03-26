# Buscar archivos con un nombre específico en un directorio y sus subdirectorios:
```bash
find /ruta/a/buscar -name "nombre_archivo"
```

# Buscar archivos modificados en las últimas 24 horas:
```bash
find /ruta/a/buscar -mtime 0
```

# Buscar archivos que ocupen más de 100 megabytes:
```bash
find /ruta/a/buscar -size +100M
```

# Buscar archivos de un tipo específico, como archivos de texto:
```bash
find /ruta/a/buscar -type f -name "*.txt"
```

# Buscar archivos que pertenezcan a un usuario específico:
```bash
find /ruta/a/buscar -user nombre_usuario
```
