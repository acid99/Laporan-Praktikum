# **Modul 4 Practicum Report**

### By : Rasyid Sabilillah  &  Catharina Prisca

* First, make 2 copies of containers, and then start

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_1.png?raw=true">
</p>





* Next, open ubuntu_php7.4_2 and change the IP address to 10.0.3.111/24. Do the same thing on ubuntu_php7.4_3, change the IP address to 10.0.3.121

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_2.png?raw=true">
  </p>



* Go to lxc_php7_2.dev and change the server name

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_3.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_4.png?raw=true">
</p>



* Restart nginx and curl it. 

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_5.png?raw=true">
  </p>



* Next step is ubuntu_php7.4_3 (IP 10.0.3.121), debian_php5.6_2 (IP 10.0.3.112), debian_php5.6_3 (IP 10.0.3.122) the same as ubuntu_php7.4_2.
*  Add name server /etc/hosts (on VM)

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_6.png?raw=true">
</p>

* Run the jmeter, and change the number of threads

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_7.png?raw=true">
  </p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_8.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_9.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_10.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_11.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_12.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_13.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_14.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_15.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_16.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_17.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_18.png?raw=true">
</p>



* Go back to the VM and write the script as below to add upstream landing, php5,and php7


```markdown
/etc/nginx/sites-available/vm.local
```

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_19.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_20.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_21.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_22.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_23.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_24.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_25.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_26.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_27.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_28.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_29.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_30.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_31.png?raw=true">
</p>

<p align="center">
      	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_32.png?raw=true">
</p>



### Analysis

* When there is 50 users that access our web, if we don't use load balancer the average time of user accessing our web is :

  ​	a) Landing : 2284

  ​	b) Blog : 3438

  ​	c) App : 15

* When we use load balancer, then :

  ​	a) Landing : 3605

  ​	b) Blog : 4104

  ​	c) App : 15

  

  *From that data then we can find out the average user accessing our web. If we don't use a load balancer, then the number of users who access our web is:*

  

  - When there is 50 users that access our web, if we don't use load balancer the amount of user accessing our web is :

    ​	a) Landing : 3219

    ​	b) Blog : 3522

    ​	c) App : 15

    

  - When we use load balancer, then :

    ​	a) Landing : 2583

    ​	b) Blog : 2753

    ​	c) App : 28



Berdasarkan dengan data yang diperoleh, maka kita dapat mengetahui bahwa waktu rata-rata jumlah pengguna yang mengakses web kita adalah 1 detik lebih cepat dengan menggunakan penyeimbang beban.