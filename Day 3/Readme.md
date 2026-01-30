**Task : 3. Buat step by step penggunaan text manipulation! (grep, sed, cat, echo)**
1. ``grep`` berfungsi untuk mencari kata atau pola tertentu di dalam file. ``Grep`` juga dapat digunakan untuk menghitung jumlah kata yang dicari.
Adapun fungsi ``grep`` untuk mencari jumlah kata "hai" yang berada di file text1 dengan ``grep "hai" test1``. Dan Berikut fungsi ``grep`` untuk menghitung jumlah kata "hai" yang berada di file text1.
<img width="903" height="102" alt="image" src="https://github.com/user-attachments/assets/0200795d-72b6-42bc-8bce-a3ec3c55e579" />

2. ``sed`` berfungsi untuk mengubah teks secara otomatis tanpa membuka filenya. Berikut contoh ``sed -i 's/hai/Hello/g' text1``
<img width="905" height="65" alt="image" src="https://github.com/user-attachments/assets/414aad94-f059-4224-b1fa-72cdf95510e7" />





**Task : 4. Nyalakan ufw dengan memberikan akses untuk port 22, 80, 443, 3000, 5000 dan 6969!**
1. Cek status ufw (Uncomplicated Firewall) apakah sudah aktif atau belum dengan mengetik ``sudo ufw status``.
   Jika belum aktif ketik ``sudo ufw enable`` . Lalu cek kembali dengan ``sudo ufw status``
   
