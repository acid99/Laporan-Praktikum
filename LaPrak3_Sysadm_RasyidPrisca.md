# **Module 3 Practicum Report**

## **By : Rasyid Sabilillah & Catharina Prisca**



### **Study Case**

Create SubDomain dev.vm.local with rules :

* Ansible
* Same lxc like vm.local
* The folder must be in var/www/html/dev{name_app}



### **Problem Solving**

* The first step is to go to the directory using ansible

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak3/2021-12-15.png?raw=true">
  </p>
  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak3/2021-12-15_1.png?raw=true">
  </p>

  ```
  ---
  - hosts: all
    become : yes
    tasks:
      - name: install bind9 dan dnsutils
        apt:
         pkg:
           - bind9
           - dnsutils
  ```

* The next step is install packages with ansible

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak3/2021-12-15_2.png?raw=true">
  </p>


* Create e config.yml file

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak3/2021-12-15_3.png?raw=true">
  </p>

  ```
  ---
  - hosts: all
    become : yes
    tasks:
     - name: membuat direktori
       file:
        path: /var/www/html/dev/landing
        state: directory
     - name: copy file vm.local
       copy:
        src: /etc/bind/vm/vm.local
        dest: /var/www/html/dev/landing
     - name: mengganti konfigurasi
       replace:
        path: /var/www/html/dev/landing/vm.local
        regexp: 'www'
        replace: 'dev'
     - name: copy file named.conf.local
       copy:
        src: /etc/bind/named.conf.local
        dest: /etc/bind/named.conf.local
     - name: mengganti konfigurasi conf local
       replace:
        path: /etc/bind/named.conf.local
        regexp: '/etc/bind/vm/vm.local'
        replace: '/var/www/html/dev/landing/vm.local'
     - name: mengganti konfigurasi conf local part2
       replace:
        path: /etc/bind/named.conf.local
        regexp: '/etc/bind/vm/115.168.192.in-addr.arpa'
        replace: '/var/www/html/dev/landing/115.168.192.in-addr.arpa'
     - name: copy file 115.168.192.in-addr.arpa
       copy:
        src: /etc/bind/vm/115.168.192.in-addr.arpa
        dest: /var/www/html/dev/landing
     - name: copy file resolv.conf
       copy:
        src: /etc/resolv.conf
        dest: /etc/resolv.conf
     - name: copy file named.conf.options
       copy:
        src: /etc/bind/named.conf.options
        dest: /etc/bind/named.conf.options
     - name: restart nginx
       service:
        name: nginx
        state: restarted
     - name: restart bind9
       action: service name=bind9 state=restarted
  ```

* Do the installation using the script below

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak3/2021-12-15_4(fix).png?raw=true">
  </p>
  
* Add subdomain to /etc/hosts

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak3/2021-12-15_5.png?raw=true">
  </p>

* Open vm.local file

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak3/2021-12-15_6.png?raw=true">
  </p>

* Add line www. After that exit lxc

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak3/2021-12-15_7.png?raw=true">
  </p>

* Open and edit vm.local in directory /etc/nginx/sites-enabled/

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak3/2021-12-15_9.png?raw=true">
  </p>

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak3/2021-12-15_10.png?raw=true">
  </p>
  
* Open and edit vm.local in directory /etc/bind/vm/

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak3/2021-12-16.png?raw=true">
  </p>

* Restart all packages

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak3/2021-12-16_1.png?raw=true">
  </p>

- Open Wifi Settings (in the case we use linux os), add dns server and uncheck automatic at menu Ipv4

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak3/2021-12-16_3.png?raw=true">
  </p>

- At menu IPv6, check disabled (we must turn off the IPv6), and then click apply

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak3/2021-12-16_4.png?raw=true">
  </p>

- Just reconnecting the wifi, and check dev.vm.local on the browser :)

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak3/2021-12-16_2.png?raw=true">
  </p>