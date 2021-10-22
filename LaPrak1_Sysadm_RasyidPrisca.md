1. Rename ubuntu_php5.6 menjadi ubuntu_landing serta ubah IP mengikuti skema baru, seperti dibawah ini

    ![](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no1/2021-10-20.png?raw=true)

    

    ![](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no1/2021-10-20_1.png?raw=true)

    

    ![2021-10-20_2.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no1/2021-10-20_2.png?raw=true)

    

    ![2021-10-20_2.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no1/2021-10-20_2.png?raw=true)

    
    
    ![2021-10-20_3.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no1/2021-10-20_3.png?raw=true)
    
    
    
    ![2021-10-20_4.png](https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak1/no1/2021-10-20_4.png?raw=true)
    
    
    
    





2. Install lxc debian 9 dengan nama debian_php5.6

   ![2021-10-20_5](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.617223b91718f6c0\2021-10-20_5.png)   



3. setup nginx pada debian_php5.6 untuk domain http://lxc_php5.dev , buat halaman index.html yang menerangkan informasi nama lxc

![2021-10-20_6](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.617223e217199978\2021-10-20_6.png) 

![2021-10-20_7](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.617223ec1719be46\2021-10-20_7.png) 

![2021-10-20_8](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.61722413171a5844\2021-10-20_8.png) 

![2021-10-20_9](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.61722424171a9a5d\2021-10-20_9.png) 

![2021-10-20_10](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.61722431171acde1\2021-10-20_10.png) 

![2021-10-20_11](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.6172243e171aff70\2021-10-20_11.png) 

![2021-10-20_12](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.6172244b171b3258\2021-10-20_12.png) 

![2021-10-20_13](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.61722466171b9a49\2021-10-20_13.png) 

![2021-10-20_14](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.61722472171bcaee\2021-10-20_14.png) 

![2021-10-20_15](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.6172247a171be982\2021-10-20_15.png) 

![2021-10-20_16](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.61722489171c2311\2021-10-20_16.png) 





4. setup nginx pada ubuntu_landing untuk domain http://lxc_landing.dev , buat halaman index.html yang menerangkan informasi nama lxc

![2021-10-20_17](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.617224b4171ccaf9\2021-10-20_17.png) 

![2021-10-20_18](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.617224c2171d0265\2021-10-20_18.png) 

![2021-10-20_19](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.617224cb171d25ea\2021-10-20_19.png) 

![2021-10-20_20](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.617224d3171d4682\2021-10-20_20.png) 

![2021-10-20_21](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.617224db171d6390\2021-10-20_21.png) 

![2021-10-20_22](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.617224e4171d85ec\2021-10-20_22.png) 

![2021-10-20_23](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.617224eb171da210\2021-10-20_23.png) 





5. LXC ubuntu_landing harus auto start ketika vm dinyalakan, hal ini digunakan untuk menjaga agar website company profile tidak mengalami *downtime*

![2021-10-20_24](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.6172251d171e664a\2021-10-20_24.png) 

![2021-10-20_25](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.61722526171e875f\2021-10-20_25.png) 





6. setup nginx pada vm.local untuk mengatur *proxy_pass* dimana :

- mengakses [http://vm.local](http://vm.local/) akan diarahkan ke http://lxc_landing.dev
- mengakses http://vm.local/blog akan diarahkan ke http://lxc_php7.dev
- mengakses http://vm.local/app akan diartahkan ke http://lxc_php5.dev

![2021-10-20_26](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.6172255c171f5be5\2021-10-20_26.png) 

![2021-10-20_26_1](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.61722579171fcc71\2021-10-20_26_1.png) 

![2021-10-20_27](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.61722582171fef4b\2021-10-20_27.png) 

![2021-10-20_28](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.6172258a17200ed9\2021-10-20_28.png) 

![2021-10-20_28_1](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.6172259117202ce1\2021-10-20_28_1.png) 

Dan akan mendapatkan tampilan seperti ini : 

![2021-10-21](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.6172259a17205028\2021-10-21.png) 

![2021-10-21_1](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.617225c01720e0ef\2021-10-21_1.png) 

![2021-10-21_2](C:\Users\CATHAR~1\AppData\Local\Temp\BNZ.617225ca17210a8f\2021-10-21_2.png) 

Analisa :

* Mengapa untuk kebutuhan php5.6 tidak bisa menggunakan ubuntu 16.04, sehingga perlu diganti os ke debian 9? 

  Karena, Ubuntu 16.04 telah beralih ke PHP 7.0 dengan infrastruktur baru untuk paket PHP. Jadi, tidak, Anda tidak dapat menginstal php5 di Ubuntu 16.04, 

* Kenapa harus menggunakan virtualisasi LXC pada skema website yang akan didevelop?

  Karena, Linux Containers (LXC) adalah teknologi virtualisasi ringan dan menyediakan sistem virtualisasi perangkat lunak gratis untuk komputer yang menjalankan GNU/Linux. Hal ini dicapai melalui isolasi level kernel, memungkinkan seseorang untuk menjalankan beberapa unit virtual (wadah) secara bersamaan pada Host yang sama.

* Apa yang dimaksud dengan proxy server? kenapa vm.local bisa kita anggap sebagai proxy server?

  Proxy server menurut kami adalah sistem yang mengendalikan suatu lalu lintas data contohnya website agar kemananan dan privasi pengguna internet tersebut tetap bisa terjaga 