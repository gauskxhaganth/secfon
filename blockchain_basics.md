# Blockchain Basic
## Bitcoin dan Blockchain
Bitcoin itu adalah mata uang digital pertama yang memungkinkan orang kirim uang langsung
ke orang lain (peer-to-peer) tanpa perantara seperti bank. Teknologi di baliknya disebut
Blockchain.

Analoginya, Bayangkan Blockchain itu seperti buku kas digital raksasa yang bisa
dilihat semua orang, tapi tidak bisa dihapus atau diubah seenaknya. Setiap transaksi
dicatat dalam sebuah "blok" dan disambungkan ke blok sebelumnya, membentuk rantai
(makanya disebut block-chain).

Kenapa Penting?: Karena tidak ada satu pihak pun (misalnya pemerintah atau bank) yang
mengontrolnya, transaksi jadi tahan sensor dan lebih aman. Bitcoin sering disebut
"emas digital" karena jumlahnya terbatas (langka seperti emas) dan dianggap sebagai
penyimpan nilai yang baik.

---

## Ethereum dan Smart Contract\
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

