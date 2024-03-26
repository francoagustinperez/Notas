# Netcat
### es una herramienta de línea de comandos que sirve para escribir y leer datos en la red. Para la transmisión de datos, Netcat usa los protocolos de red TCP/IP y UDP.
### La herramienta proviene originalmente del mundo de Unix; desde entonces, se ha expandido a todas las plataformas.
### Gracias a su universalidad, a Netcat se la llama “la navaja suiza del TCP/IP”. 
### Puede utilizarse, por ejemplo, para diagnosticar errores y problemas que afecten a la funcionalidad y la seguridad de una red. Netcat también puede escanear puertos, 
### hacer streaming de datos o simplemente transferirlos. Además, permite configurar servidores de chat y de web e iniciar consultas por correo.
### Este software minimalista, desarrollado a mediados de los 90, puede operar en modo servidor y cliente.
 

# Con netcat te puedes conectar a la propia maquina victima por el localhost que es el puerto 30000
```bash
nc localhost 30000
```

# Con esta ruta podemos ver los puertos abiertos
```bash
cat /proc/net/tcp
```


