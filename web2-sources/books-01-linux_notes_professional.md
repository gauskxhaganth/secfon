# **Bab 1**

# **Memulai dengan GNU/Linux**

## **Bagian 1.1: Perintah Manajemen Berkas**

Linux menggunakan beberapa konvensi untuk direktori saat ini dan direktori induk. Hal ini bisa sedikit membingungkan bagi pemula. Setiap kali Anda berada di terminal Linux, Anda akan berada di dalam apa yang disebut **direktori kerja saat ini** (*current working directory*). Sering kali, *command prompt* Anda akan menampilkan seluruh direktori kerja, atau hanya bagian terakhir dari direktori tersebut. *Prompt* Anda bisa terlihat seperti salah satu dari berikut ini:

```
user@host ~/somedir $
user@host somedir $
user@host /home/user/somedir $
```

Ini menunjukkan bahwa direktori kerja Anda saat ini adalah `/home/user/somedir`.

Di Linux, `..` mewakili direktori induk dan `.` mewakili direktori saat ini. Oleh karena itu, jika direktori saat ini adalah `/home/user/somedir`, maka perintah `cd ../somedir` tidak akan mengubah direktori kerja.

Tabel di bawah ini mencantumkan beberapa perintah manajemen berkas yang paling sering digunakan.

-----

### **Navigasi Direktori**

| Perintah | Kegunaan |
| :--- | :--- |
| **`pwd`** | Mendapatkan *path* lengkap dari direktori kerja saat ini. |
| **`cd -`** | Menavigasi ke direktori terakhir tempat Anda bekerja. |
| **`cd ~`** atau hanya **`cd`** | Menavigasi ke direktori *home* pengguna saat ini. |
| **`cd ..`** | Pindah ke direktori induk dari direktori saat ini (perhatikan spasi antara `cd` dan `..`). |

-----

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

-----

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

-----

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

-----

## **Bagian 1.2: Hello World**

Ketik kode berikut ke terminal Anda, lalu tekan Enter:

```
echo "Hello World"
```

Ini akan menghasilkan keluaran sebagai berikut:

```
Hello World
```

-----

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

-----

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

-----

### **Informasi Terkait Proses**

| Perintah | Kegunaan |
| :--- | :--- |
| **`top`** | Menampilkan daftar semua proses yang diurutkan berdasarkan penggunaan sumber daya sistem saat ini. Menampilkan tampilan proses yang terus diperbarui (Secara *default* 3 detik). Gunakan tombol `q` untuk keluar dari `top`. |
| **`ps`** | Menampilkan daftar proses yang sedang berjalan pada sesi *shell* saat ini. |
| **`ps -u root`** | Menampilkan semua proses dan perintah yang sedang dijalankan oleh `root`. |
| **`ps aux`** | Menampilkan semua proses oleh semua pengguna di sistem saat ini. |

-----

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

-----

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

-----

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

# **Bab 2**

# **Mendeteksi Nama dan Versi Distribusi Linux**

## **Bagian 2.1: Mendeteksi distribusi berbasis Debian yang sedang Anda gunakan**

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

-----

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

## **Bab 3: Mendapatkan informasi kernel Linux yang sedang berjalan**

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

## **Bab 4: Shell**

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

