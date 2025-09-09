# Bab 1
## Pengenalan Bitcoin

Bab ini bertujuan untuk memberi Kita pemahaman dasar tentang apa itu Bitcoin, mengapa ia penting, dan bagaimana cara kerjanya secara garis besar. Bab ini adalah fondasi sebelum kita masuk ke aspek-aspek teknis yang lebih dalam di bab-bab berikutnya.

#### **1. What is Bitcoin? (Apa itu Bitcoin?)**

Bitcoin adalah sebuah **sistem kas digital**. Sistem ini memungkinkan orang untuk mengirim *bitcoin* (unit mata uangnya) satu sama lain tanpa memerlukan perantara seperti bank atau pihak ketiga terpercaya lainnya. Kita bisa membayangkannya seperti uang tunai (koin dan kertas), tetapi sepenuhnya digital dan digunakan melalui internet.

**Istilah Penting:**

* **Bitcoin (dengan 'B' besar):** Mengacu pada sistem atau jaringannya secara keseluruhan.
* **bitcoin (dengan 'b' kecil):** Mengacu pada unit mata uangnya (simbol yang umum digunakan adalah BTC atau XBT). 

Tidak ada pemerintah atau perusahaan yang mengendalikan Bitcoin. Sebaliknya, ribuan komputer di seluruh dunia yang terhubung dalam **Jaringan Bitcoin (Bitcoin Network)** secara kolektif menjaga sistem ini tetap berjalan 24/7. Untuk menggunakan Bitcoin, Kita tidak perlu mendaftar; Kita hanya butuh koneksi internet dan sebuah program komputer, seperti aplikasi di ponsel.

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
  <img src="images/books-01-grokking_bitcoin/figure_1.1.png" alt="gambar" width="500"/>
</p>

Ekosistem Bitcoin diilustrasikan dengan Jaringan Bitcoin (kumpulan komputer/node yang terhubung) di tengah. Di sekelilingnya ada berbagai partisipan: Pengguna akhir, Pengguna korporat, Pedagang, Layanan Bitcoin, Bursa, Pengembang, dan Protokol di atas Bitcoin. Jaringan ini bertanggung jawab atas keamanan, pencetakan bitcoin baru, dan pemrosesan pembayaran.

#### **2. The big picture (Gambaran Besarnya)**

Bagian ini menjelaskan alur pembayaran Bitcoin dalam empat langkah sederhana, menggunakan contoh Alice yang ingin membayar 1 BTC kepada Bob.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_1.2.png" alt="gambar" width="500"/>
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

#### **3. Problems with money today (Masalah dengan uang saat ini)**

Bitcoin diciptakan untuk menyelesaikan beberapa masalah yang melekat pada sistem keuangan tradisional.

* **Segregation (Pemisahan):** Sekitar 38% populasi dunia tidak memiliki akses ke rekening bank. Tanpa layanan perbankan, mereka sulit berpartisipasi dalam ekonomi digital dan global. Hal ini bisa disebabkan oleh biaya yang mahal, kurangnya dokumen identitas, atau diskriminasi.
* **Privacy issues (Masalah Privasi):** Dengan pembayaran elektronik konvensional (kartu kredit, transfer bank), pemerintah atau lembaga keuangan dapat dengan mudah melacak, menyensor, membekukan, atau bahkan menyita dana Kita.
* **Inflation (Inflasi):** Inflasi adalah penurunan daya beli mata uang. Selembar uang hari ini bisa membeli lebih sedikit barang di masa depan. Ini terjadi karena pemerintah dapat mencetak lebih banyak uang, yang mengurangi nilai dari uang yang sudah beredar. Kasus ekstrem disebut *hyperinflation*, seperti yang terjadi di Zimbabwe.
* **Borders (Batas Negara):** Mengirim uang antar negara seringkali lambat, mahal, dan rumit. Layanan seperti Western Union bisa memotong biaya hingga 16% atau lebih untuk remitansi tunai.

#### **4. The Bitcoin approach (Pendekatan Bitcoin)**

Bitcoin menawarkan model yang berbeda untuk mengatasi masalah-masalah di atas.

* **Decentralized (Terdesentralisasi):** Tidak ada satu entitas pun (bank atau pemerintah) yang mengendalikan Bitcoin. Kontrol didistribusikan ke ribuan *node* di seluruh dunia. Ini membuat Bitcoin bersifat *permissionless* (tanpa izin), siapa pun bisa berpartisipasi, dan tahan terhadap sensor.
* **Limited supply (Pasokan Terbatas):** Hanya akan pernah ada total 21 juta bitcoin. Pasokan ini tidak bisa ditambah sesuka hati, sehingga membuatnya tahan terhadap inflasi tinggi yang disebabkan oleh pencetakan uang berlebih. Saat ini, pasokan terus bertambah melalui hadiah blok untuk para *miner*, tetapi laju penambahannya berkurang setengahnya setiap empat tahun.
* **Borderless (Tanpa Batas):** Karena berjalan di internet, Bitcoin bersifat global. Mengirim bitcoin ke orang di seberang benua sama mudahnya dengan mengirim ke orang di ruangan yang sama.

#### **5. How is Bitcoin used? (Bagaimana Bitcoin Digunakan?)**

* **Savings (Tabungan):** Kita dapat menyimpan kekayaan dengan aman hanya dengan mengamankan *private key* Kita. Kita bisa menyimpannya di kertas, aplikasi, atau bahkan menghafalnya.
* **Cross-border payments (Pembayaran Lintas Batas):** Bitcoin seringkali lebih murah dan cepat untuk mengirim uang ke luar negeri dibandingkan layanan remitansi tradisional.
* **Shopping (Belanja):** Ideal untuk pembayaran online karena aman. Kita tidak memberikan informasi sensitif (seperti detail kartu kredit) kepada pedagang, hanya mengirim jumlah yang disepakati. 
* **Speculation (Spekulasi):** Harga bitcoin sangat fluktuatif (naik turun), yang menarik bagi sebagian orang untuk mencoba membeli saat harga rendah dan menjual saat harga tinggi.
* **Non-currency uses (Penggunaan Non-Mata Uang):** Karena data kecil bisa disematkan dalam transaksi, Bitcoin bisa digunakan untuk hal lain:

  * **Ownership (Kepemilikan):** Mencatat transfer kepemilikan aset, seperti mobil, dengan menyertakan nomor sasis dalam transaksi.
  * **Proof of existence (Bukti Keberadaan):** Membuktikan bahwa sebuah dokumen digital sudah ada pada waktu tertentu dengan "menjangkarkan" sidik jari digital (*cryptographic hash*) dari dokumen tersebut ke dalam *blockchain*. 

#### **6. When not to use Bitcoin (Kapan Sebaiknya Tidak Menggunakan Bitcoin)**

Bitcoin belum cocok untuk semua hal:

* **Tiny payments (Pembayaran Sangat Kecil):** Biaya transaksi (*transaction fee*) terkadang bisa lebih mahal dari jumlah yang dikirim, membuatnya tidak ekonomis untuk pembayaran mikro. (Teknologi lapisan kedua seperti Lightning Network mencoba mengatasi ini).
* **Instant payments (Pembayaran Instan):** Transaksi Bitcoin memerlukan waktu (biasanya sekitar 10–60 menit) untuk mendapatkan konfirmasi yang aman. Ini tidak ideal untuk pembelian cepat seperti secangkir kopi.
* **Savings you can’t afford to lose (Tabungan yang Tidak Sanggup Kita Kehilangan):** Bitcoin masih merupakan teknologi baru dan harganya sangat fluktuatif. Ada juga risiko kehilangan *private key* Kita secara permanen. Jangan menaruh semua uang yang tidak bisa Kita relakan kehilangannya. **Di Bitcoin, Kita bertanggung jawab penuh atas keamanan dana Kita sendiri.**

#### **7. Other cryptocurrencies (Mata Uang Kripto Lainnya)**

Selain Bitcoin, ada ribuan mata uang kripto lain yang disebut *alt-coin* (koin alternatif). Beberapa menawarkan fitur unik (seperti privasi yang lebih tinggi), sementara yang lain mungkin hanya tiruan atau bahkan penipuan.

Bitcoin memiliki **network effect (efek jaringan)** yang sangat kuat: nilainya meningkat karena banyak orang dan layanan yang sudah menggunakannya. Sebuah *alt-coin* baru akan sulit bersaing jika tidak menawarkan inovasi yang signifikan, sama seperti sulitnya membuat jejaring sosial baru untuk menyaingi yang sudah ada.

<p align="center">
  <img src="images/books-01-grokking_bitcoin/figure_1.14.png" alt="gambar" width="500"/>
</p>

Perbandingan Efek Jaringan. Sisi kiri menunjukkan Internet (dengan logo Facebook, Google, Skype, Twitter) dan Jaringan Bitcoin yang ramai, dengan label "Banyak orang dan layanan". Sisi kanan menunjukkan "Wownet" dan "Wowcoin" yang sepi dan terisolasi, dengan label "Tidak ada orang atau layanan".

### **Ringkasan Bab 1**

* Bitcoin adalah uang global tanpa batas yang bisa digunakan siapa saja dengan koneksi internet.
* Jaringan komputer terdesentralisasi (*node*) memverifikasi dan mencatat semua pembayaran dalam sebuah buku besar publik yang disebut *blockchain*.
* Sebuah pembayaran diproses melalui 4 langkah: transaksi dibuat, diverifikasi oleh jaringan, ditambahkan ke *blockchain*, dan dompet penerima diberi notifikasi.
* Bitcoin mencoba menyelesaikan masalah inflasi, batas negara, eksklusi keuangan, dan privasi melalui pasokan terbatas, desentralisasi, dan sifatnya yang global.
* Selain Bitcoin, ada banyak *alt-coin* lain, tetapi Bitcoin memiliki efek jaringan yang paling kuat.

---

