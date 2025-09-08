# Bab 1

## Pengantar Bitcoin (Introduction to Bitcoin)

Tujuan utama buku ini adalah membantu kita memutuskan sendiri apakah kita mempercayai **Bitcoin**. Untuk memulai, diasumsikan kita memahami secara garis besar istilah-istilah berikut:

* Program komputer (Computer program)
* Basis data (Database)
* Jaringan komputer (Computer network)
* Server web (Web server)

---

## Apa itu Bitcoin? (What is Bitcoin?)

**Bitcoin** adalah **sistem uang tunai digital** (*digital cash system*) yang memungkinkan orang untuk **mengirimkan bitcoin** (unit mata uang Bitcoin, ditulis dengan huruf *b* kecil) satu sama lain tanpa menggunakan bank atau **pihak ketiga terpercaya** (*trusted third party*) lainnya.

Ini mirip dengan uang kertas dan koin tradisional, tetapi murni digital dan digunakan melalui internet.

Mata uang **Bitcoin** tidak terikat pada mata uang fiat tertentu seperti Dolar AS atau Renminbi Tiongkok; ia memiliki nilai tukar yang **mengambang bebas** (*free-floating exchange rates*) terhadap sebagian besar mata uang fiat. Kita dapat membeli dan menjual bitcoin dengan mata uang fiat secara online menggunakan **exchange** (bursa) seperti Kraken atau Bitstamp.

Tidak ada pemerintah atau perusahaan yang mengontrol **Bitcoin**. Sebaliknya, ribuan komputer di seluruh dunia membentuk **jaringan Bitcoin** (*Bitcoin network*) yang secara kolektif menjaga sistem ini tetap berjalan 24/7. Untuk menggunakannya, kita tidak perlu mendaftar atau *sign up* di mana pun—cukup dengan akses internet dan program komputer, misalnya aplikasi seluler (*mobile app*).

> Penting:
>
> * **Bitcoin** (dengan huruf "B" besar) → merujuk pada sistem.
> * **bitcoin** (dengan huruf "b" kecil) → merujuk pada unit mata uangnya.
>   Simbol yang umum digunakan adalah BTC atau XBT.

**Jaringan Bitcoin** bertugas memproses pembayaran, mengamankan **ledger** (buku besar) kepemilikan dari modifikasi yang tidak sah, dan memasukkan bitcoin baru ke dalam sirkulasi sesuai tingkat yang telah ditentukan.

Jaringan ini terdiri dari ribuan komputer di seluruh dunia yang disebut **Bitcoin nodes** atau **nodes**. Siapa pun dapat berpartisipasi aktif dengan menjalankan *node* sendiri. **Kita sebaiknya menjalankan *node* kita sendiri jika tidak ingin mempercayai orang lain untuk memberikan informasi keuangan yang benar.**

---

## Gambaran Besar (The Big Picture)

Mari kita ikuti proses pembayaran **Bitcoin** dalam empat langkah:

### 1. Transaksi (Transactions)

* Alice membuat **transaksi** untuk mengirim 1 bitcoin ke Bob.
* Transaksi ini berisi:

  * Jumlah yang akan dipindahkan (1 bitcoin).
  * Alamat **Bitcoin** tujuan (misalnya: `15vwoaN74MBeF5nr2BH4DKqndEFjHA6MzT`).
  * **Tanda tangan digital** (*digital signature*) yang dibuat dengan **private key** (kunci pribadi) Alice.
* Aplikasi *wallet* Alice terhubung ke satu atau lebih *node* di jaringan, lalu mengirim transaksi tersebut.

### 2. Jaringan Bitcoin (The Bitcoin network)

* Node yang menerima transaksi memverifikasi apakah transaksi valid (Alice punya saldo cukup dan tanda tangan digitalnya sah).
* Jika valid, node akan **meneruskan** transaksi ke node lain (*relaying*).
* Transaksi menyebar ke seluruh jaringan, meskipun **blockchain** belum diperbarui pada tahap ini.

### 3. Blockchain (The Blockchain)

* Node-node memperbarui salinan lokal **Bitcoin blockchain** dengan transaksi Alice.
* Karena ribuan transaksi bisa terjadi bersamaan, satu node membuat **blok** berisi transaksi-transaksi terbaru dalam urutan tertentu.
* Blok ini dikirim ke jaringan, diverifikasi oleh node lain, lalu ditambahkan ke blockchain.
* Nama **blockchain** berasal dari struktur data berupa blok-blok yang dirantai sehingga modifikasi bisa dideteksi.

### 4. Wallet (Dompet)

* Wallet Bob terhubung ke node-node di jaringan.
* Begitu transaksi Alice masuk ke blockchain, wallet Bob akan diberi tahu bahwa ia menerima 1 bitcoin.
* Wallet tidak hanya mengirim/terima transaksi, tapi juga mengelola **private key** dan **alamat Bitcoin** pengguna.

---

## Masalah dengan Uang Saat Ini (Problems with Money Today)

Bitcoin hadir karena memecahkan masalah nyata dalam sistem keuangan tradisional:

* **Segregasi (Segregation):**

  * Sekitar 38% populasi dunia tidak punya rekening bank.
  * Ini membatasi akses ke pembayaran daring dan pinjaman.

* **Masalah Privasi (Privacy Issues):**

  * Bank tahu semua detail transaksi kita dan bisa menjual data tersebut.
  * Pemerintah bisa memaksa penyitaan atau sensor transaksi.

* **Inflasi (Inflation):**

  * Pemerintah bisa mencetak uang untuk mendanai utang, perang, atau program sosial.
  * Ini bisa memicu **hiperinflasi**, yang mengikis tabungan masyarakat.

* **Batas Negara (Borders):**

  * Transfer lintas negara dengan mata uang fiat mahal (4.9%–16.3%) dan kadang dilarang.
  * Di dalam negeri, transfer biasanya mudah.

---

## Pendekatan Bitcoin (The Bitcoin Approach)

Bitcoin menawarkan solusi yang berbeda dari sistem tradisional:

* **Desentralisasi (Decentralized):**

  * Tidak ada otoritas pusat. Kendali dibagi ke ribuan node.
  * Semua pengguna diperlakukan sama.
  * Tidak ada titik pusat untuk menyensor, menolak layanan, atau menyita dana.

* **Pasokan Terbatas (Limited Supply):**

  * Total pasokan bitcoin dibatasi hanya **21 juta**.
  * Tingkat pencetakan berkurang setengah setiap 4 tahun (*halving*).

* **Tanpa Batas (Borderless):**

  * Mengirim bitcoin ke siapa pun di dunia sama mudahnya seperti mengirim email.
  * Setelah sekitar 60 menit, transaksi dianggap final dan tidak bisa dibatalkan.

---

## Bagaimana Bitcoin Digunakan? (How is Bitcoin Used?)

* **Tabungan (Savings):**

  * Simpan **private key** dengan aman (di kertas, aplikasi, atau diingat).
  * Selama kunci privat aman, dana kita aman.

* **Pembayaran Lintas Batas (Cross-border Payments):**

  * Lebih cepat dan murah dibanding sistem remitansi tradisional.

* **Belanja (Shopping):**

  * Bayar tanpa perlu memberikan data sensitif (seperti kartu kredit).

* **Spekulasi (Speculation):**

  * Banyak orang membeli bitcoin untuk trading karena harganya volatil.
  * Jangka panjang diharapkan stabil seiring meningkatnya adopsi.

* **Penggunaan Non-Mata Uang (Noncurrency Uses):**

  * **Kepemilikan (Ownership):** Data kecil (misalnya nomor sasis mobil) bisa disematkan ke transaksi.
  * **Bukti Keberadaan (Proof of Existence):** Hash kriptografi dokumen bisa dicatat di blockchain sebagai bukti keberadaan.

---

## Kapan Tidak Menggunakan Bitcoin? (When Not to Use Bitcoin)

* **Pembayaran Kecil (Tiny Payments):**

  * Biaya transaksi bisa lebih besar dari jumlah yang dikirim.
  * Solusi: **Lightning Network** (untuk micropayments instan & murah).

* **Pembayaran Instan (Instant Payments):**

  * Transaksi butuh waktu konfirmasi ±20 menit.
  * Tanpa konfirmasi, transaksi bisa berisiko **double spend**.
  * Solusi: **Lightning Network**.

---

## Cryptocurrency Lain (Other Cryptocurrencies)

Selain Bitcoin, ada ribuan **altcoin** (alternative coins) seperti **Ethereum**, **Zcash**, dan **Namecoin**.

Nilai suatu cryptocurrency sangat dipengaruhi oleh **efek jaringan** (*network effect*): semakin banyak orang yang menggunakannya, semakin berguna mata uang tersebut. Buku ini berfokus pada **Bitcoin** karena efek jaringan terbesarnya.

---

## Ringkasan (Summary)

* **Bitcoin** adalah uang global tanpa batas yang dapat digunakan oleh siapa saja dengan koneksi internet.
* Jaringan **Bitcoin** memverifikasi dan menyimpan catatan semua transaksi.
* Proses transaksi: dibuat → diverifikasi → masuk ke blockchain → diterima wallet.
* Bitcoin memecahkan masalah inflasi, privasi, batas negara, dan inklusi finansial.
* Ada cryptocurrency lain, tapi Bitcoin tetap paling dominan berkat efek jaringan.

---
