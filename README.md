# pfSense OpenVPN Remote Access Lab

Лабораторная работа по настройке VPN-сервера на базе pfSense CE с использованием OpenVPN (Remote Access SSL/TLS) и PKI инфраструктуры.

## 📚 Описание проекта

### Используемые технологии:
- **Шлюз:** pfSense CE 2.8.1
- **Клиент:** Ubuntu Desktop 24.04
- **VPN:** OpenVPN (режим Remote Access SSL/TLS)
- **PKI:** Встроенный мастер сертификатов pfSense
- **Firewall:** pf (настройка доступа в LAN)
- **Виртуализация:** VirtualBox

### Сетевая топология:
- **WAN:** DHCP (10.0.2.15/24)
- **LAN:** 192.168.1.1/24
- **OpenVPN Pool:** 10.0.8.0/24

---

## 📖 Пошаговая документация

1. [Установка pfSense](docs/01-installation.md)
2. [Настройка PKI](docs/02-pki-setup.md)
3. [OpenVPN сервер](docs/03-openvpn-server.md)
4. [Пользователи и сертификаты](docs/04-user-certificates.md)
5. [Правила фаервола](docs/05-firewall-rules.md)
6. [Клиент Ubuntu](docs/06-ubuntu-client.md)
7. [Тестирование](docs/07-testing.md)

---

## 🎥 Видео демонстрация

[Смотри видео в папке video/demo.mp4]

---

## 📁 Структура репозитория
pfsense-openvpn-lab/
├── README.md
├── docs/ # Пошаговая документация
├── screenshots/ # Скриншоты (в Word документе)
├── video/ # Видео демонстрация
└── configs/ # Конфигурационные файлы

---

## ✅ Результаты

- ✅ OpenVPN сервер настроен и запущен
- ✅ Пользователь vpnuser создан с сертификатом
- ✅ Клиент Ubuntu подключается к VPN
- ✅ Клиент получает IP из пула 10.0.8.0/24
- ✅ Доступ к веб-интерфейсу pfSense по 192.168.1.1 работает
- ✅ Ping проходит без потерь (0% packet loss)

---

## 👤 Авторы

Галай Андрей, Тарасов Алексей

## 📄 Лицензия

MIT License 
