# Crearte un usuario.
```bash
adduser tunombrehacker
```

# Darle permisos para usar el comando sudo de administrador al usuario que creamos con nuestro nombre.
```bash
usermod -aG sudo TunombreHacker
```

# Configuramos nuestra zsh
```bash
chsh -s /bin/zsh tunombrehacker
```

