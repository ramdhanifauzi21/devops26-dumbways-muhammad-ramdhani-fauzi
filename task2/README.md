##1. Membuat sebuah diagram jaringan komputer dengan spesifikasi:

    - IP Class C : 192.168.4.xxx
    - CIDR Block : 192.168.11.0/24
    - Jumlah Client : 4

<img width="514" height="470" alt="Diagram network drawio (1)" src="https://github.com/user-attachments/assets/12923f84-7ff2-4d38-a89f-f29253b627e3" />


Penjelasan:
- CIDR Blok 192.168.11.0/24 = subnetmask 255.255.255.0. 

  Artinya:
  - Network: 192.168.11.0
  - Broadcast: 192.168.11.255
  - Range host :192.168.11.1-192.168.11.254 (ip unuk host yang dapat digunakan)
- Router memiliki 2 interface
  1. WAN
    - IP: 192.168.11.1
    - Network: 192.168.11.0/24
    - Yang berfungsi menyambungkan ke internet
  2. LAN
    - IP: 192.168.4.1
    - Network: 192.168.4.0/24
    - Yang berfungsi sebagai Gateway jaringan lokal(menghubungkan jaringan lokal dengan internet)

- Semua device berada di satu jaringan LAN, disini IP bisa diatur secara DHCP(otomatis mengisi IP dengan IP host yang sudah diatur) dan Static
- Untuk yang tertera di gambar, menggunakan static maka:
  - PC1 IP Address: 192.168.4.10
  - PC2 IP Address: 192.168.4.20
  - PC3 IP Address: 192.168.4.30
  - PC4 IP Address: 192.168.4.40 

##2. Perbedaan antara SH (Shell) dan BASH (Bourne-Again Shell)
- SH (Shell) merupakan generasi awal yang digunakan pada sistem Unix/Linux sebagai command interpreter dasar. Shell memiliki fitur yang sangat minimal dan hanya mendukung fungsi-fungsi dasar untuk menjalankan perintah dan script. SH memiliki syntax yang terbatas dan tidak mendukung fitur modern array, auto-complete, dan scripting lanjutan.
- Sedang BASH (Bourne-Again Shell) merupakan pengembangan dari SH yang dirancang sebagai versi modern dengan fitur yang jauh lebih lengkap. BASH mendukung auto-complete, command history, scripting lanjutan, array variable expansion yang  lebih fleksibel, serta kemudahan debugging script.

  Jadi secara sederhana SH adalah shell dasar yang bersifat legacy dan minimalis, sedangkan BASH merupakan versi pengembangan yang lebih modern, powerfull, dan user-friendly.


##3. Dokumentasi/Kumpulan Command Linux

- Update daftar repository package: **$sudo apt update**
<img width="610" height="210" alt="1" src="https://github.com/user-attachments/assets/1f66a034-b3f0-4c17-a1a8-dd43b8702897" />

- upgrade semua package: **$sudo apt upgrade**
<img width="282" height="23" alt="2" src="https://github.com/user-attachments/assets/b003f451-d950-4e1f-afd0-175e4cd7bf79" />

- Membuat folder bernama latihan1 : **$mkdir latihan1**
- Membuat file bernama baca1: **touch $baca1**
- Memindahkan file baca1 ke folder latihan1 : **$mv baca1 latihan1/baca1**
- Masuk ke folder latihan1: **$cd latihan1**
- Menampilkan daftar file dan folder dalam directory aktif: **$ls**
- Menyalin file baca1 ke baca2: **$cp baca1 baca2**
- Memantulkan/menampilkan tulisan HELLO FAUZI: **$echo "HELLO FAUZI"**
- menulis teks ke dalam sebuah file file1: **$echo "HELLO FAUZI" > file1**
- Menampilkan isi file secara langsung: **$cat file1**
- Keluar dari direktory: **$cd ..**
<img width="460" height="431" alt="3" src="https://github.com/user-attachments/assets/623edfbc-7c26-42d6-9c81-cd924dff31cc" />

- Menghapus file: **$rm baca2**
- Mengedit file menggunakan editor nano di file baca1: **$nano baca1**
<img width="332" height="134" alt="4" src="https://github.com/user-attachments/assets/d32f0501-4e1e-444c-a495-69e4db91c912" />
<img width="624" height="467" alt="5" src="https://github.com/user-attachments/assets/7b2864af-f7d7-4b73-b63f-51910878ba8c" />
<img width="393" height="57" alt="6" src="https://github.com/user-attachments/assets/7979d877-6bac-4642-a9dd-3172dfd54951" />

- Mencari kata 'HELLO' disemua file: **$grep -r HELLO**
- Mencari kata 'HALLO' di file baca1: **$grep HALLO baca1**
<img width="396" height="86" alt="8" src="https://github.com/user-attachments/assets/51b79c05-3bb7-41bb-a14c-0ae0906fc85a" />

- Membuat file dengan nama 'file1' dengan isi 'hallo hallo fauzi: **$cat > file1**
- Menggabungkan isi dari 2 file 'file1 dan file2' dan dipindahkan isinya ke dalam 'file3' tanpa menghapus isi dari file1 dan file2: **$cat file1 file2 > file3**
<img width="330" height="212" alt="22" src="https://github.com/user-attachments/assets/1f0c692a-74bd-4dbc-96f5-e493390b1697" />
<img width="220" height="66" alt="23" src="https://github.com/user-attachments/assets/2abc2541-4f6c-4b5d-afad-639133a7ef91" />

- Mengganti kata 'hallo' menjadi kata 'pagi' di file 'file1': **$sed -i 's/hallo/pagi/g' file1**
<img width="414" height="71" alt="24" src="https://github.com/user-attachments/assets/3ba473c1-1fd0-417b-b84a-770f53ff4de5" />

- Menampilkan jumlah baris yang mengandung kata'pagi': **$grep -c pagi file1**
- Menampilkan kata 'Hello' disemua file: **$grep hello '*'**
- menghitung jumlah baris yang mengandung kata 'hai' pada setiap file: **$grep -c hai '*'**
<img width="290" height="357" alt="25" src="https://github.com/user-attachments/assets/5074c02c-d4c0-4e0f-a977-67e97dc895ae" />

- Mengurutkan angka di file dari yang terkecil ke yang terbesar: ***$sort angka**
- Mengurutkan angka di file dari yang terbesar ke yang terkecil: ***$sort -r angka**
<img width="294" height="368" alt="26" src="https://github.com/user-attachments/assets/b374865f-1380-4bfe-a096-3aceeb1ca9f5" />

- Menampilkan file secara detail termasuk hidden file (diawali .): **$ls -la**
<img width="546" height="547" alt="9" src="https://github.com/user-attachments/assets/31e01d89-a115-40bb-818e-fed6863ede43" />

- Menghapus Folder latihan2: **$rmdir latihan2**
- Menghapus file: **$rm 'namafile'**
<img width="279" height="124" alt="10" src="https://github.com/user-attachments/assets/db30126c-31ed-43d5-8e38-ec07a1258a67" />

- Menampilkan semua file dan folder yang ada di bawah directory tersebut: **$find**
- Mencari file yang lebih spesifik: **$find -type f -name baca1**
<img width="349" height="477" alt="11" src="https://github.com/user-attachments/assets/85e58429-2779-4c7d-b7f9-0fa73a2fc5b3" />

- Menampilkan IP address dan interface jaringan: **$ip a**
- Ping google: **$ping 8.8.8.8**
<img width="624" height="347" alt="12" src="https://github.com/user-attachments/assets/3df39410-bc16-4277-8721-1b8e662cc163" />

- Menampilkan routing table: **$ip route**
<img width="569" height="73" alt="13" src="https://github.com/user-attachments/assets/1967cc32-c885-4ef2-b6f9-656e7e7eb99c" />

- Melihat socket dan port aktif: **$ss -tuln**
<img width="624" height="76" alt="14" src="https://github.com/user-attachments/assets/15172e09-bab1-412d-8fa8-34104e14796f" />

- Mengambil response web via HTTP: **$curl http://example.com**
<img width="624" height="103" alt="15" src="https://github.com/user-attachments/assets/5eefded1-d2ec-498b-b3ca-b1ccc8f613f7" />

- Melihat HTTP header website: **$curl -I http://example.com**
<img width="408" height="230" alt="16" src="https://github.com/user-attachments/assets/36459460-fc02-4c26-9490-3e9829ea6938" />

- Install ssh server: **$sudo apt install opensss-server**
<img width="624" height="210" alt="17" src="https://github.com/user-attachments/assets/7bf228e3-d561-458c-b78c-d1307761f794" />

- Menampilkan direktori home user: **$echo $HOME**
- - Menampilkan user aktif: **$echo $USER**
<img width="266" height="102" alt="18" src="https://github.com/user-attachments/assets/7f794042-890e-467f-a453-4cf1796a5902" />

- Melihat semua command yang sudah diketikkan: **$history**
<img width="215" height="46" alt="19" src="https://github.com/user-attachments/assets/a36ec4d8-a993-4fdb-ae0d-08cbe0207fff" />

- Mengakses sebagai server/admin: **$sudo su**
- Jika ingin kembali ke user: **ctrl+d**
<img width="273" height="125" alt="20" src="https://github.com/user-attachments/assets/7d1b64a9-4624-4d6e-861d-d5b2ea81f3b3" />

- Menampilkan lama sistem berjalan: **$uptime**
- Melihat penggunaan RAM: **$free -h**
- Melihat kapasitas disk: **$df -h**
<img width="624" height="219" alt="21" src="https://github.com/user-attachments/assets/ad83049d-c164-4c61-b0c3-2da2413ee473" />
