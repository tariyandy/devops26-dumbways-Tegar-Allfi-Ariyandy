Challenge :
1. NodeJS + Python berjalan di background (tanpa kondisi attached di terminal)
   - artinya, teman-teman tetep bisa menggunakan terminal di window yang sama namun app tetap berjalan

2. Golang bisa dibuka di browser kalian, menampilkan text "Jangan lupa sahur baby gurl rawr"

_______________________________________________________________________________________________________________________

**Challange 1. NodeJS + Python berjalan dibackground**
1. Install `pm2` dengan `npm install pm2`
   <img width="792" height="135" alt="image" src="https://github.com/user-attachments/assets/89175534-8138-44fd-bf16-5d22ef355cac" />

2. Cek status pm2 dengan `pm2` status.
   <img width="792" height="96" alt="image" src="https://github.com/user-attachments/assets/65ef5c95-8e43-4d89-9e49-b757b9351984" />

3. Aktifkan NodeJS melalui pm2 dengan `pm2 start npm --name 'NodeJs` -- start`
   <img width="794" height="144" alt="image" src="https://github.com/user-attachments/assets/e9dbc1cb-7651-4cb0-bdc7-17a475c8cd79" />

4. Aktifkan Python melalui pm2 dengan `pm2 start index.py --interpreter python3`.
   <img width="794" height="132" alt="image" src="https://github.com/user-attachments/assets/d5d11a45-1f83-46d3-8f2c-63505f20bc5a" />

5. Cek status pm2 apakah status aplikasi sudah online atau belum dengan `pm2 status`.
   <img width="794" height="132" alt="image" src="https://github.com/user-attachments/assets/bae891d9-3a3d-4188-848c-37669495f1bc" />

6. Jalankan aplikasi di browser.
   <img width="961" height="954" alt="image" src="https://github.com/user-attachments/assets/2b8285d3-0251-4a61-bfb3-eea74d444935" />

_______________________________________________________________________________________________________________________

**Challange 2. Golang bisa dibuka di browser, dan diaktifkan dengan pm2**
1. Masuk kedalam directory golang yang sudah dibuat. dan buat file bernama `main.go`.
   <img width="793" height="296" alt="image" src="https://github.com/user-attachments/assets/69991560-c918-41d6-996c-e57da0d21a86" />
   
2. Jalankan dengan `go run main.go`.
   <img width="797" height="57" alt="image" src="https://github.com/user-attachments/assets/22d1b67f-a3e0-4d85-bf1a-43699ea3c356" />

   <img width="957" height="152" alt="image" src="https://github.com/user-attachments/assets/8e37806f-f7f9-4d1b-9ab4-816ffd76f9d0" />

3. Jika aplikasi ingin berjalan dibackground, ubah `main.go` menjadi file aplikasi siap pakai dengan `go build -o golang-app main.go`.

   <img width="797" height="66" alt="image" src="https://github.com/user-attachments/assets/1abfa789-060d-471d-85e6-a4ff6642c791" />

5. Jalankan aplikasi siap pakai tadi via pm2 dengan `pm2 start ./golang-app --name "golang". Lalu cek status yang berjalan.

   <img width="797" height="292" alt="image" src="https://github.com/user-attachments/assets/e330ecf8-9731-4a23-80e7-c49b0921a918" />

<img width="960" height="979" alt="image" src="https://github.com/user-attachments/assets/979c8c4f-245d-4e95-b58b-ee49d3a2e491" />

