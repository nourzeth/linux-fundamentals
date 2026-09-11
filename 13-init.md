# Linux Init system & Upstar & Systemd
> 'init' (initialization) - bu Linux operatsion tizimi yuklaganda (boot sequnce) ishag tushadigan **birinchi jarayon (Process ID = 1)**. U tizimdagi barcha boshqa servis va boshqa jarayonlarni (daemons) boshqaradi. 
- - -
## 1. Asosiy Init Turlari
| Init Tizimi | Status | Xususiyati | 
| :--- | :--- | :--- | 
| SysVinit | Eski (Legacy) | Ketma-ket (Sequential) scriptlarni ishga tushiradi va sekin |
| Upstart | Eski (Ubuntu) | Voqealarga asoslangan (Event-based) | 
| systemd | Zamonaviy Standart | Parallel ishga tushadi, va zamonaviy Linux distribution'larda asosiy inint hisblanadi. |
---
## 2. Systemd va 'systemctl' Buyruqlari
Zamonaviy Linux'da servislarni boshqarish uchun 'systemctl' buyrug'idan foydalaniladi.
### Asosiy buyruqlar:
```bash

# Servis holatini tekshirish
systemctl status  <service_name>

# Serviceni ishga tushirish/to'xtatish
sudo systemctl start <service_name>
sudo systemctl stop <service_name>

# Serviceni qayta yuklash
sudo systemctl restart <service_name> 