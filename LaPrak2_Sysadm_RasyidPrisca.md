

# **Praktikum Modul 2**

#### **By : Rasyid Sabilillah & Catharina Prisca**





1. 

   * Cek lxc dengan menggunakan 

   ```markdown
    lxc-ls -f
   ```

   * Hapus ubuntu landing dengan menggunakan  command seperti dibawah ini, dan buat ubuntu focal baru dengan lxc-create

   ```markdown
    lxc-destroy ubuntu_landing
   ```

   <p align="center">
         	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%201/2021-11-17.png?raw=true">
   </p>
   
   <p align="center">
         	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%201/2021-11-17_1.png?raw=true">
   </p>
   
   

​		

- Setelah membuat baru, gunakan command lxc-start untuk memulai ubuntu_landing dan gunakan command lxc-attach untuk membuka ubuntu_landing. Lalu gunakan install nano untuk mengedit config.

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%201/2021-11-17_2.png?raw=true">
  </p>			

- Atur IP ubuntu_landing

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%201/2021-11-17_3.png?raw=true">
  </p>			

  

  ```markdown
  sudo lxc-start -n ubuntu_landing
  sudo lxc-attach  -n ubuntu_landing
  nano /etc/netplan/10-lxc.yaml
  netplan apply
  
  ```

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%201/2021-11-17_4.png?raw=true">
  </p>			

  

  - atur autostart lxc, seperti dibawah ini :

    <p align="center">
          	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%201/2021-11-17_5.png?raw=true">
    </p>			

  

  

  - install ssh 

    <p align="center">
          	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%201/2021-11-17_5_1.png?raw=true">
    </p>			

    

    ```markdown
    PermitRootLogin yes
    RSAAuthentication yes
    service sshd restart
    
    ```

    <p align="center">
          	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%201/2021-11-17_5_2.png?raw=true">
    </p>			

    

  - cek ssh apakah sudah berjalan atau belum

    <p align="center">
          	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%201/2021-11-17_5_4.png?raw=true">
    </p>			





2. 

   - Cek lxc dengan menggunakan 

   ```markdown
    lxc-ls -f
   ```

   * Hapus ubuntu landing dengan menggunakan  command seperti dibawah ini, dan buat ubuntu_php7.4 baru dengan menggunakan command lxc-create

   ```markdown
    lxc-destroy ubuntu_php7.4
   ```

   <p align="center">
         	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%202/2021-11-17_6.png?raw=true">
   </p>			

   <p align="center">
         	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%202/2021-11-17_7.png?raw=true">
   </p>		

   

   - Setelah membuat baru, gunakan command lxc-start untuk memulai ubuntu_7.4 dan gunakan command lxc-attach untuk membuka ubuntu_7.4. Lalu gunakan install nano untuk mengedit config.

     <p align="center">
           	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%202/2021-11-17_8.png?raw=true">
     </p>		

     
   
   - Atur IP ubuntu_php7.4
   
     <p align="center">
           	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%202/2021-11-17_9.png?raw=true">
     </p>		

     Dengan Menggunakan

     ```markdown
     sudo lxc-start -n ubuntu_php7.4
     sudo lxc-attach  -n ubuntu_php7.4
     nano /etc/netplan/10-lxc.yaml
     netplan apply
     
     ```

     <p align="center">
           	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%202/2021-11-17_10.png?raw=true">
     </p>		

     
   
   - Hentikan ubuntu_php7.4 dengan menggunakan command

     ```markdown
     lxc-stop ubuntu_php7.4
     ```

     <p align="center">
           	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%202/2021-11-17_11.png?raw=true">
     </p>		
     
     

   - Cek lxc dengan menggunakan 

   ```markdown
    lxc-ls -f
   ```
   
   <p align="center">
         	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%202/2021-11-17_12.png?raw=true">
   </p>		
   
   
   
   - install ssh
   
     <p align="center">
           	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%202/2021-11-17_13.png?raw=true">
     </p>		
   
     
   
   - Atur password baru
   
     <p align="center">
           	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%202/2021-11-17_14.png?raw=true">
     </p>
     
   
   - cek ssh apakah sudah berjalan atau belum
   
     <p align="center">
           	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%202/2021-11-17_15.png?raw=true">
     </p>		
     
     






3. vm.local/

- Langkah pertama yang harus dilakukan yakni menginstall laravel  menggunakan ansible. Setelah menginstall, masuk ke ansible tersebut dan buatlah folder laravel

  <p align="center">
        	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%203/2021-11-30_2.png?raw=true">
  </p>		

  

- Selanjutnya, buat host untuk lxc yang nanti akan di otomasi

  <p align="center">        <img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%203/2021-11-30_3.png?raw=true"></p>   

   

  ```markdown
  [landing]
  ubuntu_landing ansible_host=lxc_landing.dev ansible_ssh_user=root ansible_become_pass=sepasi
  
  ```

  * Buatlah directory serta apapun yang akan digunakan untuk menjalankan folder php dan lakukan instalasi

    <p align="center">
          	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%203/2021-11-30_3_1.png?raw=true">
    
    

  ```
  ---
  - hosts: all
    become : yes
    tasks:
      - name: install nginx nginx extras
        apt:
         pkg:
           - nginx
           - nginx-extras
         state: latest
      - name: start nginx
        service:
         name: nginx
         state: started
      - name: menginstall tools
        apt:
         pkg:
           - curl
           - software-properties-common
           - unzip
         state: latest
      - name: "Repo PHP 7.4"
        apt_repository:
          repo="ppa:ondrej/php"
      - name: "Updating the repo"
        apt: update_cache=yes
      - name: Installation PHP 7.4
        apt: name=php7.4 state=present
      - name: install php untuk laravel
        apt:
         pkg:
            - php7.4-fpm
            - php7.4-mysql
            - php7.4-mbstring
            - php7.4-xml
            - php7.4-bcmath
            - php7.4-json
            - php7.4-zip
            - php7.4-common
         state: present
  ```

  

  - Jika instalasi telah selesai dilakukan, buat folder installcomposer.yml

    <p align="center">
          	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%203/2021-11-30_5.png?raw=true">
    </p>

    


  ```
  ---
   -hosts: all
    become : yes
    tasks:
     - name: Download and install Composer
       shell: curl -sS https://getcomposer.org/installer | php
       args:
        chdir: /usr/src/
        creates: /usr/local/bin/composer
        warn: false
     - name: Add Composer to global path
       copy:
        dest: /usr/local/bin/composer
        group: root
        mode: '0755'
        owner: root
        src: /usr/src/composer.phar
        remote_src: yes
     - name: Composer create project
       become_user: root
       composer:
        command: create-project
        arguments: laravel/laravel landing 
        working_dir: /var/www/html
        prefer_dist: yes
       environment:
          COMPOSER_NO_INTERACTION: "1"
     - name: mengkopi file .env.example jadi .env
       copy:
        dest: /var/www/html/landing/.env.example
        src: /var/www/html/landing/.env
        remote_src: yes
     - name: mengganti konfigurasi .env
       lineinfile:
        path: /var/www/html/landing/.env
        regexp: "{{ item.regexp }}"
        line: "{{ item.line }}"
        backrefs: yes
       loop:
        - { regexp: '^(.*)DB_HOST(.*)$', line: 'DB_HOST=10.0.3.200' }
        - { regexp: '^(.*)DB_DATABASE(.*)$', line: 'DB_DATABASE=landing' }
        - { regexp: '^(.*)DB_USERNAME(.*)$', line: 'DB_USERNAME=admin' }
        - { regexp: '^(.*)DB_PASSWORD(.*)$', line: 'DB_PASSWORD= ' }
        - { regexp: '^(.*)APP_URL(.*)$', line: 'APP_URL=http://vm.local' }
        - { regexp: '^(.*)APP_NAME=(.*)$', line: 'APP_NAME=landing' }
     - name: Composer install ke landing
       composer:
         command: install
         working_dir: /var/www/html/landing
       environment:
         COMPOSER_NO_INTERACTION: "1"
     - name: generate php artisan
       args:
        chdir: /var/www/html/landing
       shell: php artisan key:generate
     - name: mengganti permission storage
       file:
        path: /var/www/html/landing/storage
        mode: 0777
        recurse: yes
  
  ```

  

  

  - Lakukan instalasi kembali

    <p align="center">
          	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%203/2021-11-30_6.png?raw=true">
    </p>

  - Buatlah file lxc_landing.dev

    <p align="center">
          	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%203/2021-11-30_6_1.png?raw=true">
    </p>

    ```
    server {
            listen 80;
    
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

    

  - Buatlah file config.yml

    <p align="center">        <img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%203/2021-11-30_7.png?raw=true"></p>

    

    ```
    ---
    - hosts: all
      become : yes
      vars:
        domain: 'lxc_landing.dev'
      tasks:
       - name: stop apache2
         service:
          name: apache2
          state: stopped
          enabled: no
       - name: Write {{ domain }} to /etc/hosts
         lineinfile:
          dest: /etc/hosts
          regexp: '.*{{ domain }}$'
          line: "127.0.0.1 {{ domain }}"
          state: present
       - name: ensure nginx is at the latest version
         apt: name=nginx state=latest
       - name: start nginx
         service:
          name: nginx
          state: started
       - name: copy the nginx config file 
         copy:
          src: ~/ansible/laravel/lxc_landing.dev
          dest: /etc/nginx/sites-available/lxc_landing.dev
       - name: Symlink lxc_landing.dev
         command: ln -sfn /etc/nginx/sites-available/lxc_landing.dev /etc/nginx/sites-enabled/lxc_landing.dev
         args:
          warn: false
       - name: restart nginx
         service:
          name: nginx
          state: restarted
       - name: restart php7
         service:
          name: php7.4-fpm
          state: restarted
       - name: curl web
         command: curl -i http://lxc_landing.dev
         args:
          warn: false
    ```

    

  - Lakukan instalasi

    <p align="center">        <img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%203/2021-11-30_8.png?raw=true"></p>

    

    

  - Cek dengan cara membuka vm.local. Jika sukses, maka tampilannya akan seperti berikut ini :

    <p align="center">        <img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%203/2021-11-30_9.png?raw=true"></p>
    
    



4. vm.local/blog

   - Seperti pada nomor sebelumnya, langkah pertama dimulai dengan masuk pada folder ansible

     <p align="center">
           	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%204/2021-12-01.png?raw=true">
     </p>

     

   - Buat host untuk lxc yang nanti akan di otomasi

     <p align="center">
           	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%204/2021-12-01_1.png?raw=true">
     </p>

   ```
   [blog]
   ubuntu_php7.4 ansible_host=lxc_php7.dev ansible_ssh_user=root ansible_become_pass=sepasi
   ```
   
   
   
   - Buat direktori untuk tasks,templates dan handlers di folder wordpress. Lalu, masuk ke dalam folder tasks untuk menginstall paket
   
     <p align="center">
           	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%204/2021-12-01_2.png?raw=true">
     </p>
   
   ```
   ---
   - hosts: all
     vars:
       domain: 'lxc_php7.dev'
     tasks:
      - name: delete apt chache
        become: yes
        become_user: root
        become_method: su
        command: rm -vf /var/lib/apt/lists/*
   
      - name: install requirement
        become: yes
        become_user: root
        become_method: su
        apt: name={{ item }} state=latest update_cache=true
        with_items:
         - nginx
         - nginx-extras
         - curl
         - wget
         - php7.4
         - php7.4-fpm
         - php7.4-curl
         - php7.4-xml
         - php7.4-gd
         - php7.4-opcache
         - php7.4-mbstring
         - php7.4-zip
         - php7.4-json
         - php7.4-cli
         - php7.4-mysqlnd
         - php7.4-xmlrpc
         - php7.4-curl
   
      - name: wget wordpress
        shell: wget -c http://wordpress.org/latest.tar.gz
   
      - name: tar latest.tar.gz
        shell: tar -xvzf latest.tar.gz
   
      - name: copy folder wordpress
        shell: cp -R wordpress /var/www/html/blog
   
      - name: chmod
        become: yes
        become_user: root
        become_method: su
        command: chmod 775 -R /var/www/html/blog/
   
      - name: copy .wp-config.conf
        copy:
         src=~/ansible/wordpress/wp.conf
         dest=/var/www/html/blog/wp-config.php
   
      - name: copy wordpress.conf
        copy:
         src=~/ansible/wordpress/wordpress.conf
         dest=/etc/nginx/sites-available/{{ domain }}
        vars:
         servername: '{{ domain }}'
   
      - name: Symlink wordpress.conf
        command: ln -sfn /etc/nginx/sites-available/{{ domain }} /etc/nginx/sites-enabled/{{ domain }}
      
      - name: restart nginx
        become: yes
        become_user: root
        become_method: su
        action: service name=nginx state=restarted
   
      - name: Write {{ domain }} to /etc/hosts
        lineinfile:
         dest: /etc/hosts
         regexp: '.*{{ domain }}$'
         line: "127.0.0.1 {{ domain }}"
         state: present
   
      - name: enable module php mbstring
        command: phpenmod mbstring
   
      - name: restart php
        become: yes
        become_user: root
        become_method: su
        action: service name=php7.4-fpm state=restarted
   
      - name: restart nginx
        become: yes
        become_user: root
        become_method: su
        action: service name=nginx state=restarted
   ```
   
   
   
   - Kemudian, masuk ke dalam templates wp.conf yang merupakan tempat configuration pada wordpress
   
     <p align="center">
           	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%204/2021-12-01_2_1.png?raw=true">
     </p>
   
      
   
     ```
     <?php
     /**
      * The base configuration for WordPress
      *
      * The wp-config.php creation script uses this file during the installation.
      * You don't have to use the web site, you can copy this file to "wp-config.php"
      * and fill in the values.
      *
      * This file contains the following configurations:
      *
      * * MySQL settings
      * * Secret keys
      * * Database table prefix
      * * ABSPATH
      *
      * @link https://wordpress.org/support/article/editing-wp-config-php/
      *
      * @package WordPress
      */
     
     define( 'WP_HOME', 'http://vm.local/blog' );
     define( 'WP_SITEURL', 'http://vm.local/blog' );
     
     // ** MySQL settings - You can get this info from your web host ** //
     /** The name of the database for WordPress */
     define( 'DB_NAME', 'blog' );
     
     /** MySQL database username */
     define( 'DB_USER', 'admin' );
     
     /** MySQL database password */
     define( 'DB_PASSWORD', 'SysAdminSas0102' );
     
     /** MySQL hostname */
     define( 'DB_HOST', '10.0.3.200:3306' );
     
     /** Database charset to use in creating database tables. */
     define( 'DB_CHARSET', 'utf8' );
     
     /** The database collate type. Don't change this if in doubt. */
     define( 'DB_COLLATE', '' );
     
     /**#@+
      * Authentication unique keys and salts.
      *
      * Change these to different unique phrases! You can generate these using
      * the {@link https://api.wordpress.org/secret-key/1.1/salt/ WordPress.org secret-key service}.
      *
      * You can change these at any point in time to invalidate all existing cookies.
      * This will force all users to have to log in again.
      *
      * @since 2.6.0
      */
     define( 'AUTH_KEY',         'put your unique phrase here' );
     define( 'SECURE_AUTH_KEY',  'put your unique phrase here' );
     define( 'LOGGED_IN_KEY',    'put your unique phrase here' );
     define( 'NONCE_KEY',        'put your unique phrase here' );
     define( 'AUTH_SALT',        'put your unique phrase here' );
     define( 'SECURE_AUTH_SALT', 'put your unique phrase here' );
     define( 'LOGGED_IN_SALT',   'put your unique phrase here' );
     define( 'NONCE_SALT',       'put your unique phrase here' );
     
     /**#@-*/
     
     /**
      * WordPress database table prefix.
      *
      * You can have multiple installations in one database if you give each
      * a unique prefix. Only numbers, letters, and underscores please!
      */
     $table_prefix = 'wp_';
     
     /**
      * For developers: WordPress debugging mode.
      *
      * Change this to true to enable the display of notices during development.
      * It is strongly recommended that plugin and theme developers use WP_DEBUG
      * in their development environments.
      *
      * For information on other constants that can be used for debugging,
      * visit the documentation.
      *
      * @link https://wordpress.org/support/article/debugging-in-wordpress/
      */
     define( 'WP_DEBUG', false );
     
     /* Add any custom values between this line and the "stop editing" line. */
     
     
     
     /* That's all, stop editing! Happy publishing. */
     
     /** Absolute path to the WordPress directory. */
     if ( ! defined( 'ABSPATH' ) ) {
             define( 'ABSPATH', __DIR__ . '/' );
     }
     
     /** Sets up WordPress vars and included files. */
     require_once ABSPATH . 'wp-settings.php';
     
     ```
   
     
   
   - Masuk ke dalam templates wordpress.conf
   
     <p align="center">
           	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%204/2021-12-01_3.png?raw=true">
     </p>
   
     ```
     server {
          listen 80;
          listen [::]:80;
     
          # Log files for Debugging
          access_log /var/log/nginx/wordpress-access.log;
          error_log /var/log/nginx/wordpress-error.log;
     
          # Webroot Directory for Laravel project
          root /var/www/html/blog;
          index index.php index.html index.htm;
     
          # Your  Name
          server_name lxc_php7.dev;
     
          location / {
                  try_files $uri $uri/ /index.php?$query_string;
          }
     
          # PHP-FPM Configuration Nginx
          location ~ \.php$ {
                  try_files $uri =404;
                  fastcgi_split_path_info ^(.+\.php)(/.+)$;
                  fastcgi_pass unix:/run/php/php7.4-fpm.sock;
                  fastcgi_index index.php;
                  fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
                  include fastcgi_params;
          }
     }
     ```
   
     
   
     - Jalankan ansible kembali untuk menginstall
   
       <p align="center">
             	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%204/2021-12-01_4.png?raw=true">
       </p>
   
     
   
   - Buka vm.local/blog/ untuk melakukan checking apakah wordpressnya sudah dapat dijalankan atau belum. Jika sudah dapat dijalankan, maka tampilannya akan berubah menjadi berikut :
   
     <p align="center">
           	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%204/2021-12-01_5.png?raw=true">
     </p>
   
     <p align="center">
           	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%204/2021-12-01_6.png?raw=true">
     </p>
     
     <p align="center">
           	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%204/2021-12-01_7.png?raw=true">
     </p>
     
     <p align="center">
           	<img src= "https://github.com/acid99/Sistem-Administrasi-Server/blob/main/assets/laprak2/no%204/2021-12-01_8.png?raw=true">
     </p>
     
     

