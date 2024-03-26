# Saber que usuario eres.
```bash
whoami
```

# Lo mismo pero en ruta absoluta.
```bash
/usr/bin/whoami
```

# Cada binario tiene una ruta absoluta la podemos ver con.
```bash
which
```

# En caso de que which no exista podemos usar.
```bash
command -v
```

# Printear en pantalla el contenido de un archivo.
```bash
cat
```

# Mostrar grupos se hace cateando y nombrandole el directorio.
```bash
cat /etc/group
```

# Que se muestre algo por pantalla.
```bash
echo
```

# Algunas variables para ver su contenido necesita poner delante un $ por ej con la variable PATHs
```bash
echo $PATH
```

# Listar los grupos en los que se incluye el usuario actual (muestra nombre del grupo y un numero que es el identificador)
```bash
id
```

# De esta forma listamos los grupos con un bin cat el cual no recomiendo ya que es mas dificil de encontrar lo que buscamos.
```bash
/bin/cat /etc/group
```

# Grepeamos para filtrar por una palabra en especial
```bash
/bin/cat /etc/group | grep "floppy"
```

# Este grep tiene el parametro -n el cual se puede utilizar para filtrar y ver en que linea esta la palabra a grepear.
```bash
/bin/cat /etc/group | grep "floppy" -n
```

# Hay diferentes tipos de shells yo recomiendo usar la zsh.

# Los tipos de shells se ven desde esta ruta.
```bash
cat /etc/shells
```

# Concatenar comandos se hace con punto y coma. ;
```bash
whoami; ls 
```

# Con el aspersan o tambien llamado ant (&&) hacemos lo mismo pero solo se ejecutara el segundo comando si el primero es exitoso.
```bash
whoami && ls
```


# Si en vez de usar ANT usamos OR (||) aunque el primer comando de error el segundo puede ser exitoso.
```bash
whoami || ls
```

# Para ver el codigo de estado de un comando.
```bash
echo $?
```

# Si vemos que da 0 es que el comando anteriormente introducido es exitoso si da mas quiere decir que NO lo fue.

# Tambien puedes redirigir errores para no verlos en pantalla, el STDERR es el 2 y con > lo redirigimos.
```bash
whoam 2>/dev/null
```

# El /dev/null es un recurso que tenemos por defecto, es como un agujero negro podemos redirigir ahi lo que no queremos

# Ocultar el output de un programa.
```bash
cat /etc/hosts &>/dev/null
```

# Forma rancia de ocultar el output.
```bash
cat /etc/host > /dev/null 2>&1
```

# Forma mas comoda. de esta forma tanto el STDOUT y STDEER no molestara.
```bash
cat /etc/host &>/dev/null
```

# Para abrir solo el proceso hijo que quieras y no moleste el output.
```bash
wireshark &>/dev/null
```

# Cada proceso tiene su PID (Numero de identificacion del proceso unico)

# Si quieres hacer lo mismo pero sin que dependa de el proceso principal (terminal) y puedas cerrarlo hacemos la prueba con wireshark.
```bash
wireshark &>/dev/null & disown
```
