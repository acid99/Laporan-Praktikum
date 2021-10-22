# Laporan Praktikum Modul 1

## Kelompok 8

**Pastikan sebelum melakukan tutorial di bawah, harap backup server terlebih dahulu untuk menghindari hal-hal yang tidak diinginkan**

**Pastikan juga anda telah melakukan latihan praktikum modul 1 dengan catatan BERHASIL**



1. **Rename ubuntu_php5.6 menjadi ubuntu_landing serta ubah IP mengikuti skema baru**

    a. Buka terlebih dahulu ubuntu server di virtual box anda masing masing.

    b. Setelah itu, login sesuai username dan password yang anda telah buat

    c. Ketikkan code di bawah ini untuk mengganti nama LXC Container pada ubuntu server 20.04


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

    <p align="center">
    	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no1/2021-10-20.png?raw=true">
    </p>

    d. Menjalankan lxc ubuntu landing dengan kode di bawah ini

    ```
    #Menjalankan LXC Container
    sudo lxc-start -n ubuntu_landing -d
    
    #Membuka LXC Container
    sudo lxc-attach -n ubuntu_landing
    ```

    <p align="center">
    	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no1/2021-10-20_1.png?raw=true">
    </p>
    e. Mengganti IP  sesuai ketentuan Soal Praktikum

    ```
    #Membuka config IP (pada ubuntu_landing base ubuntu 16.04 atau xenial)
    sudo nano /etc/network/interfaces
    ```

    <p align="center">
    	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no1/2021-10-20_2.png?raw=true">
    </p>
    ```
    #Menyimpan konfigurasi file (tekan pada keyboard anda)
    Ctrl+X -> Y -> Enter
    ```

    

    f. Restart service networking agar IP berganti sesuai yang dikonfigurasi, lalu cek kembali IP dari ubuntu_landing

    ```
    #Restart service networking pada ubuntu_landing
    reboot 
    note:kenapa reboot karena jika menggunakan systemctl restart networking.service IP tidak berganti
    
    #Membuka LXC Container ubuntu_landing lagi
    sudo lxc-attach -n ubuntu_landing
    
    #Mengecek IP pada ubuntu_landing
    ifconfig 
    note:IP telah berganti menjadi 10.0.3.103 sesuai ketentuan soal
    ```

    <p align="center">
    	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no1/2021-10-20_3.png?raw=true">
    </p>

    g. Mengecek jaringan internet dan keluar pada LXC ubuntu_landing

    ```
    #Mengecek jaringan internet
    ping google.com
    
    #Keluar di LXC container
    exit
    ```

    <p align="center">
    	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no1/2021-10-20_4.png?raw=true">
    </p>
    

2. **Install lxc debian 9 dengan nama debian_php5.6**

   a. Pastikan terlebih dahulu template yang digunakan, karena debian tersedia, maka kita tinggal mencari nama dari versi debian 9 di google

   ```
   #Mendownload dan Menginstall lxc debian 9
   sudo lxc-create -n debian_php5.6 -t download -- --dist debian --release stretch --arch amd64 --force-cache --no-validate --server images.linuxcontainers.org
   
   note: Nama dari debian 9 adalah stretch
   ```

   <p align="center">
   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no2/2021-10-20_5.png?raw=true">
   </p>
   

3. **Setup nginx pada debian_php5.6 untuk domain http://lxc_php5.dev , buat halaman index.html yang menerangkan informasi nama lxc**

    a. Menjalankan LXC debian_php5.6

    ```
    #Mengecek kondisi LXC container
    sudo lxc-ls -f
    
    #Menjalankan LXC Container
    sudo lxc-start -n debian_php5.6 -d
    
    #Membuka LXC Container
    sudo lxc-attach -n debian_php5.6
    ```

    <p align="center">
    	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_6.png?raw=true">
    </p>
    b. Menginstall package nano (untuk membuka dan mengedit konfigurasi), net-tools (untuk mengatur serta mengecek kebutuhan internet), dan curl (untuk mengecek konektivitas URL)

    <p align="center">
    	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_7.png?raw=true">
    </p>
    c. Mengatur IP Static sesuai soal praktikum

    ```
    #Membuka config IP (pada debian_php5.6 base debian 9 atau stretch)
    sudo nano /etc/network/interfaces
    ```

    <p align="center">
    	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_8.png?raw=true">
    </p>
    ```
    #Menyimpan konfigurasi file (tekan pada keyboard anda)
    Ctrl+X -> Y -> Enter
    ```

    d. Restart service networking agar IP berganti sesuai yang dikonfigurasi, lalu cek kembali IP dari debian_php5.6

    ```
    #Restart service networking pada ubuntu_landing
    reboot
    note:kenapa reboot karena jika menggunakan systemctl restart networking.service IP tidak berganti
    
    #Membuka LXC Container ubuntu_landing lagi
    sudo lxc-attach -n ubuntu_landing
    
    #Mengecek IP pada ubuntu_landing
    note:IP telah berganti menjadi 10.0.3.103 sesuai ketentuan soal
    ```

    <p align="center">
    	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_9.png?raw=true">
    </p>
    e. Menginstall package nginx untuk proxy server

    <p align="center">
    	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_10.png?raw=true">
    </p>

    f. Masuk ke dalam direktori nginx, kemudian buat file konfigurasi lxc_php5.6.dev

    ```
    #Masuk ke dalam direktori nginx
    cd /etc/nginx/sites-available/
    
    #Membuat file konfigurasi
    touch lxc_php5.6.dev
    
    #Membuka dan mengedit file konfigurasi
    nano lxc_php5.6.dev
    ```

    - Isi file konfigurasi seperti gambar berikut

    <p align="center">
    	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_11.png?raw=true">
    </p>

    ```
    #Menyimpan konfigurasi file (tekan pada keyboard anda)
    Ctrl+X -> Y -> Enter
    ```

    g. Mengaktifkan konfigurasi nginx

    ```
    #Masuk ke direktori sites-enabled
    cd ../sites-enabled
    
    #Me-link file konfigurasi lxc_php5.6.dev dari direktori sites-available ke direktori sites-enabled
    ln -s /etc/nginx/sites-available/lxc_php5.6.dev
    
    #Mengaktifkan konfigurasi nginx
    nginx -t
    
    #Menyalakan ulang package nginx
    nginx -s reload
    ```

    <p align="center">
    	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_12.png?raw=true">
    </p>
    h. Menambah isi file hosts

    - Menambahkan hosts bernama lxc_php5.dev dengan IP sama seperti localhost agar file konfigurasi yang telah dibuat bisa terdefinisikan

    <p align="center">
    	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_13.png?raw=true">
    </p>
    i. Membuka file index.html agar nantinya ketika masuk ke dalam link URL lxc_php5.6.dev maka keluar sesuai isi dari file tersebut

    ```
    #Masuk ke direktori web
    cd /var/www/html
    
    #Membuat direkotri
    mkdir lxc_php5.6
    
    #Mengkopi file default index nginx ke direktori yang telah dibuat
    cp index.nginx-debian.html lxc_php5.6/index.html
    
    @Membuka dan Mengedit isi file
    nano index.html
    ```

    <p align="center">
    	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_14.png?raw=true">
    </p>
    j. Menambahkan isi dari index.html agar ketika dibuka menampilkan informasi dari LXC

    <p align="center">
    	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_15.png?raw=true">
    </p>
    ```
    #Menyimpan konfigurasi file (tekan pada keyboard anda)
    Ctrl+X -> Y -> Enter
    ```


    k. Mengecek konektivitas dari LXC yang telah dibuat

    ``` 
    curl -i http://lxc_php5.dev
    ```

    <p align="center">
    	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_16.png?raw=true">
    </p>

    ```
    #Keluar di LXC container
    exit
    ```

    Note : Jika berhasil maka tertulis bahwa HTTP/1.1 200 OK, jika belum berhasil ulangi langkah ke 3.

4. **Setup nginx pada ubuntu_landing untuk domain http://lxc_landing.dev , buat halaman index.html yang menerangkan informasi nama lxc**

   

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
   
   
5. **LXC ubuntu_landing harus auto start ketika vm dinyalakan, hal ini digunakan untuk menjaga agar website company profile tidak mengalami  downtime**

   

   <p align="center">
   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no5/2021-10-20_24.png?raw=true">
   </p>
   

   <p align="center">
   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no5/2021-10-20_25.png?raw=true">
   </p>
   
   
6. **Setup nginx pada vm.local untuk mengatur proxy_pass**

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


​     

   - mengakses http://vm.local/blog akan diarahkan ke http://lxc_php7.dev

     <p align="center">

   	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no6/2021-10-21_2.png?raw=true">
   	 </p>


​     

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