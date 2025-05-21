# home-server-docs

## Tabla de contenido
<!-- TOC -->

- [home-server-docs](#home-server-docs)
    - [Tabla de contenido](#tabla-de-contenido)
    - [Descripción](#descripci%C3%B3n)
    - [Información del servidor](#informaci%C3%B3n-del-servidor)
        - [Propósito](#prop%C3%B3sito)
        - [Configuración Red](#configuraci%C3%B3n-red)
    - [Cosas a hacer](#cosas-a-hacer)
    - [Servicios](#servicios)
    - [Estructura de carpetas](#estructura-de-carpetas)

<!-- /TOC -->



## Descripción 

Documentación para mi servidor de casa. 

Contiene información general sobre el servidor, su propósito y su configuración.

### Propósito
El servidor es una máquina reciclada que corre Ubuntu Server LTS. Su objetivo principal es funcionar como alternativa privada a Google Photos mediante Immich. También se usará para alojar proyectos personales, respaldos automáticos, y otros servicios de utilidad para el hogar o el desarrollo.


## Credenciales
### Usuarios
```
usuario: ianchu0317
contraseña: <mi contraseña xdxd>
```

### Red local `VALO 2.4`
La red local conectada tiene las siguientes credenciales.
```bash
SSID: VALO 2.4
PASSWORD: valorant123
```

## Conexiones
### Conexión local (LAN)
Localmente en red del módem, el servidor se encuentra como `server.local` utilizando **mDNS (Avahi)**, así evita usar IP estático.

Por ejemplo para conectar lpor comando localmente sería:
```bash
ssh ianchu0317@server.local
``` 

### Conexión afuera (WAN)

En el futuro se configurará **DDNS** para acceder al servidor desde fuera de la red local, sin necesidad de conocer la IP pública.


## Cosas a hacer
- [ ] Configurar IP estática por cable Ethernet.
- [ ] Configurar IP estática por Wi-Fi.
- [ ] Configurar nombre de host `server` y habilitar avahi-deamon para acceso por `server.local`.
- [ ] Configurar cuenta GitHub y Git.


## Servicios
**Prioridad**
- [ ] **Immich**: Alternativa a Google Photos para almacenar fotos y videos.
- [ ] **DDNS**: Servicio de DNS dinámico para acceder al servidor desde fuera de la red local.
- [ ] **OpenVPN**: VPN para acceder a la red local de forma segura desde fuera.
- [ ] **WireGuard**: Alternativa a OpenVPN, más rápida y fácil de configurar.

**Otros servicios útiles**
- [ ] **Nextcloud**: Almacenamiento en la nube privado.
- [ ] **Plex**: Servidor de medios para transmitir películas y programas de televisión.
- [ ] **Backup**: Copias de seguridad automáticas.

**Otros usos pensados**
- [ ] Hostear proyectos personales.
- [ ] Hostear un blog personal.

## Estructura de carpetas
