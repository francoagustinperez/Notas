# Encender modo monitor

```bash
airmon-ng start wlan0
```
# Para apagar

```bash
airmon-ng stop wlan
```
# Cada vez que encedemos hay procesos que debemos matar para que wlan0 funcione correctamente

```bash
killall dhclient wpa_supplicant 2>/dev/null
```
# O Mejor

```bash
airmon-ng check kill
```

# Cada vez que se detiene el modo monitor y no vamos a capturar ni esnifear mas nada con la antena wifi reiniciamos los servicios para volver a tener internet en nuestro sistema operativo linux

```bash
/etc/init.d/networking restart
```
# o Tambien
```bash
sudo systemctl restart networking
```
