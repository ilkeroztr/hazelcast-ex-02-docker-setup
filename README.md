# Hazelcast-EX-02: Hazelcast ve Management Center Docker Kurulumu

##  Proje Hakkında

Bu proje kapsamında **Hazelcast** ve **Hazelcast Management Center**, Google Cloud üzerinde bir VM kullanılarak **Docker** yardımıyla çalıştırılmıştır. Amaç, Hazelcast'in temel çalışma prensiplerini anlamak ve yönetim paneli üzerinden cluster kontrolü yapmaktır.

---

## ⚙ Kullanılan Teknolojiler

- 🐳 Docker
- ☁️ Google Cloud Platform (GCP) – Compute Engine VM (Debian)
- 🌩️ Hazelcast
- 🌐 Hazelcast Management Center

---

##  Proje Yapısı
hazelcast-ex-02-docker-setup/
├── README.md                → Proje açıklaması
├── hazelcast-setup.docx     → Yazılı rapor
├── docker-ps.png            → Çalışan container’ların terminal çıktısı
├── hazelcast-ui.png         → Hazelcast Management Center arayüzü

---

##  Kurulum Adımları

### ️ Docker Image'lerini Çek

```bash
sudo docker pull hazelcast/hazelcast
sudo docker pull hazelcast/management-center
```
2️⃣ Hazelcast Container’ını Başlat
```bash
sudo docker run -d --name hazelcast -p 5701:5701 hazelcast/hazelcast
```
3️⃣ Management Center Container’ını Başlat
```bash
sudo docker run -d --name hazelcast-mc -p 8080:8080 hazelcast/management-center
```
4️⃣ Container’ların Çalıştığını Kontrol Et
```bash
sudo docker ps
```
5️⃣ Management Center’a Tarayıcıdan Eriş
```bash
http://35.205.10.107:8080
```
