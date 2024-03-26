
# Teoria:
## Es una capacidad como lo dice el nombre para tener permisos a cierta tarea privilegiada, Gracias a estos mecanismos el sistema crea un contexto de trabajo para cada usuario, en el cual ejecutan sus tareas con los privilegios asignados al mismo. Sin embargo, para realizar operaciones específicas es necesario que un usuario no privilegiado pueda, en ocasiones, adquirir temporalmente un perfil de superusuario (root) y poder realizar una tarea que suponga ciertos privilegios.

## Este objetivo se consigue principalmente atribuyendo privilegios a través de sudo, o asignando permisos especiales "set user-id" o setuid a un fichero ejecutable. Este mecanismo permite que un usuario adopte el rol del propietario del fichero cuando lo ejecuta, adquiriendo los mismos privilegios que éste. Este tipo de permiso se identifica con el atributo "s" al listar ficheros ejecutables, indicativo que el bit setuid está activo.

# Vulnerabilidad: 
## Es importante tener presente que estos mecanismos  traen consigo riesgos inherentes al cambio de contexto de privilegios que sucede durante la ejecución. Esta circunstancia constituye una brecha de seguridad cuando existe una vulnerabilidad en el ejecutable que permite tomar el control de la ejecución, escapando del contexto de seguridad del proceso manteniendo los privilegios.

# Es posible comprobar los ficheros que tienen permiso setuid con el comando:

```bash
find / -perm -4000 -exec ls -l {} \; 2>/dev/null
```

# Con getcap nos permite listar las capabilitis del sistema 

```bash
which getcap
getcap -r / 2>/dev/null
```

##### Fuentes
[Linux Capabilities](https://www.incibe-cert.es/blog/linux-capabilities)
[Linux Capabilities 2](http://www.etl.it.uc3m.es/Linux_Capabilities)
