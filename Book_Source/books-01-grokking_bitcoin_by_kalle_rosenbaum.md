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
  <img src="images/books-01-grokking_bitcoin/figure_1.14.png" alt="gambar" width="575"/>
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
