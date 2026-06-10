
---

### docs/07-testing.md

```markdown
# Этап 7: Тестирование VPN подключения

## 7.1 Проверка IP адреса VPN

```bash
ip addr show tun0

3: tun0: <POINTOPOINT,MULTICAST,NOARP,UP,LOWER_UP> ...
    inet 10.0.8.2/24 brd 10.0.8.255 scope global ...
ping -c 4 192.168.1.1
PING 192.168.1.1 (192.168.1.1) 56(84) bytes of data.
64 bytes from 192.168.1.1: icmp_seq=1 ttl=64 time=1.42 ms
64 bytes from 192.168.1.1: icmp_seq=2 ttl=64 time=2.48 ms
64 bytes from 192.168.1.1: icmp_seq=3 ttl=64 time=1.46 ms
64 bytes from 192.168.1.1: icmp_seq=4 ttl=64 time=1.42 ms

--- 192.168.1.1 ping statistics ---
4 packets transmitted, 4 received, 0% packet loss
ip route show
10.0.8.1 dev tun0 proto static metric 50
default via 192.168.1.1 dev enp0s3 ...
10.0.8.0/24 dev tun0 proto kernel scope link src 10.0.8.2 metric 50
192.168.1.0/24 via 10.0.8.1 dev tun0 proto static metric 50
cat /etc/resolv.conf
nameserver 127.0.0.53
options edns0 trust-ad
search local