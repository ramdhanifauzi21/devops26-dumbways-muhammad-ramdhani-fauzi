#Day 1 - Introduction to DevOps
#Task1

#1. Pengertian DevOps
DevOps Engineer atau Development Opration Engineer Adalah pendekatan kerja yang menghubungkan tim development dan tim operation yang memiliki tugas untuk mempercepat proses pengembangan aplikasi, meningkatkan kualitas sistem, serta mengotomatikan proses building, testing, deployment agar lebih efesien dan stabil.

#2. Install Ubuntu Server
1. Download ISO Ubuntu Server 22.04 LTS dari website resmi Ubuntu
2. Buat VM baru di VirtualBox
3. Setting:
   - RAM: 2 GB
   - CPU: 1 Core
   - Storage: 10 GB
4. Start VM dan jalankan instalasi Ubuntu Server
5. Klik enter ‘Try or Install Ubuntu Server’.

![Screenshot](https://github.com/user-attachments/assets/8ba82e74-199b-4d03-8e3b-ede0a94d8c3f)

6. Pilih Bahasa ‘English’ agar nantinya dapat mempermudah untuk menulis command.

![Screenshot](https://github.com/user-attachments/assets/c68e09ba-db51-4b68-bcdd-5f8a9cd06f2b)

7. Jika ingin menginstall versi terbarunya bisa ENTER dibagian ‘update to the new installer’. Jika tidak maka bisa ENTER ‘continue without updating’.
   Karna saya tidak akan menginstall versi terbarunya jadi saya pilih bagian 'Update to the new installer'.

<img width="397" height="300" alt="image" src="https://github.com/user-attachments/assets/8c0db3b8-a4a0-4dec-bd6d-d177de1d15fa" />


8. Saya menggunakan Layout dan varian Keyboard English(US) lalu Klik Enter 'Done'.
<img width="401" height="300" alt="image" src="https://github.com/user-attachments/assets/e2c02c99-8236-4765-a641-f5d8e6043c7e" />

9. Disini saya haya Pilih ‘Ubutu Server’ lalu klik Done.
<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/cfb23f10-87de-4eab-ad7b-18364db3f8ec" />

10. -	Berikut ini konfigurasi Network agar ubuntu dapat mengakses internet.
    -	Enter dibagian ‘enp03’ lalu enter dibagian ‘Edit IpV4’, pilih manual.
    -	Isi bagian Subnet, Address, Gateway, dan Name Servers sesuai dengan koneksi di PC/Laptop Sendiri.
    -	Cara agar tau IP Network di PC/Laptop dengan menggunakan CMD lalu ketik ‘ipconfig’ dan akan muncul,
      Jika menggunakan LAN maka pilih ‘Ethernet Adaptor’, jika menggunakan Wifi maka akan muncul ‘wlan’ dan gunakan itu.
    -	Setelah selesai klik Enter 'Done'.

<img width="401" height="300" alt="image" src="https://github.com/user-attachments/assets/a7a7f1d2-b102-4210-8aa1-cebc46f5d774" />

<img width="398" height="300" alt="image" src="https://github.com/user-attachments/assets/eae9efb5-5b1e-4379-9312-4091f47fa914" />

<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/70cfdc79-ca8c-4f44-aa35-98cb5c0c61a6" />

<img width="370" height="285" alt="image" src="https://github.com/user-attachments/assets/0ff133c0-757e-40ef-b8af-a18a62022660" />

<img width="398" height="300" alt="image" src="https://github.com/user-attachments/assets/8f6ffd92-fb8a-461f-beca-909217f03349" />

11. Untuk Proxy bisa dilewat, Klik ENTER 'Done'

<img width="394" height="300" alt="image" src="https://github.com/user-attachments/assets/3788389e-d748-4b23-ab78-3e0dbb3ee1f5" />


12. Dibagian sini hanya untuk melihat tes dari ubuntunya dan bisa dilewat Klik ENTER 'Done', Lalu ENTER 'Continue'

<img width="396" height="300" alt="image" src="https://github.com/user-attachments/assets/42270aa3-113a-405a-93f1-fe87a1b6be3c" />

<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/c9b2dc7d-c1ce-4237-a38e-c0059e1ac092" />


13. Disini saya Pilih ‘Custom storage layout’ karna ingin mengcustom bagian storage yang saya miliki, Lalu klik Done.  

<img width="404" height="300" alt="image" src="https://github.com/user-attachments/assets/24494094-56a0-461b-bd1c-bcb57f113d74" />


14. Disini optional, saya akan membuat partisi dengan klik ‘free space’ ‘add GPT Partition’. Saya membuat 7Gb dan Format ext4 lalu Klik ‘Create’.

<img width="399" height="300" alt="image" src="https://github.com/user-attachments/assets/6b75442b-b55e-480d-b877-dcb16ec59f48" />

<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/2776dc8b-9ceb-430e-a73c-f79b91fcd215" />

15. Membuat lagi parisi dengan cara yang sama. Diisi 2.8Gb dan Formatnya ‘swap’ yang berfungsi sebagai RAM Cadangan.

<img width="401" height="300" alt="image" src="https://github.com/user-attachments/assets/fdbe0a3d-46a6-4538-a819-5a139f0bd9f7" />

<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/378ab9d3-2eb5-4ba9-bb89-5576e7d3d43f" />


16. Setelah selesai Klik ENTER 'Done' dan 'Continue'.

<img width="401" height="300" alt="image" src="https://github.com/user-attachments/assets/b46f0fb1-15be-450f-a0ac-ec257d505273" />

<img width="402" height="300" alt="image" src="https://github.com/user-attachments/assets/7e991949-94af-4269-be9f-20f48bb7e772" />

17. Di bagian ini sesuaikan untuk Nama Server, User, Password. Jika sudah lalu klik ENTER 'done' (jangan sampai lupa user dan password).

<img width="399" height="300" alt="image" src="https://github.com/user-attachments/assets/269459fe-5903-4848-aae4-20efa73d5a30" />

18. Dibagian ini jika pengen masuk ke Ubuntu Pro bisa Klik Enter dibagian Ubuntu Pro. Disini saya pilih 'skip' lalu ENTER 'Done'.

<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/f9bacce6-882c-4c25-9d8b-c6868c4431cc" />

19. Jika ingin menginstall SSH Server maka bisa di Enter dibagian SSh Server. Jika tidak langsung Done.

<img width="399" height="300" alt="image" src="https://github.com/user-attachments/assets/2e350bab-1afd-4c6d-a3bf-aea2cc361e0d" />

20.  - Disini saya hanya ingin menginstall Ubuntu polosan jadi saya tidak memilih apapun
     - Jika ada yang ingin di install bisa dipilih dan klik enter. Jika tidak maka tinggal klik Done.
     - Lalu akan menjalankan Install, tunggu hingga selesai.

<img width="398" height="300" alt="image" src="https://github.com/user-attachments/assets/50cae7c4-2a84-4130-8b24-8c39b6fd4c7e" />

<img width="401" height="300" alt="image" src="https://github.com/user-attachments/assets/3371d7d1-8622-4d8e-8059-bde70d5aa308" />


21. Berikut ini tampilan jika proses intall Ubuntu Selesai. Lalu Pilih 'Reboot Now'.

<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/d2608064-f219-44fd-b33d-ba26c76a9165" />

22. Jika sudah Reboot tampilan akan jadi seperti ini. Masukkan user dan pass yang sudah dibuat sebelumnya. 

<img width="403" height="300" alt="image" src="https://github.com/user-attachments/assets/3b0154c8-6990-4f4e-a9ec-209c3632793e" />

<img width="401" height="300" alt="image" src="https://github.com/user-attachments/assets/0c628c91-18c2-44fe-8a1a-70074bd645a0" />




#3. Menggunakan IP Address xxx.xxx.xxx.208 untuk server VM
Berikut ini konfigurasi Network agar ubuntu dapat mengakses internet.
- Enter dibagian ‘enp03’ lalu enter dibagian ‘Edit IpV4’, pilih manual.
- Isi bagian Subnet, Address, Gateway, dan Name Servers sesuai dengan koneksi di PC/Laptop Sendiri.
- Cara agar tau IP Network di PC/Laptop dengan menggunakan CMD lalu ketik ‘ipconfig’ dan akan muncul,
  Jika menggunakan LAN maka pilih ‘Ethernet Adaptor’, jika menggunakan Wifi maka akan muncul ‘wlan’ dan gunakan itu.
- Setelah selesai klik Enter 'Done'.

<img width="401" height="300" alt="image" src="https://github.com/user-attachments/assets/a7a7f1d2-b102-4210-8aa1-cebc46f5d774" />

<img width="398" height="300" alt="image" src="https://github.com/user-attachments/assets/eae9efb5-5b1e-4379-9312-4091f47fa914" />

<img width="400" height="300" alt="image" src="https://github.com/user-attachments/assets/70cfdc79-ca8c-4f44-aa35-98cb5c0c61a6" />

<img width="370" height="285" alt="image" src="https://github.com/user-attachments/assets/0ff133c0-757e-40ef-b8af-a18a62022660" />

<img width="398" height="300" alt="image" src="https://github.com/user-attachments/assets/8f6ffd92-fb8a-461f-beca-909217f03349" />


<img width="840" height="296" alt="image" src="https://github.com/user-attachments/assets/02497685-c0c7-47b3-b6a8-1d22aba8818a" />

#4. Ping Google.com/8.8.8.8 untuk memastikan VM terkoneksi ke internet
<img width="352" height="375" alt="image" src="https://github.com/user-attachments/assets/5b6c7476-b912-4f56-87fc-aed63208ab89" />




