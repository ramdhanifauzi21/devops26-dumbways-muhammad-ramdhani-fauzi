# Task 5

Semua Aplikasi bisa akses dengan **UFW ENABLE**

<img width="504" height="403" alt="ufw" src="https://github.com/user-attachments/assets/f46b7400-c498-45c2-9340-a5dc9414fb72" />

## 1. NodeJs - Deploy App wayshub-frontend, Berjalan di Port 3000, dan Menggunakan NodeJS 10/12
- Download dan Install NMV: **$curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash**
<img width="624" height="307" alt="install" src="https://github.com/user-attachments/assets/723c8a66-08c8-48d3-be16-33a060d10d14" />

- Restart Shell: **\. "$HOME/.nvm/nvm.sh"**
<img width="403" height="81" alt="restart" src="https://github.com/user-attachments/assets/b8d67808-f0c0-44de-a1c7-2563583c950d" />

- Install nvm versi 12: **nvm install 12**
- Gunakan versi 12: **$npm use 12**
- Cek versi: **node -v**
<img width="624" height="136" alt="instalnvm12" src="https://github.com/user-attachments/assets/a6fba896-d5b6-4bf5-b100-4d058fb27247" />

- Clone github wayshub-frontend: **$git clone https://github.com/dumbwaysdev/wayshub-frontend.git**
- Cek folder dan filenya: **$ls**
- Masuk ke folder wayshub-frontend: **$cd wayshub-frontend**
<img width="624" height="170" alt="clone" src="https://github.com/user-attachments/assets/ee7ad1c4-97d4-477f-9aa1-dfb17656e25b" />

- Install terlebih dahulu modules/package npm: **$npm install** Karna jika tidak akan error
<img width="624" height="538" alt="npminstall" src="https://github.com/user-attachments/assets/9466a7d2-cfb1-4de3-b0df-f1c3b646c60a" />

- Jalankan perintah: **$npm start** Untuk Menjalankan programnya
<img width="495" height="116" alt="start" src="https://github.com/user-attachments/assets/671b5016-0a0a-42ba-8bff-c6d064d8533d" />
<img width="624" height="487" alt="start2" src="https://github.com/user-attachments/assets/415eb98b-e011-42bf-96db-d833e62f6d9b" />

- Buka browser dan ketikan: **192.168.1.208:300** artinya IP Server:Port || Tampilan pun muncul dan tandanya Berhasil
<img width="624" height="294" alt="hasil" src="https://github.com/user-attachments/assets/f076a075-17aa-4dfc-9887-46edb3622389" />

## 2. Python - Deploy App Menampilkan Nama, Berjalan di Port 5000, Dapat dibuka Melalui Web 
- Install tools python: **$sudo apt install python3-pip**
<img width="624" height="336" alt="installtools" src="https://github.com/user-attachments/assets/e106e648-4732-471a-a3b3-1ee640e7214a" />

- Cek versi pip: **$pip -V**
<img width="603" height="61" alt="cekpip" src="https://github.com/user-attachments/assets/2c8244b6-8461-41d8-abc5-e5760985f562" />

- Buat folder baru agar tidak berantakan: **mkdir python**
- Masuk ke foldernya: **cd python**
<img width="307" height="58" alt="buatfolder" src="https://github.com/user-attachments/assets/4afa5cf0-3fcb-46eb-8e67-960380bf85af" />

- Install framework Flask ke Python 3 agar Python bisa membuat web app: **$pip3 install flask**
<img width="624" height="280" alt="installpipflash" src="https://github.com/user-attachments/assets/775c8ef9-5a97-4244-9210-a6bdaba3889f" />

- Buat file: **$nano index.py** , berikan isi nya seperti dibwah ini agar bisa tampil di web, lalu save.
<img width="624" height="187" alt="fileindex" src="https://github.com/user-attachments/assets/e79370bc-3086-4a91-9717-60362b7d19fe" />

- Jalankan file index tadi dengan perintah: **$python3 index.py**
<img width="624" height="93" alt="Jalankan" src="https://github.com/user-attachments/assets/068873ef-8dd7-43dd-bd67-f0c1a6190ed4" />

- Cek di web, Buka browser dan ketikkan: **$192.168.1.208:5000**
<img width="624" height="382" alt="Hasilweb" src="https://github.com/user-attachments/assets/b89afa32-55c7-4dfd-be82-94cc5f4ff443" />

## 3. Golang - Deploy app Menampilkan text 'Golang Geming!'
- Server Mengunduh file golang dari internet: **$wget https://go.dev/dl/go1.25.6.linux-amd64.tar.gz**
- Jika sudah akan ada file dengan nama **gol.25.6.linux-amd64.tarz.gz**
<img width="624" height="250" alt="wget" src="https://github.com/user-attachments/assets/20764d6b-812f-40af-93c1-0d2cdeec7959" />

- Masuk sebagai root: **$sudo su**
- menghapus Go lama lalu mengekstrak Go versi baru: **$ rm -rf /usr/local/go && tar -C /usr/local -xzf go1.25.6.linux-amd64.tar.gz**
<img width="624" height="55" alt="hapuslama" src="https://github.com/user-attachments/assets/3cc2943b-5817-46e9-b777-eeaf253b1b55" />

- menambahkan binary Golang ke PATH agar perintah go bisa dijalankan: **$export PATH=$PATH:/usr/local/go/bin**
<img width="483" height="44" alt="path" src="https://github.com/user-attachments/assets/bddd0829-5521-451e-8c82-85529609b350" />

- Cek Versi Golang: **$go version**
<img width="322" height="58" alt="cekversi" src="https://github.com/user-attachments/assets/6377fd32-4676-4675-8047-3a90c802ba1a" />

- Buat folder baru: **$mkdir golang**
- Masuk ke folder : **cd golang**
<img width="279" height="62" alt="buatfolder" src="https://github.com/user-attachments/assets/9f9f2fbe-c4b1-4272-a46c-4fb52b29f3ad" />

- Buat file dan isikan: **$nano index.go**
<img width="624" height="175" alt="buatfile" src="https://github.com/user-attachments/assets/0ab22eb2-bddd-461d-a569-62620694b718" />

- Cek file: **$ls**
<img width="247" height="58" alt="cekfile" src="https://github.com/user-attachments/assets/e57bd560-d86e-4a8b-ac8a-21b480416965" />

- Jalankan file golang dengan perintah: **$go run index.go**
<img width="416" height="59" alt="jalankangolang" src="https://github.com/user-attachments/assets/455c0528-3efa-4df7-a5d5-d755cbb1d26a" />
