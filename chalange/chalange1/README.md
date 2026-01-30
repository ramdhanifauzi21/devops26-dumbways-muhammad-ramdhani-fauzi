## Manipulasi Text dan Kofigurasi UFW Menggunakan Bash Script

1. Membuat file untuk diisi bash script nya: **$nano chalange.sh**
2. Setelah masuk ke file 'chalange.sh' Tulis program dan save.
<img width="624" height="803" alt="1" src="https://github.com/user-attachments/assets/6d18c581-c3ca-4ae3-b3ee-eab9ccd8f419" />

<img width="455" height="864" alt="2" src="https://github.com/user-attachments/assets/cc71cd8b-817b-4f5f-afa0-ce5b2992cb4f" />

Penjelasan:
- **#!/bin/bash** = Menentukan bahwa script ini dijalankan dengan bash shell.
- **manipulation="text_data.txt"**      = Variabel untuk file 'text_data.txt'
- **PORTS=(22 80 443 3000 5000 6969)**  = Array bash berisi daftar port yang akan dibuka di UFW
- **file_on()**      = Ini merupakan function, untuk menjalankan manipulasi text(membuat file, menambahkan kata, mencari kata, menggati kata)
- **echo "Hello Fauzi" > $manipulation**    = Membuat file baru 'text_data.txt' dan memberi isi nya "Hello Fauzi"
- **echo "Saya sedang mempelajari Bash Script" >> $manipulation**  = Menambahkan isi "Saya sedang mempelajari Bash Script" ke baris dalam file 'text_data.txt' tanpa menghapus isi sebelumnya
- **cat $manipulation**  = Menampilkan isi file 'text_data.txt' ke terminal
- **grep "mempelajari" $manipulation** = mencari kata 'mempelajari' di file 'text_data.txt'
- **sed -i 's/Mempelajari/Belajar/g' $manipulation** = Mengganti kata 'Mempelajari' menjadi 'Belajar' di file 'text_data.txt'
- **echo "\nHasil Setelah Menggunakan Sed:"**

  **cat $TEXT_FILE** = Menampilkan file hasil setelah menggunakan 'sed'
- **task3_off(){** = function untuk menghapus manipulasi text yang ada di function 'file_on'
echo "===== TASK 3: CLEANUP ====="
if [ -f "$TEXT_FILE" ]; then
rm $TEXT_FILE
echo "[+] File $TEXT_FILE dihapus"
else
echo "[-] File tidak ditemukan"
fi
}


# --------------------------
# TASK 4 FUNCTIONS
# --------------------------


task4_on() {
echo "===== TASK 4: UFW CONFIG ====="


sudo ufw enable


for port in "${PORTS[@]}"
do
sudo ufw allow $port
echo "[+] Port $port dibuka"
done


echo "\nStatus UFW:"
sudo ufw status numbered
}


task4_off() {
echo "===== TASK 4: UFW RESET ====="


sudo ufw disable
sudo ufw reset


echo "[+] UFW dimatikan & konfigurasi dihapus"
}


# --------------------------
# MAIN
# --------------------------


if [ "$1" == "on" ]; then
echo "MODE: AKTIFKAN KONFIGURASI"
task3_on
task4_on


elif [ "$1" == "off" ]; then
echo "MODE: MATIKAN KONFIGURASI"
task3_off
task4_off


else
echo "========================================"
echo "USAGE:"
echo " ./day3.sh on -> Aktifkan Task 3 & 4"
echo " ./day3.sh off -> Hapus Task 3 & 4"
echo "========================================"
fi


3. Jalankan program
<img width="531" height="436" alt="3" src="https://github.com/user-attachments/assets/785a0df7-18d2-4174-be26-ea69a386ec36" />

<img width="365" height="61" alt="4" src="https://github.com/user-attachments/assets/c8a3c35d-b1b0-43ae-bbf9-c53762875ccc" />

<img width="624" height="572" alt="5" src="https://github.com/user-attachments/assets/18fbb872-8802-4283-ad52-0fca61d6ac66" />

<img width="624" height="291" alt="6" src="https://github.com/user-attachments/assets/ebbd3c0e-d3af-4a37-9699-c88ac0029876" />
