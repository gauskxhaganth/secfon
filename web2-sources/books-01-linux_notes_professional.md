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

