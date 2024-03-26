
# Mostrar MAC de la interfaz

```bash
macchanger -s wlan0
```

# Como cambiar tu MAC diferentes formas

```bash
macchanger --mac=00:20:91:34:56:76 wlan0
```

# Solo numeros del 1 > 9 y letras, A > F

# Cambiamos al dispositivo deseado de la lista que podemos ver con

```bash
macchanger -l
```

# Podemos Grepear para encontrar una en concreto

```bash
macchanger -l | grep -l "NATIONAL SECURITY AGENCY"
```

# Y finalmente la cambiamos a la que elegimos ejemplo

```bash
macchanger --mac=00:20:91:DA:AF:91 wlan0
```

# La forma mas facil de cambiar tu mac aleatoriamente.
# Apagar interfaz

```bash
ifconfig wlan0 down
```
# Cambiar mac

```bash
macchanger -br wlan0
```

# Encender interfaz

```bash
ifconfig wlan0 up
```

