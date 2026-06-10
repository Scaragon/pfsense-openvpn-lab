# Этап 2: Настройка PKI (Certificate Manager)

## 2.1 Создание Certificate Authority

### Параметры CA:
- **Descriptive name:** MyVPN-CA
- **Method:** Create an internal Certificate Authority
- **Key length:** 2048
- **Digest Algorithm:** SHA256
- **Lifetime:** 3650 дней (10 лет)
- **Common Name:** pfsense-vpn-ca
- **Organization Name:** MyLab

## 2.2 Создание серверного сертификата

### Параметры сертификата:
- **Descriptive name:** openvpn-server
- **Method:** Create an internal Certificate
- **Certificate authority:** MyVPN-CA
- **Key length:** 2048
- **Digest Algorithm:** SHA256
- **Lifetime:** 3650 дней
- **Common Name:** pfsense.local
- **Certificate Type:** Server Certificate

### Alternative Names:
- **Type:** FQDN or Hostname, **Value:** pfsense.local
- **Type:** IP address, **Value:** 192.168.1.1

## 2.3 Результат

В Cert. Manager создано:
- ✅ 1 Certificate Authority (MyVPN-CA)
- ✅ 1 Server Certificate (openvpn-server)