# **Modul 3 Practicum Report**

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





* The next step is re-install

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak3/2021-12-15_2.png?raw=true">
  </p>

note : dikasih script sublaravel!

```markdown
    root /var/www/html/landing/public;
    index index.php index.html index.htm;
    server_name lxc_landing.dev;

    error_log /var/log/nginx/landing_error.log;
    access_log /var/log/nginx/landing_access.log;

    client_max_body_size 100M;
    location / {
            try_files $uri $uri/ /index.php$args;
    }
    location ~\.php$ {
            include snippets/fastcgi-php.conf;
            fastcgi_pass unix:run/php/php7.4-fpm.sock;
            fastcgi_param SCRIPTFILENAME $document_root$fastcgi_script_name;
    }
}
```


* Create e config.yml file

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak3/2021-12-15_3.png?raw=true">
  </p>



* Do the installation using the script below

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak3/2021-12-15_4(fix).png?raw=true">
  </p>

  

Note : kasih script config.yml!



* Add subdomain to /etc/hosts

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak3/2021-12-15_5.png?raw=true">
  </p>



* Open vm.local file

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak3/2021-12-15_6.png?raw=true">
  </p>



* Add line www

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak3/2021-12-15_7.png?raw=true">
  </p>



* The last step is exit

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak3/2021-12-15_8.png?raw=true">
  </p>

  