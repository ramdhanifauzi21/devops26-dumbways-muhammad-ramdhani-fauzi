# Task6

## 1.  Gambar Sturktur Web Server Menggunakan Reverse Proxy

<img width="496" height="233" alt="Revers Proxy" src="https://github.com/user-attachments/assets/5dbb91f6-09ad-4e3a-8fdf-5431a813eef1" />

**Cara kerja:**

User/browser mengakses domain misalnya 'http://wayshub" ➜ Request pertama kali akan diterima oleh revers proxy(nginx) yang sedang berjalan di server 
➜ Nginx akan membaca servername dan location untuk menentukan kemana request diteruskan ➜ Jika request menuju 'washub' maka nginx akan meneruskan ke NodeJs(wayshub)
➜ Web server akan memproses request tersebut dan menghasilkan response berupa halaman web atau data ➜ Response akan dikirm kembali ke nginx
➜ Nginx meneruskan response tersebut ke browser user sehingga website dapat ditampilkan.

## 2. Membuat Reverse Proxy untuk Aplilkasi wayshub dan Domain Menggunakan fauzi.xyz

- Buka notepad terlebih dahulu dan jalankan sebagai administratos
- Buka file host yang berada di **C:windows/system32/drivers/etc**
<img width="624" height="299" alt="notepad" src="https://github.com/user-attachments/assets/7d78b940-8a68-4314-b51e-4c2f6fa35334" />

- Ketikkan dibagian terbawah **192.168.1.208(IP Server)** **fauzi.xyz(Nama Domain)**
<img width="610" height="520" alt="isinotepad" src="https://github.com/user-attachments/assets/2a527888-6eb4-49fa-bf19-ad96225cd4a0" />

- Buka server dan instal nginx: **$sudo apt install nginx**
<img width="624" height="210" alt="installnginx" src="https://github.com/user-attachments/assets/bed34a45-34d1-4691-a3ab-cb453780fc11" />

- Cek status nginx dan pastikan statusnya active(running): **$sudo systemctl status nginx**
<img width="624" height="206" alt="statusnginx" src="https://github.com/user-attachments/assets/3cdda19d-a9cf-4e2f-be41-bdc47c262bdf" />

- Pastikan port 80 dan 443 memiliki akses, karna HTTP dan HTTPS berjalan di port 80 dan 443
<img width="520" height="399" alt="ufw" src="https://github.com/user-attachments/assets/dc2be4b7-f442-44d8-9948-3b88296f4f33" />

- Masuk ke folder /etc/nginx/sites-enabled: **$cd /etc/nginx/sites-enabled**
<img width="624" height="87" alt="masukfolder" src="https://github.com/user-attachments/assets/d6148df5-a161-4d9d-90fb-4fa0cad7aab9" />

- Buat file baru dengan menambahkan sudo: **$sudo nano dumbflix.conf**, Karna setiap berada didalam folder etc harus bertindak sebagai admin
- Masukkan program dan save
 <img width="624" height="217" alt="program" src="https://github.com/user-attachments/assets/ed2676e1-523c-439e-aab2-aca09bcb2708" />

- Cek hasil program tadi: **$sudo nginx -t**, Jika ada tulisan 'succesful' maka program benar
<img width="624" height="78" alt="cekfile" src="https://github.com/user-attachments/assets/9f025480-d23a-4d6b-a5ca-f5795034aa42" />

- Lakukan reload nginx dan cek status nginx kembali pastikan active(running): **$sudo systemctl nginx**
<img width="975" height="388" alt="image" src="https://github.com/user-attachments/assets/91a3368b-6271-4122-8707-7ecadba3ffaa" />

- Masuk browser lalu masukkan domain yang sudah dibuat tadi pastikan menggunakan http jangan https: **http://fauzi.xyz**
<img width="624" height="321" alt="hasil" src="https://github.com/user-attachments/assets/acd01d34-5d7e-4cc9-8efc-6a611b584397" />
