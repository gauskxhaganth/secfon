# Bab 1
## Pengenalan Bitcoin
#### **1. Apa itu Bitcoin?**

Bitcoin adalah **jaringan terdesentralisasi** untuk **mengirim dan menerima mata uang digital** bernama **bitcoin**.

* **Jaringan terdesentralisasi** → artinya tidak ada server pusat atau perusahaan yang mengatur. Semua komputer yang terhubung (**node**) saling berbagi data dan saling memverifikasi transaksi.
* **Mata uang digital (bitcoin)** → data dalam bentuk unit nilai, yang bisa dikirim dari satu alamat ke alamat lain di jaringan Bitcoin.

### **Ciri utama Bitcoin**

1. **Tanpa pihak ketiga** → tidak ada bank atau perusahaan yang memproses transaksi.
2. **Blockchain** → database publik tempat semua transaksi disimpan secara permanen.
3. **Kriptografi** → teknologi matematika untuk memastikan data transaksi tidak bisa dipalsukan dan kepemilikan bitcoin hanya bisa digunakan oleh pemilik kunci pribadinya.

**Istilah Penting:**

* **Bitcoin (dengan 'B' besar):** Mengacu pada sistem atau jaringannya secara keseluruhan.
* **bitcoin (dengan 'b' kecil):** Mengacu pada unit mata uangnya (simbol yang umum digunakan adalah BTC atau XBT). 

Tidak ada pemerintah atau perusahaan yang mengendalikan Bitcoin. Sebaliknya, ribuan komputer (sekarang mungkin jutaan) yg disebut node di seluruh dunia terhubung dalam **Jaringan Bitcoin (Bitcoin Network)** secara kolektif menjaga sistem ini tetap berjalan 24/7. Untuk menggunakan Bitcoin, Kita tidak perlu mendaftar; Kita hanya butuh koneksi internet dan sebuah program komputer, seperti aplikasi di ponsel.

**Ekosistem Bitcoin**
Jaringan Bitcoin dikelilingi oleh berbagai partisipan dan layanan:

* **End users (Pengguna akhir):** Orang-orang yang menggunakan Bitcoin untuk kebutuhan sehari-hari seperti menabung, berbelanja, atau berspekulasi.
* **Corporate users (Pengguna korporat):** Perusahaan yang menggunakan Bitcoin untuk kebutuhan bisnis, misalnya membayar gaji internasional.
* **Merchants (Pedagang):** Toko atau restoran yang menerima pembayaran Bitcoin.
* **Bitcoin services (Layanan Bitcoin):** Perusahaan yang menyediakan layanan terkait Bitcoin, seperti isi ulang pulsa, layanan anonimitas, atau pengiriman uang (remitansi).
* **Exchanges (Bursa):** Layanan komersial tempat orang menukar mata uang lokal mereka (seperti Rupiah) ke bitcoin dan sebaliknya.
* **Bitcoin developers (Pengembang Bitcoin):** Orang-orang yang bekerja (seringkali sukarela) pada program *open source* yang menjalankan Jaringan Bitcoin.
* **Bitcoin nodes (Node Bitcoin):** Komputer-komputer yang menjalankan perangkat lunak Bitcoin. Mereka bertanggung jawab untuk memproses pembayaran, menjaga keamanan, dan mencetak bitcoin baru. Siapa pun bisa menjalankan node mereka sendiri.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_1.1.png" alt="gambar" width="575"/>
</p>

Ekosistem Bitcoin diilustrasikan dengan Jaringan Bitcoin (kumpulan komputer/node yang terhubung) di tengah. Di sekelilingnya ada berbagai partisipan: Pengguna akhir, Pengguna korporat, Pedagang, Layanan Bitcoin, Bursa, Pengembang, dan Protokol di atas Bitcoin. Jaringan ini bertanggung jawab atas keamanan, pencetakan bitcoin baru, dan pemrosesan pembayaran.

#### **2. The big picture**

Bagian ini menjelaskan alur pembayaran Bitcoin dalam empat langkah sederhana, menggunakan contoh Alice yang ingin membayar 1 BTC kepada Bob.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_1.2.png" alt="gambar" width="575"/>
</p>

Diagram alur pembayaran Bitcoin dari Alice ke Bob.

1. Ponsel Alice (wallet app) membuat transaksi dan mengirimkannya ke Jaringan Bitcoin.
2. Node-node di dalam jaringan saling memverifikasi dan meneruskan transaksi tersebut.
3. Salah satu node mengumpulkan transaksi baru ke dalam sebuah "blok" dan menyebarkannya. Node lain memverifikasi blok tersebut dan menambahkannya ke catatan mereka (blockchain).
4. Ponsel Bob (wallet app) terhubung ke sebuah node. Ketika node tersebut mengupdate catatannya, ia memberi tahu wallet Bob bahwa transaksi telah dikonfirmasi dan Bob telah menerima 1 bitcoin.

**Proses Pembayaran Empat Langkah:**

1. **Alice membuat transaksi (Step 1 - Transactions):** Alice menggunakan aplikasi dompetnya (*wallet app*) untuk membuat instruksi pembayaran. Transaksi ini berisi jumlah (1 BTC), alamat Bitcoin Bob (tujuan), dan *digital signature* (tanda tangan digital) milik Alice yang membuktikan bahwa dialah pemilik sah dana tersebut.

2. **Jaringan Bitcoin memverifikasi (Step 2 - The Bitcoin network):** Transaksi dikirim ke beberapa *node* di jaringan. Setiap *node* yang menerima akan memverifikasi: apakah Alice benar-benar punya uangnya dan apakah tanda tangannya valid. Jika valid, *node* akan meneruskannya ke *node-node* lain yang terhubung dengannya (*peers*).

3. **Transaksi ditambahkan ke blockchain (Step 3 - The blockchain):** Agar semua *node* memiliki catatan yang sama dan terurut, satu *node* (disebut *miner*) akan mengambil peran untuk mengumpulkan transaksi-transaksi yang tertunda ke dalam sebuah **blok**. Blok ini kemudian ditambahkan ke rantai blok yang sudah ada sebelumnya, yang disebut **blockchain**. Blockchain ini adalah buku besar (*ledger*) dari semua transaksi yang pernah terjadi. *Miner* yang berhasil menambahkan blok baru akan mendapatkan hadiah berupa bitcoin baru.
4. **Bob menerima notifikasi (Step 4 - Wallets):** Setelah transaksi Alice masuk ke dalam sebuah blok di *blockchain*, *node* yang terhubung dengan dompet Bob akan memberitahukan bahwa pembayaran telah dikonfirmasi. Sekarang Bob dapat dengan yakin menganggap 1 BTC itu miliknya.

#### **3. Problems with money today**

Bitcoin diciptakan untuk menyelesaikan beberapa masalah yang melekat pada sistem keuangan tradisional.

* **Segregation (Pemisahan):** Sekitar 38% populasi dunia tidak memiliki akses ke rekening bank. Tanpa layanan perbankan, mereka sulit berpartisipasi dalam ekonomi digital dan global. Hal ini bisa disebabkan oleh biaya yang mahal, kurangnya dokumen identitas, atau diskriminasi.
* **Privacy issues (Masalah Privasi):** Dengan pembayaran elektronik konvensional (kartu kredit, transfer bank), pemerintah atau lembaga keuangan dapat dengan mudah melacak, menyensor, membekukan, atau bahkan menyita dana Kita.
* **Inflation (Inflasi):** Inflasi adalah penurunan daya beli mata uang. Selembar uang hari ini bisa membeli lebih sedikit barang di masa depan. Ini terjadi karena pemerintah dapat mencetak lebih banyak uang, yang mengurangi nilai dari uang yang sudah beredar. Kasus ekstrem disebut *hyperinflation*, seperti yang terjadi di Zimbabwe.
* **Borders (Batas Negara):** Mengirim uang antar negara seringkali lambat, mahal, dan rumit. Layanan seperti Western Union bisa memotong biaya hingga 16% atau lebih untuk remitansi tunai.

#### **4. The Bitcoin approach**

Bitcoin menawarkan model yang berbeda untuk mengatasi masalah-masalah di atas.

* **Decentralized (Terdesentralisasi):** Tidak ada satu entitas pun (bank atau pemerintah) yang mengendalikan Bitcoin. Kontrol didistribusikan ke ribuan *node* di seluruh dunia. Ini membuat Bitcoin bersifat *permissionless* (tanpa izin), siapa pun bisa berpartisipasi, dan tahan terhadap sensor.
* **Limited supply (Pasokan Terbatas):** Hanya akan pernah ada total 21 juta bitcoin. Pasokan ini tidak bisa ditambah sesuka hati, sehingga membuatnya tahan terhadap inflasi tinggi yang disebabkan oleh pencetakan uang berlebih. Saat ini, pasokan terus bertambah melalui hadiah blok untuk para *miner*, tetapi laju penambahannya berkurang setengahnya setiap empat tahun.
* **Borderless (Tanpa Batas):** Karena berjalan di internet, Bitcoin bersifat global. Mengirim bitcoin ke orang di seberang benua sama mudahnya dengan mengirim ke orang di ruangan yang sama.

#### **5. How is Bitcoin used?**

* **Savings (Tabungan):** Kita dapat menyimpan kekayaan dengan aman hanya dengan mengamankan *private key* Kita. Kita bisa menyimpannya di kertas, aplikasi, atau bahkan menghafalnya.
* **Cross-border payments (Pembayaran Lintas Batas):** Bitcoin seringkali lebih murah dan cepat untuk mengirim uang ke luar negeri dibandingkan layanan remitansi tradisional.
* **Shopping (Belanja):** Ideal untuk pembayaran online karena aman. Kita tidak memberikan informasi sensitif (seperti detail kartu kredit) kepada pedagang, hanya mengirim jumlah yang disepakati. 
* **Speculation (Spekulasi):** Harga bitcoin sangat fluktuatif (naik turun), yang menarik bagi sebagian orang untuk mencoba membeli saat harga rendah dan menjual saat harga tinggi.
* **Non-currency uses (Penggunaan Non-Mata Uang):** Karena data kecil bisa disematkan dalam transaksi, Bitcoin bisa digunakan untuk hal lain:

  * **Ownership (Kepemilikan):** Mencatat transfer kepemilikan aset, seperti mobil, dengan menyertakan nomor sasis dalam transaksi.
  * **Proof of existence (Bukti Keberadaan):** Membuktikan bahwa sebuah dokumen digital sudah ada pada waktu tertentu dengan "menjangkarkan" sidik jari digital (*cryptographic hash*) dari dokumen tersebut ke dalam *blockchain*. 

#### **6. When not to use Bitcoin**

Bitcoin belum cocok untuk semua hal:

* **Tiny payments (Pembayaran Sangat Kecil):** Biaya transaksi (*transaction fee*) terkadang bisa lebih mahal dari jumlah yang dikirim, membuatnya tidak ekonomis untuk pembayaran mikro. (Teknologi lapisan kedua seperti Lightning Network mencoba mengatasi ini).
* **Instant payments (Pembayaran Instan):** Transaksi Bitcoin memerlukan waktu (biasanya sekitar 10–60 menit) untuk mendapatkan konfirmasi yang aman. Ini tidak ideal untuk pembelian cepat seperti secangkir kopi.
* **Savings you can’t afford to lose (Tabungan yang Tidak Sanggup Kita Kehilangan):** Bitcoin masih merupakan teknologi baru dan harganya sangat fluktuatif. Ada juga risiko kehilangan *private key* Kita secara permanen. Jangan menaruh semua uang yang tidak bisa Kita relakan kehilangannya. **Di Bitcoin, Kita bertanggung jawab penuh atas keamanan dana Kita sendiri.**

#### **7. Other cryptocurrencies**

Selain Bitcoin, ada ribuan mata uang kripto lain yang disebut *alt-coin* (koin alternatif). Beberapa menawarkan fitur unik (seperti privasi yang lebih tinggi), sementara yang lain mungkin hanya tiruan atau bahkan penipuan.

Bitcoin memiliki **network effect (efek jaringan)** yang sangat kuat: nilainya meningkat karena banyak orang dan layanan yang sudah menggunakannya. Sebuah *alt-coin* baru akan sulit bersaing jika tidak menawarkan inovasi yang signifikan, sama seperti sulitnya membuat jejaring sosial baru untuk menyaingi yang sudah ada.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_1.14.png" alt="gambar" width="575"/>
</p>

Perbandingan Efek Jaringan. Sisi kiri menunjukkan Internet (dengan logo Facebook, Google, Skype, Twitter) dan Jaringan Bitcoin yang ramai, dengan label "Banyak orang dan layanan". Sisi kanan menunjukkan "Wownet" dan "Wowcoin" yang sepi dan terisolasi, dengan label "Tidak ada orang atau layanan".

### **Ringkasan Bab 1**

* Bitcoin adalah uang global tanpa batas yang bisa digunakan siapa saja dengan koneksi internet.
* Jaringan komputer terdesentralisasi (*node*) memverifikasi dan mencatat semua pembayaran dalam sebuah buku besar publik yang disebut *blockchain*.
* Sebuah pembayaran diproses melalui 4 langkah: transaksi dibuat, diverifikasi oleh jaringan, ditambahkan ke *blockchain*, dan dompet penerima diberi notifikasi.
* Bitcoin mencoba menyelesaikan masalah inflasi, batas negara, eksklusi keuangan, dan privasi melalui pasokan terbatas, desentralisasi, dan sifatnya yang global.
* Selain Bitcoin, ada banyak *alt-coin* lain, tetapi Bitcoin memiliki efek jaringan yang paling kuat.

---

# Bab 2
## cryptographic hash functions and digital signatures

Bab ini akan memulai perjalanan kita dalam membangun pemahaman tentang Bitcoin dari dasar. Kita akan membuat sebuah sistem uang fiktif yang sangat sederhana bernama "token kue" (*cookie token*). Kemudian, kita akan mengidentifikasi kelemahannya dan memperbaikinya dengan dua alat kriptografi yang sangat penting: **Fungsi Hash Kriptografis** (*Cryptographic Hash Functions*) dan **Tanda Tangan Digital** (*Digital Signatures*).

#### **1. The cookie token spreadsheet (Spreadsheet Token Kue)**

Bayangkan di kantor Anda ada sebuah kafe. Untuk membeli kue, Anda dan rekan kerja tidak menggunakan uang tunai, melainkan sistem internal yang dicatat dalam sebuah *spreadsheet* (lembar lajur). Sistem ini disebut **Sistem Token Kue**.

* **Pusat Kepercayaan:** Ada satu orang yang sangat dipercaya bernama Lisa. Dia yang memegang dan mengelola *spreadsheet* ini. Semua orang bisa melihatnya (*read-only*), tetapi hanya Lisa yang bisa mengubahnya.
* **Cara Kerja Transaksi:** Jika Alice ingin membeli kue seharga 10 CT (*Cookie Token*), dia akan memberitahu Lisa. Lisa akan memeriksa saldo Alice dengan mencari semua transaksi masuk dan keluar atas nama Alice. Jika saldonya cukup, Lisa akan menambahkan baris baru di akhir *spreadsheet*:
  `Dari: Alice, Ke: Cafe, Jumlah: 10 CT`.
  Kafe melihat baris baru ini dan memberikan kue kepada Alice.
* **Penciptaan Koin Baru (Coin Creation):** Bagaimana token ini muncul pertama kali? Sebagai imbalan atas pekerjaannya menjaga *spreadsheet*, Lisa dihadiahi **7.200 CT baru setiap hari**. Dia membuat baris transaksi khusus:
  `Dari: BARU, Ke: Lisa, Jumlah: 7.200 CT`.
  Ini adalah satu-satunya cara token baru diciptakan.
* **Pasokan Terbatas (Limited Supply):** Sistem ini dirancang agar hadiah untuk Lisa berkurang setengahnya setiap empat tahun (mirip seperti *Bitcoin Halving*). Dari 7.200 CT/hari, menjadi 3.600 CT/hari setelah 4 tahun, dan seterusnya, hingga hadiahnya menjadi 0. Ini memastikan total pasokan token tidak akan pernah melebihi 21 juta CT.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_2.2.png" alt="gambar" width="575"/>
</p>

lalu

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_2.4.png" alt="gambar" width="575"/>
</p>

Sebuah *spreadsheet* sederhana dengan kolom "Dari", "Ke", dan "Jumlah CT". Transaksi baru, seperti Alice membeli kue, ditambahkan sebagai baris baru di bagian paling bawah.

**Hubungan Sistem Token Kue dengan Bitcoin (Tabel 2.1):**

| Konsep di Token Kue  | Konsep di Bitcoin              | Dibahas di Bab |
| :------------------- | :----------------------------- | :------------- |
| 1 cookie token       | 1 bitcoin                      | Bab 2          |
| Spreadsheet          | The blockchain                 | Bab 6          |
| Baris di spreadsheet | Sebuah transaksi (transaction) | Bab 5          |
| Lisa                 | Seorang penambang (miner)      | Bab 7          |

Saat ini, kita berada di **Sistem Token Kue versi 1.0**.
Kelemahannya: sistem ini sepenuhnya bergantung pada kepercayaan terhadap Lisa dan kemampuannya untuk mengenali setiap orang.

#### **2. Cryptographic Hashes**

Fungsi hash kriptografis adalah alat fundamental di Bitcoin. Anda bisa membayangkannya seperti **sidik jari digital**.

* **Definisi:** Ini adalah fungsi matematis yang mengambil data input dengan ukuran berapa pun (misalnya gambar kucing berukuran 1.21 MB) dan menghasilkan output dengan ukuran tetap (misalnya 32-byte). Output ini disebut **hash**.
* **Fungsi Satu Arah (*One-Way Function*):** Sangat mudah untuk menghasilkan *hash* dari sebuah input, tetapi secara praktis mustahil untuk merekonstruksi input asli hanya dari *hash*-nya. Prosesnya seperti memasukkan gambar ke mesin penghancur kertas; Anda mendapatkan potongan-potongan kertas (*hash*), tetapi tidak bisa menyusunnya kembali menjadi gambar asli.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_2.6.png" alt="gambar" width="575"/>
</p>

Diagram yang menunjukkan sebuah gambar kucing (input) dimasukkan ke dalam sebuah kotak berlabel "Fungsi Hash Kriptografis". Outputnya adalah serangkaian angka dan huruf acak yang panjang, berlabel "A 32-byte hash".

**Sifat-sifat Penting Fungsi Hash Kriptografis (Contoh: SHA256):**

1. **Deterministik:** Input yang sama akan *selalu* menghasilkan *hash* yang sama persis.
2. **Efek Longsor (*Avalanche Effect*):** Perubahan sekecil apa pun pada input (misalnya mengubah satu piksel pada gambar kucing) akan menghasilkan *hash* yang sama sekali berbeda dan tidak terduga.
3. **Ukuran Tetap (*Fixed Size*):** Output (*hash*) selalu memiliki panjang yang sama (misalnya, SHA256 selalu menghasilkan 256-bit atau 32-byte), tidak peduli seberapa besar atau kecil inputnya.
4. **Tahan Benturan (*Collision Resistance*):** Secara praktis mustahil untuk menemukan dua input berbeda yang menghasilkan *hash* yang sama.
5. **Tahan Pra-citra (*Pre-image Resistance*):** Jika Anda hanya diberi sebuah *hash*, secara praktis mustahil untuk menemukan input yang menghasilkan *hash* tersebut.

**Istilah Penting:**

* **SHA256:** Salah satu jenis fungsi hash yang paling umum digunakan di Bitcoin. Menghasilkan output 256-bit.
* **RIPEMD160:** Jenis fungsi hash lain yang digunakan di Bitcoin. Menghasilkan output 160-bit.

**Apa gunanya?**
Fungsi hash digunakan sebagai **pemeriksaan integritas data**. Jika Anda menyimpan *hash* dari sebuah file, Anda bisa kapan saja menghitung ulang *hash* file tersebut dan membandingkannya dengan yang Anda simpan. Jika berbeda, berarti filenya telah berubah.

#### **3. Digital Signatures**

Masalah baru muncul di sistem token kue: Lisa kesulitan mengenali semua orang. Seorang penipu bernama Mallory bisa saja mengaku sebagai Anne dan menipu Lisa untuk mentransfer token milik Anne. Solusinya adalah menggunakan **tanda tangan digital**.

* **Definisi:** Tanda tangan digital adalah padanan kriptografis dari tanda tangan tulisan tangan. Bedanya, ia tidak terikat pada orang, melainkan pada sebuah angka rahasia yang sangat besar bernama **private key (kunci privat)**.

**Cara Kerja Tanda Tangan Digital**
Prosesnya melibatkan sepasang kunci (*key pair*):

1. **Private Key (Kunci Privat):** Angka acak rahasia yang sangat besar yang *hanya Anda yang tahu*. Digunakan untuk **membuat** tanda tangan.
2. **Public Key (Kunci Publik):** Sebuah angka yang dihasilkan secara matematis dari *private key*. Hubungannya satu arah: sangat mudah membuat *public key* dari *private key*, tapi mustahil mendapatkan *private key* dari *public key*. Kunci ini boleh **disebarluaskan** dan digunakan untuk **memverifikasi** tanda tangan.

**Proses Pembayaran dengan Tanda Tangan Digital**
Misalkan John ingin membeli kue:

1. **Persiapan (Satu Kali):** John membuat sepasang kunci. *Private key* dia simpan dengan aman, dan *public key* dia berikan kepada Lisa. Lisa menyimpan *public key* John dalam sebuah tabel.
2. **Membuat Tanda Tangan (Setiap Transaksi):** John menulis pesan permintaan transfer:
   `Lisa, tolong pindahkan 10 CT ke Cafe. /John`.
   Kemudian, dompet digitalnya akan melakukan:
   a. Menghitung *hash* dari pesan tersebut.
   b. Mengenkripsi *hash* tersebut menggunakan *private key* John. Hasilnya adalah **tanda tangan digital**.
   John mengirim pesan asli dan tanda tangan digitalnya ke Lisa.
3. **Verifikasi (Dilakukan Lisa):** Lisa menerima pesan dan tanda tangan. Untuk memverifikasi:
   a. Dia mengambil *public key* John dari tabelnya.
   b. Dia menggunakan *public key* John untuk mendekripsi tanda tangan. Hasilnya adalah *hash* asli (Hash A).
   c. Dia menghitung *hash* dari pesan asli yang dia terima secara terpisah (Hash B).
   d. Dia membandingkan Hash A dan Hash B. Jika **sama persis**, berarti tanda tangan itu valid dan hanya bisa dibuat oleh pemilik *private key* yang sesuai, yaitu John.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_2.14.png" alt="gambar" width="575"/>
</p>

Diagram alur proses tanda tangan digital:

1. John membuat *key pair* (kunci privat dan publik) dan memberikan kunci publiknya ke Lisa.
2. John ingin membeli kue, jadi dia membuat pesan dan menandatanganinya dengan kunci privatnya, lalu mengirimkannya ke Lisa.
3. Lisa menggunakan kunci publik John yang dia simpan untuk memverifikasi tanda tangan pada pesan tersebut. Jika verifikasi berhasil (OK), dia akan memproses transaksi.

#### **4. Private key security**

Dengan sistem baru ini, keamanan dana Anda sepenuhnya bergantung pada keamanan *private key* Anda. Jika *private key* John dicuri oleh Mallory, Mallory bisa membuat tanda tangan palsu dan mencuri semua token John. Lisa tidak akan tahu bedanya karena tanda tangannya valid secara matematis.
**Di Bitcoin, Anda adalah bank Anda sendiri. Anda bertanggung jawab penuh atas keamanan kunci Anda.**

Ada berbagai tingkatan keamanan dengan trade-off kenyamanan:

* **Online vs. Offline:** Menyimpan kunci di perangkat yang terhubung internet (online) lebih berisiko terhadap peretas, sedangkan menyimpannya di perangkat offline (seperti dompet perangkat keras/hardware wallet) jauh lebih aman tetapi kurang praktis.
* **Cleartext vs. Encrypted (Teks Biasa vs. Terenkripsi):** Menyimpan kunci sebagai teks biasa sangat berbahaya. Sebaiknya, kunci dienkripsi dengan kata sandi yang kuat.
* **Whole key vs. Split key (Kunci Utuh vs. Kunci Terpisah):** Untuk keamanan ultra-tinggi, kunci dapat dipecah menjadi beberapa bagian dan disimpan di lokasi terpisah (misalnya, menggunakan skema *multisignature*).

Sistem token kue kita sekarang telah berevolusi ke **versi 2.0**: pembayaran aman menggunakan tanda tangan digital untuk mengatasi masalah penipu. Namun, kepercayaan pada Lisa masih menjadi isu sentral.

### **Ringkasan Bab 2**

* Kita memperkenalkan sistem fiktif "Token Kue" sebagai analogi untuk memahami Bitcoin, di mana aset dicatat dalam *spreadsheet* yang dikelola oleh pihak terpercaya (Lisa).
* **Fungsi Hash Kriptografis** bertindak seperti sidik jari digital: mengubah data apa pun menjadi output satu arah dengan panjang tetap. Ini digunakan untuk memeriksa integritas data.
* **Tanda Tangan Digital** digunakan untuk mengautentikasi transaksi. Mereka dibuat menggunakan *private key* rahasia dan diverifikasi menggunakan *public key* yang bisa dibagikan.
* Dengan tanda tangan digital, masalah penipu dapat diatasi, tetapi keamanan dana kini sepenuhnya menjadi **tanggung jawab pemilik *private key***.
* Ada berbagai strategi untuk menyimpan *private key*, masing-masing dengan trade-off antara keamanan dan kenyamanan.

---

# Bab 3
## Alamat (Addresses)

**Tujuan Bab Ini:**
Bab ini akan menjelaskan evolusi dari penggunaan nama asli ke penggunaan alamat Bitcoin yang lebih anonim dan aman. Kita akan belajar:

* Bagaimana mengganti nama dengan *public key hash* untuk meningkatkan privasi dasar.
* Bagaimana melindungi diri dari kesalahan ketik yang bisa menyebabkan kehilangan dana secara permanen.

Pada akhir bab ini, sistem *spreadsheet cookie token* kita tidak akan lagi menggunakan nama orang, melainkan *hash* dari *public key*. Ini adalah langkah besar untuk membuatnya lebih mirip dengan cara kerja Bitcoin yang sebenarnya.

#### **1. Kebiasaan Makan Cookie Terungkap (Cookie-eating habits disclosed)**

**Masalah Awal: Kurangnya Privasi**

Sistem *spreadsheet* yang kita gunakan sejauh ini memiliki kelemahan besar: semua transaksi dicatat menggunakan nama asli.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_3.2.png" alt="gambar" width="580"/>
</p>

* **Gambar 3.2: Acme Insurances mengawasi kebiasaan makan cookie Chloe.**

  * Gambar ini menunjukkan bagaimana sebuah pihak ketiga (misalnya, perusahaan asuransi bernama Acme) bisa mendapatkan salinan *spreadsheet* tersebut.
  * Dengan hanya melakukan pencarian sederhana untuk nama "Chloe", perusahaan tersebut dapat melihat seluruh riwayat transaksinya. Mereka bisa tahu seberapa sering Chloe membeli cookie, berapa banyak yang dia beli, dan dari siapa dia menerima token.
  * Informasi ini bisa disalahgunakan, misalnya untuk menaikkan premi asuransi Chloe dengan asumsi dia memiliki gaya hidup yang tidak sehat.

Masalah ini tidak hanya berlaku untuk pihak ketiga. Setiap rekan kerja yang memiliki akses baca ke *spreadsheet* juga bisa dengan mudah melihat saldo dan riwayat transaksi semua orang. Ini menciptakan masalah privasi yang serius. Menanggapi hal ini, para rekan kerja meminta Lisa (administrator sistem dalam contoh kita) untuk mencari solusi.

#### **2. Mengganti Nama dengan Kunci Publik (Replacing names with public keys)**

**Solusi Pertama: Menggunakan Kunci Publik**

Lisa, yang sudah lelah mengelola daftar nama dan *public key* yang terhubung, mengusulkan ide untuk meningkatkan privasi dan menyederhanakan pekerjaannya.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_3.3.png" alt="gambar" width="580"/>
</p>

* **Gambar 3.3: Mengganti nama dengan kunci publik.**

  * Gambar ini mengilustrasikan perubahan pada *spreadsheet*. Kolom "From" (Dari) dan "To" (Ke) tidak lagi berisi nama seperti "Alice" atau "Cafe", melainkan *public key* lengkap mereka yang terdiri dari 66 karakter heksadesimal (33 byte).
  * Sekarang, *spreadsheet* menjadi jauh lebih sulit dibaca. Tanpa mengetahui *public key* milik Chloe, Acme Insurances tidak bisa lagi melacak transaksinya dengan mudah.

**Proses Pembayaran yang Baru**

Dengan perubahan ini, proses pembayaran juga berubah. Pengguna tidak lagi menggunakan nama.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_3.4.png" alt="gambar" width="580"/>
</p>

* **Gambar 3.4: Gaya pembayaran baru menggunakan kunci publik, bukan nama.**

  * Ketika John ingin membayar, pesan yang dia kirim ke Lisa tidak lagi berbunyi, "Lisa, tolong pindahkan 10 CT ke Cafe. /John".
  * Pesan barunya sekarang berisi:

    1. *Public key* pengirim.
    2. *Public key* penerima.
    3. Jumlah yang ditransfer.
  * Pesan ini kemudian ditandatangani secara digital menggunakan *private key* yang sesuai dengan *public key* pengirim.
  
<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_3.5.png" alt="gambar" width="580"/>
</p>

* **Gambar 3.5: Faiza (rekan kerja baru) menerima hadiah dari perusahaan.**

  * **Persiapan:** Faiza membuat *key pair* (*private key* dan *public key*). Dia menyimpan *private key* miliknya dengan aman.
  * **Berbagi Informasi:** Faiza memberikan **hanya *public key*-nya** kepada pihak yang akan membayarnya (perusahaan), **bukan kepada Lisa**. Ini penting karena Lisa tidak lagi perlu memelihara tabel nama dan *public key*.
  * **Proses Transaksi:** Perusahaan membuat pesan untuk memindahkan 100 CT dari *public key* mereka ke *public key* Faiza. Pesan ini ditandatangani dengan *private key* perusahaan dan dikirim ke Lisa.
  * **Verifikasi oleh Lisa:** Lisa melakukan verifikasi:

    1. Dia menggunakan *public key* pengirim (yang ada di dalam pesan) untuk memverifikasi tanda tangan digital.
    2. Dia memeriksa *spreadsheet* untuk memastikan *public key* pengirim memiliki saldo yang cukup.
    3. Lisa tidak perlu tahu siapa pemilik *public key* penerima. Selama pengirim sah dan memiliki cukup dana, dia akan mencatat transaksi tersebut.

Perubahan ini membuat sistem menjadi **pseudonim**. Identitas tidak lagi terikat pada nama, tetapi pada *public key*.

#### **3. Memperpendek Kunci Publik (Shortening the public key)**

**Masalah Baru: Ukuran Data**

Meskipun privasi meningkat, muncul masalah baru. *Public key* berukuran 33 byte, jauh lebih besar daripada nama seperti "John" yang hanya 4 byte. Hal ini membuat ukuran *spreadsheet* membengkak, memperlambat proses unduh bagi pengguna dan memakan lebih banyak ruang penyimpanan di komputer Lisa.

**Solusi Kedua: Hashing Kunci Publik menjadi 20 byte**

Para developer mengusulkan untuk mengganti *public key* dengan *hash* kriptografis dari *public key* tersebut. Proses ini tidak hanya memperpendek data tetapi juga menambahkan lapisan keamanan ekstra.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_3.6.png" alt="gambar" width="580"/>
</p>

* **Gambar 3.6: Mengganti kunci publik dengan hash RIPEMD160 dari hash SHA256 kunci publik.**

  * Prosesnya adalah sebagai berikut:

    1. Ambil *public key* (33 byte).
    2. Lakukan *hashing* menggunakan fungsi **SHA256**. Hasilnya adalah *hash* sepanjang 32 byte.
    3. Ambil hasil dari SHA256 tersebut, lalu lakukan *hashing* sekali lagi menggunakan fungsi **RIPEMD160**. Hasilnya adalah *hash* sepanjang 20 byte (160 bit).
  * Hasil akhir ini disebut **Public Key Hash (PKH)**.

> **Istilah Teknis:**
>
> * **Public Key Hash (PKH):** Ini adalah "sidik jari" dari sebuah *public key*. Ini adalah representasi yang lebih pendek dari *public key* yang dihasilkan melalui serangkaian fungsi *hash* (di Bitcoin, `RIPEMD160(SHA256(public_key))`). Tujuannya adalah untuk memperpendek alamat dan menambahkan lapisan keamanan.

Sekarang, *spreadsheet* menggunakan PKH yang hanya 20 byte, yang jauh lebih efisien daripada *public key* 33 byte.

**Proses Pembayaran Menggunakan PKH**

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_3.7.png" alt="gambar" width="580"/>
</p>

* **Gambar 3.7: John membeli cookie menggunakan PKH.**

  * Pesan yang dikirim John ke Lisa sekarang sedikit berbeda:

    * **Penerima (To):** adalah **PKH** milik Cafe.
    * **Pengirim (From):** tetap menggunakan **Public Key** milik John, bukan PKH-nya.
  * Mengapa pengirim masih menggunakan *public key*? Karena Lisa (atau siapapun yang memverifikasi) masih membutuhkan *public key* asli untuk memverifikasi tanda tangan digital.
  * Setelah menerima pesan, Lisa akan:

    1. Mengambil *public key* pengirim dari pesan.
    2. Menghitung PKH dari *public key* tersebut (`RIPEMD160(SHA256(public_key))`).
    3. Menggunakan PKH yang baru dihitung ini untuk memeriksa saldo pengirim di *spreadsheet*.
    4. Jika semua valid, dia mencatat transaksi baru, dengan PKH pengirim di kolom "From" dan PKH penerima di kolom "To".

#### **4. Mengapa Menggunakan SHA256 dan RIPEMD160?**

Menggunakan dua fungsi *hash* yang berbeda dan berurutan adalah pilihan desain yang disengaja untuk keamanan berlapis:

1. **Keamanan Ekstra:** Jika suatu saat salah satu dari fungsi *hash* ini (misalnya SHA256) ditemukan memiliki kelemahan (*vulnerability*) sehingga bisa direkayasa balik (*pre-image attack*), *public key* masih dilindungi oleh fungsi *hash* kedua (RIPEMD160). Seorang penyerang harus memecahkan keduanya untuk bisa mendapatkan *public key* dari PKH, yang secara eksponensial lebih sulit.
2. **Perbedaan Pengembang:** SHA256 dikembangkan oleh NSA (National Security Agency) AS, sementara RIPEMD160 dikembangkan oleh komunitas akademik di Eropa. Menggunakan keduanya mengurangi risiko adanya *backdoor* tersembunyi dari satu pihak pengembang.

#### **5. Menghindari Kesalahan Ketik yang Mahal (Avoiding expensive typing errors)**

**Masalah Kritis: Kesalahan Manusia**

Sistem yang sekarang menggunakan PKH (string heksadesimal 20 byte) sangat rentan terhadap kesalahan ketik.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_3.8.png" alt="gambar" width="580"/>
</p>

* **Gambar 3.8: John salah ketik saat memasukkan PKH penerima.**

  * John ingin membayar Cafe, tetapi dia salah mengetik satu karakter terakhir dari PKH Cafe (misalnya, mengetik `d` padahal seharusnya `c`).
  * Dia menandatangani pesan tersebut dan mengirimkannya ke Lisa.
  * Lisa memverifikasi tanda tangan dan saldo pengirim. Semuanya valid. Dia tidak peduli dan tidak bisa memeriksa apakah PKH penerima itu benar atau tidak. Dia hanya mencatat transaksi sesuai permintaan.
  * Akibatnya, 10 CT milik John dikirim ke sebuah PKH yang tidak memiliki *private key* yang sesuai. Tidak ada seorang pun di dunia yang bisa menggunakan dana tersebut. Uang itu **terbakar secara digital** (*digitally burned*) dan hilang selamanya.

Ini adalah masalah kegunaan dan keamanan yang sangat serius. Perlu ada cara untuk mendeteksi kesalahan ketik sebelum transaksi dikirim.

**Solusi Ketiga: Base58check**

Untuk mengatasi masalah ini, diperkenalkan konsep **Alamat Cookie Token** (di dunia nyata, ini adalah **Alamat Bitcoin**). Alamat ini adalah representasi dari PKH yang dirancang agar lebih ramah manusia dan memiliki mekanisme pendeteksi kesalahan. Proses konversi dari PKH ke alamat ini disebut **Base58check**.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_3.10.png" alt="gambar" width="580"/>
</p>

lalu

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_3.12.png" alt="gambar" width="580"/>
</p>

* **Gambar 3.10 & 3.12: Gambaran umum encoding Base58check.**

  * Proses ini mengubah PKH (byte mentah) menjadi sebuah string alamat yang bisa dibaca (contoh: `19g6oo8f...gCenRBPD`).
  * Yang terpenting, proses ini bisa dibalik (*decoding*) untuk mendapatkan kembali PKH asli, dan selama proses *decoding*, ia akan memeriksa integritas alamat untuk memastikan tidak ada salah ketik.

**Proses Encoding Base58check**

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_3.13.png" alt="gambar" width="580"/>
</p>

* **Gambar 3.13: Proses encoding Base58check pada PKH John.**
  Proses ini terdiri dari beberapa langkah:

  1. **Tambahkan Versi (Version Byte):** Sebuah byte versi ditambahkan di awal PKH. Untuk alamat P2PKH (Pay-to-Public-Key-Hash) di Bitcoin, byte versinya adalah `0x00`. Ini berguna untuk membedakan jenis-jenis alamat di masa depan.
  2. **Buat Checksum:** Sebuah *checksum* ditambahkan untuk mendeteksi kesalahan.

     * Ambil PKH yang sudah diberi versi.
     * Lakukan *hashing* dua kali dengan SHA256: `checksum_data = SHA256(SHA256(versioned_PKH))`.
     * Ambil **4 byte pertama** dari `checksum_data`. Inilah *checksum*-nya.
  3. **Gabungkan:** Tempelkan *checksum* 4 byte tersebut di akhir PKH yang sudah diberi versi. Sekarang kita punya data sepanjang 25 byte (1 byte versi + 20 byte PKH + 4 byte checksum).
  4. **Encode dengan Base58:** Ubah data 25 byte tersebut menjadi string menggunakan skema *encoding* Base58.

> **Istilah Teknis:**
>
> * **Checksum:** Sejumlah kecil data yang dihitung dari blok data yang lebih besar. Tujuannya adalah untuk mendeteksi kesalahan yang mungkin terjadi saat transmisi atau penyimpanan. Jika data utama sedikit saja berubah, *checksum* yang dihitung ulang tidak akan cocok dengan *checksum* asli.
> * **Base58:** Skema *encoding* yang menggunakan 58 karakter alfanumerik. Karakter yang ambigu secara visual dihilangkan untuk mengurangi kesalahan ketik (misalnya, `0` (nol), `O` (huruf O besar), `I` (huruf I besar), dan `l` (huruf l kecil)).

**Proses Decoding Base58check (dan Verifikasi)**

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_3.11.png" alt="gambar" width="580"/>
</p>

lalu

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_3.15.png" alt="gambar" width="580"/>
</p>

* **Gambar 3.11 & 3.15: Faiza membayar ke alamat John.**
  Ketika Faiza ingin membayar John, *wallet*-nya akan melakukan proses sebaliknya:

  1. Ambil alamat Base58check (misalnya, dari QR code).
  2. Lakukan *decode* dari Base58 kembali menjadi data 25 byte.
  3. Pisahkan data 25 byte tersebut menjadi tiga bagian:

     * Byte pertama: Versi.
     * 20 byte berikutnya: PKH.
     * 4 byte terakhir: *Checksum* yang diterima.
  4. **Verifikasi:** Ambil bagian versi dan PKH, lalu hitung ulang *checksum*-nya dengan `SHA256(SHA256(versioned_PKH))`.
  5. Bandingkan 4 byte pertama dari *checksum* yang baru dihitung dengan *checksum* yang diterima.

     * **Jika cocok:** Alamat tersebut valid. *Wallet* bisa melanjutkan untuk membuat transaksi menggunakan PKH yang diekstrak.
     * **Jika tidak cocok:** Alamat tersebut salah ketik. *Wallet* akan menampilkan pesan kesalahan dan mencegah pengiriman dana, sehingga uang tidak hilang.

Peluang sebuah kesalahan ketik menghasilkan alamat yang valid secara kebetulan sangat kecil, sekitar 1 banding 4.3 miliar. Ini membuat sistem menjadi sangat aman dari kesalahan manusia.

#### **6. Kembali ke Privasi (Back to privacy)**

Meskipun PKH dan alamat meningkatkan privasi dengan menghilangkan nama, masalah dasarnya tetap ada jika pengguna terus-menerus menggunakan alamat yang sama. Acme Insurances masih bisa mengidentifikasi bahwa semua pembayaran ke `19g6oo8f...` berasal dari satu entitas (misalnya Cafe). Jika mereka tahu satu saja transaksi milik John, mereka bisa menghubungkan semua transaksi lain yang menggunakan alamat yang sama.

**Solusi Terbaik:** Gunakan alamat baru untuk setiap transaksi yang diterima. *Wallet* modern (seperti yang nanti dibahas di Bab 4) akan mengelola pembuatan dan penyimpanan banyak alamat ini secara otomatis, sehingga sangat meningkatkan privasi pengguna.

### **Ringkasan Bab 3**

Bab ini membawa kita melalui evolusi penting dalam sistem pembayaran kita untuk membuatnya lebih mirip Bitcoin:

1. **Masalah:** Menggunakan nama asli di *spreadsheet* sangat buruk untuk privasi.

   * **Solusi:** Ganti nama dengan **kunci publik**.
2. **Masalah:** *Public key* terlalu panjang dan tidak efisien.

   * **Solusi:** Ganti *public key* dengan **Public Key Hash (PKH)** yang lebih pendek (20 byte) yang dibuat dengan `RIPEMD160(SHA256(public_key))`.
3. **Masalah:** PKH rentan terhadap kesalahan ketik yang menyebabkan dana hilang selamanya.

   * **Solusi:** Gunakan **Alamat (Address)** yang di-*encode* dengan **Base58check**. Alamat ini memiliki *checksum* internal untuk mendeteksi dan mencegah kesalahan ketik.

Sekarang, sistem kita jauh lebih privat, efisien, dan aman dari kesalahan pengguna. Kita siap untuk melanjutkan ke bab berikutnya yang akan membahas bagaimana *wallet* mengelola semua ini untuk kita.

---

# Bab 4
## Wallets

Sejauh ini, interaksi dengan sistem *cookie token* masih sangat manual dan rumit bagi pengguna. Mereka harus membuat *private key*, mengelola *public key*, dan menyusun email secara manual kepada Lisa untuk setiap transaksi. Selain itu, untuk menjaga privasi, pengguna disarankan menggunakan alamat yang berbeda untuk setiap pembayaran, yang semakin menambah kerumitan. Bab ini memperkenalkan solusi untuk masalah-masalah ini dalam bentuk aplikasi seluler yang disebut **`wallet`** (dompet).

Tujuan utama dari `wallet` adalah untuk mengotomatisasi tugas-tugas umum, mengelola *key* dengan aman, dan yang terpenting, menyederhanakan proses *backup*. Kita akan membahas evolusi `wallet`, mulai dari versi sederhana hingga implementasi canggih yang disebut **Hierarchical Deterministic (`HD`) Wallets**, yang menjadi standar industri saat ini.

### Versi Pertama Wallet

Sebuah tim pengembang di kantor memutuskan untuk membangun aplikasi seluler, yaitu `wallet`, untuk mempermudah hidup rekan-rekan mereka.

> Perlu dipahami, istilah `wallet` di dunia Bitcoin sebenarnya kurang tepat. Aplikasi ini tidak benar-benar "menyimpan" uang Kita. Uang Kita (catatan kepemilikan) ada di dalam *blockchain* (atau dalam analogi kita, *spreadsheet*). `Wallet` lebih mirip seperti **gantungan kunci (`keyring`)** yang menyimpan dan mengelola *private key* yang Kita butuhkan untuk membelanjakan uang Kita. Namun, karena istilah `wallet` sudah sangat umum, kita akan tetap menggunakannya.

`Wallet` versi pertama ini dirancang untuk menangani beberapa tugas krusial:
* **Membuat Alamat Baru**: Pengguna dapat dengan mudah membuat alamat baru untuk setiap transaksi demi privasi.
* **Mengelola Private Key**: Untuk setiap alamat yang dibuat, `wallet` akan menyimpan dan mengelola *private key* yang bersangkutan dengan aman.
* **Mentransfer Detail Pembayaran**: Proses transfer detail pembayaran dari penerima ke pembayar dipermudah. Alih-alih mengetik alamat yang panjang, `wallet` dapat menggunakan **QR code**.
* **Melakukan Pembayaran**: Aplikasi ini secara otomatis menyusun dan mengirim email yang berisi transaksi yang sudah ditandatangani secara digital ke Lisa.
* **Melacak Dana**: `Wallet` membaca *spreadsheet* dan menampilkan total saldo *cookie token* yang dimiliki pengguna.
* **Backup Private Key**: Menyediakan fasilitas untuk mencadangkan *private key* jika ponsel hilang atau rusak.

#### Alur Pembayaran Menggunakan Wallet

Mari kita lihat skenario di mana John ingin membeli kue dari kafe, di mana keduanya kini menggunakan aplikasi `wallet`.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_4.2.png" alt="gambar" width="580"/>
</p>

[Ilustrasi alur pembayaran menggunakan aplikasi wallet di ponsel, dari pemindaian QR code hingga email otomatis terkirim ke Lisa dan spreadsheet diperbarui. - Figure 4.2]

Prosesnya berjalan sebagai berikut:
1.  **Kafe Meminta Pembayaran**: `Wallet` kafe membuat alamat baru dan menampilkan detail pembayaran (alamat dan jumlah 10 CT) dalam bentuk **QR code** di layar. QR code ini berisi **payment URI** (*Uniform Resource Identifier*), sebuah format standar untuk detail pembayaran. Contohnya: `ct:19UzNFW...VtN?amount=10`.
    > Di Bitcoin, ini distandarisasi dalam **BIP21**, dan URI-nya dimulai dengan `bitcoin:`.
2.  **John Memindai (Scan)**: John menggunakan kamera ponselnya untuk memindai QR code tersebut. `Wallet`-nya secara otomatis membaca alamat tujuan dan jumlah yang harus dibayar.
3.  **Konfirmasi**: `Wallet` John menampilkan detail pembayaran untuk dikonfirmasi. John memeriksa informasinya dan menekan "OK".
4.  **Otomatisasi Latar Belakang**: `Wallet` John secara otomatis melakukan beberapa hal:
    * Memilih salah satu *key* miliknya yang memiliki saldo cukup (misalnya, ia memiliki tiga *key* dengan saldo 80 CT, 30 CT, dan 0 CT; `wallet` akan memilih salah satu dari dua yang pertama).
    * Membuat transaksi, menandatanganinya dengan *private key* yang sesuai.
    * Mengirim email berisi transaksi yang sudah ditandatangani ke Lisa.

Dari sisi Lisa, tidak ada yang berubah. Ia menerima email seperti biasa, memverifikasi transaksi, dan menambahkannya ke *spreadsheet*.

`Wallet` juga terus memantau *spreadsheet*. Ketika transaksi John dikonfirmasi oleh Lisa, `wallet` John akan memperbarui saldonya dan menampilkan notifikasi "Terkirim", sementara `wallet` kafe akan menampilkan "Diterima".

> **Transaksi yang Belum Dikonfirmasi (`Unconfirmed Transaction`)**: `Wallet` yang baik tidak akan memperbarui saldo final sebelum transaksi tersebut benar-benar tercatat di *spreadsheet* (atau *blockchain*). Transaksi yang sudah dikirim tetapi belum dicatat oleh miner disebut *unconfirmed transaction* atau **0-conf transaction**. Mengandalkannya berisiko karena ada kemungkinan transaksi tersebut tidak pernah dikonfirmasi.

---

### Backup Private Key

Kehilangan akses ke *private key* berarti kehilangan uang Kita selamanya. Oleh karena itu, *backup* adalah fitur yang mutlak diperlukan.

#### Metode Awal yang Bermasalah
Versi awal `wallet` menawarkan fitur *backup* dengan mengirimkan sebuah file teks berisi semua *private key* ke alamat email pengguna.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_4.5.png" alt="gambar" width="580"/>
</p>

[Ilustrasi proses backup private key dari wallet ke file teks yang dikirim melalui email. - Figure 4.5]

Metode ini memiliki dua kelemahan besar:
1.  **Risiko Keamanan**: Mengirim *private key* dalam bentuk teks biasa melalui email sangatlah berisiko. Siapa pun yang memiliki akses ke server email atau lalu lintas jaringan dapat mencuri *key* tersebut.
2.  **Backup yang Berlebihan**: *Backup* ini hanya mencakup *key* yang ada pada saat itu. Setiap kali pengguna membuat alamat baru, mereka harus melakukan *backup* ulang. Hal ini sangat tidak praktis dan membuat pengguna malas melakukannya.

#### Solusi: Backup Terenkripsi
Untuk mengatasi masalah keamanan, `wallet` diperbarui untuk mengenkripsi file *backup* dengan *password* yang dimasukkan oleh pengguna.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_4.6.png" alt="gambar" width="580"/>
</p>

[Ilustrasi proses backup private key yang dienkripsi dengan password sebelum dikirim. - Figure 4.6]

Jika ponsel John hilang, ia dapat memulihkan *key*-nya di ponsel baru dengan mengimpor file *backup* dan memasukkan *password* yang benar. Ini jauh lebih aman. Namun, ini masih belum menyelesaikan masalah keharusan untuk terus-menerus melakukan *backup*. Selain itu, metode ini memunculkan masalah baru.

#### Kekuatan Password dan Entropy
Kekuatan sebuah *password* diukur dalam **entropy**, yang pada dasarnya adalah tingkat ketidakpastian atau keacakan. Entropy diukur dalam bit.
* Sebuah lemparan koin memiliki 1 bit entropy.
* Sebuah *password* 8 karakter acak yang dipilih dari 64 karakter (`A-Z`, `a-z`, `0-9`, `+/`) memiliki `8 * 6 = 48` bit entropy (karena 2^6 = 64).
* Sebuah *passphrase* yang terdiri dari 5 kata acak yang dipilih dari daftar 2048 kata memiliki `5 * 11 = 55` bit entropy (karena 2^11 = 2048).

Masalahnya adalah, manusia sangat buruk dalam membuat sesuatu yang benar-benar acak. *Password* seperti `j0Hn4321` memiliki entropy yang jauh lebih rendah daripada yang terlihat karena penyerang menggunakan serangan kamus (*dictionary attack*) yang mencoba kombinasi nama, kata umum, dan pola angka yang sering digunakan.

#### Masalah dengan Backup Terenkripsi-Password
Meskipun lebih baik, pendekatan ini masih memiliki kelemahan:
* **Banyak Hal yang Harus Diamankan**: Pengguna kini harus menjaga keamanan file *backup* DAN mengingat *password*-nya.
* **Lupa Password**: *Password* yang jarang digunakan sangat rentan untuk dilupakan.
* **Perkembangan Teknologi**: Kekuatan komputasi terus meningkat. *Password* yang aman lima tahun lalu mungkin mudah dipecahkan hari ini.
* **Kesulitan Membuat Keacakan**: Pengguna cenderung memilih *password* yang mudah diingat (dan mudah ditebak).

Jelas, diperlukan solusi *backup* yang lebih fundamental dan lebih sederhana.

---

### Hierarchical Deterministic (HD) Wallets

Di sinilah sebuah terobosan besar terjadi. Para pengembang menyadari bahwa jika semua *private key* bisa dihasilkan secara deterministik (dapat diprediksi) dari satu nomor acak utama, maka pengguna hanya perlu melakukan **satu kali backup** untuk nomor acak tersebut. Nomor acak utama ini disebut **seed**.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_4.7.png" alt="gambar" width="580"/>
</p>

[Ilustrasi backup yang ideal, yaitu hanya mencadangkan satu seed saja. - Figure 4.7]

Konsep ini diimplementasikan dalam **Hierarchical Deterministic (`HD`) Wallets**, yang distandarisasi dalam **BIP32**. `HD wallet` mengorganisir *key* dalam struktur pohon (*tree*).

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_4.8.png" alt="gambar" width="580"/>
</p>

[Diagram pohon yang menunjukkan struktur key dalam HD wallet, dari master key hingga akun belanja dan tabungan, serta alamat individual. - Figure 4.8]

* **Master Private Key (`m`)**: Akar dari semua *key*. Dihasilkan dari *seed*.
* **Child Keys**: Setiap *key* dapat memiliki banyak "anak" *key*.
* **Path (Jalur)**: Setiap *key* dalam pohon dapat diidentifikasi secara unik melalui jalurnya. Contoh: `m/1/0` berarti *child key* ke-0 dari *child key* ke-1 dari *master key*.
    > Standar umum seperti **BIP44** mendefinisikan struktur jalur ini untuk berbagai tujuan (misalnya, `m/44'/0'/0'/0` untuk menerima alamat Bitcoin).

#### Proses Derivasi Key
Proses pembuatan pohon *key* ini melibatkan tiga langkah utama:
1.  **Membuat Random Seed**: Sebuah *seed* acak (misalnya, 128 bit) dibuat. Ini adalah satu-satunya bagian yang benar-benar acak.
2.  **Menderivasi Master Extended Private Key (`xprv`)**: *Seed* digunakan untuk membuat *key* utama.
3.  **Menderivasi Child Extended Private Keys**: *Key* turunan dibuat dari *master key* dan seterusnya.

#### Extended Private Key (`xprv`)
Sebuah **`xprv`** (kependekan dari *extended private key*) adalah sebuah paket data yang berisi dua komponen:
1.  **Private Key (256 bit)**: Sama seperti *private key* biasa.
2.  **Chain Code (256 bit)**: Sepotong data acak tambahan yang berfungsi sebagai "garam" atau *entropy* tambahan untuk memastikan bahwa derivasi *child key* dari *parent key* yang sama akan menghasilkan *child key* yang berbeda dan tidak dapat diprediksi.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_4.10.png" alt="gambar" width="580"/>
</p>

[Diagram yang menunjukkan sebuah xprv terdiri dari private key dan chain code. - Figure 4.10]

**Langkah 1: Menderivasi Master `xprv`**
*Master `xprv`* dibuat dengan melewatkan *random seed* melalui fungsi hash **HMAC-SHA512**. *Output* hash 512-bit ini kemudian dibagi dua:
* **256 bit pertama** menjadi **master private key**.
* **256 bit terakhir** menjadi **master chain code**.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_4.11.png" alt="gambar" width="580"/>
</p>

[Proses derivasi master xprv dari sebuah seed menggunakan HMAC-SHA512, yang hasilnya dibagi dua menjadi private key dan chain code. - Figure 4.11]

**Langkah 2: Menderivasi Child `xprv`**
Untuk menderivasi sebuah *child `xprv`* (misalnya `m/1`) dari *parent `xprv`* (`m`), prosesnya sedikit berbeda dan sangat cerdik:

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_4.12.png" alt="gambar" width="580"/>
</p>

[Diagram alur proses derivasi sebuah child xprv dari parent xprv, melibatkan parent public key, index, dan chain code. - Figure 4.12]

1.  Ambil **parent public key** (yang diderivasi dari *parent private key*), **parent chain code**, dan **index** dari *child key* yang diinginkan (misalnya, index `1`).
2.  Gabungkan ketiga data ini dan lewatkan melalui fungsi **HMAC-SHA512**.
3.  Hasil hash 512-bit yang baru ini kembali dibagi dua:
    * **256 bit pertama** (diperlakukan sebagai angka) **ditambahkan** secara matematis ke **parent private key** untuk menghasilkan **child private key**.
    * **256 bit terakhir** menjadi **child chain code**.

Proses ini dapat diulang terus-menerus untuk membuat seluruh cabang pohon *key*.

### Kembali ke Backup

Dengan adanya `HD wallet`, Rita hanya perlu melakukan satu hal untuk *backup*: mencatat **seed**-nya. Seed `16432a20...de819d` (128 bit) jauh lebih mudah dicatat daripada delapan *private key* yang berbeda. Dan yang terpenting, *backup* ini berlaku selamanya. Ia bisa membuat ribuan alamat baru di masa depan, dan semuanya dapat dipulihkan hanya dari *seed* tunggal ini.

#### Mnemonic Sentences
Meskipun mencatat *seed* heksadesimal sudah merupakan peningkatan besar, masih ada ruang untuk kesalahan pengetikan. Untuk membuatnya lebih ramah manusia, **BIP39** memperkenalkan **mnemonic sentence**.

`Wallet` dapat merepresentasikan *seed* 128-bit sebagai rangkaian 12 kata bahasa Inggris yang mudah ditulis.
* **Seed**: `16432a207785ec5c4e5a226e3bde819d`
* **Mnemonic**: `bind bone marine upper gain comfort defense dust hotel ten parrot depend`

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_4.14.png" alt="gambar" width="580"/>
</p>

[Proses encoding seed menjadi mnemonic sentence 12 kata, melibatkan checksum dan pencocokan dengan daftar kata. - Figure 4.14]

**Cara Kerja Encoding:**
1.  Ambil *seed* (misalnya 128 bit).
2.  Buat *checksum* singkat dengan mengambil beberapa bit pertama dari hash SHA256 dari *seed* tersebut (misalnya, 4 bit pertama).
3.  Gabungkan *seed* dengan *checksum* (menjadi 132 bit).
4.  Bagi rangkaian bit ini menjadi beberapa kelompok, masing-masing 11 bit. (132 / 11 = 12 kelompok).
5.  Setiap kelompok 11 bit merepresentasikan sebuah angka antara 0 dan 2047.
6.  Setiap angka ini digunakan sebagai indeks untuk memilih kata dari daftar kata standar yang berisi 2048 kata.

**Cara Kerja Decoding:**
Prosesnya dibalik. Ketika Rita memasukkan kembali 12 katanya ke `wallet` baru, `wallet` akan mengubahnya kembali menjadi rangkaian 132 bit. Empat bit terakhir kemudian diperiksa sebagai *checksum* untuk memastikan tidak ada kesalahan penulisan kata.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_4.15.png" alt="gambar" width="580"/>
</p>

[Proses decoding mnemonic sentence kembali menjadi seed dengan verifikasi checksum. - Figure 4.15]

---

### Extended Public Keys (`xpub`)

`HD wallets` memiliki satu fitur hebat lainnya yang sangat penting untuk keamanan. Kita dapat menderivasi seluruh pohon **public key** tanpa memerlukan *private key* sama sekali.

#### Kasus Penggunaan: Server Web Toko Online
Kafe ingin menjual kue secara online. Server web mereka perlu bisa menghasilkan alamat Bitcoin baru untuk setiap pesanan demi privasi. Menempatkan *private key* (atau `xprv`) di server web yang terhubung ke internet adalah ide yang sangat buruk. Jika server diretas, semua uang di akun penjualan online akan dicuri.

Solusinya adalah menggunakan **`xpub`** (kependekan dari *extended public key*). `xpub` mirip dengan `xprv`, tetapi alih-alih berisi *private key*, ia berisi **public key** dan **chain code**.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_4.17.png" alt="gambar" width="580"/>
</p>

[Diagram yang menunjukkan sebuah xpub terdiri dari public key dan chain code. - Figure 4.17]

Kafe dapat menempatkan `xpub` untuk akun penjualan online (`M/1`) di server web. Server tersebut kemudian dapat menderivasi semua *child public key* (`M/1/0`, `M/1/1`, dst.) dan membuat alamat-alamat baru tanpa pernah memiliki akses ke *private key* manapun. Uang yang masuk ke alamat-alamat ini hanya dapat dibelanjakan menggunakan *private key* yang sesuai, yang disimpan dengan aman secara *offline* di `wallet` utama kafe.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_4.18.png" alt="gambar" width="580"/>
</p>

[Proses derivasi pohon xpub dari master xpub, memungkinkan pembuatan alamat tanpa private key. - Figure 4.18]

Derivasi *child `xpub`* bekerja secara paralel dengan derivasi *child `xprv`*. Ini dimungkinkan oleh sifat matematika dari *elliptic curve cryptography* yang akan kita bahas nanti.

### Derivasi Hardened Private Keys
> **Peringatan**: Bagian ini cukup teknis dan menantang, namun sangat krusial dari sudut pandang keamanan.

Ada satu kelemahan keamanan dalam derivasi `xprv` normal. Jika seorang penyerang berhasil mendapatkan:
1.  Satu **child private key** non-hardened (misalnya `m/1/1`).
2.  **Parent extended public key (`xpub`)** (misalnya `M/1`).

Maka, penyerang tersebut dapat menghitung mundur untuk menemukan **parent private key** (`m/1`).

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_4.21.png" alt="gambar" width="580"/>
</p>

[Ilustrasi serangan di mana seorang penyerang menggunakan child private key dan parent xpub untuk menghitung parent private key. - Figure 4.21]

Ini dimungkinkan karena `child_private_key = parent_private_key + hash_output`. Penyerang mengetahui `child_private_key` dan dapat menghitung `hash_output` dari *parent `xpub`* dan index. Dengan demikian, mereka dapat menemukan `parent_private_key`. Jika penyerang mendapatkan `M` (master `xpub`) dan satu *private key* turunan mana pun, mereka bisa mendapatkan *master private key* dan mencuri semua dana di `wallet`.

Solusinya adalah **Hardened Derivation**.
* **Cara Kerja**: Alih-alih menggunakan *parent public key* untuk menghasilkan *hash* dalam proses derivasi, *hardened derivation* menggunakan **parent private key**.
* **Notasi**: Jalur *hardened* ditandai dengan tanda kutip, misalnya `m/1'`.
* **Implikasi Keamanan**: Karena *parent private key* diperlukan, mustahil untuk menderivasi *child key* (baik *private* maupun *public*) jika Kita hanya memiliki *parent `xpub`*. Ini secara efektif "memutus" rantai derivasi bagi siapa pun yang tidak memiliki *private key*.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_4.22.png" alt="gambar" width="580"/>
</p>

[Diagram perbandingan antara derivasi normal (menggunakan public key) dan derivasi hardened (menggunakan private key). - Figure 4.22]

Ini memungkinkan kompartementalisasi keamanan. Kafe dapat menggunakan *hardened derivation* untuk akun utamanya (`m/0'`, `m/1'`). Bahkan jika `xpub` untuk akun penjualan online (`M/1'`) dan salah satu *private key* di bawahnya (`m/1'/5`) bocor, penyerang tidak dapat melompat kembali untuk menemukan *master private key* (`m`). Serangan hanya terbatas pada akun penjualan online tersebut.

### Matematika Kunci Publik (Public Key Math)
> **Peringatan**: Bagian ini adalah penyelaman mendalam ke dalam matematika yang mendasari kunci publik, yang dikenal sebagai *Elliptic Curve Cryptography*.

* **Kurva Eliptik**: Kunci publik di Bitcoin adalah sebuah titik `(x, y)` pada kurva eliptik yang didefinisikan oleh persamaan `y² = x³ + 7` (dalam sebuah *finite field*).
* **Perkalian Kunci Publik**: Untuk mendapatkan sebuah *public key*, kita melakukan "perkalian" skalar. `Public Key (P) = private_key (k) * Generator Point (G)`. `G` adalah titik awal standar yang diketahui semua orang, dan `k` adalah *private key* Kita (sebuah angka yang sangat besar). Perkalian ini dilakukan melalui serangkaian operasi "penambahan titik" dan "penggandaan titik" pada kurva.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_4.24.png" alt="gambar" width="580"/>
</p>

[Grafik kurva eliptik yang menunjukkan titik-titik (public key) dan garis simetri. - Figure 4.24]

* **Keamanan**: Operasi `k * G` mudah dilakukan, tetapi kebalikannya—menemukan `k` jika Kita hanya tahu `P` dan `G`—secara komputasi tidak mungkin dilakukan. Ini dikenal sebagai **Masalah Logaritma Diskrit Kurva Eliptik**. Inilah yang membuat derivasi kunci publik menjadi fungsi satu arah.
* **Encoding Kunci Publik**: Karena kurva ini simetris terhadap sumbu x, untuk setiap nilai `x` ada dua kemungkinan nilai `y` (positif dan negatif). Untuk menghemat ruang, kita hanya perlu menyimpan koordinat `x` (32 byte) dan satu byte tambahan sebagai awalan (`02` jika `y` genap, `03` jika `y` ganjil) untuk menandakan paritas `y`. Inilah mengapa *public key* terkompresi memiliki panjang 33 byte.

### Rangkuman dan Dampak pada Sistem
Bab ini memperkenalkan `wallet` sebagai alat penting di sisi pengguna, yang secara signifikan meningkatkan kegunaan dan keamanan.
* **Pembayaran Mudah**: Otomatisasi pembuatan dan pengiriman transaksi melalui QR code.
* **Backup Sederhana dan Aman**: `HD Wallets` memungkinkan seluruh `wallet` (termasuk semua *key* di masa depan) dicadangkan dengan aman hanya dengan mencatat satu **mnemonic sentence** (12-24 kata).
* **Keamanan yang Ditingkatkan**: `HD Wallets` memungkinkan kasus penggunaan canggih seperti `watch-only wallets` dan server web yang dapat menghasilkan alamat tanpa menyimpan *private key* melalui penggunaan `xpub`. **Hardened derivation** memberikan lapisan keamanan tambahan dengan mengisolasi cabang-cabang `wallet`.

Sistem *cookie token* kini telah mencapai versi 4.0, yang jauh lebih matang dari sisi pengguna. Tabel konsep kita tidak berubah karena semua inovasi dalam bab ini terjadi di lapisan aplikasi pengguna, yang analoginya di Bitcoin juga berfungsi dengan cara yang sama.

---

# Bab 5
## Transactions

Bab ini bertujuan untuk mengatasi beberapa masalah serius yang masih ada dalam sistem *cookie token*. Meskipun penggunaan tanda tangan digital di Bab 2 telah mencegah adanya penipu, sistem ini masih memiliki kelemahan fundamental yang berpusat pada Lisa.

### Masalah dengan Sistem Lama

Sistem yang kita miliki sejauh ini memiliki tiga masalah utama:
1.  **Beban Verifikasi pada Lisa**: Seiring dengan bertambahnya jumlah pembayaran dalam *spreadsheet*, tugas Lisa untuk menghitung saldo setiap `PKH` (*Public Key Hash*) sebelum menyetujui pembayaran menjadi semakin lambat dan memakan waktu.
2.  **Tidak Fleksibel**: Jika seorang pengguna memiliki dana yang tersebar di beberapa alamat (misalnya 5 CT di alamat A dan 8 CT di alamat B), mereka tidak bisa melakukan satu pembayaran tunggal sebesar 10 CT. Mereka harus melakukan dua transaksi terpisah, yang merepotkan dan membuat *spreadsheet* menjadi "bengkak".
3.  **Kebutuhan untuk Percaya pada Lisa (Masalah Inti)**: Ini adalah masalah paling kritis. Karena hanya Lisa yang melihat email berisi tanda tangan digital, tidak ada yang bisa membuktikan jika Lisa berbuat curang. Ia bisa saja secara diam-diam mengubah jumlah pembayaran ke dirinya sendiri atau bahkan menambahkan baris transaksi palsu dari orang lain ke dirinya di dalam *spreadsheet*. Meskipun kita mengasumsikan Lisa adalah orang yang paling jujur, sistem yang baik seharusnya tidak bergantung pada kejujuran satu individu.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_5.2.png" alt="gambar" width="580"/>
</p>

[Ilustrasi dua cara Lisa dapat berbuat curang: mengubah jumlah transaksi yang ada dan menambahkan transaksi palsu baru ke spreadsheet. - Figure 5.2]

Untuk mengatasi masalah ini, Lisa memperkenalkan sebuah konsep baru yang akan merevolusi sistem: **`transaction`**.

### Membayar Menggunakan Sebuah `Transaction`

**`Transaction`** adalah sebuah paket data terstruktur yang menggantikan dua hal sekaligus: (1) email informal yang dikirim pengguna ke Lisa, dan (2) baris sederhana dalam *spreadsheet*.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_5.3.png" alt="gambar" width="580"/>
</p>

[Diagram alur pembayaran baru. Wallet John membuat sebuah 'transaction', mengirimkannya ke Lisa, yang kemudian memverifikasi dan menambahkan 'transaction' utuh tersebut ke dalam spreadsheet. - Figure 5.3]

Alur kerjanya kini berubah secara fundamental di belakang layar:
1.  **Pembuatan (`Create`)**: `Wallet` pengguna (misalnya John) membuat sebuah `transaction` formal.
2.  **Konfirmasi (`Confirm`)**: Lisa menerima `transaction` ini, memverifikasinya, dan kemudian **menambahkan seluruh `transaction` tersebut apa adanya** ke dalam *spreadsheet*. `Spreadsheet` kini tidak lagi berisi baris `Dari | Ke | Jumlah`, melainkan daftar `transaction` yang lengkap.
3.  **Verifikasi (`Verify`)**: Karena seluruh `transaction` yang ditandatangani kini bersifat publik di dalam *spreadsheet*, **siapa pun** dapat melakukan verifikasi yang sama persis seperti yang dilakukan Lisa. Ini membuat Lisa tidak bisa lagi berbuat curang.

Kunci dari sistem baru ini adalah `transaction` tidak hanya menyatakan "siapa membayar siapa", tetapi juga "uang mana yang sedang dibelanjakan". `Transaction` merujuk secara spesifik ke "koin" yang diterima dari transaksi-transaksi sebelumnya. Koin-koin ini disebut **`Unspent Transaction Outputs` (`UTXO`)**.

#### 1. Membuat `Transaction`
Mari kita bedah anatomi dari `transaction` yang dibuat oleh `wallet` John untuk membeli kue seharga 10 CT.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_5.4.png" alt="gambar" width="580"/>
</p>

[Anatomi sebuah transaction yang belum ditandatangani, menunjukkan dua input yang merujuk pada UTXO dari transaksi sebelumnya dan dua output untuk pembayaran dan kembalian. - Figure 5.4]

Sebuah `transaction` terdiri dari **`inputs`** dan **`outputs`**.

* **`Inputs`**: Bagian ini menentukan `UTXO` mana yang akan dibelanjakan. Dalam contoh ini, John memiliki dua `UTXO` (satu senilai 8 CT dan satu lagi 5 CT) dari transaksi sebelumnya. Untuk membelanjakannya, setiap `input` harus merujuk ke:
    * **`Transaction ID` (`txid`)** dari transaksi sebelumnya di mana `UTXO` itu dibuat. `txid` adalah hash double SHA256 dari `transaction` tersebut.
    * **Index output** di dalam `transaction` sebelumnya itu (misalnya, output ke-0 atau ke-1).
* **`Outputs`**: Bagian ini menentukan ke mana uang akan dikirim.
    * **Output 0**: Mengirim 10 CT ke `PKH` milik kafe.
    * **Output 1**: Mengirim sisa 3 CT kembali ke alamat baru milik John. Ini disebut **`change`** (kembalian). `Change` diperlukan karena sebuah `UTXO` harus dibelanjakan secara keseluruhan; tidak bisa sebagian.

> **Aturan Penting**: Agar sebuah `transaction` valid, jumlah total nilai `input` harus lebih besar atau sama dengan jumlah total nilai `output`. Selisihnya (jika ada) akan menjadi **`transaction fee`** untuk miner, yang akan kita bahas di Bab 7. Untuk saat ini, kita asumsikan tidak ada `fee`, sehingga `total input = total output` (13 CT = 10 CT + 3 CT).

**Menandatangani `Transaction`**
Setelah struktur `transaction` selesai dibuat, `wallet` harus menandatanganinya.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_5.5.png" alt="gambar" width="580"/>
</p>

[Proses penandatanganan transaction, di mana setiap input ditandatangani secara terpisah dan public key yang sesuai disisipkan ke dalam input. - Figure 5.5]

* **Setiap `input` harus ditandatangani secara terpisah** menggunakan *private key* yang sesuai dengan `PKH` dari `UTXO` yang dibelanjakannya.
* Tanda tangan tersebut mencakup (atau *commits to*) seluruh `transaction` (semua `input` dan `output`). Ini memastikan tidak ada bagian dari `transaction` yang dapat diubah setelah ditandatangani.
* Agar orang lain bisa memverifikasi tanda tangan, **`public key` yang sesuai harus dimasukkan ke dalam `input`**. Verifier akan menghitung hash dari `public key` ini dan mencocokkannya dengan `PKH` di `UTXO` yang dibelanjakan untuk memastikan `key` tersebut adalah `key` yang benar.

#### 2. Lisa Mengkonfirmasi `Transaction`
Lisa kini tidak perlu lagi menghitung saldo. Proses verifikasinya berubah:
1.  **Memeriksa Keberadaan `UTXO`**: Ia harus memastikan `UTXO` yang dirujuk oleh setiap `input` benar-benar ada dan belum pernah dibelanjakan sebelumnya (mencegah *double-spending*).
2.  **Memeriksa Nilai**: `Total output` ≤ `Total input`.
3.  **Memeriksa Tanda Tangan**: Semua tanda tangan di setiap `input` valid.

Untuk mempercepat langkah pertama, Lisa tidak lagi memindai seluruh *spreadsheet*. Ia kini memelihara sebuah database terpisah yang disebut **`UTXO set`**.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_5.6.png" alt="gambar" width="580"/>
</p>

[Ilustrasi Lisa menggunakan UTXO set-nya untuk memeriksa apakah input dari transaksi John valid (ada dan belum dibelanjakan). - Figure 5.6]

`UTXO set` adalah daftar semua "koin" yang belum dibelanjakan yang ada di seluruh sistem. Saat `transaction` baru masuk:
* Lisa memeriksa apakah `input`-nya ada di dalam `UTXO set`. Jika ya, `transaction` valid.
* Setelah `transaction` dikonfirmasi dan ditambahkan ke *spreadsheet*, Lisa memperbarui `UTXO set`-nya: ia **menghapus `UTXO` yang baru saja dibelanjakan** dan **menambahkan `output` baru dari `transaction` tersebut** sebagai `UTXO` baru.

#### 3. Siapa Saja Dapat Memverifikasi `Transaction`
Inilah inti dari peningkatan sistem. Karena `transaction` yang sudah ditandatangani kini tercatat secara publik di *spreadsheet*, **siapa pun dapat membuat `UTXO set` mereka sendiri** dan memverifikasi setiap `transaction` dari awal hingga akhir. Mereka dapat memastikan Lisa tidak berbuat curang.

Di Bitcoin, para verifier independen ini disebut **`full nodes`**. Mereka adalah penjaga aturan jaringan. Lisa tidak bisa lagi mencuri uang, karena jika ia mengubah `transaction` (misalnya, mengubah `PKH` tujuan menjadi miliknya), tanda tangan digital John akan menjadi tidak valid. Siapa pun yang memverifikasi *spreadsheet* akan mendeteksi kecurangan tersebut.

> **Sistem Berbasis Akun vs. Sistem Berbasis Nilai**
> Perubahan ini secara efektif mengubah sistem kita dari **sistem berbasis akun** (seperti rekening bank yang melacak saldo) menjadi **sistem berbasis nilai (`value-based`)** (seperti uang tunai fisik yang melacak koin-koin individual). Bitcoin adalah sistem berbasis nilai.

### Script
Kenyataannya, `input` dan `output` pada `transaction` Bitcoin lebih canggih dari sekadar berisi data. Mereka sebenarnya berisi bagian-bagian dari sebuah program komputer kecil yang ditulis dalam bahasa pemrograman sederhana bernama **`Script`**.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_5.11.png" alt="gambar" width="580"/>
</p>

[Diagram yang menunjukkan bahwa signature script dari input dan pubkey script dari output yang dibelanjakan digabungkan untuk membentuk satu program Script. - Figure 5.11]

* **`Pubkey Script` (di dalam `output`)**: Ini adalah semacam "kunci" atau tantangan. Ia mendefinisikan kondisi yang harus dipenuhi untuk membelanjakan `output` tersebut.
* **`Signature Script` (di dalam `input`)**: Ini adalah "jawaban" untuk tantangan tersebut. Ia menyediakan data yang memenuhi kondisi yang ditetapkan oleh `pubkey script`.

Ketika sebuah `node` memverifikasi `transaction`, ia menggabungkan `signature script` dari `input` dengan `pubkey script` dari `output` yang dibelanjakannya. Program gabungan ini kemudian dieksekusi menggunakan sebuah struktur data yang disebut **stack** (tumpukan). Jika program selesai berjalan dan hasil akhirnya adalah `TRUE` (atau `OK`), maka `input` tersebut sah dan diizinkan untuk membelanjakan `output` tersebut.

**Contoh Eksekusi Script P2PKH (Pay-to-Public-Key-Hash):**
Program gabungan untuk `transaction` P2PKH standar pada dasarnya melakukan ini:
1.  **Dari `Signature Script`**: Dorong `<signature>` dan `<public_key>` ke atas `stack`.
2.  **Dari `Pubkey Script`**:
    * `OP_DUP`: Duplikasi `<public_key>` di puncak `stack`.
    * `OP_HASH160`: Ambil `<public_key>` teratas, hash, dan dorong hasilnya (`PKH` yang dihitung) ke `stack`.
    * Dorong `<PKH_asli>` (dari `output` asli) ke `stack`.
    * `OP_EQUALVERIFY`: Bandingkan dua item teratas (`PKH` yang dihitung dan `<PKH_asli>`). Jika sama, lanjutkan. Jika tidak, gagal.
    * `OP_CHECKSIG`: Verifikasi `<signature>` terhadap `<public_key>` yang tersisa di `stack`. Jika valid, dorong `TRUE` ke `stack`.

Jika semua langkah berhasil, `stack` akan berisi `TRUE`, dan `transaction` dianggap valid. Penggunaan `Script` inilah yang membuat Bitcoin disebut sebagai "uang yang dapat diprogram" (*programmable money*).

### Jenis Pembayaran Lanjutan (`Fancy Payment Types`)

Fleksibilitas `Script` memungkinkan jenis-jenis transaksi yang lebih kompleks daripada sekadar P2PKH.

#### Multiple Signatures (`Multisig`)
Bayangkan sebuah dana amal yang dikelola oleh tiga orang (Faiza, Ellen, dan John). Mereka tidak ingin satu orang pun memiliki kendali penuh. Mereka dapat membuat sebuah `output` yang memerlukan, misalnya, **2 dari 3 tanda tangan** untuk dapat dibelanjakan.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_5.18.png" alt="gambar" width="580"/>
</p>

[Diagram yang menggambarkan setup multisignature 2-dari-3, di mana kombinasi dua dari tiga orang dapat menandatangani transaksi. - Figure 5.18]

Ini memberikan keuntungan:
* Jika satu kunci dicuri, dana tetap aman.
* Jika satu orang kehilangan kuncinya (atau meninggal), dua orang lainnya masih bisa mengakses dana.
* Tidak ada satu orang pun yang bisa kabur dengan uangnya sendirian.

Ini dicapai dengan `Script` yang menggunakan operator `OP_CHECKMULTISIG`. Namun, `multisig script` ini panjang dan kompleks. Ini menimbulkan masalah:
* `Wallet` pengirim harus tahu cara membuatnya.
* Ini membeberkan detail keamanan internal penerima kepada pengirim.
* Ukuran `transaction` menjadi besar, sehingga `transaction fee` yang dibayar oleh **pengirim** menjadi lebih mahal.

#### Pay-to-Script-Hash (`P2SH`)
**`P2SH`** (distandarisasi dalam **BIP16**) adalah solusi cerdas untuk masalah-masalah di atas.
* **Ide Utama**: Alih-alih pengirim menempatkan `multisig script` yang kompleks di dalam `output`, mereka hanya menempatkan **hash dari script tersebut**.
* **`Redeem Script`**: `Multisig script` yang asli kini disebut `redeem script`. Script ini baru diungkapkan oleh **penerima** pada saat mereka ingin membelanjakan dana tersebut.
* **Keuntungan**:
    * Bagi pengirim, `transaction` terlihat sederhana dan kecil, seolah-olah mengirim ke alamat biasa. Biaya transaksi menjadi murah.
    * Kompleksitas disembunyikan. Beban untuk menyediakan `script` yang besar dan membayar biaya yang lebih tinggi ditanggung oleh penerima saat membelanjakan, bukan oleh pengirim.

**Alamat `P2SH`**: Untuk mempermudah, alamat `P2SH` dibuat dengan mengenkode *script hash* (bukan `PKH`). Alamat ini menggunakan *version byte* yang berbeda, sehingga selalu dimulai dengan angka **`3`** (di Bitcoin `mainnet`), berbeda dari alamat P2PKH yang dimulai dengan `1`. Ini memungkinkan `wallet` pengirim untuk secara otomatis membuat `output` P2SH yang benar.

### Hal-Hal Lain dalam `Transaction`

* **Pembuatan Koin dan `Coinbase Transaction`**: Semua `bitcoin` (atau *cookie token*) berasal dari **`coinbase transaction`**. Ini adalah `transaction` khusus yang dibuat oleh miner di setiap `block`. Ini adalah satu-satunya `transaction` yang tidak memiliki `input` nyata dan berfungsi untuk "menciptakan" koin baru (hadiah `block` + `fee` transaksi) dan memberikannya kepada miner. Semua `transaction` lain pada akhirnya dapat ditelusuri kembali ke satu atau lebih `coinbase transaction`.
* **Kepercayaan pada Lisa (yang Tersisa)**: Dengan adanya `transaction` yang transparan, Lisa tidak bisa lagi mencuri atau memalsukan pembayaran. Namun, dua bentuk kepercayaan masih tersisa:
    1.  **Sensor**: Lisa masih bisa memilih untuk **tidak menyertakan (`censor`)** `transaction` yang valid di dalam `block`-nya.
    2.  **Pembalikan**: Lisa masih bisa **menghapus (`revert`)** sebuah `transaction` yang sudah ia konfirmasi dari versinya sendiri dari *spreadsheet*.

Masalah-masalah ini akan menjadi fokus dari bab-bab berikutnya. Bab ini telah berhasil mengubah sistem dari yang sangat bergantung pada kepercayaan menjadi sistem yang sebagian besar dapat diverifikasi oleh siapa saja.

---

# Bab 6
## The Blockchain

Di akhir Bab 5, kita berhasil membuat sistem di mana Lisa tidak bisa lagi mencuri uang atau memalsukan transaksi tanpa terdeteksi, karena semua `transaction` yang ditandatangani kini bersifat publik. Namun, masih ada dua hal yang mengharuskan kita untuk percaya padanya:
1.  Ia tidak akan menyensor `transaction` (akan kita bahas di bab selanjutnya).
2.  Ia tidak akan **menghapus `transaction` yang sudah dikonfirmasi**.

### Lisa Masih Bisa Menghapus Transaksi

Masalah ini sangat serius. Bayangkan Lisa membeli kue dari kafe. `Transaction`-nya dikonfirmasi dan masuk ke *spreadsheet*. Kafe memberikan kue kepada Lisa. Setelah itu, Lisa bisa saja secara diam-diam menghapus baris `transaction` tersebut dari *spreadsheet*.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_6.2.png" alt="gambar" width="580"/>
</p>

[Ilustrasi perbandingan UTXO set milik kafe dan Lisa setelah Lisa curang. UTXO set kafe masih mencatat pembayaran, sementara UTXO set Lisa tidak, seolah-olah pembayaran tidak pernah terjadi. - Figure 6.2]

Akibatnya, terjadi inkonsistensi. Menurut `UTXO set` milik kafe, mereka telah menerima 10 CT. Namun, menurut `UTXO set` Lisa (dan `UTXO set` yang akan dibuat oleh pengguna baru mana pun yang mengunduh *spreadsheet* versi terbaru), uang itu tidak pernah dibelanjakan.

Ketika kafe menyadari `transaction` tersebut hilang, mereka tidak bisa membuktikan apa-apa. Ini menjadi situasi "kata melawan kata". Kafe mengklaim `transaction` itu pernah ada, Lisa menyangkalnya. Sistem membutuhkan cara untuk membuat histori transaksi menjadi **tidak dapat diubah (`immutable`)**.

### Membangun `Blockchain`

Solusinya adalah mengganti *spreadsheet* dengan sebuah **`blockchain`**. `Blockchain` secara harfiah adalah sebuah "rantai blok". Ini adalah sebuah file log publik yang hanya bisa ditambahkan (*append-only*), di mana `transaction` dikelompokkan ke dalam struktur data yang disebut **`block`**.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_6.3.png" alt="gambar" width="580"/>
</p>

[Diagram struktur dasar sebuah blockchain, menunjukkan rantai blok-blok yang saling terhubung dari blok pertama (height 0) hingga blok terakhir (chain tip). - Figure 6.3]

Setiap `block` terhubung secara kriptografis ke `block` sebelumnya, membentuk sebuah rantai yang tidak dapat diputuskan. Setiap `block` memiliki **`height`** (ketinggian), yang menunjukkan posisinya dalam rantai, dimulai dari `height` 0 (blok pertama atau *genesis block*).

#### Anatomi Sebuah `Block`
Setiap `block` terdiri dari dua bagian utama:
1.  **Daftar `Transaction`**: `Transaction` yang dikonfirmasi dalam `block` tersebut. `Transaction` pertama dalam setiap `block` selalu merupakan **`coinbase transaction`** (hadiah untuk miner).
2.  **`Block Header`**: Bagian terpenting yang mengamankan `block` dan seluruh rantai sebelumnya.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_6.4.png" alt="gambar" width="580"/>
</p>

[Tampilan detail beberapa blok terakhir dalam blockchain, menyoroti komponen-komponen dalam block header. - Figure 6.4]

`Block header` berisi empat elemen krusial:
1.  **Hash dari `Block Header` Sebelumnya**: Ini adalah "lem" kriptografis yang menghubungkan `block` ini ke `block` sebelumnya. Hash dari `block header` juga berfungsi sebagai **`Block ID`**.
2.  **`Merkle Root`**: Sebuah hash tunggal yang secara ringkas merepresentasikan *semua* `transaction` di dalam `block` tersebut. Jika satu bit saja dari `transaction` manapun diubah, `merkle root` akan berubah total. (Detail cara kerjanya akan dibahas nanti di bab ini).
3.  **Timestamp**: Waktu perkiraan `block` dibuat.
4.  **Tanda Tangan Lisa**: Untuk saat ini, Lisa menandatangani setiap `block header` dengan *private key* khususnya. Ini adalah bukti persetujuannya. (Di Bab 7, ini akan digantikan oleh `proof-of-work`).

#### Bagaimana `Blockchain` Mencegah Penghapusan Transaksi
Mari kita lihat kembali skenario di mana Lisa mencoba menghapus `transaction` pembelian kuenya.
1.  Lisa membuat `block` #21 yang berisi `transaction` pembayarannya ke kafe. Ia menandatangani `block header` dan mempublikasikannya.
2.  Kafe melihat `block` #21, memverifikasinya, dan memberikan kue kepada Lisa.
3.  Sekarang, Lisa mencoba berbuat curang. Ia membuat versi **alternatif** dari `block` #21 (sebut saja #21b) yang **tidak berisi `transaction` pembayarannya**.
4.  Karena isi `transaction` di `block` #21b berbeda, **`merkle root`**-nya juga harus berbeda.
5.  Karena `merkle root` berubah, `block header`-nya pun berubah.
6.  Karena `block header` berubah, Lisa harus **menandatanganinya kembali**.

Lisa sekarang memiliki dua `block` yang berbeda untuk `height` 21, yaitu `block` #21 dan #21b. Keduanya valid dan ditandatangani olehnya.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_6.12.png" alt="gambar" width="580"/>
</p>

[Ilustrasi perbandingan dua versi block 21 yang dibuat Lisa. Keduanya menunjuk ke block 20 yang sama, tetapi memiliki merkle root dan tanda tangan yang berbeda karena salah satunya tidak berisi transaksi Lisa. - Figure 6.12]

Ketika kafe melihat ada dua versi `block` di `height` yang sama, mereka memiliki **bukti kriptografis yang tak terbantahkan bahwa Lisa telah berbuat curang**. Dia telah menandatangani dua histori yang saling bertentangan. Masalah "kata melawan kata" telah terpecahkan.

Lebih jauh lagi, jika Lisa mencoba mengubah `block` yang lebih tua (misalnya `block` #20), ia tidak hanya harus membuat ulang `block` #20, tetapi juga semua `block` setelahnya (`#21, #22, #23`, dst.) karena hash dari `block header` sebelumnya akan berubah, memutus rantai. Ini membuat pengubahan histori menjadi semakin sulit seiring berjalannya waktu.

### `Lightweight Wallets`

Menjalankan sebuah **`full node`**—perangkat lunak yang mengunduh dan memverifikasi seluruh `blockchain`—memberikan keamanan tertinggi tetapi membutuhkan sumber daya yang besar (penyimpanan ratusan GB, koneksi internet yang kuat, dan daya komputasi). Ini tidak praktis untuk pengguna biasa, terutama di perangkat seluler.

Untuk itu, ada jenis `wallet` lain yang disebut **`lightweight wallet`** atau **SPV (`Simplified Payment Verification`) `wallet`**. `Wallet` ini tidak mengunduh seluruh `block`, melainkan hanya **`block header`**-nya. `Wallet` ini bergantung pada `full node` untuk memberinya informasi transaksi yang relevan.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_6.15.png" alt="gambar" width="580"/>
</p>

[Diagram alur komunikasi antara lightweight wallet dan full node. Wallet mengirimkan bloom filter, lalu node mengirimkan kembali block header dan transaksi yang relevan beserta merkle path. - Figure 6.15]

Namun, ada dua masalah yang harus dipecahkan:
1.  **Privasi**: Bagaimana `wallet` bisa meminta `transaction`-nya tanpa memberitahu `full node` semua alamat yang dimilikinya?
2.  **Verifikasi**: Bagaimana `wallet` bisa yakin bahwa `transaction` yang diberikan oleh `full node` benar-benar ada di dalam `block` tersebut, jika ia tidak mengunduh semua `transaction` di `block` itu?

Solusinya adalah `Bloom Filters` dan `Merkle Trees`.

#### `Bloom Filters`: Menjaga Privasi
Alih-alih mengirimkan daftar alamatnya, `lightweight wallet` membuat dan mengirimkan sebuah **`bloom filter`** ke `full node`. `Bloom filter` adalah struktur data probabilistik yang dapat memberi tahu `full node` apakah sebuah `transaction` "mungkin" relevan untuk `wallet` tersebut, tanpa mengungkapkan alamat pastinya.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_6.17.png" alt="gambar" width="580"/>
</p>

[Proses pembuatan bloom filter. Alamat-alamat di-hash beberapa kali, dan hasilnya digunakan untuk mengatur bit dalam sebuah array menjadi 1. - Figure 6.17]

* **Cara Kerja**: `Wallet` membuat sebuah array bit (misalnya, `[0,0,0,0,0,0,0,0]`). Untuk setiap alamatnya, ia melakukan beberapa fungsi hash. Setiap hasil hash menunjuk ke sebuah indeks di array, dan bit di indeks tersebut diubah menjadi `1`.
* **Penggunaan**: `Full node` menguji setiap `transaction` baru terhadap `bloom filter` ini. Jika hasil hash dari data dalam `transaction` (seperti `PKH`) selalu menunjuk ke bit `1` di filter, `node` akan mengirim `transaction` itu ke `wallet`. Jika ada satu saja yang menunjuk ke bit `0`, `transaction` itu pasti tidak relevan.
* **`False Positives`**: Desain ini sengaja menciptakan `false positives` (hasil positif palsu), di mana `full node` juga akan mengirim beberapa `transaction` yang sebenarnya tidak relevan. Ini bagus untuk privasi karena mengaburkan alamat-alamat asli milik `wallet`. Ada *trade-off* antara privasi dan penggunaan bandwidth: semakin banyak `false positive`, semakin baik privasinya, tetapi semakin banyak data yang terbuang.

#### `Merkle Trees`: Verifikasi yang Efisien
Inilah solusi untuk masalah verifikasi. `Merkle tree` adalah cara untuk menghash semua `transaction` dalam sebuah `block` menjadi satu hash tunggal (`merkle root`) dengan cara yang sangat efisien.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_6.23.png" alt="gambar" width="580"/>
</p>

[Diagram pembuatan merkle tree. Hash dari setiap transaksi dipasangkan, digabungkan, lalu di-hash lagi, terus ke atas hingga tersisa satu hash tunggal yaitu merkle root. - Figure 6.23]

* **Pembuatan**: `txid` dari semua `transaction` di-hash secara berpasangan. Hash hasil dari setiap pasangan kemudian di-hash lagi secara berpasangan, dan seterusnya, hingga hanya tersisa satu hash. Hash tunggal terakhir inilah yang disebut **`merkle root`** dan dimasukkan ke dalam `block header`.
* **Bukti Keanggotaan (`Merkle Proof`)**: Untuk membuktikan bahwa sebuah `transaction` (misal `Tx2`) ada di dalam sebuah `block`, `full node` tidak perlu mengirim semua `transaction`. Ia hanya perlu mengirim:
    1.  `Transaction` itu sendiri (`Tx2`).
    2.  `Block header` yang berisi `merkle root`.
    3.  **`Merkle path`** (atau `partial merkle tree`): "Saudara" hash di sepanjang jalur dari `Tx2` ke `merkle root`.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_6.26.png" alt="gambar" width="580"/>
</p>

[Lightweight wallet menggunakan merkle path yang diberikan untuk merekonstruksi merkle root dan membandingkannya dengan yang ada di block header. - Figure 6.26]

Dengan informasi ini, `lightweight wallet` dapat secara mandiri menghitung ulang `merkle root`. Jika hasil perhitungannya cocok dengan `merkle root` di `block header`, maka `wallet` memiliki bukti kriptografis bahwa `transaction` tersebut benar-benar bagian dari `block` itu.

Metode ini sangat efisien. Ukuran `merkle proof` tumbuh secara logaritmik, bukan linear, dengan jumlah `transaction`. Untuk sebuah `block` dengan ribuan `transaction`, buktinya hanya terdiri dari belasan hash saja.

### Keamanan `Lightweight Wallets`

Penting untuk dipahami bahwa `lightweight wallet` mengorbankan keamanan demi kenyamanan. Pengguna `lightweight wallet` **mempercayai `full node`** yang terhubung dengannya untuk:
* Memvalidasi `script` dan tanda tangan dengan benar.
* Memastikan tidak ada *double-spending*.
* Tidak menyembunyikan `transaction` atau `block`.
* Mengikuti aturan konsensus yang benar (misalnya, tidak menerima `block` dengan hadiah yang tidak valid).

Untuk mengurangi risiko ini, pengguna `lightweight wallet` dapat melakukan dua hal:
1.  **Terhubung ke Beberapa `Full Node`**: Ini mengurangi kemungkinan ditipu oleh satu `node` jahat.
2.  **Terhubung ke `Trusted Node`**: Ini adalah pilihan paling aman. Pengguna menjalankan `full node` sendiri di rumah dan mengarahkan `lightweight wallet` di ponselnya untuk hanya terhubung ke `node` miliknya sendiri. Ini memberikan keamanan penuh dari `full node` dengan portabilitas `lightweight wallet`.

---

# Bab 7
## Proof of Work

Pada Bab 6, kita berhasil membuat histori transaksi menjadi sulit diubah dengan memperkenalkan `blockchain` yang `block`-nya ditandatangani oleh Lisa. Namun, Lisa masih memegang kekuasaan absolut untuk menentukan `transaction` mana yang akan ia masukkan ke dalam `block`. Ia bisa saja memutuskan untuk tidak memproses pembayaran kue karena alasan pribadi, secara efektif melakukan sensor. Sistem yang benar-benar terdesentralisasi tidak boleh memiliki satu titik kegagalan atau kontrol seperti ini.

### Mengkloning Lisa dan Masalah Kolisi `Block`

Solusi pertama yang terpikirkan untuk masalah sensor adalah dengan menambahkan lebih banyak "Lisa". Kita bisa menambahkan Tom dan Qi sebagai produsen `block` juga. Pengguna akan mengirim `transaction` mereka ke ketiga orang ini, dan kemungkinan `transaction` tersebut untuk dikonfirmasi akan meningkat secara dramatis.

Namun, ini menciptakan masalah baru yang fatal: **kolisi `block` (`block collisions`)**. Jika Lisa, Tom, dan Qi semuanya membuat `block` baru setiap 10 menit, maka pada `height` yang sama (misalnya, `height` 101), akan ada tiga versi `block` yang valid tetapi saling bertentangan. `Blockchain` akan langsung menjadi kacau.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_7.3.png" alt="gambar" width="580"/>
</p>

[Tiga cabang blockchain yang berbeda pada height 101, masing-masing dibuat oleh Lisa, Tom, dan Qi, menunjukkan masalah kolisi blok. - Figure 7.3]

### Solusi Naif: Mengundi Angka Keberuntungan

Untuk mengatasi kolisi, para produsen `block` (yang kini kita sebut **`miner`**) memerlukan sebuah mekanisme untuk memutuskan siapa yang berhak membuat `block` berikutnya. Alih-alih bergiliran (yang bisa macet jika satu `miner` berhenti), kita bisa menggunakan sistem lotre.

Bayangkan setiap `miner` mengundi sebuah angka acak setiap detik. Jika angka yang mereka dapatkan berada di bawah ambang batas tertentu (misalnya, di bawah 556 dari 1.000.000), mereka dianggap "beruntung" dan berhak membuat `block` berikutnya. Karena probabilitasnya rendah, biasanya hanya akan ada satu pemenang dalam satu waktu.

Namun, sesekali, dua `miner` bisa saja beruntung pada saat yang bersamaan. Ini akan menyebabkan **`blockchain split`** (pemisahan rantai), di mana ada dua cabang `block` yang valid pada `height` yang sama.

**Menyelesaikan `Split`**:
Aturan mainnya sederhana: **rantai terpanjang (`longest chain`) adalah rantai yang benar**. Para `miner` akan memilih salah satu cabang untuk melanjutkan pekerjaan mereka.
* **Resolusi Cepat**: `Miner` berikutnya yang beruntung akan menambahkan `block` ke salah satu cabang, membuatnya lebih panjang. Semua `miner` lain akan melihat ini, meninggalkan cabang yang lebih pendek, dan beralih ke cabang yang kini menjadi yang terpanjang. `Transaction` dari `block` yang ditinggalkan akan kembali ke `mempool` untuk dimasukkan ke `block` di masa depan.
* **Resolusi Tertunda**: `Split` bisa berlanjut jika `miner` di kedua cabang terus menemukan `block` baru secara bersamaan, tetapi probabilitasnya menurun secara eksponensial seiring bertambahnya panjang `split`. Pada akhirnya, satu cabang pasti akan menang.

**Kelemahan Kritis Sistem Angka Keberuntungan**:
Sistem ini, meskipun lebih baik, masih memiliki kelemahan fatal: **tidak ada cara untuk membuktikan bahwa seorang `miner` benar-benar mengundi angka secara jujur**. Seorang `miner` bisa saja berbohong dan mengklaim mereka mendapatkan angka keberuntungan kapan pun mereka mau untuk mencuri hadiah `block`. Kita membutuhkan lotre yang tidak bisa dicurangi.

### Memaksa Kejujuran: `Proof of Work`

Di sinilah konsep jenius **`proof of work`** masuk. Idenya adalah mengganti lotre yang mudah dipalsukan dengan lotre yang sangat sulit secara komputasi tetapi hasilnya sangat mudah untuk diverifikasi oleh siapa pun.

Tanda tangan digital Lisa di `block header` kini digantikan oleh `proof of work`.
Aturan barunya adalah: **sebuah `block` dianggap valid hanya jika hash dari `block header`-nya (yaitu `Block ID`-nya) secara numerik lebih kecil dari nilai `target` yang telah disepakati**.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_7.11.png" alt="gambar" width="580"/>
</p>

[Diagram yang menunjukkan bahwa Block ID, yang merupakan hash dari block header, harus lebih kecil dari nilai Target agar proof of work valid. - Figure 7.11]

`Block header` kini memiliki sebuah kolom baru: **`nonce`** (*number used once*). `Nonce` adalah angka yang bisa diubah-ubah oleh `miner` untuk mendapatkan hash `block header` yang berbeda.

Proses untuk menemukan `proof of work` yang valid (yang disebut **`mining`**) adalah sebagai berikut:
1.  Seorang `miner` merakit sebuah kandidat `block` (memilih `transaction`, membuat `coinbase transaction`, dll.).
2.  Ia mengatur `nonce` di `block header` menjadi 0.
3.  Ia menghash `block header` tersebut.
4.  Ia memeriksa apakah hash yang dihasilkan lebih kecil dari `target`.
5.  Jika tidak, ia menaikkan `nonce` (`nonce` = 1), dan kembali ke langkah 3.

`Miner` melakukan proses coba-coba (`brute-force`) ini jutaan hingga miliaran kali per detik. Karena *output* dari fungsi hash kriptografis tidak dapat diprediksi, ini setara dengan mengundi angka acak berulang kali dengan kecepatan sangat tinggi. Siapa pun yang pertama kali menemukan `nonce` yang menghasilkan hash di bawah `target` adalah "pemenang" lotre dan berhak mempublikasikan `block`-nya.

**Mengapa `Proof of Work` Lebih Baik?**
* **Sulit Dibuat, Mudah Diverifikasi**: Butuh kerja keras (listrik dan daya komputasi) untuk menemukan `proof of work`, tetapi siapa pun dapat memverifikasinya dengan melakukan **hanya satu kali operasi hash** pada `block header` pemenang dan membandingkannya dengan `target`.
* **Tidak Bisa Dicurangi**: Satu-satunya cara untuk menemukan `proof of work` adalah dengan benar-benar melakukan pekerjaan komputasi. Tidak ada jalan pintas.
* **Terdesentralisasi Penuh**: Verifikasi tidak lagi memerlukan kunci publik Lisa dari "papan buletin". Semua informasi yang dibutuhkan untuk memverifikasi sebuah `block` (termasuk `proof of work`-nya) kini terkandung di dalam `block` itu sendiri.

> **Rantai Terkuat (`Strongest Chain`) vs. Rantai Terpanjang**: Dengan `proof of work`, aturan konsensus sedikit berubah. `Node` tidak lagi sekadar mengikuti rantai terpanjang, melainkan rantai dengan **akumulasi `proof of work` terbanyak**. Ini disebut **`strongest chain`**. Untuk saat ini, keduanya hampir sama, tetapi perbedaannya menjadi penting saat kita membahas penyesuaian kesulitan.

### Penyesuaian Kesulitan (`Difficulty Adjustments`)

Sistem `proof of work` memiliki masalah: apa yang terjadi jika lebih banyak `miner` bergabung? Dengan total **`hashrate`** (jumlah hash yang dicoba per detik oleh seluruh jaringan) yang lebih tinggi, `block` akan ditemukan lebih cepat dari target rata-rata 10 menit. Ini akan menyebabkan inflasi pasokan koin yang lebih cepat dari yang direncanakan dan meningkatkan frekuensi `blockchain split`.

Solusinya adalah **`difficulty adjustment`**.
* Jaringan Bitcoin secara otomatis menyesuaikan nilai **`target`** setiap **2.016 `block`** (sekitar dua minggu).
* Ia mengukur berapa lama waktu yang dibutuhkan untuk menemukan 2.016 `block` terakhir.
* Jika waktunya **kurang dari dua minggu** (artinya `hashrate` meningkat dan `block` ditemukan terlalu cepat), jaringan akan **menurunkan `target`** (membuatnya lebih sulit untuk ditemukan).
* Jika waktunya **lebih dari dua minggu** (artinya `hashrate` menurun dan `block` ditemukan terlalu lambat), jaringan akan **menaikkan `target`** (membuatnya lebih mudah).

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_7.22.png" alt="gambar" width="580"/>
</p>

[Grafik yang menunjukkan hubungan antara waktu penyelesaian 2.016 blok dengan faktor perubahan target. Jika kurang dari 2 minggu, target turun (lebih sulit). Jika lebih dari 2 minggu, target naik (lebih mudah). - Figure 7.22]

Mekanisme ini secara elegan memastikan bahwa, tidak peduli berapa banyak `hashrate` yang ada di jaringan, rata-rata waktu antar `block` akan selalu kembali ke sekitar 10 menit.

### Apa Kerugian yang Bisa Dilakukan Miner?

Karena `block` tidak lagi ditandatangani oleh identitas tertentu, apakah ini berarti `miner` bisa melakukan serangan **`double-spend`**? Jawabannya adalah **ya, jika mereka memiliki `hashrate` yang sangat besar dan keberuntungan yang luar biasa**.

**Serangan `Double-Spend`**:
1.  Lisa (seorang `miner` jahat) ingin membeli kafe. Ia membuat dua `transaction` yang membelanjakan `UTXO` yang sama: `Tx-KAFE` (dikirim ke pemilik kafe) dan `Tx-LISA` (dikirim kembali ke dirinya sendiri).
2.  Ia menyiarkan `Tx-KAFE` ke jaringan `miner` yang jujur.
3.  Secara bersamaan, ia mulai menambang `block` secara **rahasia** yang berisi `Tx-LISA`.
4.  Jaringan jujur menemukan `block` yang berisi `Tx-KAFE`. Pemilik kafe melihatnya.
5.  Pemilik kafe menunggu beberapa `block` tambahan ditambang di atas `block` tersebut. Ini disebut **konfirmasi (`confirmations`)**. Setelah 6 konfirmasi, ia merasa aman dan menyerahkan akta kafe kepada Lisa.
6.  Sementara itu, Lisa terus menambang rantai rahasianya. Agar serangannya berhasil, ia harus bisa menambang lebih cepat dari gabungan seluruh `miner` jujur lainnya, sehingga rantai rahasianya pada akhirnya menjadi **lebih kuat** (memiliki lebih banyak akumulasi `proof of work`) daripada rantai publik yang jujur.
7.  Jika ia berhasil, ia akan menyiarkan rantai rahasianya. `Node` lain akan melihat bahwa rantai Lisa lebih kuat, melakukan reorganisasi (`reorg`), dan meninggalkan rantai yang berisi `Tx-KAFE`. `Tx-KAFE` secara efektif terhapus dari sejarah, dan `Tx-LISA` menjadi `transaction` yang sah. Lisa berhasil mendapatkan kafe dan uangnya kembali.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_7.27.png" alt="gambar" width="580"/>
</p>

[Ilustrasi kegagalan serangan double-spend Lisa. Rantai jujur terus tumbuh lebih cepat daripada rantai rahasia Lisa, membuatnya tertinggal jauh. - Figure 7.27]

**Perlindungan terhadap `Double-Spend`**:
* **Konfirmasi**: Semakin banyak konfirmasi yang ditunggu oleh pedagang, semakin sulit bagi penyerang untuk mengejar dan melampaui rantai jujur. Probabilitas keberhasilan serangan menurun secara eksponensial dengan setiap konfirmasi tambahan.
* **Serangan 51%**: Secara teoretis, jika seorang penyerang menguasai lebih dari 50% `hashrate` jaringan, mereka secara statistik dijamin akan bisa melakukan serangan `double-spend` dengan sukses.
* **Insentif Ekonomi**: Namun, bahkan seorang `miner` dengan 51% `hashrate` memiliki insentif kuat untuk **tidak menyerang jaringan**. Melakukan serangan akan menghancurkan kepercayaan pada sistem, yang akan menyebabkan harga koin anjlok. Ini akan membuat investasi besar mereka dalam perangkat keras `mining` dan koin yang mereka tambang menjadi tidak berharga. Jauh lebih menguntungkan bagi mereka untuk bermain jujur dan mengumpulkan hadiah `block`.

### `Transaction Fees`

Ada satu insentif lagi yang perlu diselaraskan. `Block` yang lebih besar membutuhkan waktu lebih lama untuk disebarkan ke seluruh jaringan. Ini meningkatkan risiko `block` tersebut menjadi "yatim" (`orphaned`) jika `miner` lain menemukan `block` yang lebih kecil pada saat yang bersamaan. Hal ini menciptakan insentif bagi `miner` untuk membuat `block` yang kecil atau bahkan kosong.

Solusinya adalah **`transaction fees`**.
* Pengguna dapat secara sukarela menyertakan `fee` dalam `transaction` mereka dengan membuat nilai total `output` sedikit lebih kecil dari nilai total `input`.
* Selisih ini dapat diklaim oleh `miner` yang berhasil menambang `block` yang berisi `transaction` tersebut.
* `Miner` menambahkan total `fee` dari semua `transaction` di `block`-nya ke dalam `output` dari `coinbase transaction` miliknya. **`Block Reward`** kini didefinisikan sebagai **`Block Subsidy` (koin baru) + Total `Transaction Fees`**.

Ini menciptakan **pasar `fee` (`fee market`)**. Pengguna bersaing satu sama lain untuk mendapatkan ruang di dalam `block` yang terbatas dengan menawarkan `fee` yang lebih tinggi. `Miner`, untuk memaksimalkan keuntungan, akan memprioritaskan `transaction` dengan `fee` per byte tertinggi.

Ketika **`block subsidy`** akhirnya menjadi nol setelah bertahun-tahun (karena proses *halving*), `transaction fees` akan menjadi **satu-satunya** sumber pendapatan bagi `miner` dan satu-satunya insentif bagi mereka untuk terus mengamankan jaringan.

---

# Bab 8
## Peer-to-peer network

### Masalah Terakhir: *Shared Folder*

Meskipun `proof-of-work` telah mendesentralisasi proses pembuatan `block`, `block-block` tersebut masih harus melewati satu titik pusat: *shared folder*. Administrator *folder* ini (sebut saja Luke) menjadi otoritas pusat yang baru. Ia memiliki kekuasaan untuk:
* **Melakukan Sensor**: Luke bisa saja menolak untuk menyimpan `block` dari `miner` tertentu (misalnya, karena `block` tersebut berisi `transaction` yang kontroversial), sehingga `block` tersebut tidak akan pernah sampai ke `node` lain.
* **Menjadi Titik Kegagalan**: Jika server *shared folder* mati, seluruh jaringan akan berhenti.
* **Menjadi Hambatan Kinerja (`Bottleneck`)**: Jika ada 100 `node` yang ingin mengunduh `block` 1 MB, *shared folder* harus melayani total lalu lintas data sebesar 100 MB, yang membuat penyebaran `block` menjadi sangat lambat.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_8.2.png" alt="gambar" width="580"/>
</p>

[Ilustrasi administrator shared folder memblokir sebuah block dari miner Rashid, mencegahnya mencapai node lain. - Figure 8.2]

Sistem ini belum benar-benar tahan sensor (`censorship-resistant`) selama masih ada satu entitas yang dapat mengontrol aliran informasi.

### Membangun Jaringan `Peer-to-peer`

Solusinya adalah dengan memungkinkan para `full node` dan `miner` untuk berkomunikasi secara langsung satu sama lain dalam sebuah **`peer-to-peer` (P2P) `network`**.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_8.3.png" alt="gambar" width="580"/>
</p>

[Diagram jaringan P2P di mana node-node terhubung satu sama lain. Sebuah block baru dari Rashid disebarkan dari node ke node. - Figure 8.3]

Jaringan ini berfungsi seperti **jaringan gosip (`gossip network`)**.
* Setiap `node` terhubung ke beberapa `node` lain yang disebut **`peers`**.
* Ketika sebuah `node` menerima informasi baru (seperti `block` atau `transaction`), ia memverifikasinya dan kemudian meneruskannya (`relay`) ke semua `peer`-nya.
* `Peer-peer` tersebut kemudian melakukan hal yang sama, menyebarkan informasi ke seluruh jaringan dalam hitungan detik.

Dalam model ini, sensor menjadi sangat sulit. Jika satu `node` (misalnya Kafe) menolak untuk meneruskan `block` ke Lisa, Lisa akan tetap menerimanya dari `peer` lain yang terhubung dengannya (misalnya Tom atau Qi). Sebuah `node` aman selama ia **terhubung dengan baik (`well-connected`)** ke beberapa `peer` yang beragam.

Jaringan P2P ini tidak hanya digunakan untuk menyebarkan `block`, tetapi juga `transaction`. `Wallet` tidak perlu lagi mengirim email ke `miner`; ia cukup menyiarkan `transaction`-nya ke satu atau beberapa `node`, dan jaringan P2P akan menyebarkannya ke semua `miner`.

#### Bagaimana `Peer` Berkomunikasi?
Komunikasi antar `node` terjadi melalui koneksi internet standar.
* Setiap `node` yang ingin menerima koneksi akan "mendengarkan" pada sebuah **IP address** dan **nomor port TCP** tertentu (port default Bitcoin adalah `8333`).
* `Node` lain kemudian dapat membuat **koneksi TCP** ke alamat tersebut untuk membangun saluran komunikasi dua arah.

Setelah terhubung, mereka harus berbicara dalam "bahasa" yang sama, yang didefinisikan oleh sebuah **protokol jaringan**. Protokol ini menentukan format pesan yang dapat mereka kirimkan satu sama lain, seperti pesan `inv` (`inventory`), yang memberitahu `peer` tentang `transaction` atau `block` baru yang Anda miliki.

### Alur Hidup Sebuah `Transaction` di Jaringan P2P

Mari kita ikuti perjalanan `transaction` John dari awal hingga akhir di jaringan P2P yang sudah berjalan.

**1. John Mengirim `Transaction`**
`Wallet` John, yang merupakan `lightweight client`, terhubung ke `full node` milik Tom. Setelah John membuat dan menandatangani `transaction` pembelian kue, proses pengirimannya adalah sebagai berikut untuk menghemat *bandwidth*:
1.  **`inv`**: `Wallet` John mengirim pesan `inv` ke Tom, yang hanya berisi `txid` dari `transaction` baru tersebut.
2.  **`getdata`**: Tom memeriksa apakah ia sudah memiliki `transaction` dengan `txid` tersebut. Karena belum, ia meminta data lengkapnya dengan mengirimkan pesan `getdata`.
3.  **`tx`**: `Wallet` John merespons dengan pesan `tx` yang berisi data `transaction` lengkap.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_8.12.png" alt="gambar" width="580"/>
</p>

[Diagram tiga langkah komunikasi antara wallet John dan node Tom: inv, getdata, dan tx. - Figure 8.12]

**2. Tom Meneruskan `Transaction`**
Setelah menerima dan memverifikasi `transaction` John, Tom akan memberitahu semua `peer`-nya (Lisa, Qi, Rashid) tentang `transaction` baru ini menggunakan pesan `inv`.
* Para `peer`-nya yang belum memiliki `transaction` tersebut akan merespons dengan `getdata`.
* Jika seorang `peer` (misalnya Lisa) menerima `inv` dari Tom untuk `transaction` yang sudah ia terima dari `peer` lain, Lisa cukup mengabaikan `inv` dari Tom. `Node` melacak `inventory` yang telah mereka lihat untuk menghindari pemrosesan dan pengunduhan yang berulang.

Proses gosip ini terus berlanjut hingga `transaction` John menyebar ke seluruh jaringan.

**3. `Wallet` Kafe Mendapat Notifikasi**
`Wallet` `lightweight` milik kafe terhubung ke `full node` milik kafe sendiri (sebagai *trusted node*).
* Ketika `full node` kafe menerima `transaction` John, ia mengujinya terhadap `bloom filter` yang telah diberikan oleh `wallet` `lightweight`-nya.
* Karena `transaction` ini ditujukan untuk kafe, ia cocok dengan `filter`.
* `Full node` kemudian memberitahu `wallet` `lightweight` (melalui proses `inv` -> `getdata` -> `tx`), yang kemudian menampilkan notifikasi kepada pemilik kafe bahwa ada pembayaran masuk yang **masih menunggu konfirmasi (0-conf)**.

**4. `Transaction` Dimasukkan ke dalam `Block`**
Para `miner` di jaringan (Rashid, Lisa, dll.) telah menerima `transaction` John. Rashid menjadi `miner` yang beruntung dan berhasil menemukan `proof-of-work` untuk `block` baru yang berisi `transaction` John.

**5. `Block` Disebarkan ke Seluruh Jaringan (`Block Propagation`)**
Rashid sekarang harus menyebarkan `block`-nya secepat mungkin. Untuk efisiensi, penyebaran `block` menggunakan protokol yang sedikit berbeda (**BIP130**):
1.  **`headers`**: Rashid mengirim pesan `headers` ke semua `peer`-nya. Pesan ini hanya berisi `block header` (80 byte), bukan seluruh `block`.
2.  **`getdata`**: `Peer` lain dapat dengan sangat cepat memverifikasi `proof-of-work` pada `header`. Jika valid, mereka akan meminta `block` penuh dengan pesan `getdata`.
3.  **`block`**: Rashid merespons dengan data `block` lengkap.

Proses ini jauh lebih cepat daripada mengirim seluruh `block` ke semua orang, karena verifikasi awal yang mahal (`proof-of-work`) dilakukan pada data yang sangat kecil.

**6. `Wallet` `Lightweight` Mendapat Notifikasi Konfirmasi**
* `Full node` (milik Tom dan kafe) menerima `header` dari `block` baru Rashid dan meneruskannya ke `wallet` `lightweight` yang terhubung.
* `Wallet` John dan kafe melihat ada `block` baru. Untuk memverifikasi bahwa `transaction` mereka ada di dalamnya tanpa mengunduh seluruh `block`, mereka meminta **`merkleblock`** dari `full node`.
* `Full node` merespons dengan `merkleblock`, yang berisi `block header` dan `merkle proof` yang diperlukan. `Wallet` memverifikasi bukti ini.
* Setelah verifikasi berhasil, `wallet` kini dapat dengan yakin menampilkan bahwa `transaction` tersebut telah memiliki **1 konfirmasi**.

Seiring berjalannya waktu dan lebih banyak `block` ditambang di atasnya, jumlah konfirmasi akan terus bertambah, membuat `transaction` semakin aman dari serangan `double-spend`.

### Meninggalkan Sistem *Cookie Token*

Pada titik ini, sistem yang telah kita bangun—dengan `HD wallets`, `transactions`, `blockchain`, `proof of work`, dan jaringan `peer-to-peer`—secara fungsional identik dengan Bitcoin. Analogi *cookie token* telah mencapai tujuannya. Mulai sekarang, kita akan membahas Bitcoin secara langsung.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_8.25.png" alt="gambar" width="580"/>
</p>

[Rangkuman visual evolusi sistem cookie token dari spreadsheet sederhana di Bab 3 hingga jaringan P2P yang terdesentralisasi penuh di Bab 8. - Figure 8.25]

### Bootstrapping Jaringan: Bagaimana `Node` Baru Bergabung?

Bagaimana sebuah `node` yang benar-benar baru (milik Selma) bisa bergabung dengan jaringan? Ia tidak tahu alamat IP `node` lain. Proses ini disebut **`bootstrapping`**.

**Langkah 1: Menjalankan Perangkat Lunak**
Selma mengunduh perangkat lunak `full node`, seperti **Bitcoin Core**.
* **Verifikasi Perangkat Lunak (Sangat Penting!)**: Sebelum menjalankan perangkat lunak, ia harus memverifikasi tanda tangan digital dari pengembang. Ini untuk memastikan perangkat lunak tersebut asli dan belum dimodifikasi oleh peretas. Proses ini melibatkan:
    1.  Mengunduh file program dan file tanda tangan (`.asc`).
    2.  Mendapatkan `public key` pengembang dari beberapa sumber terpercaya (situs web resmi, buku ini, teman) dan memverifikasi **`fingerprint`**-nya.
    3.  Menggunakan `public key` tersebut untuk memeriksa validitas tanda tangan pada file program.

**Langkah 2: Terhubung ke `Node` Lain**
`Node` Selma yang baru dimulai perlu menemukan beberapa `peer` pertama. Ia menggunakan beberapa metode:
1.  **`DNS Seeds`**: Bitcoin Core memiliki daftar nama domain (`DNS seed`) yang *hardcoded*. Ketika dijalankan, ia akan menanyakan ke server DNS untuk mendapatkan daftar alamat IP dari `node-node` aktif.
2.  **Daftar *Hardcoded***: Sebagai cadangan, perangkat lunak juga memiliki daftar alamat IP `node` yang stabil yang juga *hardcoded*.
3.  **Manual**: Pengguna dapat secara manual menambahkan alamat IP `peer`.

Setelah mendapatkan beberapa alamat, `node`-nya akan membuat koneksi TCP dan melakukan **`handshake`**: bertukar pesan `version` untuk menyetujui versi protokol dan menginformasikan `block height` masing-masing.

**Langkah 3: Sinkronisasi (`Initial Blockchain Download` - IBD)**
Selma perlu mengunduh seluruh histori `blockchain` untuk membangun `UTXO set`-nya sendiri.
* **Headers-First Sync**: Untuk efisiensi dan keamanan, `node`-nya pertama-tama akan mengunduh **seluruh rantai `block header`** dari satu `peer`. Ini cepat karena `header` berukuran kecil, dan memungkinkan `node`-nya untuk memverifikasi rantai `proof-of-work` terkuat sebelum mengunduh data `transaction` yang besar.
* **Download `Block`**: Setelah memiliki rantai `header` yang tervalidasi, ia mulai mengunduh `block` penuh secara paralel dari beberapa `peer`.
* **Optimalisasi `Assumevalid`**: Untuk mempercepat proses IBD yang bisa memakan waktu berhari-hari, Bitcoin Core memiliki `hash` `block` yang *hardcoded* dari beberapa minggu sebelum rilis. `Node` akan "mengasumsikan" semua tanda tangan sebelum `block` ini valid dan melewatkan pemeriksaan skripnya (meskipun tetap memproses `transaction` untuk membangun `UTXO set`). Ini secara dramatis mengurangi waktu sinkronisasi.

**Langkah 4: Operasi Normal**
Setelah `blockchain` sepenuhnya diunduh dan diverifikasi, `node` Selma kini menjadi peserta penuh dalam jaringan P2P, menerima dan menyebarkan `transaction` dan `block` baru seperti `node` lainnya.

Bab ini telah melengkapi fondasi teknis Bitcoin. Kita telah beralih dari sistem terpusat yang sederhana menjadi jaringan moneter global yang terdesentralisasi dan tahan sensor.

---

# Bab 9
## Transactions Revisited

Bab ini merupakan kelanjutan dari konsep `transaction` yang telah diperkenalkan sebelumnya. Jika bab-bab awal menjelaskan anatomi dasar sebuah `transaction`, bab ini mengeksplorasi fitur-fitur canggih yang membuatnya lebih dari sekadar alat transfer nilai. Fitur-fitur ini, seperti *time locks* dan *programmable scripts*, adalah fondasi dari banyak aplikasi tingkat lanjut di atas `blockchain` Bitcoin, termasuk kontrak digital.

### Time-locked Transactions

Konsep inti dari *time-locked transaction* adalah sebuah `transaction` yang sudah ditandatangani dan valid secara kriptografis, namun tidak dapat dimasukkan ke dalam `block` (dan oleh karena itu tidak dapat dikonfirmasi) hingga kondisi waktu tertentu terpenuhi.

Untuk mengaktifkan fitur ini, ada dua komponen utama dalam sebuah `transaction` yang digunakan: `locktime` dan `sequence number`.

* **`locktime`**: Field di level `transaction` yang menentukan waktu paling awal (bisa dalam format timestamp atau block height) `transaction` tersebut valid untuk ditambang.
* **`sequence number`**: Field 32-bit di setiap *input* `transaction`. Agar `locktime` pada sebuah `transaction` dapat berfungsi, setidaknya salah satu `sequence number` dari input-inputnya harus diatur ke nilai yang lebih kecil dari `ffffffff`. Jika semua `sequence number` adalah `ffffffff`, `locktime` akan diabaikan oleh jaringan.

**Skenario Penggunaan: Warisan Digital**

Buku ini memberikan contoh yang sangat baik: Anda ingin memberikan 100 bitcoin kepada putri Anda, tetapi hanya setelah Anda meninggal dunia. Anda bisa membuat sebuah `transaction` yang terkunci waktu (*time-locked*) satu tahun ke depan.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_9.1.png" alt="gambar" width="580"/>
</p>

[Diagram transaksi time-locked yang mengirim 100 BTC kepada anak perempuan, valid pada 30 April 2019. - Figure 9.1]

Anda membuat `transaction` (Tx1) yang ditandatangani, lalu memberikannya kepada putri Anda untuk disimpan. `Transaction` ini belum disiarkan ke jaringan. Jika Anda meninggal sebelum tanggal `locktime` tercapai, putri Anda dapat menyiarkan `transaction` tersebut setelah tanggal yang ditentukan untuk mengklaim dananya.

Namun, bagaimana jika Anda masih hidup setelah tanggal itu? Anda tentu tidak ingin putri Anda bisa mengambil uang tersebut. Di sinilah letak kerumitannya. Untuk membatalkan Tx1, Anda harus membuat `transaction` baru (Tx2) yang membelanjakan salah satu *output* yang sama yang digunakan oleh Tx1 (*double-spend*). Karena Tx2 tidak memiliki `locktime`, Anda bisa menyiarkannya sebelum `locktime` Tx1 tercapai. Setelah Tx2 terkonfirmasi, Tx1 menjadi tidak valid selamanya.

Untuk tetap adil kepada putri Anda, sebelum menyiarkan Tx2, Anda membuat `transaction` *time-locked* baru (Tx3) yang berlaku satu tahun lagi, yang membelanjakan *output* dari Tx2, lalu memberikannya kepada putri Anda.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_9.2.png" alt="gambar" width="580"/>
</p>

[Proses membatalkan transaksi time-locked lama (Tx1) dengan transaksi baru (Tx2), dan membuat transaksi time-locked berikutnya (Tx3). - Figure 9.2]

> **Poin Kritis untuk Auditor**: Urutan operasi di sini sangat penting. Tx3 harus diberikan kepada putri Anda *sebelum* Tx2 disiarkan. Jika tidak, ada risiko Anda meninggal setelah menyiarkan Tx2 tetapi sebelum memberikan Tx3, yang akan menyebabkan dana warisan hilang. Selain itu, skenario ini rentan terhadap **`transaction malleability`**, sebuah konsep yang akan dibahas lebih dalam di Bab 10, di mana `txid` dari Tx2 bisa berubah sebelum dikonfirmasi, sehingga membuat Tx3 tidak valid.

#### Time Measurements

`Locktime` dapat diekspresikan dalam dua cara:

1.  **Block Time (Timestamp)**: Menggunakan Unix timestamp. Sebuah `transaction` valid jika **Median Time Past (MTP)** dari 11 `block` terakhir lebih besar dari nilai `locktime` `transaction` tersebut. MTP digunakan alih-alih timestamp `block` saat ini untuk mencegah manipulasi oleh `miners`.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_9.3.png" alt="gambar" width="580"/>
</p>

    [Ilustrasi validasi locktime berdasarkan Median Time Past dari 11 block terakhir. - Figure 9.3]

2.  **Block Height**: Menggunakan nomor `block`. `Transaction` tidak valid sampai `block` dengan nomor yang ditentukan telah ditambang. Contohnya, jika `locktime` adalah 571019, `transaction` baru bisa dimasukkan ke dalam `block` 571020 atau setelahnya.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_9.4.png" alt="gambar" width="580"/>
</p>

    [Contoh transaksi time-locked berdasarkan block height. - Figure 9.4]

#### Relative Time Locks

Berbeda dengan *absolute time locks* yang merujuk pada waktu atau `block height` absolut, *relative time locks* mengunci sebuah *input* berdasarkan waktu konfirmasi dari *output* yang dibelanjakannya. Fitur ini diaktifkan melalui `sequence number` di setiap input dan memerlukan `transaction` version 2 atau lebih tinggi (**BIP68**).

`Sequence number` diinterpretasikan sebagai bitfield:
* **Bit 31 (paling kiri)**: Jika `0`, *relative lock* aktif. Jika `1`, tidak aktif.
* **Bit 22**: Jika `1`, nilai 16 bit terakhir diartikan sebagai kelipatan 512 detik. Jika `0`, diartikan sebagai jumlah `block`.
* **Bit 0-15**: Nilai *time lock* itu sendiri (baik dalam jumlah `block` atau kelipatan 512 detik).

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_9.5.png" alt="gambar" width="580"/>
</p>

[Diagram transaksi dengan dua input yang memiliki relative time lock berbeda: satu berbasis waktu (30 hari), satu lagi berbasis jumlah block (1000 block). - Figure 9.5]

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_9.6.png" alt="gambar" width="580"/>
</p>

[Penjelasan bitfield dari sequence number untuk relative lock berbasis waktu. - Figure 9.6]

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_9.7.png" alt="gambar" width="580"/>
</p>

[Penjelasan bitfield dari sequence number untuk relative lock berbasis jumlah block. - Figure 9.7]

### Time-locked Outputs

Selain mengunci seluruh `transaction`, kita juga bisa mengunci sebuah *output* spesifik, sehingga siapa pun yang ingin membelanjakannya harus memenuhi kondisi waktu yang ditentukan dalam `script` output tersebut.

#### Absolute Time-locked Outputs

Fitur ini diimplementasikan menggunakan `script` operator **`OP_CHECKLOCKTIMEVERIFY`** atau **`OP_CLTV`** (**BIP65**).

Contohnya, Anda ingin memberi uang saku kepada putri Anda yang baru bisa dibelanjakan pada tanggal 1 Mei. Anda membuat `transaction` dengan `script` output yang mengandung `OP_CLTV`.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_9.8.png" alt="gambar" width="580"/>
</p>

[Transaksi dengan satu output yang dikunci hingga 1 Mei menggunakan OP_CLTV. - Figure 9.8]

`Script`-nya akan terlihat seperti ini:
`<timestamp 1 Mei> OP_CLTV OP_DROP OP_DUP OP_HASH160 <PKHD> OP_EQUALVERIFY OP_CHECKSIG`

Cara kerjanya:
* `Transaction` yang membelanjakan output ini *harus* memiliki `locktime` yang lebih besar atau sama dengan `<timestamp 1 Mei>`.
* `OP_CLTV` akan memeriksa `locktime` dari `transaction` pembelanja. Jika tidak memenuhi syarat, `script` akan gagal.
* Jika berhasil, eksekusi dilanjutkan ke verifikasi `signature` seperti biasa.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_9.9.png" alt="gambar" width="580"/>
</p>

[Ilustrasi beberapa transaksi yang mencoba membelanjakan output OP_CLTV, menunjukkan mana yang valid dan tidak valid berdasarkan locktime-nya. - Figure 9.9]

#### Relative Time-locked Outputs

Fitur ini diimplementasikan menggunakan **`OP_CHECKSEQUENCEVERIFY`** atau **`OP_CSV`** (**BIP112**). `Script` ini memastikan bahwa sejumlah `block` atau waktu tertentu telah berlalu sejak *output* yang dikunci ini dikonfirmasi.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_9.10.png" alt="gambar" width="580"/>
</p>

[Konsep relative time-locked output, di mana output hanya bisa dibelanjakan setelah 3 block terkonfirmasi di atasnya. - Figure 9.10]

`OP_CSV` sangat krusial untuk kontrak digital canggih, seperti *atomic swaps*.

### Atomic Swaps

*Atomic swap* adalah protokol untuk menukar aset kripto dari dua `blockchain` yang berbeda (misalnya, Bitcoin dan Namecoin) antara dua pihak yang tidak saling percaya, tanpa memerlukan pihak ketiga (seperti bursa). Disebut "atomic" karena pertukaran ini dijamin berhasil sepenuhnya atau gagal sepenuhnya, tidak ada kondisi di mana salah satu pihak bisa kabur dengan dana pihak lain.

**Skenario:** John ingin menukar 2 BTC miliknya dengan 100 NMC milik Fadime.

**Mekanisme Kunci:**
1.  **Secret (S) dan Hash (H)**: John membuat sebuah angka rahasia acak (`S`) dan menghitung hash-nya (`H = SHA256(S)`). John merahasiakan `S` tetapi membagikan `H` kepada Fadime.
2.  **Contract Transactions**: Kedua belah pihak membuat `transaction` di `blockchain` masing-masing yang dikunci dengan `script` khusus. `Transaction` ini menggunakan `p2sh` (Pay-to-Script-Hash).
    * **`Redeem script` John (di Bitcoin)**:
        * **Kondisi 1 (Swap)**: Fadime dapat mengklaim 2 BTC jika ia bisa memberikan `S` (pre-image dari `H`) dan `signature`-nya.
        * **Kondisi 2 (Refund)**: John dapat mengambil kembali 2 BTC-nya jika Fadime tidak mengklaimnya setelah 48 jam (*relative time lock*).
    * **`Redeem script` Fadime (di Namecoin)**:
        * **Kondisi 1 (Swap)**: John dapat mengklaim 100 NMC jika ia bisa memberikan `S` dan `signature`-nya.
        * **Kondisi 2 (Refund)**: Fadime dapat mengambil kembali 100 NMC-nya jika John tidak mengklaimnya setelah 24 jam.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_9.11.png" alt="gambar" width="580"/>
</p>

[Diagram dua contract transaction untuk atomic swap, satu di blockchain Bitcoin dan satu di Namecoin, keduanya menggunakan redeem script dengan dua kondisi. - Figure 9.11]

> **Poin Kritis untuk Auditor**: Perhatikan perbedaan *timeout*. *Timeout* Fadime (24 jam) lebih pendek daripada John (48 jam). Ini penting karena John harus bertindak lebih dulu untuk mengklaim NMC, yang akan membuka rahasia `S`. Fadime diberikan waktu yang lebih pendek untuk membatalkan jika John tidak bertindak, sementara John diberikan waktu lebih lama untuk mengklaim kembali dananya jika terjadi masalah setelah ia mengungkapkan `S`.

**Alur Eksekusi:**
1.  John menyiarkan *contract transaction*-nya di `blockchain` Bitcoin. Fadime menunggu konfirmasi.
2.  Setelah terkonfirmasi, Fadime menyiarkan *contract transaction*-nya di `blockchain` Namecoin. John menunggu konfirmasi.
3.  John mengklaim 100 NMC dengan menyiarkan *swap transaction* di Namecoin. `Transaction` ini **mengungkapkan rahasia `S`** di dalam `script`-nya agar valid.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_9.12.png" alt="gambar" width="580"/>
</p>

    [Langkah pertama swap, di mana John mengklaim Namecoin dengan mengungkapkan rahasia S. - Figure 9.12]
4.  Fadime memantau `blockchain` Namecoin, melihat `S` yang diungkapkan oleh John.
5.  Fadime menggunakan `S` tersebut untuk membuat *swap transaction*-nya di `blockchain` Bitcoin untuk mengklaim 2 BTC.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_9.13.png" alt="gambar" width="580"/>
</p>

    [Langkah kedua swap, di mana Fadime menggunakan rahasia S untuk mengklaim Bitcoin. - Figure 9.13]

Jika ada pihak yang tidak kooperatif (misalnya, Fadime tidak menyiarkan `transaction`-nya), pihak lain dapat mengklaim kembali dananya setelah periode *timeout* berakhir.

### Storing stuff in the Bitcoin blockchain

`Blockchain` Bitcoin adalah basis data publik yang abadi, yang membuatnya menarik untuk menyimpan data arbitrer. Praktik awalnya adalah dengan menyisipkan data ke dalam `transaction` dengan cara yang tidak efisien.

Contoh historis yang diberikan adalah sebuah *tribute* untuk Len Sassaman yang disematkan dalam sebuah `transaction`. Ini dilakukan dengan membuat banyak *output* `p2pkh` di mana `PKH` (Public Key Hash) bukanlah hash dari `public key` sungguhan, melainkan data ASCII yang di-encode.

> **Poin Kritis untuk Auditor**: Praktik ini menyebabkan masalah serius yang disebut **Bloated UTXO set**. Karena `PKH` tersebut palsu, tidak ada `private key` yang dapat digunakan untuk membelanjakan *output* tersebut. Akibatnya, *output* ini menjadi *unspendable* (tidak dapat dibelanjakan) dan akan tersimpan selamanya di dalam `UTXO set` semua `full node`, membebani memori dan sumber daya jaringan.

**Solusi: `OP_RETURN`**

Untuk memfasilitasi penyimpanan data tanpa membebani `UTXO set`, `OP_RETURN` diperkenalkan.
* `OP_RETURN` adalah sebuah `script` operator yang secara otomatis membuat sebuah *output* menjadi **provably unspendable** (terbukti tidak dapat dibelanjakan).
* Ketika `full node` melihat `output` dengan `OP_RETURN`, ia tahu bahwa `output` tersebut tidak perlu dimasukkan ke dalam `UTXO set`.
* Ada kebijakan jaringan (bukan aturan konsensus) yang membatasi ukuran data `OP_RETURN` (saat ini sekitar 80 byte) dan hanya mengizinkan satu `output` `OP_RETURN` per `transaction`.

**Contoh Penggunaan: Token Kepemilikan Mobil**

Buku ini mengilustrasikan pembuatan token sederhana di atas Bitcoin. Produsen mobil "Ampere" membuat `transaction` untuk setiap mobil baru.
* **Pembuatan Token**: Ampere membuat `transaction` yang membelanjakan koin dari alamatnya sendiri (`PKHA`), dengan `output` pertama ditujukan kembali ke alamatnya, dan sebuah `output` `OP_RETURN` yang berisi data seperti `"ampere <nomor sasis>"`.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_9.14.png" alt="gambar" width="580"/>
</p>

    [Ampere membuat token mobil baru dengan transaksi OP_RETURN. - Figure 9.14]
* **Transfer Token**: Untuk mentransfer kepemilikan (misalnya, ke dealer dengan `PKHD`), Ampere membelanjakan *output* token sebelumnya, dengan `output` pertama dari `transaction` baru ini ditujukan ke `PKHD`. Rantai kepemilikan ini dapat dilacak di `blockchain`.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_9.15.png" alt="gambar" width="580"/>
</p>

lalu

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_9.16.png" alt="gambar" width="580"/>
</p>

    [Ampere mentransfer token mobil ke dealer. - Figure 9.15 & 9.16]
* **Bukti Kepemilikan**: Pemilik mobil yang sah dapat membuktikan kepemilikannya dengan menandatangani sebuah *challenge* (pesan acak) dari mobil menggunakan `private key` yang sesuai dengan `PKH` pemilik saat ini di `blockchain`.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_9.17.png" alt="gambar" width="580"/>
</p>

    [Fadime menyalakan mobilnya dengan menandatangani challenge-response. - Figure 9.17]

### Replacing pending transactions

Terkadang sebuah `transaction` bisa "macet" (tertunda konfirmasinya) karena `fee` yang dibayarkan terlalu rendah. Ada dua mekanisme utama untuk mengatasi ini:

#### Opt-in Replace-by-Fee (RBF)

**BIP125** memperkenalkan RBF, sebuah kebijakan di mana pengirim dapat menandai `transaction`-nya agar bisa diganti.
* **Mekanisme**: Jika setidaknya satu `sequence number` dari input `transaction` diatur ke nilai yang lebih rendah dari `ffffffe`, `transaction` tersebut dianggap dapat diganti.
* **Proses**: Jika `transaction` asli macet, pengirim dapat membuat `transaction` baru yang membelanjakan input yang sama tetapi dengan `fee` yang lebih tinggi. `Node` yang mendukung kebijakan RBF akan menerima `transaction` baru ini dan membuang yang lama.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_9.20.png" alt="gambar" width="580"/>
</p>

[Perbandingan transaksi asli yang macet dan transaksi pengganti RBF dengan fee lebih tinggi. - Figure 9.20]

Jika RBF tidak diaktifkan, sebagian besar `node` akan mengikuti kebijakan *first-seen*, yaitu menolak `transaction` kedua sebagai upaya *double-spend*.

#### Child Pays for Parent (CPFP)

CPFP adalah metode di mana *penerima* atau *pengirim* (melalui *change output*) dapat "mempercepat" konfirmasi `transaction` yang macet.
* **Mekanisme**: Buat `transaction` baru (*child*) yang membelanjakan salah satu *output* dari `transaction` yang macet (*parent*).
* **Proses**: `Transaction` *child* ini dibuat dengan `fee` yang sangat tinggi. `Miner` yang ingin mengklaim `fee` tinggi dari *child* harus menambang `transaction` *parent*-nya terlebih dahulu agar *child* menjadi valid. Dengan demikian, `fee` gabungan dari kedua `transaction` menjadi cukup menarik bagi `miner`.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_9.22.png" alt="gambar" width="580"/>
</p>

[Diagram Child Pays for Parent, di mana transaksi anak dengan fee tinggi mendorong miner untuk menambang transaksi induk yang macet. - Figure 9.22]

### Different signature types

Sebuah `signature` dalam Bitcoin tidak selalu harus mengunci seluruh `transaction`. Perilaku `signature` dapat diubah menggunakan **`SIGHASH flag`**, sebuah byte yang ditambahkan ke akhir `signature`.

Ini memungkinkan kontrol granural atas bagian mana dari `transaction` yang dikunci oleh `signature`. Ada dua kategori `flag`:

**1. Mode untuk Output:**
* **`SIGHASH_ALL` (default)**: Mengunci semua input dan semua output. `Signature` menjadi tidak valid jika ada bagian dari `transaction` (selain `scriptSig`) yang diubah.
* **`SIGHASH_SINGLE`**: Mengunci semua input, tetapi hanya mengunci *output* yang memiliki indeks yang sama dengan *input* yang sedang ditandatangani. `Output` lain bisa diubah.
* **`SIGHASH_NONE`**: Mengunci semua input, tetapi tidak ada *output* yang dikunci. Siapa pun dapat mengubah tujuan dana.

**2. Mode untuk Input:**
* **`SIGHASH_ANYONECANPAY`**: `Flag` ini dapat dikombinasikan dengan salah satu dari tiga mode di atas. `Flag` ini hanya mengunci *input* yang sedang ditandatangani. Input lain dapat ditambahkan, dihapus, atau diubah. Ini berguna untuk skenario *crowdfunding*, di mana banyak orang dapat "ikut membayar" dengan menambahkan input mereka sendiri ke `transaction` yang sudah ada.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_9.24.png" alt="gambar" width="580"/>
</p>

[Ilustrasi visual dari enam kombinasi SIGHASH flag yang berbeda dan bagian mana dari transaksi yang dikunci oleh masing-masing. - Figure 9.24]

Kombinasi `flag` ini memungkinkan pembuatan kontrak digital yang sangat fleksibel.

---

# Bab 10
## Segregated Witness

Bab ini membahas salah satu pembaruan teknis paling signifikan pada protokol Bitcoin, yang dikenal sebagai **`Segregated Witness`** (disingkat **`segwit`**). `Segregated Witness` secara harfiah berarti "saksi yang dipisahkan". Dalam konteks Bitcoin, "saksi" atau **`witness`** adalah data tanda tangan (`signature`) yang membuktikan otorisasi sebuah `transaction`. `Segwit` adalah mekanisme yang memisahkan data `witness` ini dari bagian utama `transaction`.

Pembaruan ini dirancang dengan sangat hati-hati untuk mengatasi beberapa masalah fundamental dalam desain asli Bitcoin, sekaligus diimplementasikan sebagai sebuah `soft fork`, yang berarti `node` lama yang belum diperbarui tetap dapat beroperasi di jaringan tanpa menyebabkan perpecahan. Bab ini akan menguraikan masalah-masalah tersebut dan bagaimana `segwit` menyelesaikannya secara elegan.

### Masalah yang Diselesaikan oleh Segwit

Sebelum kita menyelami cara kerja `segwit`, penting untuk memahami masalah-masalah yang mendorong pembuatannya.

#### Transaction Malleability

`Transaction malleability` adalah kerentanan di mana `signature` dari sebuah `transaction` dapat diubah oleh pihak ketiga (misalnya, sebuah `node` di jaringan) tanpa membuat `transaction` tersebut menjadi tidak valid. Meskipun perubahan ini tidak dapat mengubah pengirim, penerima, atau jumlah dana, perubahan sekecil apa pun pada data `transaction` akan menghasilkan **`txid`** (ID `transaction`) yang sama sekali berbeda.

Ingat kembali contoh warisan dari Bab 9: Kita memberikan `transaction` `time-locked` (Tx3) kepada putri Kita yang membelanjakan *output* dari `transaction` lain (Tx2) yang belum dikonfirmasi.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_10.1.png" alt="gambar" width="580"/>
</p>

[Diagram alur transaksi warisan dari Bab 9, menunjukkan ketergantungan Tx3 pada Tx2. - Figure 10.1]

Ketika Kita menyiarkan Tx2 ke jaringan, sebuah `node` jahat (misalnya, `node` milik Qi) dapat mencegatnya. Qi dapat memodifikasi data `signature` di dalam Tx2 untuk membuat `transaction` baru yang termodifikasi, Tx2M. Tx2M ini valid, membelanjakan input yang sama, dan mengirim dana ke tujuan yang sama, tetapi memiliki `txid` yang berbeda dari Tx2.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_10.2.png" alt="gambar" width="580"/>
</p>

[Ilustrasi bagaimana transaksi Tx2 diubah menjadi Tx2M oleh node jahat saat disiarkan di jaringan. - Figure 10.2]

Jika `miner` akhirnya menambang Tx2M, maka `transaction` asli Kita, Tx2, menjadi tidak valid. Akibatnya, `transaction` warisan putri Kita, Tx3, yang merujuk pada `txid` dari Tx2, juga menjadi **tidak valid selamanya**. Dana warisan tersebut akan hilang.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_10.3.png" alt="gambar" width="580"/>
</p>

[Diagram yang menunjukkan Tx3 menjadi tidak valid karena txid dari Tx2 telah berubah menjadi txid dari Tx2M yang dikonfirmasi. - Figure 10.3]

**Bagaimana Malleability Dilakukan?**

Ada beberapa cara untuk mengubah data `signature` (`scriptSig`) tanpa membatalkan validitasnya:
1.  **Mengubah Format Encoding `Signature`**: `Signature` dalam Bitcoin menggunakan format encoding standar (DER). Ada beberapa cara untuk merepresentasikan `signature` yang sama dalam format ini yang sedikit berbeda secara bita namun tetap valid secara matematis. (Masalah ini sebagian besar telah diatasi oleh **BIP66**).
2.  **Trik Kriptografis**: `Signature` ECDSA memiliki properti di mana nilai `s`-nya dapat dinegasikan (`s` menjadi `-s mod n`) dan `signature` tetap valid. Ini adalah bentuk `malleability` yang paling umum.
3.  **Menambahkan Opcode Redundan**: Menambahkan `opcode` yang tidak mengubah hasil eksekusi `script` ke dalam `scriptSig`, seperti `OP_DUP` diikuti oleh `OP_DROP`.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_10.4.png" alt="gambar" width="580"/>
</p>

[Tiga cara untuk melakukan transaction malleability: mengubah format signature, trik kriptografi, dan menambahkan opcode redundan. - Figure 10.4]

Meskipun `node` modern memiliki kebijakan *relay* untuk mencegah `transaction` yang termodifikasi, seorang `miner` tetap dapat memasukkan `transaction` tersebut ke dalam `block` secara langsung.

#### Inefisiensi Verifikasi Signature

Proses verifikasi `signature` pada `transaction` lawas (non-`segwit`) memiliki inefisiensi performa yang signifikan. Masalahnya terletak pada cara data di-hash sebelum ditandatangani. Untuk setiap *input* yang ditandatangani, hampir seluruh data `transaction` di-hash ulang.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_10.5.png" alt="gambar" width="580"/>
</p>

[Proses penandatanganan input pertama dalam transaksi, di mana pubkey script dari output yang dibelanjakan disalin ke dalam signature script. - Figure 10.5]

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_10.6.png" alt="gambar" width="580"/>
</p>

[Proses penandatanganan input kedua dalam transaksi, di mana proses hashing yang serupa diulang. - Figure 10.6]

Akibatnya, waktu verifikasi meningkat secara **kuadratik (O(n²))** seiring dengan jumlah input. Jika `transaction` dengan 2 input membutuhkan waktu 1 ms untuk diverifikasi, `transaction` dengan 4 input akan membutuhkan sekitar 4 ms. `Transaction` dengan 1.024 input bisa memakan waktu lebih dari 4 menit.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_10.7.png" alt="gambar" width="580"/>
</p>

[Grafik yang menunjukkan pertumbuhan waktu verifikasi kuadratik seiring bertambahnya jumlah input dalam transaksi. - Figure 10.7]

Ini membuka celah untuk serangan *Denial-of-Service* (DoS), di mana penyerang dapat membuat `block` yang penuh dengan `transaction` multi-input yang kompleks, menyebabkan `node` di seluruh jaringan menjadi lambat atau bahkan macet.

#### Pemborosan Bandwidth

`Lightweight wallet` (atau `SPV wallet`) tidak memverifikasi `signature` karena mereka tidak memiliki `UTXO set` lengkap. Namun, untuk memverifikasi bahwa `transaction` mereka termasuk dalam sebuah `block` (melalui `merkle proof`), mereka harus mengunduh `transaction` secara lengkap, termasuk semua data `signature`-nya. Ini karena `txid` dihitung dari seluruh data `transaction`, termasuk `signature`.

Data `signature` (`scriptSig`) bisa memakan lebih dari 60-70% dari total ukuran `transaction`, terutama pada `transaction` dengan banyak input. Ini adalah pemborosan `bandwidth` yang signifikan bagi pengguna `lightweight wallet`.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_10.8.png" alt="gambar" width="580"/>
</p>

[Ilustrasi mengapa lightweight wallet membutuhkan seluruh data transaksi, termasuk signature, untuk memverifikasi merkle proof. - Figure 10.8]

#### Kesulitan Pembaruan Script

Bahasa `Script` Bitcoin memiliki ruang terbatas untuk pembaruan. Sebelumnya, pembaruan seperti `OP_CLTV` dan `OP_CSV` dilakukan dengan mendefinisikan ulang fungsi dari `opcode` `OP_NOP` yang tidak terpakai.

Keterbatasannya adalah:
* Hanya ada 10 `OP_NOP` yang tersedia.
* `Opcode` baru harus berperilaku persis seperti `NOP` (tidak melakukan apa-apa pada `stack`) jika berhasil dieksekusi, untuk menjaga kompatibilitas dengan `node` lama. Ini membatasi desain `opcode` baru (misalnya, mengapa `OP_CLTV` harus diikuti oleh `OP_DROP`).

Dibutuhkan mekanisme pembaruan yang lebih fleksibel dan dapat diperluas di masa depan.

### Solusi: Cara Kerja Segwit

`Segwit` menyelesaikan semua masalah di atas dengan satu perubahan fundamental: **memisahkan data `witness` dari data inti `transaction`**.

* Pada `transaction` lawas (legacy), `txid` dihitung dari semua data, termasuk `signature`.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_10.10.png" alt="gambar" width="580"/>
</p>

    [Anatomi transaksi legacy di mana txid mencakup signature script. - Figure 10.10]
* Pada `transaction` `segwit`, `scriptSig` pada dasarnya kosong. Data `signature` dan `public key` dipindahkan ke struktur data terpisah yang disebut `witness`, yang dilampirkan pada `transaction`.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_10.11.png" alt="gambar" width="580"/>
</p>

    [Anatomi transaksi segwit di mana txid tidak lagi mencakup data signature yang telah dipisahkan ke dalam field witness. - Figure 10.11]

Dengan memisahkan `witness`, `txid` tidak lagi bergantung pada data `signature`. Ini secara efektif **menghilangkan semua vektor `transaction malleability` pihak ketiga**.

#### Segwit Addresses

Untuk menerima dana ke `wallet` `segwit`, jenis alamat baru diperkenalkan. Alamat ini menggunakan skema encoding **Bech32** (**BIP173**) dan memiliki format yang berbeda.

Contoh alamat `segwit` (P2WPKH): `bc1qeqzjk7vume5wmrdgz5xyehh54cchdjag6jdmkj`

Keunggulan Bech32 dibandingkan Base58check (alamat lawas):
* **Tidak case-sensitive**: Semua karakter dalam huruf kecil, memudahkan penulisan dan pembacaan.
* **Deteksi error lebih baik**: Mampu mendeteksi hingga 4 kesalahan karakter dengan jaminan 100%.

Struktur alamat Bech32 terdiri dari:
1.  **Human-Readable Part (HRP)**: `bc` untuk `mainnet` Bitcoin.
2.  **Separator**: Angka `1`.
3.  **Data Part**: Meng-encode dua informasi:
    * **Witness Version**: Angka 0-16 yang memungkinkan pembaruan `script` di masa depan.
    * **Witness Program**: Data inti (misalnya, `PKH` atau `script hash`).

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_10.12.png" alt="gambar" width="580"/>
</p>

[Proses decoding alamat segwit Bech32 untuk mengekstrak witness version dan witness program. - Figure 10.12]

Ketika seseorang mengirim dana ke alamat `segwit` ini, mereka membuat `output` `transaction` dengan `pubkey script` yang sangat sederhana, hanya berisi `witness version` dan `witness program`.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_10.13.png" alt="gambar" width="580"/>
</p>

[Contoh output transaksi yang dikirim ke alamat segwit, hanya berisi version byte dan witness program. - Figure 10.13]

#### Menghabiskan Output Segwit

Saat Kita ingin membelanjakan dana dari `output` `segwit`, Kita membuat `transaction` di mana:
* `scriptSig`-nya kosong.
* `Signature` dan `public key` ditempatkan di dalam *field* `witness` yang terpisah.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_10.14.png" alt="gambar" width="580"/>
</p>

[Transaksi yang membelanjakan output segwit, dengan scriptSig kosong dan data signature di dalam field witness. - Figure 10.14]

#### Verifikasi Transaksi Segwit

**Pada `Node` Baru (Segwit-aware):**
1.  `Node` mengenali pola `pubkey script` segwit: `<version_byte> <witness_program>`.
2.  `Node` memeriksa `witness version`. Saat ini, hanya versi 0 yang didefinisikan.
3.  Berdasarkan panjang `witness program` (untuk versi 0), `node` menentukan jenisnya:
    * **20 byte**: **P2WPKH** (Pay-to-Witness-Public-Key-Hash).
    * **32 byte**: **P2WSH** (Pay-to-Witness-Script-Hash).
4.  Untuk P2WPKH, `node` menggunakan *template* `script` P2PKH standar, tetapi mengambil `PKH` dari `witness program` dan `signature`/`public key` dari *field* `witness`.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_10.15.png" alt="gambar" width="580"/>
</p>

[Proses verifikasi transaksi P2WPKH oleh node segwit-aware. - Figure 10.15]

**Pada `Node` Lama (Non-segwit):**
Ini adalah bagian jenius dari desain `soft fork` `segwit`.
1.  `Node` lama tidak mengenali *field* `witness` dan mengabaikannya.
2.  Ia melihat `transaction` dengan `scriptSig` kosong dan `pubkey script` yang hanya berisi dua data push (`version byte` dan `witness program`).
3.  Saat `script` ini dieksekusi, dua nilai non-nol didorong ke `stack`. Item teratas `stack` adalah non-nol, yang diinterpretasikan sebagai `TRUE`.
4.  `Transaction` dianggap valid oleh `node` lama.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_10.16.png" alt="gambar" width="580"/>
</p>

[Bagaimana node lama memvalidasi transaksi segwit sebagai script yang selalu TRUE (anyone-can-spend). - Figure 10.16]

Ini secara efektif adalah `script` **"anyone-can-spend"** dari sudut pandang `node` lama. Keamanannya dijamin oleh fakta bahwa mayoritas besar `hashrate` jaringan adalah `segwit-aware` dan akan menolak `block` apa pun dari `miner` lama yang mencoba mencuri dana dengan cara ini.

#### Inklusi dalam Block

Agar `witness` yang terpisah tetap terikat pada `block`, `segwit` memperkenalkan aturan baru:
* Jika sebuah `block` mengandung `transaction` `segwit`, `coinbase transaction`-nya *harus* berisi sebuah **`witness commitment`**.
* `Witness commitment` ini adalah `hash` dari **`witness root hash`** dan sebuah `witness reserved value`.
* `Witness root hash` adalah `merkle root` yang dibangun dari **`wtxid`** semua `transaction` di dalam `block`. `Wtxid` adalah `hash` dari `transaction` *termasuk* data `witness`-nya.

`Commitment` ini ditempatkan di dalam sebuah `output` `OP_RETURN` di dalam `coinbase transaction`. `Node` lama mengabaikan `output` `OP_RETURN` ini, sehingga kompatibilitas tetap terjaga.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_10.17.png" alt="gambar" width="580"/>
</p>

[Diagram bagaimana merkle root dari wtxid (witness root hash) dimasukkan ke dalam coinbase transaction sebagai witness commitment. - Figure 10.17]

#### Pay-to-Witness-Script-Hash (P2WSH)

P2WSH adalah versi `segwit` dari P2SH. Ini berfungsi dengan cara yang sangat mirip:
* `Redeem script` yang kompleks (disebut **`witness script`**) di-hash menggunakan `SHA256` (menghasilkan hash 32-byte).
* Hash ini menjadi `witness program` dalam `output` P2WSH.
* Untuk membelanjakannya, `witness` harus berisi argumen `script` (misalnya, `signatures`) diikuti oleh `witness script` lengkap.
* `Node` `segwit-aware` akan memverifikasi bahwa `hash` dari `witness script` yang diberikan cocok dengan `witness program` di `output` yang dibelanjakan, lalu mengeksekusi `witness script` tersebut.

#### Metode Hashing Baru untuk Signature

`Segwit` memperkenalkan metode hashing `signature` baru (**BIP143**) yang memperbaiki masalah inefisiensi kuadratik.
* Data `transaction` yang umum untuk semua input (seperti daftar output) di-hash sekali saja untuk membuat sebuah *intermediate hash*.
* Untuk setiap input, *intermediate hash* ini kemudian di-hash bersama dengan data spesifik untuk input tersebut (seperti `outpoint` yang dibelanjakan, `script`, dan **jumlah (`amount`) yang dibelanjakan**).

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_10.26.png" alt="gambar" width="580"/>
</p>

[Proses hashing dua langkah segwit yang efisien, di mana intermediate hash digunakan kembali untuk setiap input. - Figure 10.26]

Dengan melakukan ini, waktu verifikasi menjadi **linear (O(n))**, peningkatan performa yang sangat besar.

> **Poin Kritis untuk Auditor**: `Signature` `segwit` juga meng-commit **jumlah (`amount`)** dari *output* yang dibelanjakan. Ini adalah peningkatan keamanan yang signifikan untuk `hardware wallet`, karena `wallet` dapat memverifikasi `fee` yang dibayarkan tanpa perlu mempercayai komputer host untuk memberikan informasi `amount` yang benar.

#### Peningkatan Lainnya

* **Penghematan Bandwidth**: Karena `txid` tidak lagi bergantung pada `witness`, `lightweight wallet` dapat meminta `transaction` tanpa data `witness`, menghemat lebih dari 50% `bandwidth`.
* **Script yang Dapat Diperbarui**: `Witness version byte` menyediakan mekanisme yang bersih dan dapat diperluas untuk memperkenalkan versi baru `Script` di masa depan tanpa harus menggunakan `OP_NOP` lagi.
* **Kompatibilitas Wallet**: Untuk memungkinkan `wallet` lama mengirim dana ke `wallet` `segwit`, dikembangkan skema **`nested segwit`**, di mana `output` `segwit` (P2WPKH atau P2WSH) "dibungkus" di dalam `output` P2SH. Alamat yang dihasilkan dimulai dengan angka '3', sehingga dikenali oleh `wallet` lama.

### Batas Block

`Segwit` juga memperkenalkan cara baru untuk menghitung batas ukuran `block`, yang memungkinkan peningkatan kapasitas `transaction` melalui `soft fork`.

* **Batas Lama**: Ukuran `block` maksimal 1.000.000 byte.
* **Konsep Baru**: **`Block Weight`**. Batas baru adalah 4.000.000 *Weight Units* (WU).
    * 1 byte data non-`witness` (data `transaction` inti) dihitung sebagai **4 WU**.
    * 1 byte data `witness` dihitung sebagai **1 WU**.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_10.36.png" alt="gambar" width="580"/>
</p>

[Perhitungan block weight, di mana byte non-witness dikalikan 4 dan byte witness dikalikan 1. - Figure 10.36]

Implikasinya adalah:
* Batas ukuran `block` dasar (tanpa `witness`) tetap 1MB (1.000.000 byte * 4 WU/byte = 4.000.000 WU), sehingga kompatibel dengan `node` lama.
* Namun, karena data `witness` memiliki "diskon" bobot, ukuran total `block` (data inti + `witness`) secara efektif bisa mencapai ~2MB, tergantung pada seberapa banyak `transaction` `segwit` yang ada di dalamnya. Ini meningkatkan kapasitas jaringan.
* Batas *signature operations* (sigops) juga disesuaikan dengan skema bobot yang sama.

---

# Bab 11
## Peningkatan Bitcoin

Bab ini adalah salah satu bab paling krusial untuk memahami bagaimana *Bitcoin* berevolusi dan menjaga konsensus di tengah perubahan. Sebagai calon auditor keamanan, memahami mekanisme peningkatan dan potensi risikonya, seperti *chain split*, adalah fundamental. Bab ini akan membahas dua cara utama perubahan aturan konsensus: ***hard fork*** dan ***soft fork***. Kita juga akan menelusuri bagaimana mekanisme untuk menerapkan perubahan ini telah berkembang seiring waktu, yang berpuncak pada konsep penting di mana pengguna—bukan hanya *miners*—yang pada akhirnya menentukan aturan jaringan.

### *Bitcoin Forks*

Dalam konteks *Bitcoin*, istilah ***fork*** tidak merujuk pada penyalinan kode sumber (*open source project fork*), melainkan **perubahan pada aturan konsensus**. Aturan konsensus adalah seperangkat aturan yang divalidasi oleh setiap *full node* untuk menentukan apakah sebuah *blockchain* valid atau tidak. Aturan ini memastikan bahwa semua partisipan dalam jaringan memiliki pandangan yang sama mengenai "siapa memiliki apa" (*UTXO set*).

Perubahan aturan konsensus ini terbagi menjadi dua kategori utama:

* ***Hard Forks***: Ini adalah perubahan yang **melonggarkan** aturan konsensus. Artinya, *block* yang sebelumnya dianggap tidak valid oleh aturan lama, kini dianggap valid oleh aturan baru. Contohnya adalah meningkatkan batas maksimal *block weight*.
* ***Soft Forks***: Ini adalah perubahan yang **memperketat** aturan konsensus. Artinya, semua *block* yang dianggap valid oleh aturan baru juga pasti valid menurut aturan lama. Namun, beberapa *block* yang valid menurut aturan lama bisa jadi tidak valid menurut aturan baru. Contohnya adalah mengurangi batas maksimal *block weight*.

Buku ini menggunakan analogi sebuah restoran vegetarian yang populer untuk menjelaskan konsep ini. Anggap restoran adalah seorang *miner*, para tamu adalah *full nodes*, dan makanan yang disajikan adalah *blocks*.

* **Tanpa Perubahan**: Restoran menyajikan makanan vegetarian, dan para tamu (vegetarian) menerimanya. Ini adalah keadaan normal.
* **Hard Fork**: Restoran mulai menyajikan daging (melonggarkan aturan "hanya vegetarian"). Para tamu vegetarian akan menolak makanan ini. *Node* lama akan menolak *block* baru yang hanya valid menurut aturan baru yang lebih longgar.
* **Soft Fork**: Restoran mulai hanya menyajikan makanan vegan (memperketat aturan). Para tamu vegetarian tetap bisa menerima makanan ini karena makanan vegan adalah bagian dari makanan vegetarian. *Node* lama akan tetap menerima *block* baru karena *block* tersebut masih mematuhi aturan lama yang lebih longgar.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_11.1.png" alt="gambar" width="580"/>
</p>

[Diagram Venn yang membandingkan set block yang valid. Lingkaran "Aturan Lama" (misal, block weight <= 4M) berada di tengah. Lingkaran "Hard Fork" (misal, <= 8M) melingkupi aturan lama. Lingkaran "Soft Fork" (misal, <= 2M) berada di dalam aturan lama. - Figure 11.1]

Setiap kali sebuah *fork* diimplementasikan dan ada sekelompok *node* yang menjalankannya, ada risiko terjadinya ***chain split***, di mana *blockchain* terbelah menjadi dua versi yang berbeda.

#### Perubahan Aturan Non-Konsensus

Penting untuk membedakan *fork* dari pembaruan perangkat lunak biasa yang tidak mengubah aturan konsensus. Buku ini memberikan dua contoh:
1.  **Fitur `kill`**: Jika Kita menambahkan pesan jaringan baru bernama `kill` yang bisa mematikan *node* lain, ini bukan *fork*. *Node* lama tidak akan mengerti pesan ini dan akan mengabaikannya, sementara *node* baru yang menjalankan perangkat lunak Kita akan terpengaruh. Ini adalah perubahan protokol jaringan, bukan aturan konsensus.
2.  ***Compact Blocks*** **(BIP152)**: Ini adalah fitur optimasi di mana sebuah *node* mengirimkan *block header* dan ID *transaction* yang dipersingkat kepada *peer*-nya, bukan seluruh *block*. *Peer* tersebut kemudian merekonstruksi *block* menggunakan *transaction* yang sudah ada di *mempool*-nya. Ini adalah perubahan yang sangat berguna untuk mengurangi penggunaan *bandwidth* dan mempercepat propagasi *block*. Ini adalah perubahan *opt-in* yang kompatibel; *node* baru bisa berkomunikasi dengan lebih efisien, sementara *node* lama tetap berfungsi seperti biasa. Ini bukan *fork* karena tidak mengubah validasi *block*.

#### *Hard Forks*

Ketika sebuah *hard fork* terjadi (misalnya, batas *block weight* dinaikkan dari 4M menjadi 8M WU), *node* baru akan menerima *block* dari *node* lama (karena *block* <= 4M WU pasti <= 8M WU). Namun, *node* lama akan menolak *block* dari *node* baru jika ukurannya, misalnya, 6M WU.

Jika hanya minoritas *hashrate* yang menjalankan aturan baru, *block* mereka yang lebih besar akan sering ditolak oleh mayoritas jaringan, menyebabkan mereka membuang-buang sumber daya dan akhirnya harus kembali ke rantai utama.

Namun, jika mayoritas *hashrate* menjalankan aturan baru, mereka akan mulai membangun rantai mereka sendiri yang lebih panjang (memiliki lebih banyak *proof-of-work*). *Node* lama akan mengabaikan rantai ini dan terus menambang di rantai mereka yang lebih pendek. Ini menciptakan *chain split* yang berpotensi permanen.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_11.6.png" alt="gambar" width="580"/>
</p>

[Rantai blockchain terpisah, di mana node-node baru yang memiliki hashrate mayoritas berhasil membuat rantai yang lebih panjang daripada node-node lama. - Figure 11.6]

Risiko terbesar bagi rantai baru adalah **wipeout**. Jika karena suatu alasan mayoritas *hashrate* kembali ke rantai lama, rantai lama bisa menjadi lebih kuat (memiliki lebih banyak *proof-of-work* kumulatif) daripada rantai baru. Karena *block* lama valid bagi *node* baru, *node* baru akan melakukan *reorg* besar-besaran, meninggalkan rantai baru dan kembali ke rantai lama. Semua *transaction* di rantai baru akan hilang.

Untuk mencegah ini, *hard fork* dapat mengimplementasikan **wipeout protection**. Contohnya, *Bitcoin Cash* mengharuskan *block* pertama setelah *split* berukuran lebih dari 1 MB. Aturan ini membuat *block* tersebut tidak valid bagi *node* *Bitcoin* asli, dan sebaliknya, *block* *Bitcoin* asli di ketinggian yang sama menjadi tidak valid bagi *node* *Bitcoin Cash*. Ini menciptakan perpisahan yang tidak dapat didamaikan, mencegah *reorg*.

#### *Soft Forks*

Dengan *soft fork*, aturan diperketat. *Node* lama akan selalu menerima *block* dari *node* baru. Namun, jika seorang *miner* lama membuat sebuah *block* yang valid menurut aturan lama tetapi tidak valid menurut aturan baru (misalnya, menghabiskan *output* Segwit seolah-olah itu adalah *anyone-can-spend*), maka *node* baru akan menolak *block* tersebut.

Jika hanya minoritas *hashrate* yang menjalankan aturan baru, mereka akan menolak *block* dari mayoritas dan pada dasarnya "memisahkan diri" dari jaringan utama ke rantai mereka sendiri, yang kemungkinan besar tidak akan bertahan lama.

Namun, jika mayoritas *hashrate* menjalankan aturan baru, mereka akan mengabaikan *block* yang tidak patuh dari *miner* lama. Rantai baru akan terus tumbuh lebih kuat. *Miner* lama yang terus membuat *block* yang tidak patuh akan mendapati *block* mereka ditolak oleh mayoritas dan kehilangan *block reward*. Akhirnya, mereka akan terpaksa untuk meningkatkan perangkat lunak mereka atau berhenti menambang. Rantai lama akan mengalami *reorg* dan bergabung dengan rantai baru yang lebih kuat.

> **Perbedaan Kunci**:
> * Pada **hard fork**, *node* baru berisiko mengalami *wipeout*. *Node* lama aman dari *reorg*.
> * Pada **soft fork**, *node* lama berisiko mengalami *wipeout*. *Node* baru aman dari *reorg*.

#### *Transaction Replay*

Setelah *chain split* permanen, pengguna secara efektif memiliki koin di kedua rantai. Sebuah *transaction* yang dibuat untuk satu rantai bisa jadi valid di rantai lainnya juga. Jika Kita mengirim 2 BTC Old, ada kemungkinan *transaction* yang sama "diputar ulang" (*replayed*) di rantai New, menyebabkan Kita tanpa sengaja juga mengirim 2 BTC New.

Untuk mencegah ini, *fork* dapat mengimplementasikan **replay protection**. *Bitcoin Cash*, misalnya, memperkenalkan tipe `SIGHASH` baru bernama `FORKID`. *Transaction* yang menggunakan `FORKID` hanya valid di rantai *Bitcoin Cash* dan tidak valid di rantai *Bitcoin*. Sebaliknya, *transaction* tanpa `FORKID` hanya valid di rantai *Bitcoin* dan tidak valid di *Bitcoin Cash*.

### Mekanisme Peningkatan

Karena risiko *chain split*, peningkatan *Bitcoin* harus dilakukan dengan sangat hati-hati. Sejauh ini, sebagian besar peningkatan non-kritis dilakukan melalui *soft fork*. Mekanisme untuk mengkoordinasikan *soft fork* ini telah berevolusi.

#### Sinyal Coinbase (BIP16)

Peningkatan pertama yang terkoordinasi adalah untuk *pay-to-script-hash* (P2SH) pada tahun 2012. *Miner* yang mendukung perubahan ini menyisipkan string `/P2SH/` di dalam *coinbase transaction* mereka. Pada tanggal yang ditentukan (*flag day*), para pengembang menghitung jumlah *block* yang memberi sinyal. Karena lebih dari 55% *block* mendukung, aturan P2SH diaktifkan pada tanggal 1 April 2012, dan semua *node* yang telah diperbarui mulai memberlakukan aturan baru tersebut.

#### Sinyal dengan Peningkatan Nomor Versi *Block* (BIP34, 66, 65)

Mekanisme ini menggunakan *field* versi pada *block header* untuk sinyal. Ini digunakan untuk tiga *soft fork*:
* **BIP34**: Mengharuskan tinggi *block* dicantumkan dalam *coinbase transaction*. Menggunakan versi *block* 2.
* **BIP66**: Mengharuskan penggunaan format DER yang ketat untuk *signatures*. Menggunakan versi *block* 3.
* **BIP65**: Mengaktifkan `OP_CHECKLOCKTIMEVERIFY`. Menggunakan versi *block* 4.

Proses aktivasinya bertahap:
1.  *Miner* mulai membuat *block* dengan versi yang lebih tinggi (misalnya, versi 2 untuk BIP34).
2.  Ketika 75% dari 1.000 *block* terakhir memiliki versi ≥2, *node* baru mulai menolak *block* versi 2 yang tidak mematuhi aturan baru (misalnya, tidak ada tinggi *block* di *coinbase*).
3.  Ketika 95% dari 1.000 *block* terakhir memiliki versi ≥2, *node* baru mulai menolak semua *block* versi 1. Ini memaksa *miner* yang tersisa untuk meningkatkan perangkat lunak mereka agar *block* mereka tidak ditolak.

Mekanisme ini disebut ***miner-activated soft fork*** (MASF), karena *miners* yang memberi sinyal dan pada akhirnya memberlakukan aturan baru.

#### Sinyal dengan Bit Versi *Block* (BIP9)

Mekanisme sebelumnya memiliki keterbatasan: hanya satu *soft fork* yang bisa diimplementasikan pada satu waktu, dan nomor versi *block* tidak dapat digunakan kembali. **BIP9** mengatasi ini dengan menafsirkan *field* versi *block* secara berbeda.

*Block* yang 3 bit pertamanya adalah `001` akan menggunakan 29 bit sisanya sebagai bit-flags individual. Setiap bit dapat digunakan untuk memberi sinyal dukungan terhadap satu proposal peningkatan yang berbeda secara bersamaan.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_11.21.png" alt="gambar" width="580"/>
</p>

[Representasi 32-bit dari field versi blok, di mana 3 bit pertama disetel ke 001 dan 29 bit sisanya dapat digunakan sebagai flag individual. - Figure 11.21]

Setiap proposal BIP9 memiliki parameter:
* **Name**: Nama fitur (misalnya, `csv`, `segwit`).
* **Bit**: Bit mana dari 29 bit yang digunakan (0-28).
* **Start time**: Waktu kapan penghitungan sinyal dimulai.
* **Timeout**: Waktu kapan proposal dianggap gagal jika tidak mencapai ambang batas.

Proposal akan melalui beberapa status, yang dievaluasi setiap periode *retarget* (2.016 *blocks*):
<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_11.22.png" alt="gambar" width="580"/>
</p>

[Diagram alir status untuk aktivasi BIP9. Dimulai dari DEFINED, beralih ke STARTED setelah start time. Dari STARTED, bisa beralih ke LOCKED_IN jika ambang batas 95% tercapai, atau ke FAILED jika timeout tercapai. Dari LOCKED_IN, beralih ke ACTIVE setelah satu periode retarget. - Figure 11.22]

* **DEFINED**: Status awal sebelum *start time*.
* **STARTED**: Setelah *start time*, jaringan menunggu sinyal.
* **LOCKED_IN**: Jika 95% (1.916 dari 2.016 *blocks*) memberi sinyal dukungan dalam satu periode *retarget*, status berubah menjadi `LOCKED_IN`. Ini adalah titik di mana aktivasi tidak bisa dibatalkan lagi.
* **ACTIVE**: Setelah satu periode *retarget* penuh dalam status `LOCKED_IN`, aturan baru mulai diberlakukan.
* **FAILED**: Jika *timeout* tercapai sebelum status `LOCKED_IN`, proposal gagal.

**Contoh Penerapan BIP9:**
* **Relative Lock Time (csv)**: Menggunakan bit 0. Proses ini berjalan lancar dan mencapai status `ACTIVE` setelah hanya tiga periode *retarget*.
* **Segregated Witness (Segwit)**: Ini adalah contoh yang jauh lebih kompleks dan kontroversial. Menggunakan bit 1, proposal Segwit macet di sekitar 30% dukungan dari *miner* dan berisiko gagal. Ini memicu perdebatan sengit di komunitas.

Konflik seputar Segwit melahirkan beberapa proposal tandingan:
* **Segwit2x**: Proposal untuk mengaktifkan Segwit, diikuti dengan *hard fork* untuk meningkatkan *block size*. Didukung oleh banyak *miner*.
* **BIP148**: Proposal untuk melakukan ***user-activated soft fork*** (UASF). *Node* yang menjalankan BIP148 akan mulai menolak *block* yang tidak memberi sinyal dukungan untuk Segwit (bit 1) mulai 1 Agustus 2017. Ini adalah upaya untuk "memaksa" aktivasi Segwit tanpa bergantung pada *miner*.
* **BIP91**: Proposal kompromi untuk menjembatani semua pihak. BIP91 menggunakan bit 4 dan ambang batas 80% yang lebih rendah. Setelah aktif, ia akan menolak *block* yang tidak memberi sinyal untuk Segwit (bit 1). Karena mayoritas *miner* mengadopsi BIP91, ini menyebabkan tingkat sinyal untuk proposal Segwit asli (bit 1) meroket hingga lebih dari 95%, yang akhirnya mengaktifkan Segwit melalui mekanisme BIP9 asli.

Pelajaran dari aktivasi Segwit adalah bahwa memberikan hak veto kepada minoritas kecil *hashrate* (5% dalam BIP9) dapat menghambat peningkatan yang diinginkan oleh mayoritas ekonomi.

### *User-Activated Soft Forks* (UASF)

Konsep ini menekankan bahwa kekuatan tertinggi dalam jaringan *Bitcoin* tidak terletak pada *miner*, tetapi pada **mayoritas ekonomi**—pengguna, bursa, pedagang, dan bisnis yang menggunakan *Bitcoin*. *Miner* dibayar untuk mengikuti aturan, bukan untuk menentukannya.

UASF adalah mekanisme di mana mayoritas ekonomi ini secara kolektif memutuskan untuk memberlakukan aturan baru (yang lebih ketat) pada tanggal atau tinggi *block* yang telah ditentukan.

Mari kita bayangkan sebuah skenario:
1.  99% pengguna (*node* ekonomi) ingin menerapkan *soft fork* untuk memperkecil ukuran *block*, tetapi 100% *miner* menolaknya.
2.  Pengguna memperbarui perangkat lunak mereka untuk menolak *block* yang terlalu besar setelah tanggal yang ditentukan.
3.  Setelah tanggal tersebut, *miner* terus membuat *block* besar. Namun, bagi 99% pengguna, *block-block* ini tidak valid. *Block reward* yang diterima *miner* menjadi tidak berharga karena tidak ada bursa atau pedagang yang mau menerimanya.
4.  Jika ada satu *miner* saja yang memutuskan untuk mengikuti aturan pengguna dan membuat *block* kecil, *block* tersebut akan menjadi satu-satunya *block* yang diterima oleh mayoritas ekonomi. *Miner* ini akan bisa menjual koinnya dan membayar tagihan listrik.
5.  Melihat ini, *miner* lain yang rasional akan beralih ke rantai yang diterima pengguna agar tidak merugi.
6.  Akhirnya, rantai yang didukung pengguna akan memiliki mayoritas *hashrate*, menyebabkan *reorg* pada rantai *miner* yang tidak patuh. Rantai yang tidak patuh akan terhapus. Pengguna menang.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_11.28.png" alt="gambar" width="580"/>
</p>

lalu

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_11.29.png" alt="gambar" width="580"/>
</p>

lalu

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_11.30.png" alt="gambar" width="580"/>
</p>

[Serangkaian diagram yang menggambarkan bagaimana satu miner yang mematuhi aturan pengguna berhasil membuat rantai yang valid, yang kemudian diikuti oleh miner lain, dan akhirnya menyebabkan rantai yang tidak patuh dihapus. - Figure 11.28, 11.29, 11.30]

UASF adalah penegasan kembali bahwa *Bitcoin* adalah sistem yang diatur oleh konsensus pengguna. Mekanisme deployment di masa depan kemungkinan akan menggabungkan sinyal dari *miner* dengan mekanisme aktivasi oleh pengguna untuk memastikan bahwa peningkatan yang diinginkan oleh mayoritas ekonomi dapat diimplementasikan tanpa bisa diveto oleh sekelompok kecil *miner*.

---


