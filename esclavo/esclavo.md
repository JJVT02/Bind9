# Instalar BIND
Puedes instalar el servidor DNS BIND si aún no lo tienes en tu sistema. Utiliza el gestor de paquetes de tu distribución para instalarlo. Por ejemplo, en sistemas basados en Debian/Ubuntu, puedes usar el siguiente comando:
```bash
sudo apt-get install bind9
```

# Archivos de configuracion
/etc/bind/named.conf.local: En este archivo, debes configurar la zona que deseas que tu servidor DNS esclavo replique desde el servidor DNS maestro. Por ejemplo:

```bash
zone "midominio.com" {
    type slave;
    masters { IP_DEL_SERVIDOR_DNS_MAESTRO; };
    file "midominio.com.zone";
};
```

/etc/bind/named.conf.options: En este archivo, configura las opciones globales para tu servidor DNS, como los servidores raíz a consultar, las direcciones IP a las que escuchar, entre otras.
