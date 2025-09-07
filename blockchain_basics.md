# Blockchain Basic
## Bitcoin dan Blockchain
Bitcoin itu adalah mata uang digital pertama yang memungkinkan orang kirim uang langsung
ke orang lain (peer-to-peer) tanpa perantara seperti bank. Teknologi di baliknya disebut
Blockchain.

Bayangkan Blockchain itu seperti buku kas digital raksasa yang bisa
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
Kita tidak hanya bisa menggunakannya untuk transaksi, tapi juga bisa "meng-install"
berbagai macam aplikasi di atas teknologinya.

* Aplikasi-aplikasi inilah yang dijalankan oleh Smart Contract (Kontrak Pintar).
	Nah Smart Contract adalah program komputer sederhana yang berjalan di atas
	blockchain. Logikanya seperti: "JIKA kondisi A terpenuhi, MAKA otomatis lakukan
	aksi B (kalo programmer pasti tau, ini semacam if-else statement salah satu bagian
	kecil dari suatu program)". Perjanjian ini berjalan sendiri tanpa perlu perantara.
	
		Contoh: JIKA kita transfer 1 ETH (mata uang Ethereum) ke alamat A, MAKA sebuah aset
		digital otomatis akan terkirim ke alamatmu. Semua terjadi otomatis, tanpa perlu campur
		tangan manusia.
	
* Kemampuan menjalankan Smart Contract inilah yang jadi pembeda utama antara Ethereum dan Bitcoin.

---

## Masalah Oracle (The Oracle Problem)
Ada satu kelemahan besar dari Smart Contract yaitu mereka itu "buta" dan "tuli" terhadap dunia
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
	
		On-chain = semua data dan aktivitas yang langsung tercatat di blockchain.
		Off-chain = semua data dan aktivitas yang terjadi di luar blockchain.
		

---

## Chainlink & Solusi Skalabilitas (Layer 2)	
Chainlink adalah salah satu jaringan Oracle terdesentralisasi yang paling populer.
"Terdesentralisasi" artinya datanya tidak diambil dari satu sumber saja, melainkan dari
banyak sumber agar lebih akurat dan tidak mudah dimanipulasi. Chainlink juga bisa bekerja
di blockchain mana saja (blockchain agnostic).

Pengertian mengenai Layer 2 (L2) itu Bayangkan blockchain utama (seperti Ethereum) itu adalah
jalan raya utama (disebut Layer 1). Kalau terlalu banyak mobil (transaksi), jalanan itu bakal
macet dan mahal (biaya transaksi/gas fee jadi tinggi). Layer 2 adalah solusi untuk masalah ini.

	* Analogi: L2 itu seperti membangun "jalan tol" di samping jalan raya utama. Sebagian
	besar transaksi diproses di jalan tol (L2) yang lebih cepat dan murah, lalu hasil akhirnya
	(harus melalui gate pembayaran tol final buat gabung lagi ke jalan raya) dilaporkan secara
	berkala ke jalan raya utama (L1).

	* Contoh L2: Optimism, Arbitrum, ZKsync. (buat sekarang gausah pusing2 dulu terkail detail teknis).

---

## Rangkuman Istilah Penting

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
Ini adalah cara paling gampang untuk membedakannya dengan yang sudah kita kenal:
* Web1 (Era 90-an): Read-Only. Internet isinya situs statis. Kita cuma bisa baca, tidak bisa
	banyak berinteraksi.
* Web2 (Era 2000-an - sekarang): Read-Write. Kita bisa berinteraksi, membuat konten, dan
	menggunakan aplikasi (Sosmed, E-commerce). TAPI, semua data dan platform dikontrol oleh
	perusahaan besar (Google, Meta, Amazon). Kita adalah produknya.
* Web3 (Era Baru): Read-Write-Own. Kita bisa berinteraksi seperti di Web2, TAPI Kita juga bisa
	memiliki sebagian dari aplikasi atau platform yang Kita gunakan. Semuanya berjalan di
	jaringan terdesentralisasi (blockchain), bukan server milik satu perusahaan. Ini tentang
	kepemilikan pengguna (ownership economy).
	
Intinya, Web3 mengembalikan kontrol dan kepemilikan data ke tangan pengguna, bukan lagi terpusat
di perusahaan raksasa.

---

## Inti dari Blockchain dan Smart Contract
Hampir semua hal dalam hidup kita melibatkan "perjanjian" atau "janji". Beli pulsa, bayar
listrik, servis motor—semuanya adalah bentuk perjanjian. Kita bayar, dan Kita berharap pihak
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
	
		DEX = tempat tukar-menukar crypto di blockchain, tanpa perusahaan pusat. Semua diatur otomatis
		pakai smart contract.
	
## Rangkuman Singkat
* Perjanjian Tradisional: Butuh percaya pada satu pihak terpusat (perusahaan, bank, pemerintah).
	Risikonya, kepercayaan itu bisa dikhianati.
* Smart Contract: Tidak perlu percaya. Kita hanya perlu yakin pada kode matematika yang transparan,
	tidak bisa diubah, dan berjalan otomatis.
Smart Contract adalah solusi untuk meminimalkan ketergantungan kita pada sistem berbasis
kepercayaan yang sudah berkali-kali gagal dalam sejarah.

---

## Cara Kerjanya Smart Contract si "Janji yang Tidak Bisa Diingkari"
Secara sederhana, Smart Contract itu:

1. Mengubah sebuah "janji" atau perjanjian menjadi barisan kode.
2. Kode tersebut di-deploy (diletakkan) di atas blockchain.
3. Setelah di-deploy, kode itu tidak bisa diubah atau dihapus oleh siapapun.
4. Kode itu akan berjalan/dieksekusi secara otomatis oleh jaringan komputer terdesentralisasi
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
	
Sebagai developer atau user di dunia Web3, sangat penting untuk bisa membedakan mana
proyek yang benar-benar membangun sistem terdesentralisasi yang adil, dan mana yang hanya
"berkedok" Web3 untuk mencari keuntungan.

## Rangkuman Singkat

1. Hampir semua masalah dalam perjanjian konvensional bersumber dari kebutuhan akan kepercayaan
	pada pihak ketiga.
2. Smart Contract memecahkan masalah ini dengan menyediakan sistem perjanjian yang transparan,
	adil, dan tidak bisa diubah (immutable).
3. Ini memungkinkan kita membuat "janji yang tidak bisa diingkari" tanpa perlu bergantung pada
	reputasi atau niat baik orang lain.
4. Selalu waspada terhadap platform yang mengaku Web3 tapi praktiknya terpusat, seperti kasus
	**FTX**.

---

## RECAP
### 🚀 Pendahuluan

Teknologi **blockchain** telah mengubah cara transaksi dan perjanjian digital.
💰 **Bitcoin** adalah protokol pertama yang mempopulerkan blockchain, memungkinkan transaksi tanpa perantara.
⚙️ Berdasarkan pondasi ini, **Ethereum** dan platform smart contract lainnya mengembangkan teknologi dengan memungkinkan pembuatan **smart contract** dan **dApps**.
🔗 Platform ini berinteraksi dengan dunia nyata melalui jaringan terdesentralisasi seperti **Chainlink**, yang memperluas kemampuan blockchain.
💡 Hal ini menantang sistem keuangan tradisional dengan menawarkan cara baru mengelola dan memindahkan kekayaan.

### 🪙 Bitcoin dan Ethereum

* **Bitcoin**
  🔑 Memperkenalkan konsep mata uang digital **terdesentralisasi**.
  💎 Berfungsi sebagai **store of value** dan memungkinkan transaksi **peer-to-peer** tanpa otoritas pusat.
  🛡️ Desentralisasi membuatnya tahan sensor dan kegagalan terpusat.

* **Ethereum**
  🧾 Mengembangkan teknologi Bitcoin dengan **smart contract**.
  🤖 Smart contract = kontrak otomatis dengan syarat & ketentuan ditulis jelas dalam kode.
  🙅 Menghilangkan kebutuhan perantara, meminimalkan risiko trust.
  📱 Memungkinkan pembuatan **dApps** yang bisa berinteraksi dengan blockchain + data dunia nyata lewat jaringan terdesentralisasi.

### 🔗 Chainlink

**Chainlink** = jaringan terdesentralisasi yang memungkinkan **hybrid smart contract**.
⚖️ Menggabungkan logika **on-chain** + data/komputasi **off-chain**, sambil tetap terdesentralisasi.

### 🌟 Fitur Utama & Manfaat

✅ **Desentralisasi** → jaringan node menghilangkan perantara pusat.
👀 **Transparansi & Fleksibilitas** → transaksi & kontrak terbuka untuk semua, dengan **privasi** lewat pseudo-anonimitas.
⚡ **Kecepatan & Efisiensi** → transaksi instan, tanpa lembaga kliring.
🔒 **Keamanan & Immutability** → smart contract tidak bisa diubah; blockchain sulit diretas.
🤝 **Mengurangi Risiko Pihak Ketiga** → kontrak berjalan sesuai kode, tanpa campur tangan manusia/fraud.

### 📝 Kesimpulan

🌍 Blockchain telah merevolusi transaksi & perjanjian digital:

* 💰 Bitcoin → mata uang digital terdesentralisasi.
* ⚙️ Ethereum → smart contract & dApps.
* 🔗 Chainlink → hybrid smart contract dengan data dunia nyata.

🚀 Inovasi ini menantang keuangan tradisional dengan solusi **aman, transparan, efisien**, membuka era baru perjanjian yang minim kebutuhan kepercayaan.

🧑‍💻 **Tes Diri**

📕 Jelaskan singkat apa itu **Bitcoin, Ethereum, Chainlink**.

📕 Sebutkan keunggulan utama **smart contract** dibanding sistem keuangan tradisional.

---

## Fitur-Fitur Utama Smart Contract
Smart Contract punya beberapa sifat dasar yang membuatnya jauh berbeda dari
perjanjian biasa.

**1. Desentralisasi (Tidak Terpusat) decentralization**
Smart Contract tidak berjalan di satu server milik satu perusahaan. Sebaliknya, ia
berjalan di jaringan blockchain yang dikelola oleh ribuan komputer di seluruh dunia
(yang disebut node). Karena dijalankan secara gotong royong oleh banyak pihak, tidak
ada satu "bos" pun yang bisa mengendalikannya.
	
	* Analogi: Bayangkan sebuah aplikasi. Di Web2, aplikasi itu berjalan di server Google.
	Jika server Google down, aplikasinya mati. Di Web3, aplikasi (Smart Contract) itu
	berjalan di ribuan komputer sekaligus. Jika satu komputer mati, 999 lainnya tetap
	menjalankannya. Sistemnya jadi jauh lebih kuat.
	
**2. Transparansi & Fleksibilitas**
Semua aturan dalam Smart Contract dan semua transaksi yang terjadi di blockchain bersifat
terbuka dan bisa dilihat oleh siapa saja. Tidak ada lagi "perjanjian di bawah meja" atau
syarat dan ketentuan yang disembunyikan.
	
	* Apakah ini mengorbankan privasi? Tidak juga. Walaupun transaksinya transparan, identitasmu
	tidak terhubung langsung. Kamu dikenal melalui alamat dompet digitalmu (misalnya: 0x123...abc),
	bukan nama aslimu. Ini disebut pseudo-anonim (samar-samar anonim).
	
**3. Kecepatan dan Efisiensi**⚡
Dibandingkan sistem perbankan tradisional, transaksi menggunakan Smart Contract jauh
lebih cepat.
	
	* Contoh: Transfer uang ke luar negeri via bank bisa memakan waktu berhari-hari. Dengan
	blockchain, transaksi yang sama bisa selesai dalam hitungan detik atau menit. Ini membuat
	semua interaksi jadi jauh lebih efisien.
	
**4. Keamanan dan Immutability (Tidak Bisa Diubah)**
Ini adalah fitur paling penting.

	* Immutable: Sekali sebuah Smart Contract di-deploy (diterbitkan) di blockchain, aturannya
	tidak bisa diubah, dihapus, atau diedit oleh siapapun. Aturan itu terkunci selamanya. Ini
	seperti mengukir perjanjian di atas batu, bukan menuliskannya di papan tulis yang bisa dihapus.
	
	* Aman dari Hacker: Untuk meretas server terpusat (Web2), hacker hanya perlu membobol satu
	target. Untuk meretas blockchain, hacker harus mengambil alih lebih dari setengah dari
	ribuan komputer (node) di jaringan secara bersamaan. Ini secara praktis mustahil dilakukan.
	
	* Data Tahan Banting: Di sistem biasa, jika komputermu dan backup-nya rusak, datamu hilang.
	Di blockchain, datamu disalin ke ribuan node. Bahkan jika ratusan node hancur, datamu akan
	tetap aman karena salinannya masih ada di mana-mana.
	
**5. Menghilangkan Risiko Pihak Ketiga (Counterparty Risk)**
Karena Smart Contract berjalan otomatis sesuai kode yang tidak bisa diubah, kamu tidak perlu
lagi percaya bahwa pihak lain akan menepati janjinya. Kode yang akan memaksanya.

	* Analogi: Smart Contract itu seperti vending machine. Kamu masukkan uang (memenuhi syarat),
	mesin itu pasti akan mengeluarkan minuman (melaksanakan kewajibannya). Mesin tidak punya
	niat jahat atau keinginan untuk menipumu; ia hanya menjalankan programnya.
	

Oke, sekarang kita akan bahas fitur-fitur keren dari Smart Contract dan apa saja kegunaannya
di dunia nyata. Ini akan menjelaskan kenapa teknologi ini begitu revolusioner.

Fitur-Fitur Utama Smart Contract
Smart Contract punya beberapa sifat dasar yang membuatnya jauh berbeda dari perjanjian biasa.

1. Desentralisasi (Tidak Terpusat) decentralization
Smart Contract tidak berjalan di satu server milik satu perusahaan. Sebaliknya, ia berjalan
di jaringan blockchain yang dikelola oleh ribuan komputer di seluruh dunia (yang disebut node).
Karena dijalankan secara gotong royong oleh banyak pihak, tidak ada satu "bos" pun yang bisa
mengendalikannya.

Analogi: Bayangkan sebuah aplikasi. Di Web2, aplikasi itu berjalan di server Google. Jika
server Google down, aplikasinya mati. Di Web3, aplikasi (Smart Contract) itu berjalan di ribuan
komputer sekaligus. Jika satu komputer mati, 999 lainnya tetap menjalankannya. Sistemnya jadi
jauh lebih kuat.

2. Transparansi & Fleksibilitas 🧐
Semua aturan dalam Smart Contract dan semua transaksi yang terjadi di blockchain bersifat terbuka
dan bisa dilihat oleh siapa saja. Tidak ada lagi "perjanjian di bawah meja" atau syarat dan
ketentuan yang disembunyikan.

Apakah ini mengorbankan privasi? Tidak juga. Walaupun transaksinya transparan, identitasmu tidak
terhubung langsung. Kamu dikenal melalui alamat dompet digitalmu (misalnya: 0x123...abc), bukan
nama aslimu. Ini disebut pseudo-anonim (samar-samar anonim).

3. Kecepatan dan Efisiensi ⚡
Dibandingkan sistem perbankan tradisional, transaksi menggunakan Smart Contract jauh lebih cepat.

Contoh: Transfer uang ke luar negeri via bank bisa memakan waktu berhari-hari. Dengan blockchain,
transaksi yang sama bisa selesai dalam hitungan detik atau menit. Ini membuat semua interaksi
jadi jauh lebih efisien.

4. Keamanan dan Immutability (Tidak Bisa Diubah) 🔐

Ini adalah fitur paling penting.

Immutable: Sekali sebuah Smart Contract di-deploy (diterbitkan) di blockchain, aturannya tidak
bisa diubah, dihapus, atau diedit oleh siapapun. Aturan itu terkunci selamanya. Ini seperti
mengukir perjanjian di atas batu, bukan menuliskannya di papan tulis yang bisa dihapus.

Aman dari Hacker: Untuk meretas server terpusat (Web2), hacker hanya perlu membobol satu target.
Untuk meretas blockchain, hacker harus mengambil alih lebih dari setengah dari ribuan komputer
(node) di jaringan secara bersamaan. Ini secara praktis mustahil dilakukan.

Data Tahan Banting: Di sistem biasa, jika komputermu dan backup-nya rusak, datamu hilang.
Di blockchain, datamu disalin ke ribuan node. Bahkan jika ratusan node hancur, datamu akan
tetap aman karena salinannya masih ada di mana-mana.

5. Menghilangkan Risiko Pihak Ketiga (Counterparty Risk) 👍
Karena Smart Contract berjalan otomatis sesuai kode yang tidak bisa diubah, kamu tidak perlu lagi
percaya bahwa pihak lain akan menepati janjinya. Kode yang akan memaksanya.

Analogi: Smart Contract itu seperti vending machine. Kamu masukkan uang (memenuhi syarat), mesin
itu pasti akan mengeluarkan minuman (melaksanakan kewajibannya). Mesin tidak punya niat jahat
atau keinginan untuk menipumu; ia hanya menjalankan programnya.

## Contoh Penerapan Smart Contract
Teknologi ini telah melahirkan industri-industri baru yang luar biasa. Berikut beberapa contohnya:

**1. DeFi (Decentralized Finance)**
Ini adalah layanan keuangan (meminjam, menabung, trading) yang berjalan di atas Smart Contract,
tanpa perantara seperti bank. Siapapun bisa mengakses layanan keuangan global secara adil dan
transparan, langsung dari dompet digital mereka.

**2. DAO (Decentralized Autonomous Organization)**
Ini adalah sebuah organisasi atau perusahaan yang dijalankan sepenuhnya oleh kode (Smart Contract)
dan keputusan komunitas melalui voting. Tidak ada CEO atau hierarki tradisional. Semua aturan
dan pengelolaan dana diatur secara transparan oleh kode.

**3. NFT (Non-Fungible Token)**
NFT adalah sertifikat kepemilikan digital yang unik untuk sebuah aset (bisa berupa karya seni,
item game, musik, dll) yang tercatat di blockchain. Smart Contract digunakan untuk mengatur
kepemilikan, penjualan, dan royalti dari NFT tersebut secara otomatis.

	* Analogi: NFT itu seperti sertifikat keaslian digital untuk sebuah file. Siapapun bisa
	mengunduh gambar Monalisa, tapi hanya museum Louvre yang punya lukisan aslinya. NFT memberikan
	bukti kepemilikan "asli" versi digital.

## Melakukan Transaksi Pertamamu

Kamu sudah mendapatkan pemahaman tingkat tinggi tentang smart contract dan penerapannya. Sekarang
saatnya masuk ke aspek praktis. Pada bagian berikutnya, kami akan memandu kamu untuk menyiapkan
sebuah wallet dan melakukan transaksi pertamamu. Mari kita menyelami dunia baru ini.

---

