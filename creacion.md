# Creación de archivos de zona
Los archivos de zona contienen los registros DNS para un dominio específico. Debes crear un archivo de zona en la ubicación especificada en el archivo de configuración y definir los registros DNS necesarios.

Por ejemplo, para crear un archivo de zona llamado db.tudominio.com, utiliza el siguiente comando:

```bash
sudo nano /etc/bind/zones/db.tudominio.com
```
Luego, puedes agregar registros DNS como el SOA, NS, MX, y otros, según tus requisitos específicos.

Agrega registros DNS, por ejemplo:
```bash
$TTL 1D
@   IN SOA  ns1.tudominio.com. admin.tudominio.com. (
           2023103001  ; Serial
           8H ; Refresh
           2H ; Retry
           1W ; Expire
           1D ; Minimum TTL
       )

@   IN NS  ns1.tudominio.com.
@   IN MX 10 mail.tudominio.com.

ns1   IN A  192.168.1.100
mail  IN A  192.168.1.101
```
