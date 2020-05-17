# Install MS SQL Server on Ubuntu 20.04/18.04/16.04 LTS
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
#### ```sudo add-apt-repository "$(wget -qO- https://packages.microsoft.com/config/ubuntu/20.04/mssql-server-2019.list)"```
#### Untuk Ubuntu 16. 04
#### ``` sudo add-apt-repository "$(wget -qO- https://packages.microsoft.com/config/ubuntu/16.04/mssql-server-2019.list)"```
## Langkah Keempat
#### Install MS SQL Server 2019 on Ubuntu 20.04/18.04/16.04 LTS
#### ``` sudo apt update ```
#### ``` sudo apt install mssql-server ```
#### Tekan tombol y untuk memulai instalasi Microsoft SQL Server 2019 pada Ubuntu 20.04 / 18.04 / 16.04.
``` ded packages: 
  libc-dbg libcc1-0 gdbserver
The following NEW packages will be installed:
  gawk gdb libbabeltrace1 libc++1 libc++1-10 libc++abi1-10 libdw1
  libmpfr6 libpython2-stdlib libpython2.7-minimal libpython2.7-stdlib
  libsasl2-modules libsasl2-modules-gssapi-mit libsigsegv2
  libsss-nss-idmap0 mssql-server python-is-python2 python2
  python2-minimal python2.7 python2.7-minimal
0 upgraded, 21 newly installed, 0 to remove and 9 not upgraded.
Need to get 235 MB of archives.
After this operation, 1,101 MB of additional disk space will be used.
Do you want to continue? [Y/n] y ```

### Outputnya seperti di bawah ini:
```
Unpacking mssql-server (15.0.4033.1-2) ...
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
