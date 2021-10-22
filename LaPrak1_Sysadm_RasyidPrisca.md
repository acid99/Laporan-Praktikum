1. Rename ubuntu_php5.6 menjadi ubuntu_landing serta ubah IP mengikuti skema baru, seperti dibawah ini

    ![2021-10-20.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no1/2021-10-20.png?raw=true)

    

    ![2021-10-20_1.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no1/2021-10-20_1.png?raw=true)

    

    ![2021-10-20_2.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no1/2021-10-20_2.png?raw=true)

    

    ![2021-10-20_2.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no1/2021-10-20_2.png?raw=true)

    
    
    ![2021-10-20_3.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no1/2021-10-20_3.png?raw=true)
    
    
    
    ![2021-10-20_4.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no1/2021-10-20_4.png?raw=true)
    
2. Install lxc debian 9 dengan nama debian_php5.6

   ![2021-10-20_5.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no2/2021-10-20_5.png?raw=true)

3. setup nginx pada debian_php5.6 untuk domain http://lxc_php5.dev , buat halaman index.html yang menerangkan informasi nama lxc

![2021-10-20_6.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_6.png?raw=true)

![2021-10-20_7.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_7.png?raw=true)

![2021-10-20_8.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_8.png?raw=true) 

![2021-10-20_9.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_9.png?raw=true) 

![2021-10-20_10.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_10.png?raw=true) 

![2021-10-20_11.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_11.png?raw=true) 

![2021-10-20_12.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_12.png?raw=true) 

![2021-10-20_13.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_13.png?raw=true)  

![2021-10-20_14.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_14.png?raw=true) 

 ![2021-10-20_15.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_15.png?raw=true) 

![2021-10-20_16.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no3/2021-10-20_16.png?raw=true) 

 

4. setup nginx pada ubuntu_landing untuk domain http://lxc_landing.dev , buat halaman index.html yang menerangkan informasi nama lxc

![2021-10-20_17.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no4/2021-10-20_17.png?raw=true) 

![2021-10-20_18.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no4/2021-10-20_18.png?raw=true) 

![2021-10-20_19.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no4/2021-10-20_19.png?raw=true) 

![2021-10-20_20.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no4/2021-10-20_20.png?raw=true) 

![2021-10-20_21.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no4/2021-10-20_21.png?raw=true) 

![2021-10-20_22.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no4/2021-10-20_22.png?raw=true) 

![2021-10-20_23.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no4/2021-10-20_23.png?raw=true) 

  

5. LXC ubuntu_landing harus auto start ketika vm dinyalakan, hal ini digunakan untuk menjaga agar website company profile tidak mengalami *downtime*

 ![2021-10-20_24.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no5/2021-10-20_24.png?raw=true) 

![2021-10-20_25.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no5/2021-10-20_25.png?raw=true) 



6. setup nginx pada vm.local untuk mengatur *proxy_pass* dimana :

- mengakses [http://vm.local](http://vm.local/) akan diarahkan ke http://lxc_landing.dev
- mengakses http://vm.local/blog akan diarahkan ke http://lxc_php7.dev
- mengakses http://vm.local/app akan diartahkan ke http://lxc_php5.dev

 ![2021-10-20_26.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no6/2021-10-20_26.png?raw=true) 

![2021-10-20_26_1.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no6/2021-10-20_26_1.png?raw=true) 

![2021-10-20_27.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no6/2021-10-20_27.png?raw=true) 

![2021-10-20_28.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no6/2021-10-20_28.png?raw=true) 

![2021-10-20_28_1.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no6/2021-10-20_28_1.png?raw=true) 



Dan akan mendapatkan tampilan seperti ini : 

 ![2021-10-21.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no6/2021-10-21.png?raw=true) 

![2021-10-21_1.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no6/2021-10-21_1.png?raw=true) 

![2021-10-21_2.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no6/2021-10-21_2.png?raw=true) 



Analisa :

* Mengapa untuk kebutuhan php5.6 tidak bisa menggunakan ubuntu 16.04, sehingga perlu diganti os ke debian 9? 

  Karena, Ubuntu 16.04 telah beralih ke PHP 7.0 dengan infrastruktur baru untuk paket PHP. Jadi, tidak, Anda tidak dapat menginstal php5 di Ubuntu 16.04, 

* Kenapa harus menggunakan virtualisasi LXC pada skema website yang akan didevelop?

  Karena, Linux Containers (LXC) adalah teknologi virtualisasi ringan dan menyediakan sistem virtualisasi perangkat lunak gratis untuk komputer yang menjalankan GNU/Linux. Hal ini dicapai melalui isolasi level kernel, memungkinkan seseorang untuk menjalankan beberapa unit virtual (wadah) secara bersamaan pada Host yang sama.

* Apa yang dimaksud dengan proxy server? kenapa vm.local bisa kita anggap sebagai proxy server?

  Proxy server menurut kami adalah sistem yang mengendalikan suatu lalu lintas data contohnya website agar kemananan dan privasi pengguna internet tersebut tetap bisa terjaga 