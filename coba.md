<h1 style="text-align:center">
   <b>Laporan Praktikum Modul 1</b>
</h1>
<h2 style="text-align:center">
    <b>Kelompok 8</b>
</h2>

**Pastikan sebelum melakukan tutorial di bawah, harap backup server terlebih dahulu untuk menghindari hal-hal yang tidak diinginkan**
**Pastikan juga anda telah melakukan latihan praktikum modul 1**
#


1. Rename ubuntu_php5.6 menjadi ubuntu_landing serta ubah IP mengikuti skema baru, seperti dibawah ini

   a. Buka terlebih dahulu ubuntu server di virtual box anda masing masing.

   b. Setelah itu, login sesuai username dan password yang anda telah buat

   c. Ketikkan code di bawah ini untuk mengganti nama LXC Container pada ubuntu server 20.04

   <p align="center">
   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no1/2021-10-20.png?raw=true">
   </p>

   - Untuk mengecek isi dan kondisi lxc container, apakah lxc sudah distop apa belum, karena jika ingin mengganti nama lxc, lxc harus distop terlebih dahulu

     ```
     sudo lxc-ls -f
     ```

   - Untuk mengganti nama sebuah lxc containers (-R -- rename,  -N --newnamecontainer)

     ```
     sudo lxc-copy -R ubuntu_php5.6 -N ubuntu_landing
     
     #Cek kondisi lxc container ulang
     sudo lxc-ls -f
     ```

   d. Menjalankan lxc ubuntu landing dengan kode di bawah ini

   <p align="center">
   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no1/2021-10-20_1.png?raw=true">
   </p>

   ```
   #Menjalankan LXC Container
   sudo lxc-start -n ubuntu_landing -d
   
   #Membuka LXC Container
   sudo lxc-attach -n ubuntu_landing
   ```

   e. Mengganti IP DHCP dari LXC ubuntu_landing menjadi IP static (sesuai ketentuan Soal Praktikum)

   <p align="center">
   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no1/2021-10-20_2.png?raw=true">
   </p>

   ```
   #Membuka config IP (pada ubuntu_landing base ubuntu 16.04 atau xenial)
   sudo nano /etc/network/interfaces
   
   #Setting IP static 
   auto eth0
   iface eth0 inet static
   	address 10.0.3.103
   	netmask 255.255.255.0
   	gateway 10.0.3.1
   	dns-nameservers 8.8.8.8 1.1.1.1	
   	
   #Menyimpan konfigurasi file (tekan pada keyboard anda)
   Ctrl+X -> Y -> Enter
   ```

   f. Restart service networking agar IP berganti sesuai yang dikonfigurasi, lalu cek kembali IP dari ubuntu_landing

   ```
   #Restart service networking pada ubuntu_landing
   reboot --kenapa reboot karena jika menggunakan systemctl restart networking.service IP tidak berganti
   
   #Membuka LXC Container ubuntu_landing lagi
   sudo lxc-attach -n ubuntu_landing
   
   #Cek IP pada ubuntu_landing
   ifconfig --IP telah berganti menjadi 10.0.3.103 sesuai ketentuan soal
   ```

   <p align="center">
   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no1/2021-10-20_3.png?raw=true">
   </p>

   g. Mencoba cek jaringan dengan ping google

   <p align="center">
   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no1/2021-10-20_4.png?raw=true">
   </p>

   

2. Install lxc debian 9 dengan nama debian_php5.6

   a. Pastikan terlebih dahulu template yang digunakan, karena debian tersedia, maka kita tinggal mencari nama dari versi debian 9 di google

   ```
   #Nama dari debian 9 adalah stretch
   sudo lxc-create -n debian_php5.6 -t download -- --dist debian --release stretch --arch amd64 --force-cache --no-validate --server images.linuxcontainers.org
   ```

   <p align="center">
   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no2/2021-10-20_5.png?raw=true">
   </p>

   

3. setup nginx pada debian_php5.6 untuk domain http://lxc_php5.dev , buat halaman index.html yang menerangkan informasi nama lxc

<p align="center">
	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_6.png?raw=true">
</p>



<p align="center">
	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_7.png?raw=true">
</p>




<p align="center">
	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_8.png?raw=true">
</p>




<p align="center">
	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_9.png?raw=true">
</p>




<p align="center">
	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_10.png?raw=true">
</p>




<p align="center">
	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_11.png?raw=true">
</p>



<p align="center">
	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_12.png?raw=true">
</p>




<p align="center">
	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_13.png?raw=true">
</p>




<p align="center">
	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_14.png?raw=true">
</p>




<p align="center">
	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_15.png?raw=true">
</p>




<p align="center">
	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_16.png?raw=true">
</p>



4. setup nginx pada ubuntu_landing untuk domain http://lxc_landing.dev , buat halaman index.html yang menerangkan informasi nama lxc 

   

   <p align="center">
   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no4/2021-10-20_17.png?raw=true">
   </p>

   

   <p align="center">
   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no4/2021-10-20_18.png?raw=true">
   </p>

   

   <p align="center">
   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no4/2021-10-20_19.png?raw=true">
   </p>

   

   <p align="center">
   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no4/2021-10-20_20.png?raw=true">
   </p>

   

   <p align="center">
   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no4/2021-10-20_21.png?raw=true">
   </p>

   

   <p align="center">
   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no4/2021-10-20_22.png?raw=true">
   </p>

   

   <p align="center">
   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no4/2021-10-20_23.png?raw=true">
   </p>

   

5. LXC ubuntu_landing harus auto start ketika vm dinyalakan, hal ini digunakan untuk menjaga agar website company profile tidak mengalami *downtime*

   

   <p align="center">
   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no5/2021-10-20_24.png?raw=true">
   </p>

   

   <p align="center">
   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no5/2021-10-20_25.png?raw=true">
   </p>

   

6. setup nginx pada vm.local untuk mengatur *proxy_pass* dimana :

   <p align="center">
   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no6/2021-10-20_26.png?raw=true">
   </p>

   

   <p align="center">
   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no6/2021-10-20_26_1.png?raw=true">
   </p>

   

   <p align="center">
   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no6/2021-10-20_27.png?raw=true">
   </p>

   

   <p align="center">
   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no6/2021-10-20_28.png?raw=true">
   </p>

   


   <p align="center">
   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no6/2021-10-20_28_1.png?raw=true">
   </p>

   

   Dan akan mendapatkan tampilan seperti ini : 

   - mengakses [http://vm.local](http://vm.local/) akan diarahkan ke http://lxc_landing.dev

     <p align="center">
     	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no6/2021-10-21.png?raw=true">
     </p>

     

   - mengakses http://vm.local/blog akan diarahkan ke http://lxc_php7.dev

     <p align="center">
     	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no6/2021-10-21_2.png?raw=true">
     </p>

     

   - mengakses http://vm.local/app akan diartahkan ke http://lxc_php5.dev

     <p align="center">
     	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no6/2021-10-21_1.png?raw=true">
     </p>

Analisa :

* Mengapa untuk kebutuhan php5.6 tidak bisa menggunakan ubuntu 16.04, sehingga perlu diganti os ke debian 9? 

  Karena, Ubuntu 16.04 telah beralih ke PHP 7.0 dengan infrastruktur baru untuk paket PHP. Jwadi, tidak, Anda tidak dapat menginstal php5 di Ubuntu 16.04, 

* Kenapa harus menggunakan virtualisasi LXC pada skema website yang akan didevelop?

  Karena, Linux Containers (LXC) adalah teknologi virtualisasi ringan dan menyediakan sistem virtualisasi perangkat lunak gratis untuk komputer yang menjalankan GNU/Linux. Hal ini dicapai melalui isolasi level kernel, memungkinkan seseorang untuk menjalankan beberapa unit virtual (wadah) secara bersamaan pada Host yang sama.

* Apa yang dimaksud dengan proxy server? kenapa vm.local bisa kita anggap sebagai proxy server?

  Proxy server menurut kami adalah sistem yang mengendalikan suatu lalu lintas data contohnya website agar kemananan dan privasi pengguna internet tersebut tetap bisa terjaga 
