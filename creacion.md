# Creación de archivos de zona
Los archivos de zona contienen los registros DNS para un dominio específico. Debes crear un archivo de zona en la ubicación especificada en el archivo de configuración y definir los registros DNS necesarios.

Por ejemplo, para crear un archivo de zona llamado db.tudominio.com, utiliza el siguiente comando:

```bash
sudo nano /etc/bind/zones/db.tudominio.com
```
Luego, puedes agregar registros DNS como el SOA, NS, MX, y otros, según tus requisitos específicos.
