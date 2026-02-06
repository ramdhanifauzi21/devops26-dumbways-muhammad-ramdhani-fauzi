# 1. NodeJS + Python berjalan di background (tanpa kondisi attached di terminal)
Untuk NodeJs dan Python berjalan di background ada beberapa cara, namun saya menggunakan tool yaitu pm2(proses manager)
### NodeJS
- Install pm2: **$npm install -g pm2**
<img width="624" height="538" alt="installpm2" src="https://github.com/user-attachments/assets/91874ed5-ed77-45e7-a5d8-ec90afb8e830" />

- Cek versi pm2: **$pm2 -v**
<img width="405" height="82" alt="cekversi" src="https://github.com/user-attachments/assets/f4383f2f-1e04-4eec-a5ec-1c3179201083" />

- Membuat pm2 otomatis berjalan saat server boot: **$pm2 startup**, artinya jika server restart NodeJS & Python tetap hidup.
- Copy perintah **sudo env PATH=$PATH....**
<img width="624" height="104" alt="startupdansave" src="https://github.com/user-attachments/assets/3a159210-9343-402d-829d-9522a7c54699" />

- Save daftar aplikasi yang sedang berjalan: **$pm2 save**
<img width="483" height="81" alt="save" src="https://github.com/user-attachments/assets/fbbd5446-b257-462d-a6d7-48df409f66b1" />

- Masuk ke folder NodeJS yang akan dijalankan, Lalu ketikkan: **$pm2 start npm --name wayshub-frontend -- start**. Terminal masih bisa menjalankan perintah yang lain.
- Jalankan juga browsernya untuk mengecek hasil
<img width="624" height="212" alt="hasil" src="https://github.com/user-attachments/assets/856a4129-ee63-49c6-bc6a-ad21fdfc7d90" />

### Python
- Masuk ke folder python yang akan dijalankan
- Buat file masukkan program seperti dibawah ini.
<img width="624" height="220" alt="programfile" src="https://github.com/user-attachments/assets/ba63fe13-315f-4d94-b793-89e634c970cb" />

- Lalu ketikkan: **$pm2 start index.py --name "python-app" interpreter python3**. Terminal masih bisa menjalankan perintah yang lain.
- Buka web dan masukkan ip serta port yang digunakan
<img width="624" height="118" alt="hasil2" src="https://github.com/user-attachments/assets/27a7bca9-e7f3-45ca-a8f5-5b692f32170f" />


# 2. Golang bisa dibuka di browser, menampilkan text "Jangan lupa sahur baby gurl rawr"
- Masuk folder untuk golang, buat file dan masukkan program seperti dibawah ini
<img width="624" height="421" alt="programfile" src="https://github.com/user-attachments/assets/7eb235e3-be94-490d-88ef-31f6b8ee725f" />

- Bisa langsung dijalankan: **$go run challenge.go**
- Cek browser untuk memastikan program berjalan
<img width="624" height="104" alt="hasil" src="https://github.com/user-attachments/assets/3613d432-cdab-4516-bd2f-01565bcb2cf1" />

