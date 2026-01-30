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






**Task : 4. Nyalakan ufw dengan memberikan akses untuk port 22, 80, 443, 3000, 5000 dan 6969!**
1. Cek status ufw (Uncomplicated Firewall) apakah sudah aktif atau belum dengan mengetik ``sudo ufw status``.
   Jika belum aktif ketik ``sudo ufw enable`` . Lalu cek kembali dengan ``sudo ufw status``
   
