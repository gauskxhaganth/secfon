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

