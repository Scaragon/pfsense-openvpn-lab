# Этап 4: Создание пользователя и клиентского сертификата

## 4.1 Создание пользователя

### Параметры пользователя:
- **Username:** vpnuser
- **Password:** user123
- **Full name:** VPN User
- **Certificate:** Создан автоматически

## 4.2 Настройка сертификата пользователя

### Параметры сертификата:
- **Descriptive name:** vpnuser-cert
- **Certificate authority:** MyVPN-CA
- **Key length:** 2048
- **Lifetime:** 3650 дней
- **Common Name:** vpnuser

## 4.3 Экспорт клиентской конфигурации

1. Перешел в **VPN → OpenVPN → Client Export**
2. Скачал файл конфигурации для vpnuser
3. Файл: `pfSense-UDP4-1194-vpnuser-config.ovpn`
4. Перенес файл на Ubuntu клиент

## 4.4 Результат

- ✅ Пользователь vpnuser создан
- ✅ Клиентский сертификат сгенерирован
- ✅ Конфигурационный файл .ovpn получен