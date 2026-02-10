1. Terapkan Load Balancing untuk wayshub-frontend menggunakan 2 server dengan spek yang sama
2. Gunakan 2 dari 3 pilihan method ini :
   - Round Robin
   - IP Hash
   - Least Connections

---

Urutan pengerjaan sebagai berikut :
1. Siapkan 2 App Server dengan Virtual Machine (Server 1 & Server 2)
2. Siapkan App Server sebagai Load Balancer (Server 3)
3. Config dan Testing
<img width="630" height="385" alt="image" src="https://github.com/user-attachments/assets/05da47f5-51b7-4263-897b-6f342fabd1a8" />

---

- Setelah menyiapan VMnya, Check IP di masing-masing VM dan catat.

   Server A : 192.168.0. 109
  
  <img width="623" height="246" alt="image" src="https://github.com/user-attachments/assets/a74a11de-83cf-482f-b3ad-715aed3cd495" />

  Server B : 192.168.0.108
  
  <img width="623" height="206" alt="image" src="https://github.com/user-attachments/assets/a074c8f9-006f-409f-b1ad-a17f17a6856e" />

  Server Load Balancer : 192.168.0.111

  <img width="623" height="206" alt="image" src="https://github.com/user-attachments/assets/41428d90-9547-4489-953d-f630c2aae207" />

**Config Load Balancer**

- Install nginx di Server Load Balancer
  
  <img width="623" height="145" alt="image" src="https://github.com/user-attachments/assets/cb8b8f82-3a12-4076-92e8-28ccd57ad1e8" />

- Buat file baru yang digunakan untuk konfigurasi. Dengan `sudo nano /etc/nginx/conf.d/wayshub-lb.conf`. Hapus tanda `#` di `ip_hash` jika ingin menjalankan metode IP Hash. Dan Hapus tanda `#` di `loast_conn;` jika ingin mengaktifkan metode Least Connection.
  
  <img width="623" height="399" alt="image" src="https://github.com/user-attachments/assets/0244f423-2bb5-438b-9d4b-e1e02bbd876d" />

- Setelah itu simpan dengan `ctrl+o`, `enter`, `ctrl+x`
- Setelah tersimpan, check syntax dengan `sudo nginx -t`.
  <img width="623" height="107" alt="image" src="https://github.com/user-attachments/assets/be7498b5-d1bb-474a-8f7f-4119b481280d" />

**Config Server A & Server B**
- Aktifkan Port 3000 untuk menjalankan Nodejsnya dengan `sudo ufw allow 3000`.
- Buat file dummy Nodejs di Server A dan Server B yang bernama `server.js`.

  File dummy pada Server A
  
  <img width="623" height="183" alt="image" src="https://github.com/user-attachments/assets/cee3313a-e1db-45e6-b071-f6030019bcb4" />

  File dummy pada Server B

  <img width="623" height="183" alt="image" src="https://github.com/user-attachments/assets/d76bac11-5ee0-4281-a14a-dd6917253608" />

- Jalankan file Nodejs tersebut dengan `node server.js`
  
  <img width="623" height="218" alt="image" src="https://github.com/user-attachments/assets/a12abeb0-b298-4b29-b64c-064cdf40137e" />

**Jalankan nginx pada Load Balancer**

- Untuk menjalankan nginx pada load balancer dengan memasukkan ip load balancer di browser.
- **Untuk hasil dari Metode Round Robin**, jika browser direfresh, maka akan berpindah secara bergantian dari Server A ke Server B.

  <img width="623" height="392" alt="image" src="https://github.com/user-attachments/assets/909c04ee-7fe9-4c0c-a5b6-c23b1cf34145" />

- **Untuk hasil IP HASH**, user akan diatur tetap atau stay di Server yang pertama kali masuk.

  <img width="623" height="227" alt="image" src="https://github.com/user-attachments/assets/36c34b8b-21fa-45d8-9e90-e5258e5131b8" />

- **Untuk Least Connection**, user akan otomatis masuk ke Server yang sepi dibandingkan dengan yang sedang penuh. Berikut simulasi jika Server B dijalankan file `server_labat.js`.

  <img width="623" height="227" alt="image" src="https://github.com/user-attachments/assets/a6ac2a9b-ffbf-4631-861c-07c5620e1590" />

  Browser akan loading selama 15 detik saat sudah masuk kedalam Server A. Ketika Server B antrian sudah selesai, maka otomatis akan masuk ke Server B. 

  <img width="623" height="195" alt="image" src="https://github.com/user-attachments/assets/ae539f67-e0f8-426a-8315-321d6ee9b3ef" />

  Ketika selesai antrian akan otomatis berpindah masuk ke Server B

  <img width="623" height="227" alt="image" src="https://github.com/user-attachments/assets/9efae900-c575-4e97-9b5d-9e529292d7e8" />

  

  
- 
  
