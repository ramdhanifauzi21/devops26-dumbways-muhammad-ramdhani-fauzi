# Task 4

## 1. Penjelasan Git

  Git adalah sistem pengelolaan versi (Version Control System) yang digunakan untuk mencatat dan mengatur setiap perubahan pada file atau kode dalam sebuah project. Git membantu pengembang melacak riwayat perubahan, bekerja secara kolaboratif, serta mengembalikan file ke versi sebelumnya jika terjadi kesalahan.

## 2. Menghubungkan Server ke Github. Membuat Sebuah Repository, dan Menambahkan 3 File

1. Pastikan terlebih dahulu di server sudah ada git
2. Masukkan perintah:
   - **#git config --global user.name ramdhanifauzi21** : Masukkan user Github
   - **#git config --global user.email ramdhani24fauzi.com** : Masukkan email yang ada di Github
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


Ini bisa disebut sebagai fase **stage** artinya Perubahannya sudah ditandai/ revisinya sudah ditandai

12. Commit file agar menjadi bagian repository: **$git commit -m "Commit Pertama"**
<img width="624" height="170" alt="commit" src="https://github.com/user-attachments/assets/8f7d2bb0-fc98-4a5c-9484-183acd2d72fd" />

di status bisa dilihat bahwa file-file yang sebelumnya berada di fase stage sudah tidak ada, karna sudah di commit. Bisa disebut juga sebagai fase **Commited** (file yang sudah siap menjadi bagian repository). 

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

18. Buka Github -> repository devops26-dumbways-fauzi -> Jika filenya sudah ada maka tandanya **Berhasil**
 
## 3. Manage Repository Menggunakan terminal

## 4. Mencari Perubahan Text Pada Suatu File di Github
