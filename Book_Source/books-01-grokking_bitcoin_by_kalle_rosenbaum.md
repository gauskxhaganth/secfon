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


## Bagian 1: Cookie-eating habits disclosed

Di sistem awal, *spreadsheet* Cookie Token menggunakan nama asli (seperti "Alice", "Cafe", "John").

* **Masalah Utama:** Transparansi total ini membahayakan privasi.
* **Contoh dari Buku:** Perusahaan asuransi fiktif, *Acme Insurances*, bisa mendapatkan salinan *spreadsheet* dan menganalisis kebiasaan makan kue setiap karyawan (misalnya, Chloe membeli banyak kue). Informasi ini bisa digunakan untuk menaikkan premi asuransinya. Selain itu, sesama rekan kerja juga bisa saling melihat saldo dan riwayat transaksi, yang merupakan pelanggaran privasi.

👉 Ini adalah pemicu mengapa sistem perlu diubah.

## Bagian 2: Solusi Awal Privasi – Mengganti Nama dengan Public Key

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

## Bagian 3: Masalah Baru – Public Key Terlalu Panjang

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

## Bagian 4: Masalah Kritis – Kesalahan Pengetikan (Typing Errors)

Sistem sekarang menggunakan string heksadesimal 20 *bytes* (contoh:

```
5f2613791b36f667fdb8e95608b55e3df4c5f9eb
```

). Manusia sangat rentan membuat kesalahan saat mengetik string sepanjang ini.

* **Skenario Bencana:** John ingin membayar Cafe, tetapi dia salah mengetik satu karakter di PKH milik Cafe.
* **Konsekuensi:** Lisa akan memvalidasi transaksi tersebut (karena tanda tangan digital John valid) dan mencatatnya di *spreadsheet*. Namun, uang tersebut dikirim ke sebuah "alamat" PKH yang salah, yang tidak memiliki *private key* yang sesuai.
* **Hasil:** Koin tersebut **hilang selamanya** (*digitally burned*). Tidak ada seorang pun, termasuk John atau Cafe, yang bisa mengakses atau membelanjakan koin itu lagi. Ini adalah risiko yang sangat besar.

## Bagian 5: Solusi Final – Alamat dengan Base58Check

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

## Bagian 6: Kembali ke Masalah Privasi (Back to Privacy)

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

