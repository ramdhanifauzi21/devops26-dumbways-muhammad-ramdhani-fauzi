## Manipulasi Text dan Kofigurasi UFW Menggunakan Bash Script

1. Membuat file untuk diisi bash script nya: **$nano chalange.sh**
2. Setelah masuk ke file 'chalange.sh' Tulis program dan save.
<img width="624" height="803" alt="1" src="https://github.com/user-attachments/assets/6d18c581-c3ca-4ae3-b3ee-eab9ccd8f419" />

<img width="455" height="864" alt="2" src="https://github.com/user-attachments/assets/cc71cd8b-817b-4f5f-afa0-ce5b2992cb4f" />

Penjelasan:
- **#!/bin/bash** = Menentukan bahwa script ini dijalankan dengan bash shell.
- **manipulation="text_data.txt"**      = Variabel yang diisi kan file dengan nama 'text_data.txt'
- **file_on()**      = Ini merupakan function yang dapat menjalankan manipulasi text(membuat file, menambahkan kata, mencari kata, menggati kata)
- **echo "Hello Fauzi" > $manipulation**    = Memberi isi "Hello Fauzi" pada variabel manipulation
- **echo "Saya sedang mempelajari Bash Script" >> $manipulation**  = Menambahkan isi "Saya sedang mempelajari Bash Script" ke baris dalam variabel manipulation tanpa menghapus isi sebelumnya
- **cat $manipulation**  = Menampilkan isi dari variabel manipulation ke terminal
- **grep "mempelajari" $manipulation** = mencari kata 'mempelajari' pada variabel manipulation
- **sed -i 's/Mempelajari/Belajar/g' $manipulation** = Mengganti kata 'Mempelajari' menjadi 'Belajar' pada variabel manipulation
- **echo "\nHasil Setelah Menggunakan Sed:"**

  **cat $manipulation** = Menampilkan file hasil setelah menggunakan 'sed'
- **file_off(){** = function yang dapat menghapus manipulasi text 
- **if [ -f "$manipulation" ]; then** = Membuat suatu kondisi, '-f' untuk cek file apakah ada file manipulation

  **rm $manipulation** = Jika ada maka hapus isi variabel manipulation
  **else echo "[-] File tidak ditemukan"** = jika kondisi tidak terpenuhi maka menalpilkan pesan "file tidak ditemukan"
  **fi** = menutup struktur if
- **port_on() {** = Function untuk membuka akses port dan mengaktifkan firewall
- **sudo ufw enable** = mengaktifkan firewall
- **$sudo ufw allow 22** = membuka akses port 22
- **$sudo ufw allow 80** = membuka akses port 80
- **$sudo ufw allow 443** = membuka akses port 443
- **$sudo ufw allow 3000** = membuka akses port 3000
- **$sudo ufw allow 5000** = membuka akses port 5000
- **$sudo ufw allow 6969** = membuka akses port 6969
- **$sudo ufw status** = Menampilkan status firewall UFW dan semua aturan (rule) yang aktif.
- **port_off() {** Function untuk menonaktifkan dan menghapus semua konfigurasi UFW
- **sudo ufw disable** = Mematikan firewall UFW
- **sudo ufw reset** = Menghapus semua konfigurasi UFW
- **if [ "$1" == "on" ]; then**
  
  **file_on**
  Kondisi(if) dimana argumen pertama dari command line($1) dibandingkan dengan string (file_on), jika kondisi benar maka perintah yang ada di function file_on akan dijalankan

- **elif [ "$1" == "file_of" ]; then**
  **file_off**
  Kondisi(if) dimana argumen pertama dari command line($1) dibandingkan dengan string (file_off), jika kondisi benar maka perintah yang ada di function file_off akan dijalankan.
- **elif [ "$1" == "port_on" ]; then**
  **port_on**
  Kondisi(if) dimana argumen pertama dari command line($1) dibandingkan dengan string (port_on), jika kondisi benar maka perintah yang ada di function port_on akan dijalankan.
- **if [ "$1" == "port_off" ]; then**
  **port_off**
  Kondisi(if) dimana argumen pertama dari command line($1) dibandingkan dengan string (port_off), jika kondisi benar maka perintah yang ada di function port_off akan dijalankan.
- **else** = kondisi jika tidak ada yang benar maka akan menampilkan pesan "Gunakan" "./chalange.sh file_on" "./chalange.sh file_on"
- **fi** = akhir dari perintah if

3. Memberi izin agar file chalange.sh bisa dijalankan (execute) Jika tidak maka file tidak bisa dijalankan
  <img width="357" height="39" alt="7" src="https://github.com/user-attachments/assets/ee7fbffa-3dc1-45f2-b764-badc53593f9b" />
 

4. Hasil
- Menjalankan program Manipulasi teks(membuat file, menambahkan isi, mencari kata, mengganti kata) : **$./chalange.sh file_on**
<img width="531" height="436" alt="3" src="https://github.com/user-attachments/assets/785a0df7-18d2-4174-be26-ea69a386ec36" />

- Menjalankan program Manipulasi teks(Menghapus file): **$./chalange.sh file_off**
<img width="365" height="61" alt="4" src="https://github.com/user-attachments/assets/c8a3c35d-b1b0-43ae-bbf9-c53762875ccc" />

- Menjalankan program menonaktifkan dan menghapus semua konfigurasi UFW: **$./chalange.sh port_off**
<img width="624" height="572" alt="5" src="https://github.com/user-attachments/assets/18fbb872-8802-4283-ad52-0fca61d6ac66" />

- Menjalankan program Konfigurasi UFW(MematikanMereset): **$./chalange.sh port_off**
<img width="624" height="291" alt="6" src="https://github.com/user-attachments/assets/ebbd3c0e-d3af-4a37-9699-c88ac0029876" />


