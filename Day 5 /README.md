NodeJS
- Deploy app wayshub-frontend
- Berjalan di port 3000
- Menggunakan NodeJS 10 & 12
```https://github.com/dumbwaysdev/wayshub-frontend```

Python
- Deploy app menampilkan text nama kalian!
- Berjalan di port 5000 & bisa dibuka melalui web

Golang
- Deploy app menampilkan text "Golang geming!"

Note : Semua app WAJIB bisa diakses dengan **UFW enabled** (firewall menyala abangkuh 🔥🔥🔥)

---------------------------------------------------------------------------------------------------------

Untuk menjalankan semua tugas diatas, pastikan PORT Firewall yang akan digunakan sudah aktif. Seperti : 3000, 5000, dan 8080 dengan `sudo ufw status`.

<img width="625" height="421" alt="image" src="https://github.com/user-attachments/assets/cc530a42-563d-45d4-a272-215ab7355bad" />


---------------------------------------------------------------------------------------------------------


**Task 1: Install dan Deploy app wayshub-frontend dengan Menggunakan Node JS 10 & 12**
1. Install NodeJS kedalam Ubuntu Server kita. Pastikan pilih sesuai dengan OS yang digunakan dan dengan mengikuti langkah-langkah dari link : https://nodejs.org/en/download.
   <img width="625" height="268" alt="image" src="https://github.com/user-attachments/assets/8b1ba667-b0fd-4db3-8ec3-5772d35e403e" />

   <img width="625" height="314" alt="image" src="https://github.com/user-attachments/assets/30fb8bbd-2e82-4391-a39d-13d95eafe9eb" />

2. Refresh bash karena sudah menginstall nvm baru dengan `exec bash`.
   <img width="625" height="40" alt="image" src="https://github.com/user-attachments/assets/be67d322-f2e6-4a13-b5fc-4df5cb580b7d" />

3. Install Nodejs 10 dan 12 dengan `nvm install 10` untuk versi 10. Sedangkan `nvm install 12` untuk versi 12. Lalu pilih vnm versi 12 dengan `nvm use 12`.
   <img width="625" height="263" alt="image" src="https://github.com/user-attachments/assets/e8bf9183-5e33-4cba-bf36-ec3fbba5fed3" />

4. Clone link githubnya. Lalu masuk kedalam folder yang berhasil di clone.
   <img width="628" height="75" alt="image" src="https://github.com/user-attachments/assets/95b7b022-a6b6-41c9-82c5-33bd0420320c" />

5. Setelah itu ganti name yang terdapat di `package.json` menjadi `dumbways-week1`.
   <img width="630" height="509" alt="image" src="https://github.com/user-attachments/assets/766e74cf-2ff3-48ec-9b24-d282c0276c54" />

6. Lakukan install `npm` untuk menginstal dan mengelola paket/modul Node.js dengan `npm install`.
   <img width="630" height="278" alt="image" src="https://github.com/user-attachments/assets/40fbe647-086f-42f7-89a3-207dcf77b46e" />

7. Untuk running isi yang terdapat di folder github yang sudah kita clone tadi dengan `npm start`.
   <img width="630" height="522" alt="image" src="https://github.com/user-attachments/assets/b48c6a9a-b4f1-4e32-b696-d07030b571f3" />

   Lalu akan tampil di website kita dengan memasukkan `ip:3000`.
   <img width="630" height="274" alt="image" src="https://github.com/user-attachments/assets/5ae0b23f-e646-45fe-875f-38e194899f13" />


---------------------------------------------------------------------------------------------------------


**Task 2: Deploy App dengan Python untuk menampilkan nama kalian**
1. Check versi dari python yang sudah automatic terinstall di Ubuntu Server kita dengan `python3 -V`.
   Lalu buat directory baru bernama `python`.
   
   <img width="630" height="99" alt="image" src="https://github.com/user-attachments/assets/eb257643-c2cb-4e99-91ae-483fab2228a8" />

3. Install `pip` pada python kita untuk mengelola dan menginstall paket di Python dengan `sudo apt install python3-pip`.
   
   <img width="630" height="452" alt="image" src="https://github.com/user-attachments/assets/d4858cb0-819f-436a-a81c-e6ec0440d660" />

   Check versi pip dengan `pip -V`.
   
   <img width="630" height="75" alt="image" src="https://github.com/user-attachments/assets/9f6020f4-ffb5-4e7d-8345-3f0d02a0e191" />

5. Install `flask` yang merupakan sebuah framework mikro untuk Python yang digunakan untuk membangun aplikasi web atau API (Application Programming Interface).
   <img width="630" height="372" alt="image" src="https://github.com/user-attachments/assets/daec216d-e9a0-48ff-bc1d-f17e7e2cbd9b" />

6. Buat file baru bernama `index.py`
   <img width="630" height="372" alt="image" src="https://github.com/user-attachments/assets/f5ca5091-5371-4202-b849-17cd977204e2" />

7. Jalankan file `index.py` dengan `python3 index.py`.
   <img width="787" height="151" alt="image" src="https://github.com/user-attachments/assets/5b5bf53e-6596-40e3-ae1b-a0a122d5ae0b" />

   Akan tampil di browser kita sesuai dengan `ip:5000`
   <img width="736" height="130" alt="image" src="https://github.com/user-attachments/assets/2b4f410a-7b2b-4181-97d9-1efbac5174b4" />


---------------------------------------------------------------------------------------------------------


**Task 3: Deploy App dengan Golang untuk menampilkan "Golang geming!"**
1. Install `Golang` dengan menyalin dan mengikuti langkah pada link berikut `https://go.dev/doc/install`.
   <img width="636" height="298" alt="image" src="https://github.com/user-attachments/assets/82ce3519-8beb-42c3-b179-1189d1eafee3" />
   <img width="628" height="69" alt="image" src="https://github.com/user-attachments/assets/3c1bdee4-8ab3-4e77-bec5-f9a9fcdc2a88" />

2. Buat file bernama `index.go`.
   <img width="796" height="148" alt="image" src="https://github.com/user-attachments/assets/089d5d01-0e8b-47c4-8655-202818479744" />

3. Jalankan file `index.go` dengan `go run index.go`.
   <img width="795" height="63" alt="image" src="https://github.com/user-attachments/assets/20030c01-49c2-4e92-b0af-a75271f00c6b" />
   


