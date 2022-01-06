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



* Restart nginx and curl it. Repeat for ubuntu_php7.4_3

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak4/2022-01-05_5.png?raw=true">
  </p>

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

