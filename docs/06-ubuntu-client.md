# Этап 6: Настройка клиента Ubuntu Desktop 24.04

## 6.1 Установка VirtualBox и Ubuntu

### Параметры ВМ Ubuntu:
- **RAM:** 2048 MB
- **HDD:** 20 GB
- **Network:** Internal Network "lan" (как LAN pfSense)

## 6.2 Установка OpenVPN клиента

```bash
sudo apt update
sudo apt install openvpn network-manager-openvpn network-manager-openvpn-gnome
sudo systemctl restart NetworkManager