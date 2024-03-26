### A través del archivo de configuración ‘.bashrc‘ o ‘.zshrc‘, es posible definir una serie de acciones a llevar a cabo a la hora de obtener una consola interactiva, en este caso tras ingresar por SSH.

### Es por ello que tras ingresar, somos expulsados de forma inmediata, dado que así ha sido definido en el archivo de configuración ‘.bashrc‘ para el caso que estamos tratando. Si colamos un comando al final de nuestra línea al aplicar una autenticación por SSH, lograremos que ese comando sea introducido a nivel de sistema antes de que se interprete el archivo de configuración pertinente.

# Conectarse a un host

```bash
ssh user@host 
```

# Conectar nuestro host a un puerto del usuario -p (numero de puerto)

```bash
ssh -p 0000 user@host
```

# Agregar nuestra clave al host para que el usuario habilite un inicio de sesión con clave o sin contraseña
```bash
ssh-copy-id user@host
```
