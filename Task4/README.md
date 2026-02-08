# Task 4

## 1. Penjelasan Git

  Git adalah sistem pengelolaan versi (Version Control System) yang digunakan untuk mencatat dan mengatur setiap perubahan pada file atau kode dalam sebuah project. Git membantu pengembang melacak riwayat perubahan, bekerja secara kolaboratif, serta mengembalikan file ke versi sebelumnya jika terjadi kesalahan.

## 2. Menghubungkan Server ke Github. Membuat Sebuah Repository, dan Menambahkan 3 File

1. Pastikan terlebih dahulu di server sudah ada git
2. Masukkan perintah:
   - **$git config --global user.name ramdhanifauzi21** : Masukkan user Github
   - **$git config --global user.email ramdhani24fauzi.com** : Masukkan email yang ada di Github
   - **$git config --list** : Melihat list user dan email github
  
<img width="624" height="115" alt="config" src="https://github.com/user-attachments/assets/666ac64d-e01a-4a10-bf3a-fa7959a780c4" />

3. - Untuk menghubungkan server ke Git, pastikan server sudah mengenerate privat key & publik key. jika belum bisa mengetikkan perintah: **$ssh-keygen**
   - Masuk ke dalam folder .ssh: **$cd .ssh**
   - Bisa di cek terlebih dahulu file di dalam foldernya: **$ls**
   - Buka file publik key nya 'id_rsa.pub': **$cat id_rsa.pub** dan Copy isinya
<img width="624" height="108" alt="key" src="https://github.com/user-attachments/assets/adcd07ac-df1a-4cc4-9c2c-68e95dac6a3a" />

4. Buka Github -> Settings -> Masuk ke 'SSH and GPG Keys' -> Klik 'New SSH Key' -> Masukkan title nya 'devops26-dumbways-fauzi' -> Pastekan pubkey yang sudah di copy di server tadi di bagian 'key' -> Add SSH Key -> Verifikasi -> Selesai
<img width="624" height="271" alt="key github" src="https://github.com/user-attachments/assets/ed9dd6f8-f7eb-4379-81ca-62db809b5e3a" />

5. Cek server apakah pubkey nya sudah terhubung dengan github **$ssh git@github.com -T**
<img width="624" height="110" alt="cek git" src="https://github.com/user-attachments/assets/8a1d3c54-f493-4c68-94ac-3788a72d2364" />

Jika sudah ada komen 'Hi ramdhanifauzi21! You've successfully authenticated, but GitHub does not provide shell access.' Maka sudah berhasil terhubung

6. Membuat Direktory Baru dengan nama 'devops26-dumbways-fauzi': **$mkdir dumbways** Lalu masuk ke foldernya: **$cd dumbways**
<img width="774" height="89" alt="direktory" src="https://github.com/user-attachments/assets/bf57846e-b74b-4293-91ba-fcd35718b64c" />

7. Menjadikan sebuah repository: **$git init devops26-dumbways-fauzi**
<img width="624" height="196" alt="menjadi repo" src="https://github.com/user-attachments/assets/17cc1ac9-f89d-45f8-a9d2-359320c67fff" />

Didalam baris pertama, terdapat hit yaitu 'master' sebagai branch

8. - Masuk ke dalam direktory 'devops26-dumbways-fauzi': **$cd devops26-dumbways-fauzi**
   - Buat 3 file yang berisikan teks
<img width="542" height="213" alt="file" src="https://github.com/user-attachments/assets/96f4d3d3-7221-4c76-a58a-bb0a93ad8418" />

9. Inisialisaikan direktory sebagai git: **$git init .**
<img width="624" height="58" alt="inisialisasi init" src="https://github.com/user-attachments/assets/3288fac2-9241-4eba-80bf-74f1069b8371" />

Artinya sudah berhasil membuat 'devops26-dumbways-fauzi' menjadi sebuah repository

10. Melihat status git: **$git status**
<img width="624" height="230" alt="status sebelum" src="https://github.com/user-attachments/assets/2a75233b-048d-4200-8c38-c14deb45248f" />

Fase 'untracked' -> File-file yang masih baru dan belum masuk ke repository

11. Mempersiapkan file untuk masuk ke repository: **$git add file1**, Jika ingin sekaligus: **git add .**
<img width="559" height="248" alt="stage" src="https://github.com/user-attachments/assets/6d218c4a-84b6-4344-be17-e99c610860bc" />


Ini bisa disebut sebagai fase **staging** artinya Perubahannya sudah ditandai/ revisinya sudah ditandai

12. Commit file agar menjadi bagian repository: **$git commit -m "Commit Pertama"** Jangan lupa untuk memberi komen seperti 'commit Pertama' jika tidak maka perintah akan salah
<img width="624" height="170" alt="commit" src="https://github.com/user-attachments/assets/8f7d2bb0-fc98-4a5c-9484-183acd2d72fd" />

di status bisa dilihat bahwa file-file yang sebelumnya berada di fase staging sudah tidak ada, karna sudah di commit. Bisa disebut juga sebagai fase **Commited** (file yang sudah siap menjadi bagian repository). 

13. Menghubungkan repositorry server ke github
    - Buka Github -> Buat repository baru dengan nama yang sama seperti di server -> Create Repository
<img width="624" height="609" alt="repo git" src="https://github.com/user-attachments/assets/2d0fcab3-1512-437a-8284-35afd5133d98" />

14. Tampilan akan seperti ini
<img width="624" height="298" alt="tam-github" src="https://github.com/user-attachments/assets/a8ab386d-fcbe-405f-a958-5cc51d96fc3f" />

15. Masuk ke server dan masukkan kode yang ada di'..or push an existing repository from the command line' ke server
    - **$it remote add origin https://github.com/ramdhanifauzi21/devops26-dumbways-fauzi.git**
      <img width="624" height="22" alt="remote" src="https://github.com/user-attachments/assets/dc6c10d6-5709-45c6-8044-fbe890186316" />
    
    - **$git branch -M master** Jangan sampai salah di bagian ini, branch di server saya adalah 'master'
      <img width="624" height="80" alt="branch" src="https://github.com/user-attachments/assets/72c8e61b-fda7-4c11-8bd9-2019712de7ed" />
      
    - **$git push -u origin master**

      <img width="624" height="82" alt="push" src="https://github.com/user-attachments/assets/72a0facf-9942-41d6-a4ff-b05942424d54" />

      Disini ternyata saya error
16. Cek terlebih dahulu remote nya: **$git remote -v**
<img width="624" height="66" alt="http" src="https://github.com/user-attachments/assets/f22bf214-b807-43ea-af9f-b99254f9c336" />

disini repository saya masih pakai https, akan saya coba ubah

17. Ubah repository HTTPS -> SSH: **$git remote set-url origin git@github.com:ramdhanifauzi21/devops26-dumbways-fauzi.git
**
<img width="624" height="65" alt="ubahhttp" src="https://github.com/user-attachments/assets/0547326a-ec70-4f8a-b428-673ba7f7459f" />

Dan setelah di cek kembali, yang awalnya ada Https sekarang sudah tidak ada

18. Push kembali: **$git push -u origin master** 
<img width="624" height="170" alt="pushkembali" src="https://github.com/user-attachments/assets/36824c7d-49bd-4cf0-8f8e-81aac76255de" />

Jika Seperti ini tandanya file-file yang ada diserver di direkrory ini sudah berada di github

19. Buka Github -> repository devops26-dumbways-fauzi -> Jika filenya sudah ada maka tandanya **Berhasil**
<img width="624" height="249" alt="berhasil" src="https://github.com/user-attachments/assets/d7685053-6060-40c1-a57d-1f7e284f5fb3" />

 
## 3. Manage Repository Menggunakan terminal
Manage repository menggunakan terminal menggunakan perintah
- **$git init**: Menginisialisasi repository Git di folder lokal
- **$git status**: Mengecek status file (tracked / untracked)
- **$git add .**: Menambahkan semua file ke staging area
- **$git branch**: Melihat branch
- **$git branch namabranch**: Menambahkan branch(cabang) baru
- **$git checkout**: Mengganti branch
- **$git commit**: Menyimpan perubahan ke Git
- **$git remote add origin**: Menghubungkan repo lokal ke GitHub
- **$git push**: Mengirim perubahan ke repository GitHub

Case: saya ingin mengubah isi dari file1 dan mengirimkannya ke repository github
- Disini saya menambahkan kata 'Selamat Pagi Fauzi' di file1
<img width="624" height="80" alt="editfile" src="https://github.com/user-attachments/assets/83c7ada2-1389-4a8f-a062-70c7a0ff3819" />

- Terlihat di status ada modified di file1
<img width="624" height="199" alt="statusperubahan" src="https://github.com/user-attachments/assets/2c8d4676-3fee-4152-82f3-d2e5924598e3" />

Misalkan tidak jadi untuk melakukan perubahan maka bisa menggunakan perintah: **$git restore namafile**

- Masuk ke fase staging
<img width="560" height="195" alt="image" src="https://github.com/user-attachments/assets/fbba3fa4-9d57-4873-a942-8d741dce9107" />

- Commit file
<img width="624" height="54" alt="commit" src="https://github.com/user-attachments/assets/d94b3df8-41d5-49a7-b1a5-152b360725d9" />

- Push ke Github
<img width="624" height="178" alt="push" src="https://github.com/user-attachments/assets/c35bdaa6-576a-4874-b16f-269c336a3cca" />

## 4. Mencari Perubahan Text Pada Suatu File di Github
-  Masuk ke Github
<img width="624" height="281" alt="tam" src="https://github.com/user-attachments/assets/8e86c85a-8a93-4949-ad47-359b18d40340" />

terlihat di pinggir file1 commit nya menjadi 'Update file1'

-  Bisa juga melihat Commit historynya
<img width="624" height="341" alt="history" src="https://github.com/user-attachments/assets/bf733aa6-9b35-4c1d-99dd-26d68ee8b801" />

-  Isi dari file1 yang sudah berubah, di tandai dengan wana hijau merupakan teks baru
<img width="624" height="458" alt="isi" src="https://github.com/user-attachments/assets/8d544b84-0fc8-4445-bd40-63810336e5ea" />

