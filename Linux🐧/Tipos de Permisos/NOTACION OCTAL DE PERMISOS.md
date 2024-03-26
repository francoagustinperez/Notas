# Damos permiso de prueba a un archivo (file) testing ficticio

```bash
chmod 755 testing
```

#### r-x|r--|-w-
#### 101|100|010

```bash
chmod 542 testing
```

#### rwx|rwx|rwx
#### 421|421|421
#### 010|101|001
 

# Las tres primeros son los permisos del Propietario (P) de Grupo (G) y de Otros (O)

```bash
rwxr-xr-x  2 usuario usuario 4096 Jun 30 06:17 usuario
```

#### P   G   O
#### rwx rwx rwx


#### r > Read (Leer)
#### w > Write (Escribir)
#### x > Executable (Ejecucion)

##### Fuentes
[Permisos Sistema De Archivos](https://blog.alcancelibre.org/staticpages/index.php/permisos-sistema-de-archivos)
[Permisos y Atributos](http://mural.uv.es/oshuso/8339_permisos_y_atributos.html)
