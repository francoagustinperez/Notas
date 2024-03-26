

# Secuestro del Ancho de Banda de la red


# Tramas cts Clear To Send

```bash
tshark -r Captura-01.cap -Y "wlan.fc.type_subtype==28" 2>/dev/null
```

# Filtrar en Json (Jason)

```bash
tshark -r Captura-01.cap -Y "wlan.fc.type_subtype==28" -Tjson 2>/dev/null
```

#

```bash
tshark -r Captura-01.cap -Y "wlan.fc.type_subtype==28" -Tfields -e wlan.duration 2>/dev/null | sort -u
```

# Abrimos Wireshark y lo independizamos en segundo plano para que no moleste el output por pantalla

```bash
wireshark Captura-01.cap > /dev/null 2>&1 &
```

# Independizamos el proceso hijo para que se convierta en proceso padre

```bash
disown
```

# Filtro de wireshark

```bash
wlan.fc.type_subtype==28
```

# Elegimos paquete pinchamos y buscamos la Duration (En microsegundos)
# Pinchamos uno y seleccionamos arriba a la izquierda Exportar paquetes especificados, formato: Pcap.
# Lo llamamos ctsframe y marcamos la solapa de solo paquetes seleccionados

```bash
file ctsframe.pcap
```

```bash
apt install ghex -y
```

```bash
ghex ctsframe.pcap > /dev/null 2>&1 &
```
