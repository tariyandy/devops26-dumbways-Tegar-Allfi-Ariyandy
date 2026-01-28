**Task :**
    1. Secara konsep, jelaskan apa itu DevOps dengan bahasa kalian!
    2. Install Ubuntu Server 22.04.x LTS menggunakan Virtualbox/VMware/Virtualization Tool pilihan kalian dan buat step-by-step langkah instalasinya!
        - Gunakan IP Address xxx.xxx.xxx.208 untuk server VM kalian!
        - Pastikan Ubuntu Server kalian ada jaringan dengan test menggunakan command ping 8.8.8.8 / ping google.com
---

**1. Apa itu DevOps ?**
   Devops adalah Tim yang membuat system automation untuk membatu tim Developer dan Operations mempercepat rilis program ke publik dengan meminimalisir kesalahan dan kegagalan.
   DevOps juga melalukan monitoring setelah program di rilis dan deploy ke publik. 

   
**2. Step-by-step Instalasi Ubuntu Server dengan Virtualbox**
  Karena saya menggunakan Distro Arch - CachyOS, step-by-stepnya sebagai berikut:
  1. Update system untuk memastikan sistem dalam kondisi terbaru sebelum dilakukan instalasi
     
     `sudo pacman -Syu`
     <img width="912" height="204" alt="image" src="https://github.com/user-attachments/assets/b6d1e8ba-1d75-4819-b191-16fbd3082742" />

  3. Instalasi Virtualbox
     `sudo pacman -S virtualbox virtualbox-guest-iso virtualbox-host-dkms`
     <img width="912" height="279" alt="image" src="https://github.com/user-attachments/assets/5619794c-72ac-4b9a-8c12-e951a468be26" />

  4. Sinkronisasi Database dan Header
     `sudo pacman -Syu linux-cachyos-headers`
     <img width="676" height="232" alt="image" src="https://github.com/user-attachments/assets/c05f34ba-f100-42cd-ad54-43cb75cf08c4" />

  5. Instalasi Driver DKMS
     `sudo pacman -S virtualbox-host-dkms`
     <img width="561" height="209" alt="image" src="https://github.com/user-attachments/assets/474fa3e9-4419-419c-aa8c-cb34fe095642" />

  6. Picu Kompilasi Driver
     `sudo dkms autoinstall`
     <img width="248" height="57" alt="image" src="https://github.com/user-attachments/assets/f8ad9808-b267-46b9-b7e2-ff623d6987e3" />

  7. Load Modul Kembali
     `sudo modprobe vboxdrv`
     <img width="248" height="57" alt="image" src="https://github.com/user-attachments/assets/1a28edb3-82fc-4680-8ac2-5c700860ca24" />

    ** Lalu Restart PCnya. **

  7. Instalasi Virtualbox Manager
     **Buka Aplikasi Oracle Virtualbox Manager, Klik New lalu :**
     - Masukkan VN Name yang sesuai
     - Pilih lokasi folder penyimpanan VM
     - Pilih File ISO yang sudah di download
     - Jangan di Checklist Proceed with Unattanded Instalation
     <img width="826" height="595" alt="image" src="https://github.com/user-attachments/assets/ed83d2fe-5810-47a8-ba49-3a7df7c15211" />
  
     **Pilih Spesifikasi Virtual Hardwarenya (Base memory/ RAM, dan CPU) yang nantinya akan digunakan**
    <img width="824" height="596" alt="image" src="https://github.com/user-attachments/assets/5d315013-a6e1-48ba-bdaa-88c26895308b" />

     **Buat Virtual Hardisk/ penyimpanan yang nantinya akan digunakan juga.**
    <img width="824" height="596" alt="image" src="https://github.com/user-attachments/assets/61f8fb55-ad93-4534-b3df-4a4128e264c3" />

  8. **Jalankan Virtual Ubuntu Servernya dengan Klik Start**
     <img width="968" height="860" alt="image" src="https://github.com/user-attachments/assets/4a7835bd-f273-4c69-9b5d-fa524fc8f3fd" />

  9. Klik tombol enter "try or Install Ubuntu Server"
     <img width="748" height="484" alt="image" src="https://github.com/user-attachments/assets/de9b6a1d-fdaa-4cce-84e3-9ddeda2a0daa" />

  10. Pilih bahasa yang akan digunakan, lalu Enter
     <img width="811" height="675" alt="image" src="https://github.com/user-attachments/assets/d3c7554e-b4c7-4a7b-941d-60530c46a4a6" />

  11. Pilih Continue without updating, lalu Enter
     <img width="811" height="675" alt="image" src="https://github.com/user-attachments/assets/f3976ba3-8fcf-4383-b59b-df5be642c393" />

  12. Untuk Layot Keyboard lewati saja, lalu Enter
  13. Untuk type of instalation pilih Ubuntu Server saja. Pilih Done lalu tekan Enter
      <img width="811" height="675" alt="image" src="https://github.com/user-attachments/assets/d2f933c5-8350-427d-a845-6c88b25de56c" />
  
  14. Saat halaman Network Configuration, samakan IP dan Gatewaynya dengan settingan yang ada di laptop.
      Untuk melihat IP pada PC kita ketik:
      bash : ip a
      <img width="871" height="280" alt="image" src="https://github.com/user-attachments/assets/b1e361e9-15d9-4db9-be72-27a097b775a9" />

  15. Atur manual pada IPV4 nya, dan masukkan :
      subnet 192.168.96.0/24
      addres 192.168.96.208
      gateway 192.168.96.1
      name server 8.8.8.8, 8.8.4.4
      pilih save, lalu enter
      <img width="817" height="678" alt="image" src="https://github.com/user-attachments/assets/ca719660-c469-48ec-b0c6-7d2f99548325" />

  17. Setelah muncul "Done" lalu Enter
      <img width="817" height="678" alt="image" src="https://github.com/user-attachments/assets/92b9f2c7-cc25-4838-9256-b9afb63e3573" />

  18. Tidak perlu melakukan penyetingan Proxy Address, pilin "done" lalu enter.
  19. Saat ubuntu melakukan mirror configuration, pilih "done". Lalu pilih "continue"
      <img width="813" height="678" alt="image" src="https://github.com/user-attachments/assets/a6a23df0-01aa-4761-940b-d65e61236ad0" />

  20. Pada pengaturan storage, Pilih custom storage layout.
  21. Saat muncul menu storage configuration, pada bagian free space pilih lalu enter
      pilih Add GPT Partition - Masukkan ukuran partisi yang akan diisi (saya pilih 15G)
      Format ext 4
      lalu pilih Create
      <img width="813" height="678" alt="image" src="https://github.com/user-attachments/assets/21871e18-ef55-4726-8017-8716fbb1bc3a" />

  22. Pilih free space lagi - Add GPT Partition - Masukkan sisa memory yang tersedia untuk dijadikan tambahan RAM
      Format swap
      lalu pilih Create
      <img width="813" height="678" alt="image" src="https://github.com/user-attachments/assets/f9e44b75-1f76-43e8-a753-93d28cedca96" />

  23. Setelah selesai, klik Done lalu Continue untuk melanjutkan
      <img width="813" height="678" alt="image" src="https://github.com/user-attachments/assets/9b038c3a-4b53-41c1-b61d-0451dff184b6" />

  24. Masukkan Profile configurattion
      isikan nama, nama server, username dan passwordnya
      lalu pilih Done
      <img width="813" height="678" alt="image" src="https://github.com/user-attachments/assets/d503966f-8089-4519-a2d9-058de29d5b28" />

  26. Pada pilihan upgrade to Ubuntu Pro, Pilih skip for now, lalu continue
  27. Saat diminta configuration SSH, tidak perlu di ceklis, pilih Done
      <img width="813" height="678" alt="image" src="https://github.com/user-attachments/assets/776ecdfa-ca2a-4721-99c4-f36784387571" />

  28. Saat muncul feature server naps, tidak perlu ada yang diceklis. Pilih Done
  29. Lalu tunggu proses installing system yang berjalan
      <img width="813" height="678" alt="image" src="https://github.com/user-attachments/assets/5a70678a-ff92-41c1-b8b2-963b4e59b5ee" />

  30. **Setelah proses installing selesai, login dengan username dan password yang sudah diisi sebelumnya**
  31. **Lakukan pengetesan jaringan dengan mengetik :**
      `ping 8.8.8.8`
      atau `ping google.com`
      <img width="813" height="678" alt="image" src="https://github.com/user-attachments/assets/ce5a7547-1a58-44c8-8e4a-5c9fc6414d61" />









    
