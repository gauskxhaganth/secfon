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

