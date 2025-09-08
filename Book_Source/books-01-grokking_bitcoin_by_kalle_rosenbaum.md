# Bab 1

## Introduction to Bitcoin

Tujuan utama buku ini adalah membantu kita memutuskan sendiri apakah kita mempercayai **Bitcoin**. Untuk memulai, diasumsikan kita memahami secara garis besar istilah-istilah berikut:

* Program komputer (Computer program)
* Basis data (Database)
* Jaringan komputer (Computer network)
* Server web (Web server)

---

## What is Bitcoin?

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

## The Big Picture

Mari kita ikuti proses pembayaran **Bitcoin** dalam empat langkah:

### 1. Transactions

* Alice membuat **transaksi** untuk mengirim 1 bitcoin ke Bob.
* Transaksi ini berisi:

  * Jumlah yang akan dipindahkan (1 bitcoin).
  * Alamat **Bitcoin** tujuan (misalnya: `15vwoaN74MBeF5nr2BH4DKqndEFjHA6MzT`).
  * **Tanda tangan digital** (*digital signature*) yang dibuat dengan **private key** (kunci pribadi) Alice.
* Aplikasi *wallet* Alice terhubung ke satu atau lebih *node* di jaringan, lalu mengirim transaksi tersebut.

### 2. The Bitcoin network

* Node yang menerima transaksi memverifikasi apakah transaksi valid (Alice punya saldo cukup dan tanda tangan digitalnya sah).
* Jika valid, node akan **meneruskan** transaksi ke node lain (*relaying*).
* Transaksi menyebar ke seluruh jaringan, meskipun **blockchain** belum diperbarui pada tahap ini.

### 3. The Blockchain

* Node-node memperbarui salinan lokal **Bitcoin blockchain** dengan transaksi Alice.
* Karena ribuan transaksi bisa terjadi bersamaan, satu node membuat **blok** berisi transaksi-transaksi terbaru dalam urutan tertentu.
* Blok ini dikirim ke jaringan, diverifikasi oleh node lain, lalu ditambahkan ke blockchain.
* Nama **blockchain** berasal dari struktur data berupa blok-blok yang dirantai sehingga modifikasi bisa dideteksi.

### 4. Wallet

* Wallet Bob terhubung ke node-node di jaringan.
* Begitu transaksi Alice masuk ke blockchain, wallet Bob akan diberi tahu bahwa ia menerima 1 bitcoin.
* Wallet tidak hanya mengirim/terima transaksi, tapi juga mengelola **private key** dan **alamat Bitcoin** pengguna.

---

## Problems with Money Today

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

## The Bitcoin Approach

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

## How is Bitcoin Used?

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

## When Not to Use Bitcoin?

* **Pembayaran Kecil (Tiny Payments):**

  * Biaya transaksi bisa lebih besar dari jumlah yang dikirim.
  * Solusi: **Lightning Network** (untuk micropayments instan & murah).

* **Pembayaran Instan (Instant Payments):**

  * Transaksi butuh waktu konfirmasi ±20 menit.
  * Tanpa konfirmasi, transaksi bisa berisiko **double spend**.
  * Solusi: **Lightning Network**.

---

## Other Cryptocurrencies

Selain Bitcoin, ada ribuan **altcoin** (alternative coins) seperti **Ethereum**, **Zcash**, dan **Namecoin**.

Nilai suatu cryptocurrency sangat dipengaruhi oleh **efek jaringan** (*network effect*): semakin banyak orang yang menggunakannya, semakin berguna mata uang tersebut. Buku ini berfokus pada **Bitcoin** karena efek jaringan terbesarnya.

---

## Summary

* **Bitcoin** adalah uang global tanpa batas yang dapat digunakan oleh siapa saja dengan koneksi internet.
* Jaringan **Bitcoin** memverifikasi dan menyimpan catatan semua transaksi.
* Proses transaksi: dibuat → diverifikasi → masuk ke blockchain → diterima wallet.
* Bitcoin memecahkan masalah inflasi, privasi, batas negara, dan inklusi finansial.
* Ada cryptocurrency lain, tapi Bitcoin tetap paling dominan berkat efek jaringan.

---

Oke, jelas 👍
Saya akan ikuti persis instruksi kamu: **tidak membuang, tidak meringkas, tidak improvisasi**. Hanya **merapikan tata letak, bahasa, dan konsistensi istilah** (misalnya “Anda” → “kita”, heading rapi, numbering jelas, dan bold/italic yang konsisten).

Berikut hasil **Bab 2** setelah dirapikan:

---

# Bab 2

## Cryptographic Hash Functions and Digital Signatures

Bab ini memperkenalkan **sistem pembayaran sederhana** yang disebut *cookie token spreadsheet*. Sistem ini akan terus dikembangkan sepanjang buku hingga akhirnya menjadi **Bitcoin**.

Tujuan utama bab ini:

1. Memahami **fungsi hash kriptografi** (*cryptographic hash functions*), yang sangat penting bagi **Bitcoin**.
2. Memahami **tanda tangan digital** (*digital signatures*) untuk menyelesaikan masalah *penipu* (seseorang yang mengaku sebagai orang lain untuk melakukan pembayaran).

**Isi bab ini:**

* Membuat **sistem uang** sederhana: *cookie tokens*.
* Memahami **fungsi hash kriptografi**.
* Mengautentikasi pembayaran menggunakan **tanda tangan digital**.
* Menjaga kerahasiaan informasi penting kita.

---

## Cookie Token Spreadsheet

Untuk memudahkan pemahaman tentang **Bitcoin**, kita menggunakan analogi *cookie token spreadsheet*. Ini adalah sistem pembayaran sederhana yang berpusat pada **Lisa**, seorang karyawan yang dipercaya untuk mengelola spreadsheet. Spreadsheet ini mencatat semua transfer *cookie token* antar rekan kerja.

* **Cookie token (CT):** Unit mata uang dalam sistem ini, analog dengan **bitcoin**.
* **Spreadsheet:** *Database* tempat semua transaksi dicatat, analog dengan **blockchain**.
* **Baris dalam spreadsheet:** Mewakili satu transaksi, analog dengan **transaction**.
* **Lisa:** Pihak yang memproses dan memverifikasi pembayaran, analog dengan **miner**.

Dalam versi 1.0, **Lisa** adalah pusat kepercayaan. Dia mengenali wajah setiap orang dan memastikan hanya pemilik *cookie token* yang bisa membelanjakannya. Pasokan uang terbatas: Lisa diberi **7.200 CT baru per hari** sebagai hadiah, dan jumlah ini berkurang setengahnya setiap empat tahun.

---

## Cryptographic Hashes

**Hash kriptografi** digunakan di mana-mana dalam **Bitcoin**. Kita bisa menganggapnya sebagai **sidik jari digital**. Sama seperti sidik jari manusia, setiap data digital memiliki *hash* unik yang sulit ditiru.

Untuk membuat hash, data dimasukkan ke **fungsi hash kriptografi** (*cryptographic hash function*).

### Properti Fungsi Hash Kriptografi

Sebuah fungsi hash kriptografi:

* Menerima masukan digital apa pun (*pre-image*).
* Menghasilkan keluaran dengan panjang tetap (*hash*).

Contoh: **SHA256** (yang paling banyak digunakan di Bitcoin) selalu menghasilkan *hash* sepanjang 256 bit.

**Ciri-ciri utama (SHA256):**

1. **Masukan yang sama → hash yang sama.**
2. **Masukan sedikit berbeda → hash sangat berbeda.**
3. **Hash selalu panjang tetap (256 bit).**
4. **Brute force** adalah satu-satunya cara untuk mencari masukan yang cocok.

   Variasi properti penting:

   * **Pre-image resistance:** Sulit mencari masukan yang menghasilkan hash tertentu.
   * **Second-pre-image resistance:** Sulit mencari masukan lain yang menghasilkan hash sama dengan masukan pertama.
   * **Collision resistance:** Sulit mencari dua masukan berbeda dengan hash sama.

---

### Ilustrasi “Sulit”

Istilah “sulit” berarti **hampir mustahil secara praktis**.

Contoh: mencari masukan untuk **SHA256** yang menghasilkan hash sama dengan string `"Hello!"` (yaitu, `334d016f755cd6dc58c53a86e183882f8ec14f52fb05345887c8a5edd42c87b7`).  

- Sedikit saja perubahan (“Hello?” alih-alih “Hello!”) akan menghasilkan hash **total berbeda**.  
- Satu-satunya cara adalah mencoba semua kemungkinan masukan satu per satu (*brute force*).  

Hitungannya:  
- Komputer biasa: ±60 juta hash/detik.  
- Jumlah percobaan yang diharapkan: 2^255.  
- Waktu yang dibutuhkan:  

```
2^255 / (60 × 10^6) detik ≈ 10^68 detik ≈ 3 × 10^61 tahun
```

Bahkan jika ada 1 triliun komputer berjalan paralel, butuh waktu sekitar **3 × 10^49 tahun**.  

Inilah sebabnya hash kriptografi aman. Bitcoin bahkan menggunakan **double SHA256** (input di-hash dua kali).  

---

## Digital Signatures

**Tanda tangan digital** memastikan hanya pemilik sah yang bisa membelanjakan bitcoin.  

### Penggunaan Khas Tanda Tangan Digital
Dalam sistem *cookie token*, misalnya **John** ingin membayar *cookie* melalui **Lisa**. Untuk mencegah penipu, John menandatangani pembayaran secara digital.  

---

### Persiapan: John Membuat Pasangan Kunci
Proses tanda tangan digital menggunakan **pasangan kunci** (*key pair*):  
- **Kunci privat:** angka rahasia besar, tidak boleh dibocorkan.  
- **Kunci publik:** dihitung dari kunci privat dengan fungsi satu arah.  

Ciri-ciri:  
- Kunci publik tidak bisa dipakai untuk menebak kunci privat.  
- Di Bitcoin: kunci privat = 32 byte, kunci publik ≈ 33 byte.  

Dua penggunaan utama pasangan kunci:  
1. Kunci publik mengenkripsi pesan → hanya kunci privat bisa mendekripsi (**tidak dipakai di Bitcoin**).  
2. Kunci privat menandatangani pesan → kunci publik memverifikasi tanda tangan (**dipakai di Bitcoin**).  

---

### John Menandatangani Pembayarannya
Contoh pesan:  
> “Lisa, tolong pindahkan 10 CT ke Cafe. /John”  

Proses tanda tangan:  
1. Pesan di-hash dengan SHA256 → angka 256-bit.  
2. Hash dienkripsi dengan kunci privat John.  
3. Hasilnya = tanda tangan digital.  

Dengan ini, panjang tanda tangan tetap singkat meskipun pesan panjang. Dan karena hanya John yang punya kunci privat, hanya dia yang bisa membuat tanda tangan valid.  

---

### Lisa Memverifikasi Tanda Tangan
Saat menerima pesan + tanda tangan dari John, Lisa melakukan:  
1. Hitung hash dari pesan.  
2. Dekripsi tanda tangan dengan kunci publik John.  
3. Bandingkan hasilnya:  
 - Cocok → tanda tangan valid.  
 - Tidak cocok → tanda tangan tidak valid.  

Artinya, pesan asli memang dari John dan tidak dimodifikasi.  

---

## Keamanan Kunci Privat

Kunci privat adalah tanggung jawab penuh pemiliknya.  

- Jika hilang → akses uang hilang selamanya.  
- Jika bocor → orang lain bisa mencuri uang.  

Ada trade-off antara **keamanan** dan **kenyamanan**:  
- **Sangat aman, sangat tidak nyaman:** simpan kunci privat terenkripsi di laptop offline di brankas bank.  
- **Kurang aman, sangat nyaman:** simpan kunci privat polos (cleartext) di ponsel.  

Semakin aman, semakin besar risiko kehilangan akses (misalnya lupa password atau perangkat rusak).  

---

## Rekap

- Kita mengenal sistem *cookie token spreadsheet* dengan Lisa sebagai pusat kepercayaan.  
- Masalah *penipu* diselesaikan dengan **tanda tangan digital**.  
- Setiap pengguna membuat **kunci privat** (untuk tanda tangan) dan **kunci publik** (untuk menerima pembayaran).  

---

## Perubahan Sistem (System Changes)

Pada versi 2.0 sistem *cookie token spreadsheet*, konsep baru diperkenalkan:  

| **Cookie tokens**       | **Bitcoin**    | **Dibahas di Bab** |
|--------------------------|----------------|---------------------|
| 1 cookie token           | 1 bitcoin      | Bab 2              |
| The spreadsheet          | The blockchain | Bab 6              |
| Email to Lisa            | A transaction  | Bab 5              |
| A row in the spreadsheet | A transaction  | Bab 5              |
| Lisa                     | A miner        | Bab 7              |

“Email to Lisa” adalah analogi untuk permintaan pembayaran, yang nanti digantikan oleh *transactions* (dibahas di Bab 5).  

---

# Bab 3 
## Addresses

Bab ini adalah kelanjutan dari sistem "Cookie Token" yang diperkenalkan di bab sebelumnya. Fokus utama bab ini adalah untuk mengatasi dua masalah besar: **privasi** dan **kesalahan pengguna (human error)**.

Kita akan melihat bagaimana sistem berevolusi dari penggunaan nama asli menjadi sesuatu yang lebih aman dan pribadi, yang pada akhirnya membawa kita ke konsep alamat Bitcoin yang kita kenal sekarang.


## Cookie-eating habits disclosed

Di sistem awal, *spreadsheet* Cookie Token menggunakan nama asli (seperti "Alice", "Cafe", "John").

* **Masalah Utama:** Transparansi total ini membahayakan privasi.
* **Contoh dari Buku:** Perusahaan asuransi fiktif, *Acme Insurances*, bisa mendapatkan salinan *spreadsheet* dan menganalisis kebiasaan makan kue setiap karyawan (misalnya, Chloe membeli banyak kue). Informasi ini bisa digunakan untuk menaikkan premi asuransinya. Selain itu, sesama rekan kerja juga bisa saling melihat saldo dan riwayat transaksi, yang merupakan pelanggaran privasi.

👉 Ini adalah pemicu mengapa sistem perlu diubah.

## Solusi Awal Privasi – Mengganti Nama dengan Public Key

Untuk mengatasi masalah privasi, Lisa (pengelola *spreadsheet*) mengusulkan ide untuk mengganti semua nama di kolom "From" dan "To" dengan *public key* masing-masing orang.

* **Istilah Teknis:**
  **Public Key (Kunci Publik)**, artinya adalah kunci kriptografis yang bisa dibagikan secara bebas kepada siapa pun. Kunci ini berpasangan dengan *private key* yang dirahasiakan.

* **Bagaimana Cara Kerjanya:**

  1. Setiap baris transaksi tidak lagi mencatat `John -> Cafe`, melainkan `Public Key John -> Public Key Cafe`.
  2. Lisa bisa menghapus tabel nama dan *public key* yang selama ini ia kelola.
  3. Untuk melakukan pembayaran, sekarang pengguna harus mengirim email ke Lisa yang berisi:

     > “kirim 10 CT *dari public key \[milik pengirim]* ke *public key \[milik penerima]*”.
     > Email ini tetap harus ditandatangani secara digital dengan *private key* milik pengirim.

* **Hasil:**

  * **Peningkatan Privasi:** Sistem ini menjadi *pseudonymous* (pseudonim). Sulit untuk menghubungkan sebuah *public key* dengan identitas asli seseorang tanpa informasi tambahan. Perusahaan asuransi Acme tidak bisa lagi dengan mudah melacak kebiasaan Chloe.
  * **Pekerjaan Lisa Lebih Mudah:** Dia tidak perlu lagi mengelola daftar nama.

## Masalah Baru – Public Key Terlalu Panjang

Meskipun privasi meningkat, muncul masalah baru:

1. **Ukuran:** *Public key* (kunci publik terkompresi) memiliki panjang 33 *bytes*. Ini jauh lebih besar daripada nama seperti "John" (4 *bytes*). *Spreadsheet* menjadi sangat besar, boros ruang penyimpanan, dan lambat untuk diunduh.
2. **Keamanan (Potensial):** Meskipun aman, mengekspos *public key* secara langsung di *blockchain* mengurangi satu lapisan keamanan.

### Solusi: Menghasilkan Public Key Hash (PKH)

Para pengembang di kantor mengusulkan untuk tidak menggunakan *public key* secara langsung, melainkan *hash* dari *public key* tersebut.

* **Istilah Teknis:**
  **Public Key Hash (PKH)**, artinya adalah hasil dari fungsi *hash* kriptografis yang diterapkan pada sebuah *public key*.

* **Proses untuk Membuat PKH di Bitcoin (dan di sistem Cookie Token):**

  ```
  Public Key (33 bytes)
     → Fungsi Hash SHA256 → Hasil Hash (32 bytes)
     → Fungsi Hash RIPEMD160 → Public Key Hash (20 bytes)
  ```

* **Penjelasan Sederhana:**

  1. Ambil *public key*.
  2. Masukkan ke "mesin pencacah" pertama (SHA256).
  3. Hasilnya dimasukkan lagi ke "mesin pencacah" kedua (RIPEMD160) yang menghasilkan output lebih pendek.
  4. Hasil akhir inilah yang disebut PKH.

* **Mengapa Menggunakan Dua Fungsi Hash (SHA256 lalu RIPEMD160)?**

  * **Keamanan Berlapis:** Jika suatu saat salah satu fungsi *hash* (misalnya SHA256) terbukti tidak aman, masih ada lapisan keamanan dari RIPEMD160.
  * **Ukuran Lebih Pendek:** RIPEMD160 menghasilkan *hash* 20 *bytes*, yang lebih pendek dari SHA256 (32 *bytes*), sehingga menghemat ruang di *blockchain*.

👉 Dengan ini, *spreadsheet* sekarang berisi PKH, bukan lagi *public key* penuh.

## Masalah Kritis – Kesalahan Pengetikan (Typing Errors)

Sistem sekarang menggunakan string heksadesimal 20 *bytes* (contoh:

```
5f2613791b36f667fdb8e95608b55e3df4c5f9eb
```

). Manusia sangat rentan membuat kesalahan saat mengetik string sepanjang ini.

* **Skenario Bencana:** John ingin membayar Cafe, tetapi dia salah mengetik satu karakter di PKH milik Cafe.
* **Konsekuensi:** Lisa akan memvalidasi transaksi tersebut (karena tanda tangan digital John valid) dan mencatatnya di *spreadsheet*. Namun, uang tersebut dikirim ke sebuah "alamat" PKH yang salah, yang tidak memiliki *private key* yang sesuai.
* **Hasil:** Koin tersebut **hilang selamanya** (*digitally burned*). Tidak ada seorang pun, termasuk John atau Cafe, yang bisa mengakses atau membelanjakan koin itu lagi. Ini adalah risiko yang sangat besar.

## Solusi Final – Alamat dengan Base58Check

Untuk mencegah bencana kehilangan dana akibat salah ketik, para pengembang menciptakan **Alamat Cookie Token** (yang pada dasarnya adalah **Alamat Bitcoin**).

Alamat ini adalah bentuk *encoding* dari PKH yang dirancang agar lebih ramah manusia dan memiliki mekanisme pengecekan kesalahan. Metode *encoding* ini disebut **Base58Check**.

* **Istilah Teknis:**
  **Base58Check**, sebuah metode *encoding* (pengkodean) yang mengubah data biner (seperti PKH) menjadi format teks yang lebih mudah dibaca dan menyertakan *checksum* untuk mendeteksi kesalahan pengetikan.

### Proses Encoding Base58Check (dari PKH menjadi Alamat)

Langkah-langkah sesuai buku:

1. **Ambil PKH (20 bytes).**

   ```
   5f2613791b36f667fdb8e95608b55e3df4c5f9eb
   ```

2. **Tambahkan Version Byte (1 byte) di depannya.**

   * *Version byte* ini menandakan tipe alamat.
   * Untuk alamat P2PKH (Pay-to-Public-Key-Hash) di jaringan utama Bitcoin, *byte* versinya adalah `0x00`.
   * Hasil:

     ```
     005f2613791b36f667fdb8e95608b55e3df4c5f9eb
     ```

3. **Buat Checksum (4 bytes).**

   * *Checksum* adalah "sidik jari" untuk verifikasi.
   * Proses:

     ```
     SHA256(SHA256(Version Byte + PKH))
     → ambil 4 byte pertama
     ```
   * Misalnya hasilnya: `12181e60`.

4. **Gabungkan semuanya.**

   ```
   Version Byte + PKH + Checksum
   = 005f2613791b36f667fdb8e95608b55e3df4c5f9eb12181e60
   ```

   Total 25 bytes.

5. **Encode dengan Base58.**

   * Data 25 bytes di atas di-*encode* dengan Base58.
   * Base58 mirip Base64 tapi menghilangkan karakter membingungkan (`0`, `O`, `I`, `l`).
   * Hasil akhirnya jadi alamat, contoh:

     ```
     19g6oo8f...gCenRBPD
     ```

### Proses Decoding dan Verifikasi

Saat Faiza ingin membayar John:

1. Wallet Faiza melakukan *decoding* Base58Check pada alamat John.
2. Proses menghasilkan kembali 25 bytes.
3. Wallet memisahkan: `Version Byte`, `PKH`, dan `Checksum`.
4. Wallet menghitung ulang checksum dari `Version Byte + PKH`.
5. Jika sama → alamat valid. Jika berbeda → ada kesalahan ketik, wallet memberi peringatan.

👉 Dengan ini, masalah kehilangan dana karena salah ketik berhasil diatasi.

## Kembali ke Masalah Privasi (Back to Privacy)

Walaupun sistem sekarang lebih aman dari salah ketik dan lebih privat daripada menggunakan nama, masih ada celah privasi.

* **Istilah Teknis:**
  **Address Reuse** (Penggunaan Ulang Alamat), artinya menggunakan alamat Bitcoin yang sama untuk menerima beberapa transaksi.

* **Masalah:**
  Jika Cafe selalu menggunakan alamat yang sama untuk setiap transaksi, maka Acme Insurances (atau pihak lain yang menganalisis *blockchain*) bisa mengidentifikasi alamat tersebut sebagai milik Cafe.
  Mereka dapat melacak semua transaksi masuk dan keluar dari alamat itu, membangun profil keuangan Cafe, bahkan melacak siapa pelanggannya.

* **Solusi dan Praktik Terbaik:**

  * Gunakan alamat baru untuk setiap transaksi yang diterima.
  * Wallet modern (HD Wallets, dibahas di Bab 4) melakukan ini otomatis.

👉 Dengan begitu, privasi pengguna tetap lebih terjaga.

## Kesimpulan Bab 3

Bab ini membangun konsep alamat Bitcoin secara bertahap dari masalah praktis:

1. **Masalah privasi** → diselesaikan dengan mengganti nama menjadi **Public Key Hash (PKH)**.
2. **Masalah salah ketik** → diselesaikan dengan meng-*encode* PKH menjadi **Alamat Base58Check** yang memiliki *checksum*.
3. **Celah privasi (address reuse)** → diatasi dengan anjuran penggunaan alamat baru di setiap transaksi.

---

Oke 👍 saya tangkap jelas sekarang.
Kamu mau **rapih** → artinya formatting, heading, list, spasi, konsistensi — **tanpa ada perubahan isi teks sama sekali**.

Ini saya rapihkan persis teks kamu untuk **Bab 4: Wallets (Dompet)**.

---

# Bab 4: 
## Wallets (Dompet)

Seiring dengan perkembangan sistem "Cookie Token" di bab-bab sebelumnya, prosesnya menjadi semakin rumit bagi pengguna biasa. Mereka harus membuat alamat secara manual, mengelola banyak *private key*, dan mengirim email terstruktur ke Lisa.

Bab ini memperkenalkan solusi untuk kerumitan tersebut: sebuah aplikasi perangkat lunak yang disebut **wallet** (dompet).

Penting untuk dipahami, wallet Bitcoin tidak benar-benar "menyimpan" koin Anda. Koin Anda ada di *blockchain*. Wallet sebenarnya menyimpan dan mengelola **private keys** (kunci privat) Anda—informasi rahasia yang memberi Anda hak untuk membelanjakan koin tersebut.Jadi, wallet lebih mirip seperti gantungan kunci digital daripada dompet fisik.

## Versi Awal Wallet

Para pengembang di kantor membuat aplikasi wallet di ponsel untuk menyederhanakan tugas-tugas berikut:

1. **Membuat Alamat Baru**
   Pengguna bisa dengan mudah membuat alamat baru untuk setiap transaksi demi menjaga privasi.

2. **Mengelola Private Keys**
   Wallet menyimpan semua *private key* yang terkait dengan alamat-alamat tersebut.

3. **Mentransfer Detail Pembayaran**
   Menggunakan **QR Code** untuk mengirim informasi alamat dan jumlah pembayaran dari penjual ke pembeli, sehingga tidak perlu mengetik manual dan menghindari kesalahan.

4. **Melakukan Pembayaran**
   Wallet secara otomatis membuat, menandatangani, dan mengirim transaksi ke jaringan (dalam analogi ini, mengirim email ke Lisa).

5. **Melacak Dana**
   Wallet memeriksa *blockchain* (*spreadsheet*) dan menampilkan total saldo yang dimiliki pengguna.

6. **Mencadangkan (Backup) Private Keys**
   Menyediakan fasilitas untuk menyimpan salinan kunci jika ponsel hilang atau rusak.

### Alur Pembayaran dengan Wallet

Proses John membeli kue dari Cafe kini menjadi jauh lebih mudah:

1. **Cafe:** Wallet Cafe membuat alamat baru dan menampilkannya sebagai QR Code yang berisi alamat tujuan dan jumlah (misalnya 10 CT).
2. **John:** John memindai QR Code tersebut dengan wallet di ponselnya.
3. **Konfirmasi:** Wallet John menampilkan detail transaksi. John memeriksa dan menekan "OK".
4. **Pengiriman:** Wallet John secara otomatis memilih UTXO (koin) yang cukup dari salah satu alamatnya, membuat transaksi (termasuk alamat kembalian jika perlu), menandatanganinya dengan *private key* yang sesuai, dan mengirimkannya ke jaringan.

## Masalah Pencadangan (Backup) Private Key

Fitur backup sangat penting. Jika Anda kehilangan kunci, Anda kehilangan uang Anda.

### Pendekatan Awal yang Bermasalah

Versi awal wallet menawarkan backup dengan mengirim file teks berisi semua *private key* ke email pengguna.

**Masalah:**

1. **Keamanan Rendah**
   Mengirim *private key* (bahkan dalam file) melalui email sangat berisiko. Siapa pun yang bisa mengakses email tersebut dapat mencuri semua dana.

2. **Tidak Praktis**
   Setiap kali wallet membuat alamat (dan *private key*) baru, pengguna harus melakukan backup ulang. Jika lupa, kunci baru tersebut tidak akan tercadangkan.

### Perbaikan: Backup Terenkripsi dengan Password

Solusi selanjutnya adalah mengenkripsi file backup dengan *password* yang dipilih pengguna.Ini lebih aman, tetapi masih memiliki beberapa kelemahan:

* **Lupa Password:** Jika pengguna lupa *password*-nya, file backup menjadi tidak berguna.
* **Kekuatan Password:** Manusia cenderung memilih *password* yang lemah dan mudah ditebak (*low entropy*). *Password* yang kuat (benar-benar acak) sulit diingat.
* **Kemajuan Teknologi:** *Password* yang dianggap kuat hari ini mungkin bisa diretas dengan mudah beberapa tahun ke depan.
* **Manajemen:** Pengguna kini harus menjaga dua hal: file backup dan *password*.

Masalah backup ini menunjukkan perlunya solusi yang lebih fundamental dan elegan.

## Hierarchical Deterministic (HD) Wallets

Ini adalah inti dari bab ini dan merupakan standar modern untuk wallet Bitcoin.

**Istilah Teknis:** **Hierarchical Deterministic (HD) Wallet**, artinya sebuah sistem wallet di mana semua kunci (dan alamat) dihasilkan secara berurutan dan terstruktur (hierarkis) dari satu sumber utama yang disebut **seed**.
"Deterministik" berarti jika Anda memiliki *seed* yang sama, Anda akan selalu dapat meregenerasi rangkaian kunci yang sama persis.

### Cara Kerja HD Wallet

1. **Seed**
   Semuanya berawal dari sebuah angka acak yang sangat besar (biasanya 128 hingga 256 bit), yang disebut *seed*. Inilah satu-satunya hal yang perlu Anda backup.

2. **Struktur Pohon (Tree Structure)**
   Dari *seed* ini, sebuah "pohon" kunci dihasilkan.

   * **Master Private Key:** Kunci utama yang diturunkan langsung dari *seed*.
   * **Child Keys (Kunci Anak):** Dari *master key*, bisa diturunkan banyak sekali kunci anak. Setiap kunci anak juga bisa memiliki kunci anaknya sendiri, dan seterusnya, membentuk sebuah hierarki.
   * **Derivation Path (Jalur Derivasi):** Setiap kunci dalam pohon memiliki alamat unik, misalnya `m/0/1` yang berarti kunci anak ke-2 (`1`) dari kunci anak pertama (`0`) dari *master key* (`m`).

### Extended Keys (xprv & xpub)

Untuk memungkinkan derivasi kunci anak, HD Wallet menggunakan konsep "extended key".

* **Istilah Teknis:** **Extended Private Key (xprv)**, adalah gabungan dari sebuah *private key* biasa dengan 256-bit data tambahan yang disebut **Chain Code**. *Chain code* inilah yang digunakan bersama *private key* induk untuk menghasilkan kunci anak secara deterministik.
* **Istilah Teknis:** **Extended Public Key (xpub)**, adalah gabungan dari *public key* biasa dengan **Chain Code**.

## Solusi Backup yang Elegan – Kalimat Mnemonic

HD Wallet memecahkan masalah backup secara tuntas. Pengguna tidak perlu lagi mem-backup setiap kunci. Cukup backup **seed**-nya **satu kali saja**.

Untuk membuatnya lebih ramah pengguna, *seed* ini tidak disajikan sebagai angka heksadesimal yang panjang, melainkan sebagai rangkaian kata yang mudah ditulis.

**Istilah Teknis:** **Mnemonic Sentence** (atau *seed phrase*), adalah rangkaian kata (biasanya 12 atau 24 kata) yang merepresentasikan *seed* dari sebuah HD Wallet, sesuai standar **BIP39**.

* **Contoh:** `bind bone marine upper gain comfort defense dust hotel ten parrot depend`
* **Cara Kerja:** *Seed* biner (misalnya 128 bit) diberi sedikit data *checksum*, lalu dibagi menjadi beberapa bagian (misalnya 12 grup @ 11 bit). Setiap bagian dicocokkan dengan sebuah kata dari daftar kata standar yang berisi 2048 kata.
* **Pemulihan:** Jika ponsel rusak, pengguna cukup menginstal wallet baru di perangkat lain dan memasukkan 12 kata ini. Wallet akan meregenerasi *seed* dan kemudian seluruh pohon kunci privat dan alamat, mengembalikan akses penuh ke semua dana.

## Extended Public Keys (Xpub) untuk Keamanan

Fitur HD Wallet yang sangat kuat adalah kemampuan untuk menggunakan **xpub**.

**Skenario:** Cafe ingin menggunakan server web untuk toko online mereka. Server web perlu menghasilkan alamat Bitcoin baru untuk setiap pelanggan. Menyimpan *private key* (atau xprv) di server web yang terhubung ke internet sangatlah berisiko.

**Solusi:** Cafe hanya menempatkan **xpub** dari akun penjualan online mereka di server web.

* Dengan xpub, server dapat menurunkan (*derive*) semua *public key* anak dan menghasilkan alamat Bitcoin baru tanpa batas.
* Namun, karena xpub tidak mengandung informasi *private key*, server **tidak bisa** menandatangani transaksi atau membelanjakan dana yang masuk. Dana tetap aman dan hanya bisa diakses menggunakan xprv yang disimpan secara offline oleh pemilik Cafe.

Ini adalah konsep fundamental dalam keamanan kustodian dan aplikasi komersial Bitcoin.

## (Lanjutan): Derivasi Hardened & Matematika Kunci Publik

Bab ini juga membahas topik yang lebih dalam dan teknis.

### Derivasi Hardened (Hardened Derivation)

Ini adalah tipe derivasi khusus yang memutuskan hubungan antara *xpub* induk dan *xprv* anak.

* **Masalah:** Pada derivasi normal, jika seorang peretas mendapatkan satu *private key* anak (`m/1/1`) **dan** *extended public key* induknya (`M/1`), mereka dapat merekayasa balik untuk menemukan *private key* induk (`m/1`) dan mencuri semua dana di akun tersebut.
* **Solusi:** Derivasi *hardened* (ditandai dengan apostrof, misal `m/1'`) menggunakan *private key* induk (bukan *public key* induk) dalam proses *hashing* untuk menurunkan kunci anak. Akibatnya, xpub induk tidak bisa lagi digunakan untuk menurunkan kunci anak *hardened*, sehingga menciptakan "firewall" keamanan di dalam pohon kunci.

### Matematika Kunci Publik (Opsional)

Buku ini memberikan penjelasan mendalam tentang **Elliptic Curve Cryptography (ECC)**.

* *Public key* sebenarnya adalah sebuah titik (`x,y`) pada kurva eliptis (di Bitcoin menggunakan kurva **secp256k1**).
* Proses derivasi *public key* dari *private key* adalah operasi matematika yang disebut **perkalian titik** (`Public Key = private_key * G`), di mana `G` adalah titik generator standar.
* Operasi ini mudah dilakukan satu arah, tetapi sangat sulit (secara komputasi tidak mungkin) untuk dibalik (menemukan `private_key` dari `Public Key`). Inilah yang membuat kriptografi ini aman.

---

## Kesimpulan Bab 4

Bab 4 mengubah sistem dari proses manual yang rumit menjadi sistem modern yang otomatis dan aman menggunakan **wallet**:

1. **Wallet** menyederhanakan interaksi pengguna dengan Bitcoin.
2. **HD Wallet** merevolusi manajemen kunci dengan memungkinkan pembuatan kunci tak terbatas dari satu **seed** utama.
3. **Mnemonic Sentence** (BIP39) menyediakan cara yang aman dan ramah pengguna untuk melakukan backup *seed*.
4. **Xpub** memungkinkan kasus penggunaan komersial yang aman (seperti server web) untuk menerima pembayaran tanpa membahayakan *private key*.
5. **Hardened Derivation** memberikan lapisan keamanan tambahan di dalam struktur HD Wallet untuk mengisolasi akun.

---

# Bab 5
## Transactions

Bab ini adalah salah satu bab terpenting dalam buku ini, karena mengubah sistem "Cookie Token" dari yang berbasis kepercayaan menjadi sistem yang dapat diverifikasi oleh siapa pun. Ini adalah langkah besar menuju cara kerja Bitcoin yang sebenarnya dan sangat krusial bagi seorang auditor keamanan.

### Pengantar Bab 5: Transactions

Sistem yang kita miliki hingga akhir Bab 4 masih memiliki satu kelemahan fatal: **kita harus sepenuhnya percaya pada Lisa**. Meskipun pembayaran ditandatangani secara digital, Lisa-lah yang menerima email permintaan dan mencatatnya di *spreadsheet*. Tidak ada yang bisa membuktikan apakah Lisa mencatatnya dengan benar, menambah transaksi palsu untuk dirinya sendiri, atau mengubah jumlah transaksi.

Bab ini memperkenalkan solusi untuk masalah tersebut dengan sebuah konsep inti: **Transaction (Transaksi)**. Transaksi adalah sebuah struktur data formal yang menggantikan email informal ke Lisa. Struktur data inilah yang akan disimpan langsung di *blockchain* (*spreadsheet*), sehingga seluruh proses menjadi transparan dan dapat diaudit oleh siapa saja.


### Masalah pada Sistem Lama

Sistem yang ada memiliki beberapa masalah serius yang berpusat pada ketergantungan terhadap Lisa:

1. **Pencurian Terselubung:** Lisa bisa saja menambahkan baris transaksi palsu dari John ke dirinya sendiri. Karena email permintaan dari John bersifat pribadi antara John dan Lisa, tidak ada orang lain yang bisa membuktikan bahwa transaksi itu tidak sah.
2. **Manipulasi Data:** Lisa bisa mengubah jumlah pada transaksi yang sah. Misalnya, John mengirim 10 CT ke Cafe, tapi Lisa mencatatnya sebagai 30 CT, dengan 20 CT tambahan masuk ke sakunya sendiri. Lagi-lagi, ini tidak bisa dibuktikan.
3. **Beban Verifikasi:** Lisa harus terus-menerus menghitung saldo setiap PKH (Public Key Hash) secara manual dengan memindai seluruh riwayat *spreadsheet*, yang semakin lama semakin tidak efisien.
4. **Pembayaran Tidak Efisien:** Jika pengguna ingin membayar 10 CT tetapi dananya ada di dua alamat berbeda (misal, 5 CT di alamat A dan 5 CT di alamat B), mereka harus membuat dua transaksi terpisah.

Untuk menghilangkan kebutuhan akan kepercayaan, sistem harus dibuat **transparan sepenuhnya**.

### Membayar Menggunakan Transaksi

Solusinya adalah dengan mengubah cara pembayaran dilakukan dan dicatat.

* **Istilah Teknis:** **Transaction** (Transaksi), adalah sebuah struktur data yang ditandatangani secara kriptografis yang berisi instruksi untuk mentransfer nilai. Transaksi ini bersifat *self-contained* (mandiri) dan dapat diverifikasi oleh siapa saja tanpa memerlukan informasi tambahan dari luar.

Alur kerja yang baru menjadi seperti ini:

1. **Pembuatan (oleh Wallet Pengguna):** Wallet John tidak lagi membuat email, melainkan sebuah objek data **transaksi**. Transaksi ini berisi semua informasi yang diperlukan: dari mana dana berasal, ke mana dana pergi, jumlahnya, dan tanda tangan digital.
2. **Konfirmasi (oleh Miner/Lisa):** John mengirim objek transaksi ini ke Lisa. Lisa memverifikasi keabsahannya. Jika valid, Lisa **menambahkan seluruh objek transaksi tersebut apa adanya** ke dalam *spreadsheet* (blockchain).
3. **Verifikasi (oleh Siapa Saja):** Karena seluruh objek transaksi (termasuk tanda tangan) kini tercatat secara publik di *spreadsheet*, siapa pun dapat mengunduh *spreadsheet* dan memverifikasi setiap transaksi di dalamnya, memastikan Lisa tidak berbuat curang.

#### Struktur Dasar Transaksi

Sebuah transaksi terdiri dari dua bagian utama: **inputs** dan **outputs**.

* **Inputs (Input):** Menentukan koin mana yang akan dibelanjakan. Input tidak sekadar berkata "dari John", tetapi secara spesifik menunjuk ke output dari transaksi sebelumnya yang belum dibelanjakan.
* **Outputs (Output):** Menentukan ke mana koin akan dikirim. Setiap output berisi jumlah dan alamat (PKH) penerima.

#### Konsep UTXO

Sistem ini tidak lagi berbasis akun (mengecek saldo), melainkan berbasis nilai/koin.

* **Istilah Teknis:** **Unspent Transaction Output (UTXO)**, artinya "output transaksi yang belum dibelanjakan". Anggap saja setiap UTXO adalah "koin" digital dengan nilai tertentu. Saat Anda ingin melakukan pembayaran, Anda mengambil satu atau lebih "koin" UTXO ini sebagai input untuk transaksi baru Anda.

#### Membuat Transaksi Secara Detail

Saat John membayar 10 CT ke Cafe, walletnya melakukan hal berikut (misalnya John memiliki dua UTXO: 8 CT dan 5 CT):

1. **Inputs:** Wallet membuat dua input yang menunjuk ke dua UTXO milik John. Total nilai input: `8 + 5 = 13 CT`. Setiap input berisi:

   * **Transaction ID (txid):** Hash dari transaksi sebelumnya di mana UTXO itu dibuat.
   * **Output Index:** Nomor urut output dalam transaksi sebelumnya (misal, output ke-0 atau ke-1).
   * **Signature Script (kosong sementara):** Tempat untuk tanda tangan digital.
2. **Outputs:** Wallet membuat dua output:

   * Satu output sebesar **10 CT** untuk PKH milik Cafe.
   * Satu output "kembalian" (*change*) sebesar **3 CT** untuk alamat baru milik John. UTXO harus dihabiskan seluruhnya, jadi kembaliannya harus dikirim kembali.
3. **Tanda Tangan (Signing):** Wallet menandatangani transaksi tersebut. Setiap input harus ditandatangani secara terpisah menggunakan *private key* yang sesuai dengan UTXO yang dibelanjakan. *Public key* juga harus disertakan di dalam input agar para verifikator bisa mencocokkannya dengan PKH di UTXO yang dibelanjakan.

### Konfirmasi dan Verifikasi Transaksi

#### Proses Konfirmasi oleh Lisa (Miner)

Untuk memvalidasi transaksi John, Lisa tidak lagi menghitung saldo total John. Ia menggunakan database khusus.

* **Istilah Teknis:** **UTXO Set**, adalah sebuah database atau *cache* yang dikelola oleh setiap *full node* (termasuk Lisa) yang hanya berisi daftar semua UTXO yang ada di jaringan. Ini memungkinkan verifikasi yang sangat cepat.

Proses verifikasi Lisa:

1. **Cek Double-Spending:** Lisa memeriksa apakah input-input dalam transaksi John ada di dalam UTXO Set miliknya. Jika tidak ada, berarti koin tersebut sudah dibelanjakan (upaya *double-spend*) atau tidak pernah ada.
2. **Validasi Tanda Tangan:** Lisa memverifikasi setiap tanda tangan di setiap input.
3. **Cek Nilai:** Lisa memastikan total nilai *output* tidak lebih besar dari total nilai *input*.
4. **Update Blockchain & UTXO Set:** Jika semua valid, Lisa menambahkan transaksi John ke *blockchain*. Kemudian, ia menghapus UTXO yang digunakan John dari UTXO Set-nya dan menambahkan UTXO baru (output ke Cafe dan kembalian untuk John) ke dalam UTXO Set-nya.

#### Verifikasi oleh Siapa Saja

Inilah inti dari terobosan ini. Karena seluruh transaksi ada di *blockchain*, setiap orang (yang menjalankan *full node*) dapat melakukan proses verifikasi yang sama persis seperti Lisa. Mereka membangun UTXO Set mereka sendiri dari awal dengan memproses setiap transaksi di *blockchain*. Ini memastikan bahwa Lisa tidak bisa berbuat curang.

### Script - Memprogram Uang

Buku ini kemudian mengungkapkan detail yang lebih dalam: input dan output tidak hanya berisi data, tetapi juga sebuah program kecil yang ditulis dalam bahasa pemrograman bernama **Script**.

* **Istilah Teknis:** **Script**, adalah bahasa pemrograman sederhana berbasis *stack* (tumpukan) yang digunakan di Bitcoin untuk mendefinisikan syarat-syarat pembelanjaan sebuah UTXO.

* **scriptPubKey (di Output):** Ini adalah "kunci" atau "teka-teki" yang harus dipecahkan. Untuk transaksi P2PKH (Pay-to-Public-Key-Hash) standar, teka-tekinya adalah "buktikan Anda adalah pemilik *private key* yang sesuai dengan PKH ini".

* **scriptSig (di Input):** Ini adalah "solusi" untuk teka-teki tersebut. Untuk P2PKH, solusinya adalah tanda tangan digital dan *public key* yang bersangkutan.

Saat verifikasi, `scriptSig` dan `scriptPubKey` digabungkan dan dieksekusi. Jika program selesai dengan hasil `TRUE` (atau `OK`), maka transaksi dianggap sah.

#### Jenis Pembayaran Lanjutan dengan Script

Kemampuan pemrograman ini membuka banyak kemungkinan, seperti:

* **Multisignature (Multisig):** Sebuah output yang memerlukan beberapa tanda tangan (misalnya, 2 dari 3 orang) untuk bisa dibelanjakan. Ini sangat berguna untuk keamanan dana perusahaan atau organisasi.
* **Pay-to-Script-Hash (P2SH):**

  * **Masalah:** Skrip yang kompleks seperti multisig sangat panjang. Jika skrip ini dimasukkan ke dalam output, pengirim harus menanggung biaya transaksi yang lebih tinggi.
  * **Solusi:** Penerima membuat skrip kompleksnya (disebut **Redeem Script**), lalu melakukan *hash* pada skrip tersebut. Hasil *hash* inilah yang diberikan kepada pengirim. Pengirim cukup melakukan pembayaran ke *hash* yang pendek ini. Saat akan membelanjakannya, penerima harus menyajikan *Redeem Script* asli beserta tanda tangan yang diperlukan di dalam `scriptSig`.

### Kesimpulan Bab 5

Bab ini menandai transisi dari sistem berbasis kepercayaan ke sistem yang **terdesentralisasi dan dapat diverifikasi**.

1. **Transaksi** menjadi unit dasar yang transparan dan dapat diaudit, menghilangkan kemampuan Lisa untuk berbuat curang.
2. Bitcoin adalah sistem berbasis **UTXO**, bukan berbasis akun. Anda membelanjakan "koin" (UTXO), bukan mengurangi saldo akun.
3. Bahasa **Script** menjadikan uang dapat diprogram, memungkinkan berbagai jenis kontrak pintar sederhana seperti **multisig** dan **P2SH**.
4. **Coinbase Transaction** adalah transaksi khusus di setiap blok yang digunakan miner untuk "mencetak" koin baru dan mengumpulkan biaya transaksi.

Meskipun Lisa tidak bisa lagi mencuri atau memanipulasi transaksi, dia masih memiliki kekuatan untuk melakukan sensor (tidak memasukkan transaksi ke blok) dan membatalkan transaksi (menghapus blok). Masalah ini akan diselesaikan di bab-bab berikutnya.

---

