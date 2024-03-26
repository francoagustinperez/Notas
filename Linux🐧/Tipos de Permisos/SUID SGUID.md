# Permisos SUID y SGID

#### Vamos a practicar utilizando un binario de Python 3.9 como ejemplo.

# Obtener la ruta relativa del binario


`which python3.9`

# Cambiar los permisos SUID del binario


`chmod u+s /ruta/del/binario/python3.9`

# Búsqueda de binarios con permisos SUID


`find / -type f -perm -4000 2>/dev/null`

# Verificación de los permisos SUID de un binario



`ls -l /ruta/del/binario/python3.9`

# Cambio del identificador de usuario en Python

```python
import os

# Cambiar el identificador de usuario a root (0)
os.setuid(0)

# Ejecutar comandos como root
os.system("whoami")
```