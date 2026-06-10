# Этап 5: Настройка правил межсетевого экрана

## 5.1 Правило для OpenVPN интерфейса

### Параметры правила:
- **Interface:** OpenVPN
- **Action:** Pass
- **Address Family:** IPv4
- **Protocol:** Any
- **Source:** Any (10.0.8.0/24)
- **Destination:** Network 192.168.1.0/24
- **Description:** Allow VPN to LAN

**Назначение:** Разрешить VPN клиентам доступ к локальной сети

## 5.2 Правило для LAN интерфейса (OpenVPN порт)

### Параметры правила:
- **Interface:** LAN
- **Action:** Pass
- **Address Family:** IPv4
- **Protocol:** UDP
- **Source:** Any
- **Destination:** This Firewall (self)
- **Destination Port:** 1194 (OpenVPN)
- **Description:** Allow OpenVPN on LAN

**Назначение:** Разрешить входящие подключения к OpenVPN серверу

## 5.3 Существующие правила LAN

- ✅ Anti-Lockout Rule (разрешает доступ к GUI)
- ✅ Allow LAN to pfSense GUI
- ✅ Default allow LAN to any rule

## 5.4 Результат

Все необходимые правила firewall настроены для:
- Доступа VPN клиентов в LAN
- Приема подключений на порт 1194
- Доступа к веб-интерфейсу pfSense