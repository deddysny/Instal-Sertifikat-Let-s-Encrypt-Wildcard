# Instal-Sertifikat-Let-s-Encrypt-Wildcard
## Getting started

## Tools and materials
- Ubuntu Server/VPS
- Koneksi Internet

## Stages/Tahapan Instalasi
-  Install Certbot. Karena Certbot belum tersedia dalam repositori milik Ubuntu, maka kita perlu menambahkannya terlebih dahulu melalui terminal. Caranya:
-  `sudo add-apt-repository ppa:certbot/certbot`
-  Setelah repositori berhasil ditambahkan, update paket-paket yang ada di Ubuntu:
-  `sudo apt update`
-  Setelah update, jalankan perintah berikut untuk memasang Certbot:
-  `sudo apt install certbot`
* Note : Pastikan menggunakan certbot versi 0.22 atau di atasnya. Sebab versi certbot sebelum 0.22 tidak mendukung Wildcard Certificate.  
-  Certbot sudah terpasang, sekarang waktunya untuk generate sertifikat nya. Caranya:
-  `sudo certbot certonly --manual -d *.xxxxx.com -d xxxxx.com --agree-tos --no-bootstrap --manual-public-ip-logging-ok --preferred-challenges dns-01 --server https://acme-v02.api.letsencrypt.org/directory`
-  
