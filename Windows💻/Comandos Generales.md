# Windows CMD

# Ver informacion sobre adaptadores de red

```powershell
ipconfig
```
# Ver tu IP publica (Conectado ETH)

```powershell
nslookup myip.opendns.com resolver1.opendns.com
```
# Conexiones activas
```bash
netstat -i
```
# Ver nuestros puertos en escucha
```bash
netstat -ano | find "3000"
```
# Matar el proceso
```bash
taskkill -F -PID 9308
```

# Cambiar extension de varios archivos
##### Utiliza el cmdlet `Get-ChildItem`para obtener una lista de archivos con la extensión que indiquemos. Luego, el cmdlet `Rename-Item` se utiliza para cambiar la extensión de cada archivo al deseado

```powershell
Get-ChildItem -Filter *.txt | Rename-Item -NewName { $_.Name -replace '\.txt$', '.md' }
```

