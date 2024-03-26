
# Base64 es un sistema de numeración posicional que usa 64 como base. Es la mayor potencia que puede ser representada usando únicamente los caracteres imprimibles de ASCII.
### Esto ha propiciado su uso para codificación de correos electrónicos, PGP y otras aplicaciones.

# El algoritmo de codificación Base64 no es un algoritmo de cifrado
### se decodifica fácilmente y, por lo tanto, no debe utilizarse como un método de cifrado seguro.

### No recomiendo que utilicéis esta técnica para proteger datos confidenciales, ya que se puede tensar en cuestión de segundos. En tal caso, es recomendable emplear métodos de cifrado seguros.


# Para pasar una cadena a base 64 se hace de la siguiente manera
```bash
echo "Hola esto es una prueba" | base64
```

# Para cadenas mas largas por ejemplo el etc/host le agregamos -w 0 para que nos lo muestre todo en una misma linea
```bash
cat /etc/hosts | base64 -w 0
```

# Hacerlo alrevez agregamos la cadena y le concatenamos el base64 con -d
```bash
echo "SGsySBlc3RvIGVzIHVuYSBwCcnVlYmEK" | base64 -d
```


