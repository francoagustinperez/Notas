
# Escanear Red

```bash
airodump-ng wlan0
```

# Escanear filtando por canal  

```bash
airodump-ng -c <canal> <interfaz>
```

# Escanear red especifica por filtrado de ESSID o BSSID

```bash
airodump-ng -c <canal> --essid <essid><interfaz>
airodump-ng -c <canal> --bssid <bssid> <interfaz>
```

# Escanear + Guardado de paquetes
# recomendado crear una carpeta y guardarlos ahi en este caso le asigno el nombre "Captura"

```bash
airodump-ng -c <canal> -w Captura --bssid <bssid> <interfaz>
```
