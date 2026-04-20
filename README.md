# LIVE🔴 Streaming Web Server

Bu proje, **Debian 13** üzerinde çalışan, **Nginx RTMP** modülü ile optimize edilmiş ve **10.000 eşzamanlı izleyici** kapasitesini hedefleyen yüksek performanslı bir canlı yayın sunucusudur.

## 🛠 Teknik Özellikler
- **İşletim Sistemi:** Debian 13 (64-bit)
- **Dağıtım Protokolü:** HLS (HTTP Live Streaming)
- **Depolama:** RAM Disk (tmpfs) - I/O darboğazını önlemek için.
- **Kapasite:** 10 Gbps Omurga / 65.535 File Descriptor limiti.
- **Gecikme:** ~3-5 Saniye (Düşük Gecikmeli Yapılandırma).



## 📂 Dosya Yapısı
- `/etc/nginx/nginx.conf`: Nginx ve RTMP ana konfigürasyonu.
- `/var/www/html/index.html`: IP bağımsız, Video.js tabanlı web oynatıcı.
- `/tmp/hls/`: Yayının parçalandığı RAM üzerindeki geçici klasör.

## 🚀 Hızlı Başlangıç & Komutlar

### 1. Servis Kontrolü
Konfigürasyonda değişiklik yaptıktan sonra mutlaka test edin:
```bash
sudo nginx -t && sudo systemctl status nginx
