# Bab 1
## Pendahuluan**

Bab ini memberikan gambaran umum tentang apa itu Bitcoin, sejarah singkatnya, dan langkah-langkah praktis untuk memulai, seperti memilih dompet dan melakukan transaksi pertama.

---

#### **Pendahuluan**

Bitcoin adalah sekumpulan konsep dan teknologi yang membentuk dasar dari ekosistem uang digital. Satuan mata uangnya disebut **bitcoin** (dengan 'b' kecil), digunakan untuk menyimpan dan mengirimkan nilai di antara para peserta dalam jaringan Bitcoin. Sebaliknya, sistemnya secara keseluruhan disebut **Bitcoin** (dengan 'B' besar).

Pengguna Bitcoin berkomunikasi satu sama lain menggunakan protokol Bitcoin, terutama melalui internet. Protokol ini bersifat *open source* (kode sumbernya terbuka dan bisa dilihat siapa saja) dan dapat dijalankan di berbagai perangkat, membuatnya sangat mudah diakses.

Berbeda dari mata uang tradisional, **bitcoin** sepenuhnya virtual. Tidak ada koin fisik. Kepemilikan bitcoin dibuktikan dengan **kunci kriptografi** (*cryptographic keys*). Kunci ini disimpan dalam sebuah **dompet digital** (*digital wallet*). Siapa pun yang memiliki kunci tersebut dapat menandatangani (*sign*) transaksi untuk mengirimkan nilai bitcoin miliknya ke pemilik baru.

**Istilah Penting:**

* **Peer-to-peer (P2P):** Jaringan di mana para pesertanya (disebut *peers* atau *nodes*) terhubung satu sama lain tanpa memerlukan server pusat. Setiap peserta memiliki kedudukan yang sama.
* **Mining (Penambangan):** Proses di mana transaksi-transaksi baru diverifikasi dan ditambahkan ke dalam catatan publik yang disebut *blockchain*. Para pelaku proses ini (*miners*) diberi imbalan berupa bitcoin baru dan biaya transaksi. Proses ini juga yang menciptakan bitcoin baru dan mengamankan jaringan.
* **Blockchain:** Jurnal atau buku besar publik yang berisi semua transaksi yang pernah terjadi. Jurnal ini terdistribusi (disimpan oleh banyak peserta di seluruh dunia) dan diamankan menggunakan kriptografi.

Bitcoin memiliki empat inovasi utama yang digabungkan:

1. Jaringan *peer-to-peer* yang terdesentralisasi (protokol Bitcoin).
2. Jurnal transaksi publik (*blockchain*).
3. Satu set aturan untuk validasi transaksi dan penerbitan mata uang yang independen (aturan konsensus).
4. Mekanisme untuk mencapai konsensus global yang terdesentralisasi (*Proof-of-Work algorithm*).

#### **Mata Uang Digital Sebelum Bitcoin**

Sebelum Bitcoin, sudah ada upaya untuk menciptakan uang digital. Namun, mereka menghadapi tiga tantangan mendasar:

1. **Keaslian:** Bagaimana memastikan uang tersebut asli dan tidak dipalsukan (*counterfeit*)?
2. **Masalah Pengeluaran Ganda (*Double-Spend Problem*):** Bagaimana memastikan uang digital yang sama tidak bisa dibelanjakan lebih dari satu kali? Uang fisik mengatasi ini secara alami karena satu lembar uang tidak bisa berada di dua tempat sekaligus.
3. **Kepemilikan:** Bagaimana memastikan hanya pemilik sah yang bisa mengklaim uang tersebut?

Mata uang digital awal mencoba menyelesaikan ini dengan menggunakan otoritas pusat (*centralized authority*) untuk memverifikasi semua transaksi, mirip seperti sistem perbankan. Namun, karena terpusat, sistem ini rentan terhadap serangan pemerintah atau peretas dan akhirnya gagal. Bitcoin lahir sebagai solusi untuk menciptakan sistem uang digital yang **terdesentralisasi**, tanpa titik pusat yang bisa diserang.

#### **Sejarah Bitcoin**

Bitcoin pertama kali dideskripsikan pada tahun 2008 dalam sebuah makalah (*whitepaper*) berjudul *"Bitcoin: A Peer-to-Peer Electronic Cash System"* oleh seseorang (atau sekelompok orang) dengan nama samaran **Satoshi Nakamoto**.

Inovasi kunci dari Nakamoto adalah penggunaan sistem komputasi terdistribusi yang disebut **Proof-of-Work (PoW)**. Mekanisme ini seperti lotre global yang diadakan setiap 10 menit. Pemenangnya berhak menambahkan "halaman" baru (disebut *block*) ke dalam buku besar (*blockchain*) dan mendapatkan imbalan. Proses ini secara elegan menyelesaikan masalah *double-spend* tanpa perlu otoritas pusat.

Bitcoin juga merupakan solusi praktis untuk masalah komputasi terdistribusi yang dikenal sebagai **Byzantine Generals' Problem**, yaitu bagaimana mencapai kesepakatan di antara banyak peserta dalam jaringan yang tidak dapat diandalkan tanpa adanya pemimpin pusat.

#### **Memulai (Getting Started)**

Untuk menggunakan Bitcoin, Kita memerlukan aplikasi yang disebut **dompet Bitcoin (*Bitcoin wallet*)**. Dompet ini adalah antarmuka pengguna ke sistem Bitcoin, sama seperti browser web adalah antarmuka untuk protokol HTTP. Ada banyak sekali jenis dompet dengan kelebihan dan kekurangannya masing-masing.

##### **Memilih Dompet Bitcoin (Bitcoin Wallet)**

Dompet Bitcoin bisa dikategorikan berdasarkan beberapa hal:

**1. Berdasarkan Platform:**

* **Dompet Desktop (*Desktop wallet*):** Aplikasi yang diinstal di komputer (Windows, macOS, Linux). Menawarkan kontrol penuh tetapi keamanannya sangat bergantung pada keamanan komputer itu sendiri.
* **Dompet Seluler (*Mobile wallet*):** Jenis yang paling umum, berjalan di smartphone (iOS, Android). Sangat praktis untuk pemula, tetapi seringkali mengandalkan server pihak ketiga untuk data, yang bisa mengurangi privasi.
* **Dompet Web (*Web wallet*):** Diakses melalui browser. Kunci Kita bisa jadi disimpan di server milik pihak ketiga, mirip seperti webmail. Ini sangat tidak disarankan untuk menyimpan jumlah besar karena Kita mempercayakan dana Kita pada pihak lain.
* **Perangkat Penandatanganan Perangkat Keras (*Hardware signing devices / Hardware wallets*):** Perangkat fisik khusus yang menyimpan kunci Kita secara offline. Ini adalah salah satu cara teraman untuk menyimpan bitcoin karena kunci tidak pernah terekspos ke komputer yang terhubung internet.

**2. Berdasarkan Otonomi & Interaksi dengan Jaringan:**

* **Full Node:** Program yang mengunduh dan memvalidasi *seluruh* riwayat transaksi Bitcoin. Ini memberikan otonomi dan keamanan tertinggi, tetapi membutuhkan sumber daya komputasi dan ruang penyimpanan yang besar (ratusan Gigabyte).
* **Lightweight Client (atau SPV Client):** Klien yang hanya mengunduh sebagian kecil data dari *blockchain* (hanya *block headers*). Klien ini terhubung ke *full node* untuk mendapatkan informasi transaksi, sehingga tidak se-independen *full node* tetapi jauh lebih hemat sumber daya.
* **Klien API Pihak Ketiga (*Third-party API client*):** Dompet yang berinteraksi dengan Bitcoin melalui sistem pihak ketiga, bukan terhubung langsung ke jaringan P2P Bitcoin. Ini paling tidak aman dan paling tidak privat.

**3. Berdasarkan Siapa yang Mengontrol Kunci:**
Ini adalah kategori paling penting dari sudut pandang keamanan.

* **Non-custodial wallet:** Kita, dan hanya Kita, yang memegang kendali atas *private keys*. Inilah esensi dari Bitcoin. Slogannya adalah: **"Your keys, your coins. Not your keys, not your coins."** (Kunci Anda, koin Anda. Bukan kunci Anda, bukan koin Anda).
* **Custodial service:** Pihak ketiga (seperti bursa/exchange) yang memegang *private keys* untuk Kita. Ini seperti bank. Jika mereka diretas atau bangkrut, dana Kita bisa hilang.

##### **Mulai Cepat & Kode Pemulihan (Recovery Codes)**

Saat Kita pertama kali membuat dompet *non-custodial*, aplikasi akan menghasilkan **kode pemulihan** (*recovery code*). Kode ini sangat penting karena merupakan *master backup* untuk semua kunci di dompet Kita. Jika ponsel atau komputer Kita hilang/rusak, Kita bisa memulihkan seluruh dana Kita di perangkat baru hanya dengan memasukkan kode ini.

Kode ini juga dikenal sebagai **mnemonic phrase** atau **seed phrase**, biasanya terdiri dari 12 hingga 24 kata acak.

**Contoh Kode Pemulihan:**

| Wallet     | Recovery Code                                                                                                                |
| :--------- | :--------------------------------------------------------------------------------------------------------------------------- |
| BlueWallet | (1) media (2) suspect (3) effort (4) dish (5) album (6) shaft (7) price (8) junk (9) pizza (10) situate (11) oyster (12) rib |
| Electrum   | nephew dog crane clever quantum crazy purse traffic repeat fruit old clutch                                                  |
| Muun       | LAFV TZUN V27E NU4D WPF4 BRJ4 ELLP BNFL                                                                                      |

> **Peringatan Keamanan:** Jangan pernah menyimpan kode pemulihan ini secara digital (di email, cloud, atau screenshot). Cara terbaik adalah menuliskannya di atas kertas dan menyimpannya di tempat yang sangat aman. Jangan pernah memberikannya kepada siapa pun atau memasukkannya ke situs web yang tidak terpercaya. Aplikasi dompet yang sah hanya akan meminta kode ini saat proses pemulihan (restore), bukan saat penggunaan normal.

##### **Alamat Bitcoin (Bitcoin Addresses)**

Setelah dompet dibuat, ia akan menghasilkan **alamat Bitcoin** (*Bitcoin address*). Alamat ini seperti nomor rekening bank, tetapi ada beberapa perbedaan penting:

* Kita bisa membuat alamat baru sebanyak yang Kita mau.
* Sangat disarankan untuk **menggunakan alamat baru setiap kali Kita menerima pembayaran**. Menggunakan alamat yang sama berulang kali akan mengurangi privasi Kita, karena semua orang bisa melihat total dana yang masuk ke alamat tersebut di *blockchain*.
* Alamat ini aman untuk dibagikan. Orang lain hanya bisa mengirim bitcoin *ke* alamat tersebut, tidak bisa mengambilnya.

##### **Mendapatkan Bitcoin Pertama Anda**

Ada beberapa cara untuk mendapatkan bitcoin:

* Membeli langsung dari teman.
* Menghasilkan bitcoin dengan menjual barang atau jasa.
* Menggunakan ATM Bitcoin.
* Membeli melalui bursa (*exchange*) mata uang kripto. Perlu diperhatikan bahwa bursa biasanya akan meminta verifikasi identitas (proses yang disebut **KYC - Know Your Customer**), yang menghubungkan identitas dunia nyata Kita dengan aktivitas Bitcoin Kita.

> **Catatan Penting:** Transaksi Bitcoin **tidak dapat dibatalkan** (*irreversible*). Setelah dikirim, tidak ada cara untuk menariknya kembali.

##### **Mengirim, Menerima, dan Konfirmasi**

Untuk menerima pembayaran, dompet Kita akan menampilkan alamat dalam bentuk teks dan **QR code** untuk memudahkan pengirim. Pengirim memindai QR code tersebut, memasukkan jumlah, dan mengirim transaksi.

Setelah transaksi dikirim, statusnya akan menjadi **"Unconfirmed"** (Belum terkonfirmasi). Ini berarti transaksi sudah disiarkan ke jaringan, tetapi belum dimasukkan ke dalam sebuah *block* di *blockchain*.

Sebuah transaksi dianggap **terkonfirmasi** (*confirmed*) setelah dimasukkan ke dalam sebuah *block* yang valid. Rata-rata, sebuah *block* baru ditemukan setiap 10 menit. Semakin banyak *block* yang ditambahkan di atas *block* yang berisi transaksi Kita, semakin aman dan semakin permanen transaksi tersebut. Dalam praktiknya, 6 konfirmasi (sekitar 1 jam) sudah dianggap sangat aman untuk transaksi bernilai besar.

---

# Bab 2
## Cara Kerja Bitcoin**

Berbeda dengan sistem perbankan tradisional, Bitcoin tidak memerlukan kepercayaan pada pihak ketiga. Setiap pengguna bisa menjalankan *software* di komputernya sendiri untuk memverifikasi setiap aspek dari sistem Bitcoin. Bab ini akan menelusuri satu transaksi dari awal hingga akhir.

#### **Gambaran Umum Bitcoin (*Bitcoin Overview*)**

Sistem Bitcoin terdiri dari:

1. **Pengguna** dengan **dompet (*wallets*)** yang berisi **kunci (*keys*)**.
2. **Transaksi (*transactions*)** yang disiarkan ke seluruh jaringan.
3. **Penambang (*miners*)** yang menghasilkan **konsensus *blockchain*** melalui kompetisi komputasi. *Blockchain* ini adalah catatan otoritatif dari semua transaksi.

Untuk memvisualisasikan transaksi dalam bab ini, kita akan menggunakan ***blockchain explorer***.

**Istilah Penting:**

* ***Blockchain Explorer:*** Sebuah situs web yang berfungsi seperti mesin pencari untuk *blockchain* Bitcoin. Anda bisa memasukkan alamat, ID transaksi, atau nomor *block* untuk melihat detail dan alirannya. Contohnya termasuk Blockstream Explorer atau Mempool.Space.

> **Peringatan Privasi:** Menggunakan *blockchain explorer* bisa memberitahu operator situs tersebut tentang alamat atau transaksi yang Anda minati, yang berpotensi menghubungkannya dengan alamat IP Anda.

#### **Membeli dari Toko Online (*Buying from an Online Store*)**

Kita akan melanjutkan kisah Alice dari Bab 1. Alice kini ingin membeli episode *podcast* dari toko online milik Bob.

Toko Bob menerima pembayaran Bitcoin. Saat *checkout*, sistem Bob secara otomatis membuat sebuah **faktur (*invoice*)** dalam bentuk **QR code**.

![gambar_2-1](images/books-02-mastering_bitcoin/gambar_2-1.png)

Berbeda dengan QR code biasa yang hanya berisi alamat tujuan, faktur ini berisi lebih banyak informasi dalam format URI (*Uniform Resource Identifier*):

```
bitcoin:bc1qk2g6u8p4qm2s2lh3gts5cpt2mrv5skcuu7u3e4?amount=0.01577764&label=Bob%27s%20Store&message=Purchase%20at%20Bob%27s%20Store
```

Ini terdiri dari:

* **Alamat Bitcoin:** `bc1qk2g6u8p4qm2s2lh3gts5cpt2mrv5skcuu7u3e4`
* **Jumlah Pembayaran:** `0.01577764` BTC
* **Label:** "Bob's Store"
* **Deskripsi:** "Purchase at Bob's Store"

Alice memindai QR code ini dengan dompet di ponselnya. Aplikasi dompetnya otomatis mengisi semua detail. Alice hanya perlu menekan "Kirim" untuk mengotorisasi pembayaran. Dalam beberapa detik, Bob melihat transaksi tersebut masuk di sistemnya.

#### **Transaksi Bitcoin (*Bitcoin Transactions*)**

Secara sederhana, sebuah transaksi memberitahu jaringan bahwa pemilik sejumlah bitcoin telah mengizinkan transfer nilai tersebut ke pemilik baru.

##### **Input dan Output Transaksi**

Transaksi di Bitcoin seperti entri dalam buku besar akuntansi berpasangan (*double-entry bookkeeping*):

* **Input:** Sisi "sumber dana" dari transaksi. Ini merujuk pada transaksi sebelumnya di mana si pengirim menerima bitcoin.
* **Output:** Sisi "tujuan dana" dari transaksi. Ini menciptakan "kunci" baru yang hanya bisa dibuka oleh pemilik berikutnya.

Total nilai dari *input* harus sedikit lebih besar dari total nilai *output*. Selisihnya adalah **biaya transaksi (*transaction fee*)**, yang menjadi insentif bagi *miner* untuk memasukkan transaksi tersebut ke dalam *blockchain*.

*Gambar 2-2 di buku mengilustrasikan ini: Sebuah tabel dengan kolom Input dan Output. Total Input adalah 0.55 BTC, sementara Total Output adalah 0.50 BTC. Perbedaannya, yaitu 0.05 BTC, adalah biaya transaksi.*

##### **Rantai Transaksi (*Transaction Chains*)**

Setiap transaksi terhubung dengan transaksi sebelumnya. *Input* dari sebuah transaksi sebenarnya adalah *output* dari transaksi sebelumnya. Inilah yang membentuk "rantai" kepemilikan.

*Gambar 2-3 di buku menunjukkan ini secara visual. Transaksi 1 (Tx1) mengirimkan 100,000 satoshi ke Alice. Transaksi Alice ke Bob (Tx2) menggunakan output dari Tx1 sebagai input-nya. Output dari Tx2 kemudian bisa menjadi input untuk transaksi Bob berikutnya (Tx3).*

**Istilah Penting:**

* **Satoshi (sat):** Unit terkecil dari bitcoin. 1 bitcoin = 100,000,000 satoshi. Protokol Bitcoin sendiri menggunakan satoshi untuk menghitung nilai.

##### **Membuat Kembalian (*Making Change*)**

*Input* transaksi harus dihabiskan seluruhnya, mirip seperti Anda tidak bisa menyobek selembar uang kertas untuk membayar. Jika Anda ingin membayar 5 BTC tetapi hanya memiliki *input* senilai 20 BTC, transaksi Anda akan memiliki dua *output*:

1. Satu *output* sebesar 5 BTC untuk si penerima.
2. Satu *output* sebesar 15 BTC (dikurangi biaya transaksi) yang kembali ke alamat Anda sendiri. Ini disebut ***change output***.

Untuk privasi, alamat kembalian ini biasanya adalah alamat baru yang belum pernah digunakan, yang juga dibuat oleh dompet Anda.

##### **Bentuk-Bentuk Transaksi Umum**

* **Transaksi Umum (*Common Transaction*):** Satu *input* dan dua *output* (satu untuk pembayaran, satu untuk kembalian). Ini adalah bentuk yang paling sering ditemui. *Digambarkan di Gambar 2-4*.
* **Transaksi Agregasi (*Aggregating Transaction*):** Beberapa *input* digabungkan menjadi satu *output* tunggal. Mirip seperti menukar banyak uang koin menjadi selembar uang kertas besar. *Digambarkan di Gambar 2-5*.
* **Transaksi Distribusi (*Distributing Transaction*):** Satu *input* yang membayar ke banyak *output* (banyak penerima). Sering digunakan oleh bisnis, misalnya untuk membayar gaji. *Digambarkan di Gambar 2-6*.

#### **Membangun Sebuah Transaksi (*Constructing a Transaction*)**

Dompet Alice melakukan semua pekerjaan ini secara otomatis. Alice hanya perlu menentukan tujuan, jumlah, dan biaya transaksi. Dompet bisa membangun transaksi bahkan saat sedang *offline*.

1. **Mendapatkan Input yang Tepat:** Dompet akan memindai daftar *output* yang belum terpakai yang dimilikinya, yang dikenal sebagai **UTXO (*Unspent Transaction Outputs*)**. Ia akan memilih satu atau beberapa UTXO yang cukup untuk menutupi jumlah pembayaran.
2. **Membuat Output:** Dompet membuat satu *output* untuk Bob dan (jika perlu) satu *change output* untuk Alice kembali. Setiap *output* berisi sebuah *script* yang pada dasarnya mengatakan, "Dana ini hanya bisa dibelanjakan oleh siapa pun yang bisa memberikan tanda tangan digital yang sah dari kunci milik Bob".
3. **Menambahkan Biaya Transaksi:** Biaya transaksi tidak ditulis secara eksplisit, melainkan dihitung dari selisih antara total *input* dan total *output*.

#### **Menambahkan Transaksi ke Blockchain**

Setelah transaksi dibuat dan ditandatangani, ia harus disiarkan ke jaringan Bitcoin.

##### **Propagasi Transaksi**

Dompet Alice mengirimkan transaksi tersebut ke beberapa *node* (rekan) di jaringan P2P. Setiap *node* yang menerima transaksi valid yang belum pernah dilihat sebelumnya akan meneruskannya ke semua *node* lain yang terhubung dengannya. Proses ini disebut ***gossiping***. Dalam beberapa detik, transaksi tersebut menyebar ke sebagian besar jaringan. Dompet Bob, yang juga terhubung ke jaringan, akan mendeteksi transaksi ini sebagai pembayaran masuk.

##### **Penambangan Bitcoin (*Bitcoin Mining*)**

Transaksi Alice kini ada di jaringan, tetapi belum menjadi bagian permanen dari *blockchain*. Ia harus dimasukkan ke dalam sebuah *block* melalui proses yang disebut **mining**.

*Mining* memiliki dua tujuan utama:

1. **Mencapai Konsensus:** Para *miner* berkompetisi untuk memecahkan teka-teki komputasi yang sangat sulit. *Miner* pertama yang berhasil akan "memenangkan" hak untuk membuat *block* berikutnya. Solusi ini disebut ***Proof-of-Work (PoW)***. Karena PoW sangat sulit dibuat tetapi mudah diverifikasi, ia berfungsi sebagai bukti bahwa upaya komputasi yang besar telah dilakukan, sehingga mengamankan transaksi di dalam *block* tersebut.
2. **Menerbitkan Bitcoin Baru:** *Miner* yang berhasil membuat *block* akan mendapatkan imbalan berupa bitcoin yang baru dibuat (*block subsidy*) ditambah semua biaya transaksi dari transaksi yang ia masukkan ke dalam *block*.

Sekitar lima menit setelah Alice mengirim transaksinya, seorang *miner* (misalnya Jing dari contoh di buku) menemukan solusi PoW untuk *block* yang berisi transaksi Alice. *Block* ini kemudian disiarkan ke seluruh jaringan. Setiap *node* lain memverifikasinya dan menambahkannya ke salinan *blockchain* mereka.

Saat *block* yang berisi transaksi Alice ditambahkan ke *blockchain*, transaksi tersebut mendapatkan **1 konfirmasi**. Setiap *block* baru yang ditambahkan di atasnya memberikan konfirmasi tambahan. Semakin banyak konfirmasi, semakin sulit (secara komputasi) untuk membatalkan transaksi tersebut.

*Gambar 2-7 di buku menggambarkan tumpukan block, dengan block yang berisi transaksi Alice berada di tengah. Tumpukan block di bawahnya menunjukkan sejarah (block height), sementara tumpukan block di atasnya menunjukkan tingkat keamanan atau kedalaman (block depth).*

#### **Membelanjakan Transaksi (*Spending the Transaction*)**

Setelah transaksi Alice terkonfirmasi, Bob kini adalah pemilik sah dari dana tersebut. *Output* dari transaksi Alice menjadi UTXO baru yang dikontrol oleh kunci milik Bob. Bob sekarang bisa menggunakan UTXO ini sebagai *input* untuk transaksi berikutnya, misalnya untuk membayar desainer web-nya, Gopesh.

*Gambar 2-8 mengilustrasikan rantai transaksi lengkap: Joe membayar Alice (Transaksi #1), Alice membayar Bob (Transaksi #2), dan Bob membayar Gopesh (Transaksi #3). Ini menunjukkan bagaimana nilai berpindah dari satu pemilik ke pemilik berikutnya melalui rantai transaksi yang saling terhubung.*

---

