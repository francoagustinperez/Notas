# cat /etc/passwd :
#### muestra información sobre todos los usuarios registrados en el sistema, como su nombre de usuario, número de identificación de usuario (UID), número de identificación del grupo (GID), directorio de inicio, shell predeterminado y otros detalles.

# passwd :
#### este comando se utiliza para cambiar la contraseña de un usuario existente. Si se ejecuta sin argumentos, cambia la contraseña del usuario actual. Se solicitará al usuario que proporcione su contraseña actual y luego se le pedirá que proporcione y verifique su nueva contraseña.

# useradd :
#### este comando se utiliza para crear nuevos usuarios en el sistema. Por ejemplo, para crear un nuevo usuario llamado "jane", puedes ejecutar el comando sudo useradd jane. Es posible que debas proporcionar más detalles, como el directorio de inicio, el shell predeterminado, etc.

# userdel :
#### este comando se utiliza para eliminar un usuario existente del sistema. Por ejemplo, para eliminar al usuario "jane", puedes ejecutar el comando sudo userdel jane. También puedes utilizar la opción -r para eliminar el directorio de inicio del usuario y todos sus archivos y subdirectorios: sudo userdel -r jane.

# usermod :
#### este comando se utiliza para modificar los detalles de un usuario existente. Por ejemplo, para cambiar el nombre completo del usuario "jane" a "Jane Smith", puedes ejecutar el comando sudo usermod -c "Jane Smith" jane. También puedes utilizar otras opciones para cambiar el directorio de inicio, el shell predeterminado, el grupo principal del usuario, etc.

# chown :
#### este comando se utiliza para cambiar el propietario de un archivo o directorio. Por ejemplo, para cambiar el propietario del archivo "file.txt" al usuario "jane", puedes ejecutar el comando sudo chown jane file.txt.

# chgrp :
#### este comando se utiliza para cambiar el grupo propietario de un archivo o directorio. Por ejemplo, para cambiar el grupo propietario del archivo "file.txt" al grupo "sales", puedes ejecutar el comando sudo chgrp sales file.txt.
