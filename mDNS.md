
## Instalación de mDNS (Servidor)

Cambiar Hostname en servidor
```bash
sudo hostnamectl set-hostname server
```

Instalar avahi
```bash
sudo apt update
sudo apt install avahi-daemon
```

Iniciar servicio
```bash
sudo systemctl enable --now avahi-daemon
```

Verificar que el servicio está corriendo
```bash
sudo systemctl status avahi-daemon
```

## Instalación de mDNS (Cliente)

Instalar avahi
```bash
sudo apt install avahi-daemon libnss-mdns
```

Iniciar servicio
```bash
sudo systemctl restart avahi-daemon
```

Probar conexión
```bash
ping server.local
```
