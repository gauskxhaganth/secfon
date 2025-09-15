# Bab 1

## Memulai dengan GNU/Linux

### **Bagian 1.1: Perintah Manajemen Berkas**

Linux menggunakan beberapa konvensi untuk direktori saat ini dan direktori induk. Hal ini bisa sedikit membingungkan bagi pemula. Setiap kali Anda berada di terminal Linux, Anda akan berada di dalam apa yang disebut **direktori kerja saat ini** (*current working directory*). Sering kali, *command prompt* Anda akan menampilkan seluruh direktori kerja, atau hanya bagian terakhir dari direktori tersebut. *Prompt* Anda bisa terlihat seperti salah satu dari berikut ini:

```
user@host ~/somedir $
user@host somedir $
user@host /home/user/somedir $
```

Ini menunjukkan bahwa direktori kerja Anda saat ini adalah `/home/user/somedir`.

Di Linux, `..` mewakili direktori induk dan `.` mewakili direktori saat ini. Oleh karena itu, jika direktori saat ini adalah `/home/user/somedir`, maka perintah `cd ../somedir` tidak akan mengubah direktori kerja.

Tabel di bawah ini mencantumkan beberapa perintah manajemen berkas yang paling sering digunakan.

### **Navigasi Direktori**

| Perintah | Kegunaan |
| :--- | :--- |
| **`pwd`** | Mendapatkan *path* lengkap dari direktori kerja saat ini. |
| **`cd -`** | Menavigasi ke direktori terakhir tempat Anda bekerja. |
| **`cd ~`** atau hanya **`cd`** | Menavigasi ke direktori *home* pengguna saat ini. |
| **`cd ..`** | Pindah ke direktori induk dari direktori saat ini (perhatikan spasi antara `cd` dan `..`). |


### **Melihat Daftar Berkas di Dalam Direktori**

| Perintah | Kegunaan |
| :--- | :--- |
| **`ls -l`** | Menampilkan daftar berkas dan direktori di direktori saat ini dalam format panjang (tabel). (Disarankan untuk menggunakan `-l` dengan `ls` agar lebih mudah dibaca). |
| **`ls -ld nama-dir`** | Menampilkan informasi tentang direktori `nama-dir` itu sendiri, bukan isinya. |
| **`ls -a`** | Menampilkan semua berkas termasuk yang tersembunyi (*hidden files*). (Nama berkas yang diawali dengan `.` adalah berkas tersembunyi di Linux). |
| **`ls -F`** | Menambahkan simbol di akhir nama berkas untuk menunjukkan jenisnya (`*` berarti *executable*, `/` berarti direktori, `@` berarti *symbolic link*, `=` berarti *socket*, `|` berarti *named pipe*, `>` berarti *door*). |
| **`ls -lt`** | Menampilkan daftar berkas yang diurutkan berdasarkan waktu modifikasi terakhir, dengan berkas yang paling baru diubah muncul di bagian atas (ingat, opsi `-l` menyediakan format panjang yang lebih mudah dibaca). |
| **`ls -lh`** | Menampilkan ukuran berkas dalam format yang mudah dibaca manusia (*human readable*). |
| **`ls -lR`** | Menampilkan semua subdirektori secara rekursif. |
| **`tree`** | Akan menghasilkan representasi pohon (*tree*) dari sistem berkas, dimulai dari direktori saat ini. |


### **Membuat, Menyalin, dan Menghapus Berkas/Direktori**

| Perintah | Kegunaan |
| :--- | :--- |
| **`cp -p sumber tujuan`** | Akan menyalin berkas dari sumber ke tujuan. `-p` adalah singkatan dari *preservation*. Ini akan mempertahankan atribut asli berkas saat menyalin seperti pemilik berkas, *timestamp*, grup, izin, dll. |
| **`cp -R dir_sumber dir_tujuan`** | Akan menyalin direktori sumber ke tujuan yang ditentukan secara rekursif. |
| **`mv berkas1 berkas2`** | Di Linux, tidak ada perintah *rename* secara khusus. Oleh karena itu, `mv` memindahkan/mengganti nama `berkas1` menjadi `berkas2`. |
| **`rm -i namaberkas`** | Meminta konfirmasi Anda sebelum setiap penghapusan berkas. **JIKA ANDA PENGGUNA BARU COMMAND LINE LINUX, ANDA HARUS SELALU MENGGUNAKAN `rm -i`**. Anda dapat menentukan beberapa berkas sekaligus. |
| **`rm -R nama-dir`** | Akan menghapus direktori `nama-dir` secara rekursif. |
| **`rm -rf nama-dir`** | Akan menghapus direktori `dir` secara rekursif, mengabaikan berkas yang tidak ada, dan tidak akan pernah meminta konfirmasi apa pun. **HATI-HATI MENGGUNAKAN PERINTAH INI\!** Anda dapat menentukan beberapa direktori. |
| **`rmdir nama-dir`** | Akan menghapus direktori `nama-dir` jika kosong. Perintah ini hanya dapat menghapus direktori yang kosong. |
| **`mkdir nama-dir`** | Membuat direktori `nama-dir`. |
| **`mkdir -p nama-dir/nama-dir`** | Membuat hierarki direktori. Membuat direktori induk sesuai kebutuhan jika belum ada. Anda dapat menentukan beberapa direktori. |
| **`touch namaberkas`** | Membuat berkas `namaberkas` jika belum ada, jika sudah ada, maka akan mengubah *timestamp* berkas ke waktu saat ini. |


### **Izin dan Grup Berkas/Direktori**

| Perintah | Kegunaan |
| :--- | :--- |
| **`chmod <spesifikasi> namaberkas`** | Mengubah izin (*permission*) berkas. Spesifikasi = `u` (user), `g` (group), `o` (other), `+` (tambah izin), `-` (hapus izin), `r` (read), `w` (write), `x` (execute). |
| **`chmod -R <spesifikasi> nama-dir`** | Mengubah izin direktori secara rekursif. Untuk mengubah izin direktori dan semua yang ada di dalamnya, gunakan perintah ini. |
| **`chmod go=+r myfile`** | Menambahkan izin baca untuk pemilik (*owner*) dan grup (*group*). |
| **`chmod a+rwx myfile`** | Mengizinkan semua pengguna untuk membaca, menulis, atau mengeksekusi `myfile`. |
| **`chmod go-r myfile`** | Menghapus izin baca dari grup (*group*) dan lainnya (*others*). |
| **`chown pemilik1 namaberkas`** | Mengubah kepemilikan berkas ke pengguna `pemilik1`. |
| **`chgrp pemilik_grup namaberkas`** | Mengubah kepemilikan grup utama dari berkas `namaberkas` ke grup `pemilik_grup`. |
| **`chgrp -R pemilik_grup nama-dir`** | Mengubah kepemilikan grup utama dari direktori `nama-dir` ke grup `pemilik_grup` secara rekursif. Untuk mengubah kepemilikan grup direktori dan semua yang ada di dalamnya, gunakan perintah ini. |


## **Bagian 1.2: Hello World**

Ketik kode berikut ke terminal Anda, lalu tekan Enter:

```
echo "Hello World"
```

Ini akan menghasilkan keluaran sebagai berikut:

```
Hello World
```


## **Bagian 1.3: Utilitas Dasar Linux**

Linux memiliki perintah untuk hampir semua tugas dan sebagian besar di antaranya intuitif serta mudah diinterpretasikan.

### **Mendapatkan Bantuan di Linux**

| Perintah | Kegunaan |
| :--- | :--- |
| **`man <nama>`** | Membaca halaman manual (*manual page*) dari `<nama>`. |
| **`man <bagian> <nama>`** | Membaca halaman manual dari `<nama>`, yang terkait dengan bagian yang diberikan. |
| **`man -k <editor>`** | Menampilkan semua perangkat lunak yang halaman manualnya mengandung kata kunci `<editor>`. |
| **`man -K <katakunci>`** | Menampilkan semua halaman manual yang mengandung `<katakunci>` di dalamnya. |
| **`apropos <editor>`** | Menampilkan semua aplikasi yang deskripsi satu barisnya cocok dengan kata *editor*. Gunakan perintah ini saat tidak dapat mengingat nama aplikasi. |
| **`help`** | Di *Bash shell*, ini akan menampilkan daftar semua perintah *bash* yang tersedia. |
| **`help <nama>`** | Di *Bash shell*, ini akan menampilkan info tentang perintah *bash* `<nama>`. |
| **`info <nama>`** | Melihat semua informasi tentang `<nama>`. |
| **`dpkg -l`** | Menampilkan daftar semua paket yang terinstal pada sistem berbasis Debian. |
| **`dpkg -L namaPaket`** | Akan mendaftar berkas yang diinstal dan detail *path* untuk paket yang diberikan di Debian. |
| **`dpkg -l \| grep -i <edit>`** | Mengembalikan semua paket `.deb` yang terinstal dengan `<edit>` tanpa mempedulikan huruf besar/kecil. |
| **`less /var/lib/dpkg/available`** | Mengembalikan deskripsi semua paket yang tersedia. |
| **`whatis vim`** | Menampilkan deskripsi satu baris dari `vim`. |
| **`<nama-perintah> --help`** | Menampilkan informasi penggunaan tentang `<nama-alat>`. Terkadang `perintah -h` juga berfungsi, tetapi tidak untuk semua perintah. |


### **Identifikasi Pengguna dan Siapa Saja di Dunia Linux**

| Perintah | Kegunaan |
| :--- | :--- |
| **`hostname`** | Menampilkan nama *host* dari sistem. |
| **`hostname -f`** | Menampilkan *Fully Qualified Domain Name* (FQDN) dari sistem. |
| **`passwd`** | Mengubah kata sandi pengguna saat ini. |
| **`whoami`** | Nama pengguna dari pengguna yang sedang *login* di terminal. |
| **`who`** | Daftar semua pengguna yang saat ini sedang *login* sebagai pengguna. |
| **`w`** | Menampilkan status sistem saat ini, waktu, durasi, daftar pengguna yang sedang *login* di sistem, dan informasi pengguna lainnya. |
| **`last`** | Siapa yang baru-baru ini menggunakan sistem. |
| **`last root`** | Kapan terakhir kali `root` *login* sebagai pengguna. |
| **`lastb`** | Menunjukkan semua upaya *login* yang gagal ke dalam sistem. |
| **`chmod`** | Mengubah izin - baca, tulis, eksekusi (*read, write, execute*) dari sebuah berkas atau direktori. |


### **Informasi Terkait Proses**

| Perintah | Kegunaan |
| :--- | :--- |
| **`top`** | Menampilkan daftar semua proses yang diurutkan berdasarkan penggunaan sumber daya sistem saat ini. Menampilkan tampilan proses yang terus diperbarui (Secara *default* 3 detik). Gunakan tombol `q` untuk keluar dari `top`. |
| **`ps`** | Menampilkan daftar proses yang sedang berjalan pada sesi *shell* saat ini. |
| **`ps -u root`** | Menampilkan semua proses dan perintah yang sedang dijalankan oleh `root`. |
| **`ps aux`** | Menampilkan semua proses oleh semua pengguna di sistem saat ini. |


## **Bagian 1.4: Mencari Berkas Berdasarkan Pola pada Nama/Konten**

Tugas umum bagi seseorang yang menggunakan *Linux Command Line* (*shell*) adalah mencari berkas/direktori dengan nama tertentu atau yang mengandung teks tertentu. Ada 2 perintah yang harus Anda kenali untuk mencapai ini:

### **Mencari Berkas Berdasarkan Nama**

```bash
find /var/www -name '*.css'
```

Perintah ini akan mencetak *path* lengkap/nama berkas ke semua berkas di bawah `/var/www` yang berakhiran `.css`. Contoh keluaran:

```
/var/www/html/text-cursor.css
/var/www/html/style.css
```

Untuk info lebih lanjut:

```bash
man find
```

### **Mencari Berkas yang Mengandung Teks**

```bash
grep font /var/www/html/style.css
```

Perintah ini akan mencetak semua baris yang mengandung pola `font` dalam berkas yang ditentukan. Contoh keluaran:

```
font-weight: bold;
font-family: monospace;
```

Contoh lain:

```bash
grep font /var/www/html/
```

Ini tidak berfungsi seperti yang Anda harapkan. Anda akan mendapatkan:

```
grep: /var/www/html/: Is a directory
```

Anda perlu melakukan `grep` secara rekursif agar berfungsi, dengan menggunakan opsi `-R`:

```bash
grep -R font /var/www/html/
```

Wah, keren\! Lihat keluaran yang satu ini:

```
/var/www/html/admin/index.php: echo '<font color=red><b>Error: no dice</b></font><br/>';
/var/www/html/admin/index.php: echo '<font color=red><b>Error: try again</b></font><br/>';
/var/www/html/style.css: font-weight: bold;
/var/www/html/style.css: font-family: monospace;
```

Perhatikan bahwa ketika `grep` mencocokkan beberapa berkas, ia memberi awalan pada baris yang cocok dengan nama berkasnya. Anda bisa menggunakan opsi `-h` untuk menghilangkannya jika Anda mau.

Untuk info lebih lanjut:

```bash
man grep
```


## **Bagian 1.5: Manipulasi Berkas**

Berkas dan direktori (nama lain untuk folder) adalah inti dari Linux, jadi kemampuan untuk membuat, melihat, memindahkan, dan menghapusnya dari baris perintah sangatlah penting dan sangat kuat. Perintah manipulasi berkas ini memungkinkan Anda melakukan tugas yang sama seperti yang dilakukan oleh penjelajah berkas grafis.

**Membuat berkas teks kosong bernama `myFile`:**

```bash
touch myFile
```

**Mengganti nama `myFile` menjadi `myFirstFile`:**

```bash
mv myFile myFirstFile
```

**Melihat isi dari sebuah berkas:**

```bash
cat myFirstFile
```

**Melihat konten berkas dengan *pager* (satu layar penuh pada satu waktu):**

```bash
less myFirstFile
```

**Melihat beberapa baris pertama dari sebuah berkas:**

```bash
head myFirstFile
```

**Melihat beberapa baris terakhir dari sebuah berkas:**

```bash
tail myFirstFile
```

**Mengedit sebuah berkas:**

```bash
vi myFirstFile
```

**Melihat berkas apa saja yang ada di direktori kerja Anda saat ini:**

```bash
ls
```

**Membuat direktori kosong bernama `myFirstDirectory`:**

```bash
mkdir myFirstDirectory
```

**Membuat direktori dengan multi-*path*: (membuat dua direktori, `src` dan `myFirstDirectory`)**

```bash
mkdir -p src/myFirstDirectory
```

**Memindahkan berkas ke dalam direktori:**

```bash
mv myFirstFile myFirstDirectory/
```

**Anda juga dapat mengganti nama berkas:**

```bash
user@linux-computer:~$ mv myFirstFile secondFileName
```

**Mengubah direktori kerja saat ini ke `myFirstDirectory`:**

```bash
cd myFirstDirectory
```

**Menghapus sebuah berkas:**

```bash
rm myFirstFile
```

**Pindah ke direktori induk (yang direpresentasikan sebagai `..`):**

```bash
cd ..
```

**Menghapus direktori yang kosong:**

```bash
rmdir myFirstDirectory
```

**Menghapus direktori yang tidak kosong (yaitu berisi berkas dan/atau direktori lain):**

```bash
rm -rf myFirstDirectory
```

**Perlu diingat bahwa saat menghapus direktori, pastikan Anda menghapus `./` bukan `/`, karena itu akan menghapus seluruh sistem berkas Anda.**


## **Bagian 1.6: Detail Berkas/Direktori**

Perintah `ls` memiliki beberapa opsi yang dapat digunakan bersama untuk menampilkan lebih banyak informasi.

### **Detail/Hak Akses**

Opsi `-l` menunjukkan izin berkas, ukuran, dan tanggal modifikasi terakhir. Jadi, jika direktori *root* berisi direktori bernama `test` dan berkas `someFile`, maka perintah:

```bash
user@linux-computer:~$ ls -l
```

Akan menghasilkan keluaran seperti:

```
-rw-r--r-- 1 user users   70 Jul 22 13:36 someFile.txt
drwxrwxrwx 2 user users 4096 Jul 21 07:18 test
```

Izinnya dalam format `drwxrwxrwx`. Karakter pertama menunjukkan jenis berkas: `d` jika itu direktori, `-` jika bukan. Tiga karakter berikutnya `rwx` adalah izin yang dimiliki **pengguna** (*user*) atas berkas, tiga berikutnya adalah izin yang dimiliki **grup** (*group*) atas berkas, dan tiga terakhir adalah izin yang dimiliki **orang lain** (*everyone else*) atas berkas tersebut.

`r` dari `rwx` berarti jika berkas bisa **dibaca** (*read*), `w` berarti jika berkas bisa **diubah/ditulis** (*write*), dan `x` berarti jika berkas bisa **dieksekusi** (*execute*). Jika ada izin yang tidak diberikan, tanda `-` akan menggantikan `r`, `w`, atau `x`.

Jadi dari contoh di atas, *user* dapat membaca dan mengubah `someFile.txt` tetapi *group* hanya memiliki hak baca saja.

Untuk mengubah hak akses, Anda dapat menggunakan perintah `chmod ### namaBerkas` jika Anda memiliki hak `sudo`. `r` diwakili oleh nilai **4**, `w` diwakili oleh **2**, dan `x` diwakili oleh **1**. Jadi, jika Anda ingin hanya Anda yang dapat mengubah isi direktori `test`:

  * **Pemilik** `rwx` = 4+2+1 = **7**
  * **Grup** `r-x` = 4+0+1 = **5**
  * **Lainnya** `r-x` = 4+0+1 = **5**

Maka, perintah lengkapnya adalah:

```bash
chmod 755 test
```

Sekarang, jika menjalankan `ls -l` akan menunjukkan sesuatu seperti:

```
drwxr-xr-x 2 user users 4096 Jul 21 07:20 test
```

### **Ukuran yang Mudah Dibaca (*Readable Size*)**

Digunakan bersama dengan opsi `-l`, opsi `-h` menunjukkan ukuran berkas yang mudah dibaca manusia. Menjalankan:

```bash
user@linux-computer:~$ ls -lh
```

Akan menghasilkan keluaran:

```
total 4166
-rw-r--r-- 1 user users   70 Jul 22 13:36 someFile.txt
drwxrwxrwx 2 user users 4.0K Jul 21 07:18 test
```

### **Tersembunyi (*Hidden*)**

Untuk melihat berkas tersembunyi, gunakan opsi `-a`. Contohnya:

```bash
user@linux-computer:~$ ls -a
```

Mungkin akan menampilkan:

```
.profile
someFile.txt
test
```

### **Ukuran Total Direktori**

Untuk melihat ukuran direktori saat ini, gunakan opsi `-s` (opsi `-h` juga dapat digunakan untuk membuat ukurannya lebih mudah dibaca).

```bash
user@linux-computer:~$ ls -s
```

Keluaran:

```
total 4166
someFile.txt
test
```

### **Tampilan Rekursif**

Katakanlah direktori `test` memiliki berkas `anotherFile` dan Anda ingin melihatnya dari folder *root*, Anda bisa menggunakan opsi `-R` yang akan menampilkan pohon rekursif.

```bash
user@linux-computer:~$ ls -R
```

Keluaran:

```
.:
someFile.txt
test

./test:
anotherFile
```

---

# Bab 2
## **Mendeteksi Nama dan Versi Distribusi Linux**

### **Bagian 2.1: Mendeteksi distribusi berbasis Debian yang sedang Anda gunakan**

Cukup jalankan **`lsb_release -a`**.

Pada Debian:

```bash
$ lsb_release -a
No LSB modules are available.
Distributor ID: Debian
Description:    Debian GNU/Linux testing (stretch)
Release:        testing
Codename:       stretch
```

Pada Ubuntu:

```bash
$ lsb_release -a
No LSB modules are available.
Distributor ID: Ubuntu
Description:    Ubuntu 14.04.4 LTS
Release:        14.04
Codename:       trusty
```

Jika Anda tidak memiliki `lsb_release` yang terinstal, Anda mungkin ingin mencoba menebak, sebagai contoh, ada berkas `/etc/issue` yang sering kali berisi nama distribusi. Contohnya, pada Ubuntu:

```bash
$ cat /etc/issue
Ubuntu 12.04.5 LTS \n \l
```

Jangan gunakan berkas `/etc/debian_version` karena isinya tidak cocok dengan nama distribusi\!

Perhatikan bahwa cara ini juga akan berfungsi pada distribusi non-keluarga Debian seperti Fedora, RHEL, atau openSUSE — tetapi `lsb_release` mungkin tidak terinstal.

## **Bagian 2.2: Mendeteksi distribusi berbasis systemd yang Anda gunakan**

Metode ini akan berfungsi pada versi modern dari Arch, CentOS, CoreOS, Debian, Fedora, Mageia, openSUSE, Red Hat Enterprise Linux, SUSE Linux Enterprise Server, Ubuntu, dan lainnya. Penerapannya yang luas menjadikannya pendekatan pertama yang ideal, dengan beralih ke metode lain jika Anda juga perlu mengidentifikasi sistem yang lebih lama.

Lihat isi **/etc/os-release**. Secara spesifik, lihat variabel **`NAME`**, **`VERSION`**, **`ID`**, **`VERSION_ID`**, dan **`PRETTY_NAME`**.

Pada Fedora, berkas ini mungkin terlihat seperti:

```
NAME=Fedora
VERSION="24 (Workstation Edition)"
ID=fedora
VERSION_ID=24
PRETTY_NAME="Fedora 24 (Workstation Edition)"
ANSI_COLOR="0;34"
CPE_NAME="cpe:/o:fedoraproject:fedora:24"
HOME_URL="https://fedoraproject.org/"
BUG_REPORT_URL="https://bugzilla.redhat.com/"
REDHAT_BUGZILLA_PRODUCT="Fedora"
REDHAT_BUGZILLA_PRODUCT_VERSION=24
REDHAT_SUPPORT_PRODUCT="Fedora"
REDHAT_SUPPORT_PRODUCT_VERSION=24
PRIVACY_POLICY_URL=https://fedoraproject.org/wiki/Legal:PrivacyPolicy
VARIANT="Workstation Edition"
VARIANT_ID=workstation
```

Pada CentOS, berkas ini mungkin terlihat seperti ini:

```
NAME="CentOS Linux"
VERSION="7 (Core)"
ID="centos"
ID_LIKE="rhel fedora"
VERSION_ID="7"
PRETTY_NAME="CentOS Linux 7 (Core)"
ANSI_COLOR="0;31"
CPE_NAME="cpe:/o:centos:centos:7"
HOME_URL="https://www.centos.org/"
BUG_REPORT_URL="https://bugs.centos.org/"
CENTOS_MANTISBT_PROJECT="CentOS-7"
CENTOS_MANTISBT_PROJECT_VERSION="7"
REDHAT_SUPPORT_PRODUCT="centos"
REDHAT_SUPPORT_PRODUCT_VERSION="7"
```

Berkas ini didokumentasikan di situs web freedesktop; pada prinsipnya, ini tidak spesifik untuk systemd — tetapi akan ada di semua distribusi berbasis systemd.

Dari *bash shell*, seseorang dapat mengambil sumber (*source*) berkas `/etc/os-release` dan kemudian menggunakan berbagai variabel secara langsung, seperti ini:

```bash
$ ( source /etc/os-release && echo "$PRETTY_NAME" )
Fedora 24 (Workstation Edition)
```

## **Bagian 2.3: Mendeteksi distribusi RHEL / CentOS / Fedora yang sedang Anda gunakan**

Lihat isi dari **/etc/redhat-release**

```bash
cat /etc/redhat-release
```

Berikut adalah keluaran dari mesin Fedora 24: `Fedora release 24 (Twenty Four)`

Seperti yang disebutkan dalam tanggapan berbasis Debian, Anda juga dapat menggunakan perintah **`lsb_release -a`**, yang menghasilkan keluaran ini dari mesin Fedora 24:

```
LSB Version:    :core-4.1-amd64:core-4.1-noarch:cxx-4.1-amd64:cxx-4.1-noarch:desktop-4.1-amd64:desktop-4.1-noarch:languages-4.1-amd64:languages-4.1-noarch:printing-4.1-amd64:printing-4.1-noarch
Distributor ID: Fedora
Description:    Fedora release 24 (Twenty Four)
Release:        24
Codename:       TwentyFour
```

## **Bagian 2.4: Uname - Mencetak informasi tentang sistem saat ini**

`Uname` adalah singkatan dari *unix name*. Cukup ketik `uname` di konsol untuk mendapatkan informasi tentang sistem operasi Anda.

```
uname [OPSI]
```

Jika tidak ada OPSI yang ditentukan, `uname` mengasumsikan opsi `-s`.

  * **`-a`** atau **`--all`** - Mencetak semua informasi, mengabaikan `-p` dan `-i` jika informasinya tidak diketahui.

Contoh:

```bash
> uname -a
SunOS hope 5.7 Generic_106541-08 sun4m sparc SUNW,SPARCstation-10
```

Semua opsi:

  * **`-s, --kernel-name`** - Mencetak nama kernel.
  * **`-n, --nodename`** - Mencetak nama *hostname* node jaringan.
  * **`-r, --kernel-release`** - Mencetak rilis kernel.
  * **`-v, --kernel-version`** - Mencetak versi kernel.
  * **`-m, --machine`** - Mencetak nama perangkat keras mesin.
  * **`-p, --processor`** - Mencetak tipe prosesor, atau "unknown".
  * **`-i, --hardware-platform`** - Mencetak platform perangkat keras, atau "unknown".
  * **`-o, --operating-system`** - Mencetak sistem operasi.
  * **`--help`** - Menampilkan pesan bantuan, dan keluar.
  * **`--version`** - Menampilkan informasi versi, dan keluar.

## **Bagian 2.5: Mendeteksi informasi dasar tentang distro Anda**

Cukup jalankan **`uname -a`**.

Pada Arch:

```bash
$ uname -a
Linux nokia 4.6.4-1-ARCH #1 SMP PREEMPT Mon Jul 11 19:12:32 CEST 2016 x86_64 GNU/Linux
```

## **Bagian 2.6: Menggunakan GNU coreutils**

Jadi, *GNU coreutils* seharusnya tersedia di semua sistem berbasis Linux (tolong koreksi saya jika saya salah di sini).

Jika Anda tidak tahu sistem apa yang Anda gunakan, Anda mungkin tidak bisa langsung melompat ke salah satu contoh di atas, oleh karena itu ini mungkin menjadi langkah pertama Anda.

```bash
$ uname -a
```

Pada sistem saya, ini memberi saya hasil sebagai berikut...

```
Linux Scibearspace 3.16.0-4-amd64 #1 SMP Debian 3.16.7-ckt25-2+deb8u3 (2016-07-02) x86_64 GNU/Linux
```

Di sini Anda dapat melihat hal-hal berikut:

  * `Scibearspace` : nama pc saya
  * `Scibearspace` : nama pc saya
  * `3.16.0-4-amd64` : kernel dan arsitekturnya
  * `SMP Debian 3.16.7-CKT25-2+deb8u3` : memberitahu saya bahwa saya menjalankan Debian dengan kernel 3.16
  * Akhirnya bagian terakhir saya menjalankan Debian 8 (update 3).

Saya akan menyambut siapa pun untuk menambahkan hasil untuk sistem RHEL, dan SuSe.


## **Bagian 2.7: Menemukan nama dan nomor rilis OS linux Anda (baik debian & rpm)**

Sebagian besar distro linux menyimpan info versinya di berkas `/etc/lsb-release` (debian) atau `/etc/redhat-release` (berbasis RPM). Menggunakan perintah generik di bawah ini seharusnya bisa membantu Anda melewati sebagian besar turunan Debian dan RPM seperti Linux Mint dan Cent-Os.

Contoh pada Mesin Ubuntu:

```bash
cat /etc/*release
```

```
DISTRIB_ID=Ubuntu
DISTRIB_RELEASE=14.04
DISTRIB_CODENAME=trusty
DISTRIB_DESCRIPTION="Ubuntu 14.04 LTS"
```

---

# Bab 3
## Mendapatkan informasi kernel Linux yang sedang berjalan**

### **Bagian 3.1: Mendapatkan detail kernel Linux**

Kita dapat menggunakan perintah `uname` dengan berbagai opsi untuk mendapatkan detail lengkap dari kernel yang sedang berjalan.

```bash
uname -a
```

```
Linux df1-ws-5084 4.4.0-64-generic #85-Ubuntu SMP Mon Feb 20 11:50:30 UTC 2017 x86_64 x86_64 x86_64 GNU/Linux
```

Sesuai dengan *man page*, berikut adalah beberapa opsi lainnya:

**Penggunaan:** `uname [OPSI]...`

Mencetak informasi sistem tertentu. Jika tanpa OPSI, sama dengan `-s`.

  * `-a, --all`
      * Cetak semua informasi, dalam urutan berikut, kecuali hilangkan `-p` dan `-i` jika tidak diketahui.
  * `-s, --kernel-name`
      * Cetak nama kernel.
  * `-n, --nodename`
      * Cetak nama *hostname* node jaringan.
  * `-r, --kernel-release`
      * Cetak rilis kernel.
  * `-v, --kernel-version`
      * Cetak versi kernel.
  * `-m, --machine`
      * Cetak nama perangkat keras mesin.
  * `-p, --processor`
      * Cetak tipe prosesor (tidak portabel).
  * `-i, --hardware-platform`
      * Cetak platform perangkat keras (tidak portabel).
  * `-o, --operating-system`
      * Cetak sistem operasi.
  * `--help`
      * Tampilkan bantuan ini dan keluar.
  * `--version`
      * Keluarkan informasi versi dan keluar.

---

# Bab 4
## Shell

*Shell* mengeksekusi sebuah program sebagai respons terhadap *prompt*-nya. Ketika Anda memberikan sebuah perintah, *shell* akan mencari program tersebut, lalu mengeksekusinya. Sebagai contoh, ketika Anda memberikan perintah `ls`, *shell* akan mencari utilitas/program bernama `ls`, dan kemudian menjalankannya di dalam *shell*. Argumen dan opsi yang Anda berikan bersama utilitas dapat memengaruhi hasil yang Anda dapatkan. *Shell* juga dikenal sebagai **CLI**, atau *command line interface* (antarmuka baris perintah).

### **Bagian 4.1: Mengubah shell default**

Sebagian besar distribusi modern akan hadir dengan **BASH** (*Bourne Again SHell*) yang sudah terpasang dan dikonfigurasi sebagai *shell* default. Perintah (sebenarnya sebuah *binary executable*, sebuah ELF) yang bertanggung jawab untuk mengubah *shell* di Linux adalah `chsh` (*change shell*).

Kita bisa terlebih dahulu memeriksa *shell* mana saja yang sudah terpasang dan dikonfigurasi di mesin kita dengan menggunakan perintah `chsh -l`, yang akan menghasilkan keluaran seperti ini:

```bash
[user@localhost ~]$ chsh -l
/bin/sh
/bin/bash
/sbin/nologin
/usr/bin/sh
/usr/bin/bash
/usr/sbin/nologin
/usr/bin/fish
```

Pada beberapa distribusi Linux, `chsh -l` tidak valid. Dalam kasus ini, daftar semua *shell* yang tersedia dapat ditemukan di dalam berkas `/etc/shells`. Anda dapat menampilkan isi berkas tersebut dengan `cat`:

```bash
[user@localhost ~]$ cat /etc/shells
# /etc/shells: valid login shells
/bin/sh
/bin/bash
/sbin/nologin
/usr/bin/sh
/usr/bin/bash
/usr/sbin/nologin
/usr/bin/fish
```

Sekarang kita bisa memilih *shell* default baru kita, contohnya `fish`, dan mengkonfigurasikannya menggunakan `chsh -s`:

```bash
[user@localhost ~]$ chsh -s /usr/bin/fish
Changing shell for user.
Password:
Shell changed.
```

*(Mengubah shell untuk pengguna.)*
*(Kata sandi:)*
*(Shell diubah.)*

Sekarang yang tersisa hanyalah melakukan siklus *log-off* dan *log-on*, dan nikmati *shell* default baru kita.

Jika Anda ingin mengubah *shell* default untuk pengguna yang berbeda, dan Anda memiliki hak administratif di mesin tersebut, Anda dapat melakukannya dengan menggunakan `chsh` sebagai *root*. Jadi, dengan asumsi kita ingin mengubah *shell* default `user_2` menjadi `fish`, kita akan menggunakan perintah yang sama seperti sebelumnya, tetapi dengan tambahan nama pengguna lain, `chsh -s /usr/bin/fish user_2`.

Untuk memeriksa apa *shell* default saat ini, kita dapat melihat variabel lingkungan `$SHELL`, yang menunjuk ke path *shell* default kita. Jadi, setelah perubahan kita, kita akan mendapatkan hasil yang mirip dengan ini:

```bash
~  echo $SHELL
/usr/bin/fish
```

**Opsi `chsh`:**

  * `-s shell`
      * Mengatur `shell` sebagai *login shell*.
  * `-l, --list-shells`
      * Mencetak daftar *shell* yang tercantum di `/etc/shells` dan keluar.
  * `-h, --help`
      * Mencetak pesan penggunaan dan keluar.
  * `-v, --version`
      * Mencetak informasi versi dan keluar.

### **Bagian 4.2: Utilitas Shell Dasar**

#### **Menyesuaikan Prompt Shell**

*Prompt* perintah default dapat diubah agar terlihat berbeda dan lebih singkat. Jika direktori saat ini panjang, *prompt* perintah default menjadi terlalu besar. Menggunakan `PS1` menjadi berguna dalam kasus-kasus ini. Perintah yang pendek dan disesuaikan akan terlihat cantik dan elegan. Pada tabel di bawah, `PS1` telah digunakan dengan sejumlah argumen untuk menunjukkan berbagai bentuk *prompt shell*. *Prompt* perintah default terlihat seperti ini: `user@host ~ $`, dalam kasus saya terlihat seperti ini: `bruce@gotham ~ $`. Ini dapat diubah sesuai tabel di bawah:

| Perintah | Kegunaan |
| :--- | :--- |
| `PS1='\w $ '` | `~ $` *prompt shell* sebagai nama direktori. Dalam hal ini direktori root adalah Root. |
| `PS1='\h $ '` | `gotham $` *prompt shell* sebagai *hostname*. |
| `PS1='\u $ '` | `bruce $` *prompt shell* sebagai nama pengguna. |
| `PS1='\t $ '` | `22:37:31 $` *prompt shell* dalam format 24 jam. |
| `PS1='@ $ '` | `10:37 PM` *prompt shell* dalam format waktu 12 jam. |
| `PS1='! $ '` | `732` akan menampilkan nomor riwayat perintah di tempat *prompt shell*. |
| `PS1='dude $ '`| `dude $` akan menampilkan *prompt shell* sesuai keinginan Anda. |

#### **Beberapa perintah shell dasar**

| Perintah | Kegunaan |
| :--- | :--- |
| **Ctrl-k** | potong (*cut/kill*). |
| **Ctrl-y** | tempel (*yank/paste*). |
| **Ctrl-a** | akan membawa kursor ke awal baris. |
| **Ctrl-e** | akan membawa kursor ke akhir baris. |
| **Ctrl-d** | akan menghapus karakter setelah/di kursor. |
| **Ctrl-l** | akan membersihkan layar/terminal. |
| **Ctrl-u** | akan membersihkan semua yang ada di antara *prompt* dan kursor. |
| **Ctrl-\_** | akan membatalkan hal terakhir yang diketik pada baris perintah. |
| **Ctrl-c** | akan menginterupsi/menghentikan pekerjaan/proses yang berjalan di *foreground*. |
| **Ctrl-r** | pencarian terbalik dalam riwayat. |
| `~/.bash_history` | menyimpan 500 perintah/kejadian terakhir yang digunakan pada *shell*. |
| `history` | akan menampilkan riwayat perintah. |
| `history | grep <key-word>` | akan menampilkan semua perintah dalam riwayat yang memiliki kata kunci `<key-word>` (berguna saat Anda hanya ingat sebagian dari perintah yang pernah digunakan). |

### **Bagian 4.3: Membuat Alias Perintah Anda Sendiri**

Jika Anda lelah menggunakan perintah yang panjang di bash, Anda dapat membuat alias perintah Anda sendiri.

Cara terbaik untuk melakukannya adalah dengan memodifikasi (atau membuat jika belum ada) sebuah berkas bernama `.bash_aliases` di folder *home* Anda. Sintaks umumnya adalah:

```bash
alias nama_alias='perintah_asli'
```

di mana `perintah_asli` adalah perintah yang Anda beri nama baru dan `nama_alias` adalah nama baru yang Anda berikan.

Sebagai contoh:

```bash
alias install='sudo apt-get -y install'
```

memetakan alias perintah baru `install` ke perintah asli `sudo apt-get -y install`. Ini berarti bahwa ketika Anda menggunakan `install` di terminal, ini akan diinterpretasikan oleh bash sebagai `sudo apt-get -y install`.

### **Bagian 4.4: Menemukan file di sistem Anda**

Menggunakan bash, Anda dapat dengan mudah menemukan sebuah berkas dengan perintah `locate`. Sebagai contoh, katakanlah Anda sedang mencari berkas `mykey.pem`:

```bash
locate mykey.pem
```

Terkadang nama berkas bisa aneh, misalnya Anda mungkin memiliki berkas seperti `random7897_mykey_0fidw.pem`. Katakanlah Anda mencari berkas ini tetapi Anda hanya ingat bagian `mykey` dan `pem`. Anda dapat menggabungkan perintah `locate` dengan `grep` menggunakan *pipe* seperti ini:

```bash
locate pem | grep mykey
```

Perintah ini akan menampilkan semua hasil yang mengandung kedua bagian tersebut.

Perhatikan bahwa tidak semua sistem memiliki utilitas `locate` yang terpasang, dan banyak yang memilikinya tetapi belum mengaktifkannya. `locate` cepat dan efisien karena secara berkala memindai sistem Anda dan menyimpan nama serta lokasi setiap berkas dalam *cache*, tetapi jika pengumpulan data itu tidak diaktifkan, maka ia tidak dapat memberi tahu Anda apa pun. Anda dapat menggunakan `updatedb` untuk memulai pemindaian sistem berkas secara manual guna memperbarui info yang disimpan di *cache* tentang berkas di sistem Anda.

Jika Anda tidak memiliki `locate` yang berfungsi, Anda dapat beralih ke utilitas `find`:

```bash
find / -name mykey.pem -print
```

Perintah ini kurang lebih setara dengan `locate mykey.pem` tetapi harus memindai sistem berkas Anda setiap kali Anda menjalankannya untuk mencari berkas yang dimaksud, alih-alih menggunakan data dari *cache*. Ini jelas lebih lambat dan kurang efisien, tetapi lebih *real-time*. Utilitas `find` dapat melakukan lebih dari sekadar menemukan berkas, tetapi deskripsi lengkap kemampuannya berada di luar cakupan contoh ini.

---

# Bab 5
## Memeriksa Ruang Disk**

### **Bagian 5.1: Memeriksa Penggunaan Disk pada Direktori**

Terkadang, Anda mungkin perlu mencari tahu direktori mana yang menghabiskan berapa banyak ruang disk, terutama ketika Anda menggunakan `df -h` dan menyadari bahwa ruang disk yang tersedia sudah menipis.

#### **du:**

Perintah `du` merangkum penggunaan disk dari sekumpulan BERKAS, secara rekursif untuk direktori.

Perintah ini sering digunakan dengan opsi `-sh`:

  * `-s, --summarize`
      * Hanya menampilkan total untuk setiap argumen.
  * `-h, --human-readable`
      * Mencetak ukuran dalam format yang dapat dibaca manusia (contoh: 1K, 234M, 2G).

Untuk merangkum penggunaan disk dari berkas-berkas di direktori saat ini, kita menggunakan:

```bash
du -sh *
```

Contoh keluaran:

```
572K    Documents
208M    Downloads
4,0K    Music
724K    Pictures
4,0K    Public
4,0K    Templates
4,0K    Videos
```

Kita juga dapat menyertakan berkas tersembunyi (*hidden files*) dengan menggunakan:

```bash
du -sh .[!.]* *
```

Contoh keluaran:

```
6,3M    .atom
4,0K    .bash_history
4,0K    .bash_logout
8,0K    .bashrc
350M    .cache
195M    .config
12K     .dbus
4,0K    .dmrc
44K     .gconf
60K     .gem
520K    .gimp-2.8
28K     .gnome
4,0K    .ICEauthority
8,3M    .local
8,0K    .nano
404K    .nv
36K     .pki
4,0K    .profile
8,0K    .ssh
0       .sudo_as_admin_successful
4,0K    .Xauthority
4,0K    .xsession-errors
4,0K    .xsession-errors.old
572K    Documents
208M    Downloads
4,0K    Music
724K    Pictures
4,0K    Public
4,0K    Templates
4,0K    Videos
```

Ketiga, Anda dapat menambahkan total pada keluaran dengan menambahkan opsi `-c`:

```bash
du -sch .[!.]* *
```

Hasil:

```
.
.
.
4,0K    Templates
4,0K    Videos
769M    total
```

Yang paling penting, menggunakan perintah `du` dengan benar pada direktori *root* adalah tindakan penyelamat untuk menemukan aplikasi/layanan atau pengguna mana yang menghabiskan ruang disk Anda secara tidak wajar. Misalnya, dalam kasus ketersediaan ruang disk yang sangat rendah untuk server web dan email, alasannya bisa jadi adalah serangan spam ke layanan email Anda, dan Anda dapat mendiagnosisnya hanya dengan menggunakan perintah `du`.

**Memeriksa penggunaan disk pada direktori root:**

```bash
sudo du -sch /.[!.]* /*
```

Contoh keluaran:

```
16K     /.VolumeIcon.icns
24K     /.VolumeIcon.png
13M     /bin
57M     /boot
4,0K    /cdrom
620K    /dev
13M     /etc
779M    /home
0       /initrd.img
406M    /lib
3,9M    /lib32
4,0K    /lib64
16K     /lost+found
4,0K    /media
4,0K    /mnt
367M    /opt
du: tidak dapat mengakses '/proc/18221/task/18221/fd/4': Tidak ada berkas atau direktori seperti itu
du: tidak dapat mengakses '/proc/18221/task/18221/fdinfo/4': Tidak ada berkas atau direktori seperti itu
du: tidak dapat mengakses '/proc/18221/fd/4': Tidak ada berkas atau direktori seperti itu
du: tidak dapat mengakses '/proc/18221/fdinfo/4': Tidak ada berkas atau direktori seperti itu
0       /proc
20K     /root
du: tidak dapat mengakses '/run/user/1000/gvfs': Izin ditolak
9,4M    /run
13M     /sbin
4,0K    /srv
0       /sys
72K     /tmp
3,5G    /usr
639M    /var
0       /vmlinuz
5,8G    total
```

Terakhir, metode terbaik terbentuk ketika Anda menambahkan nilai ambang batas ukuran untuk direktori agar mengabaikan yang berukuran kecil. Perintah ini hanya akan menampilkan folder dengan ukuran lebih dari 1GB yang terletak di bawah direktori *root* hingga ke cabang terjauh dari seluruh pohon direktori di sistem berkas Anda:

```bash
sudo du --threshold=1G -ch /.[!.]* /*
```

Contoh keluaran:

```
1,4G    /usr/lib
1,8G    /usr/share
3,5G    /usr
5,8G    total
```

### **Bagian 5.2: Memeriksa Ruang Disk**

Sudah menjadi hal yang biasa untuk ingin memeriksa status berbagai partisi/drive di server/komputer Anda untuk melihat seberapa penuh partisinya. Perintah berikut adalah yang ingin Anda jalankan:

```bash
df -h
```

Ini akan menghasilkan keluaran yang mirip dengan berikut ini:

```
[root@mail ~]# df -h
Filesystem                      Size  Used Avail Use% Mounted on
/dev/mapper/VolGroup-lv_root     19G  1.6G   16G   9% /
tmpfs                           245M     0  245M   0% /dev/shm
/dev/sda1                       485M   47M  413M  11% /boot
```

Dalam contoh dasar ini, kita dapat melihat bahwa partisi `/` hanya terpakai 9%.

Untuk contoh yang lebih kompleks yang juga mencakup penggunaan `df` untuk melihat berbagai *mountpoint*, lihat di bawah ini:

```
[root@mail ~]# df -h
Filesystem                Size  Used Avail Use% Mounted on
/dev/mapper/VG-root       1.9T  1.7T   89G  95% /
/dev/mapper/VG-var        431G  145G  264G  36% /var
devtmpfs                  7.8G  204K  7.8G   1% /dev
tmpfs                     7.8G  4.0K  7.8G   1% /dev/shm
/dev/md1                  495M  126M  344M  27% /boot
ku.example.com:9421       2.5T  487G  2.0T  20% /mnt/test
tmpfs                     500M   86M  415M  18% /var/ngx_pagespeed_cache
```

Dalam contoh ini, kita memiliki partisi `/` yang penuh 95% bersama dengan partisi `/var` tambahan yang hanya penuh 36%. Ada juga *mount* jaringan eksternal sebesar 2T yang di-*mount* di `/mnt/test` dan *mount* ramdisk/tmpfs sebesar 500M yang di-*mount* di `/var/ngx_pagespeed_cache`.

---

# Bab 6
## Mendapatkan Informasi Sistem**

Kumpulan perintah untuk mengambil informasi terkait sistem.

### **Bagian 6.1: Statistik tentang CPU, Memori, Jaringan, dan Disk (operasi I/O)**

Untuk mendapatkan statistik umum tentang komponen utama, keluarga perintah `stat` di Linux sangatlah berguna.

#### **CPU**

Untuk mendapatkan statistik terkait prosesor, Anda dapat menggunakan perintah `mpstat`, tetapi dengan beberapa opsi, perintah ini akan memberikan visibilitas yang lebih baik:

```bash
$ mpstat 2 10
```

#### **Memori**

Kita semua tahu perintah `free` untuk menunjukkan jumlah RAM (yang tersisa), tetapi untuk melihat semua statistik termasuk operasi I/O:

```bash
$ vmstat 2 10
```

#### **Disk**

Untuk mendapatkan informasi umum tentang operasi disk Anda secara *real-time*, Anda dapat memanfaatkan `iostat`.

```bash
$ iostat -kx 2
```

#### **Jaringan**

Untuk dapat melihat apa yang terjadi dengan layanan jaringan Anda, Anda dapat menggunakan `netstat`.

```bash
$ netstat -ntlp # soket TCP yang terbuka
$ netstat -nulp # soket UDP yang terbuka
$ netstat -nxlp # soket Unix yang terbuka
```

Tetapi Anda mungkin merasa pemantauan untuk melihat lalu lintas jaringan secara *real-time* lebih berguna:

```bash
$ sudo iftop
```

#### **Opsional**

Untuk menghasilkan statistik secara *real-time* yang terkait dengan operasi I/O di semua komponen, Anda dapat menggunakan `dstat`. Alat ini adalah pengganti serbaguna untuk `vmstat`, `iostat`, dan `ifstat`.

### **Bagian 6.2: Menggunakan alat seperti lscpu dan lshw**

Dengan menggunakan alat seperti `lscpu`, ini adalah cara mudah untuk mendapatkan informasi CPU.

```bash
$ lscpu
```

```
Architecture:          x86_64
CPU op-mode(s):        32-bit, 64-bit
Byte Order:            Little Endian
CPU(s):                4
On-line CPU(s) list:   0-3
Thread(s) per core:    1
Core(s) per socket:    4
Socket(s):             1
NUMA node(s):          1
Vendor ID:             GenuineIntel
CPU family:            6
Model:                 23
Stepping:              10
CPU MHz:               1998.000
BogoMIPS:              5303.14
Virtualization:        VT-x
L1d cache:             32K
L1i cache:             32K
L2 cache:              2048K
NUMA node0 CPU(s):     0-3
```

Dengan menggunakan alat `lshw`

```bash
$ lshw | grep cpu
```

```
df1-ws-5084
description: Computer
width: 64 bits
capabilities: vsyscall32
    *-core
          description: Motherboard
          physical id: 0
          *-memory
               description: System memory
               physical id: 0
               size: 5881MiB
          *-cpu
               product: Intel(R) Pentium(R) CPU G3220 @ 3.00GHz
               vendor: Intel Corp.
               physical id: 1
               bus info: cpu@0
               size: 3GHz
               capacity: 3GHz
               width: 64 bits
```

### **Bagian 6.3: Menampilkan Daftar Perangkat Keras**

**Ubuntu:**
`lshw` adalah alat kecil untuk mengekstrak informasi terperinci tentang konfigurasi perangkat keras mesin. Ia dapat melaporkan konfigurasi memori yang tepat, versi *firmware*, konfigurasi *mainboard*, versi dan kecepatan CPU, konfigurasi *cache*, kecepatan *bus*, dll.

```bash
$ sudo lshw | less (atau more)
$ sudo lshw -html > myhardware.html
$ sudo lshw -xml > myhardware.xml
```

Untuk menampilkan info PCI

```bash
$ lspci -tv
```

Untuk melihat info USB

```bash
$ lsusb -tv
```

Untuk menampilkan informasi BIOS

```bash
$ dmidecode -q | less
```

Untuk melihat informasi spesifik tentang disk (disk `sda` dalam contoh), Anda dapat menggunakan:

```bash
$ hdparm -i /dev/sda
```

Beberapa utilitas/perintah tambahan akan membantu mengumpulkan beberapa informasi ekstra:

```bash
# Berapa lama total disk (sistem) ini telah menyala
$ smartctl -A /dev/sda | grep Power_On_Hours

# Lakukan tes kecepatan baca pada disk sda
$ hdparm -tT /dev/sda

# Uji blok yang tidak dapat dibaca pada disk sda
$ badblocks -s /dev/sda
```

### **Bagian 6.4: Menemukan informasi model/kecepatan CPU**

**Ubuntu:**

```bash
$ cat /proc/cpuinfo
```

Contoh Keluaran:

```
processor       : 0
vendor_id       : GenuineIntel
cpu family      : 6
model           : 15
model name      : Intel(R) Core(TM)2 Quad CPU    Q6600  @ 2.40GHz
stepping        : 11
cpu MHz         : 1596.000
cache size      : 4096 KB
physical id     : 0
siblings        : 4
core id         : 0
cpu cores       : 4
apicid          : 0
initial apicid  : 0
fpu             : yes
fpu_exception   : yes
cpuid level     : 10
wp              : yes
flags           : fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx lm constant_tsc arch_perfmon pebs bts rep_good pni dtes64 monitor ds_cpl vmx est tm2 ssse3 cx16 xtpr pdcm lahf_lm tpr_shadow vnmi flexpriority
bogomips        : 4800.18
clflush size    : 64
cache_alignment : 64
address sizes   : 36 bits physical, 48 bits virtual
power management:

....
..

processor       : 3
vendor_id       : GenuineIntel
cpu family      : 6
model           : 15
model name      : Intel(R) Core(TM)2 Quad CPU    Q6600  @ 2.40GHz
stepping        : 11
cpu MHz         : 1596.000
cache size      : 4096 KB
physical id     : 0
siblings        : 4
core id         : 3
cpu cores       : 4
apicid          : 3
initial apicid  : 3
fpu             : yes
fpu_exception   : yes
cpuid level     : 10
wp              : yes
flags           : fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush dts acpi mmx fxsr sse sse2 ss ht tm pbe syscall nx lm constant_tsc arch_perfmon pebs bts rep_good pni dtes64 monitor ds_cpl vmx est tm2 ssse3 cx16 xtpr pdcm lahf_lm tpr_shadow vnmi flexpriority
bogomips        : 4800.30
clflush size    : 64
cache_alignment : 64
address sizes   : 36 bits physical, 48 bits virtual
power management:
```

Menghitung jumlah prosesor (termasuk *core*):

```bash
$ grep -c processor /proc/cpuinfo
```

### **Bagian 6.5: Pemantauan proses dan pengumpulan informasi**

Secara keseluruhan, Anda memiliki dua cara untuk memantau proses di *host* linux.

#### **Pemantauan statis**

Perintah yang paling banyak digunakan adalah `ps` (yaitu, *process status*). Perintah ini digunakan untuk memberikan informasi tentang proses yang sedang berjalan, termasuk nomor identifikasi proses (PID) mereka.

Berikut beberapa opsi yang berguna untuk mengumpulkan informasi spesifik.

Menampilkan daftar proses dalam hierarki

```bash
$ ps -e -o pid,args --forest
```

Menampilkan daftar proses yang diurutkan berdasarkan penggunaan % CPU

```bash
$ ps -e -o pcpu,cpu,nice,state,cputime,args --sort pcpu | sed '/^ 0.0 /d'
```

Menampilkan daftar proses yang diurutkan berdasarkan penggunaan memori (KB).

```bash
$ ps -e -orss=,args= | sort -b -k1,1n | pr -TW$COLUMNS
```

Menampilkan semua *thread* untuk proses tertentu (proses "firefox-bin" dalam contoh)

```bash
$ ps -C firefox-bin -L -o pid,tid,pcpu,state
```

Setelah menemukan proses tertentu, Anda dapat mengumpulkan informasi yang terkait dengannya menggunakan `lsof` untuk menampilkan daftar *path* yang dibuka oleh ID proses tersebut.

```bash
$ lsof -p $$
```

Atau berdasarkan *path*, cari tahu daftar proses yang membuka *path* yang ditentukan.

```bash
$ lsof ~
```

#### **Pemantauan interaktif**

Alat yang paling umum dikenal untuk pemantauan dinamis adalah:

```bash
$ top
```

Ini adalah perintah yang sebagian besar sudah menjadi *default* yang memiliki banyak sekali opsi untuk memfilter dan menyajikan informasi secara *real-time* (dibandingkan dengan perintah `ps`).

Namun, masih ada opsi yang lebih canggih yang dapat dipertimbangkan dan dipasang sebagai pengganti `top`.

```bash
$ htop -d 5
```

atau

```bash
$ atop
```

Yang memiliki kemampuan untuk mencatat semua aktivitas ke dalam berkas log (secara *default* `atop` akan mencatat semua aktivitas setiap 600 detik). Ke dalam daftar ini, ada beberapa perintah khusus seperti `iotop` atau `iftop`.

```bash
$ sudo iotop
```

---

# Bab 7
## Perintah `ls`

### **Bagian 7.1: Opsi untuk perintah `ls`**

Daftar lengkap opsi:

  * **`ls -a`**: Tampilkan semua berkas termasuk berkas tersembunyi yang diawali dengan `.`.
  * **`ls --color`**: Daftar berwarna `[=always/never/auto]`.
  * **`ls -d`**: Tampilkan direktori - dengan akhiran `*/`.
  * **`ls -F`**: Tambahkan satu karakter dari `*/=>@|` pada entri.
  * **`ls -i`**: Tampilkan nomor indeks *inode* berkas.
  * **`ls -l`**: Tampilkan dengan format panjang - menunjukkan izin (*permission*).
  * **`ls -la`**: Tampilkan format panjang termasuk berkas tersembunyi.
  * **`ls -lh`**: Tampilkan format panjang dengan ukuran berkas yang mudah dibaca.
  * **`ls -ls`**: Tampilkan dengan format panjang beserta ukuran berkas.
  * **`ls -r`**: Tampilkan dalam urutan terbalik.
  * **`ls -R`**: Tampilkan pohon direktori secara rekursif.
  * **`ls -s`**: Tampilkan ukuran berkas.
  * **`ls -S`**: Urutkan berdasarkan ukuran berkas.
  * **`ls -t`**: Urutkan berdasarkan waktu & tanggal.
  * **`ls -X`**: Urutkan berdasarkan nama ekstensi.

### **Bagian 7.2: Perintah `ls` dengan opsi yang paling sering digunakan**

`ls` menunjukkan berkas dan direktori di direktori kerja saat ini (jika tidak ada argumen yang diberikan). (Secara *default*, ini tidak menampilkan berkas tersembunyi yang diawali dengan `.`)

```bash
user@ubuntu14:/usr$ ls
bin    games    include   lib    lib32   local   sbin   share   src
```

Untuk melihat semua berkas (termasuk berkas/folder tersembunyi), gunakan `ls -a` ATAU `ls --all`.

```bash
user@ubuntu14:/usr$ ls -a
.    ..    bin    games    include    lib    lib32    local    sbin    share    src
```

Untuk membedakan antara berkas, folder, *symbolic link*, dan lainnya, gunakan `ls -F` ATAU `ls --classify`.

```bash
user@ubuntu14:~$ ls -F
bash_profile_course  chat_apps/      Desktop/     Downloads/        foxitsoftware/  Public/     test/
bin/                 ClionProjects/  Documents/   IDE/              Music/          Pictures/   Templates/  Videos/
```

Di sini, karakter di akhir nama digunakan untuk membedakan berkas dan folder.

  * **`/`** menunjukkan direktori.
  * **`*`** menunjukkan berkas yang dapat dieksekusi (*executable*).
  * **`@`** menunjukkan *symbolic link*.

Untuk mendapatkan detail lebih lanjut tentang berkas dan direktori, gunakan `ls -l`.

```bash
user@ubuntu14:~/example$ ls -l
total 6464
-rw-r--r-- 1 dave dave      41 Dec 24 12:19 Z.txt
drwxr-xr-x 2 user group    4096 Dec 24 12:00 a_directory
-rw-r--r-- 1 user group       6 Dec 24 12:01 a_file
lrwxrwxrwx 1 user group       6 Dec 24 12:04 a_link -> a_file
-rw-r--r-- 1 user group       6 Dec 24 12:03 a_newer_file
-rw-r----- 1 user group 6586816 Dec 24 12:07 big.zip
```

Dalam contoh ini, ukuran total dari konten adalah 6460KB.
Kemudian ada entri untuk setiap berkas/direktori dalam urutan abjad dengan huruf besar sebelum huruf kecil.

  * Karakter pertama adalah **tipe** (misalnya `d` - direktori, `l` - tautan/*link*).
  * 9 karakter berikutnya menunjukkan **izin (*permission*)** untuk pengguna (*user*), grup (*group*), dan lainnya (*other*).
  * Ini diikuti oleh jumlah ***hard link***, kemudian **nama pemilik** dan **grup**.
  * Kolom berikutnya adalah **ukuran dalam byte**. Ini dapat ditampilkan dalam bentuk yang ramah manusia dengan menambahkan opsi `-h`, misalnya `6586816` ditampilkan sebagai `6.3M`.
  * Setelah itu diikuti oleh **stempel waktu (*timestamp*)** (biasanya waktu modifikasi).
  * Kolom terakhir adalah **nama**. Catatan: untuk tautan (*link*), target dari tautan tersebut juga akan ditampilkan.
  
---

# Bab 8
## Kompresi Berkas dengan perintah `tar`

### **Opsi Umum**

| Opsi | Keterangan |
| :--- | :--- |
| **-c --create** | Buat arsip baru. |
| **-x --extract** | Ekstrak berkas dari sebuah arsip. |
| **-t --list** | Tampilkan isi dari sebuah arsip. |
| **-f --file=ARCHIVE** | Gunakan berkas arsip atau direktori ARSIP. |
| **-v --verbose** | Tampilkan daftar berkas yang diproses secara rinci. |

### **Opsi Kompresi**

| Opsi | Keterangan |
| :--- | :--- |
| **-a --auto-compress**| Gunakan akhiran arsip untuk menentukan program kompresi. |
| **-j --bzip2** | Filter arsip melalui `bzip2`. |
| **-J --xz --lzma** | Filter arsip melalui `xz`. |
| **-z --gzip** | Filter arsip melalui `gzip`. |

### **Bagian 8.1: Mengompres sebuah folder**

Perintah ini membuat sebuah arsip sederhana dari sebuah folder:

```bash
tar -cf ./my-archive.tar ./my-folder/
```

Keluaran *verbose* (rinci) menunjukkan berkas dan direktori mana yang ditambahkan ke arsip, gunakan opsi `-v`:

```bash
tar -cvf ./my-archive.tar ./my-folder/
```

Untuk mengarsipkan folder yang dikompres dengan 'gzip', Anda harus menggunakan opsi `-z`:

```bash
tar -czf ./my-archive.tar.gz ./my-folder/
```

Sebagai alternatif, Anda dapat mengompres arsip dengan 'bzip2', dengan menggunakan opsi `-j`:

```bash
tar -cjf ./my-archive.tar.bz2 ./my-folder/
```

Atau kompres dengan 'xz', dengan menggunakan opsi `-J`:

```bash
tar -cJf ./my-archive.tar.xz ./my-folder/
```

### **Bagian 8.2: Mengekstrak folder dari sebuah arsip**

Berikut adalah contoh untuk mengekstrak folder dari sebuah arsip ke lokasi saat ini:

```bash
tar -xf nama-arsip.tar
```

Jika Anda ingin mengekstrak folder dari arsip ke tujuan tertentu:

```bash
tar -xf nama-arsip.tar -C ./direktori/tujuan
```

### **Bagian 8.3: Menampilkan isi dari sebuah arsip**

Menampilkan isi dari sebuah berkas arsip tanpa mengekstraknya:

```bash
tar -tf archive.tar.gz
```

```
Folder-In-Archive/
Folder-In-Archive/file1
Folder-In-Archive/Another-Folder/
Folder-In-Archive/Another-Folder/file2
```

### **Bagian 8.4: Menampilkan konten arsip**

Berikut adalah contoh menampilkan konten:

```bash
tar -tvf archive.tar
```

Opsi `-t` digunakan untuk menampilkan daftar. Untuk menampilkan konten dari arsip `tar.gz`, Anda juga harus menggunakan opsi `-z`:

```bash
tar -tzvf archive.tar.gz
```

### **Bagian 8.5: Mengompres dan mengecualikan satu atau beberapa folder**

Jika Anda ingin mengekstrak sebuah folder, tetapi Anda ingin mengecualikan satu atau beberapa folder selama ekstraksi, Anda dapat menggunakan opsi `--exclude`.

```bash
tar -cf archive.tar ./my-folder/ --exclude="my-folder/sub1" --exclude="my-folder/sub3"
```

Dengan pohon folder ini:

```
my-folder/
├── sub1/
├── sub2/
└── sub3/
```

Hasilnya akan menjadi:

```
./archive.tar
└── my-folder/
    └── sub2/
```

### **Bagian 8.6: Menghapus komponen awal (*leading components*)**

Untuk menghapus sejumlah komponen awal, gunakan opsi `--strip-components`:
`--strip-components=JUMLAH`

> Hapus `JUMLAH` komponen awal dari nama berkas saat ekstraksi.

Sebagai contoh, untuk menghapus folder awal, gunakan:

```bash
tar -xf --strip-components=1 nama-arsip.tar
```

---

# Bab 9
## Layanan (*Services*)

### **Bagian 9.1: Menampilkan daftar layanan yang berjalan di Ubuntu**

Untuk mendapatkan daftar layanan di sistem Anda, Anda dapat menjalankan:

```bash
service --status-all
```

Keluaran dari `service --status-all` menampilkan status layanan yang dikendalikan oleh **System V**.

Tanda **`+`** menunjukkan layanan sedang berjalan, tanda **`-`** menunjukkan layanan yang berhenti. Anda dapat melihat ini dengan menjalankan `service NAMA_LAYANAN status` untuk layanan yang bertanda `+` dan `-`.

Beberapa layanan dikelola oleh **Upstart**. Anda dapat memeriksa status semua layanan Upstart dengan `sudo initctl list`. Setiap layanan yang dikelola oleh Upstart juga akan muncul dalam daftar yang diberikan oleh `service --status-all` tetapi akan ditandai dengan **`?`**.

ref: [https://askubuntu.com/questions/407075/how-to-read-service-status-all-results](https://askubuntu.com/questions/407075/how-to-read-service-status-all-results)

### **Bagian 9.2: Manajemen layanan Systemd**

#### **Menampilkan Daftar Layanan**

  * **`systemctl`**
    Untuk menampilkan daftar layanan yang sedang berjalan.
  * **`systemctl --failed`**
    Untuk menampilkan daftar layanan yang gagal (*failed*).

#### **Mengelola Target (Mirip dengan Runlevel di SysV)**

  * **`systemctl get-default`**
    Untuk menemukan target *default* untuk sistem Anda.
  * **`systemctl set-default <nama-target>`**
    Untuk mengatur target *default* untuk sistem Anda.

#### **Mengelola Layanan saat Berjalan (*Runtime*)**

  * **`systemctl start [nama-layanan]`**
    Untuk memulai sebuah layanan.
  * **`systemctl stop [nama-layanan]`**
    Untuk menghentikan sebuah layanan.
  * **`systemctl restart [nama-layanan]`**
    Untuk memulai ulang (*restart*) sebuah layanan.
  * **`systemctl reload [nama-layanan]`**
    Untuk meminta layanan memuat ulang konfigurasinya.
  * **`systemctl status [nama-layanan]`**
    Untuk menunjukkan status terkini dari sebuah layanan.

#### **Mengelola *Autostart* Layanan**

  * **`systemctl is-enabled [nama-layanan]`**
    Untuk menunjukkan apakah sebuah layanan diaktifkan saat sistem *booting*.
  * **`systemctl is-active [nama-layanan]`**
    Untuk menunjukkan apakah sebuah layanan sedang aktif (berjalan).
  * **`systemctl enable [nama-layanan]`**
    Untuk mengaktifkan sebuah layanan saat sistem *booting*.
  * **`systemctl disable [nama-layanan]`**
    Untuk menonaktifkan sebuah layanan saat sistem *booting*.

#### **Menyamarkan Layanan (*Masking Services*)**

  * **`systemctl mask [nama-layanan]`**
    Untuk menyamarkan (*mask*) sebuah layanan (Membuatnya sulit untuk memulai layanan secara tidak sengaja).
  * **`systemctl unmask [nama-layanan]`**
    Untuk membuka samaran (*unmask*) sebuah layanan.

#### **Memulai Ulang Systemd**

  * **`systemctl daemon-reload`**
  
---

# Bab 10
## Mengelola Layanan (*Services*)**

### **Bagian 10.1: Mendiagnosis masalah pada sebuah layanan**

Pada sistem yang menggunakan **systemd**, seperti Fedora \>= 15, Ubuntu (Server dan Desktop) \>= 15.04, dan RHEL/CentOS \>= 7:

```bash
systemctl status [service-name]
```

...di mana `[service-name]` adalah layanan yang dimaksud; contohnya, `systemctl status sshd`.
Perintah ini akan menampilkan informasi status dasar dan setiap kesalahan (*error*) terbaru yang tercatat.

Anda dapat melihat kesalahan lebih lanjut dengan `journalctl`. Sebagai contoh, `journalctl -xe` akan memuat 1000 catatan terakhir ke dalam *pager* (seperti `less`), dan langsung melompat ke bagian akhir. Anda juga dapat menggunakan `journalctl -f`, yang akan mengikuti pesan *log* saat pesan-pesan tersebut masuk.

Untuk melihat *log* dari layanan tertentu, gunakan *flag* `-t`, seperti ini:

```bash
journalctl -f -t sshd
```

Opsi berguna lainnya termasuk `-p` untuk prioritas (`-p warnings` untuk melihat hanya peringatan dan di atasnya), `-b` untuk "sejak *boot* terakhir", dan `-S` untuk "sejak" — dengan menggabungkan itu, kita bisa melakukan:

```bash
journalctl -p err -S yesterday
```

untuk melihat semua item yang dicatat sebagai *error* sejak kemarin.

Jika `journalctl` tidak tersedia, atau jika Anda mengikuti *log error* aplikasi yang tidak menggunakan *journal* sistem, perintah `tail` dapat digunakan untuk menunjukkan beberapa baris terakhir dari sebuah berkas. *Flag* yang berguna untuk `tail` adalah `-f` (untuk "*follow*"), yang menyebabkan `tail` terus menampilkan data saat ditambahkan ke berkas. Untuk melihat pesan dari sebagian besar layanan di sistem:

```bash
tail -f /var/log/messages
```

Atau, jika layanan tersebut memiliki hak istimewa (*privileged*), dan mungkin mencatat data sensitif:

```bash
tail -f /var/log/secure
```

Beberapa layanan memiliki berkas *log* sendiri, contoh yang baik adalah `auditd`, daemon audit linux, yang lognya disimpan di `/var/log/audit/`. Jika Anda tidak melihat keluaran dari layanan Anda di `/var/log/messages`, coba cari *log* spesifik layanan di `/var/log/`.

### **Bagian 10.2: Memulai dan Menghentikan Layanan**

Pada sistem yang menggunakan skrip init gaya **System-V**, seperti RHEL/CentOS 6:

```bash
service <service> start
service <service> stop
```

Pada sistem yang menggunakan **systemd**, seperti Ubuntu (Server dan Desktop) \>= 15.04, dan RHEL/CentOS \>= 7:

```bash
systemctl <service> dnsmasq
systemctl <service> dnsmasq
```

*[**Catatan Penerjemah:** Teks asli pada bagian ini tampaknya mengandung kesalahan ketik. Perintah yang benar untuk memulai dan menghentikan layanan dengan `systemctl` seharusnya adalah `systemctl start <service>` dan `systemctl stop <service>`.]*

### **Bagian 10.3: Mendapatkan status sebuah layanan**

Pada sistem yang menggunakan skrip init gaya **System-V**, seperti RHEL/CentOS 6:

```bash
service <service> status
```

Pada sistem yang menggunakan **systemd**, seperti Ubuntu (Server dan Desktop) \>= 15.04, dan RHEL/CentOS \>= 7.0:

```bash
systemctl status <service>
```

---

# Bab 11
## Memodifikasi Pengguna**

| Parameter | Detail |
| :--- | :--- |
| **`username`** | Nama pengguna. Jangan gunakan huruf kapital, jangan gunakan titik, jangan diakhiri dengan tanda hubung, tidak boleh mengandung titik dua, tanpa karakter khusus. Tidak boleh diawali dengan angka. |

### **Bagian 11.1: Mengatur kata sandi Anda sendiri**

```bash
passwd
```

### **Bagian 11.2: Mengatur kata sandi pengguna lain**

Jalankan perintah berikut sebagai **root**:

```bash
passwd username
```

### **Bagian 11.3: Menambahkan pengguna**

Jalankan perintah berikut sebagai **root**:

```bash
useradd username
```

### **Bagian 11.4: Menghapus pengguna**

Jalankan perintah berikut sebagai **root**:

```bash
userdel username
```

### **Bagian 11.5: Menghapus pengguna beserta folder *home*-nya**

Jalankan perintah berikut sebagai **root**:

```bash
userdel -r username
```

### **Bagian 11.6: Menampilkan daftar grup tempat pengguna saat ini berada**

```bash
groups
```

Informasi lebih detail tentang ID numerik pengguna dan grup dapat ditemukan dengan perintah `id`.

### **Bagian 11.7: Menampilkan daftar grup tempat seorang pengguna berada**

```bash
groups username
```

Informasi lebih detail tentang ID numerik pengguna dan grup dapat ditemukan dengan `id username`.

---

# Bab 12
## Perintah `tee`

### **Opsi**

| Opsi | Deskripsi |
| :--- | :--- |
| **-a, --append** | Tambahkan (*append*) ke BERKAS yang diberikan. Jangan menimpa. |
| **-i, --ignore-interrupts** | Abaikan sinyal interupsi. |
| **--help** | Tampilkan pesan bantuan, dan keluar. |
| **--version** | Tampilkan informasi versi, dan keluar. |

**`tee` - membaca dari masukan standar dan menulis ke keluaran standar dan berkas.**

Perintah `tee` dinamai dari **sambungan-T** (*T-splitter*) dalam perpipaan, yang membagi aliran air ke dua arah dan berbentuk seperti huruf T kapital.

`tee` menyalin data dari masukan standar ke setiap BERKAS, dan juga ke keluaran standar. Akibatnya, `tee` **menduplikasi masukannya**, mengarahkannya ke beberapa keluaran sekaligus.

### **Bagian 12.1: Menulis keluaran ke stdout, dan juga ke sebuah berkas**

Perintah berikut hanya menampilkan keluaran di layar (*stdout*).

```bash
$ ls
```

Perintah berikut hanya menulis keluaran ke berkas dan tidak ke layar.

```bash
$ ls > file
```

Perintah berikut (dengan bantuan perintah `tee`) menulis keluaran **baik ke layar (*stdout*) maupun ke berkas**.

```bash
$ ls | tee file
```

### **Bagian 12.2: Menulis keluaran dari tengah rantai *pipe* ke sebuah berkas dan mengembalikannya ke *pipe***

Anda juga dapat menggunakan perintah `tee` untuk menyimpan keluaran dari sebuah perintah di dalam berkas dan mengarahkan keluaran yang sama ke perintah lain.

Perintah berikut akan menulis entri *crontab* saat ini ke dalam berkas `crontab-backup.txt` **dan** meneruskan entri *crontab* tersebut ke perintah `sed`, yang akan melakukan substitusi. Setelah substitusi, hasilnya akan ditambahkan sebagai pekerjaan *cron* baru.

```bash
$ crontab -l | tee crontab-backup.txt | sed 's/old/new/' | crontab –
```

### **Bagian 12.3: Menulis keluaran ke beberapa berkas**

Anda dapat menyalurkan (*pipe*) keluaran Anda ke beberapa berkas (termasuk terminal Anda) dengan menggunakan `tee` seperti ini:

```bash
$ ls | tee file1 file2 file3
```

### **Bagian 12.4: Memerintahkan `tee` untuk menambahkan (*append*) ke berkas**

Secara *default*, perintah `tee` akan menimpa berkas yang ada. Anda dapat memerintahkan `tee` untuk menambahkan (*append*) ke berkas menggunakan opsi `–a` seperti yang ditunjukkan:

```bash
$ ls | tee –a file
```

---

# Bab 13
## Secure Shell (SSH)

*Secure shell* digunakan untuk mengakses server dari klien dari jarak jauh melalui koneksi terenkripsi. **OpenSSH** digunakan sebagai alternatif untuk koneksi Telnet yang juga mencapai akses *shell* jarak jauh tetapi tidak terenkripsi. Klien OpenSSH sudah terpasang secara *default* pada sebagian besar distribusi GNU/Linux dan digunakan untuk terhubung ke server. Contoh-contoh ini menunjukkan cara menggunakan paket SSH untuk menerima koneksi SSH dan terhubung ke *host* lain.

### **Bagian 13.1: Menghubungkan ke server jarak jauh**

Untuk terhubung ke server, kita harus menggunakan SSH pada klien sebagai berikut:

```bash
# ssh -p port pengguna@alamat-server
```

  * **port** - Port SSH server yang sedang mendengarkan (port *default* adalah 22).
  * **pengguna** - Harus merupakan pengguna yang ada di server dengan hak istimewa SSH.
  * **alamat server** - IP/Domain dari server.

Sebagai contoh dunia nyata, mari kita berpura-pura Anda sedang membuat sebuah situs web. Perusahaan yang Anda pilih untuk meng-hosting situs Anda memberitahu bahwa servernya berlokasi di `web-servers.com` pada port kustom `2020` dan nama akun Anda `usr1` telah dipilih untuk membuat pengguna di server dengan hak istimewa SSH. Dalam kasus ini, perintah SSH yang digunakan adalah sebagai berikut:

```bash
# ssh -p 2020 usr1@web-servers.com
```

Jika nama akun di sistem jarak jauh sama dengan yang ada di klien lokal, Anda dapat menghilangkan nama pengguna. Jadi jika Anda adalah `usr1` di kedua sistem, maka Anda cukup menggunakan `web-servers.com` alih-alih `usr1@web-servers.com`.

Ketika server yang ingin Anda hubungi tidak dapat diakses secara langsung oleh Anda, Anda dapat mencoba menggunakan sakelar `ProxyJump` untuk terhubung melaluinya lewat server lain yang dapat Anda akses dan dapat terhubung ke server yang diinginkan.

```bash
# ssh -J usr1@10.0.0.1:2020 usr2@10.0.0.2 -p 2222
```

Ini akan memungkinkan Anda terhubung ke server `10.0.0.2` (menjalankan ssh di port 2222) melalui server di `10.0.0.1` (menjalankan ssh di port 2020). Tentu saja, Anda perlu memiliki akun di kedua server tersebut. Perhatikan juga bahwa sakelar `-J` diperkenalkan di OpenSSH versi 7.3.

### **Bagian 13.2: Memasang paket OpenSSH**

Baik untuk terhubung ke server SSH jarak jauh maupun untuk menerima koneksi SSH, keduanya memerlukan instalasi `openssh`.

**Debian:**

```bash
# apt-get install openssh
```

**Arch Linux:**

```bash
# pacman -S openssh
```

**Yum:**

```bash
# yum install openssh
```

### **Bagian 13.3: Mengonfigurasi server SSH untuk menerima koneksi**

Pertama, kita harus menyunting berkas konfigurasi *daemon* SSH. Meskipun pada distribusi Linux yang berbeda lokasinya mungkin berbeda, biasanya berkas ini disimpan di `/etc/ssh/sshd_config`.

Gunakan editor teks Anda untuk mengubah nilai yang diatur dalam berkas ini, semua baris yang diawali dengan `#` adalah komentar dan karakter ini harus dihapus agar dapat berlaku. Berikut adalah daftar rekomendasinya:

  * `Port` (pilih angka antara 0 - 65535, biasanya lebih besar dari empat digit)
  * `PasswordAuthentication yes`
  * `AllowUsers user1 user2 ...dst`

Perlu dicatat bahwa lebih baik **menonaktifkan login dengan kata sandi sama sekali** dan menggunakan **Kunci SSH** untuk keamanan yang lebih baik seperti yang dijelaskan dalam dokumen ini.

### **Bagian 13.4: Koneksi tanpa kata sandi (menggunakan pasangan kunci)**

Pertama-tama, Anda harus memiliki pasangan kunci (*key pair*). Jika Anda belum memilikinya, lihat topik 'Menghasilkan kunci publik dan privat'.

Pasangan kunci Anda terdiri dari kunci privat (`id_rsa`) dan kunci publik (`id_rsa.pub`). Yang perlu Anda lakukan hanyalah menyalin kunci publik ke *host* jarak jauh dan menambahkan isinya ke berkas `~/.ssh/authorized_keys`.

Salah satu cara sederhana untuk melakukannya adalah:

```bash
ssh <pengguna>@<ssh-server> 'cat >> ~/.ssh/authorized_keys' < id_rsa.pub
```

Setelah kunci publik ditempatkan dengan benar di direktori *home* pengguna Anda, Anda hanya perlu login menggunakan kunci privat yang sesuai:

```bash
ssh <pengguna>@<ssh-server> -i id_rsa
```

### **Bagian 13.5: Menghasilkan kunci publik dan privat**

Untuk menghasilkan kunci bagi klien SSH:

```bash
ssh-keygen [-t rsa | rsa1 | dsa ] [-C <komentar>] [-b bits]
```

Sebagai contoh:

```bash
ssh-keygen -t rsa -b 4096 -C emailku@email.com
```

Lokasi *default* adalah `~/.ssh/id_rsa` untuk kunci privat dan `~/.ssh/id_rsa.pub` untuk kunci publik.

Untuk info lebih lanjut, silakan kunjungi `man.openbsd.org`.

### **Bagian 13.6: Menonaktifkan layanan ssh**

Ini akan menonaktifkan layanan sisi server SSH, yang jika diperlukan, akan memastikan bahwa klien tidak dapat terhubung melalui ssh.

**Ubuntu**

```bash
sudo service ssh stop
sudo systemctl disable sshd.service
```

**Debian**

```bash
sudo /etc/init.d/ssh stop
sudo systemctl disable sshd.service
```

**Arch Linux**

```bash
sudo killall sshd
sudo systemctl disable sshd.service
```

---

# Bab 14
## SCP

### **Bagian 14.1: Salin Aman (*Secure Copy*)**

Perintah `scp` digunakan untuk menyalin berkas secara aman **ke** atau **dari** tujuan jarak jauh. Jika berkas berada di direktori kerja saat ini, hanya nama berkas saja yang cukup. Jika tidak, diperlukan path lengkap yang menyertakan *hostname* jarak jauh, contohnya:

```
pengguna_jarakjauh@beberapa_server.org:/path/ke/berkas
```

#### **Menyalin berkas lokal di CWD Anda ke direktori baru**

```bash
scp berkaslokal.txt /home/teman/share/
```

#### **Menyalin berkas jarak jauh ke direktori kerja Anda saat ini**

```bash
scp rocky@arena51.net:/home/rocky/game/data.txt ./
```

#### **Menyalin berkas dari satu lokasi jarak jauh ke lokasi jarak jauh lainnya**

```bash
scp mars@universe.org:/beacon/light/bitmap.conf jupiter@universe.org:/beacon/night/
```

Untuk menyalin direktori dan sub-direktori, gunakan opsi rekursif **'-r'** pada `scp`.

```bash
scp -r user@192.168.0.4:~/project/* ./workspace/
```

### **Bagian 15.2: Penggunaan Dasar**

```bash
# Salin berkas jarak jauh ke direktori lokal
scp user@remotehost.com:/remote/path/to/foobar.md /local/dest

# Salin berkas lokal ke direktori jarak jauh
scp foobar.md user@remotehost.com:/remote/dest

# Berkas kunci dapat digunakan (sama seperti ssh)
scp -i my_key.pem foobar.md user@remotehost.com:/remote/dest
```

---

# Bab 15
## GnuPG (GPG)
 
**GnuPG** adalah sistem manajemen kunci canggih yang memungkinkan penandatanganan atau enkripsi data secara aman. **GPG** adalah alat baris perintah (*command-line*) yang digunakan untuk membuat dan memanipulasi kunci GnuPG.

GnuPG paling banyak digunakan untuk koneksi **SSH** (*Secure Shell*) tanpa kata sandi atau otentikasi interaktif apa pun, yang secara signifikan meningkatkan tingkat keamanan.

Bagian-bagian berikut menjelaskan cara membuat, menggunakan, dan menjaga keamanan kunci GnuPG.

### **Bagian 15.1: Mengekspor kunci publik Anda**

Agar pasangan kunci publik-privat Anda berguna, Anda harus membuat kunci publik Anda tersedia secara bebas untuk orang lain. Pastikan Anda hanya bekerja dengan **kunci publik** Anda di sini, karena Anda **tidak boleh membagikan kunci privat Anda**. Anda dapat mengekspor kunci publik Anda dengan perintah berikut:

```bash
gpg —armor —export ALAMAT_EMAIL > public_key.asc
```

di mana `ALAMAT_EMAIL` adalah alamat email yang terkait dengan kunci tersebut.

Sebagai alternatif, Anda dapat mengunggah kunci publik Anda ke server kunci publik seperti `keys.gnupg.net` agar orang lain dapat menggunakannya. Untuk melakukannya, masukkan perintah berikut di terminal:

```bash
gpg —list-keys
```

Kemudian, cari string 8 digit (ID primer) yang terkait dengan kunci yang ingin Anda ekspor. Selanjutnya, jalankan perintah:

```bash
gpg —send-keys ID_PRIMER
```

di mana `ID_PRIMER` adalah ID aktual dari kunci tersebut.

Sekarang, kunci publik telah diunggah ke server kunci dan tersedia untuk umum.

### **Bagian 15.2: Membuat dan menggunakan kunci GnuPG dengan cepat**

Pasang `haveged` (contoh `sudo apt-get install haveged`) untuk mempercepat proses pembuatan *byte* acak. Kemudian:

```bash
gpg --gen-key
gpg --list-keys
```

menghasilkan keluaran:

```
pub   2048R/NNNNNNNN 2016-01-01
uid                  Nama <nama@contoh.com>
sub   2048R/xxxxxxxx 2016-01-01
```

Kemudian publikasikan:

```bash
gpg --keyserver pgp.mit.edu --send-keys NNNNNNNN
```

Selanjutnya, rencanakan untuk pencabutan (*revoke*): [https://www.hackdiary.com/2004/01/18/revoking-a-gpg-key/](https://www.hackdiary.com/2004/01/18/revoking-a-gpg-key/)

---

# Bab 16
## Konfigurasi Jaringan**

Dokumen ini mencakup dasar-dasar jaringan TCP/IP, administrasi jaringan, dan konfigurasi sistem. Linux dapat mendukung beberapa perangkat jaringan. Nama perangkat diberi nomor yang dimulai dari nol dan terus bertambah. Sebagai contoh, komputer dengan dua NIC akan memiliki dua perangkat berlabel `eth0` dan `eth1`.

### **Bagian 16.1: Resolusi DNS lokal**

Berkas: `/etc/hosts` berisi daftar *host* yang akan diresolusi secara lokal (bukan oleh DNS).

Contoh isi berkas:

```
127.0.0.1       localhost.localdomain   localhost
XXX.XXX.XXX.XXX your-node-name.your-domain.com node-name
```

Format berkas untuk `hosts` ditentukan oleh RFC 952.

### **Bagian 16.2: Mengonfigurasi server DNS untuk resolusi nama domain**

Berkas: `/etc/resolv.conf` berisi daftar server DNS untuk resolusi nama domain.

Contoh isi berkas:

```
nameserver 8.8.8.8 # Alamat IP dari server nama primer
nameserver 8.8.4.4 # Alamat IP dari server nama sekunder
```

Jika Anda menggunakan server DNS internal, Anda dapat memvalidasi apakah server ini me-resolusi nama DNS dengan benar menggunakan perintah `dig`:

```bash
$ dig google.com @your.dns.server.com +short
```

### **Bagian 16.3: Melihat dan memanipulasi rute (*routes*)**

#### **Memanipulasi tabel rute IP menggunakan `route`**

**Menampilkan tabel rute**

```bash
$ route # Menampilkan daftar rute dan juga me-resolusi nama host
$ route -n # Menampilkan daftar rute tanpa me-resolusi nama host untuk hasil yang lebih cepat
```

**Menambah/Menghapus rute**

| Opsi | Deskripsi |
| :--- | :--- |
| `add` atau `del` | Tambah atau hapus rute. |
| `-host x.x.x.x` | Tambah rute ke satu *host* yang diidentifikasi oleh alamat IP. |
| `-net x.x.x.x` | Tambah rute ke sebuah jaringan yang diidentifikasi oleh alamat jaringan. |
| `gw x.x.x.x` | Tentukan *gateway* jaringan. |
| `netmask x.x.x.x`| Tentukan *netmask* jaringan. |
| `default` | Tambah rute *default*. |

**Contoh:**

```bash
# Tambah rute ke sebuah host
$ route add -host x.x.x.x eth1

# Tambah rute ke sebuah jaringan
$ route add -net 2.2.2.0 netmask 255.255.255.0 eth0

# Sebagai alternatif, Anda juga bisa menggunakan format cidr untuk menambahkan rute ke jaringan
route add -net 2.2.2.0/24 eth0

# Tambah gateway default
$ route add default gw 2.2.2.1 eth0

# Hapus rute
$ route del -net 2.2.2.0/24
```

#### **Memanipulasi tabel rute IP menggunakan `ip`**

**Menampilkan tabel rute**

```bash
$ ip route show # Tampilkan daftar tabel rute
```

**Menambah/Menghapus rute**
| Opsi | Deskripsi |
| :--- | :--- |
| `add`, `del`, `change`, `append`, `replace` | Ubah sebuah rute. |
| `show` atau `flush` | Perintah ini menampilkan isi tabel rute atau menghapusnya. |
| `restore` | Pulihkan informasi tabel rute dari `stdin`. |
| `get` | Perintah ini mendapatkan satu rute ke tujuan dan mencetak isinya persis seperti yang dilihat oleh kernel. |

**Contoh:**

```bash
# Atur gateway default ke 1.2.3.254
$ ip route add default via 1.2.3.254

# Menambahkan rute default (untuk semua alamat) melalui gateway lokal 192.168.1.1 yang dapat dijangkau pada perangkat eth0
$ ip route add default via 192.168.1.1 dev eth0
```

### **Bagian 16.4: Mengonfigurasi *hostname* untuk sistem lain di jaringan Anda**

Anda dapat mengonfigurasi sistem Linux (atau macOS) Anda untuk mengikat sebuah pengidentifikasi `<hostname>` ke alamat IP sistem lain di jaringan Anda. Anda dapat mengonfigurasinya:

  * **Untuk seluruh sistem (*Systemwide*)**. Anda harus memodifikasi berkas `/etc/hosts`. Anda hanya perlu menambahkan baris baru ke berkas tersebut yang berisi:
    1.  alamat IP sistem jarak jauh `<ip_rem>`,
    2.  satu atau lebih spasi kosong, dan
    3.  pengidentifikasi `<hostname>`.
  * **Untuk satu pengguna**. Anda harus memodifikasi berkas `~/.hosts` --- Anda harus membuatnya terlebih dahulu. Caranya tidak sesederhana untuk seluruh sistem. Di sini Anda dapat melihat penjelasannya.

Misalnya, Anda bisa menambahkan baris ini menggunakan alat Unix `cat`. Misalkan Anda ingin melakukan `ping` ke PC di jaringan lokal Anda yang alamat IP-nya adalah `192.168.1.44` dan Anda ingin merujuk ke alamat IP tersebut hanya dengan `remote_pc`. Maka Anda harus menulis di *shell* Anda:

```bash
$ sudo cat 192.168.1.44 remote_pc
```

*[**Catatan Penerjemah:** Perintah `cat` di atas tidak benar untuk tujuan ini. Perintah yang benar untuk menambahkan baris ke `/etc/hosts` adalah `echo "192.168.1.44 remote_pc" | sudo tee -a /etc/hosts`.]*

Kemudian Anda dapat melakukan `ping` tersebut hanya dengan:

```bash
$ ping remote_pc
```

### **Bagian 16.5: Detail Antarmuka (*Interface*)**

#### **Ifconfig**

**Tampilkan semua antarmuka yang tersedia di mesin**

```bash
$ ifconfig -a
```

**Tampilkan detail dari antarmuka tertentu**

  * **Sintaks:** `$ ifconfig <antarmuka>`
  * **Contoh:**

<!-- end list -->

```bash
$ ifconfig eth0
```

```
eth0      Link encap:Ethernet  HWaddr xx:xx:xx:xx:xx:xx
          inet addr:x.x.x.x  Bcast:x.x.x.x  Mask:x.x.x.x
          inet6 addr: xxxx::xxx:xxxx:xxxx:xxxx/64 Scope:Link
          UP BROADCAST RUNNING MULTICAST  MTU:1500  Metric:1
          RX packets:4426618 errors:0 dropped:1124 overruns:0 frame:0
          TX packets:189171 errors:0 dropped:0 overruns:0 carrier:0
          collisions:0 txqueuelen:1000
          RX bytes:382611580 (382.6 MB)  TX bytes:36923665 (36.9 MB)
          Interrupt:16 Memory:fb5e0000-fb600000
```

#### **Ethtool** - menanyakan pengaturan driver jaringan dan perangkat keras

  * **Sintaks:** `$ ethtool <antarmuka>`
  * **Contoh:**

<!-- end list -->

```bash
$ ethtool eth0
```

```
Settings for eth0:
        Supported ports: [ TP ]
        Supported link modes:   10baseT/Half 10baseT/Full
                                100baseT/Half 100baseT/Full
                                1000baseT/Full
        Supported pause frame use: No
        Supports auto-negotiation: Yes
        Advertised link modes:  10baseT/Half 10baseT/Full
                                100baseT/Half 100baseT/Full
                                1000baseT/Full
        Advertised pause frame use: No
        Advertised auto-negotiation: Yes
        Speed: 1000Mb/s
        Duplex: Full
        Port: Twisted Pair
        PHYAD: 1
        Transceiver: internal
        Auto-negotiation: on
        MDI-X: on (auto)
        Supports Wake-on: pumbg
        Wake-on: g
        Current message level: 0x00000007 (7)
                               drv probe link
        Link detected: yes
```

#### **ip** - menampilkan / memanipulasi rute, perangkat, kebijakan rute, dan terowongan

  * **Sintaks:** `$ ip { link | ... | route | macsec }` (silakan lihat `man ip` untuk daftar objek lengkap)
  * **Contoh**

<!-- end list -->

```bash
# Tampilkan daftar antarmuka jaringan
$ ip link show

# Ganti nama antarmuka eth0 menjadi wan
$ ip link set dev eth0 name wan

# Aktifkan (atau nonaktifkan) antarmuka eth0
$ ip link set dev eth0 up

# Tampilkan daftar alamat untuk antarmuka
$ ip addr show

# Tambah (atau hapus) ip dan mask (255.255.255.0)
$ ip addr add 1.2.3.4/24 brd + dev eth0
```

### **Bagian 16.6: Menambahkan IP ke sebuah antarmuka**

Alamat IP untuk sebuah antarmuka dapat diperoleh melalui **DHCP** atau penetapan **Statis**.

  * **DHCP**
    Jika Anda terhubung ke jaringan dengan server DHCP yang berjalan, perintah `dhclient` dapat memperoleh alamat IP untuk antarmuka Anda.
    ```bash
    $ dhclient <antarmuka>
    ```
    atau sebagai alternatif, Anda dapat membuat perubahan pada berkas `/etc/network/interfaces` agar antarmuka diaktifkan saat *boot* dan memperoleh IP DHCP.
    ```
    auto eth0
    iface eth0 inet dhcp
    ```
  * **Konfigurasi Statis (Perubahan Permanen)** menggunakan berkas `/etc/network/interfaces`
    Jika Anda ingin mengonfigurasi pengaturan antarmuka secara statis (perubahan permanen), Anda dapat melakukannya di berkas `/etc/network/interfaces`.
    **Contoh:**
    ```
    auto eth0 # Aktifkan antarmuka saat boot
    iface eth0 inet static
        address 10.10.70.10
        netmask 255.255.0.0
        gateway 10.10.1.1
        dns-nameservers 10.10.1.20
        dns-nameservers 10.10.1.30
    ```
    Perubahan ini akan tetap ada bahkan setelah sistem di-*reboot*.
  * **Konfigurasi Statis (Perubahan Sementara)** menggunakan utilitas `ifconfig`
    Alamat IP statis dapat ditambahkan ke antarmuka menggunakan utilitas `ifconfig` sebagai berikut:
    ```bash
    $ ifconfig <antarmuka> <alamat-ip>/<mask> up
    ```
    **Contoh:**
    ```bash
    $ ifconfig eth0 10.10.50.100/16 up
    ```

---

# Bab 17
## Mengubah *root* (`chroot`)

Mengubah *root* (`chroot`) adalah operasi yang mengubah direktori *root* yang tampak untuk proses yang sedang berjalan dan proses turunannya (*children*). Sebuah program yang dijalankan dalam lingkungan yang dimodifikasi seperti ini tidak dapat mengakses berkas dan perintah di luar pohon direktori lingkungan tersebut.

### **Bagian 17.1: Persyaratan**

  * **Hak akses root**
  * Lingkungan Linux lain yang berfungsi, seperti boot dari **Live CD** atau distribusi yang sudah ada
  * **Arsitektur lingkungan yang cocok** antara sumber `chroot` dan tujuannya (periksa arsitektur lingkungan saat ini dengan `uname -m`)
  * **Modul kernel** yang mungkin Anda butuhkan di lingkungan `chroot` harus dimuat (misalnya, dengan `modprobe`)

### **Bagian 17.2: Mengubah *root* secara manual di dalam sebuah direktori**

1.  Pastikan Anda memenuhi semua persyaratan, sesuai dengan bagian **Persyaratan**.
2.  *Mount* sistem berkas API sementara:
    ```bash
    cd /lokasi/root/baru
    mount -t proc proc proc/
    mount --rbind /sys sys/
    mount --rbind /dev dev/
    mount --rbind /run run/ (opsional)
    ```
3.  Jika Anda perlu menggunakan koneksi internet di lingkungan `chroot`, salin detail DNS:
    ```bash
    cp /etc/resolv.conf etc/resolv.conf
    ```
4.  Ubah *root* ke `/lokasi/root/baru`, dengan menentukan *shell* (dalam contoh ini `/bin/bash`):
    ```bash
    chroot /lokasi/root/baru /bin/bash
    ```
5.  Setelah melakukan `chroot`, mungkin perlu untuk memuat konfigurasi bash lokal:
    ```bash
    source /etc/profile
    source ~/.bashrc
    ```
6.  Secara opsional, buat *prompt* yang unik agar dapat membedakan lingkungan `chroot` Anda:
    ```bash
    export PS1="(chroot) $PS1"
    ```
7.  Setelah selesai dengan `chroot`, Anda dapat keluar melaluinya dengan:
    ```bash
    exit
    ```
8.  *Unmount* sistem berkas sementara:
    ```bash
    cd /
    umount --recursive /lokasi/root/baru
    ```

### **Bagian 17.3: Alasan menggunakan `chroot`**

Mengubah *root* biasanya dilakukan untuk melakukan **pemeliharaan sistem** pada sistem di mana proses *booting* dan/atau *login* tidak lagi memungkinkan.

Contoh umum penggunaannya adalah:

  * Menginstal ulang **bootloader**
  * Membangun ulang citra (*image*) **initramfs**
  * Meningkatkan atau menurunkan versi **paket**
  * Mengatur ulang **kata sandi** yang terlupa
  * Membangun perangkat lunak di lingkungan *root* yang **bersih**
 
  
---

#Bab 18
## Mengompilasi kernel Linux

### **Bagian 21.1: Kompilasi Kernel Linux di Ubuntu**

**Peringatan:** pastikan Anda memiliki setidaknya **15 GB** ruang disk kosong.

#### **Kompilasi di Ubuntu \>=13.04**

#### **Opsi A) Gunakan Git**

Gunakan `git` jika Anda ingin tetap sinkron dengan kode sumber kernel Ubuntu terbaru. Instruksi terperinci dapat ditemukan di *Kernel Git Guide*. Repositori `git` tidak menyertakan berkas-berkas kontrol yang diperlukan, jadi Anda harus membuatnya dengan:

```bash
fakeroot debian/rules clean
```

#### **Opsi B) Unduh arsip sumber (*source archive*)**

Unduh arsip sumber - Ini untuk pengguna yang ingin membangun ulang paket standar Ubuntu dengan *patch* tambahan. Gunakan perintah berikut untuk menginstal dependensi *build* dan mengekstrak sumbernya (ke direktori saat ini):

1.  Pasang paket-paket berikut:
    ```bash
    sudo apt-get build-dep linux-image-`uname -r`
z    ```

#### **Opsi C) Unduh paket sumber dan bangun (*build*)**

Ini untuk pengguna yang ingin memodifikasi, atau bermain-main dengan, kode sumber kernel Ubuntu yang sudah di-*patch*.

1.  Ambil kode sumber kernel terbaru dari `kernel.org`.
2.  Ekstrak arsip ke sebuah direktori dan masuk ke dalamnya:
    ```bash
    tar xf linux-*.tar.xz
    cd linux-*
    ```
3.  Bangun antarmuka konfigurasi `ncurses`:
    ```bash
    make menuconfig
    ```
4.  Untuk menerima konfigurasi *default*, tekan `→` untuk menyorot **`< Exit >`** lalu tekan `Return`.
5.  Tekan `Return` lagi untuk menyimpan konfigurasi.
6.  Gunakan `make` untuk membangun kernel:
    ```bash
    make
    ```
    Perhatikan bahwa Anda dapat menggunakan *flag* `-j<jumlah-core>` untuk mengompilasi berkas secara paralel dan memanfaatkan banyak inti prosesor.

Citra (*image*) kernel yang terkompresi dapat ditemukan di `arch/[arch]/boot/bzImage`, di mana `[arch]` sama dengan keluaran dari `uname -a`.
