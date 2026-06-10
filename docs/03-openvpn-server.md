# Этап 3: Настройка OpenVPN сервера

## 3.1 Создание сервера

### General Configuration:
- **Mode:** Remote Access (SSL/TLS + User Auth)
- **Backend:** Local Database
- **Protocol:** UDP4 on IPv4 only
- **Device mode:** tun - Layer3 Tunnel Mode
- **Interface:** LAN
- **Local port:** 1194

## 3.2 Cryptographic Settings:
- **Peer Certificate Authority:** MyVPN-CA
- **Server Certificate:** openvpn-server
- **DH Parameters Length:** 2048
- **ECC Curve:** prime256v1
- **Auth Digest Algorithm:** SHA256

## 3.3 Tunnel Settings:
- **IPv4 Tunnel Network:** 10.0.8.0/24
- **IPv4 Remote Network:** 192.168.1.0/24
- **IPv4 Local Network:** 192.168.1.0/24
- **Concurrent connections:** 10

## 3.4 Client Settings:
- **Dynamic IP:** Enabled
- **Topology:** subnet - One IP address per client
- **DNS Default Domain:** local
- **DNS Server 1:** 192.168.1.1
- **DNS Server enable:** Enabled

## 3.5 Запуск сервера

1. Включил сервис через консоль: `sysrc openvpn_enable=YES`
2. Запустил сервис: `service openvpn start`
3. Проверил статус: сервис запущен и работает