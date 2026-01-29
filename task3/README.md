##1. Akses Server Melalui Windows Terminal
-
1. Pastikan server sudah install openssh server. Jika belum install terlebih dahulu dengan mengetikkan command: **$sudo apt install openssh-server**
    <img width="420" height="96" alt="1" src="https://github.com/user-attachments/assets/509468a4-3141-423c-a18c-7cf49d8f7aac" />


2. Pastikan ssh aktif dengan status 'running' dengan command: **$sudo systemctl status ssh**
    <img width="418" height="192" alt="2" src="https://github.com/user-attachments/assets/a05f1ac9-2006-46c2-ad97-271afc0548b4" />


3. Akses ssh melalui windows terminal mengetikkan command: **ssh uzi@192.168.1.208**, dan memasukkan password server

    dengan keterangan uzi = nama user yang ada di server dan 192.168.1.208= IP Servernya. Untuk melihat IP di server bisa mengetikkan command: **$ip a**
 <img width="624" height="389" alt="3" src="https://github.com/user-attachments/assets/4b93bba1-48d9-420c-b18d-78b9c1f59dd0" />

 Windows Terminal pun sudah memiliki akses server


##2. Ssh hanya dapat di akses menggunakan publickey.  
-
1. membuat(Generate) pasangan kunci SSH (Privat key dan Public key) di Client(W Terminal): **ssh-keygen**
<img width="624" height="309" alt="key1" src="https://github.com/user-attachments/assets/0955d946-d7c9-4464-835c-e40d203aec2e" />

   Disini saya menyimpan di folder **C:\Users|\USER/.ssh/kunci** dengan nama file kunci, yang nantinya akan ada 2 file di folder .ssh yaitu **kunci** dan **kunci.pub**
<img width="624" height="260" alt="key2" src="https://github.com/user-attachments/assets/1c03b4b8-b243-4284-b39e-f44ca5f6355d" />


2. - Buka terlebih dahulu file 'kunci.pub' menggunakan noted, Copy semua isinya
<img width="624" height="99" alt="key3" src="https://github.com/user-attachments/assets/ce9dd477-44f8-4333-89eb-abcaa7849a57" />

   - Masuk ke dalam Server, masuk ke folder '.ssh': **$cd .ssh**
<img width="238" height="97" alt="key11" src="https://github.com/user-attachments/assets/8e95c8d7-5741-4599-8ca7-fbde290e0a97" />
    
   -  Setelah berada di folder .ssh, masuk ke file authorized_keys: **$nano authorized_keys**
   -  Paste kan isi file tadi di dalam file authorized_keys dengan menekan 'ctrl+shift+v', jika sudah tekan 'ctrl+x' lalu 'y' lalu ENTER.
<img width="624" height="357" alt="key12" src="https://github.com/user-attachments/assets/ab7b49de-9b11-41f3-9631-ee5460207cb1" />


3. Masukkan perintah:**$sudo nano /etc/ssh/sshd_config**
<img width="441" height="40" alt="key7" src="https://github.com/user-attachments/assets/23b5d768-9043-46b0-9d34-6c9c788c6993" />

Maka tampilan akan seperti pada gambar dibawah ini. 

Pastikan:
- PubkeyAuthentication yes
- PasswordAuthentication no
- PermitRootLogin no

Jika susah untuk mencarinya tinggal tekan 'ctrl+w' lalu tulis kata yang akan dicari contohnya 'pubkey' lalu enter, maka akan otomatis mengarah ke kata tersebut. Jika sudah di edit tekan 'ctrl+x' lalu 'y' lalu ENTER.
<img width="624" height="347" alt="key8" src="https://github.com/user-attachments/assets/d228e15f-74ca-4f92-9484-c0d0be48a408" />
<img width="624" height="340" alt="key9" src="https://github.com/user-attachments/assets/591f8972-c926-47cc-bb9d-a26db7c4e966" />

Artinya:
- PubkeyAuthentication yes = login pakai key
- PasswordAuthentication no = login password dimatikan
- PermitRootLogin no = root tidak boleh login


4. - Mengamankan folder SSH agar hanya owner yang bisa akses :**$chmod 700 ~/.ssh**
   - Mengamankan daftar public key agar tidak bisa dimanipulasi user lain: **$chmod 600 ~/.ssh/authorized_keys** 
<img width="624" height="147" alt="key10" src="https://github.com/user-attachments/assets/84d6ab8c-8e38-43e9-9d5d-f9ab7483e462" />
Artinya Hanya owner yang dapat masuk folder, lihat isi, dan ubah isi.


5.  Restart konfigurasi ssh tadi: **$sudo systemctl restart ssh**
<img width="418" height="55" alt="key13" src="https://github.com/user-attachments/assets/901d8023-659b-49f6-b1e5-7ca5c912dcec" />


6. Mencoba masuk dan tidak harus memasukkan password lewat Client(Windows Terminal): **ssh -i ~/.ssh/kunci uzi@192.168.1.208** 
<img width="624" height="611" alt="key14" src="https://github.com/user-attachments/assets/c9678366-c147-42ca-8e0f-95eeddfc38ee" />



##3. Text Manipulation
-
1. Membuat file dengan nama 'file1' dan  'file2' berserta isinya langsung menggunakan command : **$cat > file1**
2. Menggabungkan isi file 'file1' dan 'file2' dan dimasukkan ke 'file3' : **$cat file1 file2 > file3**
3. Menampilkan isi file: **$cat file3**
<img width="330" height="212" alt="22" src="https://github.com/user-attachments/assets/b79883fc-019b-4d95-8244-61058ac98837" />
<img width="220" height="66" alt="23" src="https://github.com/user-attachments/assets/cd6b6628-17e9-4a8b-a1fd-2743d11cf258" />


4. Mengganti kata 'hallo' menjadi 'pagi' didalam 'file1': **$sed -i 's/hallo/pagi/g' file1**
<img width="414" height="71" alt="24" src="https://github.com/user-attachments/assets/bd689c37-8928-450a-9f70-bcb315a9314b" />


5. Mencari kata 'pagi' dalam file: **$grep pagi file1**
<img width="290" height="31" alt="25" src="https://github.com/user-attachments/assets/c892bc23-11d3-47aa-b63d-a36392887ac1" />


6. Mencari kata 'hai' disemua file: **$grep hai'*'**
<img width="317" height="48" alt="4-2" src="https://github.com/user-attachments/assets/c3fddcad-17db-4ae7-a657-190cce0dccbe" />


7. Menghitung berapa baris yang mengandung kata "hai" pada semua file: **$grep -c hai ***
<img width="317" height="134" alt="4-3" src="https://github.com/user-attachments/assets/65c3d11d-a88d-4b00-bdb7-5254db1d7281" />


8. Membuat file file4 dan mengisi teks "hahaha" : **$echo "Hello DevOps" > file4**
<img width="336" height="70" alt="5" src="https://github.com/user-attachments/assets/04944c0b-61bc-4b0c-9dae-9857631d2281" />


##4. Menyalakan ufw dengan memberikan akses untuk port 22, 80, 443, 3000, 5000 dan 6969
-
1. Instal terlebih dahulu ufw(Uncomplicated Firewall) di ubuntu jika belum terinstal: **$sudo apt install ufw**
<img width="589" height="162" alt="ufw1" src="https://github.com/user-attachments/assets/d3d7836d-2da3-4413-90f8-9d33d7b97149" />

Kondisi awal status untuk ufw 'inactive', untuk melihat status: **$sudo ufw status**
<img width="305" height="36" alt="ufw3" src="https://github.com/user-attachments/assets/a043850f-2df3-41ed-bc9b-2cbb8668717b" />


2. Membuka akses untuk port 22, 80, 443, 3000, 5000 dan 6969:
   - **$sudo ufw allow 22**
   - **$sudo ufw allow 80**
   - **$sudo ufw allow 443**
   - **$sudo ufw allow 3000**
   - **$sudo ufw allow 5000**
   - **$sudo ufw allow 6969**
<img width="341" height="342" alt="ufw2" src="https://github.com/user-attachments/assets/9a1e91c3-2703-44a8-b171-7ee3e3cc538d" />


3. Cek untuk status ufw nya dan apakah sudah diizinkan untuk port-port diatas: **$sudo ufw status**
<img width="490" height="361" alt="ufw5" src="https://github.com/user-attachments/assets/1440a2de-4bc2-40f3-aff2-01361aec5583" />

Jika tampilan sudah seperti diatas ini, tandanya firewall aktif dan port yang tertera diizinkan oleh firewall dan bisa di akses dari semua IP.






