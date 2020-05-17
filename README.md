# Install / Uninstall MS SQL Server on Ubuntu 20.04/18.04/16.04 LTS
## System Requirements
#### 1. Minimum memory of 2 GB
#### 2. Prosesor CPU dengan kecepatan minimum 1,4 GHz. Tetapi yang direkomendasikan adalah> = 2 GHz
#### 3. SQL Server requires a minimum of 10 GB of available hard-disk space
## Ikuti langkah-langkah di bawah ini untuk menginstal dan mengkonfigurasi server database MS SQL di Ubuntu 20.04 / 18.04 / 16.04:
## Langkah Pertama
#### ```sudo apt-get update```
#### ```sudo apt-get -y upgrade [optional]```
## Langkah Kedua
#### Tambahkan kunci GPG untuk sistem untuk mempercayai paket repositori MS SQL apt:
#### ```sudo wget -qO- https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -```
## Langkah Ketiga
#### Langkah 3: Tambahkan repositori Ubuntu Microsoft SQL Server 2019:
#### Tambahkan repositori APT Microsoft SQL Server 2019 ke sistem Ubuntu 20.04 / 18.04 / 16.04 Anda.
#### Untuk Ubuntu 18.04 /Ubuntu 20.04
#### ```sudo add-apt-repository "$(wget -qO- https://packages.microsoft.com/config/ubuntu/18.04/mssql-server-2019.list)"```
#### Untuk Ubuntu 16. 04
#### ``` sudo add-apt-repository "$(wget -qO- https://packages.microsoft.com/config/ubuntu/16.04/mssql-server-2019.list)"```
## Langkah Keempat
#### Install MS SQL Server 2019 on Ubuntu 20.04/18.04/16.04 LTS
#### ``` sudo apt update ```
#### ``` sudo apt install mssql-server ```
#### Tekan tombol y untuk memulai instalasi Microsoft SQL Server 2019 pada Ubuntu 20.04 / 18.04 / 16.04.
``` ded packages: libc-dbg libcc1-0 gdbserver 
The following NEW packages will be installed:
gawk gdb libbabeltrace1 libc++1 libc++1-10 libc++abi1-10 libdw1
libmpfr6 libpython2-stdlib libpython2.7-minimal libpython2.7-stdlib
libsasl2-modules libsasl2-modules-gssapi-mit libsigsegv2
libsss-nss-idmap0 mssql-server python-is-python2 python2
python2-minimal python2.7 python2.7-minimal
0 upgraded, 21 newly installed, 0 to remove and 9 not upgraded
Need to get 235 MB of archives
After this operation, 1,101 MB of additional disk space will be used
Do you want to continue? [Y/n] y
```
### Outputnya seperti di bawah ini:
#### 
``` Unpacking mssql-server (15.0.4033.1-2) ...
Setting up libdw1:amd64 (0.176-1.1build1) ...
Setting up gawk (1:5.0.1+dfsg-1) ...
Setting up libsasl2-modules:amd64 (2.1.27+dfsg-2) ...
Setting up libpython2.7-stdlib:amd64 (2.7.18~rc1-2) ...
Setting up libbabeltrace1:amd64 (1.5.8-1build1) ...
Setting up libc++abi1-10:amd64 (1:10.0.0-4ubuntu1) ...
Setting up libsss-nss-idmap0 (2.2.3-3) ...
Setting up libsasl2-modules-gssapi-mit:amd64 (2.1.27+dfsg-2) ...
Setting up libc++1-10:amd64 (1:10.0.0-4ubuntu1) ...
Setting up python2.7 (2.7.18~rc1-2) ...
Setting up libpython2-stdlib:amd64 (2.7.17-2ubuntu4) ...
Setting up python2 (2.7.17-2ubuntu4) ...
Setting up gdb (9.1-0ubuntu1) ...
Setting up python-is-python2 (2.7.17-4) ...
Setting up libc++1:amd64 (1:10.0-50~exp1) ...
Setting up mssql-server (15.0.4033.1-2) ...
debconf: unable to initialize frontend: Dialog
debconf: (Dialog frontend requires a screen at least 13 lines tall and 31 columns wide.)
debconf: falling back to frontend: Readline
debconf: unable to initialize frontend: Readline
debconf: (Can't locate Term/ReadLine.pm in @INC (you may need to install the Term::ReadLine module) (@INC contains: /etc/perl /usr/local/lib/x86_64-linux-gnu/perl/5.30.0 /usr/local/share/perl/5.30.0 /usr/lib/x86_64-linux-gnu/perl5/5.30 /usr/share/perl5 /usr/lib/x86_64-linux-gnu/perl/5.30 /usr/share/perl/5.30 /usr/local/lib/site_perl /usr/lib/x86_64-linux-gnu/perl-base) at /usr/share/perl5/Debconf/FrontEnd/Readline.pm line 7.)
debconf: falling back to frontend: Teletype
+--------------------------------------------------------------+
Please run 'sudo /opt/mssql/bin/mssql-conf setup'
to complete the setup of Microsoft SQL Server
+--------------------------------------------------------------+
Processing triggers for man-db (2.9.1-1) ...
Processing triggers for mime-support (3.64ubuntu1) ...
Processing triggers for libc-bin (2.31-0ubuntu9) ... 
```
### Langkah Kelima 
#### Ketika instalasi selesai, lanjutkan untuk mengatur kata sandi pengguna root dengan menjalankan pengaturan awal / opt / mssql / bin / mssql-conf setup
### ``` sudo /opt/mssql/bin/mssql-conf setup```
``` Choose an edition of SQL Server:
  1) Evaluation (free, no production use rights, 180-day limit)
  2) Developer (free, no production use rights)
  3) Express (free)
  4) Web (PAID)
  5) Standard (PAID)
  6) Enterprise (PAID)
  7) Enterprise Core (PAID)
  8) I bought a license through a retail sales channel and have a product key to enter.

Details about editions can be found at
https://go.microsoft.com/fwlink/?LinkId=852748&clcid=0x409

Use of PAID editions of this software requires separate licensing through a
Microsoft Volume Licensing program.
By choosing a PAID edition, you are verifying that you have the appropriate
number of licenses in place to install and run this software.

Enter your edition(1-8): 2
The license terms for this product can be found in
/usr/share/doc/mssql-server or downloaded from:
https://go.microsoft.com/fwlink/?LinkId=855862&clcid=0x409

The privacy statement can be viewed at:
https://go.microsoft.com/fwlink/?LinkId=853010&clcid=0x409

Do you accept the license terms? [Yes/No]:Yes

Enter the SQL Server system administrator password:  <SetStrongNewPassword>
Confirm the SQL Server system administrator password: <ConfirmStrongPassword>
Configuring SQL Server...

ForceFlush is enabled for this instance. 
ForceFlush feature is enabled for log durability.
Created symlink /etc/systemd/system/multi-user.target.wants/mssql-server.service → /lib/systemd/system/mssql-server.service.
Setup has completed successfully. SQL Server is now starting.
```
#### Untuk mengcek MS SQL sudah aktif atau belum.
#### 
```systemctl status mssql-server --no-pager 
● mssql-server.service - Microsoft SQL Server Database Engine
     Loaded: loaded (/lib/systemd/system/mssql-server.service; enabled; vendor preset: enabled)
     Active: active (running) since Tue 2020-05-05 21:08:00 CEST; 26s ago
       Docs: https://docs.microsoft.com/en-us/sql/linux
   Main PID: 3626 (sqlservr)
      Tasks: 135
     Memory: 592.1M
     CGroup: /system.slice/mssql-server.service
             ├─3626 /opt/mssql/bin/sqlservr
             └─3669 /opt/mssql/bin/sqlservr

May 05 21:08:05 ubuntu-4gb-hel1-1 sqlservr[3669]: [78B blob data]
May 05 21:08:05 ubuntu-4gb-hel1-1 sqlservr[3669]: [84B blob data]
May 05 21:08:05 ubuntu-4gb-hel1-1 sqlservr[3669]: [145B blob data]
May 05 21:08:05 ubuntu-4gb-hel1-1 sqlservr[3669]: [96B blob data]
May 05 21:08:05 ubuntu-4gb-hel1-1 sqlservr[3669]: [66B blob data]
May 05 21:08:06 ubuntu-4gb-hel1-1 sqlservr[3669]: [75B blob data]
May 05 21:08:06 ubuntu-4gb-hel1-1 sqlservr[3669]: [96B blob data]
May 05 21:08:06 ubuntu-4gb-hel1-1 sqlservr[3669]: [100B blob data]
May 05 21:08:06 ubuntu-4gb-hel1-1 sqlservr[3669]: [71B blob data]
May 05 21:08:06 ubuntu-4gb-hel1-1 sqlservr[3669]: [124B blob data]
```
###  Langkah Keenam 
#### Install MS SQL tools and unixODBC plugin
#### Untuk Ubuntu 20.04:
#### 
``` curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
curl https://packages.microsoft.com/config/ubuntu/19.10/prod.list > /etc/apt/sources.list.d/mssql-release.list
sudo apt update 
sudo ACCEPT_EULA=Y apt install mssql-tools unixodbc-dev 
```
#### Untuk Ubuntu 18.04
#### 
``` curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
curl https://packages.microsoft.com/config/ubuntu/18.04/prod.list | sudo tee /etc/apt/sources.list.d/msprod.list
sudo apt update 
sudo sudo ACCEPT_EULA=Y apt install mssql-tools unixodbc-dev 
```
#### Untuk Ubuntu 16.04
#### 
``` curl https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
curl https://packages.microsoft.com/config/ubuntu/16.04/prod.list | sudo tee /etc/apt/sources.list.d/msprod.list
sudo apt update 
sudo sudo ACCEPT_EULA=Y apt install mssql-tools unixodbc-dev
```
### Langkah Ketujuh
#### Konfigurasikan PATH untuk binari MS SQL
#### ``` echo 'export PATH="$PATH:/opt/mssql-tools/bin"' >> ~/.bash_profile ```
#### Untuk membuat sqlcmd / bcp dapat diakses dari bash shell untuk sesi interaktif / non-login, modifikasi PATH dalam file ~ / .bashrc dengan perintah berikut:
#### ``` echo 'export PATH="$PATH:/opt/mssql-tools/bin"' >> ~/.bashrc
#### source ~/.bashrc ```
#### Terhubung keconsole MS SQL:
#### ``` sqlcmd -S 127.0.0.1 -U SA 
Password: 
1> create database testDB; ```
### Selesai

# Untuk Uninstallnya
## ``` sudo apt-get remove mssql-sever ```
## ``` sudo system status mssql-server ```
# Untuk Menghapus folder MssQl
## Masuk sebagai root
## ``` sudo su ```
## ``` sudo rm -rf /var/opt/mssql ```
## Untuk mengecek folder MssQl sudah terhapus atau belum
## ```sudo ls -lrt /var/opt/mssql```
