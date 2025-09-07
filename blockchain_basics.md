# Blockchain Basic
## Bitcoin dan Blockchain
Bitcoin itu adalah mata uang digital pertama yang memungkinkan orang kirim uang langsung
ke orang lain (peer-to-peer) tanpa perantara seperti bank. Teknologi di baliknya disebut
Blockchain.

Analoginya, Bayangkan Blockchain itu seperti buku kas digital raksasa yang bisa
dilihat semua orang, tapi tidak bisa dihapus atau diubah seenaknya. Setiap transaksi
dicatat dalam sebuah "blok" dan disambungkan ke blok sebelumnya, membentuk rantai
(makanya disebut block-chain).

Kenapa Penting? Karena tidak ada satu pihak pun (misalnya pemerintah atau bank) yang
mengontrolnya, transaksi jadi tahan sensor dan lebih aman. Bitcoin sering disebut
"emas digital" karena jumlahnya terbatas (langka seperti emas) dan dianggap sebagai
penyimpan nilai yang baik.

---

## Ethereum dan Smart Contract
Beberapa tahun setelah Bitcoin, muncullah Ethereum. Kalau Bitcoin itu ibarat kalkulator
yang fungsinya spesifik untuk transaksi keuangan, maka Ethereum itu ibarat smartphone.
Kamu tidak hanya bisa menggunakannya untuk transaksi, tapi juga bisa "meng-install"
berbagai macam aplikasi di atas teknologinya.

* Aplikasi-aplikasi inilah yang dijalankan oleh Smart Contract (Kontrak Pintar).
	Apa itu Smart Contract?: Ini adalah program komputer sederhana yang berjalan di atas
	blockchain. Logikanya seperti ini: "JIKA kondisi A terpenuhi, MAKA otomatis lakukan
	aksi B". Perjanjian ini berjalan sendiri tanpa perlu perantara.
	
* Contoh: JIKA kamu transfer 1 ETH (mata uang Ethereum) ke alamat A, MAKA sebuah aset
	digital otomatis akan terkirim ke alamatmu. Semua terjadi otomatis, tanpa perlu campur
	tangan manusia.
	
* Perbedaan Utama: Kemampuan menjalankan Smart Contract inilah yang jadi pembeda utama
	antara Ethereum dan Bitcoin.

---

## Masalah Oracle (The Oracle Problem)
Ada satu kelemahan besar dari Smart Contract: mereka itu "buta" dan "tuli" terhadap dunia
luar. Mereka hanya tahu apa yang terjadi di dalam blockchain itu sendiri.

*  Masalahnya: Bagaimana sebuah smart contract untuk asuransi pertanian bisa tahu apakah
	di dunia nyata benar-benar terjadi kekeringan? Jawabannya: tidak bisa. Inilah yang
	disebut The Oracle Problem.

* Solusinya: Di sinilah Oracle berperan. Oracle adalah layanan pihak ketiga yang bertindak
	sebagai jembatan data antara dunia nyata dan blockchain. Oracle menyediakan data eksternal
	(seperti data cuaca, harga saham, hasil pertandingan bola) ke dalam smart contract.

* Hybrid Smart Contract: Ketika sebuah smart contract menggunakan data dari Oracle, ia
	disebut Hybrid Smart Contract (gabungan logika on-chain di blockchain dan data off-chain 
	dari dunia luar).

---

## Chainlink & Solusi Skalabilitas (Layer 2)	
Chainlink: Ini adalah salah satu jaringan Oracle terdesentralisasi yang paling populer.
"Terdesentralisasi" artinya datanya tidak diambil dari satu sumber saja, melainkan dari
banyak sumber agar lebih akurat dan tidak mudah dimanipulasi. Chainlink juga bisa bekerja
di blockchain mana saja (blockchain agnostic).

Layer 2 (L2): Bayangkan blockchain utama (seperti Ethereum) itu adalah jalan raya utama
(disebut Layer 1). Kalau terlalu banyak mobil (transaksi), jalanan itu bakal macet dan mahal
(biaya transaksi/gas fee jadi tinggi). Layer 2 adalah solusi untuk masalah ini.

	* Analogi: L2 itu seperti membangun "jalan tol" di samping jalan raya utama. Sebagian
	besar transaksi diproses di jalan tol (L2) yang lebih cepat dan murah, lalu hasil akhirnya
	dilaporkan secara berkala ke jalan raya utama (L1).

	* Contoh L2: Optimism, Arbitrum, ZKsync. (Tidak perlu pusing soal detail teknisnya sekarang).

---

## Rangkuman Istilah Penting
Ini kamus singkatnya versi gampang:

* Blockchain: Buku kas digital yang tersebar dan tidak bisa diubah.
* Smart Contract: Kode program "Jika-Maka" yang berjalan otomatis di blockchain.
* Oracle: Jembatan atau kurir data dari dunia nyata ke blockchain.
* Dapp (Decentralized Application): Aplikasi (seperti web atau mobile app) yang backend-nya
	bukan di server perusahaan, tapi berjalan di atas blockchain menggunakan Smart Contract.
* Layer 2 (L2): "Jalan tol" untuk membuat blockchain lebih cepat dan murah.
* Ethereum/EVM: Ethereum adalah nama blockchain-nya. EVM (Ethereum Virtual Machine) adalah
	"mesin" atau lingkungan komputasi di dalam Ethereum yang tugasnya menjalankan kode
	Smart Contract.

---

## Apa itu Web3?
Ini adalah cara paling gampang untuk membedakannya dengan yang sudah kamu kenal:
* Web1 (Era 90-an): Read-Only. Internet isinya situs statis. Kamu cuma bisa baca, tidak bisa
	banyak berinteraksi.
* Web2 (Era 2000-an - sekarang): Read-Write. Kamu bisa berinteraksi, membuat konten, dan
	menggunakan aplikasi (Sosmed, E-commerce). TAPI, semua data dan platform dikontrol oleh
	perusahaan besar (Google, Meta, Amazon). Kita adalah produknya.
* Web3 (Era Baru): Read-Write-Own. Kamu bisa berinteraksi seperti di Web2, TAPI kamu juga bisa
	memiliki sebagian dari aplikasi atau platform yang kamu gunakan. Semuanya berjalan di
	jaringan terdesentralisasi (blockchain), bukan server milik satu perusahaan. Ini tentang
	kepemilikan pengguna (ownership economy).
	
Intinya, Web3 mengembalikan kontrol dan kepemilikan data ke tangan pengguna, bukan lagi terpusat
di perusahaan raksasa.

---

## Inti dari Blockchain dan Smart Contract
Hampir semua hal dalam hidup kita melibatkan "perjanjian" atau "janji". Beli pulsa, bayar
listrik, servis motor—semuanya adalah bentuk perjanjian. Kamu bayar, dan kamu berharap pihak
lain menepati janjinya (memberi pulsa, listrik, atau servis yang benar).

Masalahnya, perjanjian tradisional ini sangat bergantung pada rasa percaya. Dan seperti yang
kita tahu, rasa percaya itu bisa disalahgunakan.

### Masalah dengan Perjanjian Tradisional (Berbasis Kepercayaan)

Mari kita lihat beberapa contoh di dunia nyata di mana sistem berbasis kepercayaan ini gagal
total, dan bagaimana Smart Contract bisa mengatasinya.

#### 1. Kepercayaan Konsumen: Kasus Game Monopoli McDonald's
* Masalah: Dulu di tahun 80-90an, McDonald's punya undian berhadiah besar lewat game Monopoli.
	Janjinya, semua pelanggan punya kesempatan yang sama untuk menang.

* Kenyataan: Ternyata, game itu dicurangi oleh orang dalam. Hadiah-hadiah utama sudah diatur
	untuk orang-orang tertentu. Janji McDonald's kepada jutaan pelanggannya diingkari.

* Solusi dengan Smart Contract: Coba bayangkan jika undian itu dijalankan di atas blockchain
	pakai Smart Contract. Aturan mainnya (misalnya, tiket mana yang menang) akan ditulis dalam
	kode yang transparan, tidak bisa diubah, dan dieksekusi otomatis. Kecurangan oleh orang dalam
	menjadi mustahil dilakukan.

#### 2. Kepercayaan pada Bank: Krisis Keuangan
* Masalah: Bank berjanji untuk menjaga uang kita dengan aman. Tapi sejarah membuktikan
	sebaliknya. Saat krisis ekonomi parah (Great Depression di AS), banyak bank bangkrut dan uang
	nasabah hilang begitu saja.

* Solusi dengan Smart Contract: Di sistem keuangan berbasis blockchain (DeFi - Decentralized Finance),
	semua transaksi dan kondisi keuangan bisa dibuat transparan. Bisa dibuat aturan otomatis
	yang mencegah sebuah institusi meminjamkan uang lebih banyak dari aset yang mereka miliki.
	Tidak ada lagi rahasia "dapur" yang ditutup-tutupi.
	
#### 3. Akses Pasar Keuangan: Kasus Robinhood & GameStop
* Masalah: Pada tahun 2021, aplikasi trading saham Robinhood tiba-tiba melarang penggunanya
	untuk membeli saham tertentu (GameStop, $GME) yang sedang viral. Ini menunjukkan bahwa platform
	terpusat punya kuasa penuh untuk mengubah aturan main seenaknya demi kepentingan mereka.

* Solusi dengan Smart Contract: Bandingkan dengan platform Decentralized Exchange (DEX)
	seperti Uniswap yang berjalan di atas Smart Contract. Di sana, tidak ada satu pun pihak
	yang bisa menghentikan atau melarang perdagangan. Aturannya sama untuk semua orang,
	menciptakan pasar yang lebih adil dan terbuka.
	
## Rangkuman Singkat
* Perjanjian Tradisional: Butuh percaya pada satu pihak terpusat (perusahaan, bank, pemerintah).
	Risikonya, kepercayaan itu bisa dikhianati.
* Smart Contract: Tidak perlu percaya. Kamu hanya perlu yakin pada kode matematika yang transparan,
	tidak bisa diubah, dan berjalan otomatis.
Smart Contract adalah solusi untuk meminimalkan ketergantungan kita pada sistem berbasis
kepercayaan yang sudah berkali-kali gagal dalam sejarah.

---

## Cara Kerjanya: "Janji yang Tidak Bisa Diingkari"
1. Secara sederhana, Smart Contract itu:
2. Mengubah sebuah "janji" atau perjanjian menjadi barisan kode.
3. Kode tersebut di-deploy (diletakkan) di atas blockchain.
4. Setelah di-deploy, kode itu tidak bisa diubah atau dihapus oleh siapapun.
5. Kode itu akan berjalan/dieksekusi secara otomatis oleh jaringan komputer terdesentralisasi
	ketika syaratnya terpenuhi.

Karena sifatnya yang seperti ini, perjanjian yang dibuat di atas Smart Contract sering disebut
"unbreakable promises" atau janji yang tidak bisa diingkari.

---

> Peringatan Penting: Tidak Semuanya Sama!

**HATI-HATI!** Seiring populernya Web3, banyak platform yang pura-pura terdesentralisasi
padahal aslinya tidak. Mereka hanya menggunakan istilah "crypto" atau "blockchain" untuk
marketing.

* Contoh Paling Fatal: FTX. Platform ini mempromosikan diri sebagai bursa kripto Web3 yang
	canggih. Kenyataannya, di belakang layar, mereka adalah perusahaan Web2 yang sangat terpusat.
	Mereka tidak menggunakan Smart Contract untuk mengelola dana nasabah. Hasilnya? Dana nasabah
	disalahgunakan oleh segelintir orang di dalamnya.
	
Sebagai developer atau pengguna di dunia Web3, sangat penting untuk bisa membedakan mana
proyek yang benar-benar membangun sistem terdesentralisasi yang adil, dan mana yang hanya
"berkedok" Web3 untuk mencari keuntungan.

1. Hampir semua masalah dalam perjanjian konvensional bersumber dari kebutuhan akan kepercayaan
	pada pihak ketiga.
2. Smart Contract memecahkan masalah ini dengan menyediakan sistem perjanjian yang transparan,
	adil, dan tidak bisa diubah (immutable).
3. Ini memungkinkan kita membuat "janji yang tidak bisa diingkari" tanpa perlu bergantung pada
	reputasi atau niat baik orang lain.
4. Selalu waspada terhadap platform yang mengaku Web3 tapi praktiknya terpusat, seperti kasus
	**FTX**.

---

