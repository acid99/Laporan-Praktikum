# **Final Project Report**

### By : Rasyid Sabilillah  &  Catharina Prisca (Kelompok 08)

* First make lxc settings manual IP and SSH, dont forget to on autosatart

  LXC_LARAVEL, LXC_WORDPRESS, LXC_YII with ubuntu focal php7.4

  LXC_DB_SERVER, LXC_CI with debian buster php5.6

  ```
  hint : 
  sudo lxc-create -n LXC_LARAVEL -t download -- --dist ubuntu --release focal --arch amd64 --force-cache --no-validate --server images.linuxcontainers.org
  
  sudo lxc-create -n LXC_DB_SERVER -t download -- --dist debian --release buster --arch amd64 --force-cache --no-validate --server images.linuxcontainers.org
  ```

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/2022-01-30_17.png?raw=true">
  </p>

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/2022-01-30_18.png?raw=true">
  </p>

- Install nginx on VM and settings with load balancer. Configure sub domain news.kelompok08.fpsas like https://github.com/aldonesia/Sistem-Administrasi-Server-2021/blob/master/modul-2/silabus.md

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/2022-01-30_15.png?raw=true">
  </p>

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/2022-01-30_16.png?raw=true">
  </p>


* Install mariadb on LXC_DB_SERVER and  CodeIgniter 3 on LXC_CI with ansible

  https://github.com/acid99/Sistem-Administrasi-Server/tree/main/assets/uas/ansible/db_server

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/2022-01-30.png?raw=true">
  </p>

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/2022-01-30_12.png?raw=true">
  </p>

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/2022-01-30_1.png?raw=true">
  </p>

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/2022-01-30_7.png?raw=true">
  </p>

- Install laravel 8 on LXC_LARAVEL with ansible

  https://github.com/acid99/Sistem-Administrasi-Server/tree/main/assets/uas/ansible/laravel

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/2022-01-30_2.png?raw=true">
  </p>

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/2022-01-30_3.png?raw=true">
  </p>

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/2022-01-30_4.png?raw=true">
  </p>

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/2022-01-30_6.png?raw=true">
  </p>

- Install latest wordpress on LXC_WORDPRESS with ansible

  https://github.com/acid99/Sistem-Administrasi-Server/tree/main/assets/uas/ansible/wordpress

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/2022-01-30_5.png?raw=true">
  </p>

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/2022-01-30_8.png?raw=true">
  </p>

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/2022-01-30_9.png?raw=true">
  </p>

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/2022-01-30_10.png?raw=true">
  </p>

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/2022-01-30_11.png?raw=true">
  </p>

- Install YII 2.0 on LXC_YII with ansible

  https://github.com/acid99/Sistem-Administrasi-Server/tree/main/assets/uas/ansible/yii

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/2022-01-30_13_1.png?raw=true">
  </p>

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/2022-01-30_13.png?raw=true">
  </p>

- Copy LXC earlier on steps 1, like architecture like https://github.com/acid99/Sistem-Administrasi-Server/blob/main/LaPrak4_Sysadm_RasyidPrisca.md

  <p align="center">
        	<img src= "https://github.com/aldonesia/Sistem-Administrasi-Server-2021/blob/master/Final%20Project/assets/arsitektur.png?raw=true">
  </p>

- Jmeter on 50 users

  - Graph

    <p align="center">
          	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/graph50.png?raw=true">
    </p>

  - Results

    <p align="center">
          	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/result50.png?raw=true">
    </p>

  - Report

    <p align="center">
          	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/report50.png?raw=true">
    </p>

- Jmeter on 150 users

  - Graph

    <p align="center">
          	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/graph150.png?raw=true">
    </p>

  - Results

    <p align="center">
          	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/resut150.png?raw=true">
    </p>

  - Report

    <p align="center">
          	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/report150.png?raw=true">
    </p>

  

- Jmeter on 300 users

  - Graph

    <p align="center">
          	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/graph300.png?raw=true">
    </p>

  - Results

    <p align="center">
          	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/result300.png?raw=true">
    </p>

  - Report

    <p align="center">
          	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/report300.png?raw=true">
    </p>

  

- Jmeter on 500 users

  - Graph

    <p align="center">
          	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/graph500.png?raw=true">
    </p>

  - Results

    <p align="center">
          	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/result500.png?raw=true">
    </p>

  - Report

    <p align="center">
          	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/uas/report500.png?raw=true">
    </p>



### Analysis Architectural Performance

1. Averages troughput
   - 50 users 4,97/sec
   - 150 users 4,9/sec
   - 300 users 4,9/sec
   - 500 users 6,57/sec

2. Averages users 
   - 50 users 1425/sec
   - 150 users 4353/sec
   - 300 users 8633/sec
   - 500 users 8527/sec

3. With methods load balancer with IP hash. Load balancer is the biggest factor in influencing performance, and load from LXC itself.