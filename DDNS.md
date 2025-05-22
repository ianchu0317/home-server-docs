## DDNS Hostnames 

`skibidi-server.ddns.net`
```
hostname: all.ddnskey.com
username: prt8dsy
email: prt8dsy@ddnskey.com
password: vDwZxXfmn8tf
```

## Configuración 
### Configuracion servicio `noip-duc`
Corre `noip-duc` como un servicio al iniciar sistema.

Para chequear `status`
```sh
sudo systemctl status noip-duc
```

Para iniciar
```sh
sudo systemctl enable --now noip-duc
```

Archivo en `/usr/lib/systemd/system/noip-duc.service`
O en `/etc/init.d/noip-duc`
```ini
[Unit]
Description=No-IP Dynamic Update Client
After=network.target auditd.service

[Service]
EnvironmentFile=/etc/default/noip-duc
ExecStart=/usr/local/bin/noip-duc
Restart=on-failure
Type=simple
 
[Install]
WantedBy=multi-user.target
```


### Configuración ENTORNO
`/etc/default/noip-duc`
```sh
## /etc/defaults/noip-duc (Debian) or /etc/sysconfig/noip-duc (RedHat, Suse)
## or anywhere you like.
NOIP_USERNAME=prt8dsy
NOIP_PASSWORD=vDwZxXfmn8tf

## Comma separated list of hostnames and group names
NOIP_HOSTNAMES=all.ddnskey.com

## Less common options
#NOIP_CHECK_INTERVAL=5m
#NOIP_EXEC_ON_CHANGE=
#NOIP_HTTP_TIMEOUT=10s
## ip methods: aws, http, http-port-8245, static:<IP>
#NOIP_IP_METHOD=dns,http,http-port-8245
#NOIP_LOG_LEVEL=info

## Daemon options should not be set if using systemd. They only apply when `--daemon` is used.
#NOIP_DAEMON_GROUP=
#NOIP_DAEMON_PID_FILE=
#NOIP_DAEMON_USER=
```