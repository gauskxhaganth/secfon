# Bab 1
## Apa Itu Uang dan Sejarah Singkatnya?

Bab ini mungkin tampak seperti pengantar filosofis, tetapi bagi seorang auditor keamanan, bab ini adalah fondasi terpenting. Sebelum kita bisa mengamankan sebuah sistem finansial berbasis *blockchain*, kita harus memahami masalah fundamental yang coba dipecahkan oleh teknologi ini. Bab ini tidak hanya membahas "apa itu uang," tetapi "mengapa uang itu ada" dan bagaimana evolusinya membentuk kebutuhan akan sistem seperti *Bitcoin* dan *Ethereum*.

### Pengantar: Konteks untuk Auditor

Penulis memulai dengan menegaskan bahwa meskipun ini adalah buku tentang Solidity, pemahaman tentang uang sangatlah esensial. *Smart contracts* yang akan Kita audit nantinya sering kali mengelola aset digital yang berfungsi sebagai uang. Kesalahan dalam logika kontrak dapat mengakibatkan kerugian finansial yang nyata. Oleh karena itu, memahami properti uang, sejarah kepercayaannya, dan kelemahannya akan memberi Kita perspektif yang lebih tajam dalam mengidentifikasi potensi risiko dalam sebuah *smart contract*.

Bab ini menjawab pertanyaan-pertanyaan berikut:
* Apa yang membuat sesuatu berharga dan dapat berfungsi sebagai uang?
* Bagaimana masyarakat secara historis menyelesaikan masalah koordinasi dalam pertukaran nilai?
* Bagaimana *cryptocurrency* dan *smart contracts* membangun pola historis ini sambil memperkenalkan kapabilitas baru?

### Apa Itu Uang?

Penulis tidak mendefinisikan uang secara kaku, melainkan menjelajahinya dari berbagai sudut pandang:
1.  **Sebagai Medium Pertukaran:** Alat untuk memfasilitasi perdagangan barang dan jasa.
2.  **Sebagai Representasi Energi:** Uang dilihat sebagai bentuk fisik dari waktu dan energi yang telah kita curahkan, yang kemudian dapat ditukarkan dengan energi orang lain (misalnya, membeli mobil yang dibuat oleh orang lain).
3.  **Sebagai Bahasa dan Teknologi:** Ini adalah konsep inti bab ini. Uang adalah **bahasa universal** untuk mengkomunikasikan nilai. Saat Kita mengatakan "pisau ini harganya $50," Kita dan penjual menggunakan bahasa yang sama untuk menyetujui nilai dari pisau tersebut. Sistem ekonomi global kemudian dilihat sebagai sebuah **protokol** yang dibangun di atas bahasa ini.

#### Uang sebagai Teknologi Kontrak

Sebagai seorang calon auditor, ini adalah poin krusial. Penulis menggambarkan uang itu sendiri sebagai sebuah kontrak sosial yang implisit:
* **Kontrak dalam Komunitas:** Kesepakatan di antara sekelompok orang untuk menggunakan objek tertentu (misalnya, Dolar AS) sebagai alat transaksi.
* **Kontrak antar Komunitas:** Ketika dua komunitas dengan "uang" yang berbeda ingin berdagang, mereka memerlukan alat transaksional standar yang disepakati bersama, seperti Dolar AS untuk perdagangan internasional saat ini.

### Tiga Properti Inti Uang

Untuk dapat berfungsi secara efektif, teknologi "uang" harus memiliki tiga properti utama. Setiap properti ini memiliki sub-properti yang menentukan kualitasnya. Memahami ini akan membantu Kita mengevaluasi aset digital di masa depan.

#### 1. Medium of Exchange (Alat Tukar)

Ini adalah fungsi paling dasar: sebuah alat perantara untuk memfasilitasi pertukaran. Agar bisa diandalkan, alat tukar harus memiliki sifat-sifat berikut:

* **Durability (Daya Tahan):** Harus tahan terhadap kerusakan fisik.
* **Transportability (Mudah Dibawa):** Mudah untuk dipindahkan baik dari segi kecepatan maupun berat.
* **Divisibility (Dapat Dibagi):** Dapat dipecah menjadi unit-unit yang lebih kecil tanpa kehilangan nilai.
* **Fungibility (Dapat Dipertukarkan):** Setiap unitnya harus identik dan memiliki nilai yang sama. Satu lembar $100 sama nilainya dengan lembar $100 lainnya.
* **Non-counterfeitability (Sulit Dipalsukan):** Harus sulit untuk ditiru atau dipalsukan.
* **Scarcity (Kelangkaan):** Pasokannya harus terbatas untuk mempertahankan nilainya. Jika terlalu melimpah, nilainya akan turun.
* **Acceptability (Dapat Diterima):** Semakin banyak pihak yang mau menerimanya, semakin efektif fungsinya.

#### 2. Store of Value (Penyimpan Nilai)

Uang harus mampu mempertahankan daya belinya dari waktu ke waktu. Properti ini tidak hanya dimiliki oleh uang, tetapi juga aset lain seperti emas, properti, atau saham. Sifat penyimpan nilai yang baik berasal dari:

* **Stability (Stabilitas):** Permintaan yang stabil dan dapat diprediksi.
* **Predictability (Dapat Diprediksi):** Pasokan masa depan yang stabil atau menyusut.
* **Cultural and Societal Values (Nilai Kultural dan Sosial):** Persepsi nilai budaya yang melekat pada aset tersebut.
* **Liquidity (Likuiditas):** Kemudahan untuk mengubahnya kembali menjadi alat tukar (uang tunai) tanpa kehilangan nilai secara signifikan.
* **Portability and Transferability (Portabilitas dan Kemudahan Transfer):** Kemudahan memindahkan kepemilikan aset tersebut.

#### 3. Unit of Account (Satuan Hitung)

Uang harus berfungsi sebagai tolok ukur standar untuk menyatakan harga barang dan jasa. Misalnya, kita mengatakan "perjalanan ini harganya $10.000," bukan "perjalanan ini harganya empat ekor sapi." Agar efektif sebagai satuan hitung, nilainya harus **stabil** dan tidak volatil dalam jangka pendek. Inilah kelemahan utama *cryptocurrency* saat ini dibandingkan mata uang fiat.

> Penulis menyimpulkan bahwa **tidak ada bentuk uang yang sempurna saat ini** karena tidak ada yang dapat memenuhi semua properti tersebut secara ideal. Sering kali, memaksimalkan satu properti akan mengorbankan properti lainnya.

### Sejarah dan Evolusi Uang

Bagian ini melacak perjalanan uang dari sistem paling primitif hingga yang paling modern, menunjukkan bagaimana manusia secara bertahap membangun sistem kepercayaan dan kerja sama yang lebih kompleks.

#### 1. Barter

Sistem paling awal adalah barter: pertukaran langsung barang dan jasa tanpa perantara. Ini hanya efektif dalam komunitas kecil di mana semua orang saling kenal dan reputasi menjadi jaminan. Kelemahan utamanya adalah masalah **"double coincidence of wants" (kebetulan ganda keinginan)**, di mana kedua belah pihak harus menginginkan apa yang dimiliki oleh pihak lain. Sistem ini menjadi tidak praktis seiring dengan pertumbuhan dan kompleksitas ekonomi.

#### 2. Primitive Money (Uang Primitif)

Untuk mengatasi keterbatasan barter, masyarakat mulai menggunakan "uang primitif". Bentuknya sangat bervariasi tergantung pada budaya dan lingkungan geografis, tetapi semuanya memiliki kesamaan: benda-benda tersebut memiliki nilai intrinsik atau simbolis yang disepakati oleh komunitas.

Penulis memberikan banyak contoh untuk mengilustrasikan satu poin penting: **meskipun bentuk fisiknya berbeda, dasar psikologis dan properti yang harus dipenuhi tetap sama.**

* **Shells (Kerang):** Seperti kerang *cowrie* yang digunakan di Afrika dan Asia. Selain sebagai uang, kerang juga memiliki nilai budaya dan spiritual yang signifikan.
* **Wampum Belts (Sabuk Wampum):** Digunakan oleh suku-suku asli Amerika tidak hanya sebagai uang, tetapi juga sebagai catatan fisik perjanjian, hukum, dan sejarah.
* **Cattle (Ternak):** Digunakan di banyak budaya agraris sebagai simbol kekayaan dan status karena menyediakan sumber daya penting.
* **Whale Teeth (Gigi Ikan Paus):** Di komunitas pesisir seperti Fiji, gigi ikan paus melambangkan status, keberanian, dan hubungan sosial.
* **Grain (Biji-bijian), Salt (Garam), Tobacco (Tembakau), Tea Bricks (Bata Teh), Feathers (Bulu), dan Beads (Manik-manik):** Semua ini adalah contoh lain di mana benda-benda dari lingkungan sekitar diadopsi sebagai uang karena memenuhi properti dasar seperti daya tahan, kelangkaan, dan penerimaan budaya.

> **Poin Kunci untuk Auditor:** Uang pada dasarnya adalah sebuah **konstruk psikologis dan sosial**. Kepercayaan kolektif adalah yang memberinya nilai. Ini relevan ketika Kita menganalisis tokenomik atau mekanisme stabilitas sebuah *stablecoin*.

### Jenis Uang Modern

Evolusi berlanjut ke bentuk yang lebih canggih dan terstandarisasi.

* **Coins (Koin):** Diciptakan di Lydia kuno, koin menawarkan standardisasi, daya tahan, dan kemudahan pembagian yang lebih baik. Namun, koin juga memperkenalkan masalah baru: **pemalsuan dan *debasement* (penurunan nilai)**, di mana penguasa mencampur logam mulia dengan logam yang lebih murah.
* **Paper Money (Uang Kertas):** Berawal di Tiongkok sebagai tanda terima untuk simpanan koin. Ini memecahkan masalah portabilitas untuk transaksi besar. Di dunia Barat, Bank of Amsterdam menjadi pelopor perbankan modern dan secara tidak sengaja memperkenalkan ***fractional-reserve banking*** (perbankan cadangan fraksional), di mana bank hanya menyimpan sebagian kecil dari simpanan dan meminjamkan sisanya. Ini adalah dasar dari sistem keuangan modern.
* **Bretton Woods Conference:** Pada tahun 1944, sistem ini menetapkan Dolar AS sebagai mata uang cadangan dunia, yang dipatok ke emas. Mata uang negara lain kemudian dipatok ke Dolar AS. Sistem ini runtuh pada tahun 1971, mengakhiri era mata uang yang didukung logam dan memulai era **mata uang *fiat*** (uang yang nilainya didasarkan pada kepercayaan pada pemerintah yang menerbitkannya).

> Penulis kembali menekankan bahwa uang modern pun tidak lepas dari akar budayanya. Gambar pahlawan nasional, bangunan bersejarah, atau simbol negara pada uang kertas dan koin berfungsi untuk memperkuat identitas dan kebanggaan nasional, mirip dengan bagaimana uang primitif terjalin dengan budaya sukunya.

### Cryptocurrency

Ini adalah transisi ke bagian inti yang relevan dengan Solidity. Penulis memperkenalkan *cryptocurrency* sebagai evolusi berikutnya dari uang, yang kini sepenuhnya digital dan terdesentralisasi.

#### 1. Bitcoin

Diperkenalkan oleh Satoshi Nakamoto pada tahun 2008 sebagai "*peer-to-peer electronic cash system*". Penulis menguraikan properti moneter *Bitcoin*:
* **Distributed (Terdistribusi), Secure (Aman), Reliable (Dapat Diandalkan):** Jaringan tersebar di seluruh dunia, diamankan oleh mayoritas *node* yang jujur.
* **Peer-to-peer, Open (Terbuka), Public (Publik), Permissionless (Tanpa Izin), Borderless (Tanpa Batas), Censorship-resistant (Tahan Sensor), Neutral (Netral):** Ini adalah karakteristik fundamental yang membedakannya dari sistem keuangan tradisional.

**"Kebijakan Moneter" Bitcoin:**
* **Pasokan Tetap:** Hanya akan ada 21 juta *bitcoin*.
* **Jadwal Deflasi:** Emisi koin baru berkurang setengahnya kira-kira setiap empat tahun dalam sebuah peristiwa yang disebut ***halving***.
* **Dapat Diprediksi:** Tidak seperti bank sentral, kebijakan moneter *Bitcoin* bersifat algoritmik dan transparan.

Analisis *Bitcoin* dan *Ether* terhadap Tiga Properti Uang:
* **Medium of Exchange:** Sangat portabel dan tahan lama, tetapi skalabilitas yang rendah dan *transaction fees* yang tinggi (terutama di *Ethereum*) menjadi penghalang.
* **Store of Value:** Sangat volatil dalam jangka pendek, membuatnya menjadi penyimpan nilai yang buruk untuk periode singkat. Namun, dalam jangka panjang, *Bitcoin* (karena kelangkaannya) cenderung terapresiasi, membuatnya dianggap sebagai "emas digital".
* **Unit of Account:** Belum dapat dianggap sebagai satuan hitung karena harganya masih sering dikutip dalam mata uang *fiat*. Pengecualian penting adalah *NFT*, yang harganya sering dikutip dalam *Ether (ETH)*.

### Ethereum dan Smart Contracts

Ini adalah jembatan langsung ke topik utama buku ini. Jika *Bitcoin* adalah evolusi uang, *Ethereum* adalah evolusi kontrak.

#### Apa itu Smart Contracts?

*Smart contracts* didefinisikan sebagai kontrak yang dikodekan dan dapat dieksekusi secara otomatis tanpa perantara ketika kondisi tertentu terpenuhi.

> **Poin Kunci untuk Auditor:** Penulis membuat koneksi brilian di sini. Uang itu sendiri adalah bentuk **kontrak kerja sama** yang paling dasar. *Bitcoin* adalah kontrak untuk bertransaksi nilai. *Ethereum*, dengan bahasa *Turing-complete* seperti Solidity, memungkinkan **kontrak kerja sama yang jauh lebih canggih dan kompleks** antara orang-orang di seluruh dunia.

Kritik Vitalik Buterin terhadap *Bitcoin* menjadi dasar lahirnya *Ethereum*: *scripting language* *Bitcoin* tidak cukup kuat untuk aplikasi yang kompleks (*non-Turing complete*).

#### Aplikasi Praktis Smart Contract (Contoh dari Buku)

Bab ini memberikan banyak contoh nyata untuk mengilustrasikan potensi *smart contracts*. Saya akan menjelaskannya secara naratif, bukan sekadar daftar.

* **Tokenisasi Aset Dunia Nyata:** Konsep ini merevolusi likuiditas aset. Sebagai contoh, sebuah rumah yang biasanya membutuhkan waktu berbulan-bulan untuk dijual, dapat diwakili oleh *token* digital di *blockchain*. Ini bisa dalam bentuk **kepemilikan fraksional**, di mana banyak *token* mewakili sebagian kecil rumah, atau sebagai satu **NFT** yang mewakili seluruh properti. Ini membuka pasar real estat menjadi global dan dapat diakses siapa saja. Contoh nyata yang diberikan adalah **Propy** (tokenisasi rumah fisik sebagai NFT) dan **Red Swan** (kepemilikan fraksional real estat).
* **Contoh Lain yang Lebih Kreatif:** Potensi *smart contracts* melampaui keuangan. **CryptoWine** adalah *startup* yang mentokenisasi botol anggur sebagai NFT, di mana kepemilikan digital dapat diperdagangkan dan botol fisik akan dikirim saat NFT "dibuka". Di dunia hiburan, film **Calladita** didanai sepenuhnya melalui NFT, di mana investor dapat memperoleh bagian keuntungan atau bahkan mempengaruhi alur cerita.
* **Ekonomi Digital dan Kepemilikan:** Di dunia *fashion* digital, **Mutani** menciptakan pakaian untuk avatar. Di dunia penerbitan, **Book.io** menjual *e-book* sebagai NFT, yang memberikan **kepemilikan sejati** kepada pembeli, tidak seperti lisensi baca dari platform tradisional. Di industri musik, **Violetta Zironi** menjual musiknya sebagai NFT, mengubah penggemarnya menjadi investor. Contoh seni digital paling ikonik adalah **CryptoPunks**, yang nilainya terletak pada signifikansi historisnya sebagai salah satu koleksi NFT pertama.
* **Meningkatkan Model Bisnis Tradisional:** *Smart contracts* juga dapat meningkatkan model bisnis yang sudah ada. **Hotel Le Bristol di Prancis** menggunakan kunci NFT untuk memberikan akses ke pengalaman eksklusif bagi pelanggan setia. Di bidang pendidikan, **Universitas Nicosia** menyelenggarakan kursus pertama yang diakses melalui NFT.
* **Identitas dan Keanggotaan:** Konsep identitas digital terdesentralisasi memungkinkan pengguna untuk mengontrol dan bahkan memonetisasi data pribadi mereka. Klub keanggotaan seperti **Flyfish Club Restaurant** menggunakan NFT untuk memberikan akses eksklusif, di mana keanggotaan itu sendiri menjadi aset yang dapat diperdagangkan.

#### Decentralized Autonomous Organizations (DAOs)

DAOs adalah organisasi yang diatur oleh *smart contracts*, di mana para pemegang *token* dapat mengajukan proposal dan memberikan suara. Ini adalah bentuk tertinggi dari kontrak sosial yang dikodekan. Bab ini memberikan beberapa contoh menarik:
* **Decentralized Exchanges (DEXs):** Seperti **Uniswap**, yang beroperasi sebagai pembuat pasar otomatis tanpa pemimpin terpusat.
* **Lending/Borrowing:** Protokol seperti **Aave** menciptakan pasar pinjam-meminjam global.
* **Niche DAOs:** **Travala** adalah agensi perjalanan terdesentralisasi. **VitaDAO** mendanai penelitian umur panjang. **BeerDAO** mentokenisasi merek bir. **CityDAO** secara kolektif mengelola sebidang tanah di Wyoming.

### Kesimpulan Bab 1

Bab ini ditutup dengan sebuah definisi uang yang komprehensif, yang merangkum semua yang telah dibahas:

> Uang adalah teknologi dan bahasa kompleks yang digunakan manusia untuk berkomunikasi dan memfasilitasi pertukaran nilai, diatur oleh protokol yang disepakati bersama. Ia berevolusi dari barter ke bentuk digital, dan sekarang, dengan *cryptocurrency* dan *smart contracts*, ia menggabungkan prinsip desentralisasi, transparansi, dan programabilitas, yang berpotensi membentuk kembali kontrak ekonomi, tata kelola, dan sosial di era digital.

---

# Bab 2
## Pengantar Arsitektur Ethereum

Bab ini menggunakan analogi yang sangat kuat untuk menyederhanakan konsep *blockchain* yang kompleks. Penulis membandingkan *Ethereum* dengan sebuah *spreadsheet* Excel yang terdistribusi untuk membantu kita memahami bagaimana sebuah "komputer dunia" yang terdesentralisasi dapat beroperasi. Sebagai auditor, memahami arsitektur ini akan memungkinkan Kita untuk mengidentifikasi di mana letak potensi kelemahan, baik itu di tingkat protokol maupun dalam implementasi *smart contract*.

### Dasar-Dasar Ethereum

Pada level paling dasar, *Ethereum* dan *blockchain* lainnya dapat dianggap sebagai sebuah buku besar digital, atau sebuah file Excel yang berisi daftar *transaction*. *Spreadsheet* ini tidak dimiliki oleh satu entitas tunggal, melainkan didistribusikan ke ribuan komputer di seluruh dunia yang disebut ***nodes*** (*node* adalah komputer yang berpartisipasi dalam jaringan).

* **Mekanisme Konsensus Sederhana:** Komputer-komputer ini terus berkomunikasi satu sama lain untuk memastikan bahwa setiap salinan *spreadsheet* tetap identik. Jika satu *node* mencoba mengubah data secara curang (misalnya, menghapus sebuah *transaction*), *node-node* lain akan mendeteksi ketidaksesuaian ini, menolak versi yang telah diubah, dan mengisolasinya dari jaringan. Versi yang jujur dan disepakati bersama adalah yang terus berlanjut.
* **Validator dan Blocks:** Beberapa *node* khusus yang disebut ***validators*** (validator) bertugas untuk mengelompokkan *transaction-transaction* baru yang belum dikonfirmasi (yang berada di dalam ***mempool***, atau "ruang tunggu" *transaction*) ke dalam sebuah blok. Setiap blok ini kemudian diberi ***hash*** (pengenal kriptografis unik) yang juga merujuk ke *hash* dari blok sebelumnya, menciptakan sebuah rantai yang saling terhubung—inilah asal mula istilah "*blockchain*" Proses ini terjadi di *Ethereum* kira-kira setiap 12 detik.
* **"World Computer":** Visi Vitalik Buterin adalah agar semua *node* ini berfungsi sebagai satu komputer global yang terdesentralisasi, yang disebut **"World Computer"**.

Penulis kemudian mengulangi kritik Vitalik terhadap keterbatasan *Bitcoin* yang memotivasi lahirnya *Ethereum*:
* ***Bitcoin is not Turing complete:*** Bahasa *scripting*-nya terlalu sederhana untuk aplikasi yang kompleks.
* ***Bitcoin suffers from value blindness:*** *Script*-nya tidak dapat mengevaluasi atau membandingkan nilai *transaction* secara *native*.
* ***Bitcoin lacks state:*** Sistemnya tidak memiliki cara bawaan untuk "mengingat" status dari *transaction* sebelumnya, yang krusial untuk aplikasi kompleks.
* ***Bitcoin suffers from blockchain blindness:*** *Script*-nya tidak dapat membaca data historis dari *blockchain* itu sendiri.

*Ethereum* dirancang untuk mengatasi semua ini, memungkinkan pembangunan:
* **Aplikasi Finansial:** Dari *transaction* sederhana hingga ekosistem *Decentralized Finance (DeFi)* yang kompleks, termasuk tokenisasi aset.
* **Aplikasi Non-Finansial:** Seperti manajemen identitas digital di mana pengguna memegang kendali penuh atas data mereka, dan sistem pemungutan suara (*voting*) yang transparan dan tahan terhadap kecurangan.

Terakhir, bagian ini menegaskan kembali properti fundamental *Ethereum* sebagai sebuah *blockchain*: *permissionless*, *borderless*, *censorship-resistant*, *immutable*, *transparent*, *global*, dan *decentralized*.

### Trilema Blockchain

Ini adalah konsep inti dalam desain *blockchain*, yang dicetuskan oleh Vitalik Buterin. Trilema ini menyatakan bahwa sebuah *blockchain* hanya dapat mengoptimalkan dua dari tiga properti berikut secara bersamaan:

1.  **Scalability (Skalabilitas):** Kemampuan untuk memproses *transaction* dalam jumlah besar per detik (*Transactions Per Second* atau TPS).
2.  **Security (Keamanan):** Ketahanan jaringan terhadap serangan.
3.  **Decentralization (Desentralisasi):** Kemampuan untuk beroperasi tanpa adanya entitas pengendali tunggal atau kelompok kecil.

Saat ini, *Ethereum* memprioritaskan **keamanan** dan **desentralisasi**, yang berakibat pada **skalabilitas yang rendah**. Ini adalah akar dari masalah biaya ***gas fees*** (*biaya untuk pemrosesan komputasi*) yang tinggi.

### Smart Contracts

Penulis kembali mendefinisikan *smart contracts* sebagai program komputer yang mengeksekusi perjanjian secara otomatis, di mana aturannya tertanam langsung di dalam kode.

* **Analogi Mesin Penjual Otomatis (*Vending Machine*):** Sebuah analogi yang sangat baik digunakan di sini. Mesin penjual otomatis adalah bentuk fisik dari *smart contract*. Kita memasukkan koin (memenuhi kondisi), memilih minuman (memanggil fungsi), dan mesin secara otomatis mengeluarkan minuman tersebut (mengeksekusi hasil). Tidak ada negosiasi, tidak ada perantara.

Bab ini merangkum properti *smart contracts* dalam sebuah tabel (Tabel 2.1), yang akan saya jelaskan secara naratif:

* **Keuntungan (*Pros*):** Otomatisasi mengurangi intervensi manusia dan biaya perantara. Transparansi di *blockchain* memungkinkan siapa saja untuk mengaudit histori *transaction*. Sifat *trustless* memungkinkan pihak yang tidak saling kenal untuk bertransaksi dengan aman karena kode yang menegakkan aturan. Imutabilitas memastikan bahwa setelah diterapkan, kode tidak dapat diubah.
* **Kerugian (*Cons*) dan Tantangan:** Imutabilitas juga menjadi pedang bermata dua; bug yang terdeteksi setelah penerapan sangat sulit untuk diperbaiki. Ketergantungan pada data eksternal (melalui *oracles*) dapat menjadi titik kegagalan jika sumber data terpusat. Kurangnya privasi adalah kebalikan dari transparansi, karena semua detail *transaction* bersifat publik. Isu skalabilitas juga menjadi tantangan besar, terutama di *Ethereum*. Selain itu, teknologi ini masih baru, sehingga preseden hukumnya terbatas dan sulit menemukan ahli yang benar-benar berpengalaman.

### Ethereum Virtual Machine (EVM)

EVM adalah lingkungan eksekusi untuk *smart contracts* di *Ethereum*. Inilah yang menjadikan *Ethereum* sebuah "World Computer". Semua *node* di jaringan menjalankan EVM, yang memastikan bahwa setiap *smart contract* dieksekusi dengan cara yang sama di seluruh jaringan, menjaga konsensus.

*Ethereum* memiliki dua jenis akun:
1.  **Externally Owned Accounts (EOAs):** Akun yang dikendalikan oleh pengguna melalui *private keys*.
2.  **Contract Accounts:** Akun yang dikendalikan oleh kode *smart contract* itu sendiri, yang dieksekusi oleh EVM.

### The Ether Coin (Koin Ether)

*Ether (ETH)* adalah aset *native* dari *blockchain Ethereum*. Fungsinya adalah sebagai "bahan bakar" untuk EVM. Setiap operasi komputasi di *Ethereum* memerlukan biaya dalam bentuk *gas*, dan biaya ini dibayarkan menggunakan ETH.

Penulis merinci unit-unit denominasi *Ether*, dengan **wei** sebagai unit terkecil. Satu *Ether* setara dengan 1 kwintiliun (10^18) *wei*. Unit yang sering Kita temui adalah **gwei** (10^9 *wei*), yang biasa digunakan untuk menyatakan harga *gas*.

### The Byzantine General's Problem dan Mekanisme Konsensus Ethereum

* ***The Byzantine General's Problem*** adalah masalah klasik dalam ilmu komputer: bagaimana mencapai kesepakatan (*consensus*) dalam sistem terdistribusi di mana beberapa partisipan mungkin tidak dapat dipercaya atau bahkan berniat jahat.
* **Proof-of-Work (PoW):** Solusi pertama yang sukses untuk masalah ini diimplementasikan oleh Satoshi Nakamoto di *Bitcoin*.
* **Proof-of-Stake (PoS):** Mekanisme konsensus yang kini digunakan *Ethereum*. Alih-alih menggunakan daya komputasi (seperti PoW), *validators* di PoS mengunci sejumlah ETH (minimal 32 ETH) sebagai jaminan (*stake*) untuk berpartisipasi dalam validasi blok. Mereka dipilih secara acak untuk membuat blok baru. Jika mereka bertindak jujur, mereka mendapatkan imbalan. Jika mereka berbuat curang, *stake* mereka akan disita (proses ini disebut ***slashing***). Proses ini mencapai **finality** (finalitas), di mana sebuah blok dianggap permanen dan tidak dapat diubah, dalam waktu sekitar 12 menit.

### Gas Fees

Ini adalah konsep yang sangat penting bagi auditor karena efisiensi *gas* adalah bagian krusial dari keamanan dan optimisasi *smart contract*.

* **Definisi:** *Gas* adalah unit yang mengukur sumber daya komputasi yang dibutuhkan untuk mengeksekusi operasi. Biaya totalnya, *gas fee*, dihitung dengan rumus:
    $$
    \text{Gas Terpakai} \times (\text{Base Fee} + \text{Priority Fee}) \text{ }
    $$
* ***Base Fee:*** Harga minimum per unit *gas* yang ditetapkan oleh protokol. *Base fee* ini akan "dibakar" (*burned*), artinya dikeluarkan dari sirkulasi.
* ***Priority Fee (Tip):*** Biaya tambahan yang diberikan oleh pengguna untuk memberi insentif kepada *validator* agar memprioritaskan *transaction* mereka.

Penulis menggunakan analogi restoran: *Base Fee* adalah harga makanan di menu, sedangkan *Priority Fee* adalah tip untuk pelayan agar pesanan Kita dilayani lebih dulu.

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_2-1.png" alt="gambar" width="550"/>
</p>

[Tiga tangkapan layar antarmuka MetaMask yang menunjukkan proses penyesuaian gas fee, dari estimasi awal hingga pengaturan lanjutan. - Figure 2.1]

Gambar 2.1 dalam buku menunjukkan bagaimana pengguna di *wallet* MetaMask dapat memilih tingkat *gas fee* (Rendah, Pasar, Agresif) atau mengaturnya secara manual di menu lanjutan, dengan menyesuaikan *Max Base Fee* dan *Priority Fee*.

### Masalah Skalabilitas Ethereum

Dengan kapasitas hanya sekitar 20 TPS, *Ethereum* jauh tertinggal dibandingkan sistem pembayaran tradisional seperti Visa (65.000 TPS). Keterbatasan ini menyebabkan "perang penawaran" (*bidding war*) untuk ruang blok, di mana pengguna saling menaikkan *priority fee* agar *transaction* mereka diproses, menyebabkan lonjakan *gas fees* yang ekstrem pada saat permintaan tinggi.

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_2-2.png" alt="gambar" width="550"/>
</p>

[Grafik garis yang menunjukkan harga gas rata-rata Ethereum dari waktu ke waktu, dengan beberapa puncak lonjakan harga yang signifikan. - Figure 2.2]

Gambar 2.2 mengilustrasikan masalah ini dengan menunjukkan grafik historis harga *gas*, di mana terlihat puncak-puncak harga yang sangat tinggi, bahkan mencapai ratusan *gwei*.

### Solusi Layer 2

Untuk mengatasi masalah skalabilitas, solusi ***Layer 2*** dibangun "di atas" *blockchain* utama *Ethereum* (yang disebut *Layer 1*). Solusi ini memproses *transaction* di luar rantai utama (*off-chain*) untuk mengurangi beban, kemudian mengirimkan hasilnya kembali ke *Layer 1*.

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_2-3.png" alt="gambar" width="550"/>
</p>

[Diagram yang mengilustrasikan konsep sharding, di mana sebuah tabel data besar dengan 'Shard Key' dipecah menjadi tiga tabel yang lebih kecil berdasarkan rentang nilai. - Figure 2.3]

## Rollups

**Rollups** adalah teknologi Layer 2 yang **memproses transaksi di luar L1 (off-chain)**, lalu **mengirim ringkasan hasilnya ke L1**.
Jadi:

* Eksekusi transaksi → dilakukan di L2
* Data hasil transaksi → dikirim ke L1 (Ethereum mainnet)

**Manfaatnya:**

* Mengurangi beban komputasi di L1
* Biaya jauh lebih murah
* Throughput tinggi

Ada dua jenis utama:

### Optimistic Rollups

* Disebut *optimistic* karena **diasumsikan semua transaksi valid secara default**.
* Mereka **tidak langsung membuktikan keabsahan transaksi** saat mengirim ke L1.
* Tapi mereka memberi **periode tantangan (challenge period)**, biasanya beberapa hari.
* Jika ada yang mencurigai kecurangan, mereka bisa **mengajukan *fraud proof*** ke L1.
* Jika terbukti, transaksi penipu dibatalkan dan penipunya kehilangan deposit.

Contoh: Arbitrum, Optimism

Karakteristik:

* Murah dan throughput tinggi
* Tapi finalitas (kepastian transaksi valid) lambat → harus tunggu challenge period selesai

### Zero-Knowledge (ZK) Rollups

* ZK-Rollups **tidak mengasumsikan valid**, mereka **membuktikan semua transaksi benar sejak awal**.
* Setiap batch transaksi dikirim ke L1 bersama **bukti kriptografis (zero-knowledge proof)**.
* Bukti ini **diverifikasi oleh smart contract di L1**.

Contoh: zkSync, Starknet, Scroll

Karakteristik:

* Finalitas cepat (karena langsung ada bukti)
* Lebih kompleks secara teknis (membuat bukti mahal & lambat saat ini)
* Lebih ramah privasi karena bukti tidak mengungkap data mentah transaksi

## Validiums

* **Mirip ZK-Rollups**, tapi **data transaksi disimpan off-chain** sepenuhnya.
* L1 hanya menyimpan **bukti validitas**, **bukan data transaksi mentah**.
* Ini **menghemat ruang dan biaya sangat besar**, karena L1 tidak menyimpan data.

Karakteristik:

* Skalabilitas tinggi (karena data tidak dibebankan ke L1)
* Tapi **keamanan datanya tergantung pada penyedia data off-chain**, bukan Ethereum → ada risiko jika penyedia data hilang atau jahat

Contoh: StarkEx (dalam mode validium)

## Sidechains

* **Blockchain terpisah** yang berjalan berdampingan (paralel) dengan Ethereum.
* Memiliki **konsensus sendiri** dan **validator sendiri**, **bukan dijamin oleh Ethereum**.
* Terhubung ke Ethereum lewat **jembatan (*bridge*)** untuk transfer aset.

Karakteristik:

* Biaya sangat murah dan throughput tinggi
* Tapi keamanan bergantung pada jaringan sidechain itu sendiri (jika validator mereka diserang, dana bisa hilang)

Contoh: Polygon PoS chain, Gnosis Chain

## Sharding

* Teknik untuk **memecah satu blockchain besar jadi banyak *shard* kecil**, masing-masing memproses subset transaksi secara paralel.
* Setiap shard seperti *mini blockchain* yang menyumbangkan hasilnya ke beacon chain (rangka utama Ethereum).

Tujuan:

* Menambah kapasitas transaksi Ethereum
* Mengurangi beban setiap node → setiap node hanya perlu memvalidasi shard tertentu

Catatan:

* Sharding ini rencananya bagian dari roadmap Ethereum, tapi model awal sharding transaksi **diubah menjadi fokus data (lihat Danksharding)**

## Danksharding

* Evolusi dari konsep sharding dalam roadmap Ethereum terbaru.
* Fokus bukan lagi memproses transaksi, tapi **menyediakan ruang data murah dalam bentuk *data blobs*** untuk rollups.
* Dengan **proto-danksharding (EIP-4844)**, Ethereum mulai mendukung **blob-carrying transactions** yang jauh lebih murah untuk rollups.

Tujuan:

* Memberikan **ruang data besar dan murah** supaya rollups bisa menyimpan datanya tanpa membebani gas fee L1.
* Membuat Ethereum menjadi **settlement layer**: tempat rollups memposting bukti dan data ringkasan mereka.

Dampaknya:

* Rollups menjadi jauh lebih murah
* Ethereum tetap aman dan ringan karena hanya menyimpan bukti dan data blob, bukan semua transaksi mentah

## Rangkuman Tabel

| Teknologi          | Eksekusi di Mana | Data disimpan di Mana | Jaminan Keamanan                        | Contoh                      |
| ------------------ | ---------------- | --------------------- | --------------------------------------- | --------------------------- |
| Optimistic Rollups | L2               | L1                    | Fraud proofs (challenge period)         | Arbitrum, Optimism          |
| ZK-Rollups         | L2               | L1                    | Validity proofs (langsung diverifikasi) | zkSync, Starknet            |
| Validiums          | L2               | Off-chain             | Validity proofs, tapi data off-chain    | StarkEx (validium mode)     |
| Sidechains         | Chain terpisah   | Chain terpisah        | Keamanan sendiri (bukan Ethereum)       | Polygon PoS, Gnosis         |
| Sharding           | L1               | L1 (per shard)        | Ethereum validator                      | (rencana lama Ethereum)     |
| Danksharding       | L1               | L1 (data blobs)       | Ethereum validator                      | (roadmap Ethereum sekarang) 

### Solusi Layer 3

**Layer 3 adalah jaringan blockchain khusus (application-specific chain)** yang dibangun **di atas Layer 2**, bukan langsung di Layer 1.

🧠 Sederhananya:

> L1 = keamanan dan konsensus dasar
> L2 = skalabilitas umum untuk semua
> L3 = eksekusi super cepat untuk aplikasi spesifik

#### Cara Kerja Layer 3

* L3 berjalan **di atas infrastruktur L2** seperti Arbitrum Orbit, zkSync Hyperchains, atau Starknet Appchains.
* L3 **mewarisi keamanan dari L2 (dan secara tidak langsung dari L1)**, tapi bisa dikonfigurasi secara bebas:

  * Aturan konsensus sendiri
  * Biaya gas sendiri
  * Token native sendiri
  * Mekanisme privasi sendiri
* Transaksi di L3 → dikumpulkan ke batch → dikirim ke L2 → lalu ke L1 untuk finalitas dan keamanan akhir.

Artinya: mereka **tidak membebani L1 langsung**, sehingga **lebih murah dan lebih cepat**.

#### Contoh Kasus Penggunaan L3

| Bidang                          | Kebutuhan                      | Kenapa Cocok L3                                  |
| ------------------------------- | ------------------------------ | ------------------------------------------------ |
| Game blockchain                 | Ribuan transaksi kecil/detik   | Biaya rendah, finalitas cepat, kustomisasi penuh |
| Media sosial terdesentralisasi  | Banyak interaksi pengguna      | Throughput tinggi, biaya nyaris nol              |
| DeFi perusahaan (institutional) | Privasi, izin akses, kontrol   | Bisa atur siapa yang bisa akses & melihat data   |
| Rollup ekosistem besar          | Sub-rollup khusus per aplikasi | Isolasi performa dan biaya dari aplikasi lain    |

#### Perbedaan L2 vs L3

| Aspek              | Layer 2 (L2)                | Layer 3 (L3)                                 |
| ------------------ | --------------------------- | -------------------------------------------- |
| Tujuan utama       | Skalabilitas umum           | Skalabilitas & kustomisasi aplikasi spesifik |
| Dijalankan di atas | Layer 1                     | Layer 2 (yang di atas L1)                    |
| Biaya transaksi    | Rendah                      | Lebih rendah lagi                            |
| Keamanan           | Disediakan langsung oleh L1 | Mewarisi keamanan dari L2 → lalu ke L1       |
| Kustomisasi        | Terbatas                    | Sangat tinggi (token, konsensus, dll)        |

#### Tantangan Layer 3

* **Kompleksitas meningkat** (stack 3 lapisan harus dikelola)
* **Keamanan tergantung L2** → kalau L2 diserang, semua L3 di atasnya ikut terdampak
* **Masih sangat baru** → banyak eksperimen, standar belum matang

#### Contoh Nyata L3 Saat Ini

* **Arbitrum Orbit:** Framework untuk membangun L3 di atas Arbitrum Nitro
* **zkSync Hyperchains:** L3 berbasis ZK-Rollup yang dapat disesuaikan
* **Starknet Appchains:** Membuat L3 di atas Starknet

### Ethereum: Menuju Finalisasi

*Ethereum* masih dalam pengembangan aktif. Penulis menguraikan *roadmap*-nya:
* **The Merge:** Transisi dari PoW ke PoS (telah selesai).
* **The Surge:** Peningkatan skalabilitas besar-besaran melalui *Danksharding*.
* **The Scourge:** Mengatasi masalah sentralisasi dan sensor terkait *Miner Extractable Value (MEV)*.
* **The Verge:** Mempermudah verifikasi blok dengan memperkenalkan *Verkle trees*.
* **The Purge:** Menghapus data historis lama untuk mengurangi beban penyimpanan pada *node*.
* **The Splurge:** Perbaikan dan penyempurnaan lainnya, termasuk ***Account Abstraction***.

Bab 2 memberikan gambaran arsitektur yang komprehensif. Sebagai seorang auditor, pemahaman tentang Trilema Blockchain, mekanisme *gas*, dan berbagai solusi skalabilitas sangatlah penting. Banyak *bug* dan kerentanan muncul dari interaksi yang salah antara *Layer 1* dan *Layer 2*, atau dari asumsi yang salah tentang bagaimana EVM menangani *state* dan eksekusi. Bab ini adalah dasar teknis Kita untuk bab-bab berikutnya yang lebih fokus pada kode Solidity.

---

# Bab 3
## Wallets, MetaMask, and Block Explorers

Bab ini merupakan fondasi praktis yang sangat penting. Sebelum Kita dapat mengaudit atau mengamankan sebuah *smart contract*, Kita harus terlebih dahulu memahami alat-alat fundamental untuk berinteraksi dengan sebuah *blockchain*. Bab ini memperkenalkan tiga pilar utama: *cryptocurrency wallets* sebagai gerbang Kita ke aset digital, MetaMask sebagai implementasi *browser wallet* yang populer, dan *block explorers* sebagai jendela transparan untuk memverifikasi semua aktivitas *on-chain*.

Bagi seorang auditor, penguasaan materi ini bukan sekadar pengetahuan dasar, melainkan kemampuan inti. Kita akan belajar bagaimana dana dikelola dengan aman, bagaimana interaksi dengan *Decentralized Applications* (DApps) terjadi, dan yang terpenting, bagaimana cara memverifikasi setiap *transaction* dan status *contract* secara independen—sebuah praktik yang merangkum esensi dari moto "jangan percaya, verifikasi" (*don't trust, verify*).

### Memahami Wallets

Di dunia fisik, *wallet* (dompet) adalah tempat Kita menyimpan uang tunai. Namun, dalam dunia *cryptocurrency*, konsep ini sedikit berbeda dan lebih teknis. Sebuah **`wallet`** pada dasarnya bukanlah wadah yang menyimpan *cryptocurrency* Kita. Sebaliknya, *wallet* adalah sebuah antarmuka perangkat lunak (*software*) atau perangkat keras (*hardware*) yang mengelola **kunci kriptografis** Kita. Kunci-kunci inilah yang memberi Kita akses dan kontrol atas aset Kita yang tercatat di *blockchain*.

Ada dua jenis kunci utama:
* **`Private Key`**: Ini adalah kunci rahasia, mirip dengan kata sandi super penting atau PIN ATM Kita. Siapa pun yang memiliki `private key` Kita dapat mengakses dan membelanjakan dana Kita. Menjaga kerahasiaan `private key` adalah prioritas keamanan tertinggi.
* **`Public Key`**: Kunci ini berasal dari `private key` Kita dan dapat dibagikan secara bebas. Dari `public key` inilah alamat *wallet* Kita (*wallet address*) dibuat, yang berfungsi seperti nomor rekening bank yang bisa Kita berikan kepada orang lain untuk menerima dana.

Bab ini mengkategorikan *wallets* ke dalam beberapa jenis, masing-masing dengan kelebihan, kekurangan, dan skenario penggunaan yang berbeda.

#### Hosted Wallets

*Hosted wallets* adalah *wallets* di mana `private key` Kita dikelola oleh pihak ketiga, biasanya sebuah bursa *cryptocurrency* (*cryptocurrency exchange*) seperti Binance atau Coinbase. Ini adalah jenis *wallet* yang paling umum digunakan oleh pemula karena kemudahannya.

* **Keuntungan**:
    * **Kemudahan Penggunaan**: Kita tidak perlu khawatir mengelola `private key` sendiri. Jika Kita lupa kata sandi, biasanya ada opsi pemulihan.
    * **Tanpa Biaya Tambahan**: Tidak perlu membeli perangkat keras khusus.
    * **Hemat Waktu**: Tidak perlu belajar tentang berbagai jenis *wallet* dan cara mengamankannya.

* **Kekurangan (Sangat Krusial untuk Auditor)**:
    * **Sentralisasi**: Ini bertentangan dengan etos desentralisasi. Kita pada dasarnya membuat ulang sistem perbankan tradisional di mana Kita mempercayakan dana Kita kepada pihak ketiga.
    * **Risiko Pihak Ketiga**: Jika bursa tersebut bangkrut, diretas, atau dikelola oleh pelaku kejahatan, dana Kita kemungkinan besar akan hilang selamanya. Ini adalah poin kegagalan tunggal (*single point of failure*).
    * **Risiko Regulasi**: Pemerintah dapat memerintahkan bursa untuk membekukan atau menyita aset pengguna.

* **Praktik Terbaik**:
    1.  **Diversifikasi**: Jika harus menggunakan *hosted wallets*, sebarkan dana Kita di beberapa bursa terkemuka untuk mengurangi risiko jika salah satu bursa gagal.
    2.  **Bookmark Situs**: Selalu akses situs bursa melalui *bookmark* yang telah Kita simpan untuk menghindari situs *phishing*.
    3.  **Verifikasi Tim di Komunitas**: Di server Discord atau Telegram, pastikan setiap pengumuman penting (seperti *Airdrop*) datang dari anggota tim resmi yang memiliki lencana terverifikasi.

* **Studi Kasus (Pelajaran dari Kegagalan)**:
    * **Mount Gox**: Sebuah bursa yang menangani >70% *transaction* Bitcoin pada tahun 2014, bangkrut setelah serangkaian peretasan. Bertahun-tahun kemudian, para pelanggan masih berjuang untuk mendapatkan kembali sebagian kecil dari dana mereka. Ini adalah contoh klasik dari risiko mempercayakan `private key` Kita kepada pihak lain.
    * **QuadrigaCX**: Bursa asal Kanada ini runtuh setelah pendirinya, Gerald Cotten, dilaporkan meninggal secara misterius di India, membawa serta akses ke `private key` yang menyimpan dana pelanggan senilai hampir $200 juta. Kasus ini menyoroti bahaya ketika hanya satu orang yang memiliki kontrol penuh.
    * **FTX**: Salah satu bursa terbesar di dunia yang runtuh pada tahun 2022 karena salah urus dana dan penipuan. Kejatuhannya, meskipun didukung oleh tokoh-tokoh terkenal, menegaskan kembali prinsip utama dalam *blockchain*: **"jangan percaya, verifikasi" (*don't trust, verify*)**. Satu-satunya kebenaran yang dapat diandalkan adalah apa yang tercatat *on-chain*.

#### Browser Wallets

*Browser wallets* adalah ekstensi yang terintegrasi langsung ke peramban web Kita, seperti MetaMask. Mereka berfungsi sebagai jembatan yang mudah antara pengguna dan DApps.

* **Keuntungan**:
    * **Akses Mudah dan Cepat**: Sangat praktis untuk *transaction* sehari-hari bernilai kecil dan interaksi dengan DApps.
    * **Integrasi DApps**: Memungkinkan koneksi yang mulus ke situs-situs Web3.

* **Kekurangan**:
    * **Kerentanan Online**: Karena terhubung langsung ke internet, *wallets* ini rentan terhadap serangan *phishing*, situs web berbahaya, dan *malware* yang dapat mencuri `private key` atau `seed phrase` Kita.

* **Studi Kasus (Taktik Penipuan)**:
    * **Situs Web Berbahaya**: Penipu membuat situs yang terlihat identik dengan situs asli, misalnya `binαnce.com` (menggunakan huruf Yunani 'α') bukan `binance.com`. Ketika pengguna menghubungkan *wallet* mereka, dana mereka akan terkuras.
    * **Penipuan Lowongan Pekerjaan**: Penipu yang menyamar sebagai perekrut akan melalui proses wawancara yang meyakinkan. Di tahap akhir, mereka meminta kandidat untuk menghubungkan *wallet* mereka ke "situs tim" untuk "menguji fitur". Setelah kepercayaan dibangun, korban akan kehilangan asetnya saat menghubungkan *wallet*.

#### Desktop Wallets

*Desktop wallets* adalah aplikasi yang diunduh dan dijalankan di komputer Kita. Ada dua sub-tipe:

1.  **Desktop Wallet (Full Nodes)**:
    * **Cara Kerja**: Mengunduh dan menyimpan seluruh riwayat *blockchain*.
    * **Keuntungan**: Memberikan kontrol dan keamanan penuh, serta berkontribusi pada desentralisasi dan keamanan jaringan. Sulit bagi penyerang untuk menargetkan individu dibandingkan bursa terpusat.
    * **Kekurangan**: Membutuhkan ruang penyimpanan yang sangat besar (bisa mencapai terabyte) dan waktu sinkronisasi yang lama. Rentan terhadap *malware* di komputer.

2.  **Desktop Wallet (Lightweight)**:
    * **Cara Kerja**: Tidak mengunduh seluruh *blockchain*. Sebaliknya, ia mengandalkan *full nodes* lain untuk mendapatkan data *transaction* yang relevan.
    * **Keuntungan**: Lebih hemat ruang dan *bandwidth*. `Private key` tetap disimpan di komputer pengguna, memberikan kontrol penuh.
    * **Kekurangan**: Bergantung pada pihak ketiga (*full nodes*) untuk data, yang dapat menimbulkan risiko privasi jika *node* tersebut memata-matai *transaction* Kita.

#### Mobile Wallets

*Mobile wallets* adalah aplikasi di ponsel Kita, menawarkan portabilitas dan kemudahan untuk *transaction* saat bepergian.

* **Keuntungan**:
    * **Portabel dan Nyaman**: Mudah digunakan untuk pembayaran sehari-hari, sering kali dengan pemindaian kode QR.
    * **Backup**: Dana dapat dipulihkan melalui `seed phrase` jika ponsel hilang atau dicuri.

* **Kekurangan**:
    * **Risiko Fisik**: PIN atau detail sensitif lainnya dapat terlihat oleh orang lain atau kamera.
    * **Serangan SIM Swap**: Penyerang dapat mengambil alih nomor telepon Kita untuk melewati otentikasi dua faktor berbasis SMS.
    * **Malware**: Ponsel juga rentan terhadap aplikasi berbahaya yang dapat mencuri `seed phrase`.

* **Studi Kasus (SIM Swap)**:
    * Bahkan Vitalik Buterin, pendiri Ethereum, pernah menjadi korban serangan **`SIM swap`**. Penyerang berhasil menguasai akun Twitter-nya dan memposting tautan *phishing*, yang menyebabkan pengikutnya kehilangan dana senilai $700.000. Ini menunjukkan betapa berbahayanya mengandalkan keamanan berbasis nomor telepon.

#### Cold Storage / Hardware Wallet

Ini adalah metode penyimpanan `private key` secara *offline*, dianggap sebagai cara teraman untuk melindungi aset digital dari ancaman online.

* **`Hardware Wallet`**: Perangkat fisik (seperti Trezor atau Ledger) yang menyimpan `private key` Kita secara terisolasi. *Transaction* ditandatangani di dalam perangkat tanpa `private key` pernah meninggalkan perangkat tersebut.
* **Keuntungan**:
    * **Keamanan Maksimal**: Isolasi *offline* membuatnya sangat tahan terhadap peretasan dan *malware*.
    * **Kontrol Penuh**: Pengguna memegang kendali penuh atas `private key` mereka.
    * **Keamanan Tambahan**: Dilindungi oleh PIN dan frasa pemulihan (*seed phrase*).
* **Kekurangan**:
    * **Biaya**: Perangkat ini harus dibeli.
    * **Kurang Praktis**: Tidak secepat *browser* atau *mobile wallet* untuk *transaction* harian.
    * **Risiko Rantai Pasokan (*Supply Chain Attack*)**: Perangkat dapat dirusak selama pengiriman. **Selalu beli langsung dari produsen resmi.**

* **Praktik Terbaik**:
    * Gunakan cadangan logam (*metal backup*) untuk `seed phrase` Kita, bukan hanya kertas, agar tahan terhadap api dan air.

* **Metode Alternatif (DIY Hardware Wallet)**:
    * Bab ini juga menyarankan cara membuat *hardware wallet* dengan biaya rendah, seperti menggunakan **ponsel lama**. Prosesnya meliputi reset pabrik, menginstal aplikasi seperti **Airgap Vault**, dan kemudian mengisolasi perangkat sepenuhnya dari internet (*air-gapped*).
    * **Keuntungan**: Hemat biaya, tahan terhadap *supply chain attack*, dan menjaga privasi.
    * **Kekurangan**: Tidak sekuat *hardware wallet* komersial (misalnya, tidak tahan api/air) dan tidak mendukung semua fitur seperti NFT.

#### Multisignature Wallets

**`Multisignature (multisig) wallets`** adalah *wallets* yang memerlukan lebih dari satu tanda tangan (`private key`) untuk mengotorisasi sebuah *transaction*. Ini bekerja dengan skema "N dari M", di mana N adalah jumlah tanda tangan yang diperlukan dari total M pemilik kunci.

* **Contoh**: Sebuah *wallet* 3 dari 5 memerlukan persetujuan dari 3 `private key` yang berbeda dari total 5 yang terdaftar.
* **Kegunaan**:
    * **Organisasi (DAO)**: Mencegah satu individu membuat keputusan sepihak dan menambahkan lapisan akuntabilitas.
    * **Individu**: Meningkatkan keamanan pribadi. Jika satu kunci Kita dicuri, dana tetap aman karena penyerang masih memerlukan kunci lainnya.
* **Kelemahan**: Kompleksitas dalam mengelola beberapa `private key`.

#### Hierarchical Deterministic (HD) Wallets

**`HD wallets`** adalah standar modern untuk *wallets*. Mereka menghasilkan sebuah **`master private key`** (biasanya direpresentasikan sebagai `seed phrase`) yang darinya serangkaian `child private key` dan alamat dapat dibuat secara deterministik (dapat diprediksi).

* **Keuntungan**: Menyederhanakan proses *backup*. Kita hanya perlu mencadangkan satu `seed phrase` untuk memulihkan semua alamat yang pernah dibuat oleh *wallet* tersebut. Ini sangat berguna dalam konteks *multisig*.
* **Kelemahan**: Jika `master private key` (atau `seed phrase`) Kita bocor, semua alamat anak (*child addresses*) juga akan terancam.

### Tutorial Praktis: Menggunakan MetaMask

Bab ini menggunakan MetaMask sebagai contoh utama untuk *browser wallet*. Tujuannya adalah untuk mengakses *testnets*, mendapatkan ETH percobaan dari *faucets*, dan mendeploy *smart contracts* tanpa menggunakan uang sungguhan.

#### Menginstal MetaMask

Proses instalasi dijelaskan langkah demi langkah:
1.  Kunjungi situs web resmi `metamask.io`. (Sangat penting untuk memastikan URL-nya benar).
2.  Unduh ekstensi untuk peramban Kita (Chrome, Firefox, Brave, dll.).
3.  Pilih "Create New Wallet".
4.  Buat kata sandi. Kata sandi ini hanya untuk mengunci dan membuka ekstensi di peramban Kita, BUKAN `private key` Kita.
5.  **Langkah Paling Krusial**: MetaMask akan menampilkan **`Secret Recovery Phrase`** atau **`seed phrase`** Kita, yang biasanya terdiri dari 12 kata.

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_3-1.png" alt="gambar" width="550"/>
</p>

[Contoh 12 kata seed phrase yang dihasilkan oleh MetaMask, seperti mammal, transfer, hint, dll. - Figure 3.1]

> **PERINGATAN**: `Seed phrase` ini adalah `master key` Kita. Tulis di atas kertas atau logam, simpan di tempat yang sangat aman, dan **JANGAN PERNAH** membagikannya kepada siapa pun atau menyimpannya secara digital (misalnya di komputer atau cloud). Jika Kita kehilangan `seed phrase` ini, dana Kita akan hilang selamanya. Jika orang lain mendapatkannya, mereka dapat mencuri semua dana Kita.

6.  Konfirmasi `seed phrase` Kita, dan instalasi selesai. Kita akan melihat antarmuka utama MetaMask.

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_3-2.png" alt="gambar" width="550"/>
</p>

[Tampilan antarmuka utama ekstensi browser MetaMask setelah instalasi berhasil, menunjukkan saldo 0 ETH. - Figure 3.2]

#### Login Kembali dengan Seed Phrase

Untuk memperkuat pemahaman tentang pentingnya `seed phrase`, bab ini memandu Kita untuk menghapus ekstensi MetaMask dan menginstalnya kembali. Kali ini, alih-alih membuat *wallet* baru, Kita akan memilih "Import An Existing Wallet" dan memasukkan 12 kata `seed phrase` yang telah Kita simpan. Proses ini menunjukkan bahwa selama Kita memiliki `seed phrase`, Kita dapat memulihkan akses ke dana Kita di perangkat apa pun.

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_3-5.png" alt="gambar" width="550"/>
</p>

[Tampilan proses impor seed phrase di MetaMask, di mana pengguna memasukkan 12 kata rahasia. - Figure 3.5]

#### Mengganti Jaringan

*Blockchain* memiliki dua jenis jaringan utama:
* **`Mainnet`**: Jaringan utama tempat *transaction* bernilai nyata terjadi.
* **`Testnet`**: Jaringan percobaan yang meniru *mainnet* tetapi menggunakan aset tanpa nilai. Ini adalah tempat bagi *developer* untuk menguji *smart contracts* mereka.

MetaMask secara default terhubung ke Ethereum Mainnet. Bab ini menunjukkan cara beralih ke *testnet* seperti **Sepolia**:
1.  Klik menu jaringan di pojok kiri atas MetaMask.
2.  Aktifkan "Show test networks".
3.  Pilih "Sepolia" dari daftar.

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_3-9.png" alt="gambar" width="550"/>
</p>

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_3-10.png" alt="gambar" width="550"/>
</p>

[Menu pilihan jaringan di MetaMask, dengan tombol 'Show test networks' diaktifkan. - Figure 3.9 & 3.10]

ETH di jaringan Sepolia (SepoliaETH) tidak memiliki nilai di dunia nyata dan hanya digunakan untuk tujuan pengujian.

#### Berinteraksi dengan Faucets

**`Faucets`** adalah situs web atau aplikasi yang memberikan sejumlah kecil ETH *testnet* secara gratis kepada pengguna untuk tujuan pengujian.
Bab ini mencantumkan beberapa *faucets* terkemuka seperti Alchemy, Infura, dan Chainlink. Namun, banyak dari mereka memerlukan saldo ETH *mainnet* minimal untuk mencegah penyalahgunaan.

Sebagai alternatif, bab ini merekomendasikan `sepolia-faucet.pk910.de`, sebuah *faucet* berbasis *Proof-of-Work* (PoW). Namun, untuk menggunakannya, Kita perlu memverifikasi identitas Kita melalui **Gitcoin Passport** untuk mencapai skor minimum. Ini dilakukan dengan menghubungkan akun-akun seperti GitHub, Google, atau LinkedIn Kita untuk membuktikan bahwa Kita adalah pengguna unik.

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_3-13.png" alt="gambar" width="550"/>
</p>

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_3-14.png" alt="gambar" width="550"/>
</p>

[Tampilan faucet Sepolia yang meminta verifikasi melalui Gitcoin Passport sebelum memulai proses mining. - Figure 3.13 & 3.14]

Setelah terverifikasi, Kita bisa memulai proses "mining" untuk mendapatkan SepoliaETH.

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_3-15.png" alt="gambar" width="550"/>
</p>

[Tampilan layar faucet yang sedang dalam proses "mining" SepoliaETH, menunjukkan hashrate dan reward yang terkumpul. - Figure 3.15]

#### Mengirim Transaksi Pertama Anda

Setelah mendapatkan SepoliaETH, bab ini memandu Kita melakukan *transaction* pertama:
1.  Klik tombol "Send" di MetaMask.
2.  Masukkan alamat ETH penerima.
3.  Masukkan jumlah ETH yang akan dikirim (misalnya, 0.01 SepoliaETH).
4.  MetaMask akan menampilkan perkiraan **`gas fee`**, yaitu biaya untuk memproses *transaction* di jaringan.
5.  Klik "Confirm". *Transaction* akan dikirim dan statusnya akan berubah dari "Pending" menjadi "Confirmed" setelah beberapa detik.

Selamat, Kita telah berhasil mengirim *transaction cryptocurrency* pertama Kita!

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_3-20.png" alt="gambar" width="550"/>
</p>

[Tampilan ringkasan transaksi di MetaMask sebelum konfirmasi akhir, menunjukkan jumlah yang akan dikirim dan estimasi gas fee. - Figure 3.20]

### Block Explorers: Jendela Transparan Menuju Blockchain

Karena *blockchain* bersifat publik, semua *transaction* dapat diverifikasi oleh siapa pun. Alat utama untuk melakukan ini adalah **`block explorer`**, sebuah situs web yang berfungsi seperti mesin pencari untuk *blockchain*. Untuk Ethereum, *block explorer* yang paling populer adalah **Etherscan** (`etherscan.io` untuk *mainnet* dan `sepolia.etherscan.io` untuk *testnet* Sepolia).

Bagi seorang auditor, *block explorer* adalah alat yang paling esensial.

#### Anatomi Transaksi di Block Explorer

Dengan mengklik *transaction hash* dari *transaction* yang baru saja Kita kirim, Etherscan akan menampilkan rincian lengkapnya:

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_3-25.png" alt="gambar" width="550"/>
</p>

[Tampilan detail transaksi di Etherscan, menunjukkan hash, status, nomor blok, dan alamat pengirim/penerima. - Figure 3.25]

* **`Transaction Hash`**: ID unik untuk *transaction* tersebut.
* **`Status`**: Menunjukkan apakah *transaction* berhasil (*Success*), gagal (*Failed*), atau masih tertunda (*Pending*).
* **`Block`**: Nomor *block* di mana *transaction* ini dimasukkan.
* **`Timestamp`**: Waktu kapan *transaction* dikonfirmasi.
* **`From`**: Alamat pengirim.
* **`To`**: Alamat penerima.
* **`Value`**: Jumlah ETH yang ditransfer.
* **`Transaction Fee`**: Total *gas fee* yang dibayarkan.

#### Anatomi Block di Block Explorer

Kita juga dapat memeriksa seluruh *block*:

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_3-27.png" alt="gambar" width="550"/>
</p>

[Tampilan detail sebuah blok di Etherscan, menunjukkan tinggi blok, timestamp, jumlah transaksi, dan penggunaan gas. - Figure 3.27]

* **`Block Height`**: Nomor urut *block* sejak *block* pertama (*genesis block*).
* **`Timestamp`**: Waktu saat *block* divalidasi.
* **`Transactions`**: Jumlah *transaction* yang termasuk di dalam *block* ini.
* **`Fee Recipient`**: Alamat *validator* yang menerima *fee* dari *block* ini.
* **`Gas Used` & `Gas Limit`**: Jumlah *gas* yang digunakan oleh semua *transaction* di *block* dan batas maksimum *gas* per *block*.

#### Menghubungkan ke DApps dan Anatomi Wallet/Contract

Bab ini menggunakan Uniswap sebagai contoh untuk menunjukkan interaksi *wallet* dengan DApp. Prosesnya meliputi mengunjungi situs DApp, mengklik "Connect Wallet", dan memberikan izin di MetaMask.

Lebih penting lagi bagi auditor, Kita dapat menggunakan *block explorer* untuk menganalisis alamat *wallet* atau *smart contract* apa pun. Dengan memasukkan alamat di Etherscan, Kita dapat melihat:
* **Balance**: Saldo ETH.
* **Token Holdings**: Daftar semua token ERC-20 dan NFT (ERC-721) yang dimiliki alamat tersebut. Ini sangat berguna untuk mengidentifikasi token mencurigakan atau penipuan.
* **Transactions**: Riwayat lengkap semua *transaction* yang masuk dan keluar.
* **Internal Transactions**: *Transaction* yang dipicu oleh *smart contract* lain.
* **Contract Tab**: Jika alamat tersebut adalah *smart contract*, tab ini sangat penting.
    * **Code**: Jika *contract* telah diverifikasi, Kita dapat melihat kode sumber Solidity-nya secara langsung di Etherscan.
    * **Read Contract**: Memungkinkan Kita memanggil semua fungsi `view` dan `pure` dari *contract* tanpa biaya *gas* untuk membaca statusnya.
    * **Write Contract**: Memungkinkan Kita untuk terhubung dengan *wallet* Kita dan memanggil fungsi yang mengubah status *contract*, yang akan memerlukan *gas fee*.
    * **Read/Write as Proxy**: Jika *contract* menggunakan pola *proxy* (dibahas di Bab 12), tab ini memungkinkan Kita berinteraksi dengan *logic contract* yang mendasarinya.

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_3-52.png" alt="gambar" width="550"/>
</p>

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_3-53.png" alt="gambar" width="550"/>
</p>

[Tampilan tab 'Contract' di Etherscan untuk sebuah smart contract yang terverifikasi, menunjukkan kode sumber, serta opsi Read, Write, dan Proxy. - Figure 3.52 & 3.53]

Kita sekarang memiliki kemampuan praktis untuk berinteraksi, mengelola aset, dan yang terpenting, memverifikasi aktivitas di *blockchain* Ethereum. Keterampilan ini akan menjadi dasar saat kita mulai menulis dan mendeploy *smart contract* kita sendiri di bab-bab berikutnya.

---

# Bab 4
## Remix, Data Types, Visibility, and HelloWorld

Bab ini adalah titik awal Anda dalam menulis kode Solidity secara praktis. Kita akan beralih dari konsep teoretis ke implementasi nyata dengan menggunakan **Remix IDE**, sebuah lingkungan pengembangan yang sangat ramah bagi pemula. Tujuan utama bab ini adalah membangun *smart contract* pertama Kita—sebuah program klasik "HelloWorld"—sambil membedah elemen-elemen paling fundamental dalam pemrograman Solidity.

Bagi seorang calon auditor, bab ini sangat krusial karena memperkenalkan "anatomi" dasar dari sebuah *smart contract*: bagaimana lisensi dan versi dideklarasikan, bagaimana data disimpan melalui **`data types`**, dan bagaimana akses ke fungsi dikontrol melalui **`visibility levels`**. Memahami fondasi ini akan memungkinkan Kita untuk mulai "membaca" dan menganalisis kode dengan benar.

### Apa Itu Pemrograman?

Sebelum masuk ke kode, bab ini memberikan analogi yang sangat membantu: **pemrograman adalah proses belajar bahasa baru untuk berkomunikasi dengan komputer** Sama seperti bahasa manusia (misalnya, Bahasa Spanyol atau Rusia), bahasa pemrograman memiliki struktur, aturan (sintaks), dan ekspresi yang unik.

  * **Evolusi dan Budaya**: Bahasa pemrograman berevolusi, dengan versi baru yang memperkenalkan fitur-fitur baru, sama seperti kata "selfie" masuk ke dalam leksikon global. Setiap bahasa juga memiliki "budaya" atau etosnya sendiri; misalnya, Python menekankan kesederhanaan, sementara Solidity mencerminkan prinsip-prinsip *blockchain* seperti transparansi, keamanan, dan desentralisasi.
  * **Compiler sebagai Penerjemah**: Perbedaan utama adalah tujuan komunikasinya. Bahasa manusia untuk antar-manusia, sementara bahasa pemrograman untuk manusia ke komputer. Komputer pada dasarnya hanya memahami kode biner (angka 0 dan 1). Oleh karena itu, kita memerlukan **`compiler`**, yang bertindak sebagai "penerjemah" yang mengubah kode Solidity yang dapat dibaca manusia menjadi *bytecode* yang dapat dipahami dan dieksekusi oleh komputer (khususnya, oleh *Ethereum Virtual Machine* atau EVM).

### Memulai dengan Solidity, Remix, dan HelloWorld

**Solidity** adalah bahasa pemrograman *high-level*, yang berarti sintaksnya lebih dekat dengan bahasa manusia sehingga lebih mudah dibaca dan dipahami dibandingkan bahasa *low-level*. Hal penting yang harus selalu diingat adalah Solidity bersifat **`case-sensitive`**. Ini berarti huruf besar dan huruf kecil dianggap berbeda. Misalnya, `pragma` adalah sintaks yang valid, tetapi `Pragma` akan menghasilkan *error* karena *compiler* tidak mengenalinya. Bagi Solidity, `p` dan `P` adalah karakter yang sama sekali berbeda.

Untuk mulai menulis kode, kita akan menggunakan **Remix IDE**.

#### Membuat File HelloWorld.sol di Remix

Remix adalah *Integrated Development Environment* (IDE) berbasis web yang bisa diakses langsung melalui peramban di `https://remix.ethereum.org`. Langkah-langkah berikut akan memandu Kita dalam menyiapkan *workspace* dan membuat *file* pertama Kita.

1.  **Buka Remix**: Saat Kita membuka situs Remix, Kita akan disambut dengan antarmuka default yang berisi beberapa *file* dan folder contoh.

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_4-1.png" alt="gambar" width="550"/>
</p>

[Tampilan antarmuka awal Remix IDE saat pertama kali dibuka. - Figure 4.1]

2.  **Bersihkan Workspace**: Untuk memulai dari awal, bab ini menginstruksikan untuk menghapus semua *file* dan folder default (`contracts`, `scripts`, `tests`, dll.). Kita dapat melakukannya dengan mengklik kanan pada setiap item dan memilih "Delete".

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_4-2.png" alt="gambar" width="550"/>
</p>

[Tampilan panel File Explorer di Remix, menunjukkan proses menghapus file default. - Figure 4.2]

3.  **Buat File Baru**: Klik kanan di area kosong pada panel *File Explorer* dan pilih "New File".

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_4-3.png" alt="gambar" width="550"/>
</p>

[Menu konteks yang muncul setelah klik kanan di File Explorer Remix, dengan opsi 'New File' disorot. - Figure 4.3]

4.  **Beri Nama File**: Sebuah *file* kosong akan muncul. Beri nama **`HelloWorld.sol`**. Bagian `.sol` adalah ekstensi yang memberitahu *compiler* bahwa *file* ini berisi kode Solidity.

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_4-5.png" alt="gambar" width="550"/>
</p>

[File baru yang telah dibuat dan diberi nama HelloWorld.sol di workspace Remix. - Figure 4.5]

Setelah langkah-langkah ini, Kita akan memiliki kanvas kosong yang siap untuk diisi dengan kode *smart contract* pertama Kita.

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_4-6.png" alt="gambar" width="550"/>
</p>

[Tampilan editor kode Remix yang kosong dengan tab file HelloWorld.sol yang aktif. - Figure 4.6]

### //SPDX-License-Identifier

Setiap *file* Solidity harus dimulai dengan baris komentar khusus ini. Di Solidity, dua garis miring (`//`) menandakan sebuah **`comment`** (komentar). Teks apa pun setelah `//` pada baris yang sama akan diabaikan oleh *compiler* dan tidak dianggap sebagai kode. Komentar sangat berguna untuk:

  * Menjelaskan logika kode yang kompleks kepada rekan tim atau diri Kita di masa depan.
  * Mendokumentasikan fungsi dan keputusan desain.
  * Membantu orang lain (termasuk auditor) memahami maksud dari kode Kita di *blockchain* yang bersifat *open-source*.

Namun, baris `//SPDX-License-Identifier: MIT` adalah sebuah pengecualian. Meskipun diawali dengan `//`, *compiler* tidak mengabaikannya. Ini adalah deklarasi standar yang mengidentifikasi lisensi *software* dari kode Kita, misalnya, `MIT`, `GPL-3.0`, atau `Unlicensed`. Jika baris ini tidak ada, *compiler* akan memberikan peringatan. Pikirkan ini sebagai "salam pembuka" wajib untuk setiap *file* Solidity.

### Versi Solidity dan Baris `pragma`

Baris kedua yang krusial adalah deklarasi versi *compiler*.

```solidity
//SPDX-License-Identifier: MIT
pragma solidity 0.8.25;
```

  * **`pragma`**: Ini adalah arahan (*directive*) khusus untuk *compiler*. Dalam hal ini, `pragma solidity` memberitahu *compiler* versi mana yang harus digunakan untuk mengompilasi kode ini.
  * **`0.8.25`**: Ini adalah nomor versinya. Bab ini memecahnya dengan sangat baik:
      * **`0` (Major Version)**: Menandakan perubahan besar yang dapat merusak kompatibilitas (*breaking changes*). Analogi yang diberikan adalah perubahan dari Bahasa Yunani Kuno ke Bahasa Yunani Modern.
      * **`8` (Minor Version)**: Menandakan penambahan fitur baru yang tidak merusak kompatibilitas. Analogi yang diberikan adalah penambahan kata baru seperti "selfie" ke dalam kamus.
      * **`25` (Patch Version)**: Menandakan perbaikan *bug* atau pembaruan kecil. Analogi yang diberikan adalah koreksi ejaan dalam sebuah kata.
  * **`;` (Semicolon)**: Di Solidity, setiap pernyataan (*statement*) harus diakhiri dengan titik koma. Ini mirip dengan penggunaan titik di akhir kalimat dalam bahasa manusia.

### `contract HelloWorld {}`

Setelah lisensi dan versi, baris berikutnya adalah deklarasi *contract* itu sendiri.

```solidity
//SPDX-License-Identifier: MIT
pragma solidity 0.8.25;

contract HelloWorld {}
```

  * **`contract`**: Ini adalah *keyword* yang mendefinisikan sebuah *smart contract*.
  * **`HelloWorld`**: Ini adalah nama yang Kita berikan untuk *contract* Kita.
  * **`{}` (Curly Braces)**: Tanda kurung kurawal ini mendefinisikan "tubuh" atau cakupan (*scope*) dari *contract*. Semua kode, variabel, dan fungsi yang menjadi bagian dari *contract* ini akan ditulis di antara `{` dan `}`.

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_4-8.png" alt="gambar" width="550"/>
</p>

[Tampilan kode dasar contract HelloWorld di Remix dengan kurung kurawal pembuka dan penutup. - Figure 4.8]

### Data Types dan Variables di Solidity

Dalam bahasa manusia, kita menyampaikan informasi (data) melalui kata atau angka. Demikian pula, Solidity berkomunikasi dengan komputer melalui **`data types`**. *Data type* mendefinisikan jenis data yang dapat disimpan oleh sebuah **`variable`**. Bab ini memperkenalkan enam tipe data dasar.

1.  **`int` (Integer)**: Mewakili bilangan bulat, bisa positif atau negatif (misalnya, 3, -3).

    ```solidity
    int number = -5;
    ```

2.  **`uint` (Unsigned Integer)**: Mewakili bilangan bulat positif saja (termasuk 0). Ini adalah tipe data yang paling umum digunakan untuk nilai moneter atau hitungan, karena jumlah token tidak mungkin negatif.

    ```solidity
    uint number2 = 35;
    ```

3.  **`string`**: Mewakili serangkaian karakter atau teks. Teks harus diapit oleh tanda kutip ganda (`"`) atau tunggal (`'`).

    ```solidity
    string name = "Alexandros";
    ```

4.  **`address`**: Tipe data khusus untuk menyimpan alamat Ethereum (20-byte). Ini digunakan untuk mereferensikan akun pengguna atau *smart contract* lain.

    ```solidity
    address MyETHaddress = 0xd0A7f0e336af86aCC72d85af1EDf25790bAd76a4;
    ```

5.  **`bool` (Boolean)**: Hanya dapat menyimpan dua nilai: `true` atau `false`.

    ```solidity
    bool isTrue = true;
    ```

6.  **`bytes`**: Mewakili serangkaian data *byte*. Tipe ini sering kali lebih efisien dari segi *gas* dibandingkan `string` untuk menangani data teks, karena `string` di-encode dalam format UTF-8 sementara `bytes` adalah data mentah. Saat Kita mendeklarasikan variabel `bytes` dengan nilai teks, di belakang layar Solidity akan mengonversinya menjadi representasi heksadesimal.

    ```solidity
    bytes dynamicBytes = "Hello";
    ```

    Seperti yang ditunjukkan dalam buku, jika Kita memiliki dua variabel `string public myname1 = "Alexandros";` dan `bytes public myname2 = "Alexandros";`, outputnya akan berbeda. `myname1` akan mengembalikan "Alexandros", sedangkan `myname2` akan mengembalikan representasi *byte*-nya, yaitu `0x416c6578616e64726f73`.

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_4-12.png" alt="gambar" width="550"/>
</p>

[Perbandingan output antara variabel string dan bytes di Remix, satu menampilkan 'Alexandros' dan yang lainnya menampilkan kode heksadesimal. - Figure 4.12]

### Function Visibility Levels

**`Functions`** adalah blok kode yang dapat dieksekusi yang melakukan tugas tertentu. Mereka adalah "kata kerja" dalam bahasa Solidity.

#### Anatomi Fungsi

Sebuah deklarasi fungsi dasar di Solidity terlihat seperti ini:

```solidity
function helloWorld() public view returns (string memory) {}
```

  * **`function`**: *Keyword* yang memulai deklarasi fungsi.
  * **`helloWorld`**: Nama fungsi.
  * **`()`**: Tempat untuk mendefinisikan parameter (input) untuk fungsi.
  * **`public`**: Ini adalah **`visibility level`**, yang menentukan siapa yang dapat memanggil fungsi ini.
  * **`view`**: Ini adalah *state mutability modifier*. `view` berarti fungsi ini hanya "membaca" data dari *blockchain* dan tidak mengubahnya.
  * **`returns (string memory)`**: Mendeklarasikan tipe data output dari fungsi.
  * **`{}`**: Tubuh fungsi, tempat logika dieksekusi.

#### Tingkat Visibilitas (Visibility Levels)

Solidity memiliki empat tingkat visibilitas yang sangat penting untuk keamanan:

1.  **`public`**: Fungsi dapat dipanggil oleh siapa saja, baik dari dalam *contract* itu sendiri, dari *contract* turunan, maupun dari *transaction* eksternal.
2.  **`private`**: Fungsi hanya dapat dipanggil dari dalam *contract* tempat ia didefinisikan. *Contract* turunan tidak dapat memanggilnya.
3.  **`external`**: Fungsi hanya dapat dipanggil dari luar *contract* (melalui *transaction* atau *contract* lain). Mereka tidak dapat dipanggil secara internal (kecuali dengan sintaks khusus `this.functionName()`). Ini sering kali lebih efisien dari segi *gas* daripada `public`.
4.  **`internal`**: Mirip dengan `private`, tetapi fungsi juga dapat diakses oleh *contract* yang mewarisinya (*inheritance*).

#### Keyword `view` dan `pure`

  * **`view`**: Fungsi ini berjanji untuk tidak memodifikasi *state* *blockchain*. Ia hanya membaca data. Memanggil fungsi `view` secara eksternal tidak memerlukan *gas*.
  * **`pure`**: Fungsi ini lebih ketat lagi. Ia berjanji untuk tidak memodifikasi maupun membaca *state* *blockchain*. Logikanya hanya bergantung pada parameter inputnya. Contohnya adalah fungsi matematika murni.

### HelloWorld Contract

Sekarang, kita menggabungkan semua konsep ini untuk membuat *smart contract* "HelloWorld".

**Versi Pertama (Paling Sederhana)**
Versi ini menggunakan variabel `public` untuk secara otomatis membuat fungsi *getter*.

```solidity
//SPDX-License-Identifier: MIT
pragma solidity 0.8.25;

contract HelloWorld {
    string public helloWorld = "Hello World";
}
```

Ketika Kita mendeploy *contract* ini di Remix, sebuah tombol bernama `helloWorld` akan muncul secara otomatis. Jika Kita mengkliknya, itu akan mengembalikan nilai "Hello World".

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_4-14.png" alt="gambar" width="550"/>
</p>

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_4-15.png" alt="gambar" width="550"/>
</p>

[Tampilan contract HelloWorld yang telah di-deploy di Remix, dengan tombol biru 'helloWorld'. - Figure 4.14 & 4.15]

**Versi Kedua (Menggunakan Fungsi Eksplisit)**
Versi ini menunjukkan cara mencapai hasil yang sama dengan fungsi yang ditulis secara eksplisit.

```solidity
//SPDX-License-Identifier: MIT
pragma solidity 0.8.25;

contract HelloWorld {
    string helloWorld = "Hello World";

    function returnHelloWorld() public view returns (string memory) {
        return helloWorld;
    }
}
```

Di sini, kita membuat fungsi `returnHelloWorld` yang bersifat `public` dan `view`. Fungsi ini membaca nilai dari variabel `helloWorld` dan mengembalikannya. Keyword `memory` menandakan bahwa nilai *string* yang dikembalikan disimpan sementara di memori selama eksekusi. Konsep `memory` akan dijelaskan lebih lanjut di bab berikutnya.

---

# Bab 5
## Membangun Kontrak `ZooManagement`

Bab ini bertujuan untuk memperdalam pemahaman Anda tentang konsep pemrograman Solidity dengan menggunakan contoh praktis, yaitu kontrak `ZooManagement`. Kontrak ini dirancang untuk mengelola data di kebun binatang fiktif, seperti melacak jumlah pengunjung dan mengelola data hewan. Melalui bab ini, Anda akan mempelajari cara menggunakan `structs`, `mappings`, dan `arrays` untuk mengelola kumpulan data yang kompleks. Selain itu, bab ini juga akan memperkenalkan konsep *inheritance* (pewarisan), impor kontrak, serta praktik terbaik untuk efisiensi dan keamanan.

Tujuan utamanya adalah agar Anda dapat membangun sebuah kontrak yang canggih dan mampu menangani kasus penggunaan berbasis data di lingkungan yang terdesentralisasi.

## Mempersiapkan Kontrak `ZooManagement`

Seperti pada bab sebelumnya, kita akan menggunakan Remix IDE. Langkah pertama adalah membersihkan *workspace* dari file-file contoh dan membuat file baru bernama `ZooManagement.sol`.

### 1\. Inisialisasi Kontrak dan Pengelolaan Pengunjung

Kontrak kita dimulai dengan deklarasi lisensi dan versi Solidity, sama seperti praktik terbaik yang telah kita pelajari.

```solidity
//SPDX-License-Identifier: MIT
pragma solidity 0.8.26;

contract ZooManagement {
    // ... konten kontrak akan ditambahkan di sini
}
```

> **Catatan Penting tentang Versi `pragma`**: Buku ini mungkin menggunakan versi `0.8.25` atau `0.8.26`. Remix IDE secara *default* akan menggunakan *compiler* versi terbaru. Jika Kita melihat garis berlekuk-lekuk merah di bawah baris `pragma`, itu artinya versi *compiler* Kita tidak cocok. Kita bisa mengubah versi *compiler* di tab "Solidity Compiler" di Remix agar sesuai dengan yang ada di kode, atau, yang lebih disarankan, perbarui versi `pragma` di kode Kita ke versi terbaru yang didukung Remix. Bab ini menjelaskan secara detail cara mengatasi masalah ini, yang merupakan keterampilan praktis yang penting.

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_5-1.png" alt="gambar" width="550"/>
</p>

[Tangkapan layar antarmuka Remix IDE yang menunjukkan ikon Solidity Compiler di bilah sisi kiri. - Figure 5.1]

#### **Variabel dan Fungsi Awal**

Kontrak ini pertama-tama akan mengelola jumlah total pengunjung. Untuk itu, kita mendeklarasikan sebuah variabel *state* dan dua fungsi: satu untuk memperbarui jumlah pengunjung dan satu lagi untuk mengambilnya.

```solidity
contract ZooManagement {
    uint256 public totalVisitors; 

    function updateVisitorCount(uint256 _newVisitorCount) public {
        totalVisitors = _newVisitorCount;
    }
 
    function getTotalVisitors() public view returns(uint256) {
        return totalVisitors;
    }
}
```

Mari kita bedah kode ini:

  * `uint256 public totalVisitors;`: Kita mendeklarasikan sebuah *state variable* (variabel yang statusnya disimpan secara permanen di *blockchain*) bernama `totalVisitors` dengan tipe `uint256`. *Keyword* `public` secara otomatis membuat sebuah fungsi *getter* dengan nama yang sama (`totalVisitors()`), sehingga kita bisa membaca nilainya dari luar kontrak.
  * `function updateVisitorCount(uint256 _newVisitorCount) public`: Ini adalah fungsi untuk mengubah nilai `totalVisitors`.
      * Fungsi ini `public`, artinya bisa dipanggil oleh siapa saja (baik dari luar *blockchain* maupun oleh kontrak lain).
      * Fungsi ini menerima satu parameter, `_newVisitorCount`, yang merupakan jumlah pengunjung baru.
      * Di dalam fungsi, `totalVisitors = _newVisitorCount;` adalah operasi penugasan (*assignment*) yang mengubah status variabel `totalVisitors`. Karena operasi ini mengubah *state* *blockchain*, eksekusinya akan memerlukan *gas fee*.
  * `function getTotalVisitors() public view returns(uint256)`: Fungsi ini digunakan untuk membaca nilai `totalVisitors`.
      * *Keyword* `view` sangat penting di sini. Ini menandakan bahwa fungsi ini hanya "melihat" atau membaca data dari *blockchain* dan tidak mengubah *state* apa pun. Akibatnya, memanggil fungsi `view` dari luar *blockchain* (misalnya dari DApp) tidak memerlukan *gas fee*.
      * `returns(uint256)` mendeklarasikan bahwa fungsi ini akan mengembalikan sebuah nilai bertipe `uint256`.

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_5-7.png" alt="gambar" width="550"/>
</p>

[Tangkapan layar antarmuka Remix setelah kontrak di-deploy, menunjukkan tombol untuk fungsi updateVisitorCount, getTotalVisitors, dan totalVisitors. - Figure 5.7]

Ketika kontrak ini di-*deploy*, kita bisa memasukkan angka (misalnya `10`) ke dalam fungsi `updateVisitorCount`, dan kemudian memanggil `getTotalVisitors` atau `totalVisitors` untuk melihat bahwa nilainya telah berubah menjadi `10`.

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_5-9.png" alt="gambar" width="550"/>
</p>

[Tangkapan layar hasil di Remix setelah memasukkan nilai 10 ke updateVisitorCount dan memanggil getTotalVisitors, yang menunjukkan output 10. - Figure 5.9]

## `Structs` - Mengelompokkan Data Terstruktur

Sejauh ini kita hanya menyimpan satu jenis data (jumlah pengunjung). Bagaimana jika kita ingin menyimpan informasi yang lebih kompleks, seperti data hewan yang memiliki beberapa atribut (spesies, nama, umur)? Di sinilah `struct` berperan.

**Struct** (kependekan dari *structure*) adalah tipe data kustom yang memungkinkan kita untuk mengelompokkan beberapa variabel yang berbeda tipe di bawah satu nama. Ini sangat berguna untuk merepresentasikan objek dunia nyata.

```solidity
// SPDX-License-Identifier: MIT
pragma solidity 0.8.26;

contract ZooManagement {
    uint256 public totalVisitors; 
    
    struct Animal {
        string species;
        string name;
        uint256 age;
    }
 
    Animal public tiger = Animal("Tiger", "Peanut", 3);
    Animal public bear = Animal("Bear", "Honey", 4);
    Animal public lion = Animal("Lion", "Simba", 8); // Seharusnya "Lion", bukan "Animal"
 
    function updateVisitorCount(uint256 _newVisitorCount) public {
        totalVisitors = _newVisitorCount;
    }
 
    function getTotalVisitors() public view returns(uint256) {
        return totalVisitors;
    }
}
```

> **Perbaikan Kode**: Dalam buku, contoh untuk `lion` salah memasukkan `"Animal"` sebagai spesies. Seharusnya `"Lion"`. Versi di atas sudah diperbaiki untuk kejelasan.
> `Animal public lion = Animal("Lion", "Simba", 8);`

Analisis kode baru:

  * `struct Animal { ... }`: Kita mendefinisikan sebuah `struct` baru bernama `Animal`. Di dalamnya, kita mendeklarasikan tiga "kolom" atau *field*: `species` (string), `name` (string), dan `age` (uint256).
  * `Animal public tiger = Animal("Tiger", "Peanut", 3);`: Ini adalah cara kita membuat sebuah *instance* (contoh nyata) dari `struct` `Animal`.
      * `Animal public tiger`: Kita mendeklarasikan variabel publik bernama `tiger` yang tipenya adalah `Animal`.
      * `= Animal("Tiger", "Peanut", 3)`: Kita menginisialisasi variabel ini dengan nilai-nilai yang sesuai dengan urutan *field* di dalam `struct`: spesiesnya "Tiger", namanya "Peanut", dan umurnya 3.

Setelah di-*deploy*, akan muncul tombol-tombol baru untuk `tiger`, `bear`, dan `lion`. Ketika diklik, mereka akan mengembalikan semua data yang terkait dengan hewan tersebut secara terstruktur.

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_5-12.png" alt="gambar" width="550"/>
</p>

[Tangkapan layar Remix menunjukkan hasil pemanggilan variabel struct 'bear', 'lion', dan 'tiger', yang menampilkan semua field dan nilainya. - Figure 5.12]

## `Arrays` - Mengelola Daftar Data

Mendeklarasikan setiap hewan sebagai variabel terpisah tidak efisien jika kita memiliki ratusan hewan. Solusinya adalah menggunakan **array**. *Array* adalah struktur data yang dapat menyimpan daftar nilai dengan tipe yang sama.

Solidity mendukung dua jenis *array*:

1.  **Dynamic Arrays**: Ukurannya tidak ditentukan di awal dan bisa bertambah seiring waktu.
2.  **Fixed-Size Arrays**: Ukurannya ditentukan saat deklarasi dan tidak bisa diubah.

### 1\. Dynamic Arrays

*Dynamic array* lebih fleksibel tetapi bisa lebih mahal dari segi *gas* karena ukurannya yang bisa berubah.

```solidity
// Kode sebelumnya ...
struct Animal {
    string species;
    string name;
    uint256 age;
}
 
Animal[] public listofAnimals; // Deklarasi Dynamic Array

// Hapus deklarasi tiger, bear, lion yang individual

function addAnimal(string memory _species, string memory _name, uint256 _age) public {
    listofAnimals.push(Animal(_species, _name, _age));
}

// ... sisa fungsi lainnya
```

Pembahasan:

  * `Animal[] public listofAnimals;`: Kita mendeklarasikan sebuah *dynamic array* publik bernama `listofAnimals`. Tanda `[]` tanpa angka di dalamnya menandakan bahwa ini adalah *dynamic array*. Tipe data elemen di dalamnya adalah `Animal` (struct yang kita buat).
  * `function addAnimal(...)`: Fungsi ini sekarang digunakan untuk menambahkan hewan baru ke dalam daftar.
  * `listofAnimals.push(Animal(_species, _name, _age));`: Ini adalah bagian kuncinya.
      * `Animal(_species, _name, _age)`: Pertama, kita membuat *instance* `Animal` baru secara sementara (*in-memory*).
      * `.push(...)`: Kemudian, kita menggunakan metode `.push()` untuk menambahkan *instance* baru ini ke akhir dari *array* `listofAnimals`.

### 2\. Fixed-Size Arrays

Jika kita tahu persis berapa banyak hewan yang akan ada di kebun binatang (misalnya, hanya 3), kita bisa menggunakan *fixed-size array* untuk menghemat *gas*.

```solidity
// ...
struct Animal {
    string species;
    string name;
    uint256 age;
}
 
Animal[3] public listofAnimals; // Deklarasi Fixed-Size Array untuk 3 hewan
uint256 public animalCount; // Helper untuk melacak indeks

// ... fungsi lainnya ...

function addAnimal(string memory _species, string memory _name, uint256 _age) public {
    require(animalCount < 3, "Zoo is full");
 
    listofAnimals[animalCount] = Animal(_species, _name, _age);
 
    animalCount++;
}

function getAnimal(uint256 _index) public view returns (string memory, string memory, uint256) {
    require(_index < animalCount, "Animal does not exist");
 
    Animal memory animal = listofAnimals[_index];
 
    return (animal.species, animal.name, animal.age);
}
```

Analisis:

  * `Animal[3] public listofAnimals;`: Tanda `[3]` mendefinisikan bahwa *array* ini hanya bisa menampung 3 elemen.
  * `require(animalCount < 3, "Zoo is full");`: Ini adalah sebuah *check* keamanan yang sangat penting. `require` akan memeriksa kondisi di dalamnya. Jika `false`, eksekusi akan berhenti (revert) dan menampilkan pesan error. Ini memastikan kita tidak mencoba menambahkan hewan keempat ke dalam *array* yang hanya berkapasitas tiga.
  * `listofAnimals[animalCount] = ...`: Kita tidak lagi menggunakan `.push()`. Sebaliknya, kita mengakses elemen *array* berdasarkan indeksnya (`animalCount`) dan menugaskan nilainya.
  * `animalCount++;`: Setelah menambahkan hewan, kita menaikkan penghitung agar hewan berikutnya ditambahkan di indeks selanjutnya.
  * `function getAnimal(...)`: Fungsi ini memungkinkan kita untuk mengambil data hewan berdasarkan indeksnya. Ini juga menggunakan `require` untuk memastikan kita tidak mencoba mengakses indeks yang tidak ada.

## `Mappings` - Pencarian Data Efisien dengan Key-Value

*Array* bagus untuk menyimpan daftar, tetapi tidak efisien untuk mencari item tertentu. Jika kita ingin menemukan hewan dengan nama "Simba" di dalam *array* yang berisi 1000 hewan, kita harus mengulang (*iterate*) satu per satu. Di sinilah **mapping** bersinar.

**Mapping** adalah struktur data *key-value* (kunci-nilai), mirip seperti kamus atau *hash table*. Kita menyediakan sebuah "kunci" unik, dan *mapping* akan langsung mengembalikan "nilai" yang terkait. Pencarian ini sangat efisien (*O(1)*), artinya biayanya tetap, tidak peduli seberapa banyak data yang disimpan.

Mari kita modifikasi kontrak *dynamic array* kita untuk menambahkan *mapping*.

```solidity
// ...
struct Animal {
    string species;
    string name;
    uint256 age;
}
 
Animal[] public listofAnimals;
 
mapping (string => uint256) public nameToAge; // Deklarasi Mapping

// ... fungsi lainnya ...

function addAnimal(string memory _species, string memory _name, uint256 _age) public {
    listofAnimals.push(Animal(_species, _name, _age));
    nameToAge[_name] = _age; // Menambahkan data ke mapping
}
```

Pembahasan:

  * `mapping (string => uint256) public nameToAge;`:
      * `mapping`: *Keyword* untuk deklarasi.
      * `(string => uint256)`: Mendefinisikan tipe data. `string` adalah tipe untuk **kunci** (dalam hal ini, nama hewan), dan `uint256` adalah tipe untuk **nilai** (umur hewan).
      * `public nameToAge`: Mendeklarasikan *mapping* publik bernama `nameToAge`.
  * `nameToAge[_name] = _age;`: Di dalam fungsi `addAnimal`, setelah menambahkan hewan ke *array*, kita juga menambahkan entri ke *mapping*. Kita menggunakan nama hewan (`_name`) sebagai kunci dan umurnya (`_age`) sebagai nilai.

Sekarang, setelah di-*deploy*, akan ada fungsi baru `nameToAge`. Jika kita memasukkan "Simba" sebagai input, fungsi tersebut akan langsung mengembalikan `8` tanpa perlu mencari di seluruh *array*.
<p align="center">
  <img src="images/books-04_beginning_solidity/figure_5-15.png" alt="gambar" width="550"/>
</p>

[Tangkapan layar Remix menunjukkan pemanggilan mapping 'nameToAge' dengan input "Simba" dan hasilnya adalah "8". - Figure 5.15]

Bab ini juga menunjukkan bagaimana kita bisa membuat beberapa *mapping* untuk menghubungkan berbagai atribut, misalnya `speciesToName`, `ageToName`, dll.

## `Contract Importing` - Menggunakan Kode dari File Lain

Seiring bertambahnya kompleksitas, menyimpan semua kode dalam satu file menjadi tidak praktis. Solidity memungkinkan kita untuk memisahkan kontrak ke dalam beberapa file dan mengimpornya saat dibutuhkan.

**Importing** adalah proses memuat definisi kontrak dari file lain agar bisa digunakan di file saat ini.

```solidity
// Di file ContractInheritance.sol
import {ZooManagement} from "./ZooManagement.sol"; // Impor kontrak
```

Pembahasan Sintaks:

  * `import {ZooManagement} ...`: Kita memberitahu *compiler* bahwa kita ingin mengimpor kontrak spesifik bernama `ZooManagement`.
  * `from "./ZooManagement.sol";`: Kita menunjukkan lokasi file tempat kontrak tersebut didefinisikan.
      * `./`: Menandakan direktori saat ini.
      * `../`: Menandakan direktori induk (satu tingkat di atas).
      * `NamaFolder/NamaFile.sol`: Menandakan file berada di dalam sub-folder.

Bab ini memberikan contoh yang sangat baik tentang bagaimana path ini berubah tergantung pada lokasi file, sebuah konsep yang sangat penting untuk dipahami saat bekerja dengan proyek yang lebih besar.

## `Inheritance` - Mewarisi Sifat dari Kontrak Lain

**Inheritance** (Pewarisan) adalah mekanisme di mana sebuah kontrak (*child contract*) dapat mewarisi fungsi, variabel, dan *modifier* dari kontrak lain (*parent contract*). Ini adalah pilar dari *Object-Oriented Programming* (OOP) dan sangat berguna untuk penggunaan ulang kode (*code reusability*) dan menciptakan hierarki kontrak.

#### **Tipe-tipe Inheritance**

1.  **Single Inheritance**: Satu *child* mewarisi dari satu *parent*.

    ```solidity
    contract AddSubtractiontoAdditionContract is CreateNumber {
        // ...
    }
    ```

      * *Keyword* `is` digunakan untuk menandakan pewarisan.

2.  **Multilevel Inheritance**: Sebuah rantai pewarisan (C mewarisi dari B, B mewarisi dari A).

    ```solidity
    contract CreateNumber { /* ... */ } // Grandparent
    contract SubtractionContract is CreateNumber { /* ... */ } // Parent
    contract AdditionContract is SubtractionContract { /* ... */ } // Child
    ```

3.  **Multiple Inheritance**: Satu *child* mewarisi dari beberapa *parent*.

    ```solidity
    contract Contract3 is Contract1, Contract2 {
        // ...
    }
    ```

4.  **Hierarchical Inheritance**: Beberapa *child* mewarisi dari satu *parent* yang sama.

    ```solidity
    contract Contract1 { /* ... */ } // Parent
    contract Contract2 is Contract1 { /* ... */ } // Child 1
    contract Contract3 is Contract1 { /* ... */ } // Child 2
    ```

<p align="center">
  <img src="images/books-04_beginning_solidity/figure_5-30.png" alt="gambar" width="550"/>
</p>

[Diagram yang mengilustrasikan empat jenis inheritance: Single, Multilevel, Multiple, dan Hierarchical. - Figure 5.30]

#### **Keyword `virtual` dan `override`**

Ini adalah konsep yang sangat penting. Jika sebuah fungsi di *parent contract* akan diubah perilakunya di *child contract*, maka:

  * Fungsi di **parent contract** harus ditandai dengan *keyword* `virtual`.
  * Fungsi di **child contract** harus ditandai dengan *keyword* `override`.

<!-- end list -->

```solidity
// Parent Contract
contract CreateNumber {
    function addNumber(uint256 _number) public virtual { // Ditandai virtual
        // ...
    }
}

// Child Contract
contract AddSubtractiontoAdditionContract is CreateNumber {
    function addNumber(uint256 _newnumber) public override { // Ditandai override
        // ...
    }
}
```

Jika aturan ini tidak diikuti, *compiler* akan memberikan *error*. Ini adalah mekanisme keamanan untuk memastikan bahwa pengembang sadar ketika mereka mengubah perilaku fungsi yang diwarisi.

## Menerapkan dan Menjalankan Kontrak dari Kontrak Lain (Pola *Factory*)

Terkadang, kita membutuhkan sebuah kontrak yang tugasnya adalah men-*deploy* atau membuat *instance* dari kontrak lain. Pola ini disebut **Factory Pattern**.

```solidity
// File: ZooManagementFactory.sol
import {ZooManagement} from "./ZooManagement.sol";

contract ZooManagementFactory {
    ZooManagement[] public listOfZooManagementContracts;

    function deployZooManagement() public {
        ZooManagement newZooManagement = new ZooManagement();
        listOfZooManagementContracts.push(newZooManagement);
    }
    
    function fUpdateVisitorCount(uint256 _zooManagementContractIndex, uint256 _myNewVisitorCount) public {
        ZooManagement myNewZooManagement = listOfZooManagementContracts[_zooManagementContractIndex];
        myNewZooManagement.updateVisitorCount(_myNewVisitorCount);
    }
    
    function fGetTotalVisitors(uint256 _zooManagementContractIndex) public view returns (uint256) {
        ZooManagement myNewZooManagement = listOfZooManagementContracts[_zooManagementContractIndex];
        return myNewZooManagement.getTotalVisitors();
    }
}
```

Analisis Kode *Factory*:

1.  `ZooManagement[] public listOfZooManagementContracts;`: Kita membuat sebuah *array* untuk menyimpan alamat dari semua kontrak `ZooManagement` yang telah di-*deploy* oleh *factory* ini. Ini sangat penting untuk melacak kontrak-kontrak yang telah dibuat.
2.  `ZooManagement newZooManagement = new ZooManagement();`: *Keyword* `new` digunakan untuk men-*deploy* sebuah *instance* baru dari kontrak `ZooManagement`. Operasi ini mengembalikan alamat dari kontrak yang baru dibuat.
3.  `listOfZooManagementContracts.push(newZooManagement);`: Kita menyimpan alamat kontrak baru tersebut ke dalam *array* kita.
4.  `fUpdateVisitorCount` dan `fGetTotalVisitors`: Ini adalah contoh fungsi "proxy". *Factory* ini dapat berinteraksi dengan kontrak-kontrak yang telah dibuatnya.
      * Pertama, ia mengambil alamat kontrak target dari *array* berdasarkan indeksnya (`listOfZooManagementContracts[_zooManagementContractIndex]`).
      * Kemudian, ia memanggil fungsi yang sesuai (`updateVisitorCount` atau `getTotalVisitors`) pada alamat kontrak tersebut.

Pola *factory* sangat kuat dan umum digunakan untuk mengelola ekosistem kontrak yang saling terkait.

### Kesimpulan Bab 5

Kita telah belajar bagaimana mengelola data yang lebih kompleks menggunakan **structs**, **arrays** (baik dinamis maupun tetap), dan **mappings**. Kita juga telah memahami dua konsep fundamental dalam arsitektur perangkat lunak Solidity: **importing** untuk modularitas dan **inheritance** (beserta `virtual` dan `override`) untuk penggunaan ulang kode. Terakhir, Kita diperkenalkan pada **pola factory**, sebuah teknik canggih untuk mengelola siklus hidup kontrak.

---

