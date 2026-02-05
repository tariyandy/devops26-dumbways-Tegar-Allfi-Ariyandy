Task :
1. Gambarkan sturktur web server menggunakan reverse proxy dan jelaskan cara kerjanya!
2. Buatlah Reverse Proxy untuk aplilkasi yang sudah kalian deploy kemarin. (wayshub), untuk domain nya sesuaikan nama masing" ex: ade.xyz .

------------------------------------------------------------------------------------------------------
**Task 1. Gambarkan struktur web server menggunakan reverse proxy dan jelaskan cara kerjanya**
<img width="711" height="283" alt="image" src="https://github.com/user-attachments/assets/2f1a8878-ffb1-4f67-a944-dbbfed2b83e7" />

**Alur Kerja Sistem:**
  1. Permintaan pengguna mengakses website melalui device mereka via internet menggunakan protokol HTTP/HTTPS.
  2. Nginx sebagai Reverse Proxy menerima semua permintaan yang masuk. Nginx bertindak sebagai "polisi lalu lintas" yang meneruskan permintaan tersebut berdasarkan alamat URL yang dituju.
  3. Rute Frontend (/) aktif ketika pengguna mengakses halaman utama, Nginx meneruskan permintaan ke Server Frontend (React) yang berjalan.
  4. Rute Backend (/api) aktif ketika pengguna atau aplikasi Frontend meminta data, Nginx meneruskan permintaan ke Server Backend (Golang) yang berjalan.
  5. Respon Server Aplikasi Frontend atau Backend memproses permintaan tersebut dan mengirimkan hasilnya kembali ke Nginx.
  6. Nginx menerima hasil dari aplikasi, lalu mengirimkannya kembali ke device pengguna. Dari sisi pengguna, mereka hanya berinteraksi dengan satu server (Nginx), tanpa mengetahui bahwa di belakangnya terdapat dua layanan berbeda yang bekerja sama.


------------------------------------------------------------------------------------------------------

**Task 2. Buatlah Reverse Proxy untuk aplikasi Wayshub, dengan domain disesuaikan nama masing-masing**
1. Masuk ke directory `/etc` dan tambahkan ip server dan domain yang akan digunakan di file `host`. Contoh `100.75.106.107 tariyandy.xyz`.
   <img width="755" height="146" alt="image" src="https://github.com/user-attachments/assets/c59a6278-161b-4254-b537-e0ada22f49b7" />

2. Didalam Ubuntu Server, install `nginx` dengan `sudo apt install nginx`. Lalu cek status `nginx` dengan `sudo systemctl status nginx` apakah sudah running atau belum. Jika belum dapat diaktifkan dengan `sudo systemctl restart nginx`.
   
   <img width="755" height="138" alt="image" src="https://github.com/user-attachments/assets/53d9f22f-ca5d-494e-bb60-86aa1e85f16c" />
   <img width="755" height="282" alt="image" src="https://github.com/user-attachments/assets/042201a0-68c3-41f5-9221-80f6fcc508d2" />

3. Lakukan ujicoba apakah `nginx` sudah aktif ketika `run IP dan domain` yang sudah didaftarkan di directory `/etc/hosts/`.

   <img width="755" height="593" alt="image" src="https://github.com/user-attachments/assets/5cfcbd1d-3ff1-44e8-b003-3e24c66890a8" />

5. Ketika nginx telah berjalan, masuk kembali ke directory `/etc/nginx`, dan cek apakah folder `sites-available` tersedia atau tidak.
   <img width="755" height="110" alt="image" src="https://github.com/user-attachments/assets/4493d977-fff9-40ba-b22f-a20b4e0140c0" />

6. Daftarkan kembali dengan membuat file baru bernama `wayshub_frontend.conf` dan memasukkan server name dan lokasi proxy nya seperti gambar berikut.
   <img width="755" height="139" alt="image" src="https://github.com/user-attachments/assets/40a4bd52-800d-4bcd-bc65-c5d73153730e" />

7. Setelah server name dan lokasi proxy dimasukkan, selanjutkan lakukan pengecekan apakah konfigurasi nginx sudah benar dengan `sudo nginx -t`.
   Setelah tampil `OK dan SUccessful`, masukkan domain ke browser.
   
   <img width="755" height="106" alt="image" src="https://github.com/user-attachments/assets/1f5523b2-fd9f-4ad4-93bf-ab280c169d85" />
   <img width="755" height="719" alt="image" src="https://github.com/user-attachments/assets/ee5435c5-1711-4836-bc1a-52c5e41d2523" />


