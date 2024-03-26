### Si le agregamos un punto . a nuestro archivo o directorio sera oculto.

### A continuacion te mostrare como listarlos

# Utilizando ls y parametro -a , listamos los directorios ocultos
```bash
ls -a
```

# Si nos vamos hacia atras a la carpeta raiz y usamos find listamos archivos
```bash
..
find .
```

# El contenido de un archivo oculto se lista de esta manera
```bash
file .hidden
cat .hidden
```

# Otra forma de listar archivos
```bash
find . -type f
```

# Asi es como podemos filtrar por lo que nos interesa para no tener que buscar la flag entre todo el output
```bash
find . -type f | grep "hidden"
```

# Y sobre eso podemos aplicar un xargs para catearlo (siempre sobre la ruta)
```bash
find . -type f | grep "hidden" | xargs cat
```

# Con grep ademas tambien podemos quitar las lineas que no queremos ver por ejemplo bashrc
```bash
find . -type f | grep -v bashrc
```

# Cuando queremos quitar mas de una linea le agregamos una E junta o separada del parametro -v
```bash
find . -type f | grep -vE "bashrc|profile"
```

# Asi le agregamos mas cosas y obtendriamos justo lo que queremos en este caso, la flag de la maquina bandit
```bash\
find . -type f | grep -vE "bashrc|profile|logout" | xargs cat
```






