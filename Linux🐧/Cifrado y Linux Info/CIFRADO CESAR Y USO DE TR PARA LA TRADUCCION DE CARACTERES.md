# El cifrado César lleva el nombre de Julio César. Es uno de los tipos de cifrados más antiguos y se basa en el cifrado monoalfabético más simple. Se considera un método débil de criptografía
### ya que es fácil decodificar el mensaje debido a sus técnicas de seguridad mínimas.

# De todos los cifrados de tipo de sustitución
### este cifrado de César es el más simple de resolver, ya que solo hay 25 combinaciones posibles.

# La idea es que rota depende que "rot" y con el numero de valor a su lado hacia adelante o atras 

# La siguiente pagina nos permite hacer un cifrado cesar automaticamente
[ROT13](https://rot13.com)

# Si lo quisieras hacer tu mismo, es englobando los rangos esto se hace marcando desde la letra que empieza hasta que -letra queremos
```bash
cat data.txt | tr '[G-ZA-Fg-za-f]' '[T-ZA-St-za-s]'
```

# Si queremos hacerlo en rot13 es mas facil
```bash
cat data.txt | tr '[G-ZA-Fg-za-f]' '[N-ZA-Mn-za-m]'
```


# En este caso nos interesa la parte final que pertenece a la contrasena de la maquina bandit12
```bash
cat data.txt | tr '[G-ZA-Fg-za-f]' '[N-ZA-Mn-za-m]' | awk 'NF{print $NF}'
```


