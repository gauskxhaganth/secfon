# Bab 1
## Memulai dengan Bash**

| Versi | Tanggal Rilis |
| :--- | :--- |
| 0.99 | 1989-06-08 |
| 1.01 | 1989-06-23 |
| 2.0 | 1996-12-31 |
| 2.02 | 1998-04-20 |
| 2.03 | 1999-02-19 |
| 2.04 | 2001-03-21 |
| 2.05b| 2002-07-17 |
| 3.0 | 2004-08-03 |
| 3.1 | 2005-12-08 |
| 3.2 | 2006-10-11 |
| 4.0 | 2009-02-20 |
| 4.1 | 2009-12-31 |
| 4.2 | 2011-02-13 |
| 4.3 | 2014-02-26 |
| 4.4 | 2016-09-15 |

### **Bagian 1.1: Hello World**

#### **Shell Interaktif**

*Shell* Bash biasanya digunakan secara interaktif: memungkinkan Anda memasukkan dan menyunting perintah, lalu mengeksekusinya saat Anda menekan tombol `Return`. Banyak sistem operasi berbasis Unix dan mirip Unix menggunakan Bash sebagai *shell default* mereka (terutama Linux dan macOS). Terminal secara otomatis memasuki proses *shell* Bash interaktif saat dimulai.

Keluarkan tulisan `Hello World` dengan mengetikkan yang berikut:

```bash
echo "Hello World"
#> Hello World # Contoh Keluaran
```

**Catatan**

  * Anda dapat mengubah *shell* hanya dengan mengetikkan nama *shell* di terminal. Contohnya: `sh`, `bash`, dll.
  * `echo` adalah perintah *built-in* Bash yang menulis argumen yang diterimanya ke keluaran standar. Secara *default*, `echo` menambahkan baris baru ke keluaran.

#### **Shell Non-Interaktif**

*Shell* Bash juga dapat dijalankan secara non-interaktif dari sebuah skrip, membuat *shell* tidak memerlukan interaksi manusia.

Perilaku interaktif dan perilaku skrip seharusnya identik – sebuah pertimbangan desain penting dari *shell* Bourne Unix V7 dan secara transitif juga Bash. Oleh karena itu, apa pun yang dapat dilakukan di baris perintah dapat dimasukkan ke dalam berkas skrip untuk digunakan kembali.

Ikuti langkah-langkah ini untuk membuat skrip Hello World:

1.  Buat berkas baru bernama `hello-world.sh`

    ```bash
    touch hello-world.sh
    ```

2.  Jadikan skrip dapat dieksekusi dengan menjalankan `chmod +x hello-world.sh`

3.  Tambahkan kode ini:

    ```bash
    #!/bin/bash
    echo "Hello World"
    ```

      * **Baris 1:** Baris pertama skrip harus dimulai dengan urutan karakter `#!`, yang disebut sebagai **shebang**¹. *Shebang* menginstruksikan sistem operasi untuk menjalankan `/bin/bash`, yaitu *shell* Bash, dengan memberikan path skrip sebagai argumennya.
        Contoh: `/bin/bash hello-world.sh`
      * **Baris 2:** Menggunakan perintah `echo` untuk menulis `Hello World` ke keluaran standar.

4.  Eksekusi skrip `hello-world.sh` dari baris perintah menggunakan salah satu cara berikut:

    ```bash
    ./hello-world.sh         # Paling umum digunakan, dan direkomendasikan
    /bin/bash hello-world.sh
    bash hello-world.sh      # Dengan asumsi /bin ada di dalam $PATH Anda
    sh hello-world.sh
    ```

Untuk penggunaan produksi nyata, Anda akan menghilangkan ekstensi `.sh` (yang sebenarnya menyesatkan, karena ini adalah skrip Bash, bukan skrip `sh`) dan mungkin memindahkan berkas tersebut ke direktori di dalam `PATH` Anda sehingga tersedia bagi Anda terlepas dari direktori kerja Anda saat ini, sama seperti perintah sistem seperti `cat` atau `ls`.

**Kesalahan umum meliputi:**

1.  Lupa memberikan izin eksekusi pada berkas, yaitu, `chmod +x hello-world.sh`, yang mengakibatkan keluaran `./hello-world.sh: Permission denied.`
2.  Menyunting skrip di Windows, yang menghasilkan karakter akhir baris yang salah yang tidak dapat ditangani oleh Bash. Gejala umumnya adalah `: command not found` di mana karakter *carriage return* telah memaksa kursor ke awal baris, menimpa teks sebelum titik dua dalam pesan kesalahan. Skrip dapat diperbaiki menggunakan program `dos2unix`.
    Contoh penggunaan: `dos2unix hello-world.sh`
    `dos2unix` akan menyunting berkas secara langsung.
3.  Menggunakan `sh ./hello-world.sh`, tanpa menyadari bahwa `bash` dan `sh` adalah *shell* yang berbeda dengan fitur yang berbeda (meskipun karena Bash kompatibel ke belakang, kesalahan sebaliknya tidak berbahaya).

Bagaimanapun, hanya mengandalkan baris *shebang* skrip jauh lebih baik daripada secara eksplisit menulis `bash` atau `sh` (atau `python` atau `perl` atau `awk` atau `ruby` atau...) sebelum nama berkas setiap skrip.

Baris *shebang* yang umum digunakan untuk membuat skrip Anda lebih portabel adalah dengan menggunakan `#!/usr/bin/env bash` alih-alih menuliskan path absolut ke Bash. Dengan cara itu, `/usr/bin/env` harus ada, tetapi setelah itu, `bash` hanya perlu berada di `PATH` Anda. Di banyak sistem, `/bin/bash` tidak ada, dan Anda harus menggunakan `/usr/local/bin/bash` atau path absolut lainnya; perubahan ini menghindari keharusan mencari tahu detailnya.

¹ *Juga disebut sebagai sha-bang, hashbang, pound-bang, hash-pling.*

### **Bagian 1.2: Hello World Menggunakan Variabel**

Buat berkas baru bernama `hello.sh` dengan konten berikut dan berikan izin eksekusi dengan `chmod +x hello.sh`.

Eksekusi/Jalankan melalui: `./hello.sh`

```bash
#!/usr/bin/env bash

# Perhatikan bahwa spasi tidak dapat digunakan di sekitar operator penugasan `=`
whom_variable="World"

# Gunakan printf untuk mengeluarkan data dengan aman
printf "Hello, %s\n" "$whom_variable"

#> Hello, World
```

Ini akan mencetak `Hello, World` ke keluaran standar saat dieksekusi.

Untuk memberitahu bash di mana skrip berada, Anda harus sangat spesifik, dengan menunjuk ke direktori yang memuatnya, biasanya dengan `./` jika itu adalah direktori kerja Anda, di mana `.` adalah alias untuk direktori saat ini. Jika Anda tidak menentukan direktori, bash mencoba mencari skrip di salah satu direktori yang terdapat dalam variabel lingkungan `$PATH`.

Kode berikut menerima argumen `$1`, yang merupakan argumen baris perintah pertama, dan mengeluarkannya dalam string yang diformat, setelah `Hello,`.

Eksekusi/Jalankan melalui: `./hello.sh World`

```bash
#!/usr/bin/env bash
printf "Hello, %s\n" "$1"

#> Hello, World
```

Penting untuk dicatat bahwa `$1` harus dikutip dalam **tanda kutip ganda**, bukan tanda kutip tunggal. `"$1"` akan diperluas menjadi argumen baris perintah pertama, seperti yang diinginkan, sementara `'$1'` dievaluasi sebagai string literal `$1`.

**Catatan Keamanan:**
Baca *Implikasi keamanan lupa mengutip variabel di shell bash* untuk memahami pentingnya menempatkan teks variabel di dalam tanda kutip ganda.

### **Bagian 1.3: Hello World dengan Masukan Pengguna (*User Input*)**

Berikut ini akan meminta masukan dari pengguna, dan kemudian menyimpan masukan tersebut sebagai string (teks) dalam sebuah variabel. Variabel tersebut kemudian digunakan untuk memberikan pesan kepada pengguna.

```bash
#!/usr/bin/env bash
echo "Siapa namamu?"
read name
echo "Halo, $name."
```

Perintah `read` di sini membaca satu baris data dari masukan standar ke dalam variabel `name`. Ini kemudian dirujuk menggunakan `$name` dan dicetak ke keluaran standar menggunakan `echo`.

Contoh keluaran:

```
$ ./hello_world.sh
Siapa namamu?
Matt
Halo, Matt.
```

Di sini pengguna memasukkan nama "Matt", dan kode ini digunakan untuk mengatakan `Halo, Matt.`.

Dan jika Anda ingin menambahkan sesuatu ke nilai variabel saat mencetaknya, gunakan kurung kurawal di sekitar nama variabel seperti yang ditunjukkan pada contoh berikut:

```bash
#!/usr/bin/env bash
echo "Apa yang sedang kamu lakukan?"
read action
echo "Kamu sedang ${action}."
```

Contoh keluaran:

```
$ ./hello_world.sh
Apa yang sedang kamu lakukan?
Tidur
Kamu sedang Tidur.
```

Di sini ketika pengguna memasukkan suatu tindakan, "ing" ditambahkan ke tindakan tersebut saat mencetak (dalam contoh ini, terjemahannya disesuaikan agar logis dalam Bahasa Indonesia).

### **Bagian 1.4: Pentingnya Tanda Kutip (*Quoting*) dalam String**

Tanda kutip penting untuk ekspansi string di bash. Dengan ini, Anda dapat mengontrol bagaimana bash mem-parsing dan memperluas string Anda.

Ada dua jenis tanda kutip:

  * **Lemah (*Weak*):** menggunakan tanda kutip ganda: `"`
  * **Kuat (*Strong*):** menggunakan tanda kutip tunggal: `'`

Jika Anda ingin bash memperluas argumen Anda, Anda dapat menggunakan **Tanda Kutip Lemah**:

```bash
#!/usr/bin/env bash
world="Dunia"
echo "Halo $world"
#> Halo Dunia
```

Jika Anda tidak ingin bash memperluas argumen Anda, Anda dapat menggunakan **Tanda Kutip Kuat**:

```bash
#!/usr/bin/env bash
world="Dunia"
echo 'Halo $world'
#> Halo $world
```

Anda juga dapat menggunakan karakter *escape* untuk mencegah ekspansi:

```bash
#!/usr/bin/env bash
world="Dunia"
echo "Halo \$world"
#> Halo $world
```

Untuk informasi lebih detail selain dari detail pemula, Anda dapat melanjutkan membacanya di sini.


### **Bagian 1.5: Melihat informasi untuk *built-in* Bash**

```bash
help <perintah>
```

Ini akan menampilkan halaman bantuan (manual) Bash untuk *built-in* yang ditentukan.

Sebagai contoh, `help unset` akan menampilkan:

```
unset: unset [-f] [-v] [-n] [name ...]
    Unset values and attributes of shell variables and functions.
    
    For each NAME, remove the corresponding variable or function.
    
    Options:
      -f        treat each NAME as a shell function
      -v        treat each NAME as a shell variable
      -n        treat each NAME as a name reference and unset the variable itself
                rather than the variable it references
    
    Without options, unset first tries to unset a variable, and if that fails,
    tries to unset a function.
    
    Some variables cannot be unset; also see `readonly'.
    
    Exit Status:
    Returns success unless an invalid option is given or a NAME is read-only.
```

Untuk melihat daftar semua *built-in* dengan deskripsi singkat, gunakan:

```bash
help -d
```

-----

### **Bagian 1.6: Hello World dalam mode "Debug"**

```bash
$ cat hello.sh
#!/bin/bash
echo "Hello World"

$ bash -x hello.sh
+ echo Hello World
Hello World
```

Argumen `-x` memungkinkan Anda menelusuri setiap baris dalam skrip. Salah satu contoh yang baik ada di sini:

```bash
$ cat hello.sh
#!/bin/bash
echo "Hello World\n"
adding_string_to_number="s"
v=$(expr 5 + $adding_string_to_number)

$ ./hello.sh
Hello World

expr: non-integer argument
```

Kesalahan yang muncul di atas tidak cukup untuk melacak skrip; namun, menggunakan cara berikut memberi Anda pemahaman yang lebih baik di mana harus mencari kesalahan dalam skrip.

```bash
$ bash -x hello.sh
+ echo 'Hello World\n'
Hello World\n
+ adding_string_to_number=s
+ expr 5 + s
expr: non-integer argument
+ v=
```

-----

### **Bagian 1.7: Menangani Argumen Bernama**

```bash
#!/bin/bash
deploy=false
uglify=false
while (( $# > 1 )); do case $1 in
    --deploy) deploy="$2";;
    --uglify) uglify="$2";;
    *) break;
esac; shift 2
done

$deploy && echo "akan mendeploy... deploy = $deploy"
$uglify && echo "akan meng-uglify... uglify = $uglify"

# cara menjalankan
# chmod +x script.sh
# ./script.sh --deploy true --uglify false
```

---

# Bab 2
## *Shebang* pada Skrip**

### **Bagian 2.1: *Shebang* Env**

Untuk mengeksekusi berkas skrip dengan *executable* `bash` yang ditemukan di variabel lingkungan `PATH` menggunakan *executable* `env`, baris pertama dari berkas skrip harus menunjukkan path absolut ke *executable* `env` dengan argumen `bash`:

```bash
#!/usr/bin/env bash
```

Path `env` dalam *shebang* akan diresolusi dan digunakan hanya jika skrip diluncurkan secara langsung seperti ini:

```bash
script.sh
```

Skrip tersebut harus memiliki izin eksekusi.

*Shebang* akan diabaikan ketika interpreter `bash` secara eksplisit ditunjukkan untuk mengeksekusi sebuah skrip:

```bash
bash script.sh
```

### **Bagian 2.2: *Shebang* Langsung**

Untuk mengeksekusi berkas skrip dengan interpreter `bash`, baris pertama dari berkas skrip harus menunjukkan path absolut ke *executable* `bash` yang akan digunakan:

```bash
#!/bin/bash
```

Path `bash` dalam *shebang* akan diresolusi dan digunakan hanya jika skrip diluncurkan secara langsung seperti ini:

```bash
./script.sh
```

Skrip tersebut harus memiliki izin eksekusi.

*Shebang* akan diabaikan ketika interpreter `bash` secara eksplisit ditunjukkan untuk mengeksekusi sebuah skrip:

```bash
bash script.sh
```
### **Bagian 2.3: *Shebang* Lainnya**

Ada dua jenis program yang dikenali oleh kernel. Program **biner** diidentifikasi oleh *header* **ELF** (*Extensible Loadable Format*), yang biasanya dihasilkan oleh sebuah kompilator. Yang kedua adalah **skrip** dari berbagai jenis.

Jika sebuah berkas dimulai pada baris paling pertama dengan urutan `#!`, maka string berikutnya harus merupakan *pathname* dari sebuah interpreter. Jika kernel membaca baris ini, ia akan memanggil interpreter yang disebutkan oleh *pathname* tersebut dan memberikan semua kata berikutnya di baris ini sebagai argumen kepada interpreter. Jika tidak ada berkas bernama "something" atau "wrong":

```bash
#!/bin/bash something wrong
echo "Baris ini tidak akan pernah tercetak"
```

`bash` akan mencoba mengeksekusi argumennya `"something wrong"` yang tidak ada. Nama berkas skrip juga akan ditambahkan. Untuk melihat ini dengan jelas, gunakan *shebang* `echo`:

```bash
#"/bin/echo something wrong
```

```bash
# dan sekarang panggil skrip ini yang bernama "thisscript" seperti ini:
# thisscript one two

# keluarannya akan menjadi:
something wrong ./thisscript one two
```

Beberapa program seperti `awk` menggunakan teknik ini untuk menjalankan skrip yang lebih panjang yang berada di dalam sebuah berkas di disk.

---

# Bab 3
## Menavigasi direktori

### Bagian 3.1: Direktori absolut vs relatif

Untuk berpindah ke direktori yang ditentukan secara absolut, gunakan nama lengkapnya, dimulai dengan garis miring `/`, seperti ini:

```bash
cd /home/username/project/abc
```

Jika Anda ingin berpindah ke direktori yang dekat dengan direktori Anda saat ini, Anda dapat menentukan lokasi relatif. Sebagai contoh, jika Anda sudah berada di `/home/username/project`, Anda dapat masuk ke subdirektori `abc` seperti ini:

```bash
cd abc
```

Jika Anda ingin pergi ke direktori di atas direktori saat ini, Anda dapat menggunakan alias `..`. Sebagai contoh, jika Anda berada di `/home/username/project/abc` dan ingin pergi ke `/home/username/project`, maka Anda akan melakukan hal berikut:

```bash
cd ..
```

Ini juga bisa disebut "naik" satu direktori.

### Bagian 3.2: Berpindah ke direktori terakhir

Untuk shell saat ini, perintah ini akan membawa Anda ke direktori sebelumnya tempat Anda berada, di mana pun itu.

```bash
cd -
```

Melakukannya beberapa kali secara efektif akan "beralih" antara direktori saat ini dan direktori sebelumnya.

### Bagian 3.3: Berpindah ke direktori home

Direktori default adalah direktori home (`$HOME`, biasanya `/home/username`), jadi `cd` tanpa direktori apa pun akan membawa Anda ke sana.

```bash
cd
```

Atau Anda bisa lebih eksplisit:

```bash
cd $HOME
```

Pintasan untuk direktori home adalah `~`, jadi itu juga bisa digunakan.

```bash
cd ~
```

### Bagian 3.4: Berpindah ke Direktori Skrip

Secara umum, ada dua jenis skrip Bash:

1.  Alat sistem yang beroperasi dari direktori kerja saat ini.
2.  Alat proyek yang memodifikasi file relatif terhadap lokasi mereka sendiri di sistem file.

Untuk jenis skrip kedua, akan sangat berguna untuk berpindah ke direktori tempat skrip disimpan. Ini dapat dilakukan dengan perintah berikut:

```bash
cd "$(dirname "$(readlink -f "$0")")"
```

Perintah ini menjalankan 3 perintah:

1.  `readlink -f "$0"` menentukan path ke skrip saat ini (`$0`).
2.  `dirname` mengubah path ke skrip menjadi path ke direktorinya.
3.  `cd` mengubah direktori kerja saat ini ke direktori yang diterimanya dari `dirname`.

---

# Bab 4
## Mendaftar File

| Opsi | Deskripsi |
| :--- | :--- |
| `-a`, `--all` | Mendaftar semua entri termasuk yang dimulai dengan titik |
| `-A`, `--almost-all`| Mendaftar semua entri kecuali `.` dan `..` |
| `-c` | Urutkan file berdasarkan waktu perubahan |
| `-d`, `--directory` | Mendaftar entri direktori |
| `-h`, `--human-readable` | Tampilkan ukuran dalam format yang mudah dibaca manusia (yaitu K, M) |
| `-H` | Sama seperti di atas hanya dengan pangkat 1000 bukan 1024 |
| `-l` | Tampilkan konten dalam format daftar panjang |
| `-o` | Format daftar panjang tanpa info grup |
| `-r`, `--reverse` | Tampilkan konten dalam urutan terbalik |
| `-s`, `--size` | Cetak ukuran setiap file dalam blok |
| `-S` | Urutkan berdasarkan ukuran file |
| `--sort=WORD` | Urutkan konten berdasarkan kata. (yaitu size, version, status) |
| `-t` | Urutkan berdasarkan waktu modifikasi |
| `-u` | Urutkan berdasarkan waktu akses terakhir |
| `-v` | Urutkan berdasarkan versi |
| `-1` | Daftar satu file per baris |

### Bagian 4.1: Mendaftar File dalam Format Daftar Panjang

Opsi `-l` pada perintah `ls` mencetak konten direktori yang ditentukan dalam format daftar panjang. Jika tidak ada direktori yang ditentukan, maka secara default, konten dari direktori saat ini akan didaftar.

```bash
ls -l /etc
```

Contoh Output:

```
total 1204
drwxr-xr-x   3 root root  4096 Apr 21 03:44 acpi
-rw-r--r--   1 root root  3028 Apr 21 03:38 adduser.conf
drwxr-xr-x   2 root root  4096 Jun 11 20:42 alternatives
...
```

Output pertama menampilkan `total`, yang menunjukkan ukuran total dalam blok dari semua file di direktori yang didaftar. Kemudian menampilkan delapan kolom informasi untuk setiap file di direktori yang didaftar. Di bawah ini adalah rincian untuk setiap kolom dalam output:

| No. Kolom | Contoh | Deskripsi |
| :--- | :--- | :--- |
| 1.1 | `d` | Tipe file (lihat tabel di bawah) |
| 1.2 | `rwxr-xr-x` | String izin akses |
| 2 | `3` | Jumlah hard link |
| 3 | `root` | Nama pemilik |
| 4 | `root` | Grup pemilik |
| 5 | `4096` | Ukuran file dalam byte |
| 6 | `Apr 21 03:44` | Waktu modifikasi |
| 7 | `acpi` | Nama file |

**Tipe File**

Tipe file bisa berupa salah satu dari karakter berikut.

| Karakter | Tipe File |
| :--- | :--- |
| `-` | File biasa |
| `b` | File spesial blok |
| `c` | File spesial karakter |
| `C` | File performa tinggi ("contiguous data") |
| `d` | Direktori |
| `D` | Door (file IPC khusus di Solaris 2.5+ saja) |
| `l` | Symbolic link |
| `M` | File off-line ("migrated") (Cray DMF) |
| `n` | File spesial jaringan (HP-UX) |
| `p` | FIFO (pipe bernama) |
| `P` | Port (file sistem khusus di Solaris 10+ saja) |
| `s` | Socket |
| `?` | Tipe file lainnya |

### Bagian 4.2: Mendaftar Sepuluh File yang Terakhir Dimodifikasi

Perintah berikut akan mendaftar hingga sepuluh file yang paling baru dimodifikasi di direktori saat ini, menggunakan format daftar panjang (`-l`) dan diurutkan berdasarkan waktu (`-t`).

```bash
ls -lt | head
```

### Bagian 4.3: Mendaftar Semua File Termasuk Dotfile

*Dotfile* adalah file yang namanya dimulai dengan `.`. File-file ini biasanya disembunyikan oleh `ls` dan tidak akan didaftar kecuali diminta.

Sebagai contoh, output `ls` berikut:

```bash
$ ls
bin pki
```

Opsi `-a` atau `--all` akan mendaftar semua file, termasuk *dotfile*.

```bash
$ ls -a
.               .bash_logout     .lesshst
..              .bash_profile    pki
.ansible        .bashrc          .puppetlabs
.bash_history   bin              .ssh
                                 .viminfo
```

Opsi `-A` atau `--almost-all` akan mendaftar semua file, termasuk *dotfile*, tetapi tidak mendaftar `.` dan `..` yang tersirat. Perhatikan bahwa `.` adalah direktori saat ini dan `..` adalah direktori induk.

```bash
$ ls -A
.ansible        .bashrc          pki
.bash_history   bin              .puppetlabs
.bash_logout    .lesshst         .ssh
.bash_profile                    .viminfo
```

### Bagian 4.4: Mendaftar File Tanpa Menggunakan `ls`

Gunakan kemampuan ekspansi nama file dan ekspansi kurung kurawal dari shell Bash untuk mendapatkan nama file:

```bash
# menampilkan file dan direktori yang ada di direktori saat ini
printf "%s\n" *

# menampilkan hanya direktori di direktori saat ini
printf "%s\n" */

# menampilkan hanya (beberapa) file gambar
printf "%s\n" *.{gif,jpg,png}
```

Untuk menangkap daftar file ke dalam sebuah variabel untuk diproses, biasanya merupakan praktik yang baik untuk menggunakan array bash:

```bash
files=( * )

# melakukan iterasi pada mereka
for file in "${files[@]}"; do
  echo "$file"
done
```

### Bagian 4.5: Mendaftar File

Perintah `ls` mendaftar konten dari direktori yang ditentukan, tidak termasuk *dotfile*. Jika tidak ada direktori yang ditentukan, maka secara default, konten dari direktori saat ini akan didaftar.

File yang didaftar diurutkan secara abjad, secara default, dan disejajarkan dalam kolom jika tidak muat dalam satu baris.

```bash
$ ls
apt          Documents    Fonts    Pictures       Public      Videos
configs      eclipse      git      Programming    Templates   workspace
bin          Desktop      Music
```

### Bagian 4.6: Mendaftar File dalam Format seperti Pohon

Perintah `tree` mendaftar konten dari direktori yang ditentukan dalam format seperti pohon. Jika tidak ada direktori yang ditentukan, maka secara default, konten dari direktori saat ini akan didaftar.

Contoh Output:

```bash
$ tree /tmp
/tmp
├── 5037
├── adb.log
└── evince-20965
    └── image.FPWTJY.png
```

Gunakan opsi `-L` dari perintah `tree` untuk membatasi kedalaman tampilan dan opsi `-d` untuk hanya mendaftar direktori.

Contoh Output:

```bash
$ tree -L 1 -d /tmp
/tmp
└── evince-20965
```

### Bagian 4.7: Mendaftar File Diurutkan Berdasarkan Ukuran

Opsi `-S` pada perintah `ls` mengurutkan file dalam urutan menurun berdasarkan ukuran file.

```bash
$ ls -l -S ./Fruits
total 444
-rw-rw-rw- 1 root root 295303 Jul 28 19:19 apples.jpg
-rw-rw-rw- 1 root root 102283 Jul 28 19:19 kiwis.jpg
-rw-rw-rw- 1 root root  50197 Jul 28 19:19 bananas.jpg
```

Ketika digunakan dengan opsi `-r`, urutan pengurutan dibalik.

```bash
$ ls -l -S -r /Fruits
total 444
-rw-rw-rw- 1 root root  50197 Jul 28 19:19 bananas.jpg
-rw-rw-rw- 1 root root 102283 Jul 28 19:19 kiwis.jpg
-rw-rw-rw- 1 root root 295303 Jul 28 19:19 apples.jpg
```

---

Tentu, ini adalah kelanjutan terjemahannya.

-----

## Bab 5: Menggunakan cat

| Opsi | Detail |
| :--- | :--- |
| `-n` | Cetak nomor baris |
| `-v` | Tampilkan karakter non-cetak menggunakan notasi `^` dan `M-` kecuali LFD dan TAB |
| `-T` | Tampilkan karakter TAB sebagai `^I` |
| `-E` | Tampilkan karakter baris baru (LF) sebagai `$` |
| `-e` | Sama dengan `-vE` |
| `-b` | Beri nomor pada baris output yang tidak kosong, menimpa `-n` |
| `-A` | Setara dengan `-vET` |
| `-s` | Hilangkan baris output kosong yang berulang, `s` merujuk pada *squeeze* |

### Bagian 5.1: Menggabungkan file

Ini adalah tujuan utama dari `cat`.

```bash
cat file1 file2 file3 > file_all
```

`cat` juga dapat digunakan dengan cara yang sama untuk menggabungkan file sebagai bagian dari sebuah *pipeline*, contohnya:

```bash
cat file1 file2 file3 | grep foo
```

### Bagian 5.2: Mencetak Isi File

```bash
cat file.txt
```

perintah di atas akan mencetak isi dari sebuah file.

Jika file berisi karakter non-ASCII, Anda dapat menampilkan karakter tersebut secara simbolis dengan `cat -v`. Ini bisa sangat berguna untuk situasi di mana karakter kontrol tidak akan terlihat.

```bash
cat -v unicode.txt
```

Namun, sangat sering, untuk penggunaan interaktif, Anda lebih baik menggunakan *pager* interaktif seperti `less` atau `more`. (`less` jauh lebih kuat daripada `more` dan disarankan untuk lebih sering menggunakan `less` daripada `more`.)

```bash
less file.txt
```

Untuk meneruskan isi file sebagai input ke sebuah perintah, pendekatan yang biasanya dianggap lebih baik (UUOC - *Useless Use of Cat*) adalah dengan menggunakan pengalihan (*redirection*).

```bash
tr A-Z a-z <file.txt
# sebagai alternatif dari cat file.txt | tr A-Z a-z
```

Jika konten perlu didaftar secara terbalik dari akhir, perintah `tac` dapat digunakan:

```bash
tac file.txt
```

Jika Anda ingin mencetak konten dengan nomor baris, maka gunakan `-n` dengan `cat`:

```bash
cat -n file.txt
```

Untuk menampilkan isi file dalam bentuk byte-demi-byte yang sama sekali tidak ambigu, *hex dump* adalah solusi standar. Ini bagus untuk cuplikan file yang sangat singkat, seperti ketika Anda tidak tahu pengkodean pastinya. Utilitas *hex dump* standar adalah `od -cH`, meskipun representasinya sedikit merepotkan; pengganti umum termasuk `xxd` dan `hexdump`.

```bash
$ printf 'Hëllö wörld' | xxd
0000000: 48c3 ab6c 6cc3 b620 77c3 b672 6c64  H..ll.. w..rld
```

### Bagian 5.3: Menulis ke sebuah file

```bash
cat >file
```

Perintah ini akan memungkinkan Anda menulis teks di terminal yang akan disimpan dalam file bernama `file`.

```bash
cat >>file
```

akan melakukan hal yang sama, kecuali itu akan menambahkan teks ke akhir file.

**N.B:** Tekan `Ctrl+D` untuk mengakhiri penulisan teks di terminal (Linux)

Sebuah *here document* dapat digunakan untuk menyisipkan konten file secara langsung ke dalam baris perintah atau skrip:

```bash
cat <<END >file
Hello, World.
END
```

Token setelah simbol pengalihan `<<` adalah string arbitrer yang harus muncul sendirian di satu baris (tanpa spasi di awal atau akhir) untuk menunjukkan akhir dari *here document*. Anda dapat menambahkan tanda kutip untuk mencegah shell melakukan substitusi perintah dan interpolasi variabel:

```bash
cat <<'fnord'
Nothing in `here` will be $changed
fnord
```

(Tanpa tanda kutip, `here` akan dieksekusi sebagai perintah, dan `$changed` akan diganti dengan nilai dari variabel `changed` -- atau tidak ada apa-apa, jika tidak terdefinisi.)

### Bagian 5.4: Menampilkan karakter yang tidak dapat dicetak

Ini berguna untuk melihat apakah ada karakter yang tidak dapat dicetak, atau karakter non-ASCII.
Misalnya, jika Anda menyalin-tempel kode dari web, Anda mungkin memiliki tanda kutip seperti `”` bukan standar `"`.

```bash
$ cat -v file.txt
$ cat -vE file.txt # Berguna dalam mendeteksi spasi di akhir baris.
```

Contoh:

```bash
$ echo '”
' | cat -vE # echo | akan digantikan oleh file sebenarnya.
M-bM-^@M-^]$
$
```

Anda mungkin juga ingin menggunakan `cat -A` (A untuk *All*) yang setara dengan `cat -vET`. Ini akan menampilkan karakter TAB (ditampilkan sebagai `^I`), karakter yang tidak dapat dicetak, dan akhir dari setiap baris:

```bash
$ echo '” `' | cat -A
M-bM-^@M-^]^I`$
```

### Bagian 5.5: Membaca dari input standar

```bash
cat < file.txt
```

Outputnya sama dengan `cat file.txt`, tetapi perintah ini membaca konten file dari input standar alih-alih langsung dari file.

```bash
printf "first line\nSecond line\n" | cat -n
```

Perintah `echo` sebelum `|` menghasilkan dua baris. Perintah `cat` bertindak pada output tersebut untuk menambahkan nomor baris.

### Bagian 5.6: Menampilkan nomor baris dengan output

Gunakan flag `--number` untuk mencetak nomor baris sebelum setiap baris. Sebagai alternatif, `-n` melakukan hal yang sama.

```bash
$ cat --number file
     1  line 1
     2  line 2
     3
     4  line 4
     5  line 5
```

Untuk melewati baris kosong saat menghitung baris, gunakan `--number-nonblank`, atau cukup `-b`.

```bash
$ cat -b file
     1  line 1
     2  line 2

     3  line 4
     4  line 5
```

### Bagian 5.7: Menggabungkan file yang di-gzip

File yang dikompresi oleh `gzip` dapat langsung digabungkan menjadi file `gzip` yang lebih besar.

```bash
cat file1.gz file2.gz file3.gz > combined.gz
```

Ini adalah properti `gzip` yang kurang efisien daripada menggabungkan file input dan kemudian melakukan `gzip` pada hasilnya:

```bash
cat file1 file2 file3 | gzip > combined.gz
```

Sebuah demonstrasi lengkap:

```bash
echo 'Hello world!' > hello.txt
echo 'Howdy world!' > howdy.txt
gzip hello.txt
gzip howdy.txt
cat hello.txt.gz howdy.txt.gz > greetings.txt.gz
gunzip greetings.txt.gz
cat greetings.txt
```

Yang menghasilkan:

```
Hello world!
Howdy world!
```

Perhatikan bahwa `greetings.txt.gz` adalah satu file tunggal dan didekompresi sebagai satu file tunggal `greetings.txt`. Bandingkan ini dengan `tar -czf hello.txt howdy.txt > greetings.tar.gz`, yang menjaga file-file tetap terpisah di dalam *tarball*.

---

# Bab 6
## Grep

### Bagian 6.1: Cara mencari pola dalam file

Untuk menemukan kata `foo` di dalam file `bar`:

```bash
grep foo ~/Desktop/bar
```

Untuk menemukan semua baris yang tidak mengandung `foo` di dalam file `bar`:

```bash
grep –v foo ~/Desktop/bar
```

Untuk menemukan semua kata yang mengandung `foo` di akhirnya (Ekspansi Wildcard):

```bash
grep "*foo" ~/Desktop/bar
```

---

# Bab 7
## Aliasing

Alias shell adalah cara sederhana untuk membuat perintah baru atau untuk membungkus perintah yang sudah ada dengan kode Anda sendiri. Mereka agak tumpang tindih dengan fungsi shell, yang bagaimanapun lebih serbaguna dan oleh karena itu seringkali lebih disukai.

### Bagian 7.1: Melewati sebuah alias

Terkadang Anda mungkin ingin melewati sebuah alias untuk sementara, tanpa menonaktifkannya. Untuk bekerja dengan contoh konkret, pertimbangkan alias ini:

```bash
alias ls='ls --color=auto'
```

Dan katakanlah Anda ingin menggunakan perintah `ls` tanpa menonaktifkan alias. Anda memiliki beberapa opsi:

  * Gunakan `builtin` `command`: `command ls`
  * Gunakan path lengkap dari perintah: `/bin/ls`
  * Tambahkan `\` di mana saja dalam nama perintah, misalnya: `\ls`, atau `l\s`
  * Beri tanda kutip pada perintah: `"ls"` atau `'ls'`

### Bagian 7.2: Membuat Alias

```bash
alias kata='perintah'
```

Memanggil `kata` akan menjalankan `perintah`. Argumen apa pun yang diberikan ke alias hanya ditambahkan ke target alias:

```bash
alias myAlias='some command --with --options'
myAlias foo bar baz
```

Shell kemudian akan mengeksekusi:

```bash
some command --with --options foo bar baz
```

Untuk menyertakan beberapa perintah dalam alias yang sama, Anda dapat merangkainya bersama dengan `&&`. Sebagai contoh:

```bash
alias print_things='echo "foo" && echo "bar" && echo "baz"'
```

### Bagian 7.3: Menghapus sebuah alias

Untuk menghapus alias yang ada, gunakan:

```bash
unalias {nama_alias}
```

Contoh:

```bash
# membuat sebuah alias
$ alias now='date'

# melihat pratinjau alias
$ now
Thu Jul 21 17:11:25 CEST 2016

# menghapus alias
$ unalias now

# tes jika sudah terhapus
$ now
-bash: now: command not found
```

### Bagian 7.4: BASH\_ALIASES adalah array asosiatif internal bash

Alias adalah pintasan bernama dari perintah, yang dapat didefinisikan dan digunakan dalam instance bash interaktif. Mereka disimpan dalam array asosiatif bernama `BASH_ALIASES`. Untuk menggunakan variabel ini dalam skrip, skrip tersebut harus dijalankan di dalam shell interaktif.

```bash
#!/bin/bash -li
# perhatikan -li di atas! -l membuatnya berperilaku seperti login shell
# -i membuatnya berperilaku seperti shell interaktif
#
# shopt -s expand_aliases tidak akan berfungsi dalam banyak kasus

echo Ada ${#BASH_ALIASES[*]} alias yang didefinisikan.

for ali in "${!BASH_ALIASES[@]}"; do
    printf "alias: %-10s memicu: %s\n" "$ali" "${BASH_ALIASES[$ali]}"
done
```

### Bagian 7.5: Memperluas alias

Dengan asumsi bahwa `bar` adalah alias untuk `someCommand -flag1`.

Ketik `bar` di baris perintah lalu tekan `Ctrl` + `alt` + `e`.

Anda akan mendapatkan `someCommand -flag1` di tempat `bar` berada.

### Bagian 7.6: Mendaftar semua Alias

```bash
alias -p
```

akan mendaftar semua alias saat ini.

---

# Bab 8
## Jobs dan Proses

### Bagian 8.1: Penanganan job

**Membuat jobs**

Untuk membuat sebuah *job*, cukup tambahkan satu `&` setelah perintah:

```bash
$ sleep 10 &
[1] 20024
```

Anda juga dapat membuat proses yang sedang berjalan menjadi sebuah *job* dengan menekan `Ctrl + z`:

```bash
$ sleep 10
^Z
[1]+  Dihentikan              sleep 10
```

**Memindahkan proses ke background dan foreground**

Untuk membawa Proses ke *foreground*, perintah `fg` digunakan bersama dengan `%`.

```bash
$ sleep 10 &
[1] 20024
$ fg %1
sleep 10
```

Sekarang Anda dapat berinteraksi dengan proses tersebut. Untuk membawanya kembali ke *background*, Anda dapat menggunakan perintah `bg`. Karena sesi terminal yang sedang digunakan, Anda perlu menghentikan proses terlebih dahulu dengan menekan `Ctrl + z`.

```bash
$ sleep 10
^Z
[1]+  Dihentikan              sleep 10
$ bg %1
[1]+  sleep 10 &
```

Karena kemalasan beberapa Programmer, semua perintah ini juga berfungsi dengan satu `%` jika hanya ada satu proses, atau untuk proses pertama dalam daftar. Contohnya:

```bash
$ sleep 10 &
[1] 20024
$ fg %
sleep 10
# untuk membawa proses ke foreground, 'fg %' juga berfungsi.
```

atau cukup

```bash
$ %
sleep 10
# kemalasan tidak mengenal batas, '%' juga berfungsi.
```

Selain itu, hanya mengetik `fg` atau `bg` tanpa argumen apa pun akan menangani *job* terakhir:

```bash
$ sleep 20 &
$ sleep 10 &
$ fg
sleep 10
^C
$ fg
sleep 20
```

**Menghentikan jobs yang sedang berjalan**

```bash
$ sleep 10 &
[1] 20024
$ kill %1
[1]+  Terminated              sleep 10
```

Proses `sleep` berjalan di *background* dengan id proses (pid) `20024` dan nomor *job* `1`. Untuk merujuk ke proses tersebut, Anda dapat menggunakan pid atau nomor *job*. Jika Anda menggunakan nomor *job*, Anda harus mengawalinya dengan `%`. Sinyal *kill* default yang dikirim oleh `kill` adalah `SIGTERM`, yang memungkinkan proses target untuk keluar secara baik-baik.

Beberapa sinyal *kill* yang umum ditunjukkan di bawah ini. Untuk melihat daftar lengkap, jalankan `kill -l`.

| Nama Sinyal | Nilai Sinyal | Efek |
| :--- | :--- | :--- |
| `SIGHUP` | 1 | Hangup |
| `SIGINT` | 2 | Interupsi dari keyboard |
| `SIGKILL` | 9 | Sinyal Kill (paksa berhenti) |
| `SIGTERM` | 15 | Sinyal Terminasi |

**Memulai dan menghentikan proses spesifik**

Mungkin cara termudah untuk menghentikan proses yang sedang berjalan adalah dengan memilihnya melalui nama proses seperti pada contoh berikut menggunakan perintah `pkill`:

```bash
pkill -f test.py
```

(atau) cara yang lebih aman menggunakan `pgrep` untuk mencari id-proses yang sebenarnya

```bash
kill $(pgrep -f 'python test.py')
```

Hasil yang sama dapat diperoleh dengan menggunakan `grep` pada `ps -ef | grep nama_proses` lalu menghentikan proses yang terkait dengan pid (id proses) yang dihasilkan. Memilih proses menggunakan namanya nyaman di lingkungan pengujian tetapi bisa sangat berbahaya ketika skrip digunakan di produksi: hampir tidak mungkin untuk memastikan bahwa nama tersebut akan cocok dengan proses yang sebenarnya ingin Anda hentikan. Dalam kasus tersebut, pendekatan berikut sebenarnya jauh lebih aman.

Mulai skrip yang pada akhirnya akan dihentikan dengan pendekatan berikut. Mari kita asumsikan bahwa perintah yang ingin Anda eksekusi dan akhirnya hentikan adalah `python test.py`.

```bash
#!/bin/bash
if [[ ! -e /tmp/test.py.pid ]]; then
    # Periksa apakah file sudah ada
    python test.py &
    #+dan jika ya, jangan jalankan proses lain.
    echo $! > /tmp/test.py.pid
else
    echo -n "ERROR: Proses sudah berjalan dengan pid "
    cat /tmp/test.py.pid
    echo
fi
```

Ini akan membuat file di direktori `/tmp` yang berisi pid dari proses `python test.py`. Jika file sudah ada, kita berasumsi bahwa perintah sudah berjalan dan skrip mengembalikan kesalahan.

Kemudian, ketika Anda ingin menghentikannya, gunakan skrip berikut:

```bash
#!/bin/bash
if [[ -e /tmp/test.py.pid ]]; then
    kill `cat /tmp/test.py.pid`
    rm /tmp/test.py.pid
else
    echo "test.py tidak berjalan"
fi
# Jika file tidak ada, maka proses
#+tidak berjalan. Tidak ada gunanya
#+mencoba menghentikannya.
```

Ini akan menghentikan persis proses yang terkait dengan perintah Anda, tanpa bergantung pada informasi yang mudah berubah (seperti string yang digunakan untuk menjalankan perintah). Bahkan dalam kasus ini jika file tidak ada, skrip mengasumsikan bahwa Anda ingin menghentikan proses yang tidak berjalan.

Contoh terakhir ini dapat dengan mudah ditingkatkan untuk menjalankan perintah yang sama beberapa kali (menambahkan ke file pid alih-alih menimpanya, misalnya) dan untuk mengelola kasus di mana proses mati sebelum dihentikan.

### Bagian 8.2: Memeriksa proses mana yang berjalan di port spesifik

Untuk memeriksa proses mana yang berjalan di port `8080`:

```bash
lsof -i :8080
```

### Bagian 8.3: Melepaskan job background

```bash
$ gzip extremelylargefile.txt &
$ bg
$ disown %1
```

Ini memungkinkan proses yang berjalan lama untuk terus berlanjut setelah shell Anda (terminal, ssh, dll) ditutup.

### Bagian 8.4: Mendaftar Jobs Saat Ini

```bash
$ tail -f /var/log/syslog > log.txt
^Z
[1]+  Dihentikan              tail -f /var/log/syslog > log.txt
$ sleep 10 &
$ jobs
[1]+  Dihentikan              tail -f /var/log/syslog > log.txt
[2]-  Berjalan                sleep 10 &
```

### Bagian 8.5: Menemukan informasi tentang proses yang berjalan

`ps aux | grep <istilah-pencarian>` menunjukkan proses yang cocok dengan istilah pencarian.

Contoh:

```
root@server7:~# ps aux | grep nginx
root      315  0.0  0.3 144392  1020 ?        Ss   May28   0:00 nginx: master process /usr/sbin/nginx
www-data 5647  0.0  1.1 145124  3048 ?        S    Jul18   2:53 nginx: worker process
www-data 5648  0.0  0.1 144392   376 ?        S    Jul18   0:00 nginx: cache manager process
root     13134 0.0  0.3   4960   920 pts/0    S+   14:33   0:00 grep --color=auto nginx
root@server7:~#
```

Di sini, kolom kedua adalah id proses. Misalnya, jika Anda ingin menghentikan proses nginx, Anda dapat menggunakan perintah `kill 5647`. Selalu disarankan untuk menggunakan perintah `kill` dengan `SIGTERM` daripada `SIGKILL`.

### Bagian 8.6: Mendaftar semua proses

Ada dua cara umum untuk mendaftar semua proses pada sistem. Keduanya mendaftar semua proses yang berjalan oleh semua pengguna, meskipun keduanya berbeda dalam format outputnya (alasan perbedaannya bersifat historis).

```bash
ps -ef    # mendaftar semua proses
ps aux    # mendaftar semua proses dalam format alternatif (BSD)
```

Ini dapat digunakan untuk memeriksa apakah aplikasi tertentu sedang berjalan. Misalnya, untuk memeriksa apakah server SSH (`sshd`) sedang berjalan:

```bash
ps -ef | grep sshd
```
---

# Bab 9
## Pengalihan (Redirection)

| Parameter | Detail |
| :--- | :--- |
| deskriptor file internal | Sebuah integer. |
| arah | Salah satu dari `>`, `<`, atau `<>`. |
| deskriptor file eksternal atau path | `&` diikuti oleh integer untuk deskriptor file atau sebuah path. |

### Bagian 9.1: Mengalihkan output standar

`>` mengalihkan output standar (alias STDOUT) dari perintah saat ini ke dalam file atau deskriptor lain.

Contoh-contoh ini menulis output dari perintah `ls` ke dalam file `file.txt`.

```bash
ls >file.txt
> file.txt ls
```

File target dibuat jika belum ada, jika tidak, isi file ini akan dipotong (*truncated*).

Deskriptor pengalihan default adalah output standar atau `1` ketika tidak ada yang ditentukan. Perintah ini setara dengan contoh sebelumnya dengan output standar yang ditunjukkan secara eksplisit:

```bash
ls 1>file.txt
```

Catatan: pengalihan diinisialisasi oleh shell yang dieksekusi dan bukan oleh perintah yang dieksekusi, oleh karena itu hal ini dilakukan sebelum eksekusi perintah.

### Bagian 9.2: Menambahkan (Append) vs Memotong (Truncate)

**Memotong `>`**

1.  Buat file yang ditentukan jika tidak ada.
2.  Potong (hapus konten file).
3.  Tulis ke file.

<!-- end list -->

```bash
$ echo "first line" > /tmp/lines
$ echo "second line" > /tmp/lines
$ cat /tmp/lines
second line
```

**Menambahkan `>>`**

1.  Buat file yang ditentukan jika tidak ada.
2.  Tambahkan ke file (menulis di akhir file).

<!-- end list -->

```bash
# Timpa file yang ada
$ echo "first line" > /tmp/lines
# Tambahkan baris kedua
$ echo "second line" >> /tmp/lines
$ cat /tmp/lines
first line
second line
```

### Bagian 9.3: Mengalihkan STDOUT dan STDERR sekaligus

Deskriptor file seperti `0` dan `1` adalah pointer. Kita mengubah ke mana deskriptor file menunjuk dengan pengalihan. `>/dev/null` berarti `1` menunjuk ke `/dev/null`.

Pertama kita arahkan `1` (STDOUT) ke `/dev/null` lalu arahkan `2` (STDERR) ke mana pun `1` menunjuk.

```bash
# STDERR dialihkan ke STDOUT: yang dialihkan ke /dev/null,
# secara efektif mengalihkan baik STDERR maupun STDOUT ke /dev/null
echo 'hello' > /dev/null 2>&1
```

**Versi ≥ 4.0**

Ini dapat dipersingkat lebih lanjut menjadi berikut:

```bash
echo 'hello' &> /dev/null
```

Namun, bentuk ini mungkin tidak diinginkan dalam produksi jika kompatibilitas shell menjadi perhatian karena bertentangan dengan POSIX, menimbulkan ambiguitas parsing, dan shell tanpa fitur ini akan salah menafsirkannya:

```bash
# Kode aktual
echo 'hello' &> /dev/null
echo 'hello' &> /dev/null 'goodbye'

# Perilaku yang diinginkan
echo 'hello' > /dev/null 2>&1
echo 'hello' 'goodbye' > /dev/null 2>&1

# Perilaku aktual
echo 'hello' &
echo 'hello' & goodbye > /dev/null
```

CATATAN: `&>` diketahui berfungsi seperti yang diinginkan di Bash dan Zsh.

### Bagian 9.4: Menggunakan pipe bernama

Terkadang Anda mungkin ingin mengeluarkan sesuatu oleh satu program dan memasukkannya ke program lain, tetapi tidak dapat menggunakan *pipe* standar.

```bash
ls -l | grep ".log"
```

Anda bisa saja menulis ke file sementara:

```bash
touch tempFile.txt
ls -l > tempFile.txt
grep ".log" < tempFile.txt
```

Ini berfungsi dengan baik untuk sebagian besar aplikasi, namun, tidak ada yang akan tahu apa fungsi `tempFile` dan seseorang mungkin menghapusnya jika berisi output dari `ls -l` di direktori itu. Di sinilah *pipe* bernama berperan:

```bash
mkfifo myPipe
ls -l > myPipe
grep ".log" < myPipe
```

`myPipe` secara teknis adalah file (semuanya adalah file di Linux), jadi mari kita lakukan `ls -l` di direktori kosong tempat kita baru saja membuat *pipe*:

```bash
mkdir pipeFolder
cd pipeFolder
mkfifo myPipe
ls -l
```

Outputnya adalah:

```
prw-r--r-- 1 root root 0 Jul 25 11:20 myPipe
```

Perhatikan karakter pertama dalam izin akses, itu terdaftar sebagai *pipe*, bukan file.

Sekarang mari kita lakukan sesuatu yang keren.
Buka satu terminal, dan catat direktorinya (atau buat satu agar pembersihan mudah), dan buat *pipe*.

```bash
mkfifo myPipe
```

Sekarang mari kita masukkan sesuatu ke dalam *pipe*.

```bash
echo "Hello from the other side" > myPipe
```

Anda akan melihat ini menggantung, sisi lain dari *pipe* masih tertutup. Mari kita buka sisi lain dari *pipe* dan biarkan isinya lewat.

Buka terminal lain dan pergi ke direktori tempat *pipe* berada (atau jika Anda tahu lokasinya, awali nama *pipe* dengan pathnya):

```bash
cat < myPipe
```

Anda akan melihat bahwa setelah `Hello from the other side` ditampilkan, program di terminal pertama selesai, begitu juga program di terminal kedua.

Sekarang jalankan perintah secara terbalik. Mulai dengan `cat < myPipe` dan kemudian `echo` sesuatu ke dalamnya. Ini masih berfungsi, karena sebuah program akan menunggu sampai sesuatu dimasukkan ke dalam *pipe* sebelum berakhir, karena ia tahu ia harus mendapatkan sesuatu.

*Pipe* bernama bisa berguna untuk memindahkan informasi antar terminal atau antar program.

*Pipe* berukuran kecil. Setelah penuh, penulis akan memblokir sampai beberapa pembaca membaca isinya, jadi Anda perlu menjalankan pembaca dan penulis di terminal yang berbeda atau menjalankan salah satunya di *background*:

```bash
ls -l /tmp > myPipe &
cat < myPipe
```

Contoh lain menggunakan *pipe* bernama:

**Contoh 1 - semua perintah di terminal / shell yang sama**

```bash
$ { ls -l && cat file3; } >mypipe &
$ cat <mypipe
# Output: Mencetak data ls -l dan kemudian mencetak isi file3 di layar
```

**Contoh 2 - semua perintah di terminal / shell yang sama**

```bash
$ ls -l >mypipe &
$ cat file3 >mypipe &
$ cat <mypipe
#Output: Ini mencetak isi mypipe di layar.
```

Perhatikan bahwa isi `file3` ditampilkan terlebih dahulu dan kemudian data `ls -l` ditampilkan (konfigurasi LIFO).

**Contoh 3 - semua perintah di terminal / shell yang sama**

```bash
$ { pipedata=$(<mypipe) && echo "$pipedata"; } &
$ ls >mypipe
# Output: Mencetak output dari ls langsung di layar
```

Perhatikan bahwa variabel `$pipedata` tidak tersedia untuk digunakan di terminal utama / shell utama karena penggunaan `&` memanggil *subshell* dan `$pipedata` hanya tersedia di *subshell* ini.

**Contoh 4 - semua perintah di terminal / shell yang sama**

```bash
$ export pipedata
$ pipedata=$(<mypipe) &
$ ls -l *.sh >mypipe
$ echo "$pipedata"
#Output : Mencetak dengan benar isi dari mypipe
```

Ini mencetak dengan benar nilai variabel `$pipedata` di shell utama karena deklarasi `export` dari variabel tersebut. Terminal utama/shell utama tidak menggantung karena pemanggilan shell *background* (`&`).

### Bagian 9.5: Pengalihan ke alamat jaringan

**Versi ≥ 2.04**

Bash memperlakukan beberapa path sebagai sesuatu yang istimewa dan dapat melakukan beberapa komunikasi jaringan dengan menulis ke `/dev/{udp|tcp}/host/port`. Bash tidak dapat menyiapkan server pendengar, tetapi dapat memulai koneksi, dan untuk TCP setidaknya dapat membaca hasilnya.

Sebagai contoh, untuk mengirim permintaan web sederhana, seseorang dapat melakukan:

```bash
exec 3</dev/tcp/www.google.com/80
printf 'GET / HTTP/1.0\r\n\r\n' >&3
cat <&3
```

dan hasil dari halaman web default [www.google.com](https://www.google.com) akan dicetak ke stdout.

Demikian pula:

```bash
printf 'HI\n' >/dev/udp/192.168.1.1/6666
```

akan mengirim pesan UDP berisi `HI\n` ke pendengar di `192.168.1.1:6666`.

### Bagian 9.6: Mencetak pesan kesalahan ke stderr

Pesan kesalahan umumnya disertakan dalam skrip untuk tujuan *debugging* atau untuk memberikan pengalaman pengguna yang kaya.

Hanya menulis pesan kesalahan seperti ini:

```bash
cmd || echo 'cmd failed'
```

mungkin berfungsi untuk kasus sederhana tetapi itu bukan cara yang biasa. Dalam contoh ini, pesan kesalahan akan mencemari output aktual dari skrip dengan mencampur kesalahan dan output yang berhasil di stdout.

Singkatnya, pesan kesalahan harus masuk ke stderr bukan stdout. Cukup sederhana:

```bash
cmd || echo 'cmd failed' >/dev/stderr
```

Contoh lain:

```bash
if cmd; then
    echo 'success'
else
    echo 'cmd failed' >/dev/stderr
fi
```

Dalam contoh di atas, pesan sukses akan dicetak di stdout sementara pesan kesalahan akan dicetak di stderr.

Cara yang lebih baik untuk mencetak pesan kesalahan adalah dengan mendefinisikan sebuah fungsi:

```bash
err(){
    echo "E: $*" >>/dev/stderr
}
```

Sekarang, ketika Anda harus mencetak kesalahan:

```bash
err "My error message"
```

### Bagian 9.7: Mengalihkan beberapa perintah ke file yang sama

```bash
{
  echo "contents of home directory"
  ls ~
} > output.txt
```

### Bagian 9.8: Mengalihkan STDIN

`<` membaca dari argumen kanannya dan menulis ke argumen kirinya.
Untuk menulis file ke STDIN kita harus membaca `/tmp/a_file` dan menulis ke STDIN yaitu `0</tmp/a_file`.

Catatan: Deskriptor file internal defaultnya adalah `0` (STDIN) untuk `<`.

```bash
$ echo "b" > /tmp/list.txt
$ echo "a" >> /tmp/list.txt
$ echo "c" >> /tmp/list.txt
$ sort < /tmp/list.txt
a
b
c
```

### Bagian 9.9: Mengalihkan STDERR

`2` adalah STDERR.

```bash
$ echo_to_stderr 2>/dev/null # tidak menampilkan apa-apa
```

Definisi:
`echo_to_stderr` adalah perintah yang menulis "stderr" ke STDERR.

```bash
echo_to_stderr () {
    echo stderr >&2
}
$ echo_to_stderr
stderr
```

### Bagian 9.10: Penjelasan STDIN, STDOUT, dan STDERR

Perintah memiliki satu input (STDIN) dan dua jenis output, output standar (STDOUT) dan error standar (STDERR).

Sebagai contoh:

**STDIN**

```
root@server~# read
Ketik beberapa teks di sini
```

Input standar digunakan untuk memberikan input ke sebuah program. (Di sini kita menggunakan *builtin* `read` untuk membaca baris dari STDIN.)

**STDOUT**

```
root@server~# ls file
file
```

Output standar umumnya digunakan untuk output "normal" dari sebuah perintah. Misalnya, `ls` mendaftar file, jadi daftar file dikirim ke STDOUT.

**STDERR**

```
root@server~# ls anotherfile
ls: cannot access 'anotherfile': No such file or directory
```

Error standar (seperti namanya) digunakan untuk pesan kesalahan. Karena pesan ini bukan daftar file, ia dikirim ke STDERR.

STDIN, STDOUT, dan STDERR adalah tiga aliran standar. Mereka diidentifikasi ke shell oleh nomor daripada nama:

  * `0` = Standard in (Input Standar)
  * `1` = Standard out (Output Standar)
  * `2` = Standard error (Error Standar)

Secara default, STDIN terhubung ke keyboard, dan baik STDOUT maupun STDERR muncul di terminal. Namun, kita dapat mengalihkan STDOUT atau STDERR ke mana pun yang kita butuhkan. Misalnya, katakanlah Anda hanya memerlukan output standar dan semua pesan kesalahan yang dicetak di error standar harus diabaikan. Saat itulah kita menggunakan deskriptor `1` dan `2`.

**Mengalihkan STDERR ke /dev/null**

Mengambil contoh sebelumnya,

```
root@server~# ls anotherfile 2>/dev/null
root@server~#
```

Dalam kasus ini, jika ada STDERR, itu akan dialihkan ke `/dev/null` (file khusus yang mengabaikan apa pun yang dimasukkan ke dalamnya), jadi Anda tidak akan mendapatkan output kesalahan apa pun di shell.

---

# Bab 10
## Struktur Kontrol

**Parameter untuk `[` atau `test`**

**Operator File**

| Detail | Detail |
| :--- | :--- |
| `-e "$file"` | Mengembalikan *true* jika file ada. |
| `-d "$file"` | Mengembalikan *true* jika file ada dan merupakan sebuah direktori. |
| `-f "$file"` | Mengembalikan *true* jika file ada dan merupakan file reguler. |
| `-h "$file"` | Mengembalikan *true* jika file ada dan merupakan *symbolic link*. |

**Pembanding String**

| Detail | Detail |
| :--- | :--- |
| `-z "$str"` | *True* jika panjang string adalah nol. |
| `-n "$str"` | *True* jika panjang string bukan nol. |
| `"$str" = "$str2"` | *True* jika string `$str` sama dengan string `$str2`. Bukan yang terbaik untuk integer. Mungkin berfungsi tetapi akan tidak konsisten. |
| `"$str" != "$str2"` | *True* jika string tidak sama. |

**Pembanding Integer**

| Detail | Detail |
| :--- | :--- |
| `"$int1" -eq "$int2"` | *True* jika integer sama. |
| `"$int1" -ne "$int2"` | *True* jika integer tidak sama. |
| `"$int1" -gt "$int2"` | *True* jika `int1` lebih besar dari `int2`. |
| `"$int1" -ge "$int2"` | *True* jika `int1` lebih besar atau sama dengan `int2`. |
| `"$int1" -lt "$int2"` | *True* jika `int1` lebih kecil dari `int2`. |
| `"$int1" -le "$int2"` | *True* jika `int1` lebih kecil atau sama dengan `int2`. |

### Bagian 10.1: Eksekusi kondisional daftar perintah

**Cara menggunakan eksekusi kondisional daftar perintah**

Setiap perintah *builtin*, ekspresi, atau fungsi, serta perintah atau skrip eksternal apa pun dapat dieksekusi secara kondisional menggunakan operator `&&` (dan) dan `||` (atau).

Sebagai contoh, ini hanya akan mencetak direktori saat ini jika perintah `cd` berhasil.

```bash
cd my_directory && pwd
```

Demikian pula, ini akan keluar jika perintah `cd` gagal, mencegah bencana:

```bash
cd my_directory || exit
rm -rf *
```

Saat menggabungkan beberapa pernyataan dengan cara ini, penting untuk diingat bahwa (tidak seperti banyak bahasa bergaya C) operator ini tidak memiliki preseden dan bersifat asosiatif kiri.

Jadi, pernyataan ini akan berfungsi seperti yang diharapkan...

```bash
cd my_directory && pwd || echo "No such directory"
```

Jika `cd` berhasil, `&& pwd` dieksekusi dan nama direktori kerja saat ini dicetak. Kecuali jika `pwd` gagal (jarang terjadi), `|| echo ...` tidak akan dieksekusi.
Jika `cd` gagal, `&& pwd` akan dilewati dan `|| echo ...` akan dijalankan.

Tetapi ini tidak akan (jika Anda berpikir if...then...else)...

```bash
cd my_directory && ls || echo "No such directory"
```

Jika `cd` gagal, `&& ls` dilewati dan `|| echo ...` dieksekusi.
Jika `cd` berhasil, `&& ls` dieksekusi.
Jika `ls` berhasil, `|| echo ...` diabaikan. (sejauh ini bagus)
TAPI... jika `ls` gagal, `|| echo ...` juga akan dieksekusi.
Ini adalah `ls`, bukan `cd`, yang merupakan perintah sebelumnya.

**Mengapa menggunakan eksekusi kondisional daftar perintah**

Eksekusi kondisional sedikit lebih cepat daripada `if...then` tetapi keuntungan utamanya adalah memungkinkan fungsi dan skrip untuk keluar lebih awal, atau "hubungan pendek" (*short circuit*).

Tidak seperti banyak bahasa seperti C di mana memori secara eksplisit dialokasikan untuk *struct* dan variabel dan sejenisnya (dan dengan demikian harus dibatalkan alokasinya), bash menangani ini di balik layar. Dalam kebanyakan kasus, kita tidak perlu membersihkan apa pun sebelum meninggalkan fungsi. Pernyataan `return` akan membatalkan alokasi semua yang bersifat lokal untuk fungsi dan melanjutkan eksekusi di alamat kembali pada *stack*.

Kembali dari fungsi atau keluar dari skrip sesegera mungkin dengan demikian dapat secara signifikan meningkatkan kinerja dan mengurangi beban sistem dengan menghindari eksekusi kode yang tidak perlu. Sebagai contoh...

```bash
my_function () {
    ### SELALU PERIKSA KODE KEMBALIAN
    # satu argumen diperlukan. "" dievaluasi sebagai false(1)
    [[ "$1" ]] \
        || return 1
    # bekerja dengan argumen. keluar jika gagal
    do_something_with "$1" || return 1
    do_something_else \
        || return 1
    # Sukses! tidak ada kegagalan yang terdeteksi, atau kita tidak akan berada di sini
    return 0
}
```

### Bagian 10.2: Pernyataan If

```bash
if [[ $1 -eq 1 ]]; then
    echo "1 dilewatkan pada parameter pertama"
elif [[ $1 -gt 2 ]]; then
    echo "2 tidak dilewatkan pada parameter pertama"
else
    echo "Parameter pertama bukan 1 dan tidak lebih dari 2."
fi
```

Penutup `fi` diperlukan, tetapi klausa `elif` dan/atau `else` dapat dihilangkan.

Titik koma sebelum `then` adalah sintaks standar untuk menggabungkan dua perintah pada satu baris; titik koma dapat dihilangkan hanya jika `then` dipindahkan ke baris berikutnya.

Penting untuk dipahami bahwa kurung siku `[[` bukan bagian dari sintaks, tetapi diperlakukan sebagai perintah; adalah kode keluar dari perintah ini yang sedang diuji. Oleh karena itu, Anda harus selalu menyertakan spasi di sekitar kurung siku.

Ini juga berarti bahwa hasil dari perintah apa pun dapat diuji. Jika kode keluar dari perintah adalah nol, pernyataan dianggap benar.

```bash
if grep "foo" bar.txt; then
    echo "foo ditemukan"
else
    echo "foo tidak ditemukan"
fi
```

Ekspresi matematika, ketika ditempatkan di dalam kurung ganda, juga mengembalikan `0` atau `1` dengan cara yang sama, dan juga dapat diuji:

```bash
if (( $1 + 5 > 91 )); then
    echo "$1 lebih besar dari 86"
fi
```

Anda mungkin juga menemukan pernyataan `if` dengan kurung siku tunggal. Ini didefinisikan dalam standar POSIX dan dijamin berfungsi di semua shell yang sesuai dengan POSIX termasuk Bash. Sintaksnya sangat mirip dengan yang ada di Bash:

```bash
if [ "$1" -eq 1 ]; then
    echo "1 dilewatkan pada parameter pertama"
elif [ "$1" -gt 2 ]; then
    echo "2 tidak dilewatkan pada parameter pertama"
else
    echo "Parameter pertama bukan 1 dan tidak lebih dari 2."
fi
```

### Bagian 10.3: Melakukan Looping pada Array

**for loop:**

```bash
arr=(a b c d e f)
for i in "${arr[@]}";do
    echo "$i"
done
```

Atau

```bash
for ((i=0;i<${#arr[@]};i++));do
    echo "${arr[$i]}"
done
```

**while loop:**

```bash
i=0
while [ $i -lt ${#arr[@]} ];do
    echo "${arr[$i]}"
    i=$(expr $i + 1)
done
```

Atau

```bash
i=0
while (( $i < ${#arr[@]} ));do
    echo "${arr[$i]}"
    ((i++))
done
```

### Bagian 10.4: Menggunakan For Loop untuk Iterasi Angka

```bash
#! /bin/bash
for i in {1..10}; do # {1..10} diekspansi menjadi "1 2 3 4 5 6 7 8 9 10"
    echo $i
done
```

Ini menghasilkan output berikut:

```
1
2
3
4
5
6
7
8
9
10
```

### Bagian 10.5: continue dan break

**Contoh untuk `continue`**

```bash
for i in [series]
do
    perintah 1
    perintah 2
    if (kondisi) # Kondisi untuk melompati perintah 3
        continue # lanjut ke nilai berikutnya dalam "series"
    fi
    perintah 3
done
```

**Contoh untuk `break`**

```bash
for i in [series]
do
    perintah 4
    if (kondisi) # Kondisi untuk menghentikan loop
    then
        perintah 5 # Perintah jika loop perlu dihentikan
        break
    fi
    perintah 6 # Perintah untuk dijalankan jika "kondisi" tidak pernah benar
done
```

### Bagian 10.6: Menghentikan Loop (break)

**Menghentikan beberapa loop:**

```bash
arr=(a b c d e f)
for i in "${arr[@]}";do
    echo "$i"
    for j in "${arr[@]}";do
        echo "$j"
        break 2
    done
done
```

Output:

```
a
a
```

**Menghentikan satu loop:**

```bash
arr=(a b c d e f)
for i in "${arr[@]}";do
    echo "$i"
    for j in "${arr[@]}";do
        echo "$j"
        break
    done
done
```

Output:

```
a
a
b
a
c
a
d
a
e
a
f
a
```

### Bagian 10.7: While Loop

```bash
#! /bin/bash
i=0
while [ $i -lt 5 ] # Selama i lebih kecil dari 5
do
    echo "i saat ini adalah $i"
    i=$[$i+1] # Perhatikan tidak adanya spasi di sekitar kurung siku. Ini membuatnya bukan ekspresi tes
done # mengakhiri loop
```

Perhatikan bahwa ada spasi di sekitar kurung siku selama tes (setelah pernyataan `while`). Spasi ini diperlukan.

Loop ini menghasilkan output:

```
i saat ini adalah 0
i saat ini adalah 1
i saat ini adalah 2
i saat ini adalah 3
i saat ini adalah 4
```

### Bagian 10.8: For Loop dengan sintaks gaya-C

Format dasar dari *for loop* gaya-C adalah:
`for (( penugasan variabel; kondisi; proses iterasi ))`

Catatan:

  * Penugasan variabel di dalam *for loop* gaya-C dapat berisi spasi tidak seperti penugasan biasa.
  * Variabel di dalam *for loop* gaya-C tidak diawali dengan `$`.

Contoh:

```bash
for (( i = 0; i < 10; i++ ))
do
    echo "Nomor iterasi adalah $i"
done
```

Kita juga dapat memproses beberapa variabel di dalam *for loop* gaya-C:

```bash
for (( i = 0, j = 0; i < 10; i++, j = i * i ))
do
    echo "Kuadrat dari $i sama dengan $j"
done
```

### Bagian 10.9: Until Loop

*Until loop* dieksekusi sampai kondisi menjadi benar.

```bash
i=5
until [[ i -eq 10 ]]; do # Memeriksa apakah i=10
    echo "i=$i" # Cetak nilai i
    i=$((i+1))   # Tambah i dengan 1
done
```

Output:

```
i=5
i=6
i=7
i=8
i=9
```

Ketika `i` mencapai 10, kondisi di *until loop* menjadi benar dan loop berakhir.

### Bagian 10.10: Pernyataan Switch dengan case

Dengan pernyataan `case`, Anda dapat mencocokkan nilai terhadap satu variabel. Argumen yang dilewatkan ke `case` diperluas dan dicoba untuk dicocokkan dengan setiap pola. Jika kecocokan ditemukan, perintah hingga `;;` dieksekusi.

```bash
case "$BASH_VERSION" in
    [34]*)
        echo {1..4}
        ;;
    *)
        seq -s" " 1 4
esac
```

Pola bukanlah ekspresi reguler tetapi pencocokan pola shell (alias *globs*).

### Bagian 10.11: For Loop tanpa parameter daftar-kata

```bash
for arg; do
    echo arg=$arg
done
```

Sebuah *for loop* tanpa parameter daftar kata akan melakukan iterasi pada parameter posisional. Dengan kata lain, contoh di atas setara dengan kode ini:

```bash
for arg in "$@"; do
    echo arg=$arg
done
```

Dengan kata lain, jika Anda mendapati diri Anda menulis `for i in "$@"; do ...; done`, cukup hilangkan bagian `in`, dan tulis saja `for i; do ...; done`.

---

# Bab 11
## Perintah true, false, dan :

### Bagian 11.1: Loop Tak Terbatas (Infinite Loop)

```bash
while true; do
    echo ok
done
```

atau

```bash
while :; do
    echo ok
done
```

atau

```bash
until false; do
    echo ok
done
```

### Bagian 11.2: Pengembalian Fungsi (Function Return)

```bash
function positive() {
    return 0
}

function negative() {
    return 1
}
```

### Bagian 11.3: Kode yang akan selalu/tidak pernah dieksekusi

```bash
if true; then
    echo Selalu dieksekusi
fi

if false; then
    echo Tidak akan pernah dieksekusi
fi
```

-----

## Bab 12: Array

### Bagian 12.1: Penugasan Array

**Penugasan Daftar**

Jika Anda terbiasa dengan Perl, C, atau Java, Anda mungkin berpikir bahwa Bash akan menggunakan koma untuk memisahkan elemen array, namun ini tidak terjadi; sebaliknya, Bash menggunakan spasi:

```perl
# Array di Perl
my @array = (1, 2, 3, 4);
```

```bash
# Array di Bash
array=(1 2 3 4)
```

Buat array dengan elemen baru:
`array=('elemen pertama' 'elemen kedua' 'elemen ketiga')`

**Penugasan Subskrip**

Buat array dengan indeks elemen eksplisit:
`array=([3]='elemen keempat' [4]='elemen kelima')`

**Penugasan berdasarkan indeks**

```bash
array[0]='elemen pertama'
array[1]='elemen kedua'
```

**Penugasan berdasarkan nama (array asosiatif)**

**Versi ≥ 4.0**

```bash
declare -A array
array[first]='Elemen pertama'
array[second]='Elemen kedua'
```

**Penugasan Dinamis**

Buat array dari output perintah lain, misalnya gunakan `seq` untuk mendapatkan rentang dari 1 hingga 10:
`array=($(seq 1 10))`

Penugasan dari argumen input skrip:
`array=("$@")`

Penugasan di dalam loop:

```bash
while read -r; do
    #array+=("$REPLY")      # Tambahkan ke array
    array[$i]="$REPLY"     # Penugasan berdasarkan indeks
    let i++                # Naikkan indeks
done < <(seq 1 10)         # substitusi perintah

echo ${array[@]}
# output: 1 2 3 4 5 6 7 8 9 10
```

di mana `$REPLY` selalu merupakan input saat ini.

### Bagian 12.2: Mengakses Elemen Array

Cetak elemen di indeks 0
`echo "${array[0]}"`

**Versi \< 4.3**
Cetak elemen terakhir menggunakan sintaks ekspansi substring
`echo "${arr[@]: -1 }"`

**Versi ≥ 4.3**
Cetak elemen terakhir menggunakan sintaks subskrip
`echo "${array[-1]}"`

Cetak semua elemen, masing-masing dikutip secara terpisah
`echo "${array[@]}"`

Cetak semua elemen sebagai satu string yang dikutip
`echo "${array[*]}"`

Cetak semua elemen dari indeks 1, masing-masing dikutip secara terpisah
`echo "${array[@]:1}"`

Cetak 3 elemen dari indeks 1, masing-masing dikutip secara terpisah
`echo "${array[@]:1:3}"`

**Operasi String**

Jika merujuk pada satu elemen, operasi string diizinkan:

```bash
array=(zero one two)
echo "${array[0]:0:3}" # menghasilkan zer (karakter pada posisi 0, 1 dan 2 dalam string zero)
echo "${array[0]:1:3}" # menghasilkan ero (karakter pada posisi 1, 2 dan 3 dalam string zero)
```

jadi `${array[$i]:N:M}` menghasilkan string dari posisi ke-N (dimulai dari 0) dalam string `${array[$i]}` dengan M karakter berikutnya.

### Bagian 12.3: Modifikasi Array

**Ubah Indeks**

Inisialisasi atau perbarui elemen tertentu dalam array
`array[10]="elemen kesebelas"` \# karena dimulai dari 0

**Versi ≥ 3.1**
**Tambahkan (Append)**

Modifikasi array, menambahkan elemen ke akhir jika tidak ada subskrip yang ditentukan.
`array+=('elemen keempat' 'elemen kelima')`

Ganti seluruh array dengan daftar parameter baru.
`array=("${array[@]}" "elemen keempat" "elemen kelima")`

Tambahkan elemen di awal:
`array=("elemen baru" "${array[@]}")`

**Sisipkan (Insert)**

Sisipkan elemen pada indeks tertentu:

```bash
arr=(a b c d)
# sisipkan elemen pada indeks 2
i=2
arr=("${arr[@]:0:$i}" 'new' "${arr[@]:$i}")

echo "${arr[2]}" #output: new
```

**Hapus (Delete)**

Hapus indeks array menggunakan *builtin* `unset`:

```bash
arr=(a b c)
echo "${arr[@]}"    # menghasilkan: a b c
echo "${!arr[@]}"   # menghasilkan: 0 1 2
unset -v 'arr[1]'
echo "${arr[@]}"    # menghasilkan: a c
echo "${!arr[@]}"   # menghasilkan: 0 2
```

**Gabungkan (Merge)**

`array3=("${array1[@]}" "${array2[@]}")`
Ini juga berfungsi untuk *sparse array*.

**Pengindeksan ulang array**

Ini bisa berguna jika elemen telah dihapus dari array, atau jika Anda tidak yakin apakah ada celah dalam array. Untuk membuat ulang indeks tanpa celah:
`array=("${array[@]}")`

### Bagian 12.4: Iterasi Array

Iterasi array datang dalam dua jenis, *foreach* dan *for-loop* klasik:

```bash
a=(1 2 3 4)

# foreach loop
for y in "${a[@]}"; do
    # tindakan pada $y
    echo "$y"
done

# for-loop klasik
for ((idx=0; idx < ${#a[@]}; ++idx)); do
    # tindakan pada ${a[$idx]}
    echo "${a[$idx]}"
done
```

Anda juga dapat melakukan iterasi pada output sebuah perintah:

```bash
a=($(tr ',' ' ' <<<"a,b,c,d")) # tr dapat mengubah satu karakter menjadi karakter lain
for y in "${a[@]}"; do
    echo "$y"
done
```

### Bagian 12.5: Panjang Array

`${#array[@]}` memberikan panjang array `${array[@]}`:

```bash
array=('elemen pertama' 'elemen kedua' 'elemen ketiga')
echo "${#array[@]}" # memberikan panjang 3
```

Ini juga berfungsi dengan String dalam elemen tunggal:

```bash
echo "${#array[0]}"
# memberikan panjang string pada elemen 0: 14
```

### Bagian 12.6: Array Asosiatif

**Versi ≥ 4.0**

**Deklarasikan array asosiatif**
`declare -A aa`
Mendeklarasikan array asosiatif sebelum inisialisasi atau penggunaan adalah wajib.

**Inisialisasi elemen**
Anda dapat menginisialisasi elemen satu per satu sebagai berikut:

```bash
aa[hello]=world
aa[ab]=cd
aa["key with space"]="hello world"
```

Anda juga dapat menginisialisasi seluruh array asosiatif dalam satu pernyataan:
`aa=([hello]=world [ab]=cd ["key with space"]="hello world")`

**Akses elemen array asosiatif**
`echo ${aa[hello]}`
`# Out: world`

**Mendaftar kunci array asosiatif**
`echo "${!aa[@]}"`
`#Out: hello ab key with space`

**Mendaftar nilai array asosiatif**
`echo "${aa[@]}"`
`#Out: world cd hello world`

**Iterasi melalui kunci dan nilai array asosiatif**

```bash
for key in "${!aa[@]}"; do
    echo "Kunci: ${key}"
    echo "Nilai: ${aa[$key]}"
done
# Out:
# Kunci: hello
# Nilai: world
# Kunci: ab
# Nilai: cd
# Kunci: key with space
# Nilai: hello world
```

**Hitung elemen array asosiatif**
`echo "${#aa[@]}"`
`# Out: 3`

### Bagian 12.7: Melakukan Looping pada Array

Array contoh kita:
`arr=(a b c d e f)`

Menggunakan `for..in loop`:

```bash
for i in "${arr[@]}"; do
    echo "$i"
done
```

**Versi ≥ 2.04**
Menggunakan `for loop` gaya-C:

```bash
for ((i=0;i<${#arr[@]};i++)); do
    echo "${arr[$i]}"
done
```

Menggunakan `while loop`:

```bash
i=0
while [ $i -lt ${#arr[@]} ]; do
    echo "${arr[$i]}"
    i=$((i + 1))
done
```

**Versi ≥ 2.04**
Menggunakan `while loop` dengan kondisional numerik:

```bash
i=0
while (( $i < ${#arr[@]} )); do
    echo "${arr[$i]}"
    ((i++))
done
```

Menggunakan `until loop`:

```bash
i=0
until [ $i -ge ${#arr[@]} ]; do
    echo "${arr[$i]}"
    i=$((i + 1))
done
```

**Versi ≥ 2.04**
Menggunakan `until loop` dengan kondisional numerik:

```bash
i=0
until (( $i >= ${#arr[@]} )); do
    echo "${arr[$i]}"
    ((i++))
done
```

### Bagian 12.8: Hancurkan, Hapus, atau Batalkan Array

Untuk menghancurkan, menghapus, atau membatalkan array:
`unset array`

Untuk menghancurkan, menghapus, atau membatalkan satu elemen array:
`unset array[10]`

### Bagian 12.9: Array dari string

```bash
stringVar="Apple Orange Banana Mango"
arrayVar=(${stringVar// / })
```

Setiap spasi dalam string menunjukkan item baru dalam array yang dihasilkan.

```bash
echo ${arrayVar[0]} # akan mencetak Apple
echo ${arrayVar[3]} # akan mencetak Mango
```

Demikian pula, karakter lain dapat digunakan sebagai pembatas.

```bash
stringVar="Apple+Orange+Banana+Mango"
arrayVar=(${stringVar//+/ })
echo ${arrayVar[0]} # akan mencetak Apple
echo ${arrayVar[2]} # akan mencetak Banana
```

### Bagian 12.10: Daftar indeks yang diinisialisasi

Dapatkan daftar indeks yang diinisialisasi dalam array

```bash
$ arr[2]='second'
$ arr[10]='tenth'
$ arr[25]='twenty five'
$ echo ${!arr[@]}
2 10 25
```

### Bagian 12.11: Membaca seluruh file ke dalam array

Membaca dalam satu langkah:
`IFS=$'\n' read -r -a arr < file`

Membaca dalam sebuah loop:

```bash
arr=()
while IFS= read -r line; do
    arr+=("$line")
done
```

**Versi ≥ 4.0**
Menggunakan `mapfile` atau `readarray` (yang merupakan sinonim):

```bash
mapfile -t arr < file
readarray -t arr < file
```

### Bagian 12.12: Fungsi sisip Array (insert)

Fungsi ini akan menyisipkan elemen ke dalam array pada indeks tertentu:

```bash
insert(){
    h='
################## insert ########################
# Penggunaan:
#
    insert nama_arr indeks elemen
#
#
# Parameter:
#
    nama_arr    : Nama variabel array
#
    indeks      : Indeks untuk menyisipkan
#
    elemen      : Elemen untuk disisipkan
##################################################
'
    [[ $1 = -h ]] && { echo "$h" >/dev/stderr; return 1; }
    declare -n __arr__=$1
    # referensi ke variabel array
    i=$2
    # indeks untuk menyisipkan
    el="$3"
    # elemen untuk disisipkan

    # menangani error
    [[ ! "$i" =~ ^[0-9]+$ ]] && { echo "E: insert: indeks harus integer yang valid" >/dev/stderr;
return 1; }
    (( $i < 0 )) && { echo "E: insert: indeks tidak boleh negatif" >/dev/stderr; return 1; }

    # Sekarang sisipkan $el di $i
    __arr__=("${__arr__[@]:0:$i}" "$el" "${__arr__[@]:$i}")
}
```

**Penggunaan:**

`insert nama_variabel_array indeks elemen`

**Contoh:**

```bash
arr=(a b c d)
echo "${arr[2]}" # output: c

# Sekarang panggil fungsi insert dan berikan nama variabel array,
# indeks untuk menyisipkan
# dan elemen yang akan disisipkan
insert arr 2 'Elemen Baru'

# 'Elemen Baru' disisipkan pada indeks 2 di arr, sekarang cetak mereka
echo "${arr[2]}" # output: Elemen Baru
echo "${arr[3]}" # output: c
```

---

# Bab 13
## Array asosiatif

### Bagian 13.1: Memeriksa array asosiatif

Semua penggunaan yang diperlukan ditunjukkan dengan cuplikan ini:

```bash
#!/usr/bin/env bash

declare -A assoc_array=([key_string]=value \
[one]="something" \
[two]="another thing" \
[ three ]='perhatikan spasinya!' \
[ " four" ]='hitung spasi dari kunci ini nanti!' \
[IMPORTANT]='SPASI ITU BERPENGARUH!!!' \
[1]='tidak ada integer!' \
[info]="untuk menghindari ekspansi histori " \
[info2]="beri tanda kutip pada tanda seru dengan kutip tunggal" \
)

echo # hanya baris kosong
echo sekarang ini adalah nilai dari assoc_array:
echo ${assoc_array[@]}
echo tidak begitu berguna,
echo # hanya baris kosong
echo ini lebih baik:
declare -p assoc_array
# -p == print
echo perhatikan baik-baik spasi di atas\!\!\!
echo # hanya baris kosong
echo mengakses kunci
echo kunci di assoc_array adalah ${!assoc_array[*]}
echo perhatikan penggunaan operator indireksi \!
echo # hanya baris kosong
echo sekarang kita melakukan loop pada assoc_array baris per baris
echo perhatikan operator indireksi \! yang bekerja secara berbeda,
echo jika digunakan dengan assoc_array.
echo # hanya baris kosong
for key in "${!assoc_array[@]}"; do # mengakses kunci menggunakan indireksi ! !!!!
    printf "kunci: \"%s\"\nnilai: \"%s\"\n\n" "$key" "${assoc_array[$key]}"
done
echo perhatikan baik-baik spasi dalam entri dengan kunci two, three dan four di atas\!\!\!
echo # hanya baris kosong
echo # hanya baris kosong lagi
echo ada perbedaan menggunakan integer sebagai kunci\!\!\!
i=1
echo mendeklarasikan var integer i=1
echo # hanya baris kosong
echo Di dalam sebuah integer_array, bash mengenali konteks aritmatika.
echo Di dalam sebuah assoc_array, bash TIDAK mengenali konteks aritmatika.
echo # hanya baris kosong
echo ini berfungsi: \${assoc_array[\$i]}: ${assoc_array[$i]}
echo ini TIDAK!!: \${assoc_array[i]}: ${assoc_array[i]}
echo # hanya baris kosong
echo # hanya baris kosong lagi
echo sebuah \${assoc_array[i]} memiliki konteks string di dalam kurung kurawal berbeda dengan integer_array
declare -i integer_array=( one two three )
echo "melakukan: declare -i integer_array=( one two three )"
echo # hanya baris kosong
echo kedua bentuk berfungsi: \${integer_array[i]} : ${integer_array[i]}
echo dan ini juga: \${integer_array[\$i]} : ${integer_array[$i]}
```
---

# Bab 14
## Fungsi

### Bagian 14.1: Fungsi dengan argumen

Dalam `helloJohn.sh`:

```bash
#!/bin/bash
greet() {
    local name="$1"
    echo "Hello, $name"
}

greet "John Doe"
```

```bash
# menjalankan skrip di atas
$ bash helloJohn.sh
Hello, John Doe
```

1.  Jika Anda tidak memodifikasi argumen dengan cara apa pun, tidak perlu menyalinnya ke variabel lokal - cukup `echo "Hello, $1"`.
2.  Anda dapat menggunakan `$1`, `$2`, `$3`, dan seterusnya untuk mengakses argumen di dalam fungsi.
    **Catatan**: untuk argumen lebih dari 9, `$10` tidak akan berfungsi (bash akan membacanya sebagai `$1` dan `0`), Anda perlu melakukan `${10}`, `${11}` dan seterusnya.
3.  `$@` merujuk ke semua argumen dari sebuah fungsi:
    ```bash
    #!/bin/bash
    foo() {
        echo "$@"
    }
    foo 1 2 3 # output => 1 2 3
    ```
    **Catatan**: Anda sebaiknya hampir selalu menggunakan tanda kutip ganda di sekitar `"$@"`, seperti di sini. Menghilangkan tanda kutip akan menyebabkan shell memperluas wildcard (bahkan ketika pengguna secara khusus mengutipnya untuk menghindari itu) dan umumnya menimbulkan perilaku yang tidak diinginkan dan bahkan berpotensi masalah keamanan.
    ```bash
    foo "string with spaces;" '$HOME' "*"
    # output => string with spaces; $HOME *
    ```
4.  Untuk argumen default gunakan `${1:-default_val}`. Contoh:
    ```bash
    #!/bin/bash
    foo() {
        local val=${1:-25}
        echo "$val"
    }
    foo      # output => 25
    foo 30   # output => 30
    ```
5.  Untuk mewajibkan argumen gunakan `${var:?pesan error}`
    ```bash
    foo() {
        local val=${1:?Harus menyediakan sebuah argumen}
        echo "$val"
    }
    ```

### Bagian 14.2: Fungsi Sederhana

Dalam `helloWorld.sh`

```bash
#!/bin/bash
# Mendefinisikan sebuah fungsi greet
greet ()
{
    echo "Hello World!"
}

# Memanggil fungsi greet
greet
```

Dalam menjalankan skrip, kita melihat pesan kita

```bash
$ bash helloWorld.sh
Hello World!
```

Perhatikan bahwa melakukan `source` pada file dengan fungsi akan membuat fungsi tersebut tersedia di sesi bash Anda saat ini.

```bash
$ source helloWorld.sh
$ greet
Hello World!
# atau, yang lebih portabel, ". helloWorld.sh"
```

Anda dapat mengekspor fungsi di beberapa shell, sehingga terekspos ke proses anak.

```bash
bash -c 'greet'       # gagal
export -f greet       # ekspor fungsi; perhatikan -f
bash -c 'greet'       # sukses
```

### Bagian 14.3: Menangani flag dan parameter opsional

*Builtin* `getopts` dapat digunakan di dalam fungsi untuk menulis fungsi yang mengakomodasi *flag* dan parameter opsional. Ini tidak menimbulkan kesulitan khusus tetapi seseorang harus menangani nilai yang disentuh oleh `getopts` dengan tepat.

Sebagai contoh, kita mendefinisikan fungsi `failwith` yang menulis pesan di `stderr` dan keluar dengan kode 1 atau kode arbitrer yang diberikan sebagai parameter ke opsi `-x`:

```bash
# failwith [-x STATUS] PRINTF-LIKE-ARGV
# Gagal dengan pesan diagnostik yang diberikan
#
# Flag -x dapat digunakan untuk menyampaikan status keluar kustom,
# alih-alih nilai 1. Baris baru secara otomatis ditambahkan ke output.
failwith()
{
    local OPTIND OPTION OPTARG status
    status=1
    OPTIND=1
    while getopts 'x:' OPTION; do
        case ${OPTION} in
            x)
                status="${OPTARG}";;
            *)
                1>&2 printf 'failwith: %s: Opsi tidak didukung.\n' "${OPTION}";;
        esac
    done
    shift $(( OPTIND - 1 ))
    {
        printf 'Kegagalan: '
        printf "$@"
        printf '\n'
    } 1>&2
    exit "${status}"
}
```

Fungsi ini dapat digunakan sebagai berikut:

```bash
failwith '%s: File tidak ditemukan.' "${filename}"
failwith -x 70 'Kesalahan internal umum.'
```

dan seterusnya.

Perhatikan bahwa seperti pada `printf`, variabel tidak boleh digunakan sebagai argumen pertama. Jika pesan yang akan dicetak terdiri dari konten variabel, seseorang harus menggunakan penentu `%s` untuk mencetaknya, seperti dalam
`failwith '%s' "${message}"`

### Bagian 14.4: Mencetak definisi fungsi

```bash
getfunc() {
    declare -f "$@"
}

function func(){
    echo "Saya adalah fungsi contoh"
}

funcd="$(getfunc func)"
getfunc func # atau echo "$funcd"
```

Output:

```
func ()
{
    echo "Saya adalah fungsi contoh"
}
```

### Bagian 14.5: Fungsi yang menerima parameter bernama

```bash
foo() {
    while [[ "$#" -gt 0 ]]
    do
        case $1 in
            -f|--follow)
            local FOLLOW="following"
            ;;
            -t|--tail)
            local TAIL="tail=$2"
            ;;
        esac
        shift
    done
    echo "FOLLOW: $FOLLOW"
    echo "TAIL: $TAIL"
}
```

Contoh penggunaan:

```bash
foo -f
foo -t 10
foo -f --tail 10
foo --follow --tail 10
```

### Bagian 14.6: Nilai kembali dari sebuah fungsi

Pernyataan `return` di Bash tidak mengembalikan nilai seperti fungsi C, sebaliknya ia keluar dari fungsi dengan status kembali. Anda dapat menganggapnya sebagai status keluar dari fungsi tersebut.

Jika Anda ingin mengembalikan nilai dari fungsi, maka kirimkan nilai tersebut ke `stdout` seperti ini:

```bash
fun() {
    local var="Nilai contoh yang akan dikembalikan"
    echo "$var"
    #printf "%s\n" "$var"
}
```

Sekarang, jika Anda melakukan:
`var="$(fun)"`
output dari `fun` akan disimpan di `$var`.

### Bagian 14.7: Kode keluar fungsi adalah kode keluar dari perintah terakhirnya

Perhatikan contoh fungsi ini untuk memeriksa apakah host aktif:

```bash
is_alive() {
    ping -c1 "$1" &> /dev/null
}
```

Fungsi ini mengirimkan satu `ping` ke host yang ditentukan oleh parameter fungsi pertama. Output dan output error dari `ping` keduanya dialihkan ke `/dev/null`, jadi fungsi tidak akan pernah mengeluarkan apa pun. Tetapi perintah `ping` akan memiliki kode keluar `0` jika berhasil, dan bukan nol jika gagal. Karena ini adalah perintah terakhir (dan dalam contoh ini, satu-satunya) dari fungsi, kode keluar dari `ping` akan digunakan kembali untuk kode keluar fungsi itu sendiri.

Fakta ini sangat berguna dalam pernyataan kondisional.
Sebagai contoh, jika host `graucho` aktif, maka hubungkan ke sana dengan `ssh`:

```bash
if is_alive graucho; then
    ssh graucho
fi
```

Contoh lain: periksa berulang kali sampai host `graucho` aktif, lalu hubungkan dengan `ssh`:

```bash
while ! is_alive graucho; do
    sleep 5
done
ssh graucho
```

---

# Bab 15
## Ekspansi Parameter Bash

Karakter `$` memperkenalkan ekspansi parameter, substitusi perintah, atau ekspansi aritmatika. Nama parameter atau simbol yang akan diekspansi dapat diapit dalam kurung kurawal, yang bersifat opsional tetapi berfungsi untuk melindungi variabel yang akan diekspansi dari karakter yang langsung mengikutinya yang dapat ditafsirkan sebagai bagian dari nama.

Baca lebih lanjut di [Bash User Manual](https://www.google.com/search?q=https://www.gnu.org/software/bash/manual/bash.html%23Shell-Parameter-Expansion).

### Bagian 15.1: Memodifikasi kapitalisasi karakter alfabet

**Versi ≥ 4.0**
**Ke huruf besar**

```bash
$ v="hello"
# Hanya karakter pertama
$ printf '%s\n' "${v^}"
Hello
# Semua karakter
$ printf '%s\n' "${v^^}"
HELLO
# Alternatif
$ v="hello world"
$ declare -u string="$v"
$ echo "$string"
HELLO WORLD
```

**Ke huruf kecil**

```bash
$ v="BYE"
# Hanya karakter pertama
$ printf '%s\n' "${v,}"
bYE
# Semua karakter
$ printf '%s\n' "${v,,}"
bye
# Alternatif
$ v="HELLO WORLD"
$ declare -l string="$v"
$ echo "$string"
hello world
```

**Bolak-balik Kapitalisasi**

```bash
$ v="Hello World"
# Semua karakter
$ echo "${v~~}"
hELLO wORLD
$ echo "${v~}"
# Hanya karakter pertama
hello World
```

### Bagian 15.2: Panjang parameter

```bash
# Panjang sebuah string
$ var='12345'
$ echo "${#var}"
```

Perhatikan bahwa ini adalah panjang dalam jumlah karakter yang tidak selalu sama dengan jumlah byte (seperti dalam UTF-8 di mana sebagian besar karakter dikodekan dalam lebih dari satu byte), atau jumlah *glyph/grapheme* (beberapa di antaranya adalah kombinasi karakter), juga tidak selalu sama dengan lebar tampilan.

```bash
# Jumlah elemen array
$ myarr=(1 2 3)
$ echo "${#myarr[@]}"
3
# Bekerja untuk parameter posisional juga
$ set -- 1 2 3 4
$ echo "${#@}"
4
# Tetapi lebih umum (dan portabel ke shell lain), orang akan menggunakan
$ echo "$#"
4
```

### Bagian 15.3: Ganti pola dalam string

**Kecocokan pertama:**

```bash
$ a='I am a string'
$ echo "${a/a/A}"
I Am a string
```

**Semua kecocokan:**

```bash
$ echo "${a//a/A}"
I Am A string
```

**Kecocokan di awal:**

```bash
$ echo "${a/#I/y}"
y am a string
```

**Kecocokan di akhir:**

```bash
$ echo "${a/%g/N}"
I am a strinN
```

**Ganti pola dengan ketiadaan:**

```bash
$ echo "${a/g/}"
I am a strin
```

**Tambahkan awalan ke item array:**

```bash
$ A=(hello world)
$ echo "${A[@]/#/R}"
Rhello Rworld
```

### Bagian 15.4: Substring dan subarray

```bash
var='0123456789abcdef'
# Tentukan offset berbasis nol
$ printf '%s\n' "${var:3}"
3456789abcdef
# Offset dan panjang substring
$ printf '%s\n' "${var:3:4}"
3456
```

**Versi ≥ 4.2**

```bash
# Panjang negatif dihitung dari akhir string
$ printf '%s\n' "${var:3:-5}"
3456789a
# Offset negatif dihitung dari akhir
# Membutuhkan spasi untuk menghindari kebingungan dengan ${var:-6}
$ printf '%s\n' "${var: -6}"
abcdef
# Alternatif: tanda kurung
$ printf '%s\n' "${var:(-6)}"
abcdef
# Offset negatif dan panjang negatif
$ printf '%s\n' "${var: -6:-5}"
a
```

Ekspansi yang sama berlaku jika parameter adalah parameter posisional atau elemen dari array bersubskrip:

```bash
# Atur parameter posisional $1
set -- 0123456789abcdef
# Tentukan offset
$ printf '%s\n' "${1:5}"
56789abcdef
# Tetapkan ke elemen array
myarr[0]='0123456789abcdef'
# Tentukan offset dan panjang
$ printf '%s\n' "${myarr[0]:7:3}"
789
```

Ekspansi analog berlaku untuk parameter posisional, di mana offset berbasis satu:

```bash
# Atur parameter posisional $1, $2, ...
$ set -- 1 2 3 4 5 6 7 8 9 0 a b c d e f
# Tentukan offset (waspadai $0 (bukan parameter posisional)
# sedang dipertimbangkan di sini juga)
$ printf '%s\n' "${@:10}"
0
a
b
c
d
e
f
# Tentukan offset dan panjang
$ printf '%s\n' "${@:10:3}"
0
a
b
# Tidak ada panjang negatif yang diizinkan untuk parameter posisional
$ printf '%s\n' "${@:10:-2}"
bash: -2: substring expression < 0
# Offset negatif dihitung dari akhir
# Membutuhkan spasi untuk menghindari kebingungan dengan ${@:-10:2}
$ printf '%s\n' "${@: -10:2}"
7
8
# ${@:0} adalah $0 yang bukan parameter posisional atau bagian
# dari $@
$ printf '%s\n' "${@:0:2}"
/usr/bin/bash
1
```

Ekspansi substring dapat digunakan dengan array terindeks:

```bash
# Buat array (indeks berbasis nol)
$ myarr=(0 1 2 3 4 5 6 7 8 9 a b c d e f)
# Elemen dengan indeks 5 dan lebih tinggi
$ printf '%s\n' "${myarr[@]:12}"
c
d
e
f
# 3 elemen, dimulai dengan indeks 5
$ printf '%s\n' "${myarr[@]:5:3}"
5
6
7
# Elemen terakhir dari array
$ printf '%s\n' "${myarr[@]: -1}"
f
```

### Bagian 15.5: Hapus pola dari awal string

**Kecocokan terpendek:**

```bash
$ a='I am a string'
$ echo "${a#*a}"
m a string
```

**Kecocokan terpanjang:**

```bash
$ echo "${a##*a}"
string
```

### Bagian 15.6: Indireksi parameter

Indireksi Bash memungkinkan untuk mendapatkan nilai dari variabel yang namanya terkandung dalam variabel lain.
Contoh variabel:

```bash
$ red="warna merah"
$ green="warna hijau"
$ color=red
$ echo "${!color}"
warna merah
$ color=green
$ echo "${!color}"
warna hijau
```

Beberapa contoh lagi yang menunjukkan penggunaan ekspansi tidak langsung:

```bash
$ foo=10
$ x=foo
$ echo ${x}         #Cetak variabel klasik
foo
$ foo=10
$ x=foo
$ echo ${!x}        #Ekspansi tidak langsung
10
```

Satu contoh lagi:

```bash
$ argtester () { for (( i=1; i<="$#"; i++ )); do echo "${i}";done; }; argtester -ab -cd -ef
1            #i diekspansi menjadi 1
2            #i diekspansi menjadi 2
3            #i diekspansi menjadi 3
$ argtester () { for (( i=1; i<="$#"; i++ )); do echo "${!i}";done; }; argtester -ab -cd -ef
-ab          # i=1 --> diekspansi menjadi $1 ---> diekspansi menjadi argumen pertama yang dikirim ke fungsi
-cd          # i=2 --> diekspansi menjadi $2 ---> diekspansi menjadi argumen kedua yang dikirim ke fungsi
-ef          # i=3 --> diekspansi menjadi $3 ---> diekspansi menjadi argumen ketiga yang dikirim ke fungsi
```

### Bagian 15.7: Ekspansi parameter dan nama file

Anda dapat menggunakan Ekspansi Parameter Bash untuk meniru operasi pemrosesan nama file umum seperti `basename` dan `dirname`.
Kita akan menggunakan ini sebagai path contoh kita:
`FILENAME="/tmp/example/myfile.txt"`

Untuk meniru `dirname` dan mengembalikan nama direktori dari path file:
`echo "${FILENAME%/*}"`
`#Out: /tmp/example`

Untuk meniru `basename $FILENAME` dan mengembalikan nama file dari path file:
`echo "${FILENAME##*/}"`
`#Out: myfile.txt`

Untuk meniru `basename $FILENAME .txt` dan mengembalikan nama file tanpa ekstensi `.txt`:

```bash
BASENAME="${FILENAME##*/}"
echo "${BASENAME%%.txt}"
#Out: myfile
```

### Bagian 15.8: Substitusi nilai default

**`${parameter:-word}`**
Jika parameter tidak disetel atau null, ekspansi dari `word` disubstitusikan. Jika tidak, nilai `parameter` disubstitusikan.

```bash
$ unset var
$ echo "${var:-XX}"    # Parameter tidak disetel -> ekspansi XX terjadi
XX
$ var=""
$ echo "${var:-XX}"    # Parameter null -> ekspansi XX terjadi
XX
$ var=23
$ echo "${var:-XX}"    # Parameter tidak null -> ekspansi asli terjadi
23
```

**`${parameter:=word}`**
Jika parameter tidak disetel atau null, ekspansi `word` ditugaskan ke `parameter`. Nilai `parameter` kemudian disubstitusikan. Parameter posisional dan parameter khusus tidak dapat ditugaskan dengan cara ini.

```bash
$ unset var
$ echo "${var:=XX}"    # Parameter tidak disetel -> word ditugaskan ke XX
XX
$ echo "$var"
XX
$ var=""
$ echo "${var:=XX}"    # Parameter null -> word ditugaskan ke XX
XX
$ echo "$var"
XX
$ var=23
$ echo "${var:=XX}"    # Parameter tidak null -> tidak ada penugasan yang terjadi
23
$ echo "$var"
23
```

### Bagian 15.9: Hapus pola dari akhir string

**Kecocokan terpendek:**

```bash
$ a='I am a string'
$ echo "${a%a*}"
I am
```

**Kecocokan terpanjang:**

```bash
$ echo "${a%%a*}"
I
```

### Bagian 15.10: Munging saat ekspansi

Variabel tidak harus selalu diekspansi ke nilainya - substring dapat diekstraksi selama ekspansi, yang dapat berguna untuk mengekstraksi ekstensi file atau bagian dari path. Karakter globbing mempertahankan makna biasanya, jadi `.*` merujuk pada titik harfiah, diikuti oleh urutan karakter apa pun; itu bukan ekspresi reguler.

```bash
$ v=foo-bar-baz
$ echo ${v%%-*}
foo
$ echo ${v%-*}
foo-bar
$ echo ${v##*-}
baz
$ echo ${v#*-}
bar-baz
```

Juga memungkinkan untuk mengekspansi variabel menggunakan nilai default - katakanlah saya ingin memanggil editor pengguna, tetapi jika mereka belum mengaturnya, saya ingin memberi mereka `vim`.

```bash
$ EDITOR=nano
$ ${EDITOR:-vim} /tmp/some_file
# membuka nano
$ unset EDITOR
$ ${EDITOR:-vim} /tmp/some_file
# membuka vim
```

Ada dua cara berbeda untuk melakukan ekspansi ini, yang berbeda dalam apakah variabel yang relevan kosong atau tidak disetel. Menggunakan `:-` akan menggunakan default jika variabelnya tidak disetel atau kosong, sedangkan `-` hanya menggunakan default jika variabelnya tidak disetel, tetapi akan menggunakan variabel jika disetel ke string kosong:

```bash
$ a="set"
$ b=""
$ unset c
$ echo ${a:-default_a} ${b:-default_b} ${c:-default_c}
set default_b default_c
$ echo ${a-default_a} ${b-default_b} ${c-default_c}
set default_c
```

Mirip dengan default, alternatif dapat diberikan; di mana default digunakan jika variabel tertentu tidak tersedia, alternatif digunakan jika variabel tersedia.

```bash
$ a="set"
$ b=""
$ echo ${a:+alternative_a} ${b:+alternative_b}
alternative_a
```

Memperhatikan bahwa ekspansi ini dapat bersarang, menggunakan alternatif menjadi sangat berguna saat memberikan argumen ke flag baris perintah;

```bash
$ output_file=/tmp/foo
$ wget ${output_file:+"-o ${output_file}"} www.stackexchange.com
# diekspansi menjadi wget -o /tmp/foo www.stackexchange.com
$ unset output_file
$ wget ${output_file:+"-o ${output_file}"} www.stackexchange.com
# diekspansi menjadi wget www.stackexchange.com
```

### Bagian 15.11: Error jika variabel kosong atau tidak disetel

Semantiknya mirip dengan substitusi nilai default, tetapi alih-alih mengganti nilai default, ia menghasilkan error dengan pesan kesalahan yang disediakan. Bentuknya adalah `${VARNAME?ERRMSG}` dan `${VARNAME:?ERRMSG}`. Bentuk dengan `:` akan menghasilkan error jika variabelnya tidak disetel atau kosong, sedangkan bentuk tanpa `:` hanya akan menghasilkan error jika variabelnya tidak disetel. Jika error dilemparkan, `ERRMSG` ditampilkan dan kode keluar diatur ke 1.

```bash
#!/bin/bash
FOO=
# ./script.sh: baris 4: FOO: EMPTY
echo "FOO adalah ${FOO:?EMPTY}"
# FOO adalah
echo "FOO adalah ${FOO?UNSET}"
# ./script.sh: baris 8: BAR: EMPTY
echo "BAR adalah ${BAR:?EMPTY}"
# ./script.sh: baris 10: BAR: UNSET
echo "BAR adalah ${BAR?UNSET}"
```

Untuk menjalankan contoh lengkap di atas, setiap pernyataan `echo` yang menghasilkan error perlu dikomentari untuk melanjutkan.

---

# Bab 16
## Menyalin (cp)

| Opsi | Deskripsi |
| :--- | :--- |
| `-a`, `-archive` | Menggabungkan opsi `d`, `p` dan `r` |
| `-b`, `-backup` | Sebelum menghapus, membuat cadangan |
| `-d`, `--no-deference` | Mempertahankan link |
| `-f`, `--force` | Hapus tujuan yang ada tanpa meminta pengguna |
| `-i`, `--interactive` | Tampilkan prompt sebelum menimpa |
| `-l`, `--link` | Alih-alih menyalin, buat link file |
| `-p`, `--preserve` | Pertahankan atribut file jika memungkinkan |
| `-R`, `--recursive` | Salin direktori secara rekursif |

### Bagian 16.1: Menyalin satu file

Salin `foo.txt` dari `/path/to/source/` ke `/path/to/target/folder/`
`cp /path/to/source/foo.txt /path/to/target/folder/`

Salin `foo.txt` dari `/path/to/source/` ke `/path/to/target/folder/` ke dalam file bernama `bar.txt`
`cp /path/to/source/foo.txt /path/to/target/folder/bar.txt`

### Bagian 16.2: Menyalin folder

salin folder `foo` ke dalam folder `bar`
`cp -r /path/to/foo /path/to/bar`

jika folder `bar` ada sebelum mengeluarkan perintah, maka `foo` dan kontennya akan disalin ke dalam folder `bar`. Namun, jika `bar` tidak ada sebelum mengeluarkan perintah, maka folder `bar` akan dibuat dan konten `foo` akan ditempatkan di dalam `bar`.

---

# Bab 17
## Find

`find` adalah perintah untuk secara rekursif mencari direktori untuk file (atau direktori) yang cocok dengan kriteria, dan kemudian melakukan beberapa tindakan pada file yang dipilih.
`find search_path selection_criteria action`

### Bagian 17.1: Mencari file berdasarkan nama atau ekstensi

Untuk menemukan file/direktori dengan nama tertentu, relatif terhadap `pwd`:

```bash
$ find . -name "myFile.txt"
./myFile.txt
```

Untuk menemukan file/direktori dengan ekstensi tertentu, gunakan wildcard:

```bash
$ find . -name "*.txt"
./myFile.txt
./myFile2.txt
```

Untuk menemukan file/direktori yang cocok dengan salah satu dari banyak ekstensi, gunakan flag `or`:
`$ find . -name "*.txt" -o -name "*.sh"`

Untuk menemukan file/direktori yang namanya dimulai dengan `abc` dan diakhiri dengan satu karakter alfa diikuti oleh satu digit:
`$ find . -name "abc[a-z][0-9]"`

Untuk menemukan semua file/direktori yang terletak di direktori tertentu:
`$ find /opt`

Untuk mencari file saja (bukan direktori), gunakan `-type f`:
`find /opt -type f`

Untuk mencari direktori saja (bukan file biasa), gunakan `-type d`:
`find /opt -type d`

### Bagian 17.2: Menjalankan perintah pada file yang ditemukan

Terkadang kita perlu menjalankan perintah pada banyak file. Ini dapat dilakukan menggunakan `xargs`.
`find . -type d -print | xargs -r chmod 770`

Perintah di atas akan secara rekursif menemukan semua direktori (`-type d`) relatif terhadap `.` (yang merupakan direktori kerja Anda saat ini), dan menjalankan `chmod 770` pada mereka. Opsi `-r` menentukan kepada `xargs` untuk tidak menjalankan `chmod` jika `find` tidak menemukan file apa pun.

Jika nama file atau direktori Anda memiliki karakter spasi di dalamnya, perintah ini mungkin macet; solusinya adalah menggunakan yang berikut:
`find . -type d -print0 | xargs -r -0 chmod 770`

Dalam contoh di atas, flag `-print0` dan `-0` menentukan bahwa nama file akan dipisahkan menggunakan byte null, dan memungkinkan penggunaan karakter khusus, seperti spasi, dalam nama file. Ini adalah ekstensi GNU, dan mungkin tidak berfungsi di versi `find` dan `xargs` lainnya.

Cara yang lebih disukai untuk melakukan ini adalah dengan melewati perintah `xargs` dan membiarkan `find` memanggil subproses itu sendiri:
`find . -type d -exec chmod 770 {} \;`
Di sini, `{}` adalah placeholder yang menunjukkan bahwa Anda ingin menggunakan nama file pada titik itu. `find` akan menjalankan `chmod` pada setiap file secara individual.

Anda juga dapat meneruskan semua nama file ke satu panggilan `chmod`, dengan menggunakan:
`find . -type d -exec chmod 770 {} +`
Ini juga merupakan perilaku cuplikan `xargs` di atas. (Untuk memanggil setiap file secara individual, Anda dapat menggunakan `xargs -n1`).

Opsi ketiga adalah membiarkan `bash` melakukan loop pada daftar nama file yang dihasilkan `find`:
`find . -type d | while read -r d; do chmod 770 "$d"; done`

Ini secara sintaksis yang paling canggung, tetapi nyaman ketika Anda ingin menjalankan beberapa perintah pada setiap file yang ditemukan. Namun, ini tidak aman jika ada nama file dengan nama aneh.
`find . -type f | while read -r d; do mv "$d" "${d// /_}"; done`
yang akan mengganti semua spasi di nama file dengan garis bawah. (Contoh ini juga tidak akan berfungsi jika ada spasi di nama direktori terkemuka.)

Masalah dengan yang di atas adalah `while read -r` mengharapkan satu entri per baris, tetapi nama file dapat berisi baris baru (dan juga, `read -r` akan kehilangan spasi di akhir). Anda dapat memperbaikinya dengan membalik keadaan:
`find . -type d -exec bash -c 'for f; do mv "$f" "${f// /_}"; done' _ {} +`

Dengan cara ini, `-exec` menerima nama file dalam bentuk yang sepenuhnya benar dan portabel; `bash -c` menerimanya sebagai sejumlah argumen, yang akan ditemukan di `$@`, dikutip dengan benar, dll. (Skrip perlu menangani nama-nama ini dengan benar, tentu saja; setiap variabel yang berisi nama file perlu dalam tanda kutip ganda.)

`_` yang misterius diperlukan karena argumen pertama untuk `bash -c 'script'` digunakan untuk mengisi `$0`.

### Bagian 17.3: Menemukan file berdasarkan waktu akses / modifikasi

Pada sistem file `ext`, setiap file memiliki waktu Akses, Modifikasi, dan Perubahan (Status) yang tersimpan - untuk melihat informasi ini Anda dapat menggunakan `stat myFile.txt`; menggunakan flag di dalam `find`, kita dapat mencari file yang dimodifikasi dalam rentang waktu tertentu.

Untuk menemukan file yang telah dimodifikasi dalam 2 jam terakhir:
`$ find . -mmin -120`

Untuk menemukan file yang belum dimodifikasi dalam 2 jam terakhir:
`$ find . -mmin +120`

Contoh di atas hanya mencari pada waktu modifikasi - untuk mencari pada waktu akses, atau waktu perubahan, gunakan `a`, atau `c` secara berurutan.

```bash
$ find . -amin -120
$ find . -cmin +120
```

**Format umum:**

  * `-mmin n` : File dimodifikasi n menit yang lalu
  * `-mmin -n` : File dimodifikasi kurang dari n menit yang lalu
  * `-mmin +n` : File dimodifikasi lebih dari n menit yang lalu

Temukan file yang telah dimodifikasi dalam 2 hari terakhir:
`find . -mtime -2`

Temukan file yang belum dimodifikasi dalam 2 hari terakhir:
`find . -mtime +2`

Gunakan `-atime` dan `-ctime` untuk waktu akses dan waktu perubahan status.

**Format umum:**

  * `-mtime n` : File dimodifikasi n x 24 jam yang lalu
  * `-mtime -n` : File dimodifikasi kurang dari n x 24 jam yang lalu
  * `-mtime +n` : File dimodifikasi lebih dari n x 24 jam yang lalu

Temukan file yang dimodifikasi dalam rentang tanggal, dari 2007-06-07 hingga 2007-06-08:
`find . -type f -newermt 2007-06-07 ! -newermt 2007-06-08`

Temukan file yang diakses dalam rentang stempel waktu (menggunakan file sebagai stempel waktu), dari 1 jam yang lalu hingga 10 menit yang lalu:

```bash
touch -t $(date -d '1 HOUR AGO' +%Y%m%d%H%M.%S) start_date
touch -t $(date -d '10 MINUTE AGO' +%Y%m%d%H%M.%S) end_date
timeout 10 find "$LOCAL_FOLDER" -newerat "start_date" ! -newerat "end_date" -print
```

**Format umum:**
`-newerXY referensi` : Membandingkan stempel waktu file saat ini dengan `referensi`. `XY` dapat memiliki salah satu nilai berikut: `at` (waktu akses), `mt` (waktu modifikasi), `ct` (waktu perubahan) dan lainnya. `referensi` adalah nama file yang ingin kita bandingkan stempel waktu yang ditentukan (akses, modifikasi, perubahan) atau string yang menggambarkan waktu absolut.

### Bagian 17.4: Menemukan file berdasarkan ukuran

Temukan file yang lebih besar dari 15MB:
`find -type f -size +15M`

Temukan file yang kurang dari 12KB:
`find -type f -size -12k`

Temukan file yang ukurannya tepat 12KB:

```bash
find -type f -size 12k
```

Atau

```bash
find -type f -size 12288c
```

Atau

```bash
find -type f -size 24b
```

Atau

```bash
find -type f -size 24
```

**Format umum:**
`find [opsi] -size n[cwbkMG]`
Temukan file berukuran n-blok, di mana `+n` berarti lebih dari n-blok, `-n` berarti kurang dari n-blok dan `n` (tanpa tanda apa pun) berarti tepat n-blok.

**Ukuran blok:**

1.  `c`: byte
2.  `w`: 2 byte
3.  `b`: 512 byte (default)
4.  `k`: 1 KB
5.  `M`: 1 MB
6.  `G`: 1 GB

### Bagian 17.5: Filter path

Parameter `-path` memungkinkan untuk menentukan pola yang cocok dengan path hasil. Pola tersebut juga dapat cocok dengan nama itu sendiri.

Untuk menemukan hanya file yang mengandung `log` di mana saja di pathnya (folder atau nama):
`find . -type f -path '*log*'`

Untuk menemukan hanya file di dalam folder bernama `log` (di tingkat mana pun):
`find . -type f -path '*/log/*'`

Untuk menemukan hanya file di dalam folder bernama `log` atau `data`:
`find . -type f -path '*/log/*' -o -path '*/data/*'`

Untuk menemukan semua file kecuali yang terkandung dalam folder bernama `bin`:
`find . -type f -not -path '*/bin/*'`

Untuk menemukan semua file kecuali yang terkandung dalam folder bernama `bin` atau file `log`:
`find . -type f -not -path '*log' -not -path '*/bin/*'`

### Bagian 17.6: Menemukan file berdasarkan tipe

Untuk menemukan file, gunakan flag `-type f`
`$ find . -type f`

Untuk menemukan direktori, gunakan flag `-type d`
`$ find . -type d`

Untuk menemukan perangkat blok, gunakan flag `-type b`
`$ find /dev -type b`

Untuk menemukan symlink, gunakan flag `-type l`
`$ find . -type l`

### Bagian 17.7: Menemukan file berdasarkan ekstensi spesifik

Untuk menemukan semua file dengan ekstensi tertentu di dalam path saat ini, Anda dapat menggunakan sintaks `find` berikut. Ini bekerja dengan memanfaatkan konstruk `glob` bawaan bash untuk mencocokkan semua nama yang memiliki `.ekstensi`.
`find /direktori/untuk/dicari -maxdepth 1 -type f -name "*.ekstensi"`

Untuk menemukan semua file tipe `.txt` dari direktori saat ini saja, lakukan:
`find . -maxdepth 1 -type f -name "*.txt"`

---

