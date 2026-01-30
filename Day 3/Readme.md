**Task : 1. Akses server menggunakan terminal**
1. Instal OpenSSH agar koneksi dari terminal Laptop kita dapat terhubung dengan Virtual Machine. Dengan ``sudo install openssh-server``.
   <img width="801" height="146" alt="image" src="https://github.com/user-attachments/assets/218e7dbf-c3e6-4e50-8dad-b4a3a2693aee" />

2. Pastikan system ssh sudah running yang dapat dilihat dengan ``sudo systemctl status ssh`` digunakan untuk mengatur beberapa aplikasi yang berjalan di server.
   <img width="807" height="426" alt="image" src="https://github.com/user-attachments/assets/750e046f-f029-4527-a500-52063b8645b2" />
Namun jika belum running dapat dengan ``sudo systemctl restart ssh``.

3. Untuk akses Virtual Machine, dapat diakses dengan ``ssh username@ipvm``. Contohnya ``ssh tariyandy@100.75.106.107``.
   <img width="905" height="429" alt="image" src="https://github.com/user-attachments/assets/c946da5c-80ec-4184-82c7-2655285d5570" />

4. Untuk mengakses file yang terdapat pada Virtual Machine, apa yang diakses pada terminal komputer akan sama dengan yang terdapat pada Virtual Machine. Contohnya dengan ``ls`` untuk melihat isi file.
   <img width="1364" height="186" alt="image" src="https://github.com/user-attachments/assets/c255ea58-5b4b-4685-91ff-2d2a0f7e6ee1" />


----------------------------------------------------------------------------------------------------------------------


**Task : 2. Konfigurasi SSH agar dapat diakses hanya menggunakan publickey**
1. ``ssh-keygen`` digunakan untuk membuat dan mendapatkan kunci ssh. Lalu masukkan lokasi penyimpanan kunci dengan /home/username/.ssh/namakunci``. Contohnya ``/home/tariyandy/.ssh/gembok``.
   <img width="886" height="368" alt="image" src="https://github.com/user-attachments/assets/68df5df8-badb-480f-9b67-0ded5ddb97bd" />

2. Lalu check isi folder ``.ssh`` dengan ``ls``.
   <img width="886" height="66" alt="image" src="https://github.com/user-attachments/assets/435dbbc0-40a6-490b-b4c0-c53be4c1a31d" />

3. Buka file gembok.pub untuk melihat public keynya dengan ``cat gembok.pub`` lalu copy isi public keynya. 
   <img width="881" height="164" alt="image" src="https://github.com/user-attachments/assets/cc296d1f-3177-48d3-8f57-94400bf79d4d" />

4. Setelah mengcopy publik keynya, masuk kedalam file ``authorized_keys`` lalu paste public keynya kedalam file tersebut dengan ``nano authorized_key``
   <img width="881" height="164" alt="image" src="https://github.com/user-attachments/assets/b2935dc0-771d-4ab9-9aa0-cc1e475bcea6" />

5. Keluar dari ssh sebelumnya dengan ``logout``, lalu masuk lagi kedalam ssh dengan ``ssh -i .ssh/gembok username@ipvm``
   <img width="886" height="66" alt="image" src="https://github.com/user-attachments/assets/b370e86c-c801-4e5a-a49a-aca7b2962cda" />


----------------------------------------------------------------------------------------------------------------------


**Task : 3. Buat step by step penggunaan text manipulation! (grep, sed, cat, echo)**
1. ``grep`` berfungsi untuk mencari kata atau pola tertentu di dalam file. ``Grep`` juga dapat digunakan untuk menghitung jumlah kata yang dicari.
Adapun fungsi ``grep`` untuk mencari jumlah kata "hai" yang berada di file test1 dengan ``grep "hai" test1``. Dan Berikut fungsi ``grep`` untuk menghitung jumlah kata "hai" yang berada di file test1.
   <img width="903" height="102" alt="image" src="https://github.com/user-attachments/assets/0200795d-72b6-42bc-8bce-a3ec3c55e579" />

2. ``sed`` berfungsi untuk mengubah teks secara otomatis tanpa membuka filenya. Berikut contoh ``sed -i 's/hai/Hello/g' text1``
   <img width="905" height="65" alt="image" src="https://github.com/user-attachments/assets/414aad94-f059-4224-b1fa-72cdf95510e7" />

3. ``cat`` berfungsi untuk melihat isi file tanpa harus membukanya dengan editor seperti nano. ``cat`` juga dapat digunakan untuk menggabungkan 2 file yang berbeda menjadi 1 file.
Adapun fungsi ``cat`` untuk membuka file dengan ``cat test1``, dan untuk menggabungkan 2 file berbeda dengan ``cat test1 test2 > gabungantest``.
   <img width="900" height="100" alt="image" src="https://github.com/user-attachments/assets/3785a78a-15cd-410e-9e1e-64552a5123bd" />

4. ``echo`` berfungsi untuk menampilkan teks ke layar, membuat file baru dengan isi teks, menambah teks ke file yang sudah ada dan juga untuk menampilkan nilai variabel. Untuk menampilkan ``echo`` untuk menampilkan isi teks ke layar dengan ``echo "Hallo, saya belajar menampilkan echo"``, Untuk membuat file baru dengan isi teks dengan ``echo "Ini latihan isi file dengan echo" > latihanecho1``, Untuk Menambahkan teks ke file yang sudah ada dengan ``echo "Ini tambahan teksnya" >> latihanecho1``, dan untuk mengetahui lokasi folder saat ini dengan ``echo $PWD``.
   <img width="908" height="228" alt="image" src="https://github.com/user-attachments/assets/e224ff39-7477-44a8-b240-1ac12d5bf216" />


----------------------------------------------------------------------------------------------------------------------


**Task : 4. Nyalakan ufw dengan memberikan akses untuk port 22, 80, 443, 3000, 5000 dan 6969!**
1. Untuk mengaktifkan port dengan ``sudo ufw allow "Port". Contohnya dengan ``sudo ufw allow 22"
   <img width="902" height="664" alt="image" src="https://github.com/user-attachments/assets/f9217b82-d1e4-4b7b-a5ae-73fdd0d38f16" />
3. Untuk mematikan port yang tidak digunakan dengan ``sudo ufw deny "Port"``. Contohnya ``sudo ufw deny 6969``
   <img width="902" height="437" alt="image" src="https://github.com/user-attachments/assets/82305603-053c-4085-af70-bd18c96b5906" />
4. Untuk menghapus port yang tidak digunakan dengan ``sudo ufw delete allow "port"``. Contohnya dengan ``sudo ufw delete ufw allow 80``.
   <img width="902" height="405" alt="image" src="https://github.com/user-attachments/assets/ee82fc66-34c7-43b8-99f9-ccf143135cd7" />

   


   








   
   
