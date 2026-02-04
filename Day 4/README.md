**DAY-4 - Version Control System**

------------------------------------------------------------------------------------------------------------------------------------------------------


**Task : 1. Penjelasan tentang Git**
Git adalah sebuah Version Control System (VCS) terdistribusi. Sederhananya, Git adalah sistem yang mencatat setiap perubahan pada file proyekmu.
Bayangkan kamu sedang menulis kode:
- Tanpa Git: Kamu mungkin akan membuat file seperti `kodingan_final.js`, `kodingan_final_banget.js`, `kodingan_fix_bismillah.js`. Berantakan, bukan?
- Dengan Git: Kamu hanya punya satu file, tapi kamu bisa melihat, membandingkan, dan kembali ke versi mana pun di masa lalu jika ada kode yang rusak.

**Perintah Dasar Git :**
Jika kamu ingin mulai menggunakan Git di terminal (tempat kamu menjalankan PM2 tadi), inilah perintah yang paling sering digunakan:
- `git init`: Mengubah folder biasa menjadi "folder Git" (inisialisasi).
- `git add .`: Memasukkan semua perubahan ke Staging Area (siap-siap disimpan).
- `git commit -m "pesan"`: Menyimpan perubahan secara permanen dengan catatan singkat tentang apa yang kamu ubah.
- `git push`: Mengirim kodingan dari laptop kamu ke internet (GitHub).
- `git pull`: Mengambil kodingan terbaru dari internet ke laptop kamu.

------------------------------------------------------------------------------------------------------------------------------------------------------


**Task : 2. Buat sebuah repository bernama "devops26-dumbways-'nama' ", lalu tambahkan 3 file yang berisi text**
1. Check versi dari git yang terinstall di server dengan `git --version`
   <img width="620" height="59" alt="image" src="https://github.com/user-attachments/assets/d856d7ad-1a7b-4663-b667-3260f980f1e6" />

2. Hubungkan username github dengan `git config --global user.name "username"`, dan email github dengan `git config --global user.email "email"`. Lalu check apakah sudah terhubung dengan `git config --list`.
   <img width="619" height="125" alt="image" src="https://github.com/user-attachments/assets/8c95ef8b-f8cd-4b42-95a5-dd6c1535d091" />
   <img width="617" height="81" alt="image" src="https://github.com/user-attachments/assets/de2ecbd2-00fa-47b3-a571-856fc8c7a7d7" />

3. Hubungkan Public Key yang terdapat di Ubuntu Server dengan Github. Copy Public Key Server pada directory `/.ssh` dengan `cat id_rsa.pub`.
   
   <img width="617" height="116" alt="image" src="https://github.com/user-attachments/assets/2f06e061-e710-44d7-80f0-a2c1050de892" />

  
  Paste Public Key ke `Menu Setting -> SSH and GPG Keys -> New SSH Key`. Isikan Tittle dan Key lalu `klik Add SSH Key`.
  
  <img width="624" height="448" alt="image" src="https://github.com/user-attachments/assets/562f77d1-6dea-4ec9-8132-a818ea37b8f3" />

  Setelah `Add SSH Key` akan tampil menu Authentication keys seperti ini.
  <img width="624" height="299" alt="image" src="https://github.com/user-attachments/assets/53344715-3d85-4916-a1eb-f11b17872474" />

4. Untuk menguji apakah koneksi SSH antara Ubuntu Server dan GitHub sudah berhasil terkonfigurasi dengan benar dengan `ssh git@github.com -T`.
   
   <img width="628" height="72" alt="image" src="https://github.com/user-attachments/assets/3b8f0691-9ddf-4c6c-bf2d-dbed47aa2861" />


6. Membuat Folder Baru + Inisialisasi `git init devops26-dumbways-Tegar`.
   <img width="628" height="149" alt="image" src="https://github.com/user-attachments/assets/5ee26152-e46a-4dd9-9804-f28c643db4b4" />

7. Setelah dibuat folder baru dan inisialisasi, akan tampil folder baru didalam directory Server kita. Buat atau copy file yang sudah ada kedalam direcotry `devops26-dumbways-Tegar`. Lalu `git init`.
   <img width="628" height="276" alt="image" src="https://github.com/user-attachments/assets/7a5030b5-1980-4b4b-9cce-1ee9d1e70143" />

8. Untuk menyembunyikan file agar tidak tampil di git dengan cara membuat file baru bernama `.gitignore`. Lalu tuliskan didalam file tersebut file mana yang akan disembunyikan. COntoh `file4`.

   <img width="626" height="185" alt="image" src="https://github.com/user-attachments/assets/bb221908-ca39-4f2b-9d07-6d95b0012536" />

10. Setelah file4 disembunyikan di git, lakukan comit untuk mendeploy file yang sudah kita kerjakan tadi dengan `git commit -m "catatan commit"`.
    <img width="629" height="196" alt="image" src="https://github.com/user-attachments/assets/58b9bc91-2736-48f6-a45a-30bd40e9b63c" />

    <img width="626" height="162" alt="image" src="https://github.com/user-attachments/assets/817d9291-024e-4034-ba20-5aa9b5f5cb2d" />

