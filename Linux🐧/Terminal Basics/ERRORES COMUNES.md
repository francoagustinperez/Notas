# Tres errores y sus soluciones

# Error Initramsf este error se da por dejar varios procesos abiertos en nuestra maquina virtual
```bash
fsck -c -y /dev/sda1
```

# Error parrot deprecated dkms
```bash
sudo apt remove realtek-rtl8188eus-dkms
```

# Error fernwificracker no detecta interfaz si no nos cambia el nombre a mon
```bash
sudo ip link set wlan0 down
sudo ip link set wlan0 name wlan0mon
```


