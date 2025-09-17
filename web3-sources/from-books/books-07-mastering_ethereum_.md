### **Glosarium Singkat**

Glosarium singkat ini berisi banyak istilah yang digunakan dalam kaitannya dengan Ethereum. Istilah-istilah ini digunakan di seluruh buku, jadi tandai halaman ini untuk referensi cepat.

**Account (Akun)**
Sebuah objek yang berisi alamat, saldo, *nonce*, serta penyimpanan dan kode opsional. Sebuah akun dapat berupa akun kontrak atau *externally owned account* (EOA).

**Address (Alamat)**
Secara umum, ini mewakili sebuah EOA atau kontrak yang dapat menerima (alamat tujuan) atau mengirim (alamat sumber) transaksi di *blockchain*. Lebih spesifiknya, ini adalah 160 bit paling kanan dari *hash* Keccak sebuah *public key* ECDSA.

**Assert**
Di Solidity, `assert(false)` dikompilasi menjadi `0xfe`, sebuah *opcode* yang tidak valid, yang akan menghabiskan semua sisa *gas* dan mengembalikan semua perubahan. Ketika pernyataan `assert()` gagal, sesuatu yang sangat salah dan tidak terduga sedang terjadi, dan Anda perlu memperbaiki kode Anda. Anda harus menggunakan `assert()` untuk menghindari kondisi yang seharusnya tidak pernah terjadi.

**Big-endian**
Sebuah representasi bilangan posisional di mana digit paling signifikan berada di urutan pertama. Kebalikan dari *little-endian*, di mana digit paling tidak signifikan berada di urutan pertama.

**BIPs**
*Bitcoin Improvement Proposals* (Proposal Peningkatan Bitcoin). Satu set proposal yang diajukan oleh anggota komunitas Bitcoin untuk meningkatkan Bitcoin. Sebagai contoh, BIP-21 adalah proposal untuk meningkatkan skema *uniform resource identifier* (URI) Bitcoin.

**Block (Blok)**
Kumpulan informasi yang diperlukan (*block header*) tentang transaksi-transaksi yang terkandung di dalamnya, dan satu set *block header* lain yang dikenal sebagai *ommers*. Blok ditambahkan ke jaringan Ethereum oleh para penambang (*miner*).

**Blockchain**
Di Ethereum, sebuah urutan blok yang divalidasi oleh sistem *proof-of-work*, di mana setiap blok terhubung ke pendahulunya hingga ke *genesis block*. Ini berbeda dari protokol Bitcoin karena tidak memiliki batas ukuran blok; sebaliknya, Ethereum menggunakan batas *gas* yang bervariasi.

**Bytecode**
Sebuah set instruksi abstrak yang dirancang untuk eksekusi efisien oleh interpreter perangkat lunak atau mesin virtual. Berbeda dengan kode sumber yang dapat dibaca manusia, *bytecode* diekspresikan dalam format numerik.

**Byzantium fork**
Yang pertama dari dua *hard fork* untuk tahap pengembangan Metropolis. Ini termasuk EIP-649: Penundaan *Difficulty Bomb* Metropolis dan Pengurangan Hadiah Blok, di mana *Ice Age* (lihat di bawah) ditunda selama 1 tahun dan hadiah blok dikurangi dari 5 menjadi 3 ether.

**Compiling (Kompilasi)**
Mengubah kode yang ditulis dalam bahasa pemrograman tingkat tinggi (misalnya, Solidity) menjadi bahasa tingkat lebih rendah (misalnya, *bytecode* EVM).

**Consensus (Konsensus)**
Ketika banyak *node*—biasanya sebagian besar *node* di jaringan—semuanya memiliki blok yang sama dalam *blockchain* terbaik yang telah mereka validasi secara lokal. Jangan disamakan dengan aturan konsensus.

**Consensus rules (Aturan Konsensus)**
Aturan validasi blok yang diikuti oleh *full node* untuk tetap berada dalam konsensus dengan *node* lain. Jangan disamakan dengan konsensus.

**Constantinople fork**
Bagian kedua dari tahap Metropolis, yang awalnya direncanakan untuk pertengahan 2018. Diharapkan akan mencakup peralihan ke algoritma konsensus hibrida *proof-of-work*/*proof-of-stake*, di antara perubahan lainnya.

**Contract account (Akun Kontrak)**
Sebuah akun yang berisi kode yang dieksekusi setiap kali menerima transaksi dari akun lain (EOA atau kontrak).

**Contract creation transaction (Transaksi Pembuatan Kontrak)**
Sebuah transaksi khusus, dengan "alamat nol" sebagai penerimanya, yang digunakan untuk mendaftarkan kontrak dan mencatatnya di *blockchain* Ethereum (lihat "zero address").

**DAO**
*Decentralized Autonomous Organization* (Organisasi Otonom Terdesentralisasi). Sebuah perusahaan atau organisasi lain yang beroperasi tanpa manajemen hierarkis. Juga dapat merujuk pada sebuah kontrak bernama "The DAO" yang diluncurkan pada 30 April 2016, yang kemudian diretas pada Juni 2016; ini pada akhirnya memotivasi sebuah *hard fork* (dengan nama kode DAO) di blok \#1.192.000, yang membalikkan kontrak DAO yang diretas dan menyebabkan Ethereum dan Ethereum Classic terpecah menjadi dua sistem yang bersaing.

**DApp**
*Decentralized application* (Aplikasi Terdesentralisasi). Minimal, ini adalah sebuah *smart contract* dan antarmuka pengguna web. Secara lebih luas, DApp adalah aplikasi web yang dibangun di atas layanan infrastruktur *peer-to-peer* yang terbuka dan terdesentralisasi. Selain itu, banyak DApp menyertakan penyimpanan terdesentralisasi dan/atau protokol dan platform pesan.

**Deed (Akta)**
Standar *non-fungible token* (NFT) yang diperkenalkan oleh proposal ERC721. Berbeda dengan token ERC20, *deed* membuktikan kepemilikan dan tidak dapat dipertukarkan, meskipun tidak diakui sebagai dokumen legal di yurisdiksi mana pun—setidaknya untuk saat ini (lihat juga "NFT").

**Difficulty (Tingkat Kesulitan)**
Pengaturan di seluruh jaringan yang mengontrol seberapa banyak komputasi yang diperlukan untuk menghasilkan sebuah *proof of work*.

**Digital signature (Tanda Tangan Digital)**
Sebuah string data pendek yang dihasilkan pengguna untuk sebuah dokumen menggunakan *private key* sedemikian rupa sehingga siapa pun dengan *public key* yang sesuai, tanda tangan, dan dokumen tersebut dapat memverifikasi bahwa (1) dokumen itu "ditandatangani" oleh pemilik *private key* tersebut, dan (2) dokumen tidak diubah setelah ditandatangani.

**ECDSA**
*Elliptic Curve Digital Signature Algorithm*. Sebuah algoritma kriptografi yang digunakan oleh Ethereum untuk memastikan bahwa dana hanya dapat dibelanjakan oleh pemiliknya.

**EIP**
*Ethereum Improvement Proposal* (Proposal Peningkatan Ethereum). Sebuah dokumen desain yang memberikan informasi kepada komunitas Ethereum, menjelaskan fitur baru yang diusulkan atau proses atau lingkungannya. Untuk informasi lebih lanjut, lihat [https://github.com/ethereum/EIPs](https://github.com/ethereum/EIPs) (lihat juga "ERC").

**ENS**
*Ethereum Name Service*. Untuk informasi lebih lanjut, lihat [https://github.com/ethereum/ens/](https://github.com/ethereum/ens/).

**Entropy (Entropi)**
Dalam konteks kriptografi, kurangnya prediktabilitas atau tingkat keacakan. Saat menghasilkan informasi rahasia, seperti *private key*, algoritma biasanya mengandalkan sumber entropi yang tinggi untuk memastikan hasilnya tidak dapat diprediksi.

**EOA**
*Externally Owned Account* (Akun yang Dimiliki Secara Eksternal). Sebuah akun yang dibuat oleh atau untuk pengguna manusia di jaringan Ethereum.

**ERC**
*Ethereum Request for Comments* (Permintaan Komentar Ethereum). Sebuah label yang diberikan pada beberapa EIP yang mencoba mendefinisikan standar penggunaan Ethereum tertentu.

**Ethash**
Sebuah algoritma *proof-of-work* untuk Ethereum 1.0. Untuk informasi lebih lanjut, lihat [https://github.com/ethereum/wiki/wiki/Ethash](https://www.google.com/search?q=https://github.com/ethereum/wiki/wiki/Ethash).

**Ether**
Mata uang kripto asli yang digunakan oleh ekosistem Ethereum, yang menutupi biaya *gas* saat mengeksekusi *smart contract*. Simbolnya adalah Ξ, karakter Xi huruf besar Yunani.

**Event (Peristiwa)**
Memungkinkan penggunaan fasilitas pencatatan (*logging*) EVM. DApp dapat mendengarkan *event* dan menggunakannya untuk memicu *callback* JavaScript di antarmuka pengguna. Untuk informasi lebih lanjut, lihat [http://solidity.readthedocs.io/en/develop/contracts.html\#events](http://solidity.readthedocs.io/en/develop/contracts.html#events).

**EVM**
*Ethereum Virtual Machine* (Mesin Virtual Ethereum). Sebuah mesin virtual berbasis tumpukan (*stack-based*) yang mengeksekusi *bytecode*. Di Ethereum, model eksekusi menentukan bagaimana keadaan sistem diubah berdasarkan serangkaian instruksi *bytecode* dan sebuah tupel kecil data lingkungan. Ini dispesifikasikan melalui model formal dari mesin keadaan virtual.

**EVM assembly language (Bahasa rakitan EVM)**
Bentuk *bytecode* EVM yang dapat dibaca manusia.

**Fallback function (Fungsi fallback)**
Fungsi default yang dipanggil jika tidak ada data atau nama fungsi yang dideklarasikan.

**Faucet**
Sebuah layanan yang memberikan dana dalam bentuk ether uji coba gratis yang dapat digunakan di *testnet*.

**Finney**
Sebuah denominasi ether. `$10^{15}$` finney = 1 ether.

**Fork**
Perubahan dalam protokol yang menyebabkan terciptanya rantai alternatif, atau divergensi sementara dalam dua jalur blok potensial selama penambangan.

**Frontier**
Tahap pengembangan uji coba awal Ethereum, yang berlangsung dari Juli 2015 hingga Maret 2016.

**Ganache**
Sebuah *blockchain* Ethereum pribadi yang dapat Anda gunakan untuk menjalankan tes, mengeksekusi perintah, dan memeriksa keadaan sambil mengontrol cara kerja rantai tersebut.

**Gas**
Bahan bakar virtual yang digunakan di Ethereum untuk mengeksekusi *smart contract*. EVM menggunakan mekanisme akuntansi untuk mengukur konsumsi *gas* dan membatasi konsumsi sumber daya komputasi (lihat "Turing complete").

**Gas limit (Batas gas)**
Jumlah maksimum *gas* yang dapat dikonsumsi oleh sebuah transaksi atau blok.

**Gavin Wood**
Seorang programmer Inggris yang merupakan salah satu pendiri dan mantan CTO Ethereum. Pada Agustus 2014, ia mengusulkan Solidity, sebuah bahasa pemrograman berorientasi kontrak untuk menulis *smart contract*.

**Genesis block (Blok Genesis)**
Blok pertama dalam sebuah *blockchain*, digunakan untuk menginisialisasi jaringan tertentu dan mata uang kriptonya.

**Geth**
Go Ethereum. Salah satu implementasi paling terkemuka dari protokol Ethereum, yang ditulis dalam bahasa Go.

**Hard fork**
Sebuah divergensi permanen dalam *blockchain*; juga dikenal sebagai perubahan yang menyebabkan *hard-forking*. Hal ini biasa terjadi ketika *node* yang belum ditingkatkan tidak dapat memvalidasi blok yang dibuat oleh *node* yang sudah ditingkatkan yang mengikuti aturan konsensus yang lebih baru. Jangan disamakan dengan *fork*, *soft fork*, *software fork*, atau *Git fork*.

**Hash**
Sebuah sidik jari dengan panjang tetap dari input berukuran variabel, yang dihasilkan oleh fungsi *hash*.

**HD wallet**
Dompet yang menggunakan protokol pembuatan dan transfer kunci deterministik hierarkis (HD) (BIP-32).

**HD wallet seed**
Sebuah nilai yang digunakan untuk menghasilkan *master private key* dan *master chain code* untuk sebuah dompet HD. *Wallet seed* dapat direpresentasikan oleh kata-kata mnemonik, membuatnya lebih mudah bagi manusia untuk menyalin, mencadangkan, dan memulihkan *private key*.

**Homestead**
Tahap pengembangan kedua Ethereum, diluncurkan pada Maret 2016 di blok \#1.150.000.

**ICAP**
*Inter-exchange Client Address Protocol*. Sebuah pengkodean alamat Ethereum yang sebagian kompatibel dengan pengkodean *International Bank Account Number* (IBAN), menawarkan pengkodean yang serbaguna, memiliki *checksum*, dan dapat dioperasikan untuk alamat Ethereum. Alamat ICAP menggunakan kode negara semu IBAN baru: XE, yang merupakan singkatan dari "eXtended Ethereum," seperti yang digunakan pada mata uang non-yurisdiksi (misalnya, XBT, XRP, XCP).

**Ice Age**
Sebuah *hard fork* Ethereum di blok \#200.000 untuk memperkenalkan peningkatan kesulitan eksponensial (alias *Difficulty Bomb*), yang memotivasi transisi ke *proof of stake*.

**IDE**
*Integrated Development Environment* (Lingkungan Pengembangan Terintegrasi). Sebuah antarmuka pengguna yang biasanya menggabungkan editor kode, *compiler*, *runtime*, dan *debugger*.

**Immutable deployed code problem (Masalah kode yang tidak dapat diubah setelah dideploy)**
Setelah kode sebuah kontrak (atau *library*) di-*deploy*, kode tersebut menjadi tidak dapat diubah (*immutable*). Praktik pengembangan perangkat lunak standar bergantung pada kemampuan untuk memperbaiki kemungkinan *bug* dan menambahkan fitur baru, sehingga ini menjadi tantangan bagi pengembangan *smart contract*.

**Internal transaction (juga "message") (Transaksi Internal atau "pesan")**
Sebuah transaksi yang dikirim dari akun kontrak ke akun kontrak lain atau ke sebuah EOA.

**IPFS**
*InterPlanetary File System*. Sebuah protokol, jaringan, dan proyek sumber terbuka yang dirancang untuk menciptakan metode penyimpanan dan berbagi hipermedia yang dapat dialamatkan berdasarkan konten dan secara *peer-to-peer* dalam sebuah sistem file terdistribusi.

**KDF**
*Key Derivation Function*. Juga dikenal sebagai "algoritma peregangan kata sandi," digunakan oleh format *keystore* untuk melindungi dari serangan *brute-force*, kamus, dan *rainbow table* pada enkripsi *passphrase*, dengan cara melakukan *hashing* berulang kali pada *passphrase*.

**Keccak-256**
Fungsi *hash* kriptografi yang digunakan di Ethereum. Keccak-256 distandarisasi sebagai SHA-3.

**Keystore file (File Keystore)**
Sebuah file berenkode JSON yang berisi satu *private key* (yang dibuat secara acak), dienkripsi dengan sebuah *passphrase* untuk keamanan tambahan.

**LevelDB**
Penyimpanan nilai-kunci (*key-value*) on-disk sumber terbuka, diimplementasikan sebagai pustaka ringan untuk satu tujuan, dengan *binding* ke banyak platform.

**Library (Pustaka)**
Jenis kontrak khusus yang tidak memiliki fungsi *payable*, tidak memiliki fungsi *fallback*, dan tidak ada penyimpanan data. Oleh karena itu, ia tidak dapat menerima atau menampung ether, atau menyimpan data. Sebuah *library* berfungsi sebagai kode yang sudah di-*deploy* sebelumnya yang dapat dipanggil oleh kontrak lain untuk komputasi *read-only*.

**Lightweight client (Klien Ringan)**
Klien Ethereum yang tidak menyimpan salinan lokal dari *blockchain*, atau memvalidasi blok dan transaksi. Klien ini menawarkan fungsi dompet dan dapat membuat serta menyiarkan transaksi.

**Merkle Patricia Tree**
Struktur data yang digunakan di Ethereum untuk menyimpan pasangan kunci-nilai (*key-value pairs*) secara efisien.

**Message (Pesan)**
Transaksi internal yang tidak pernah diserialisasi dan hanya dikirim di dalam EVM.

**Message call (Panggilan pesan)**
Tindakan mengirimkan pesan dari satu akun ke akun lain. Jika akun tujuan terkait dengan kode EVM, maka VM akan dimulai dengan keadaan objek tersebut dan pesan akan ditindaklanjuti.

**METoken**
*Mastering Ethereum Token*. Sebuah token ERC20 yang digunakan untuk demonstrasi dalam buku ini.

**Metropolis**
Tahap pengembangan ketiga Ethereum, diluncurkan pada Oktober 2017.

**Miner (Penambang)**
Sebuah *node* jaringan yang menemukan *proof of work* yang valid untuk blok baru, melalui *hashing* berulang.

**Mist**
Browser pertama yang mendukung Ethereum, dibuat oleh Ethereum Foundation. Ini berisi dompet berbasis browser yang merupakan implementasi pertama dari standar token ERC20 (Fabian Vogelsteller, penulis ERC20, juga merupakan pengembang utama Mist). Mist juga merupakan dompet pertama yang memperkenalkan *checksum* camelCase (EIP-55; lihat "Hex Encoding with Checksum in Capitalization (EIP-55)" di halaman 76). Mist menjalankan *full node* dan menawarkan browser DApp penuh dengan dukungan untuk penyimpanan berbasis Swarm dan alamat ENS.

**Network (Jaringan)**
Merujuk pada jaringan Ethereum, sebuah jaringan *peer-to-peer* yang menyebarkan transaksi dan blok ke setiap *node* Ethereum (peserta jaringan).

**NFT**
*Non-fungible token* (juga dikenal sebagai "deed"). Ini adalah standar token yang diperkenalkan oleh proposal ERC721. NFT dapat dilacak dan diperdagangkan, tetapi setiap token unik dan berbeda; mereka tidak dapat dipertukarkan seperti token ERC20. NFT dapat merepresentasikan kepemilikan aset digital atau fisik.

**Node**
Sebuah klien perangkat lunak yang berpartisipasi dalam jaringan.

**Nonce**
Dalam kriptografi, sebuah nilai yang hanya dapat digunakan satu kali. Ada dua jenis *nonce* yang digunakan di Ethereum: *nonce* akun adalah penghitung transaksi di setiap akun, yang digunakan untuk mencegah serangan pemutaran ulang (*replay attacks*); *nonce* *proof-of-work* adalah nilai acak dalam sebuah blok yang digunakan untuk memenuhi *proof of work*.

**Ommer**
Sebuah blok anak dari leluhur yang bukan merupakan leluhur itu sendiri. Ketika seorang penambang menemukan blok yang valid, penambang lain mungkin telah mempublikasikan blok pesaing yang ditambahkan ke ujung *blockchain*. Berbeda dengan Bitcoin, blok yatim (*orphaned blocks*) di Ethereum dapat dimasukkan oleh blok yang lebih baru sebagai *ommers* dan menerima hadiah blok parsial. Istilah "ommer" adalah istilah netral-gender yang lebih disukai untuk saudara dari sebuah *node* induk, tetapi ini juga terkadang disebut sebagai "uncle."

**Parity**
Salah satu implementasi interoperable paling terkemuka dari perangkat lunak klien Ethereum.

**Private key (Kunci Privat)**
Lihat "secret key".

**Proof of stake (PoS)**
Sebuah metode di mana protokol *blockchain* mata uang kripto bertujuan untuk mencapai konsensus terdistribusi. PoS meminta pengguna untuk membuktikan kepemilikan sejumlah mata uang kripto tertentu ("stake" mereka di jaringan) agar dapat berpartisipasi dalam validasi transaksi.

**Proof of work (PoW)**
Sepotong data (bukti) yang memerlukan komputasi signifikan untuk ditemukan. Di Ethereum, penambang harus menemukan solusi numerik untuk algoritma Ethash yang memenuhi target kesulitan di seluruh jaringan.

**Public key (Kunci Publik)**
Sebuah angka, yang diturunkan melalui fungsi satu arah dari *private key*, yang dapat dibagikan secara publik dan digunakan oleh siapa saja untuk memverifikasi tanda tangan digital yang dibuat dengan *private key* yang sesuai.

**Receipt (Resi)**
Data yang dikembalikan oleh klien Ethereum untuk merepresentasikan hasil dari transaksi tertentu, termasuk *hash* transaksi, nomor bloknya, jumlah *gas* yang digunakan, dan, dalam kasus *deployment* *smart contract*, alamat kontrak tersebut.

**Re-entrancy attack (Serangan Re-entrancy)**
Sebuah serangan yang terdiri dari kontrak penyerang yang memanggil fungsi kontrak korban sedemikian rupa sehingga selama eksekusi, kontrak korban memanggil kembali kontrak penyerang, secara rekursif. Hal ini dapat mengakibatkan, misalnya, pencurian dana dengan melewatkan bagian dari kontrak korban yang memperbarui saldo atau menghitung jumlah penarikan.

**Reward (Hadiah)**
Sejumlah ether yang disertakan dalam setiap blok baru sebagai hadiah oleh jaringan kepada penambang yang menemukan solusi *proof-of-work*.

**RLP**
*Recursive Length Prefix*. Standar pengkodean yang dirancang oleh pengembang Ethereum untuk mengkodekan dan menserialisasi objek (struktur data) dengan kompleksitas dan panjang yang sewenang-wenang.

**Satoshi Nakamoto**
Nama yang digunakan oleh orang atau sekelompok orang yang merancang Bitcoin, menciptakan implementasi referensi aslinya, dan merupakan yang pertama memecahkan masalah pembelanjaan ganda (*double-spend*) untuk mata uang digital. Identitas asli mereka tetap tidak diketahui.

**Secret key (alias private key) (Kunci Rahasia atau Kunci Privat)**
Nomor rahasia yang memungkinkan pengguna Ethereum untuk membuktikan kepemilikan sebuah akun atau kontrak, dengan menghasilkan tanda tangan digital (lihat "public key," "address," "ECDSA").

**Serenity**
Tahap pengembangan keempat dan terakhir dari Ethereum. Serenity belum memiliki tanggal rilis yang direncanakan.

**Serpent**
Bahasa pemrograman *smart contract* prosedural (imperatif) dengan sintaks yang mirip dengan Python.

**SHA**
*Secure Hash Algorithm*. Keluarga fungsi *hash* kriptografi yang diterbitkan oleh *National Institute of Standards and Technology* (NIST).

**Singleton**
Istilah dalam pemrograman komputer yang menggambarkan sebuah objek yang hanya dapat ada satu instansinya saja.

**Smart contract (Kontrak Pintar)**
Sebuah program yang dieksekusi pada infrastruktur komputasi Ethereum.

**Solidity**
Bahasa pemrograman prosedural (imperatif) dengan sintaks yang mirip dengan JavaScript, C++, atau Java. Bahasa yang paling populer dan paling sering digunakan untuk *smart contract* Ethereum. Diciptakan oleh Dr. Gavin Wood (salah satu penulis buku ini).

**Solidity inline assembly (Rakitan inline Solidity)**
Bahasa rakitan EVM dalam sebuah program Solidity. Dukungan Solidity untuk rakitan *inline* memudahkan penulisan operasi tertentu.

**Spurious Dragon**
Sebuah *hard fork* dari *blockchain* Ethereum, yang terjadi di blok \#2.675.000 untuk mengatasi lebih banyak vektor serangan *denial-of-service* dan membersihkan keadaan (*state*) (lihat juga "Tangerine Whistle"). Juga, sebuah mekanisme perlindungan serangan pemutaran ulang (*replay attack*).

**Swarm**
Jaringan penyimpanan terdesentralisasi (P2P), digunakan bersama dengan Web3 dan Whisper untuk membangun DApp.

**Szabo**
Sebuah denominasi ether. `$10^{12}$` szabo = 1 ether.

**Tangerine Whistle**
Sebuah *hard fork* dari *blockchain* Ethereum, yang terjadi di blok \#2.463.000 untuk mengubah perhitungan *gas* untuk operasi I/O-intensif tertentu dan untuk membersihkan akumulasi keadaan dari serangan *denial-of-service*, yang mengeksploitasi biaya *gas* yang rendah dari operasi-operasi tersebut.

**Testnet**
Singkatan dari "*test network*" (jaringan uji), sebuah jaringan yang digunakan untuk mensimulasikan perilaku jaringan utama Ethereum.

**Transaction (Transaksi)**
Data yang dimasukkan ke *Blockchain* Ethereum yang ditandatangani oleh akun asal, menargetkan alamat tertentu. Transaksi tersebut berisi metadata seperti batas *gas* untuk transaksi itu.

**Truffle**
Salah satu kerangka kerja pengembangan Ethereum yang paling umum digunakan.

**Turing complete (Turing lengkap)**
Sebuah konsep yang dinamai menurut matematikawan dan ilmuwan komputer Inggris Alan Turing: sebuah sistem aturan manipulasi data (seperti set instruksi komputer, bahasa pemrograman, atau automaton seluler) dikatakan "Turing lengkap" atau "universal secara komputasi" jika dapat digunakan untuk mensimulasikan mesin Turing apa pun.

**Vitalik Buterin**
Seorang programmer dan penulis Rusia-Kanada yang terutama dikenal sebagai salah satu pendiri Ethereum dan *Bitcoin Magazine*.

**Vyper**
Bahasa pemrograman tingkat tinggi, mirip dengan Serpent, dengan sintaks seperti Python. Dimaksudkan untuk lebih mendekati bahasa fungsional murni. Diciptakan oleh Vitalik Buterin.

**Wallet (Dompet)**
Perangkat lunak yang menyimpan *secret keys*. Digunakan untuk mengakses dan mengontrol akun Ethereum serta berinteraksi dengan *smart contract*. Kunci tidak harus disimpan di dalam dompet, dan sebaliknya dapat diambil dari penyimpanan luring (*offline*) (misalnya, kartu memori atau kertas) untuk keamanan yang lebih baik. Meskipun namanya dompet, dompet tidak pernah menyimpan koin atau token yang sebenarnya.

**Web3**
Versi ketiga dari web. Pertama kali diusulkan oleh Dr. Gavin Wood, Web3 merepresentasikan visi dan fokus baru untuk aplikasi web: dari aplikasi yang dimiliki dan dikelola secara terpusat, menjadi aplikasi yang dibangun di atas protokol terdesentralisasi.

**Wei**
Denominasi terkecil dari ether. `$10^{18}$` wei = 1 ether.

**Whisper**
Layanan pesan terdesentralisasi (P2P). Digunakan bersama dengan Web3 dan Swarm untuk membangun DApp.

**Zero address (Alamat nol)**
Alamat Ethereum khusus, yang seluruhnya terdiri dari angka nol, yang ditentukan sebagai alamat tujuan dari transaksi pembuatan kontrak.

---

# BAB 1
## Apa Itu Ethereum?

Ethereum sering dideskripsikan sebagai "komputer dunia". Tapi apa artinya itu? Mari kita mulai dengan deskripsi yang berfokus pada ilmu komputer, lalu mencoba menguraikannya dengan analisis yang lebih praktis tentang kemampuan dan karakteristik Ethereum, sambil membandingkannya dengan Bitcoin dan platform pertukaran informasi terdesentralisasi lainnya (atau singkatnya, "*blockchain*").

Dari perspektif ilmu komputer, **Ethereum adalah sebuah *state machine* (mesin keadaan) yang deterministik namun secara praktis tidak terbatas**, yang terdiri dari sebuah *singleton state* (keadaan tunggal) yang dapat diakses secara global dan sebuah mesin virtual yang menerapkan perubahan pada keadaan tersebut.

Dari perspektif yang lebih praktis, **Ethereum adalah infrastruktur komputasi sumber terbuka yang terdesentralisasi secara global yang menjalankan program-program yang disebut *smart contract*** (kontrak pintar). Ethereum menggunakan sebuah *blockchain* untuk menyinkronkan dan menyimpan perubahan keadaan sistem, bersama dengan sebuah mata uang kripto yang disebut **ether** untuk mengukur dan membatasi biaya sumber daya eksekusi.

Platform Ethereum memungkinkan para pengembang untuk membangun aplikasi terdesentralisasi yang kuat dengan fungsi ekonomi bawaan. Sambil menyediakan **ketersediaan tinggi, kemampuan diaudit, transparansi, dan netralitas**, platform ini juga **mengurangi atau menghilangkan sensor** dan **mengurangi risiko pihak lawan (*counterparty risk*) tertentu**.

-----

### **Dibandingkan dengan Bitcoin**

Banyak orang akan datang ke Ethereum dengan pengalaman sebelumnya tentang mata uang kripto, khususnya Bitcoin. Ethereum memiliki banyak elemen yang sama dengan *blockchain* terbuka lainnya: jaringan *peer-to-peer* yang menghubungkan para partisipan, algoritma konsensus yang toleran terhadap kesalahan Bizantium (*Byzantine fault-tolerant*) untuk sinkronisasi pembaruan keadaan (sebuah *blockchain proof-of-work*), penggunaan primitif kriptografi seperti tanda tangan digital dan *hash*, serta sebuah mata uang digital (ether).

Namun dalam banyak hal, baik tujuan maupun konstruksi Ethereum sangat berbeda dari *blockchain* terbuka yang mendahuluinya, termasuk Bitcoin.

**Tujuan Ethereum bukanlah primernya untuk menjadi jaringan pembayaran mata uang digital**. Meskipun mata uang digital ether bersifat integral dan diperlukan untuk operasi Ethereum, ether dimaksudkan sebagai **mata uang utilitas** untuk membayar penggunaan platform Ethereum sebagai komputer dunia.

Berbeda dengan Bitcoin, yang memiliki bahasa skrip yang sangat terbatas, Ethereum dirancang untuk menjadi **blockchain yang dapat diprogram untuk tujuan umum** yang menjalankan mesin virtual yang mampu mengeksekusi kode dengan kompleksitas arbitrer dan tak terbatas. Di mana bahasa Skrip Bitcoin sengaja dibatasi pada evaluasi benar/salah sederhana dari kondisi pengeluaran, bahasa Ethereum adalah **Turing lengkap**, yang berarti Ethereum dapat dengan mudah berfungsi sebagai komputer serbaguna.

-----

### **Komponen-Komponen Sebuah Blockchain**

Komponen-komponen dari sebuah *blockchain* yang terbuka dan publik (biasanya) adalah:

  * Sebuah **jaringan *peer-to-peer* (P2P)** yang menghubungkan para partisipan dan menyebarkan transaksi serta blok dari transaksi yang terverifikasi, berdasarkan protokol "gosip" (*gossip*) yang terstandarisasi.
  * **Pesan**, dalam bentuk transaksi, yang merepresentasikan transisi keadaan (*state transitions*).
  * Satu set **aturan konsensus**, yang mengatur apa yang dianggap sebagai transaksi dan apa yang membuat transisi keadaan menjadi valid.
  * Sebuah ***state machine*** (mesin keadaan) yang memproses transaksi sesuai dengan aturan konsensus.
  * Sebuah **rantai blok yang diamankan secara kriptografis** yang berfungsi sebagai jurnal dari semua transisi keadaan yang terverifikasi dan diterima.
  * Sebuah **algoritma konsensus** yang mendesentralisasi kontrol atas *blockchain*, dengan memaksa partisipan untuk bekerja sama dalam penegakan aturan konsensus.
  * Sebuah **skema insentif yang sehat secara teori permainan (*game-theoretically sound*)** (misalnya, biaya *proof-of-work* ditambah hadiah blok) untuk mengamankan *state machine* secara ekonomis di lingkungan yang terbuka.
  * Satu atau lebih **implementasi perangkat lunak sumber terbuka** dari komponen di atas ("klien").

Semua atau sebagian besar komponen ini biasanya digabungkan dalam satu klien perangkat lunak tunggal. Sebagai contoh, di Bitcoin, implementasi referensi dikembangkan oleh proyek sumber terbuka Bitcoin Core dan diimplementasikan sebagai klien `bitcoind`. Di Ethereum, alih-alih implementasi referensi, terdapat **spesifikasi referensi**, sebuah deskripsi matematis dari sistem dalam Yellow Paper (lihat "Bacaan Lebih Lanjut" di halaman 7). Ada sejumlah klien yang dibangun sesuai dengan spesifikasi referensi.

Di masa lalu, kita menggunakan istilah "*blockchain*" untuk mewakili semua komponen yang baru saja disebutkan, sebagai referensi singkat untuk kombinasi teknologi yang mencakup semua karakteristik yang dijelaskan. Namun, saat ini, ada berbagai macam *blockchain* dengan properti yang berbeda. Kita memerlukan kualifikasi untuk membantu kita memahami karakteristik *blockchain* yang dimaksud, seperti **terbuka, publik, global, terdesentralisasi, netral, dan tahan sensor**, untuk mengidentifikasi karakteristik penting yang muncul dari sistem "*blockchain*" yang dimungkinkan oleh komponen-komponen ini.

Tidak semua *blockchain* diciptakan sama. Ketika seseorang memberi tahu Anda bahwa sesuatu adalah *blockchain*, Anda belum menerima jawaban; sebaliknya, Anda perlu mulai mengajukan banyak pertanyaan untuk mengklarifikasi apa yang mereka maksud ketika mereka menggunakan kata "*blockchain*". Mulailah dengan meminta deskripsi komponen-komponen dalam daftar sebelumnya, lalu tanyakan apakah "*blockchain*" ini menunjukkan karakteristik terbuka, publik, dll.

-----

### **Kelahiran Ethereum**

Semua inovasi besar memecahkan masalah nyata, dan Ethereum tidak terkecuali. Ethereum digagas pada saat orang-orang mengakui kekuatan model Bitcoin, dan mencoba untuk melampaui aplikasi mata uang kripto. Tetapi para pengembang menghadapi sebuah teka-teki: mereka harus membangun di atas Bitcoin atau memulai *blockchain* baru.

Membangun di atas Bitcoin berarti hidup dalam batasan yang disengaja dari jaringan dan mencoba mencari solusi alternatif. Keterbatasan jenis transaksi, tipe data, dan ukuran penyimpanan data tampaknya membatasi jenis aplikasi yang dapat berjalan langsung di Bitcoin; hal lain memerlukan lapisan tambahan di luar rantai (*off-chain*), dan itu segera meniadakan banyak keuntungan menggunakan *blockchain* publik. Untuk proyek yang membutuhkan lebih banyak kebebasan dan fleksibilitas sambil tetap berada di dalam rantai (*on-chain*), *blockchain* baru adalah satu-satunya pilihan. Tetapi itu berarti banyak pekerjaan: memulai semua elemen infrastruktur, pengujian yang mendalam, dll.

Menjelang akhir tahun 2013, Vitalik Buterin, seorang programmer muda dan penggemar Bitcoin, mulai berpikir tentang memperluas kemampuan Bitcoin dan Mastercoin (sebuah protokol lapisan atas atau *overlay* yang memperluas Bitcoin untuk menawarkan *smart contract* sederhana). Pada bulan Oktober tahun itu, Vitalik mengusulkan pendekatan yang lebih umum kepada tim Mastercoin, yang memungkinkan kontrak yang fleksibel dan dapat diskrip (tetapi tidak Turing lengkap) untuk menggantikan bahasa kontrak khusus Mastercoin. Meskipun tim Mastercoin terkesan, proposal ini merupakan perubahan yang terlalu radikal untuk dimasukkan ke dalam peta jalan pengembangan mereka.

Pada bulan Desember 2013, Vitalik mulai membagikan sebuah *whitepaper* yang menguraikan gagasan di balik Ethereum: sebuah *blockchain* serbaguna yang Turing lengkap. Beberapa lusin orang melihat draf awal ini dan memberikan umpan balik, membantu Vitalik mengembangkan proposal tersebut.

Kedua penulis buku ini menerima draf awal *whitepaper* dan memberikan komentar. Andreas M. Antonopoulos tertarik dengan gagasan tersebut dan menanyakan banyak pertanyaan kepada Vitalik tentang penggunaan *blockchain* terpisah untuk menegakkan aturan konsensus pada eksekusi *smart contract* dan implikasi dari bahasa yang Turing lengkap. Andreas terus mengikuti kemajuan Ethereum dengan minat besar tetapi sedang dalam tahap awal penulisan bukunya *Mastering Bitcoin*, dan tidak berpartisipasi secara langsung di Ethereum sampai jauh kemudian. Dr. Gavin Wood, bagaimanapun, adalah salah satu orang pertama yang menghubungi Vitalik dan menawarkan bantuan dengan keterampilan pemrograman C++-nya. Gavin menjadi salah satu pendiri, salah satu perancang, dan CTO Ethereum.

Seperti yang diceritakan Vitalik dalam postingannya "Ethereum Prehistory":

> Inilah saatnya ketika protokol Ethereum sepenuhnya merupakan ciptaan saya sendiri. Namun, dari sini dan seterusnya, para partisipan baru mulai bergabung. Yang paling menonjol di sisi protokol adalah Gavin Wood...
>
> Gavin juga sebagian besar dapat dikreditkan atas perubahan visi yang halus dari memandang Ethereum sebagai platform untuk membangun uang yang dapat diprogram, dengan kontrak berbasis *blockchain* yang dapat menampung aset digital dan mentransfernya sesuai dengan aturan yang telah ditetapkan, menjadi platform komputasi serbaguna. Ini dimulai dengan perubahan halus dalam penekanan dan terminologi, dan kemudian pengaruh ini menjadi lebih kuat dengan meningkatnya penekanan pada ansambel "Web 3", yang melihat Ethereum sebagai salah satu bagian dari serangkaian teknologi terdesentralisasi, dua lainnya adalah Whisper dan Swarm.

Mulai Desember 2013, Vitalik dan Gavin menyempurnakan dan mengembangkan gagasan tersebut, bersama-sama membangun lapisan protokol yang menjadi Ethereum.

Para pendiri Ethereum berpikir tentang sebuah *blockchain* tanpa tujuan spesifik, yang dapat mendukung berbagai macam aplikasi dengan cara diprogram. Idenya adalah bahwa dengan menggunakan *blockchain* serbaguna seperti Ethereum, seorang pengembang dapat memprogram aplikasi khusus mereka tanpa harus mengimplementasikan mekanisme dasar jaringan *peer-to-peer*, *blockchain*, algoritma konsensus, dll. Platform Ethereum dirancang untuk mengabstraksi detail-detail ini dan menyediakan lingkungan pemrograman yang deterministik dan aman untuk aplikasi *blockchain* terdesentralisasi.

Sama seperti Satoshi, Vitalik dan Gavin tidak hanya menciptakan teknologi baru; mereka menggabungkan penemuan baru dengan teknologi yang ada dengan cara yang baru dan mengirimkan kode prototipe untuk membuktikan ide-ide mereka kepada dunia.

Para pendiri bekerja selama bertahun-tahun, membangun dan menyempurnakan visi tersebut. Dan pada tanggal 30 Juli 2015, blok Ethereum pertama ditambang. Komputer dunia mulai melayani dunia.

> Artikel Vitalik Buterin "A Prehistory of Ethereum" diterbitkan pada September 2017 dan memberikan pandangan orang pertama yang menarik tentang momen-momen paling awal Ethereum.
>
> Anda dapat membacanya di [https://vitalik.ca/general/2017/09/14/prehistory.html](https://www.google.com/search?q=https://vitalik.ca/general/2017/09/14/prehistory.html).

-----

### **Empat Tahap Pengembangan Ethereum**

Pengembangan Ethereum direncanakan dalam empat tahap yang berbeda, dengan perubahan besar terjadi di setiap tahap. Sebuah tahap dapat mencakup sub-rilis, yang dikenal sebagai "*hard fork*", yang mengubah fungsionalitas dengan cara yang tidak kompatibel mundur (*backward compatible*).

Empat tahap pengembangan utama diberi nama kode **Frontier, Homestead, Metropolis, dan Serenity**. *Hard fork* perantara yang telah terjadi (atau direncanakan) hingga saat ini diberi nama kode **Ice Age, DAO, Tangerine Whistle, Spurious Dragon, Byzantium, dan Constantinople**. Baik tahap pengembangan maupun *hard fork* perantara ditunjukkan pada garis waktu berikut, yang "diberi tanggal" berdasarkan nomor blok:

**Blok \#0**
**Frontier**—Tahap awal Ethereum, berlangsung dari 30 Juli 2015, hingga Maret 2016.

**Blok \#200.000**
**Ice Age**—Sebuah *hard fork* untuk memperkenalkan peningkatan kesulitan eksponensial, untuk memotivasi transisi ke PoS ketika sudah siap.

**Blok \#1.150.000**
**Homestead**—Tahap kedua Ethereum, diluncurkan pada Maret 2016.

**Blok \#1.192.000**
**DAO**—Sebuah *hard fork* yang memberikan kompensasi kepada korban dari kontrak DAO yang diretas dan menyebabkan Ethereum dan Ethereum Classic terpecah menjadi dua sistem yang bersaing.

**Blok \#2.463.000**
**Tangerine Whistle**—Sebuah *hard fork* untuk mengubah perhitungan *gas* untuk operasi padat I/O tertentu dan untuk membersihkan akumulasi keadaan dari serangan *denial-of-service* (DoS) yang mengeksploitasi biaya *gas* yang rendah dari operasi-operasi tersebut.

**Blok \#2.675.000**
**Spurious Dragon**—Sebuah *hard fork* untuk mengatasi lebih banyak vektor serangan DoS, dan pembersihan keadaan lainnya. Juga, sebuah mekanisme perlindungan serangan pemutaran ulang (*replay attack*).

**Blok \#4.370.000**
**Metropolis Byzantium**—Metropolis adalah tahap ketiga Ethereum, yang sedang berjalan pada saat penulisan buku ini, diluncurkan pada Oktober 2017. Byzantium adalah yang pertama dari dua *hard fork* yang direncanakan untuk Metropolis.

Setelah Byzantium, ada satu lagi *hard fork* yang direncanakan untuk Metropolis: **Constantinople**. Metropolis akan diikuti oleh tahap akhir penyebaran Ethereum, dengan nama kode **Serenity**.

-----

### **Ethereum: Blockchain Serbaguna**

*Blockchain* asli, yaitu *blockchain* Bitcoin, melacak keadaan unit bitcoin dan kepemilikannya. Anda dapat menganggap Bitcoin sebagai mesin keadaan konsensus terdistribusi, di mana transaksi menyebabkan transisi keadaan global, mengubah kepemilikan koin. Transisi keadaan dibatasi oleh aturan konsensus, memungkinkan semua partisipan untuk (pada akhirnya) mencapai keadaan umum (konsensus) dari sistem, setelah beberapa blok ditambang.

Ethereum juga merupakan mesin keadaan terdistribusi. Tetapi alih-alih hanya melacak keadaan kepemilikan mata uang, Ethereum melacak transisi keadaan dari sebuah **penyimpanan data serbaguna**, yaitu, sebuah penyimpanan yang dapat menampung data apa pun yang dapat diekspresikan sebagai tupel kunci-nilai (*key-value tuple*). Penyimpanan data kunci-nilai menampung nilai-nilai arbitrer, masing-masing direferensikan oleh beberapa kunci; misalnya, nilai "Mastering Ethereum" yang direferensikan oleh kunci "Book Title". Dalam beberapa hal, ini melayani tujuan yang sama dengan model penyimpanan data *Random Access Memory* (RAM) yang digunakan oleh sebagian besar komputer serbaguna. Ethereum memiliki memori yang menyimpan baik kode maupun data, dan menggunakan *blockchain* Ethereum untuk melacak bagaimana memori ini berubah dari waktu ke waktu. Seperti komputer *stored-program* serbaguna, Ethereum dapat memuat kode ke dalam *state machine*-nya dan menjalankan kode itu, menyimpan perubahan keadaan yang dihasilkan di dalam *blockchain*-nya. Dua perbedaan kritis dari sebagian besar komputer serbaguna adalah bahwa perubahan keadaan Ethereum diatur oleh aturan konsensus dan keadaannya didistribusikan secara global. Ethereum menjawab pertanyaan: "Bagaimana jika kita bisa melacak keadaan arbitrer apa pun dan memprogram *state machine* untuk menciptakan komputer dunia yang beroperasi di bawah konsensus?"

-----

### **Komponen-Komponen Ethereum**

Di Ethereum, komponen-komponen dari sistem *blockchain* yang dijelaskan dalam "Komponen-Komponen Sebuah Blockchain" di halaman 2, secara lebih spesifik adalah:

**Jaringan P2P**
Ethereum berjalan di jaringan utama Ethereum, yang dapat dialamatkan pada port TCP 30303, dan menjalankan protokol yang disebut ÐΞVp2p.

**Aturan Konsensus**
Aturan konsensus Ethereum didefinisikan dalam spesifikasi referensi, Yellow Paper (lihat "Bacaan Lebih Lanjut" di halaman 7).

**Transaksi**
Transaksi Ethereum adalah pesan jaringan yang mencakup (antara lain) pengirim, penerima, nilai, dan muatan data (*data payload*).

***State machine***
Transisi keadaan Ethereum diproses oleh *Ethereum Virtual Machine* (EVM), sebuah mesin virtual berbasis tumpukan (*stack-based*) yang mengeksekusi *bytecode* (instruksi bahasa mesin). Program EVM, yang disebut "*smart contracts*", ditulis dalam bahasa tingkat tinggi (misalnya, Solidity) dan dikompilasi menjadi *bytecode* untuk dieksekusi di EVM.

**Struktur Data**
Keadaan Ethereum disimpan secara lokal di setiap *node* sebagai sebuah basis data (biasanya LevelDB dari Google), yang berisi transaksi dan keadaan sistem dalam struktur data *hash* berseri yang disebut Pohon Merkle Patricia (*Merkle Patricia Tree*).

**Algoritma Konsensus**
Ethereum menggunakan model konsensus Bitcoin, Konsensus Nakamoto, yang menggunakan blok tanda tangan tunggal berurutan, yang bobot kepentingannya ditentukan oleh PoW untuk menentukan rantai terpanjang dan oleh karena itu keadaan saat ini. Namun, ada rencana untuk beralih ke sistem pemungutan suara berbobot PoS, dengan nama kode Casper, dalam waktu dekat.

**Keamanan Ekonomi**
Ethereum saat ini menggunakan algoritma PoW yang disebut Ethash, tetapi ini pada akhirnya akan ditinggalkan dengan perpindahan ke PoS di masa depan.

**Klien**
Ethereum memiliki beberapa implementasi perangkat lunak klien yang dapat saling beroperasi, yang paling menonjol adalah Go-Ethereum (Geth) dan Parity.

-----

### **Bacaan Lebih Lanjut**

Referensi berikut memberikan informasi tambahan tentang teknologi yang disebutkan di sini:

  * The Ethereum Yellow Paper: [https://ethereum.github.io/yellowpaper/paper.pdf](https://ethereum.github.io/yellowpaper/paper.pdf)
  * The Beige Paper, sebuah penulisan ulang Yellow Paper untuk audiens yang lebih luas dalam bahasa yang kurang formal: [https://github.com/chronaeon/beigepaper](https://github.com/chronaeon/beigepaper)
  * Protokol jaringan ÐΞVp2p: [http://bit.ly/2quAlTE](http://bit.ly/2quAlTE)
  * Daftar sumber daya Ethereum Virtual Machine: [http://bit.ly/2PmtjiS](http://bit.ly/2PmtjiS)
  * Basis data LevelDB (paling sering digunakan untuk menyimpan salinan lokal dari *blockchain*): [http://leveldb.org](http://leveldb.org)
  * Pohon Merkle Patricia: [https://github.com/ethereum/wiki/wiki/Patricia-Tree](https://github.com/ethereum/wiki/wiki/Patricia-Tree)
  * Algoritma PoW Ethash: [https://github.com/ethereum/wiki/wiki/Ethash](https://github.com/ethereum/wiki/wiki/Ethash)
  * Panduan Implementasi Casper PoS v1: [http://bit.ly/2DyPr3l](http://bit.ly/2DyPr3l)
  * Klien Go-Ethereum (Geth): [https://geth.ethereum.org/](https://geth.ethereum.org/)
  * Klien Parity Ethereum: [https://parity.io/](https://parity.io/)

-----

### **Ethereum dan Kelengkapan Turing (Turing Completeness)**

Segera setelah Anda mulai membaca tentang Ethereum, Anda akan segera menemukan istilah "**Turing lengkap**". Ethereum, kata mereka, tidak seperti Bitcoin, adalah Turing lengkap. Apa sebenarnya artinya itu?

Istilah ini merujuk pada matematikawan Inggris Alan Turing, yang dianggap sebagai bapak ilmu komputer. Pada tahun 1936 ia menciptakan model matematis dari sebuah komputer yang terdiri dari sebuah *state machine* yang memanipulasi simbol dengan membaca dan menulisnya pada memori berurutan (menyerupai pita kertas dengan panjang tak terbatas). Dengan konstruksi ini, Turing kemudian memberikan dasar matematis untuk menjawab (secara negatif) pertanyaan tentang komputabilitas universal, yang berarti apakah semua masalah dapat diselesaikan. Dia membuktikan bahwa ada kelas masalah yang tidak dapat dihitung. Secara khusus, ia membuktikan bahwa **masalah penghentian (*halting problem*)** (apakah mungkin, dengan program dan input yang arbitrer, untuk menentukan apakah program tersebut pada akhirnya akan berhenti berjalan) tidak dapat diselesaikan.

Alan Turing lebih lanjut mendefinisikan sebuah sistem sebagai **Turing lengkap** jika dapat digunakan untuk mensimulasikan mesin Turing apa pun. Sistem semacam itu disebut **Mesin Turing Universal (*Universal Turing machine* - UTM)**.

Kemampuan Ethereum untuk mengeksekusi program yang tersimpan, dalam sebuah *state machine* yang disebut *Ethereum Virtual Machine*, sambil membaca dan menulis data ke memori membuatnya menjadi sistem yang Turing lengkap dan oleh karena itu sebuah UTM. Ethereum dapat menghitung algoritma apa pun yang dapat dihitung oleh mesin Turing mana pun, dengan batasan memori yang terbatas.

Inovasi terobosan Ethereum adalah menggabungkan arsitektur komputasi serbaguna dari komputer *stored-program* dengan *blockchain* terdesentralisasi, dengan demikian menciptakan **komputer dunia dengan keadaan tunggal (*singleton*) yang terdistribusi**. Program-program Ethereum berjalan "di mana-mana," namun menghasilkan keadaan umum yang diamankan oleh aturan konsensus.

#### **Kelengkapan Turing sebagai sebuah "Fitur"**

Mendengar bahwa Ethereum adalah Turing lengkap, Anda mungkin sampai pada kesimpulan bahwa ini adalah fitur yang entah bagaimana kurang dalam sistem yang tidak Turing lengkap. Sebenarnya, sebaliknya. Kelengkapan Turing sangat mudah dicapai; faktanya, *state machine* Turing lengkap paling sederhana yang diketahui memiliki 4 keadaan dan menggunakan 6 simbol, dengan definisi keadaan yang hanya sepanjang 22 instruksi. Memang, terkadang sistem ditemukan "secara tidak sengaja menjadi Turing lengkap". Referensi yang menyenangkan tentang sistem semacam itu dapat ditemukan di [http://bit.ly/2Og1VgX](http://bit.ly/2Og1VgX).

Namun, kelengkapan Turing sangat berbahaya, terutama dalam sistem akses terbuka seperti *blockchain* publik, karena masalah penghentian (*halting problem*) yang telah kita singgung sebelumnya. 

sebagai contoh, printer modern bersifat Turing lengkap dan dapat diberikan file untuk dicetak yang mengirimnya ke kondisi macet (*frozen state*). Fakta bahwa Ethereum adalah Turing lengkap berarti bahwa program apa pun dengan kompleksitas apa pun dapat dihitung oleh Ethereum. Tetapi fleksibilitas itu membawa beberapa masalah keamanan dan manajemen sumber daya yang pelik. Printer yang tidak responsif dapat dimatikan dan dihidupkan kembali. Hal itu tidak mungkin dilakukan dengan *blockchain* publik.

### **Implikasi dari Kelengkapan Turing**

Turing membuktikan bahwa Anda tidak dapat memprediksi apakah sebuah program akan berakhir dengan mensimulasikannya di komputer. Secara sederhana, kita tidak dapat memprediksi jalur sebuah program tanpa menjalankannya. Sistem yang Turing lengkap dapat berjalan dalam "**loop tak terbatas**," sebuah istilah yang digunakan (secara terlalu sederhana) untuk menggambarkan program yang tidak berhenti. Sangat mudah untuk membuat program yang menjalankan *loop* yang tidak pernah berakhir. Tetapi *loop* yang tidak pernah berakhir secara tidak sengaja dapat muncul tanpa peringatan, karena interaksi yang kompleks antara kondisi awal dan kode. Di Ethereum, ini menimbulkan sebuah tantangan: setiap *node* (klien) yang berpartisipasi harus memvalidasi setiap transaksi, menjalankan *smart contract* apa pun yang dipanggilnya.

Namun seperti yang dibuktikan Turing, Ethereum tidak dapat memprediksi apakah sebuah *smart contract* akan berhenti, atau berapa lama ia akan berjalan, tanpa benar-benar menjalankannya (yang mungkin berjalan selamanya). Baik secara sengaja maupun tidak, sebuah *smart contract* dapat dibuat sedemikian rupa sehingga berjalan selamanya ketika sebuah *node* mencoba memvalidasinya. Ini secara efektif merupakan serangan DoS. Dan tentu saja, di antara program yang membutuhkan satu milidetik untuk divalidasi dan yang berjalan selamanya, terdapat rentang tak terbatas dari program-program jahat yang boros sumber daya, membebani memori, dan membuat CPU panas berlebih yang hanya membuang-buang sumber daya. Di dalam sebuah komputer dunia, sebuah program yang menyalahgunakan sumber daya berarti menyalahgunakan sumber daya dunia. Bagaimana Ethereum membatasi sumber daya yang digunakan oleh *smart contract* jika ia tidak dapat memprediksi penggunaan sumber daya di muka?

Untuk menjawab tantangan ini, Ethereum memperkenalkan mekanisme pengukuran yang disebut **gas**. Saat EVM mengeksekusi *smart contract*, ia dengan cermat menghitung setiap instruksi (komputasi, akses data, dll.). Setiap instruksi memiliki biaya yang telah ditentukan dalam satuan gas. Ketika sebuah transaksi memicu eksekusi *smart contract*, transaksi tersebut harus menyertakan sejumlah gas yang menetapkan batas atas dari apa yang dapat dikonsumsi saat menjalankan *smart contract*. EVM akan menghentikan eksekusi jika jumlah gas yang dikonsumsi oleh komputasi melebihi gas yang tersedia dalam transaksi. Gas adalah mekanisme yang digunakan Ethereum untuk memungkinkan komputasi Turing lengkap sambil membatasi sumber daya yang dapat dikonsumsi oleh program apa pun.

Pertanyaan selanjutnya adalah, bagaimana seseorang mendapatkan gas untuk membayar komputasi di komputer dunia Ethereum? Anda tidak akan menemukan gas di bursa mana pun. Gas hanya dapat dibeli sebagai bagian dari transaksi, dan hanya dapat dibeli dengan **ether**. Ether perlu dikirim bersama dengan transaksi dan perlu dialokasikan secara eksplisit untuk pembelian gas, bersama dengan harga gas yang dapat diterima. Sama seperti di pom bensin, harga gas tidak tetap. Gas dibeli untuk transaksi, komputasi dieksekusi, dan gas yang tidak terpakai dikembalikan kepada pengirim transaksi.

### **Dari Blockchain Serbaguna ke Aplikasi Terdesentralisasi (DApps)**

Ethereum dimulai sebagai cara untuk membuat *blockchain* serbaguna yang dapat diprogram untuk berbagai kegunaan. Namun dengan sangat cepat, visi Ethereum meluas menjadi platform untuk memprogram **DApps**. DApps merepresentasikan perspektif yang lebih luas daripada *smart contract*. Sebuah DApp, minimal, adalah sebuah *smart contract* dan sebuah antarmuka pengguna web. Secara lebih luas, DApp adalah aplikasi web yang dibangun di atas layanan infrastruktur *peer-to-peer* yang terbuka dan terdesentralisasi.

Sebuah DApp terdiri dari setidaknya:
* *Smart contract* di sebuah *blockchain*
* Antarmuka pengguna *frontend* web

Selain itu, banyak DApp menyertakan komponen terdesentralisasi lainnya, seperti:
* Protokol dan platform penyimpanan terdesentralisasi (P2P)
* Protokol dan platform pesan terdesentralisasi (P2P)

> Anda mungkin melihat DApps dieja sebagai **ÐApps**. Karakter Ð adalah karakter Latin yang disebut "ETH," yang merujuk pada Ethereum. Untuk menampilkan karakter ini, gunakan kodepoin Unicode `0xD0`, atau jika perlu entitas karakter HTML `&eth;` (atau entitas desimal `&#208;`).

### **Era Ketiga Internet**

Pada tahun 2004, istilah "Web 2.0" menjadi terkenal, menggambarkan evolusi web menuju konten yang dibuat pengguna, antarmuka yang responsif, dan interaktivitas. Web 2.0 bukanlah spesifikasi teknis, melainkan istilah yang menggambarkan fokus baru aplikasi web.

Konsep DApps dimaksudkan untuk membawa World Wide Web ke tahap evolusi alaminya yang berikutnya, memperkenalkan desentralisasi dengan protokol *peer-to-peer* ke dalam setiap aspek aplikasi web. Istilah yang digunakan untuk menggambarkan evolusi ini adalah **web3**, yang berarti "versi" ketiga dari web. Pertama kali diusulkan oleh Dr. Gavin Wood, web3 merepresentasikan visi dan fokus baru untuk aplikasi web: dari aplikasi yang dimiliki dan dikelola secara terpusat, menjadi aplikasi yang dibangun di atas protokol terdesentralisasi.

Di bab-bab selanjutnya, kita akan menjelajahi pustaka JavaScript `web3.js` Ethereum, yang menjembatani aplikasi JavaScript yang berjalan di browser Anda dengan *blockchain* Ethereum. Pustaka `web3.js` juga mencakup antarmuka ke jaringan penyimpanan P2P yang disebut Swarm dan layanan pesan P2P yang disebut Whisper. Dengan ketiga komponen ini yang disertakan dalam pustaka JavaScript yang berjalan di browser web Anda, para pengembang memiliki seperangkat pengembangan aplikasi lengkap yang memungkinkan mereka membangun DApps web3.

### **Budaya Pengembangan Ethereum**

Sejauh ini kita telah membahas bagaimana tujuan dan teknologi Ethereum berbeda dari *blockchain* lain yang mendahuluinya, seperti Bitcoin. Ethereum juga memiliki budaya pengembangan yang sangat berbeda.

Di Bitcoin, pengembangan dipandu oleh prinsip-prinsip konservatif: semua perubahan dipelajari dengan cermat untuk memastikan tidak ada sistem yang ada yang terganggu. Sebagian besar, perubahan hanya diimplementasikan jika kompatibel mundur (*backward compatible*). Klien yang ada diizinkan untuk ikut serta, tetapi akan terus beroperasi jika mereka memutuskan untuk tidak melakukan pembaruan.

Di Ethereum, sebagai perbandingan, budaya pengembangan komunitasnya berfokus pada masa depan daripada masa lalu. Mantra (yang tidak sepenuhnya serius) adalah "*move fast and break things*" (bergerak cepat dan merusak banyak hal). Jika perubahan diperlukan, itu akan diimplementasikan, bahkan jika itu berarti membatalkan asumsi sebelumnya, merusak kompatibilitas, atau memaksa klien untuk memperbarui. Budaya pengembangan Ethereum ditandai oleh inovasi yang cepat, evolusi yang cepat, dan kesediaan untuk menerapkan perbaikan yang berwawasan ke depan, bahkan jika ini mengorbankan beberapa kompatibilitas mundur.

Apa artinya ini bagi Anda sebagai pengembang adalah Anda harus tetap fleksibel dan bersiap untuk membangun kembali infrastruktur Anda saat beberapa asumsi yang mendasarinya berubah. Salah satu tantangan besar yang dihadapi pengembang di Ethereum adalah kontradiksi yang melekat antara men-deploy kode ke sistem yang tidak dapat diubah (*immutable*) dan platform pengembangan yang masih terus berkembang. Anda tidak bisa begitu saja "memperbarui" *smart contract* Anda. Anda harus siap untuk men-deploy yang baru, memigrasikan pengguna, aplikasi, dan dana, lalu memulai dari awal.

Ironisnya, ini juga berarti bahwa tujuan membangun sistem dengan lebih banyak otonomi dan lebih sedikit kontrol terpusat masih belum sepenuhnya terwujud. Otonomi dan desentralisasi memerlukan sedikit lebih banyak stabilitas pada platform daripada yang mungkin Anda dapatkan di Ethereum dalam beberapa tahun ke depan. Untuk "mengembangkan" platform, Anda harus siap untuk membuang dan memulai kembali *smart contract* Anda, yang berarti Anda harus mempertahankan tingkat kontrol tertentu atasnya.

Tetapi, di sisi positifnya, Ethereum bergerak maju dengan sangat cepat. Ada sedikit peluang untuk "*bike-shedding*," sebuah ekspresi yang berarti menunda pengembangan dengan memperdebatkan detail-detail kecil seperti bagaimana membangun gudang sepeda di belakang stasiun tenaga nuklir. Jika Anda mulai melakukan *bike-shedding*, Anda mungkin tiba-tiba menemukan bahwa saat Anda teralihkan, sisa tim pengembangan telah mengubah rencana dan meninggalkan sepeda demi *hovercraft* otonom.

Pada akhirnya, pengembangan platform Ethereum akan melambat dan antarmukanya akan menjadi tetap. Tetapi untuk saat ini, inovasi adalah prinsip pendorongnya. Sebaiknya Anda mengikutinya, karena tidak ada yang akan melambat untuk Anda.

### **Mengapa Belajar Ethereum?**

*Blockchain* memiliki kurva belajar yang sangat curam, karena mereka menggabungkan berbagai disiplin ilmu menjadi satu domain: pemrograman, keamanan informasi, kriptografi, ekonomi, sistem terdistribusi, jaringan *peer-to-peer*, dll. Ethereum membuat kurva belajar ini jauh lebih landai, sehingga Anda dapat memulai dengan cepat. Tetapi tepat di bawah permukaan lingkungan yang tampak sederhana ini, terdapat lebih banyak lagi. Saat Anda belajar dan mulai melihat lebih dalam, selalu ada lapisan kompleksitas dan keajaiban lainnya.

Ethereum adalah platform yang hebat untuk belajar tentang *blockchain* dan sedang membangun komunitas pengembang yang besar, lebih cepat daripada platform *blockchain* lainnya. Lebih dari yang lain, Ethereum adalah *blockchain* untuk pengembang, dibangun oleh pengembang untuk pengembang. Seorang pengembang yang akrab dengan aplikasi JavaScript dapat langsung terjun ke Ethereum dan mulai menghasilkan kode yang berfungsi dengan sangat cepat. Selama beberapa tahun pertama kehidupan Ethereum, umum untuk melihat kaus yang mengumumkan bahwa Anda dapat membuat token hanya dalam lima baris kode. Tentu saja, ini adalah pedang bermata dua. Sangat mudah untuk menulis kode, tetapi sangat sulit untuk menulis kode yang baik dan aman.

### **Apa yang Akan Anda Pelajari dari Sini**

Buku ini akan menyelami Ethereum dan memeriksa setiap komponennya. Anda akan mulai dengan transaksi sederhana, membedah cara kerjanya, membangun kontrak sederhana, membuatnya lebih baik, dan mengikuti perjalanannya melalui sistem Ethereum.

Anda tidak hanya akan belajar cara menggunakan Ethereum—bagaimana cara kerjanya—tetapi juga **mengapa** ia dirancang seperti itu. Anda akan dapat memahami bagaimana setiap bagian bekerja, dan bagaimana mereka saling cocok satu sama lain dan mengapa.

---

# BAB 2
## Dasar-Dasar Ethereum

Dalam bab ini kita akan mulai menjelajahi Ethereum, mempelajari cara menggunakan dompet, cara membuat transaksi, dan juga cara menjalankan *smart contract* dasar.

### **Unit Mata Uang Ether**

Unit mata uang Ethereum disebut **ether**, diidentifikasi juga sebagai "ETH" atau dengan simbol **Ξ** (dari huruf Yunani "Xi" yang terlihat seperti huruf kapital E yang digayakan) atau, lebih jarang, **♦**: contohnya, 1 ether, atau 1 ETH, atau Ξ1, atau ♦1.

> Gunakan karakter Unicode U+039E untuk Ξ dan U+2666 untuk ♦.

Ether dibagi lagi menjadi unit-unit yang lebih kecil, hingga unit terkecil yang mungkin, yang diberi nama **wei**. Satu ether adalah 1 kuintiliun wei ($1 \times 10^{18}$ atau 1.000.000.000.000.000.000). Anda mungkin mendengar orang merujuk mata uang ini sebagai "Ethereum" juga, tetapi ini adalah kesalahan umum pemula. **Ethereum adalah sistemnya, ether adalah mata uangnya.**

Nilai ether selalu direpresentasikan secara internal di Ethereum sebagai nilai integer tak bertanda (*unsigned integer*) dalam denominasi wei. Ketika Anda bertransaksi 1 ether, transaksi tersebut mengkodekan `1000000000000000000` wei sebagai nilainya.

Berbagai denominasi ether memiliki nama ilmiah yang menggunakan Sistem Satuan Internasional (SI) dan nama sehari-hari (*colloquial*) yang memberikan penghormatan kepada banyak pemikir hebat di bidang komputasi dan kriptografi.

Tabel 2-1 menunjukkan berbagai unit, nama sehari-hari (umum), dan nama SI-nya. Sesuai dengan representasi nilai internal, tabel ini menunjukkan semua denominasi dalam wei (baris pertama), dengan ether ditunjukkan sebagai $10^{18}$ wei di baris ke-7.

<p align="center">
  <img src="images/books-07-mastering_ethereum/tabel-2.1.png" alt="gambar" width="580"/>
</p>

