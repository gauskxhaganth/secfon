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
Sebuah nilai yang digunakan untuk menghasilkan *master private key* dan *master chain code* untuk sebuah dompet HD. *Wallet seed* dapat direpresentasikan oleh kata-kata mnemonic, membuatnya lebih mudah bagi manusia untuk menyalin, mencadangkan, dan memulihkan *private key*.

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

### **Dibandingkan dengan Bitcoin**

Banyak orang akan datang ke Ethereum dengan pengalaman sebelumnya tentang mata uang kripto, khususnya Bitcoin. Ethereum memiliki banyak elemen yang sama dengan *blockchain* terbuka lainnya: jaringan *peer-to-peer* yang menghubungkan para partisipan, algoritma konsensus yang toleran terhadap kesalahan Bizantium (*Byzantine fault-tolerant*) untuk sinkronisasi pembaruan keadaan (sebuah *blockchain proof-of-work*), penggunaan primitif kriptografi seperti tanda tangan digital dan *hash*, serta sebuah mata uang digital (ether).

Namun dalam banyak hal, baik tujuan maupun konstruksi Ethereum sangat berbeda dari *blockchain* terbuka yang mendahuluinya, termasuk Bitcoin.

**Tujuan Ethereum bukanlah primernya untuk menjadi jaringan pembayaran mata uang digital**. Meskipun mata uang digital ether bersifat integral dan diperlukan untuk operasi Ethereum, ether dimaksudkan sebagai **mata uang utilitas** untuk membayar penggunaan platform Ethereum sebagai komputer dunia.

Berbeda dengan Bitcoin, yang memiliki bahasa skrip yang sangat terbatas, Ethereum dirancang untuk menjadi **blockchain yang dapat diprogram untuk tujuan umum** yang menjalankan mesin virtual yang mampu mengeksekusi kode dengan kompleksitas arbitrer dan tak terbatas. Di mana bahasa Skrip Bitcoin sengaja dibatasi pada evaluasi benar/salah sederhana dari kondisi pengeluaran, bahasa Ethereum adalah **Turing lengkap**, yang berarti Ethereum dapat dengan mudah berfungsi sebagai komputer serbaguna.

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

### **Ethereum: Blockchain Serbaguna**

*Blockchain* asli, yaitu *blockchain* Bitcoin, melacak keadaan unit bitcoin dan kepemilikannya. Anda dapat menganggap Bitcoin sebagai mesin keadaan konsensus terdistribusi, di mana transaksi menyebabkan transisi keadaan global, mengubah kepemilikan koin. Transisi keadaan dibatasi oleh aturan konsensus, memungkinkan semua partisipan untuk (pada akhirnya) mencapai keadaan umum (konsensus) dari sistem, setelah beberapa blok ditambang.

Ethereum juga merupakan mesin keadaan terdistribusi. Tetapi alih-alih hanya melacak keadaan kepemilikan mata uang, Ethereum melacak transisi keadaan dari sebuah **penyimpanan data serbaguna**, yaitu, sebuah penyimpanan yang dapat menampung data apa pun yang dapat diekspresikan sebagai tupel kunci-nilai (*key-value tuple*). Penyimpanan data kunci-nilai menampung nilai-nilai arbitrer, masing-masing direferensikan oleh beberapa kunci; misalnya, nilai "Mastering Ethereum" yang direferensikan oleh kunci "Book Title". Dalam beberapa hal, ini melayani tujuan yang sama dengan model penyimpanan data *Random Access Memory* (RAM) yang digunakan oleh sebagian besar komputer serbaguna. Ethereum memiliki memori yang menyimpan baik kode maupun data, dan menggunakan *blockchain* Ethereum untuk melacak bagaimana memori ini berubah dari waktu ke waktu. Seperti komputer *stored-program* serbaguna, Ethereum dapat memuat kode ke dalam *state machine*-nya dan menjalankan kode itu, menyimpan perubahan keadaan yang dihasilkan di dalam *blockchain*-nya. Dua perbedaan kritis dari sebagian besar komputer serbaguna adalah bahwa perubahan keadaan Ethereum diatur oleh aturan konsensus dan keadaannya didistribusikan secara global. Ethereum menjawab pertanyaan: "Bagaimana jika kita bisa melacak keadaan arbitrer apa pun dan memprogram *state machine* untuk menciptakan komputer dunia yang beroperasi di bawah konsensus?"

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

### **Bacaan Lebih Lanjut**

Referensi berikut memberikan informasi tambahan tentang teknologi yang disebutkan di sini:

  * [The Ethereum Yellow Paper](https://ethereum.github.io/yellowpaper/paper.pdf)
  * [The Beige Paper, sebuah penulisan ulang Yellow Paper untuk audiens yang lebih luas dalam bahasa yang kurang formal](https://github.com/chronaeon/beigepaper)
  * [Protokol jaringan ÐΞVp2p](http://bit.ly/2quAlTE)
  * [Daftar sumber daya Ethereum Virtual Machine][http://bit.ly/2PmtjiS](http://bit.ly/2PmtjiS)
  * [Basis data LevelDB (paling sering digunakan untuk menyimpan salinan lokal dari *blockchain*](http://leveldb.org)
  * [Pohon Merkle Patricia](https://github.com/ethereum/wiki/wiki/Patricia-Tree)
  * [Algoritma PoW Ethash](https://github.com/ethereum/wiki/wiki/Ethash)
  * [Panduan Implementasi Casper PoS v1](http://bit.ly/2DyPr3l)
  * [Klien Go-Ethereum (Geth)](https://geth.ethereum.org/)
  * [Klien Parity Ethereum](https://parity.io/)

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

### **Memilih Dompet Ethereum**

Istilah "dompet" (*wallet*) telah memiliki banyak arti, meskipun semuanya saling terkait dan dalam penggunaan sehari-hari pada dasarnya merujuk pada hal yang sama. Kami akan menggunakan istilah "dompet" untuk mengartikan **aplikasi perangkat lunak yang membantu Anda mengelola akun Ethereum Anda**. Singkatnya, dompet Ethereum adalah gerbang Anda ke sistem Ethereum. Dompet ini menyimpan kunci Anda dan dapat membuat serta menyiarkan transaksi atas nama Anda. Memilih dompet Ethereum bisa jadi sulit karena ada banyak pilihan berbeda dengan fitur dan desain yang beragam. Beberapa lebih cocok untuk pemula dan beberapa lebih cocok untuk para ahli. Platform Ethereum itu sendiri masih terus disempurnakan, dan dompet "terbaik" sering kali adalah yang dapat beradaptasi dengan perubahan yang datang bersama pembaruan platform.

Tapi jangan khawatir! Jika Anda memilih dompet dan tidak menyukai cara kerjanya—atau jika Anda menyukainya pada awalnya tetapi kemudian ingin mencoba yang lain—Anda dapat mengganti dompet dengan cukup mudah. Yang harus Anda lakukan adalah membuat transaksi yang mengirimkan dana Anda dari dompet lama ke dompet baru, atau mengekspor kunci privat (*private keys*) Anda dan mengimpornya ke dompet yang baru.

Kami telah memilih tiga jenis dompet yang berbeda untuk digunakan sebagai contoh di seluruh buku: **dompet seluler, dompet desktop, dan dompet berbasis web**. Kami memilih ketiga dompet ini karena mereka merepresentasikan berbagai macam kompleksitas dan fitur. Namun, pemilihan dompet-dompet ini **bukanlah sebuah dukungan** terhadap kualitas atau keamanannya. Mereka hanyalah titik awal yang baik untuk demonstrasi dan pengujian.

Ingatlah bahwa agar aplikasi dompet dapat berfungsi, ia harus memiliki akses ke kunci privat Anda, jadi sangat penting bagi Anda untuk hanya mengunduh dan menggunakan aplikasi dompet dari sumber yang Anda percayai. Untungnya, secara umum, semakin populer sebuah aplikasi dompet, semakin besar kemungkinannya untuk dapat dipercaya. Meskipun demikian, merupakan praktik yang baik untuk tidak "menaruh semua telur Anda dalam satu keranjang" dan menyebarkan akun Ethereum Anda di beberapa dompet.

Berikut adalah beberapa dompet yang bagus untuk memulai:

**MetaMask**
MetaMask adalah dompet ekstensi browser yang berjalan di browser Anda (Chrome, Firefox, Opera, atau Brave Browser). Dompet ini mudah digunakan dan nyaman untuk pengujian, karena dapat terhubung ke berbagai *node* Ethereum dan *blockchain* uji. MetaMask adalah dompet berbasis web.

**Jaxx**
Jaxx adalah dompet multiplatform dan multikurensi yang berjalan di berbagai sistem operasi, termasuk Android, iOS, Windows, macOS, dan Linux. Ini sering menjadi pilihan yang baik untuk pengguna baru karena dirancang untuk kesederhanaan dan kemudahan penggunaan. Jaxx bisa menjadi dompet seluler atau desktop, tergantung di mana Anda menginstalnya.

**MyEtherWallet (MEW)**
MyEtherWallet adalah dompet berbasis web yang berjalan di browser apa pun. Dompet ini memiliki banyak fitur canggih yang akan kita jelajahi dalam banyak contoh kita. MyEtherWallet adalah dompet berbasis web.

**Emerald Wallet**
Emerald Wallet dirancang untuk bekerja dengan *blockchain* Ethereum Classic, tetapi kompatibel dengan *blockchain* berbasis Ethereum lainnya. Ini adalah aplikasi desktop sumber terbuka dan bekerja di bawah Windows, macOS, dan Linux. Emerald Wallet dapat menjalankan *full node* atau terhubung ke *node* publik jarak jauh, bekerja dalam mode "ringan" (*light*). Dompet ini juga memiliki alat pendamping untuk melakukan semua operasi dari baris perintah (*command line*).

Kita akan mulai dengan menginstal MetaMask di desktop—tetapi pertama-tama, kita akan membahas secara singkat tentang mengontrol dan mengelola kunci.

### **Kontrol dan Tanggung Jawab**

*Blockchain* terbuka seperti Ethereum itu penting karena beroperasi sebagai sistem terdesentralisasi. Itu berarti banyak hal, tetapi satu aspek krusial adalah bahwa setiap pengguna Ethereum dapat—dan seharusnya—**mengontrol kunci privat mereka sendiri**, yang merupakan hal yang mengontrol akses ke dana dan *smart contract*. Terkadang kita menyebut kombinasi akses ke dana dan *smart contract* sebagai "akun" atau "dompet". Istilah-istilah ini bisa menjadi cukup kompleks dalam fungsionalitasnya, jadi kita akan membahas ini lebih detail nanti. Namun, sebagai prinsip dasar, sesederhana **satu kunci privat sama dengan satu "akun."**

Beberapa pengguna memilih untuk menyerahkan kontrol atas kunci privat mereka dengan menggunakan kustodian pihak ketiga, seperti bursa daring (*online exchange*). Dalam buku ini, kami akan mengajari Anda cara mengambil kendali dan mengelola kunci privat Anda sendiri.

Dengan kontrol datanglah tanggung jawab besar. **Jika Anda kehilangan kunci privat, Anda kehilangan akses ke dana dan kontrak Anda.** Tidak ada yang bisa membantu Anda mendapatkan kembali akses—dana Anda akan terkunci selamanya. Berikut adalah beberapa tips untuk membantu Anda mengelola tanggung jawab ini:

* **Jangan mengimprovisasi keamanan.** Gunakan pendekatan standar yang sudah teruji.
* Semakin penting sebuah akun (misalnya, semakin tinggi nilai dana yang dikendalikan, atau semakin signifikan *smart contract* yang dapat diakses), semakin tinggi pula langkah-langkah keamanan yang harus diambil.
* Keamanan tertinggi diperoleh dari perangkat *air-gapped* (terisolasi dari jaringan), tetapi level ini tidak diperlukan untuk setiap akun.
* **Jangan pernah menyimpan kunci privat Anda dalam bentuk teks biasa**, terutama secara digital. Untungnya, sebagian besar antarmuka pengguna saat ini bahkan tidak akan membiarkan Anda melihat kunci privat mentahnya.
* Kunci privat dapat disimpan dalam bentuk terenkripsi, sebagai file "*keystore*" digital. Karena dienkripsi, kunci tersebut memerlukan kata sandi untuk membukanya. Saat Anda diminta untuk memilih kata sandi, **buatlah yang kuat** (yaitu, panjang dan acak), cadangkan, dan jangan bagikan. Jika Anda tidak memiliki pengelola kata sandi, tuliskan dan simpan di tempat yang aman dan rahasia. Untuk mengakses akun Anda, Anda memerlukan file *keystore* dan kata sandinya.
* **Jangan menyimpan kata sandi apa pun** dalam dokumen digital, foto digital, tangkapan layar, drive daring, PDF terenkripsi, dll. Sekali lagi, jangan mengimprovisasi keamanan. Gunakan pengelola kata sandi atau pena dan kertas.
* Saat Anda diminta untuk mencadangkan kunci sebagai **urutan kata mnemonic**, gunakan pena dan kertas untuk membuat cadangan fisik. Jangan menunda tugas itu "untuk nanti"; Anda akan lupa. Cadangan ini dapat digunakan untuk membangun kembali kunci privat Anda jika Anda kehilangan semua data yang tersimpan di sistem Anda, atau jika Anda lupa atau kehilangan kata sandi. Namun, mereka juga dapat digunakan oleh penyerang untuk mendapatkan kunci privat Anda, jadi **jangan pernah menyimpannya secara digital**, dan simpan salinan fisiknya dengan aman di laci atau brankas yang terkunci.
* Sebelum mentransfer jumlah besar (terutama ke alamat baru), **lakukan transaksi uji coba kecil terlebih dahulu** (misalnya, senilai kurang dari $1) dan tunggu konfirmasi penerimaan.
* Saat Anda membuat akun baru, mulailah dengan hanya mengirim transaksi uji coba kecil ke alamat baru tersebut. Setelah Anda menerima transaksi uji coba, coba kirim kembali dari akun itu. Ada banyak alasan pembuatan akun bisa salah, dan jika salah, lebih baik mengetahuinya dengan kerugian kecil. Jika pengujian berhasil, semuanya baik-baik saja.
* Penjelajah blok (*block explorer*) publik adalah cara mudah untuk melihat secara independen apakah sebuah transaksi telah diterima oleh jaringan. Namun, kemudahan ini berdampak negatif pada privasi Anda, karena Anda mengungkapkan alamat Anda ke penjelajah blok, yang dapat melacak Anda.
* **Jangan mengirim uang ke alamat mana pun yang ditampilkan dalam buku ini.** Kunci privatnya tercantum di dalam buku dan seseorang akan segera mengambil uang itu.

Sekarang setelah kita membahas beberapa praktik terbaik dasar untuk manajemen kunci dan keamanan, mari kita mulai menggunakan MetaMask!

### **Memulai dengan MetaMask**

Buka browser Google Chrome dan navigasikan ke [https://chrome.google.com/webstore/category/extensions](https://chrome.google.com/webstore/category/extensions).

Cari "MetaMask" dan klik pada logo rubah. Anda akan melihat sesuatu seperti hasil yang ditunjukkan pada Gambar 2-1.

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.1.png" alt="gambar" width="580"/>
</p>

Penting untuk memverifikasi bahwa Anda mengunduh ekstensi MetaMask yang asli, karena terkadang orang dapat menyelundupkan ekstensi berbahaya melewati filter Google. Yang asli:

* Menunjukkan ID `nkbihfbeogaeaoehlefnkodbefgpgknn` di bilah alamat (*address bar*)
* Ditawarkan oleh [https://metamask.io](https://metamask.io)
* Memiliki lebih dari 1.400 ulasan
* Memiliki lebih dari 1.000.000 pengguna

Setelah Anda memastikan sedang melihat ekstensi yang benar, klik "**Tambahkan ke Chrome**" untuk menginstalnya.

### **Membuat Dompet**

Setelah MetaMask terinstal, Anda akan melihat ikon baru (kepala rubah) di bilah alat (*toolbar*) browser Anda. Klik ikon tersebut untuk memulai. Anda akan diminta untuk menyetujui syarat dan ketentuan, lalu membuat dompet Ethereum baru Anda dengan memasukkan kata sandi (lihat Gambar 2-2).

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.2.png" alt="gambar" width="580"/>
</p>

> Kata sandi ini mengontrol akses ke MetaMask, sehingga tidak dapat digunakan oleh siapa pun yang memiliki akses ke browser Anda.

Setelah Anda mengatur kata sandi, MetaMask akan membuat dompet untuk Anda dan menunjukkan cadangan mnemonic yang terdiri dari 12 kata dalam bahasa Inggris (lihat Gambar 2-3). Kata-kata ini dapat digunakan di dompet kompatibel mana pun untuk memulihkan akses ke dana Anda jika terjadi sesuatu pada MetaMask atau komputer Anda. **Anda tidak memerlukan kata sandi untuk pemulihan ini; 12 kata tersebut sudah cukup.**

> **Peringatan Keamanan** ✍️
>
> Cadangkan mnemonic Anda (12 kata) **di atas kertas, sebanyak dua kali**. Simpan kedua cadangan kertas di dua lokasi aman yang terpisah, seperti brankas tahan api, laci terkunci, atau kotak deposit. Perlakukan cadangan kertas ini seperti uang tunai dengan nilai yang setara dengan apa yang Anda simpan di dompet Ethereum Anda. **Siapa pun yang memiliki akses ke kata-kata ini dapat memperoleh akses dan mencuri uang Anda.**

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.3.png" alt="gambar" width="580"/>
</p>

Setelah Anda mengkonfirmasi bahwa Anda telah menyimpan mnemonic dengan aman, Anda akan dapat
Untuk melihat detail akun Ethereum Anda, seperti yang ditunjukkan pada Gambar 2-4.

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.4.png" alt="gambar" width="580"/>
</p>

Halaman akun Anda menampilkan nama akun Anda ("Akun 1" secara default), sebuah alamat Ethereum (`0x9E713…` dalam contoh), dan ikon berwarna-warni untuk membantu Anda membedakan akun ini secara visual dari akun lain. Di bagian atas halaman akun, Anda dapat melihat jaringan Ethereum mana yang sedang Anda gunakan ("Jaringan Utama" dalam contoh).

Selamat! Anda telah menyiapkan dompet Ethereum pertama Anda.

### **Beralih Jaringan**

Seperti yang dapat Anda lihat di halaman akun MetaMask, Anda dapat memilih di antara beberapa jaringan Ethereum. Secara default, MetaMask akan mencoba terhubung ke jaringan utama. Pilihan lainnya adalah *testnet* publik, *node* Ethereum apa pun pilihan Anda, atau *node* yang menjalankan *blockchain* privat di komputer Anda sendiri (*localhost*):

**Main Ethereum Network (Jaringan Utama Ethereum)**
*Blockchain* publik utama Ethereum. ETH asli, nilai nyata, dan konsekuensi nyata.

**Ropsten Test Network (Jaringan Uji Ropsten)**
*Blockchain* dan jaringan uji publik Ethereum. ETH di jaringan ini tidak memiliki nilai.

**Kovan Test Network (Jaringan Uji Kovan)**
*Blockchain* dan jaringan uji publik Ethereum yang menggunakan protokol konsensus Aura dengan *proof of authority* (penandatanganan terfederasi). ETH di jaringan ini tidak memiliki nilai. Jaringan uji Kovan hanya didukung oleh Parity. Klien Ethereum lainnya menggunakan protokol konsensus Clique, yang diusulkan kemudian, untuk verifikasi berbasis *proof of authority*.

**Rinkeby Test Network (Jaringan Uji Rinkeby)**
*Blockchain* dan jaringan uji publik Ethereum, yang menggunakan protokol konsensus Clique dengan *proof of authority* (penandatanganan terfederasi). ETH di jaringan ini tidak memiliki nilai.

**Localhost 8545**
Terhubung ke *node* yang berjalan di komputer yang sama dengan browser. *Node* tersebut dapat menjadi bagian dari *blockchain* publik mana pun (utama atau *testnet*), atau *testnet* privat.

**Custom RPC (RPC Kustom)**
Memungkinkan Anda untuk menghubungkan MetaMask ke *node* mana pun dengan antarmuka *Remote Procedure Call* (RPC) yang kompatibel dengan Geth. *Node* tersebut bisa menjadi bagian dari *blockchain* publik atau privat mana pun.

> Dompet MetaMask Anda menggunakan kunci privat dan alamat Ethereum yang sama di semua jaringan yang terhubung dengannya. Namun, saldo alamat Ethereum Anda di setiap jaringan Ethereum akan berbeda. Kunci Anda mungkin mengontrol ether dan kontrak di Ropsten, misalnya, tetapi tidak di jaringan utama.

### **Mendapatkan Ether Uji Coba**

Tugas pertama Anda adalah mendanai dompet Anda. Anda tidak akan melakukannya di jaringan utama karena ether sungguhan membutuhkan uang dan menanganinya memerlukan sedikit lebih banyak pengalaman. Untuk saat ini, Anda akan mengisi dompet Anda dengan ether dari *testnet*.

Alihkan MetaMask ke **Jaringan Uji Ropsten**. Klik **Beli**, lalu klik **Ropsten Test Faucet**. MetaMask akan membuka halaman web baru, seperti yang ditunjukkan pada Gambar 2-5.

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.5.png" alt="gambar" width="580"/>
</p>

Anda mungkin memperhatikan bahwa halaman web tersebut sudah berisi alamat Ethereum dari dompet MetaMask Anda. MetaMask mengintegrasikan halaman web yang mendukung Ethereum dengan dompet MetaMask Anda dan dapat "melihat" alamat Ethereum di halaman web, memungkinkan Anda, misalnya, untuk mengirim pembayaran ke toko daring yang menampilkan alamat Ethereum. MetaMask juga dapat mengisi halaman web dengan alamat dompet Anda sendiri sebagai alamat penerima jika halaman web tersebut memintanya. Di halaman ini, aplikasi *faucet* meminta alamat dompet dari MetaMask untuk mengirimkan ether uji coba.

Klik tombol hijau "**request 1 ether from faucet**". Anda akan melihat ID transaksi muncul di bagian bawah halaman. Aplikasi *faucet* telah membuat sebuah transaksi—pembayaran untuk Anda. ID transaksi terlihat seperti ini:

`0x7c7ad5aaea6474adccf6f5c5d6abed11b70a350fbc6f9590109e099568090c57`

Dalam beberapa detik, transaksi baru akan ditambang oleh para penambang Ropsten dan dompet MetaMask Anda akan menunjukkan saldo sebesar 1 ETH. Klik pada ID transaksi dan browser Anda akan membawa Anda ke penjelajah blok (*block explorer*), yaitu sebuah situs web yang memungkinkan Anda untuk memvisualisasikan dan menjelajahi blok, alamat, dan transaksi. MetaMask menggunakan penjelajah blok **Etherscan**, salah satu penjelajah blok Ethereum yang lebih populer. Transaksi yang berisi pembayaran dari Ropsten Test Faucet ditunjukkan pada Gambar 2-6.

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.6.png" alt="gambar" width="580"/>
</p>

[Gambar 2-6: Tampilan transaksi pembayaran dari faucet di Etherscan]

Transaksi tersebut telah dicatat di *blockchain* Ropsten dan dapat dilihat kapan saja oleh siapa saja, hanya dengan mencari ID transaksi, atau mengunjungi tautan tersebut. Coba kunjungi tautan itu, atau masukkan *hash* transaksi ke situs web `ropsten.etherscan.io`, untuk melihatnya sendiri.

### **Mengirim Ether dari MetaMask**

Setelah Anda menerima ether uji coba pertama Anda dari Ropsten Test Faucet, Anda dapat bereksperimen dengan mengirim ether dengan mencoba mengirim sebagian kembali ke *faucet*. Seperti yang Anda lihat di halaman Ropsten Test Faucet, ada pilihan untuk "menyumbang" 1 ETH ke *faucet*. Opsi ini tersedia agar setelah Anda selesai menguji, Anda dapat mengembalikan sisa ether uji coba Anda, sehingga orang lain dapat menggunakannya selanjutnya. Meskipun ether uji coba tidak memiliki nilai, beberapa orang menimbunnya, sehingga menyulitkan orang lain untuk menggunakan jaringan uji. Menimbun ether uji coba sangat tidak disukai!

Untungnya, kita bukanlah penimbun ether uji coba. Klik tombol oranye "**1 ether**" untuk memberitahu MetaMask agar membuat transaksi pembayaran 1 ether ke *faucet*. MetaMask akan menyiapkan transaksi dan memunculkan jendela konfirmasi, seperti yang ditunjukkan pada Gambar 2-7.

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.7.png" alt="gambar" width="580"/>
</p>

[Gambar 2-7: Jendela konfirmasi transaksi pengiriman di MetaMask]

Ups! Anda mungkin menyadari bahwa Anda tidak dapat menyelesaikan transaksi—MetaMask mengatakan saldo Anda tidak mencukupi. Sekilas ini mungkin tampak membingungkan: Anda memiliki 1 ETH, Anda ingin mengirim 1 ETH, jadi mengapa MetaMask mengatakan dana Anda tidak cukup?

Jawabannya adalah karena **biaya gas**. Setiap transaksi Ethereum memerlukan pembayaran biaya, yang dikumpulkan oleh para penambang untuk memvalidasi transaksi. Biaya di Ethereum dibebankan dalam mata uang virtual yang disebut **gas**. Anda membayar gas dengan ether, sebagai bagian dari transaksi.

> Biaya juga diperlukan di jaringan uji. Tanpa biaya, jaringan uji akan berperilaku berbeda dari jaringan utama, membuatnya menjadi platform pengujian yang tidak memadai. Biaya juga melindungi jaringan uji dari serangan DoS dan kontrak yang dibuat dengan buruk (misalnya, *infinite loops*), sama seperti mereka melindungi jaringan utama.

Saat Anda mengirim transaksi, MetaMask menghitung harga gas rata-rata dari transaksi yang berhasil baru-baru ini sebesar 3 **gwei**, yang merupakan singkatan dari gigawei. Wei adalah subdivisi terkecil dari mata uang ether, seperti yang kita bahas di "Unit Mata Uang Ether" di halaman 13. Batas gas ditetapkan pada biaya pengiriman transaksi dasar, yaitu 21.000 unit gas. Oleh karena itu, jumlah maksimum ETH yang akan Anda keluarkan adalah 3 * 21.000 gwei = 63.000 gwei = 0,000063 ETH. (Perlu diketahui bahwa harga gas rata-rata dapat berfluktuasi, karena sebagian besar ditentukan oleh penambang. Kita akan melihat di bab selanjutnya bagaimana Anda dapat menaikkan/menurunkan batas gas Anda untuk memastikan transaksi Anda diprioritaskan jika diperlukan.)

Semua ini berarti: melakukan transaksi 1 ETH membutuhkan biaya 1,000063 ETH. MetaMask secara membingungkan membulatkannya menjadi 1 ETH saat menampilkan total, tetapi jumlah sebenarnya yang Anda butuhkan adalah 1,000063 ETH dan Anda hanya memiliki 1 ETH. Klik **Tolak** untuk membatalkan transaksi ini.

Mari kita dapatkan lebih banyak ether uji coba! Klik tombol hijau "request 1 ether from the faucet" lagi dan tunggu beberapa detik. Jangan khawatir, *faucet* seharusnya memiliki banyak ether dan akan memberi Anda lebih banyak jika Anda meminta.

Setelah Anda memiliki saldo 2 ETH, Anda bisa mencoba lagi. Kali ini, saat Anda mengklik tombol donasi oranye "1 ether", Anda memiliki saldo yang cukup untuk menyelesaikan transaksi. Klik **Kirim** saat MetaMask memunculkan jendela pembayaran. Setelah semua ini, Anda akan melihat saldo sebesar 0,999937 ETH karena Anda mengirim 1 ETH ke *faucet* dengan biaya gas sebesar 0,000063 ETH.

### **Menjelajahi Riwayat Transaksi Sebuah Alamat**

Sekarang Anda telah menjadi ahli dalam menggunakan MetaMask untuk mengirim dan menerima ether uji coba. Dompet Anda telah menerima setidaknya dua pembayaran dan mengirim setidaknya satu. Anda dapat melihat semua transaksi ini menggunakan penjelajah blok `ropsten.etherscan.io`. Anda bisa menyalin alamat dompet Anda dan menempelkannya ke kotak pencarian penjelajah blok, atau meminta MetaMask membukakan halaman untuk Anda. Di sebelah ikon akun Anda di MetaMask, Anda akan melihat tombol yang menunjukkan tiga titik. Klik tombol itu untuk menampilkan menu opsi terkait akun (lihat Gambar 2-8).

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.8.png" alt="gambar" width="580"/>
</p>

[Gambar 2-8: Menu opsi akun di MetaMask]

Pilih "**Lihat akun di Etherscan**" untuk membuka halaman web di penjelajah blok yang menunjukkan riwayat transaksi akun Anda, seperti yang ditunjukkan pada Gambar 2-9.

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.9.png" alt="gambar" width="580"/>
</p>

[Gambar 2-9: Riwayat transaksi sebuah alamat di Etherscan]

Di sini Anda dapat melihat seluruh riwayat transaksi alamat Ethereum Anda. Ini menunjukkan semua transaksi yang tercatat di *blockchain* Ropsten di mana alamat Anda adalah pengirim atau penerima. Klik beberapa transaksi ini untuk melihat detail lebih lanjut.

Anda dapat menjelajahi riwayat transaksi dari alamat mana pun. Coba lihat riwayat transaksi alamat Ropsten Test Faucet (petunjuk: itu adalah alamat "pengirim" yang tercantum dalam pembayaran tertua ke alamat Anda). Anda dapat melihat semua ether uji coba yang dikirim dari *faucet* kepada Anda dan ke alamat lain. Setiap transaksi yang Anda lihat dapat membawa Anda ke lebih banyak alamat dan lebih banyak transaksi. Tak lama kemudian Anda akan tersesat dalam labirin data yang saling terhubung. *Blockchain* publik berisi kekayaan informasi yang sangat besar, yang semuanya dapat dieksplorasi secara terprogram, seperti yang akan kita lihat dalam contoh-contoh di masa depan.

### **Memperkenalkan Komputer Dunia**

Anda sekarang telah membuat dompet serta mengirim dan menerima ether. Sejauh ini, kita telah memperlakukan Ethereum sebagai mata uang kripto. Tetapi Ethereum jauh, jauh lebih dari itu. Faktanya, fungsi mata uang kripto hanyalah pendukung fungsi Ethereum sebagai **komputer dunia yang terdesentralisasi**. Ether dimaksudkan untuk digunakan membayar biaya menjalankan *smart contract*, yang merupakan program komputer yang berjalan di atas komputer emulasi yang disebut **Ethereum Virtual Machine (EVM)**.

EVM adalah sebuah *global singleton*, yang berarti ia beroperasi seolah-olah ia adalah komputer instans tunggal global, yang berjalan di mana-mana. Setiap *node* di jaringan Ethereum menjalankan salinan lokal dari EVM untuk memvalidasi eksekusi kontrak, sementara *blockchain* Ethereum mencatat perubahan keadaan dari komputer dunia ini saat memproses transaksi dan *smart contract*. Kita akan membahas ini secara lebih rinci di Bab 13.

### **Externally Owned Accounts (EOA) dan Kontrak**

Jenis akun yang Anda buat di dompet MetaMask disebut **externally owned account (EOA)** atau akun yang dimiliki secara eksternal. EOA adalah akun yang memiliki kunci privat; memiliki kunci privat berarti memiliki kendali atas akses ke dana atau kontrak. Sekarang, Anda mungkin menebak ada jenis akun lain. Jenis akun lainnya adalah **akun kontrak**. Akun kontrak memiliki kode *smart contract*, yang tidak dimiliki oleh EOA biasa. Selain itu, akun kontrak **tidak memiliki kunci privat**. Sebaliknya, ia dimiliki (dan dikendalikan) oleh logika kode *smart contract*-nya: program perangkat lunak yang dicatat di *blockchain* Ethereum saat pembuatan akun kontrak dan dieksekusi oleh EVM.

Kontrak memiliki alamat, sama seperti EOA. Kontrak juga dapat mengirim dan menerima ether, sama seperti EOA. Namun, ketika tujuan transaksi adalah alamat kontrak, hal itu menyebabkan kontrak tersebut berjalan di EVM, menggunakan transaksi, dan data transaksi, sebagai inputnya. Selain ether, transaksi dapat berisi data yang menunjukkan fungsi spesifik mana dalam kontrak yang harus dijalankan dan parameter apa yang harus diteruskan ke fungsi tersebut. Dengan cara ini, transaksi dapat memanggil fungsi di dalam kontrak.

Perhatikan bahwa karena akun kontrak tidak memiliki kunci privat, ia tidak dapat **memulai** sebuah transaksi. Hanya EOA yang dapat memulai transaksi, tetapi kontrak dapat bereaksi terhadap transaksi dengan memanggil kontrak lain, membangun alur eksekusi yang kompleks. Salah satu penggunaan umum dari ini adalah EOA yang mengirimkan transaksi permintaan ke dompet *smart contract* multisignature untuk mengirim sejumlah ETH ke alamat lain. Pola pemrograman DApp yang umum adalah memiliki Kontrak A memanggil Kontrak B untuk menjaga keadaan bersama di antara para pengguna Kontrak A.

Dalam beberapa bagian berikutnya, kita akan menulis kontrak pertama kita. Anda kemudian akan belajar cara membuat, mendanai, dan menggunakan kontrak tersebut dengan dompet MetaMask dan ether uji coba di jaringan uji Ropsten.
### **Kontrak Sederhana: Sebuah Faucet Ether Uji Coba**

Ethereum memiliki banyak bahasa tingkat tinggi yang berbeda, yang semuanya dapat digunakan untuk menulis kontrak dan menghasilkan *bytecode* EVM. Anda dapat membaca tentang banyak bahasa yang paling terkemuka dan menarik di "Pengantar Bahasa Tingkat Tinggi Ethereum" di halaman 129. Salah satu bahasa tingkat tinggi sejauh ini merupakan pilihan dominan untuk pemrograman *smart contract*: **Solidity**. Solidity diciptakan oleh Dr. Gavin Wood, salah satu penulis buku ini, dan telah menjadi bahasa yang paling banyak digunakan di Ethereum (dan di luarnya). Kita akan menggunakan Solidity untuk menulis kontrak pertama kita.

Untuk contoh pertama kita (Contoh 2-1), kita akan menulis kontrak yang mengontrol sebuah *faucet*. Anda sudah menggunakan *faucet* untuk mendapatkan ether uji coba di jaringan uji Ropsten. *Faucet* adalah hal yang relatif sederhana: ia memberikan ether ke alamat mana pun yang meminta, dan dapat diisi ulang secara berkala. Anda dapat mengimplementasikan *faucet* sebagai dompet yang dikendalikan oleh manusia atau server web.

**Contoh 2-1. Faucet.sol: Sebuah kontrak Solidity yang mengimplementasikan sebuah faucet**

```solidity
1 // Kontrak pertama kita adalah sebuah faucet!
2 contract Faucet {
3
4   // Berikan ether kepada siapa pun yang meminta
5   function withdraw(uint withdraw_amount) public {
6
7       // Batasi jumlah penarikan
8       require(withdraw_amount <= 100000000000000000);
9
10      // Kirim jumlah tersebut ke alamat yang memintanya
11      msg.sender.transfer(withdraw_amount);
12  }
13
14  // Terima jumlah masuk berapa pun
15  function () public payable {}
16
17 }
```

> Anda akan menemukan semua contoh kode untuk buku ini di subdirektori `code` dari repositori GitHub buku ini. Secara spesifik, kontrak `Faucet.sol` kita berada di:
> `code/Solidity/Faucet.sol`

Ini adalah kontrak yang sangat sederhana, sesederhana yang bisa kita buat. Ini juga merupakan kontrak yang **cacat**, menunjukkan sejumlah praktik buruk dan kerentanan keamanan. Kita akan belajar dengan memeriksa semua kekurangannya di bagian selanjutnya. Tapi untuk saat ini, mari kita lihat apa yang dilakukan kontrak ini dan cara kerjanya, baris per baris. Anda akan segera menyadari bahwa banyak elemen soliditas mirip dengan bahasa pemrograman yang ada, seperti JavaScript, Java, atau C ++.

Baris pertama adalah sebuah komentar:

```solidity
// Kontrak pertama kita adalah sebuah faucet!
```

Komentar ditujukan untuk dibaca oleh manusia dan tidak disertakan dalam *bytecode* EVM yang dapat dieksekusi. Biasanya kita meletakkannya di baris sebelum kode yang ingin kita jelaskan, atau terkadang di baris yang sama. Komentar dimulai dengan dua garis miring: `//`. Segala sesuatu dari garis miring pertama hingga akhir baris tersebut diperlakukan sama seperti baris kosong dan diabaikan.

Baris berikutnya adalah tempat di mana kontrak kita sebenarnya dimulai:

```solidity
contract Faucet {
```

Baris ini mendeklarasikan sebuah objek `contract`, mirip dengan deklarasi `class` di bahasa berorientasi objek lainnya. Definisi kontrak mencakup semua baris di antara kurung kurawal (`{}`), yang mendefinisikan sebuah lingkup (*scope*), sama seperti bagaimana kurung kurawal digunakan di banyak bahasa pemrograman lain.

Selanjutnya, kita mendeklarasikan fungsi pertama dari kontrak `Faucet`:

```solidity
function withdraw(uint withdraw_amount) public {
```

Fungsi ini bernama `withdraw`, dan menerima satu argumen integer tak bertanda (`uint`) bernama `withdraw_amount`. Fungsi ini dideklarasikan sebagai fungsi `public`, yang berarti dapat dipanggil oleh kontrak lain. Definisi fungsi mengikuti, di antara kurung kurawal. Bagian pertama dari fungsi `withdraw` menetapkan batas penarikan:

```solidity
require(withdraw_amount <= 100000000000000000);
```

Fungsi ini menggunakan fungsi bawaan Solidity, `require`, untuk menguji sebuah prasyarat, yaitu `withdraw_amount` harus kurang dari atau sama dengan 100.000.000.000.000.000 wei, yang merupakan unit dasar ether (lihat Tabel 2-1) dan setara dengan 0,1 ether. Jika fungsi `withdraw` dipanggil dengan `withdraw_amount` yang lebih besar dari jumlah itu, fungsi `require` di sini akan menyebabkan eksekusi kontrak berhenti dan gagal dengan sebuah pengecualian (*exception*). Perhatikan bahwa pernyataan di Solidity harus diakhiri dengan titik koma.

Bagian dari kontrak ini adalah logika utama dari *faucet* kita. Bagian ini mengontrol aliran dana keluar dari kontrak dengan menempatkan batasan pada penarikan. Ini adalah kontrol yang sangat sederhana tetapi dapat memberi Anda gambaran sekilas tentang kekuatan *blockchain* yang dapat diprogram: perangkat lunak terdesentralisasi yang mengendalikan uang.

Berikutnya adalah penarikan yang sebenarnya:

```solidity
msg.sender.transfer(withdraw_amount);
```

Beberapa hal menarik terjadi di sini. Objek `msg` adalah salah satu input yang dapat diakses oleh semua kontrak. Objek ini mewakili transaksi yang memicu eksekusi kontrak ini. Atribut `sender` adalah alamat pengirim dari transaksi tersebut. Fungsi `transfer` adalah fungsi bawaan yang mentransfer ether dari kontrak saat ini ke alamat pengirim. Jika dibaca dari belakang, ini berarti **transfer ke pengirim `msg` yang memicu eksekusi kontrak ini**. Fungsi `transfer` menerima jumlah sebagai satu-satunya argumen. Kita meneruskan nilai `withdraw_amount` yang merupakan parameter untuk fungsi `withdraw` yang dideklarasikan beberapa baris sebelumnya.

Baris berikutnya adalah kurung kurawal penutup, yang menandakan akhir dari definisi fungsi `withdraw` kita.

Selanjutnya, kita mendeklarasikan satu fungsi lagi:

```solidity
function () public payable {}
```

Fungsi ini adalah apa yang disebut fungsi *fallback* atau **default**, yang dipanggil jika transaksi yang memicu kontrak tidak menyebutkan nama fungsi apa pun yang dideklarasikan dalam kontrak, atau tidak ada fungsi sama sekali, atau tidak berisi data. Kontrak dapat memiliki satu fungsi default seperti ini (tanpa nama) dan biasanya inilah yang menerima ether. Itulah mengapa fungsi ini didefinisikan sebagai fungsi `public` dan `payable`, yang berarti dapat menerima ether ke dalam kontrak. Fungsi ini tidak melakukan apa-apa, selain menerima ether, seperti yang ditunjukkan oleh definisi kosong dalam kurung kurawal (`{}`). Jika kita membuat transaksi yang mengirim ether ke alamat kontrak, seolah-olah itu adalah dompet, fungsi ini akan menanganinya.

Tepat di bawah fungsi default kita adalah kurung kurawal penutup terakhir, yang menutup definisi dari kontrak `Faucet`. Selesai\!

### **Mengkompilasi Kontrak Faucet**

Sekarang kita memiliki kontrak contoh pertama kita, kita perlu menggunakan *compiler* Solidity untuk mengubah kode Solidity menjadi *bytecode* EVM sehingga dapat dieksekusi oleh EVM di *blockchain* itu sendiri.

*Compiler* Solidity tersedia sebagai *executable* mandiri, sebagai bagian dari berbagai kerangka kerja, dan dibundel dalam Lingkungan Pengembangan Terpadu (IDE). Agar tetap sederhana, kita akan menggunakan salah satu IDE yang lebih populer, bernama **Remix**.

Gunakan browser Chrome Anda (dengan dompet MetaMask yang telah Anda instal sebelumnya) untuk menavigasi ke Remix IDE di [https://remix.ethereum.org](https://remix.ethereum.org).

Saat Anda pertama kali memuat Remix, ia akan dimulai dengan contoh kontrak bernama `ballot.sol`. Kita tidak memerlukannya, jadi tutup dengan mengklik `x` di sudut tab, seperti yang terlihat pada Gambar 2-10.

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.10.png" alt="gambar" width="580"/>
</p>

[Gambar 2-10: Menutup file default di Remix IDE]

Sekarang, tambahkan tab baru dengan mengklik tanda tambah melingkar di bilah alat kiri atas, seperti yang terlihat pada Gambar 2-11. Beri nama file baru `Faucet.sol`.

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.11.png" alt="gambar" width="580"/>
</p>

[Gambar 2-11: Menambahkan file baru di Remix IDE]

Setelah Anda membuka tab baru, salin dan tempel kode dari contoh `Faucet.sol` kita, seperti yang terlihat pada Gambar 2-12.

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.12.png" alt="gambar" width="580"/>
</p>

[Gambar 2-12: Menempelkan kode Faucet.sol ke Remix IDE]

Setelah Anda memuat kontrak `Faucet.sol` ke dalam Remix IDE, IDE akan secara otomatis mengkompilasi kode tersebut. Jika semua berjalan lancar, Anda akan melihat kotak hijau dengan tulisan "Faucet" di dalamnya muncul di sebelah kanan, di bawah tab **Compile**, yang mengonfirmasi kompilasi berhasil (lihat Gambar 2-13).

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.13.png" alt="gambar" width="580"/>
</p>

[Gambar 2-13: Konfirmasi kompilasi berhasil di Remix IDE]

> Jika terjadi kesalahan, masalah yang paling mungkin adalah Remix IDE menggunakan versi *compiler* Solidity yang berbeda dari 0.4.19. Dalam hal ini, arahan `pragma` kita akan mencegah `Faucet.sol` untuk dikompilasi. Untuk mengubah versi *compiler*, buka tab **Settings**, atur versi ke 0.4.19, dan coba lagi.

*Compiler* Solidity sekarang telah mengkompilasi `Faucet.sol` kita menjadi *bytecode* EVM. Jika Anda penasaran, *bytecode*-nya terlihat seperti ini:

```
PUSH1 0x60 PUSH1 0x40 MSTORE CALLVALUE ISZERO PUSH2 0xF JUMPI PUSH1 0x0 DUP1
REVERT JUMPDEST PUSH1 0xE5 DUP1 PUSH2 0x1D PUSH1 0x0 CODECOPY PUSH1 0x0 RETURN
STOP PUSH1 0x60 PUSH1 0x40 MSTORE PUSH1 0x4 CALLDATASIZE LT PUSH1 0x3F JUMPI
PUSH1 0x0 CALLDATALOAD PUSH29
0x100000000000000000000000000000000000000000000000000000000
SWAP1 DIV PUSH4 0xFFFFFFFF AND DUP1 PUSH4 0x2E1A7D4D EQ PUSH1 0x41 JUMPI
JUMPDEST STOP JUMPDEST CALLVALUE ISZERO PUSH1 0x4B JUMPI PUSH1 0x0 DUP1 REVERT
JUMPDEST PUSH1 0x5F PUSH1 0x4 DUP1 DUP1 CALLDATALOAD SWAP1 PUSH1 0x20 ADD SWAP1
SWAP2 SWAP1 POP POP PUSH1 0x61 JUMP JUMPDEST STOP JUMPDEST PUSH8
0x16345785D8A0000 DUP2 GT ISZERO ISZERO ISZERO PUSH1 0x77 JUMPI PUSH1 0x0 DUP1
REVERT JUMPDEST CALLER PUSH20 0xFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFFF AND
PUSH2 0x8FC DUP3 SWAP1 DUP2 ISZERO MUL SWAP1 PUSH1 0x40 MLOAD PUSH1 0x0 PUSH1
0x40 MLOAD DUP1 DUP4 SUB DUP2 DUP6 DUP9 DUP9 CALL SWAP4 POP POP POP POP ISZERO
ISZERO PUSH1 0xB6 JUMPI PUSH1 0x0 DUP1 REVERT JUMPDEST POP JUMP STOP LOG1 PUSH6
0x627A7A723058 KECCAK256 PUSH9 0x13D1EA839A4438EF75 GASLIMIT CALLVALUE LOG4 0x5f
PUSH24 0x7541F409787592C988A079407FB28B4AD000290000000000
```

Senang kan Anda menggunakan bahasa tingkat tinggi seperti Solidity alih-alih memprogram langsung dalam *bytecode* EVM? Saya juga\!

### **Membuat Kontrak di Blockchain**

Jadi, kita punya sebuah kontrak. Kita sudah mengkompilasinya menjadi *bytecode*. Sekarang, kita perlu "mendaftarkan" kontrak tersebut di *blockchain* Ethereum. Kita akan menggunakan *testnet* Ropsten untuk menguji kontrak kita, jadi itulah *blockchain* tempat kita ingin mengirimkannya.

Mendaftarkan kontrak di *blockchain* melibatkan pembuatan transaksi khusus yang tujuannya adalah alamat `0x0000000000000000000000000000000000000000`, yang juga dikenal sebagai **alamat nol**. Alamat nol adalah alamat khusus yang memberitahu *blockchain* Ethereum bahwa Anda ingin mendaftarkan sebuah kontrak. Untungnya, Remix IDE akan menangani semua itu untuk Anda dan mengirimkan transaksi ke MetaMask.

Pertama, beralih ke tab **Run** dan pilih **Injected Web3** di kotak pilihan *drop-down* **Environment**. Ini menghubungkan Remix IDE ke dompet MetaMask, dan melalui MetaMask ke jaringan uji Ropsten. Setelah Anda melakukannya, Anda dapat melihat **Ropsten** di bawah Environment. Juga, di kotak pilihan **Account** akan ditampilkan alamat dompet Anda (lihat Gambar 2-14).

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.14.png" alt="gambar" width="580"/>
</p>

[Gambar 2-14: Mengkonfigurasi lingkungan 'Run' di Remix untuk men-deploy kontrak]

Tepat di bawah pengaturan Run yang baru saja Anda konfirmasi adalah kontrak `Faucet`, siap untuk dibuat. Klik tombol **Deploy** yang ditunjukkan pada Gambar 2-14.

Remix akan membuat transaksi "pembuatan" khusus dan MetaMask akan meminta Anda untuk menyetujuinya, seperti yang ditunjukkan pada Gambar 2-15. Anda akan melihat transaksi pembuatan kontrak tidak berisi ether, tetapi memiliki 258 byte data (kontrak yang dikompilasi) dan akan mengonsumsi 10 gwei gas. Klik **Submit** untuk menyetujuinya

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.15.png" alt="gambar" width="580"/>
</p>

[Gambar 2-15: Jendela konfirmasi MetaMask untuk transaksi pembuatan kontrak]

Sekarang Anda harus menunggu. Butuh waktu sekitar 15 hingga 30 detik agar kontrak ditambang di Ropsten. Remix mungkin tidak akan terlihat melakukan banyak hal, tetapi bersabarlah.

Setelah kontrak dibuat, ia akan muncul di bagian bawah tab **Run** (lihat Gambar 2-16).

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.16.png" alt="gambar" width="580"/>
</p>

[Gambar 2-16: Kontrak yang telah di-*deploy* ditampilkan di tab Run Remix]

Perhatikan bahwa kontrak `Faucet` sekarang memiliki alamatnya sendiri: Remix menampilkannya sebagai "**Faucet at 0x72e…c7829**" (meskipun alamat Anda, yang berupa huruf dan angka acak, akan berbeda). Simbol papan klip (*clipboard*) kecil di sebelah kanan memungkinkan Anda untuk menyalin alamat kontrak ke papan klip Anda. Kita akan menggunakannya di bagian selanjutnya.

### **Berinteraksi dengan Kontrak**

Mari kita rekap apa yang telah kita pelajari sejauh ini: Kontrak Ethereum adalah program yang mengendalikan uang, yang berjalan di dalam mesin virtual yang disebut EVM. Kontrak ini dibuat oleh transaksi khusus yang mengirimkan *bytecode* mereka untuk dicatat di *blockchain*. Setelah dibuat di *blockchain*, mereka memiliki alamat Ethereum, sama seperti dompet. Setiap kali seseorang mengirim transaksi ke alamat kontrak, hal itu akan menyebabkan kontrak berjalan di EVM, dengan transaksi tersebut sebagai inputnya. Transaksi yang dikirim ke alamat kontrak dapat berisi ether atau data, atau keduanya. Jika mengandung ether, ether tersebut akan "disetorkan" ke saldo kontrak. Jika mengandung data, data tersebut dapat menentukan fungsi bernama di dalam kontrak dan memanggilnya, serta meneruskan argumen ke fungsi tersebut.

#### **Melihat Alamat Kontrak di Penjelajah Blok**

Sekarang kita memiliki kontrak yang tercatat di *blockchain*, dan kita dapat melihat ia memiliki alamat Ethereum. Mari kita periksa di penjelajah blok `ropsten.etherscan.io` dan lihat seperti apa bentuk sebuah kontrak. Di Remix IDE, salin alamat kontrak dengan mengklik ikon papan klip di sebelah namanya (lihat Gambar 2-17).

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.17.png" alt="gambar" width="580"/>
</p>

[Gambar 2-17: Menyalin alamat kontrak Faucet dari Remix IDE]

Biarkan Remix tetap terbuka; kita akan kembali lagi nanti. Sekarang, arahkan browser Anda ke `ropsten.etherscan.io` dan tempelkan alamat tersebut ke dalam kotak pencarian. Anda akan melihat riwayat alamat Ethereum kontrak tersebut, seperti yang ditunjukkan pada Gambar 2-18.\

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.18.png" alt="gambar" width="580"/>
</p>

[Gambar 2-18: Riwayat alamat kontrak Faucet di Etherscan]

### **Mendanai Kontrak**

Untuk saat ini, kontrak tersebut hanya memiliki satu transaksi dalam riwayatnya: transaksi pembuatan kontrak. Seperti yang Anda lihat, kontrak tersebut juga tidak memiliki ether (saldo nol). Itu karena kita tidak mengirim ether apa pun ke kontrak dalam transaksi pembuatan, meskipun kita bisa saja melakukannya.

*Faucet* kita butuh dana\! Proyek pertama kita adalah menggunakan MetaMask untuk mengirim ether ke kontrak. Alamat kontrak seharusnya masih ada di papan klip Anda (jika tidak, salin lagi dari Remix). Buka MetaMask, dan kirim 1 ether ke alamat tersebut, persis seperti yang Anda lakukan ke alamat Ethereum lainnya (lihat Gambar 2-19).
<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.19.png" alt="gambar" width="580"/>
</p>

[Gambar 2-19: Mengirim ether ke alamat kontrak Faucet menggunakan MetaMask]

Dalam satu menit, jika Anda memuat ulang penjelajah blok Etherscan, ia akan menunjukkan transaksi lain ke alamat kontrak dan saldo yang diperbarui menjadi 1 ether.

Ingat fungsi `public payable` default tanpa nama dalam kode `Faucet.sol` kita? Kodenya terlihat seperti ini:

```solidity
function () public payable {}
```

Ketika Anda mengirim transaksi ke alamat kontrak, tanpa data yang menentukan fungsi mana yang harus dipanggil, transaksi itu memanggil fungsi default ini. Karena kita mendeklarasikannya sebagai `payable`, fungsi ini menerima dan menyetorkan 1 ether ke dalam saldo akun kontrak. Transaksi Anda menyebabkan kontrak berjalan di EVM, memperbarui saldonya. Anda telah mendanai *faucet* Anda\!

### **Menarik Dana dari Kontrak Kita**

Selanjutnya, mari kita tarik sejumlah dana dari *faucet*. Untuk menarik dana, kita harus membuat transaksi yang memanggil fungsi `withdraw` dan meneruskan argumen `withdraw_amount` ke dalamnya. Agar tetap sederhana untuk saat ini, Remix akan membuat transaksi itu untuk kita dan MetaMask akan menampilkannya untuk persetujuan kita.

Kembali ke tab Remix dan lihat kontrak di tab **Run**. Anda akan melihat sebuah kotak merah berlabel `withdraw` dengan kolom masukan berlabel `uint256 withdraw_amount` (lihat Gambar 2-20).

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.20.png" alt="gambar" width="580"/>
</p>

[Gambar 2-20: Antarmuka fungsi `withdraw` di Remix]

Ini adalah antarmuka Remix ke kontrak. Ini memungkinkan kita untuk membuat transaksi yang memanggil fungsi yang didefinisikan dalam kontrak. Kita akan memasukkan `withdraw_amount` dan mengklik tombol `withdraw` untuk menghasilkan transaksi.

Pertama, mari kita tentukan `withdraw_amount`. Kita ingin mencoba menarik 0,1 ether, yang merupakan jumlah maksimum yang diizinkan oleh kontrak kita. Ingat bahwa semua nilai mata uang di Ethereum secara internal didenominasikan dalam **wei**, dan fungsi `withdraw` kita juga mengharapkan `withdraw_amount` didenominasikan dalam wei. Jumlah yang kita inginkan adalah 0,1 ether, yaitu `100.000.000.000.000.000` wei (angka 1 diikuti oleh 17 angka nol).

> Karena keterbatasan pada JavaScript, angka sebesar `$10^{17}$` tidak dapat diproses oleh Remix. Sebagai gantinya, kita harus membungkusnya dengan tanda kutip ganda, agar Remix dapat menerimanya sebagai *string* dan memanipulasinya sebagai `BigNumber`. Jika kita tidak membungkusnya dengan tanda kutip, Remix IDE akan gagal memprosesnya dan menampilkan "Error encoding arguments: Error: Assertion failed."

Ketik `“100000000000000000”` (dengan tanda kutip) ke dalam kotak `withdraw_amount` dan klik tombol **withdraw** (lihat Gambar 2-21).

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.21.png" alt="gambar" width="580"/>
</p>

[Gambar 2-21: Memasukkan jumlah penarikan di Remix]

MetaMask akan memunculkan jendela transaksi untuk Anda setujui. Klik **Submit** untuk mengirim panggilan penarikan Anda ke kontrak (lihat Gambar 2-22).

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.22.png" alt="gambar" width="580"/>
</p>

[Gambar 2-22: Menyetujui transaksi pemanggilan fungsi di MetaMask]

Tunggu sebentar lalu muat ulang penjelajah blok Etherscan untuk melihat transaksi tersebut tercermin dalam riwayat alamat kontrak Faucet (lihat Gambar 2-23).

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.23.png" alt="gambar" width="580"/>
</p>

[Gambar 2-23: Riwayat alamat kontrak Faucet setelah transaksi penarikan]

Kita sekarang melihat transaksi baru dengan alamat kontrak sebagai tujuan dan nilai 0 ether. Saldo kontrak telah berubah dan sekarang menjadi 0,9 ether karena telah mengirimkan 0,1 ether kepada kita seperti yang diminta. Tetapi kita tidak melihat transaksi "KELUAR" (*OUT*) dalam riwayat alamat kontrak.

Di manakah penarikan keluar itu? Sebuah tab baru telah muncul di halaman riwayat alamat kontrak, bernama **Internal Transactions**. Karena transfer 0,1 ether berasal dari kode kontrak, itu adalah sebuah **transaksi internal** (juga disebut *message* atau pesan). Klik tab tersebut untuk melihatnya (lihat Gambar 2-24).

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-2.24.png" alt="gambar" width="580"/>
</p>

"Transaksi internal" ini dikirim oleh kontrak pada baris kode ini (dari fungsi `withdraw` di `Faucet.sol`):

```solidity
msg.sender.transfer(withdraw_amount);
```

Sebagai rekap: Anda mengirim sebuah transaksi dari dompet MetaMask Anda yang berisi instruksi data untuk memanggil fungsi `withdraw` dengan argumen `withdraw_amount` sebesar 0,1 ether. Transaksi itu menyebabkan kontrak berjalan di dalam EVM. Saat EVM menjalankan fungsi `withdraw` dari kontrak `Faucet`, pertama ia memanggil fungsi `require` dan memvalidasi bahwa jumlah yang diminta kurang dari atau sama dengan penarikan maksimum yang diizinkan sebesar 0,1 ether. Kemudian ia memanggil fungsi `transfer` untuk mengirimkan ether kepada Anda. Menjalankan fungsi `transfer` menghasilkan sebuah transaksi internal yang menyetorkan 0,1 ether ke alamat dompet Anda, dari saldo kontrak. Itulah yang ditampilkan di tab **Internal Transactions** di Etherscan.

### **Kesimpulan**

Dalam bab ini, Anda telah menyiapkan dompet menggunakan MetaMask dan mendanainya menggunakan *faucet* di jaringan uji Ropsten. Anda menerima ether ke alamat Ethereum dompet Anda, kemudian Anda mengirim ether ke alamat Ethereum *faucet*.

Selanjutnya, Anda menulis kontrak *faucet* di Solidity. Anda menggunakan Remix IDE untuk mengkompilasi kontrak menjadi *bytecode* EVM, kemudian menggunakan Remix untuk membentuk transaksi dan membuat kontrak `Faucet` di *blockchain* Ropsten. Setelah dibuat, kontrak `Faucet` memiliki alamat Ethereum, dan Anda mengiriminya sejumlah ether. Terakhir, Anda membuat transaksi untuk memanggil fungsi `withdraw` dan berhasil meminta 0,1 ether. Kontrak memeriksa permintaan tersebut dan mengirimi Anda 0,1 ether dengan sebuah transaksi internal.

Mungkin tidak tampak seperti hal besar, tetapi Anda baru saja berhasil berinteraksi dengan perangkat lunak yang mengendalikan uang di atas sebuah komputer dunia yang terdesentralisasi.

Kita akan melakukan lebih banyak lagi pemrograman *smart contract* di Bab 7 dan belajar tentang praktik terbaik serta pertimbangan keamanan di Bab 9.

---

# BAB 3
## Klien Ethereum

Sebuah **klien Ethereum** adalah aplikasi perangkat lunak yang mengimplementasikan spesifikasi Ethereum dan berkomunikasi melalui jaringan *peer-to-peer* dengan klien Ethereum lainnya. Klien Ethereum yang berbeda dapat saling beroperasi jika mereka mematuhi spesifikasi referensi dan protokol komunikasi yang terstandarisasi. Meskipun klien-klien yang berbeda ini diimplementasikan oleh tim yang berbeda dan dalam bahasa pemrograman yang berbeda, mereka semua "berbicara" dengan protokol yang sama dan mengikuti aturan yang sama. Dengan demikian, mereka semua dapat digunakan untuk mengoperasikan dan berinteraksi dengan jaringan Ethereum yang sama.

Ethereum adalah proyek **sumber terbuka** (*open source*), dan kode sumber untuk semua klien utama tersedia di bawah lisensi sumber terbuka (misalnya, LGPL v3.0), gratis untuk diunduh dan digunakan untuk tujuan apa pun. Namun, sumber terbuka lebih dari sekadar gratis untuk digunakan. Ini juga berarti bahwa Ethereum dikembangkan oleh komunitas sukarelawan yang terbuka dan dapat dimodifikasi oleh siapa saja. Lebih banyak mata yang melihat berarti kode yang lebih dapat dipercaya.

Ethereum didefinisikan oleh spesifikasi formal yang disebut **“Yellow Paper”** (lihat “Bacaan Lebih Lanjut” di halaman 7).
Ini berbeda dengan, misalnya, Bitcoin, yang tidak didefinisikan secara formal. Jika "spesifikasi" Bitcoin adalah implementasi referensi Bitcoin Core, spesifikasi Ethereum didokumentasikan dalam sebuah makalah yang menggabungkan spesifikasi bahasa Inggris dan matematis (formal). Spesifikasi formal ini, selain berbagai *Ethereum Improvement Proposals*, mendefinisikan perilaku standar dari sebuah klien Ethereum. Yellow Paper diperbarui secara berkala seiring dengan perubahan besar yang dibuat pada Ethereum.

Sebagai hasil dari spesifikasi formal Ethereum yang jelas, ada sejumlah implementasi perangkat lunak klien Ethereum yang dikembangkan secara independen namun dapat saling beroperasi. Ethereum memiliki keragaman implementasi yang berjalan di jaringan lebih banyak daripada *blockchain* lainnya, yang secara umum dianggap sebagai hal yang baik. Memang, hal ini telah terbukti menjadi cara yang sangat baik untuk bertahan dari serangan di jaringan, karena eksploitasi terhadap strategi implementasi klien tertentu hanya akan merepotkan para pengembang saat mereka menambal eksploitasi tersebut, sementara klien lain menjaga jaringan tetap berjalan hampir tanpa terpengaruh.

### Jaringan Ethereum

Terdapat berbagai jaringan berbasis Ethereum yang sebagian besar sesuai dengan spesifikasi formal yang didefinisikan dalam Ethereum Yellow Paper, tetapi mungkin atau mungkin tidak dapat saling beroperasi satu sama lain.

Di antara jaringan-jaringan berbasis Ethereum ini adalah Ethereum, Ethereum Classic, Ella, Expanse, Ubiq, Musicoin, dan banyak lainnya. Meskipun sebagian besar kompatibel pada tingkat protokol, jaringan-jaringan ini sering kali memiliki fitur atau atribut yang mengharuskan pengelola perangkat lunak klien Ethereum untuk membuat perubahan kecil agar dapat mendukung setiap jaringan. Karena itu, tidak setiap versi perangkat lunak klien Ethereum dapat menjalankan setiap *blockchain* berbasis Ethereum.

Saat ini, ada enam implementasi utama dari protokol Ethereum, yang ditulis dalam enam bahasa yang berbeda:

  * **Parity**, ditulis dalam Rust
  * **Geth**, ditulis dalam Go
  * **cpp-ethereum**, ditulis dalam C++
  * **pyethereum**, ditulis dalam Python
  * **Mantis**, ditulis dalam Scala
  * **Harmony**, ditulis dalam Java

Di bagian ini, kita akan melihat dua klien yang paling umum, Parity dan Geth. Kami akan menunjukkan cara menyiapkan *node* menggunakan setiap klien, dan menjelajahi beberapa opsi baris perintah (*command-line*) dan antarmuka pemrograman aplikasi (API) mereka.

### Haruskah Saya Menjalankan Full Node?

Kesehatan, ketahanan, dan resistensi terhadap sensor dari *blockchain* bergantung pada banyaknya ***full node*** yang dioperasikan secara independen dan tersebar secara geografis. Setiap *full node* dapat membantu *node* baru lainnya mendapatkan data blok untuk memulai operasi mereka, serta menawarkan operator verifikasi yang otoritatif dan independen dari semua transaksi dan kontrak.

Namun, menjalankan *full node* akan menimbulkan biaya dalam sumber daya perangkat keras dan *bandwidth*. *Full node* harus mengunduh 80–100 GB data (per September 2018, tergantung pada konfigurasi klien) dan menyimpannya di *hard drive* lokal. Beban data ini meningkat cukup pesat setiap hari seiring dengan penambahan transaksi dan blok baru. Kita akan membahas topik ini lebih detail di “Kebutuhan Perangkat Keras untuk Full Node” di halaman 45.

*Full node* yang berjalan di jaringan utama (*mainnet*) tidak diperlukan untuk pengembangan Ethereum. Anda dapat melakukan hampir semua yang perlu Anda lakukan dengan *node testnet* (yang menghubungkan Anda ke salah satu *blockchain* uji publik yang lebih kecil), dengan *blockchain* pribadi lokal seperti Ganache, atau dengan klien Ethereum berbasis *cloud* yang ditawarkan oleh penyedia layanan seperti Infura.

Anda juga memiliki opsi untuk menjalankan **klien jarak jauh** (*remote client*), yang tidak menyimpan salinan lokal dari *blockchain* atau memvalidasi blok dan transaksi. Klien ini menawarkan fungsionalitas dompet (*wallet*) dan dapat membuat serta menyiarkan transaksi. Klien jarak jauh dapat digunakan untuk terhubung ke jaringan yang ada, seperti *full node* Anda sendiri, *blockchain* publik, *testnet* publik atau berizin (*proof-of-authority*), atau *blockchain* pribadi lokal. Dalam praktiknya, Anda kemungkinan akan menggunakan klien jarak jauh seperti MetaMask, Emerald Wallet, MyEtherWallet, atau MyCrypto sebagai cara yang mudah untuk beralih di antara semua opsi *node* yang berbeda.

Istilah "klien jarak jauh" dan "dompet" digunakan secara bergantian, meskipun ada beberapa perbedaan. Biasanya, klien jarak jauh menawarkan API (seperti web3.js API) selain fungsionalitas transaksi dari sebuah dompet.

Jangan bingung antara konsep dompet jarak jauh di Ethereum dengan ***light client*** (yang analog dengan klien *Simplified Payment Verification* di Bitcoin). *Light client* memvalidasi *header* blok dan menggunakan bukti Merkle (*Merkle proofs*) untuk memvalidasi penyertaan transaksi di dalam *blockchain* dan menentukan dampaknya, memberikan mereka tingkat keamanan yang serupa dengan *full node*. Sebaliknya, klien jarak jauh Ethereum не memvalidasi *header* blok atau transaksi. Mereka sepenuhnya mempercayai *full client* untuk memberi mereka akses ke *blockchain*, dan karenanya kehilangan jaminan keamanan dan anonimitas yang signifikan. Anda dapat mengurangi masalah ini dengan menggunakan *full client* yang Anda jalankan sendiri.

### Kelebihan dan Kekurangan Full Node

Memilih untuk menjalankan *full node* membantu operasi jaringan yang Anda hubungkan, tetapi juga menimbulkan beberapa biaya ringan hingga sedang bagi Anda. Mari kita lihat beberapa kelebihan dan kekurangannya.

**Kelebihan:**

  * Mendukung ketahanan dan resistensi sensor dari jaringan berbasis Ethereum.
  * Memvalidasi semua transaksi secara otoritatif.
  * Dapat berinteraksi dengan kontrak apa pun di *blockchain* publik tanpa perantara.
  * Dapat secara langsung menerapkan kontrak ke dalam *blockchain* publik tanpa perantara.
  * Dapat menanyakan (hanya-baca) status *blockchain* (akun, kontrak, dll.) secara *offline*.
  * Dapat menanyakan *blockchain* tanpa memberi tahu pihak ketiga informasi yang Anda baca.

**Kekurangan:**

  * Membutuhkan sumber daya perangkat keras dan *bandwidth* yang signifikan dan terus bertambah.
  * Mungkin memerlukan beberapa hari untuk sinkronisasi penuh saat pertama kali dimulai.
  * Harus dipelihara, ditingkatkan, dan dijaga agar tetap *online* untuk tetap tersinkronisasi.

### Kelebihan dan Kekurangan Testnet Publik

Baik Anda memilih untuk menjalankan *full node* atau tidak, Anda mungkin ingin menjalankan *node testnet* publik. Mari kita lihat beberapa kelebihan dan kekurangan menggunakan *testnet* publik.

**Kelebihan:**

  * *Node testnet* perlu menyinkronkan dan menyimpan data yang jauh lebih sedikit—sekitar 10 GB tergantung pada jaringan (per April 2018).
  * *Node testnet* dapat sinkronisasi penuh dalam beberapa jam.
  * Menyebarkan kontrak atau melakukan transaksi memerlukan *test ether*, yang tidak memiliki nilai dan dapat diperoleh secara gratis dari beberapa “*faucet*” (keran).
  * *Testnet* adalah *blockchain* publik dengan banyak pengguna dan kontrak lain, yang berjalan secara “*live*”.

**Kekurangan:**

  * Anda не dapat menggunakan uang “nyata” di *testnet*; ia berjalan dengan *test ether*. Akibatnya, Anda не dapat menguji keamanan terhadap musuh nyata, karena tidak ada yang dipertaruhkan.
  * Ada beberapa aspek dari *blockchain* publik yang tidak dapat Anda uji secara realistis di *testnet*. Misalnya, biaya transaksi, meskipun diperlukan untuk mengirim transaksi, tidak menjadi pertimbangan di *testnet*, karena gas gratis. Lebih lanjut, *testnet* tidak mengalami kemacetan jaringan seperti yang terkadang terjadi pada *mainnet* publik.

### Kelebihan dan Kekurangan Simulasi Blockchain Lokal

Untuk banyak tujuan pengujian, opsi terbaik adalah meluncurkan *blockchain* pribadi satu instans. **Ganache** (sebelumnya bernama testrpc) adalah salah satu simulasi *blockchain* lokal paling populer yang dapat Anda gunakan untuk berinteraksi, tanpa peserta lain. Ini memiliki banyak kelebihan dan kekurangan yang sama dengan *testnet* publik, tetapi juga memiliki beberapa perbedaan.

**Kelebihan:**

  * Tidak ada sinkronisasi dan hampir tidak ada data di disk; Anda menambang blok pertama sendiri.
  * Tidak perlu mendapatkan *test ether*; Anda "memberi hadiah" pada diri sendiri berupa imbalan penambangan yang dapat Anda gunakan untuk pengujian.
  * Tidak ada pengguna lain, hanya Anda.
  * Tidak ada kontrak lain, hanya yang Anda sebarkan setelah Anda meluncurkannya.

**Kekurangan:**

  * Tidak adanya pengguna lain berarti perilakunya tidak sama dengan *blockchain* publik. Tidak ada persaingan untuk ruang transaksi atau urutan transaksi.
  * Tidak ada penambang selain Anda berarti penambangan lebih dapat diprediksi; oleh karena itu, Anda tidak dapat menguji beberapa skenario yang terjadi di *blockchain* publik.
  * Tidak adanya kontrak lain berarti Anda harus menyebarkan semua yang ingin Anda uji, termasuk dependensi dan pustaka kontrak.
  * Anda tidak dapat menciptakan kembali beberapa kontrak publik dan alamatnya untuk menguji beberapa skenario (misalnya, kontrak DAO).

### Menjalankan Klien Ethereum

Jika Anda memiliki waktu dan sumber daya, Anda harus mencoba menjalankan *full node*, meskipun hanya untuk mempelajari lebih lanjut tentang prosesnya. Di bagian ini kami membahas cara mengunduh, mengompilasi, dan menjalankan klien Ethereum Parity dan Geth. Ini memerlukan beberapa keakraban dengan penggunaan antarmuka baris perintah (*command-line interface*) pada sistem operasi Anda. Layak untuk menginstal klien-klien ini, baik Anda memilih untuk menjalankannya sebagai *full node*, sebagai *node testnet*, atau sebagai klien untuk *blockchain* pribadi lokal.

#### Kebutuhan Perangkat Keras untuk Full Node

Sebelum kita mulai, Anda harus memastikan Anda memiliki komputer dengan sumber daya yang cukup untuk menjalankan *full node* Ethereum. Anda akan memerlukan setidaknya **80 GB** ruang disk untuk menyimpan salinan penuh dari *blockchain* Ethereum. Jika Anda juga ingin menjalankan *full node* di *testnet* Ethereum, Anda akan memerlukan tambahan setidaknya **15 GB**. Mengunduh 80 GB data *blockchain* bisa memakan waktu lama, jadi disarankan agar Anda bekerja dengan koneksi internet yang cepat.

Sinkronisasi *blockchain* Ethereum sangat intensif dalam hal *input/output* (I/O). Sebaiknya Anda memiliki ***solid-state drive* (SSD)**. Jika Anda memiliki *hard disk drive* (HDD) mekanis, Anda akan memerlukan setidaknya **8 GB RAM** untuk digunakan sebagai *cache*. Jika tidak, Anda mungkin akan menemukan bahwa sistem Anda terlalu lambat untuk mengimbangi dan melakukan sinkronisasi penuh.

**Kebutuhan minimum:**

  * CPU dengan 2+ *core*
  * Ruang penyimpanan kosong setidaknya 80 GB
  * RAM minimal 4 GB dengan SSD, 8 GB+ jika Anda memiliki HDD
  * Layanan internet dengan kecepatan unduh 8 MBit/detik

Ini adalah persyaratan minimum untuk menyinkronkan salinan penuh (namun telah dipangkas/*pruned*) dari *blockchain* berbasis Ethereum.

Pada saat penulisan ini, basis kode Parity lebih ringan dalam penggunaan sumber daya, jadi jika Anda berjalan dengan perangkat keras terbatas, Anda kemungkinan akan melihat hasil yang lebih baik menggunakan Parity.

Jika Anda ingin melakukan sinkronisasi dalam waktu yang wajar dan menyimpan semua alat pengembangan, pustaka, klien, dan *blockchain* yang kita bahas dalam buku ini, Anda akan menginginkan komputer yang lebih mumpuni.

**Spesifikasi yang direkomendasikan:**

  * CPU cepat dengan 4+ *core*
  * RAM 16 GB+
  * SSD cepat dengan setidaknya 500 GB ruang kosong
  * Layanan internet dengan kecepatan unduh 25+ MBit/detik

Sulit untuk memprediksi seberapa cepat ukuran *blockchain* akan bertambah dan kapan ruang disk lebih banyak akan diperlukan, jadi disarankan untuk memeriksa ukuran terbaru *blockchain* sebelum Anda mulai melakukan sinkronisasi.

> Kebutuhan ukuran disk yang tercantum di sini mengasumsikan Anda akan menjalankan *node* dengan pengaturan default, di mana *blockchain* "dipangkas" (*pruned*) dari data *state* lama. Jika Anda menjalankan *node* "arsip" (*archival*) penuh, di mana semua *state* disimpan di disk, kemungkinan akan memerlukan lebih dari 1 TB ruang disk.

Tautan-tautan ini memberikan perkiraan terkini tentang ukuran *blockchain*:

  * [Ethereum](https://bitinfocharts.com/ethereum/)
  * [Ethereum Classic](https://bitinfocharts.com/ethereum%20classic/)

#### Kebutuhan Perangkat Lunak untuk Membangun dan Menjalankan Klien (Node)

Bagian ini membahas perangkat lunak klien Parity dan Geth. Ini juga mengasumsikan Anda menggunakan lingkungan baris perintah mirip Unix. Contoh-contoh menunjukkan perintah dan output seperti yang muncul pada sistem operasi Ubuntu GNU/Linux yang menjalankan *shell* bash (lingkungan eksekusi baris perintah).

Biasanya setiap *blockchain* akan memiliki versi Geth-nya sendiri, sementara Parity memberikan dukungan untuk beberapa *blockchain* berbasis Ethereum (Ethereum, Ethereum Classic, Ellaism, Expanse, Musicoin) dengan unduhan klien yang sama.

> Dalam banyak contoh di bab ini, kita akan menggunakan antarmuka baris perintah sistem operasi (juga dikenal sebagai "*shell*"), yang diakses melalui aplikasi "terminal". *Shell* akan menampilkan sebuah *prompt*; Anda mengetikkan perintah, dan *shell* merespons dengan beberapa teks dan *prompt* baru untuk perintah Anda berikutnya. *Prompt* mungkin terlihat berbeda di sistem Anda, tetapi dalam contoh berikut, itu ditandai dengan simbol **$**. Dalam contoh, ketika Anda melihat teks setelah simbol **$**, jangan ketik simbol **$** tetapi ketik perintah yang langsung mengikutinya (ditampilkan dalam **teks tebal**), lalu tekan Enter untuk menjalankan perintah tersebut. Dalam contoh, baris-baris di bawah setiap perintah adalah respons sistem operasi terhadap perintah itu. Ketika Anda melihat awalan **$** berikutnya, Anda akan tahu itu adalah perintah baru dan Anda harus mengulangi prosesnya.

Sebelum kita mulai, Anda mungkin perlu menginstal beberapa perangkat lunak. Jika Anda belum pernah melakukan pengembangan perangkat lunak di komputer yang sedang Anda gunakan, Anda mungkin perlu menginstal beberapa alat dasar. Untuk contoh-contoh berikut, Anda perlu menginstal **git**, sistem manajemen kode sumber; **golang**, bahasa pemrograman Go dan pustaka standarnya; dan **Rust**, sebuah bahasa pemrograman sistem.

Git dapat diinstal dengan mengikuti instruksi di [https://git-scm.com](https://git-scm.com).
Go dapat diinstal dengan mengikuti instruksi di [https://golang.org](https://golang.org).

> Persyaratan Geth bervariasi, tetapi jika Anda menggunakan Go versi 1.10 atau lebih tinggi, Anda seharusnya dapat mengompilasi versi Geth apa pun yang Anda inginkan. Tentu saja, Anda harus selalu merujuk pada dokumentasi untuk jenis Geth pilihan Anda.

> Versi golang yang terinstal di sistem operasi Anda atau tersedia dari manajer paket sistem Anda mungkin jauh lebih tua dari 1.10. Jika demikian, hapus dan instal versi terbaru dari [https://golang.org/](https://golang.org/).

Rust dapat diinstal dengan mengikuti instruksi di [https://www.rustup.rs/](https://www.rustup.rs/).

> Parity memerlukan Rust versi 1.27 atau lebih tinggi.

Parity juga memerlukan beberapa pustaka perangkat lunak, seperti OpenSSL dan libudev. Untuk menginstalnya pada sistem yang kompatibel dengan Ubuntu atau Debian GNU/Linux, gunakan perintah berikut:

`$ sudo apt-get install openssl libssl-dev libudev-dev cmake`

Untuk sistem operasi lain, gunakan manajer paket OS Anda atau ikuti instruksi Wiki untuk menginstal pustaka yang diperlukan.

Sekarang setelah Anda menginstal git, golang, Rust, dan pustaka yang diperlukan, mari kita mulai bekerja\!

### Parity

Parity adalah implementasi dari klien Ethereum *full-node* dan peramban DApp. Ini ditulis "dari awal" dalam Rust, sebuah bahasa pemrograman sistem, dengan tujuan membangun klien Ethereum yang modular, aman, dan dapat diskalakan. Parity dikembangkan oleh Parity Tech, sebuah perusahaan Inggris, dan dirilis di bawah lisensi perangkat lunak bebas GPLv3.

> Pengungkapan: Salah satu penulis buku ini, Dr. Gavin Wood, adalah pendiri Parity Tech dan menulis sebagian besar klien Parity. Parity mewakili sekitar 25% dari basis klien Ethereum yang terpasang.

Untuk menginstal Parity, Anda dapat menggunakan manajer paket Rust `cargo` atau mengunduh kode sumber dari GitHub. Manajer paket juga mengunduh kode sumber, jadi tidak banyak perbedaan antara kedua opsi tersebut. Di bagian selanjutnya, kami akan menunjukkan cara mengunduh dan mengompilasi Parity sendiri.

#### Menginstal Parity

Wiki Parity menawarkan instruksi untuk membangun Parity di berbagai lingkungan dan *container*. Kami akan menunjukkan cara membangun Parity dari sumber. Ini mengasumsikan Anda telah menginstal Rust menggunakan `rustup` (lihat “Kebutuhan Perangkat Lunak untuk Membangun dan Menjalankan Klien (Node)” di halaman 47).

Pertama, dapatkan kode sumber dari GitHub:

`$ git clone https://github.com/paritytech/parity`

Kemudian pindah ke direktori `parity` dan gunakan `cargo` untuk membangun file *executable*:

`$ cd parity`
`$ cargo install`

Jika semuanya berjalan lancar, Anda akan melihat sesuatu seperti:

```
$ cargo install
Updating git repository `https://github.com/paritytech/js-precompiled.git`
Downloading log v0.3.7
Downloading isatty v0.1.1
Downloading regex v0.2.1
[...]
Compiling parity-ipfs-api v1.7.0
Compiling parity-rpc v1.7.0
Compiling parity-rpc-client v1.4.0
Compiling rpc-cli v1.4.0 (file:///home/aantonop/Dev/parity/rpc_cli)
Finished dev [unoptimized + debuginfo] target(s) in 479.12 secs
$
```

Coba jalankan `parity` untuk melihat apakah sudah terinstal, dengan memanggil opsi `--version`:

```
$ parity --version
Parity
version Parity/v1.7.0-unstable-02edc95-20170623/x86_64-linux-gnu/rustc1.18.0
Copyright 2015, 2016, 2017 Parity Technologies (UK) Ltd
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>.
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
By Wood/Paronyan/Kotewicz/Drwięga/Volf
Habermeier/Czaban/Greeff/Gotchac/Redmann
$
```

Bagus\! Sekarang Parity sudah terinstal, Anda dapat menyinkronkan *blockchain* dan memulai dengan beberapa opsi baris perintah dasar.

### Go-Ethereum (Geth)

Geth adalah implementasi bahasa Go yang dikembangkan secara aktif oleh Ethereum Foundation, sehingga dianggap sebagai implementasi "resmi" dari klien Ethereum. Biasanya, setiap *blockchain* berbasis Ethereum akan memiliki implementasi Geth-nya sendiri. Jika Anda menjalankan Geth, maka Anda harus memastikan Anda mengambil versi yang benar untuk *blockchain* Anda menggunakan salah satu tautan repositori berikut:

  * [Ethereum](https://github.com/ethereum/go-ethereum) (or go [https://geth.ethereum.org/](https://geth.ethereum.org/)))
  * [Ethereum Classic](https://github.com/ethereumproject/go-ethereum)
  * [Ellaism](https://github.com/ellaism/go-ellaism)
  * [Expanse](https://github.com/expanse-org/go-expanse)
  * [Musicoin](https://github.com/Musicoin/go-musicoin)
  * [Ubiq](https://github.com/ubiq/go-ubiq)

> Anda juga dapat melewati instruksi ini dan menginstal biner yang sudah dikompilasi (*precompiled binary*) untuk platform pilihan Anda. Rilisan yang sudah dikompilasi jauh lebih mudah untuk diinstal dan dapat ditemukan di bagian "releases" dari salah satu repositori yang tercantum di sini. Namun, Anda mungkin belajar lebih banyak dengan mengunduh dan mengompilasi perangkat lunak sendiri.

#### Melakukan Kloning Repositori

Langkah pertama adalah melakukan kloning repositori Git, untuk mendapatkan salinan kode sumber.

Untuk membuat klon lokal dari repositori pilihan Anda, gunakan perintah `git` sebagai berikut, di direktori *home* Anda atau di bawah direktori mana pun yang Anda gunakan untuk pengembangan:

`$ git clone <Tautan Repositori>`

Anda akan melihat laporan kemajuan saat repositori disalin ke sistem lokal Anda:

```
Cloning into 'go-ethereum'...
remote: Counting objects: 62587, done.
remote: Compressing objects: 100% (26/26), done.
remote: Total 62587 (delta 10), reused 13 (delta 4), pack-reused 62557
Receiving objects: 100% (62587/62587), 84.51 MiB | 1.40 MiB/s, done.
Resolving deltas: 100% (41554/41554), done.
Checking connectivity... done.
```

Bagus\! Sekarang Anda memiliki salinan lokal Geth, Anda dapat mengompilasi *executable* untuk platform Anda.

#### Membangun Geth dari Kode Sumber

Untuk membangun Geth, pindah ke direktori tempat kode sumber diunduh dan gunakan perintah `make`:

`$ cd go-ethereum`
`$ make geth`

Jika semuanya berjalan lancar, Anda akan melihat kompiler Go membangun setiap komponen hingga menghasilkan *executable* `geth`:

```
build/env.sh go run build/ci.go install ./cmd/geth
>>> /usr/local/go/bin/go install -ldflags -X main.gitCommit=58a1e13e6dd7f52a1d...
github.com/ethereum/go-ethereum/common/hexutil
github.com/ethereum/go-ethereum/common/math
github.com/ethereum/go-ethereum/crypto/sha3
github.com/ethereum/go-ethereum/rlp
github.com/ethereum/go-ethereum/crypto/secp256k1
github.com/ethereum/go-ethereum/common
[...]
github.com/ethereum/go-ethereum/cmd/utils
github.com/ethereum/go-ethereum/cmd/geth
Done building.
Run "build/bin/geth" to launch geth.
$
```

Mari kita pastikan `geth` berfungsi tanpa benar-benar menjalankannya:

```
$ ./build/bin/geth version
Geth
Version: 1.6.6-unstable
Git Commit: 58a1e13e6dd7f52a1d5e67bee47d23fd6cfdee5c
Architecture: amd64
Protocol Versions: [63 62]
Network Id: 1
Go Version: go1.8.3
Operating System: linux
[...]
```

Perintah `geth version` Anda mungkin menampilkan informasi yang sedikit berbeda, tetapi Anda akan melihat laporan versi yang mirip dengan yang terlihat di sini.

Jangan jalankan `geth` dulu, karena itu akan mulai menyinkronkan *blockchain* dengan “cara lambat” dan itu akan memakan waktu terlalu lama (berminggu-minggu). Bagian selanjutnya menjelaskan tantangan dengan sinkronisasi awal *blockchain* Ethereum.

### Sinkronisasi Pertama Blockchain Berbasis Ethereum

Biasanya, saat menyinkronkan *blockchain* Ethereum, klien Anda akan mengunduh dan memvalidasi setiap blok dan setiap transaksi sejak awal—yaitu, dari blok genesis.

Meskipun dimungkinkan untuk menyinkronkan *blockchain* sepenuhnya dengan cara ini, sinkronisasi akan memakan waktu sangat lama dan memiliki persyaratan sumber daya yang tinggi (akan membutuhkan lebih banyak RAM, dan akan memakan waktu sangat lama jika Anda tidak memiliki penyimpanan cepat).

Banyak *blockchain* berbasis Ethereum menjadi korban serangan *denial-of-service* (DoS) pada akhir tahun 2016. *Blockchain* yang terpengaruh akan cenderung sinkronisasi dengan lambat saat melakukan sinkronisasi penuh.

Misalnya, di Ethereum, klien baru akan membuat kemajuan pesat hingga mencapai blok 2.283.397. Blok ini ditambang pada 18 September 2016, dan menandai awal dari serangan DoS. Dari blok ini hingga blok 2.700.031 (26 November 2016), validasi transaksi menjadi sangat lambat, intensif memori, dan intensif I/O. Ini menghasilkan waktu validasi yang melebihi 1 menit per blok. Ethereum mengimplementasikan serangkaian peningkatan, menggunakan *hard fork*, untuk mengatasi kerentanan mendasar yang dieksploitasi dalam serangan DoS. Peningkatan ini juga membersihkan blockchain dengan menghapus sekitar 20 juta akun kosong yang dibuat oleh transaksi spam.

Jika Anda melakukan sinkronisasi dengan validasi penuh, klien Anda akan melambat dan mungkin memerlukan beberapa hari, atau bahkan lebih lama, untuk memvalidasi blok-blok yang terkena dampak serangan DoS. Untungnya, sebagian besar klien Ethereum menyertakan opsi untuk melakukan sinkronisasi "cepat" (*fast*) yang melewatkan validasi penuh transaksi hingga klien tersinkronisasi ke ujung *blockchain*, kemudian melanjutkan validasi penuh.

Untuk Geth, opsi untuk mengaktifkan sinkronisasi cepat biasanya disebut `--fast`. Anda mungkin perlu merujuk pada instruksi spesifik untuk rantai Ethereum pilihan Anda.

Parity melakukan sinkronisasi cepat secara default.

> Geth hanya dapat mengoperasikan sinkronisasi cepat saat memulai dengan database blok yang kosong. Jika Anda sudah mulai menyinkronkan tanpa mode cepat, Geth tidak dapat beralih. Lebih cepat menghapus direktori data *blockchain* dan memulai sinkronisasi cepat dari awal daripada melanjutkan sinkronisasi dengan validasi penuh. Berhati-hatilah agar tidak menghapus dompet apa pun saat menghapus data *blockchain*\!

#### Menjalankan Geth atau Parity

Sekarang setelah Anda memahami tantangan dari "sinkronisasi pertama," Anda siap untuk memulai klien Ethereum dan menyinkronkan *blockchain*. Baik untuk Geth maupun Parity, Anda dapat menggunakan opsi `--help` untuk melihat semua parameter konfigurasi. Selain menggunakan `--fast` untuk Geth, seperti yang dijelaskan di bagian sebelumnya, pengaturan default biasanya sudah masuk akal dan sesuai untuk sebagian besar penggunaan. Pilih cara mengonfigurasi parameter opsional apa pun sesuai kebutuhan Anda, lalu mulai Geth atau Parity untuk menyinkronkan rantai. Kemudian tunggulah…

> Sinkronisasi *blockchain* Ethereum akan memakan waktu mulai dari setengah hari pada sistem yang sangat cepat dengan banyak RAM, hingga beberapa hari pada sistem yang lebih lambat.

### Antarmuka JSON-RPC

Klien Ethereum menawarkan antarmuka pemrograman aplikasi (API) dan serangkaian perintah *Remote Procedure Call* (RPC), yang dikodekan sebagai *JavaScript Object Notation* (JSON). Anda akan melihat ini disebut sebagai **JSON-RPC API**. Pada dasarnya, JSON-RPC API adalah antarmuka yang memungkinkan kita menulis program yang menggunakan klien Ethereum sebagai gerbang ke jaringan dan *blockchain* Ethereum.

Biasanya, antarmuka RPC ditawarkan sebagai layanan HTTP pada port 8545. Untuk alasan keamanan, secara default dibatasi untuk hanya menerima koneksi dari `localhost` (alamat IP komputer Anda sendiri, yaitu 127.0.0.1).

Untuk mengakses JSON-RPC API, Anda dapat menggunakan pustaka khusus (ditulis dalam bahasa pemrograman pilihan Anda) yang menyediakan pemanggilan fungsi "stub" yang sesuai dengan setiap perintah RPC yang tersedia, atau Anda dapat secara manual membuat permintaan HTTP dan mengirim/menerima permintaan yang dikodekan dalam format JSON. Anda bahkan dapat menggunakan klien HTTP baris perintah generik, seperti `curl`, untuk memanggil antarmuka RPC. Mari kita coba. Pertama, pastikan Anda telah mengonfigurasi dan menjalankan Geth, lalu beralih ke jendela terminal baru (misalnya, dengan Ctrl-Shift-N atau Ctrl-Shift-T di jendela terminal yang ada) seperti yang ditunjukkan di sini:

```
$ curl -X POST -H "Content-Type: application/json" --data \
'{"jsonrpc":"2.0","method":"web3_clientVersion","params":[],"id":1}' \
http://localhost:8545
{"jsonrpc":"2.0","id":1,
"result":"Geth/v1.8.0-unstable-02aeb3d7/linux-amd64/go1.8.3"}
```

Dalam contoh ini, kita menggunakan `curl` untuk membuat koneksi HTTP ke alamat http://localhost:8545. Kita sudah menjalankan `geth`, yang menawarkan JSON-RPC API sebagai layanan HTTP pada port 8545. Kita menginstruksikan `curl` untuk menggunakan perintah HTTP `POST` dan untuk mengidentifikasi konten sebagai tipe `application/json`. Terakhir, kita memberikan permintaan yang dikodekan dalam format JSON sebagai komponen data dari permintaan HTTP kita. Sebagian besar baris perintah kita hanya untuk mengatur `curl` agar membuat koneksi HTTP dengan benar. Bagian yang menarik adalah perintah JSON-RPC sebenarnya yang kita keluarkan:

`{"jsonrpc":"2.0","method":"web3_clientVersion","params":[],"id":1}`

Permintaan JSON-RPC diformat sesuai dengan spesifikasi JSON-RPC 2.0. Setiap permintaan berisi empat elemen:

**`jsonrpc`**
Versi protokol JSON-RPC. Ini HARUS persis `"2.0"`.
**`method`**
Nama metode yang akan dipanggil.
**`params`**
Nilai terstruktur yang berisi nilai parameter yang akan digunakan selama pemanggilan metode. Anggota ini DAPAT dihilangkan.
**`id`**
Pengenal yang ditetapkan oleh klien yang HARUS berisi String, Angka, atau nilai NULL jika disertakan. Server HARUS membalas dengan nilai yang sama dalam objek respons jika disertakan. Anggota ini digunakan untuk menghubungkan konteks antara dua objek.

> Parameter `id` digunakan terutama saat Anda membuat beberapa permintaan dalam satu panggilan JSON-RPC, sebuah praktik yang disebut *batching*. *Batching* digunakan untuk menghindari *overhead* dari koneksi HTTP dan TCP baru untuk setiap permintaan. Dalam konteks Ethereum, misalnya, kita akan menggunakan *batching* jika kita ingin mengambil ribuan transaksi melalui satu koneksi HTTP. Saat melakukan *batching*, Anda menetapkan `id` yang berbeda untuk setiap permintaan dan kemudian mencocokkannya dengan `id` di setiap respons dari server JSON-RPC. Cara termudah untuk mengimplementasikan ini adalah dengan mempertahankan sebuah penghitung dan menaikkan nilainya untuk setiap permintaan.

Respons yang kita terima adalah:

`{"jsonrpc":"2.0","id":1, "result":"Geth/v1.8.0-unstable-02aeb3d7/linux-amd64/go1.8.3"}`

Ini memberitahu kita bahwa JSON-RPC API dilayani oleh klien Geth versi 1.8.0.

Mari kita coba sesuatu yang sedikit lebih menarik. Dalam contoh berikutnya, kita meminta API JSON-RPC untuk harga gas saat ini dalam wei:

```
$ curl -X POST -H "Content-Type: application/json" --data \
'{"jsonrpc":"2.0","method":"eth_gasPrice","params":[],"id":4213}' \
http://localhost:8545
{"jsonrpc":"2.0","id":4213,"result":"0x430e23400"}
```

Respons, `0x430e23400`, memberitahu kita bahwa harga gas saat ini adalah 18 gwei (gigawei atau miliar wei). Jika, seperti kami, Anda tidak berpikir dalam heksadesimal, Anda dapat mengubahnya menjadi desimal di baris perintah dengan sedikit trik `bash`:

`$ echo $((0x430e23400))`
`18000000000`

JSON-RPC API lengkap dapat diselidiki di wiki Ethereum.

#### Mode Kompatibilitas Geth pada Parity

Parity memiliki "mode kompatibilitas Geth" khusus, di mana ia menawarkan JSON-RPC API yang identik dengan yang ditawarkan oleh Geth. Untuk menjalankan Parity dalam mode ini, gunakan sakelar `--geth`:

`$ parity --geth`

### Klien Ethereum Jarak Jauh (Remote)

Klien jarak jauh menawarkan sebagian kecil dari fungsionalitas klien penuh. Mereka tidak menyimpan seluruh *blockchain* Ethereum, sehingga lebih cepat untuk disiapkan dan memerlukan penyimpanan data yang jauh lebih sedikit. Klien-klien ini biasanya menyediakan kemampuan untuk melakukan satu atau lebih dari hal berikut:

  * Mengelola kunci privat dan alamat Ethereum dalam sebuah dompet (*wallet*).
  * Membuat, menandatangani, dan menyiarkan transaksi.
  * Berinteraksi dengan *smart contract*, menggunakan *data payload*.
  * Menjelajahi dan berinteraksi dengan DApps.
  * Menawarkan tautan ke layanan eksternal seperti penjelajah blok (*block explorer*).
  * Mengonversi unit ether dan mengambil nilai tukar dari sumber eksternal.
  * Menyuntikkan (*inject*) instans `web3` ke dalam peramban web sebagai objek JavaScript.
  * Menggunakan instans `web3` yang disediakan/disuntikkan ke dalam peramban oleh klien lain.
  * Mengakses layanan RPC pada *node* Ethereum lokal atau jarak jauh.

Beberapa klien jarak jauh, misalnya dompet seluler (*smartphone*), hanya menawarkan fungsionalitas dompet dasar. Klien jarak jauh lainnya adalah peramban DApp yang lengkap. Klien jarak jauh umumnya menawarkan beberapa fungsi klien Ethereum *full-node* tanpa menyinkronkan salinan lokal dari *blockchain* Ethereum dengan terhubung ke *full node* yang dijalankan di tempat lain, misalnya, oleh Anda secara lokal di mesin Anda atau di server web, atau oleh pihak ketiga di server mereka.

Mari kita lihat beberapa klien jarak jauh paling populer dan fungsi yang mereka tawarkan.

#### Dompet Seluler (*Smartphone*)

Semua dompet seluler adalah klien jarak jauh, karena *smartphone* tidak memiliki sumber daya yang memadai untuk menjalankan klien Ethereum penuh. *Light client* sedang dalam pengembangan dan belum digunakan secara umum untuk Ethereum. Dalam kasus Parity, *light client* ditandai "eksperimental" dan dapat digunakan dengan menjalankan `parity` dengan opsi `--light`.

Dompet seluler populer termasuk yang berikut (kami mencantumkannya hanya sebagai contoh; ini bukan merupakan dukungan atau indikasi keamanan atau fungsionalitas dompet-dompet ini):

**Jaxx**
Dompet seluler multi-mata uang berdasarkan *mnemonic seed* BIP-39, dengan dukungan untuk Bitcoin, Litecoin, Ethereum, Ethereum Classic, ZCash, berbagai token ERC20, dan banyak mata uang lainnya. Jaxx tersedia di Android dan iOS, sebagai dompet *plug-in* peramban, dan sebagai dompet desktop untuk berbagai sistem operasi.

**Status**
Dompet seluler dan peramban DApp, dengan dukungan untuk berbagai token dan DApps populer. Tersedia untuk iOS dan Android.

**Trust Wallet**
Dompet seluler Ethereum dan Ethereum Classic yang mendukung token ERC20 dan ERC223. Trust Wallet tersedia untuk iOS dan Android.

**Cipher Browser**
Peramban DApp dan dompet seluler berkemampuan Ethereum yang berfitur lengkap yang memungkinkan integrasi dengan aplikasi dan token Ethereum. Tersedia untuk iOS dan Android.

#### Dompet Peramban (*Browser Wallet*)

Berbagai dompet dan peramban DApp tersedia sebagai *plug-in* atau ekstensi dari peramban web seperti Chrome dan Firefox. Ini adalah klien jarak jauh yang berjalan di dalam peramban Anda.

Beberapa yang lebih populer adalah MetaMask, Jaxx, MyEtherWallet/MyCrypto, dan Mist.

**MetaMask**
MetaMask, yang diperkenalkan di Bab 2, adalah dompet berbasis peramban yang serbaguna, klien RPC, dan penjelajah kontrak dasar. Ini tersedia di Chrome, Firefox, Opera, dan Brave Browser.
Tidak seperti dompet peramban lainnya, MetaMask menyuntikkan instans `web3` ke dalam konteks JavaScript peramban, bertindak sebagai klien RPC yang terhubung ke berbagai *blockchain* Ethereum (*mainnet*, *testnet* Ropsten, *testnet* Kovan, *node* RPC lokal, dll.). Kemampuan untuk menyuntikkan instans `web3` dan bertindak sebagai gerbang ke layanan RPC eksternal membuat MetaMask menjadi alat yang sangat kuat bagi pengembang dan pengguna. Ini dapat digabungkan, misalnya, dengan MyEtherWallet atau MyCrypto, bertindak sebagai penyedia `web3` dan gerbang RPC untuk alat-alat tersebut.

**Jaxx**
Jaxx, yang diperkenalkan sebagai dompet seluler di bagian sebelumnya, juga tersedia sebagai ekstensi Chrome dan Firefox dan sebagai dompet desktop.

**MyEtherWallet (MEW)**
MyEtherWallet adalah klien jarak jauh JavaScript berbasis peramban yang menawarkan:

  * Dompet perangkat lunak yang berjalan di JavaScript.
  * Jembatan ke dompet perangkat keras populer seperti Trezor dan Ledger.
  * Antarmuka `web3` yang dapat terhubung ke instans `web3` yang disuntikkan oleh klien lain (misalnya, MetaMask).
  * Klien RPC yang dapat terhubung ke klien penuh Ethereum.
  * Antarmuka dasar yang dapat berinteraksi dengan *smart contract*, dengan adanya alamat kontrak dan *application binary interface* (ABI).

MyEtherWallet sangat berguna untuk pengujian dan sebagai antarmuka ke dompet perangkat keras. Ini tidak boleh digunakan sebagai dompet perangkat lunak utama, karena terpapar ancaman melalui lingkungan peramban dan bukan sistem penyimpanan kunci yang aman.

> Anda harus sangat berhati-hati saat mengakses MyEtherWallet dan dompet JavaScript berbasis peramban lainnya, karena mereka sering menjadi target *phishing*. Selalu gunakan *bookmark* dan bukan mesin pencari atau tautan untuk mengakses URL web yang benar.

**MyCrypto**
Tepat sebelum publikasi buku ini, proyek MyEtherWallet terpecah menjadi dua implementasi yang bersaing, dipandu oleh dua tim pengembangan independen: sebuah “*fork*,” sebagaimana disebut dalam pengembangan sumber terbuka. Kedua proyek tersebut disebut MyEtherWallet (merek asli) dan MyCrypto. Pada saat perpecahan, MyCrypto menawarkan fungsionalitas yang identik dengan MyEtherWallet, tetapi kemungkinan kedua proyek akan berbeda seiring kedua tim pengembangan mengadopsi tujuan dan prioritas yang berbeda.

**Mist**
Mist adalah peramban berkemampuan Ethereum pertama, yang dibuat oleh Ethereum Foundation. Ini berisi dompet berbasis peramban yang merupakan implementasi pertama dari standar token ERC20 (Fabian Vogelsteller, penulis ERC20, juga merupakan pengembang utama Mist). Mist juga merupakan dompet pertama yang memperkenalkan *checksum* camelCase (EIP-55). Mist menjalankan *full node*, dan menawarkan peramban DApp penuh dengan dukungan untuk penyimpanan berbasis Swarm dan alamat ENS.

### Kesimpulan

Dalam bab ini kita menjelajahi klien Ethereum. Anda telah mengunduh, menginstal, dan menyinkronkan klien, menjadi peserta dalam jaringan Ethereum, dan berkontribusi pada kesehatan dan stabilitas sistem dengan mereplikasi *blockchain* di komputer Anda sendiri.

---

# BAB 4
## Kriptografi

Salah satu teknologi dasar Ethereum adalah **kriptografi**, yang merupakan cabang matematika yang digunakan secara luas dalam keamanan komputer. Kriptografi berarti “tulisan rahasia” dalam bahasa Yunani, tetapi studi tentang kriptografi mencakup lebih dari sekadar tulisan rahasia, yang disebut sebagai **enkripsi**. Kriptografi, misalnya, juga dapat digunakan untuk membuktikan pengetahuan tentang suatu rahasia tanpa mengungkapkan rahasia itu (misalnya, dengan **tanda tangan digital**), atau untuk membuktikan keaslian data (misalnya, dengan sidik jari digital, juga dikenal sebagai “**hash**”). Jenis-jenis bukti kriptografis ini adalah alat matematika yang sangat penting untuk pengoperasian platform Ethereum (dan, memang, semua sistem *blockchain*), dan juga digunakan secara luas dalam aplikasi Ethereum.

Perlu dicatat bahwa, pada saat publikasi ini, tidak ada bagian dari protokol Ethereum yang melibatkan enkripsi; artinya semua komunikasi dengan platform Ethereum dan antar-*node* (termasuk data transaksi) tidak dienkripsi dan dapat (dan memang harus) dibaca oleh siapa saja. Hal ini bertujuan agar semua orang dapat memverifikasi kebenaran pembaruan *state* dan konsensus dapat tercapai. Di masa depan, alat kriptografi canggih, seperti *zero knowledge proofs* dan enkripsi homomorfik, akan tersedia yang akan memungkinkan beberapa perhitungan terenkripsi untuk dicatat di *blockchain* sambil tetap memungkinkan konsensus; namun, meskipun persiapan telah dibuat untuknya, alat-alat tersebut belum diterapkan.

Dalam bab ini kita akan memperkenalkan beberapa kriptografi yang digunakan di Ethereum: yaitu **kriptografi kunci publik (PKC)**, yang digunakan untuk mengontrol kepemilikan dana, dalam bentuk kunci privat dan alamat.

### Kunci dan Alamat

Seperti yang kita lihat sebelumnya dalam buku ini, Ethereum memiliki dua jenis akun yang berbeda: **akun milik eksternal (EOA)** dan **kontrak**. Kepemilikan ether oleh EOA ditetapkan melalui kunci privat digital, alamat Ethereum, dan tanda tangan digital. Kunci privat adalah inti dari semua interaksi pengguna dengan Ethereum. Faktanya, alamat akun diturunkan langsung dari kunci privat: sebuah kunci privat secara unik menentukan satu alamat Ethereum, yang juga dikenal sebagai akun.

Kunci privat tidak digunakan secara langsung dalam sistem Ethereum dengan cara apa pun; kunci tersebut tidak pernah ditransmisikan atau disimpan di Ethereum. Artinya, kunci privat harus tetap bersifat privat dan tidak pernah muncul dalam pesan yang diteruskan ke jaringan, juga tidak boleh disimpan secara *on-chain*; hanya alamat akun dan tanda tangan digital yang pernah ditransmisikan dan disimpan di sistem Ethereum. Untuk informasi lebih lanjut tentang cara menjaga keamanan kunci privat, lihat “Kontrol dan Tanggung Jawab” di halaman 15 dan Bab 5.

Akses dan kontrol dana dicapai dengan tanda tangan digital, yang juga dibuat menggunakan kunci privat. Transaksi Ethereum memerlukan tanda tangan digital yang valid untuk dimasukkan ke dalam *blockchain*. Siapa pun yang memiliki salinan kunci privat memiliki kendali atas akun yang sesuai dan ether apa pun yang dimilikinya. Dengan asumsi pengguna menjaga keamanan kunci privatnya, tanda tangan digital dalam transaksi Ethereum membuktikan pemilik sebenarnya dari dana tersebut, karena tanda tangan tersebut membuktikan kepemilikan kunci privat.

Dalam sistem berbasis kriptografi kunci publik, seperti yang digunakan oleh Ethereum, kunci datang berpasangan yang terdiri dari kunci privat (rahasia) dan kunci publik. Anggaplah kunci publik mirip dengan nomor rekening bank, dan kunci privat mirip dengan PIN rahasia; yang terakhir inilah yang memberikan kontrol atas akun, dan yang pertama yang mengidentifikasinya kepada orang lain. Kunci privat itu sendiri sangat jarang dilihat oleh pengguna Ethereum; sebagian besar, kunci tersebut disimpan (dalam bentuk terenkripsi) dalam file khusus dan dikelola oleh perangkat lunak dompet Ethereum.

Dalam bagian pembayaran dari sebuah transaksi Ethereum, penerima yang dituju diwakili oleh sebuah alamat Ethereum, yang digunakan dengan cara yang sama seperti detail rekening penerima manfaat dari sebuah transfer bank. Seperti yang akan kita lihat lebih detail nanti, alamat Ethereum untuk sebuah EOA dihasilkan dari bagian kunci publik dari sepasang kunci. Namun, tidak semua alamat Ethereum mewakili pasangan kunci publik-privat; alamat tersebut juga bisa mewakili kontrak, yang, seperti yang akan kita lihat di Bab 7, tidak didukung oleh kunci privat.

Di sisa bab ini, pertama-tama kita akan menjelajahi kriptografi dasar dengan sedikit lebih detail dan menjelaskan matematika yang digunakan di Ethereum. Kemudian kita akan melihat bagaimana kunci dibuat, disimpan, dan dikelola. Terakhir, kita akan meninjau berbagai format pengkodean yang digunakan untuk merepresentasikan kunci privat, kunci publik, dan alamat.

### Kriptografi Kunci Publik dan Mata Uang Kripto

**Kriptografi kunci publik** (juga disebut “kriptografi asimetris”) adalah bagian inti dari keamanan informasi modern. Protokol pertukaran kunci, yang pertama kali diterbitkan pada tahun 1970-an oleh Martin Hellman, Whitfield Diffie, dan Ralph Merkle, merupakan terobosan monumental yang memicu gelombang besar pertama minat publik di bidang kriptografi. Sebelum tahun 1970-an, pengetahuan kriptografi yang kuat dirahasiakan oleh pemerintah.

Kriptografi kunci publik menggunakan kunci unik untuk mengamankan informasi. Kunci-kunci ini didasarkan pada fungsi matematika yang memiliki sifat khusus: mudah untuk dihitung, tetapi sulit untuk menghitung kebalikannya. Berdasarkan fungsi-fungsi ini, kriptografi memungkinkan pembuatan rahasia digital dan tanda tangan digital yang tidak dapat dipalsukan, yang dijamin oleh hukum matematika.

Misalnya, mengalikan dua bilangan prima besar adalah hal yang sepele. Tetapi jika diberikan hasil kali dari dua bilangan prima besar, sangat sulit untuk menemukan faktor-faktor primanya (sebuah masalah yang disebut **faktorisasi prima**). Katakanlah kami menyajikan angka 8.018.009 dan memberitahu Anda bahwa itu adalah hasil kali dari dua bilangan prima. Menemukan kedua bilangan prima tersebut jauh lebih sulit bagi Anda daripada bagi saya untuk mengalikannya untuk menghasilkan 8.018.009.

Beberapa fungsi matematika ini dapat dibalik dengan mudah jika Anda mengetahui beberapa informasi rahasia. Dalam contoh sebelumnya, jika saya memberitahu Anda bahwa salah satu faktor primanya adalah 2.003, Anda dapat dengan mudah menemukan yang lain dengan pembagian sederhana: 8.018.009 ÷ 2.003 = 4.003. Fungsi semacam itu sering disebut ***trapdoor function*** karena sangat sulit untuk dibalik kecuali Anda diberi sepotong informasi rahasia yang dapat digunakan sebagai jalan pintas untuk membalikkan fungsi tersebut.

Kategori fungsi matematika yang lebih canggih yang berguna dalam kriptografi didasarkan pada operasi aritmatika pada **kurva eliptik**. Dalam aritmatika kurva eliptik, perkalian modulo sebuah bilangan prima itu sederhana tetapi pembagian (kebalikannya) secara praktis tidak mungkin. Ini disebut **masalah logaritma diskrit** dan saat ini tidak ada *trapdoor* yang diketahui. Kriptografi kurva eliptik digunakan secara luas dalam sistem komputer modern dan merupakan dasar dari penggunaan kunci privat dan tanda tangan digital oleh Ethereum (dan mata uang kripto lainnya).

> Lihat sumber daya berikut jika Anda tertarik untuk membaca lebih lanjut tentang kriptografi dan fungsi matematika yang digunakan dalam kriptografi modern:
>
>   * Kriptografi [http://bit.ly/2DcwNhn](http://bit.ly/2DcwNhn)
>   * *Trapdoor function* [http://bit.ly/2zeZV3c](http://bit.ly/2zeZV3c)
>   * Faktorisasi prima [http://bit.ly/2ACJjnV](http://bit.ly/2ACJjnV)
>   * Logaritma diskrit [http://bit.ly/2Q7mZYI](http://bit.ly/2Q7mZYI)
>   * Kriptografi kurva eliptik [http://bit.ly/2zfeKCP](http://bit.ly/2zfeKCP)

Di Ethereum, kita menggunakan kriptografi kunci publik (juga dikenal sebagai kriptografi asimetris) untuk membuat pasangan kunci publik-privat yang telah kita bicarakan dalam bab ini. Keduanya dianggap sebagai "pasangan" karena kunci publik diturunkan dari kunci privat. Bersama-sama, keduanya mewakili sebuah akun Ethereum dengan menyediakan, masing-masing, sebuah penanda akun yang dapat diakses publik (alamat) dan kontrol privat atas akses ke ether apa pun di akun tersebut dan atas otentikasi apa pun yang dibutuhkan akun saat menggunakan *smart contract*. Kunci privat mengontrol akses dengan menjadi satu-satunya informasi yang diperlukan untuk membuat tanda tangan digital, yang diperlukan untuk menandatangani transaksi untuk membelanjakan dana apa pun di akun tersebut. Tanda tangan digital juga digunakan untuk mengotentikasi pemilik atau pengguna kontrak, seperti yang akan kita lihat di Bab 7.

> Dalam sebagian besar implementasi dompet, kunci privat dan publik disimpan bersama sebagai pasangan kunci untuk kenyamanan. Namun, kunci publik dapat dihitung dengan mudah dari kunci privat, jadi menyimpan hanya kunci privat juga dimungkinkan.

Tanda tangan digital dapat dibuat untuk menandatangani pesan apa pun. Untuk transaksi Ethereum, detail dari transaksi itu sendiri digunakan sebagai pesan. Matematika kriptografi—dalam hal ini, kriptografi kurva eliptik—menyediakan cara agar pesan (yaitu, detail transaksi) dapat digabungkan dengan kunci privat untuk membuat kode yang hanya dapat diproduksi dengan pengetahuan tentang kunci privat. Kode itu disebut **tanda tangan digital**. Perhatikan bahwa transaksi Ethereum pada dasarnya adalah permintaan untuk mengakses akun tertentu dengan alamat Ethereum tertentu. Ketika sebuah transaksi dikirim ke jaringan Ethereum untuk memindahkan dana atau berinteraksi dengan *smart contract*, transaksi tersebut perlu dikirim dengan tanda tangan digital yang dibuat dengan kunci privat yang sesuai dengan alamat Ethereum yang bersangkutan. Matematika kurva eliptik berarti bahwa siapa pun dapat memverifikasi bahwa sebuah transaksi valid, dengan memeriksa bahwa tanda tangan digital cocok dengan detail transaksi dan alamat Ethereum yang aksesnya diminta. Proses verifikasi tidak melibatkan kunci privat sama sekali; itu tetap privat. Namun, proses verifikasi menentukan tanpa keraguan bahwa transaksi tersebut hanya bisa berasal dari seseorang dengan kunci privat yang sesuai dengan kunci publik di balik alamat Ethereum tersebut. Inilah "keajaiban" dari kriptografi kunci publik.

> Tidak ada enkripsi sebagai bagian dari protokol Ethereum—semua pesan yang dikirim sebagai bagian dari operasi jaringan Ethereum dapat (dan harus) dibaca oleh semua orang. Dengan demikian, kunci privat hanya digunakan untuk membuat tanda tangan digital untuk otentikasi transaksi.

### Kunci Privat

**Kunci privat** hanyalah sebuah angka, yang dipilih secara acak. Kepemilikan dan kontrol atas kunci privat adalah akar dari kontrol pengguna atas semua dana yang terkait dengan alamat Ethereum yang sesuai, serta akses ke kontrak yang mengotorisasi alamat tersebut. Kunci privat digunakan untuk membuat tanda tangan yang diperlukan untuk membelanjakan ether dengan membuktikan kepemilikan dana yang digunakan dalam sebuah transaksi. Kunci privat harus tetap **rahasia** setiap saat, karena mengungkapkannya kepada pihak ketiga sama dengan memberi mereka kendali atas ether dan kontrak yang diamankan oleh kunci privat tersebut. Kunci privat juga harus **dicadangkan** dan dilindungi dari kehilangan yang tidak disengaja. Jika hilang, kunci tersebut tidak dapat dipulihkan dan dana yang diamankan olehnya juga akan hilang selamanya.

> Kunci privat Ethereum hanyalah sebuah angka. Salah satu cara untuk memilih kunci privat Anda secara acak adalah dengan hanya menggunakan koin, pensil, dan kertas: lempar koin sebanyak 256 kali dan Anda memiliki digit biner dari kunci privat acak yang dapat Anda gunakan di dompet Ethereum (mungkin—lihat bagian selanjutnya). Kunci publik dan alamat kemudian dapat dihasilkan dari kunci privat.

#### Menghasilkan Kunci Privat dari Angka Acak

Langkah pertama dan terpenting dalam menghasilkan kunci adalah menemukan sumber entropi, atau keacakan, yang aman. Membuat kunci privat Ethereum pada dasarnya melibatkan pemilihan angka antara 1 dan 2\<sup\>256\</sup\>. Metode persis yang Anda gunakan untuk memilih angka itu tidak menjadi masalah selama tidak dapat diprediksi atau deterministik. Perangkat lunak Ethereum menggunakan generator angka acak dari sistem operasi yang mendasarinya untuk menghasilkan 256 bit acak. Biasanya, generator angka acak OS diinisialisasi oleh sumber keacakan manusia, itulah sebabnya Anda mungkin diminta untuk menggoyangkan mouse Anda selama beberapa detik, atau menekan tombol acak di keyboard Anda. Alternatifnya bisa berupa derau radiasi kosmik di saluran mikrofon komputer.

Lebih tepatnya, kunci privat dapat berupa angka bukan nol apa pun hingga angka yang sangat besar sedikit kurang dari 2\<sup\>256\</sup\>—angka 78 digit yang sangat besar, sekitar 1,158 \* 10\<sup\>77\</sup\>. Angka pastinya berbagi 38 digit pertama dengan 2\<sup\>256\</sup\> dan didefinisikan sebagai urutan kurva eliptik yang digunakan di Ethereum (lihat “Penjelasan Kriptografi Kurva Eliptik” di halaman 65). Untuk membuat kunci privat, kita secara acak memilih angka 256-bit dan memeriksa apakah berada dalam rentang yang valid. Dalam istilah pemrograman, ini biasanya dicapai dengan memasukkan string bit acak yang lebih besar (dikumpulkan dari sumber keacakan yang aman secara kriptografis) ke dalam algoritma hash 256-bit seperti Keccak-256 atau SHA-256, keduanya akan dengan mudah menghasilkan angka 256-bit. Jika hasilnya berada dalam rentang yang valid, kita memiliki kunci privat yang sesuai. Jika tidak, kita cukup mencoba lagi dengan angka acak lainnya.

> 2\<sup\>256\</sup\>—ukuran ruang kunci privat Ethereum—adalah angka yang luar biasa besar. Kira-kira 10\<sup\>77\</sup\> dalam desimal; yaitu, angka dengan 77 digit. Sebagai perbandingan, alam semesta yang terlihat diperkirakan mengandung 10\<sup\>80\</sup\> atom. Jadi, hampir ada cukup kunci privat untuk memberikan setiap atom di alam semesta sebuah akun Ethereum. Jika Anda memilih kunci privat secara acak, tidak ada cara yang masuk akal bagi siapa pun untuk menebaknya atau memilihnya sendiri.

Perhatikan bahwa proses pembuatan kunci privat adalah proses *offline*; tidak memerlukan komunikasi apa pun dengan jaringan Ethereum, atau bahkan komunikasi dengan siapa pun. Dengan demikian, untuk memilih angka yang tidak akan pernah dipilih oleh orang lain, angka itu harus benar-benar acak. Jika Anda memilih angka itu sendiri, kemungkinan orang lain akan mencobanya (dan kemudian kabur dengan ether Anda) terlalu tinggi. Menggunakan generator angka acak yang buruk (seperti fungsi `rand` pseudorandom di sebagian besar bahasa pemrograman) bahkan lebih buruk, karena lebih jelas dan lebih mudah untuk direplikasi. Sama seperti kata sandi untuk akun online, kunci privat harus tidak dapat ditebak. Untungnya, Anda tidak perlu mengingat kunci privat Anda, jadi Anda dapat mengambil pendekatan terbaik untuk memilihnya: yaitu, keacakan sejati.

> Jangan menulis kode Anda sendiri untuk membuat angka acak atau menggunakan generator angka acak "sederhana" yang ditawarkan oleh bahasa pemrograman Anda. Sangat penting bagi Anda untuk menggunakan generator angka pseudorandom yang aman secara kriptografis (seperti CSPRNG) dengan *seed* dari sumber entropi yang cukup. Pelajari dokumentasi pustaka generator angka acak yang Anda pilih untuk memastikannya aman secara kriptografis. Implementasi yang benar dari pustaka CSPRNG sangat penting untuk keamanan kunci.

Berikut ini adalah kunci privat yang dihasilkan secara acak yang ditampilkan dalam format heksadesimal (256 bit ditampilkan sebagai 64 digit heksadesimal, masing-masing 4 bit):

`f8f8a2f43c8376ccb0871305060d7b27b0554d2cc72bccf41b2705608452f315`

### Kunci Publik

Kunci publik Ethereum adalah sebuah titik pada kurva eliptik, yang berarti itu adalah satu set koordinat x dan y yang memenuhi persamaan kurva eliptik.

Dalam istilah yang lebih sederhana, kunci publik Ethereum adalah dua angka, yang digabungkan. Angka-angka ini dihasilkan dari kunci privat melalui perhitungan yang hanya bisa berjalan satu arah. Itu berarti bahwa sangat mudah untuk menghitung kunci publik jika Anda memiliki kunci privat, tetapi Anda tidak dapat menghitung kunci privat dari kunci publik.

> **MATEMATIKA** akan segera terjadi\! Jangan panik. Jika Anda mulai bingung di salah satu paragraf berikut, Anda dapat melewati beberapa bagian berikutnya. Ada banyak alat dan pustaka yang akan melakukan perhitungan untuk Anda.

Kunci publik dihitung dari kunci privat menggunakan perkalian kurva eliptik, yang secara praktis tidak dapat dibalik: **K = k \* G**, di mana **k** adalah kunci privat, **G** adalah titik konstan yang disebut *generator point*, **K** adalah kunci publik yang dihasilkan, dan \*\*\*\*\* adalah operator "perkalian" kurva eliptik khusus. Perhatikan bahwa perkalian kurva eliptik tidak seperti perkalian normal. Ia memiliki atribut fungsional yang sama dengan perkalian normal, tetapi hanya itu. Misalnya, operasi kebalikannya (yang akan menjadi pembagian untuk bilangan normal), yang dikenal sebagai "menemukan logaritma diskrit"—yaitu, menghitung **k** jika Anda tahu **K**—sama sulitnya dengan mencoba semua nilai **k** yang mungkin (pencarian *brute-force* yang kemungkinan akan memakan waktu lebih lama dari yang diizinkan oleh alam semesta ini).

Dalam istilah yang lebih sederhana: aritmatika pada kurva eliptik berbeda dari aritmatika integer "biasa". Sebuah titik (**G**) dapat dikalikan dengan sebuah integer (**k**) untuk menghasilkan titik lain (**K**). Tetapi tidak ada yang namanya pembagian, jadi tidak mungkin untuk hanya "membagi" kunci publik **K** dengan titik **G** untuk menghitung kunci privat **k**. Inilah fungsi matematika satu arah yang dijelaskan dalam “Kriptografi Kunci Publik dan Mata Uang Kripto” di halaman 60.

> Perkalian kurva eliptik adalah jenis fungsi yang oleh para kriptografer disebut fungsi "satu arah": mudah dilakukan dalam satu arah (perkalian) dan tidak mungkin dilakukan dalam arah sebaliknya (pembagian). Pemilik kunci privat dapat dengan mudah membuat kunci publik dan kemudian membagikannya kepada dunia, dengan mengetahui bahwa tidak ada yang dapat membalikkan fungsi tersebut dan menghitung kunci privat dari kunci publik. Trik matematika ini menjadi dasar untuk tanda tangan digital yang tidak dapat dipalsukan dan aman yang membuktikan kepemilikan dana Ethereum dan kontrol atas kontrak.

Sebelum kita mendemonstrasikan cara menghasilkan kunci publik dari kunci privat, mari kita lihat kriptografi kurva eliptik dengan sedikit lebih detail.

### Penjelasan Kriptografi Kurva Eliptik

Kriptografi kurva eliptik adalah jenis kriptografi asimetris atau kunci publik yang didasarkan pada masalah logaritma diskrit seperti yang diekspresikan oleh penjumlahan dan perkalian pada titik-titik kurva eliptik.

Gambar 4-1 adalah contoh kurva eliptik, mirip dengan yang digunakan oleh Ethereum.

> Ethereum menggunakan kurva eliptik yang sama persis, yang disebut **secp256k1**, seperti Bitcoin. Hal itu memungkinkan untuk menggunakan kembali banyak pustaka dan alat kurva eliptik dari Bitcoin.

<p align="center">
  <img src="images/books-07-mastering_ethereum/tabel-4.1.png" alt="gambar" width="580"/>
</p>

Ethereum uses a specific elliptic curve and set of mathematical constants, as defined
in a standard called secp256k1, established by the US National Institute of Standards
and Technology (NIST). The secp256k1 curve is defined by the following function,
which produces an elliptic curve:
y2 = x3 + 7 over � p
or:
y2 mod p = x3 + 7 mod p
The mod p (modulo prime number p) indicates that this curve is over a finite field of
prime order p, also written as � p, where p = 2256 – 232 – 29 – 28 – 27 – 26 – 24 – 1, which
is a very large prime number.
Because this curve is defined over a finite field of prime order instead of over the real
numbers, it looks like a pattern of dots scattered in two dimensions, which makes it
difficult to visualize. However, the math is identical to that of an elliptic curve over
real numbers. As an example, Figure 4-2 shows the same elliptic curve over a much
smaller finite field of prime order 17, showing a pattern of dots on a grid. The
secp256k1 Ethereum elliptic curve can be thought of as a much more complex pat‐
tern of dots on an unfathomably large grid.

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-4.1.png" alt="gambar" width="580"/>
</p>

Jadi, sebagai contoh, berikut ini adalah titik Q dengan koordinat (x,y) yang merupakan sebuah titik pada kurva `secp256k1`:
$Q =$
(49790390825249384486033144355916864607616083520101638681403973749255924539515,
59574132161899900045862086493921015780032175291755807399284007721050341297360\)

Contoh 4-1 menunjukkan bagaimana Anda dapat memeriksanya sendiri menggunakan Python. Variabel `x` dan `y` adalah koordinat dari titik Q, seperti pada contoh sebelumnya. Variabel `p` adalah orde prima dari kurva eliptik (bilangan prima yang digunakan untuk semua operasi modulo). Baris terakhir Python adalah persamaan kurva eliptik (operator `%` di Python adalah operator modulo). Jika `x` dan `y` memang koordinat dari sebuah titik pada kurva eliptik, maka mereka memenuhi persamaan dan hasilnya adalah nol (`0L` adalah bilangan bulat panjang dengan nilai nol). Cobalah sendiri, dengan mengetik `python` pada baris perintah dan menyalin setiap baris (setelah prompt `>>>`) dari daftar.

**Contoh 4-1. Menggunakan Python untuk mengonfirmasi bahwa titik ini berada pada kurva eliptik**

```python
Python 3.4.0 (default, Mar 30 2014, 19:23:13) 
[GCC 4.2.1 Compatible Apple LLVM 5.1 (clang-503.0.38)] on darwin 
Type "help", "copyright", "credits" or "license" for more information. 
>>> p = 115792089237316195423570985008687907853269984665640564039457584007908834671663 
>>> x = 49790390825249384486033144355916864607616083520101638681403973749255924539515 
>>> y = 59574132161899900045862086493921015780032175291755807399284007721050341297360 
>>> (x ** 3 + 7 - y**2) % p 
0L
```

## Operasi Aritmetika Kurva Eliptik

Banyak matematika kurva eliptik terlihat dan bekerja sangat mirip dengan aritmetika bilangan bulat yang kita pelajari di sekolah. Secara spesifik, kita dapat mendefinisikan sebuah operator penjumlahan, yang alih-alih melompat di sepanjang garis bilangan, ia melompat ke titik-titik lain pada kurva. Setelah kita memiliki operator penjumlahan, kita juga dapat mendefinisikan perkalian antara sebuah titik dan sebuah bilangan bulat, yang setara dengan penjumlahan berulang.

Penjumlahan kurva eliptik didefinisikan sedemikian rupa sehingga jika diberikan dua titik $P\_1$ dan $P\_2$ pada kurva eliptik, ada titik ketiga $P\_3 = P\_1 + P\_2$, yang juga berada pada kurva eliptik.

Secara geometris, titik ketiga $P\_3$ ini dihitung dengan menggambar garis antara $P\_1$ dan $P\_2$. Garis ini akan memotong kurva eliptik di tepat satu tempat tambahan (luar biasa). Sebut titik ini $P\_3' = (x, y)$. Kemudian cerminkan terhadap sumbu-x untuk mendapatkan $P\_3 = (x, –y)$.

Jika $P\_1$ dan $P\_2$ adalah titik yang sama, garis "antara" $P\_1$ dan $P\_2$ harus diperluas menjadi garis singgung kurva pada titik $P\_1$ ini. Garis singgung ini akan memotong kurva di tepat satu titik baru. Anda dapat menggunakan teknik dari kalkulus untuk menentukan kemiringan garis singgung. Anehnya, teknik-teknik ini berfungsi, meskipun kita membatasi minat kita pada titik-titik di kurva dengan dua koordinat bilangan bulat\!

Dalam matematika kurva eliptik, ada juga sebuah titik yang disebut **“titik di tak terhingga” (point at infinity)**, yang secara kasar sesuai dengan peran angka nol dalam penjumlahan. Di komputer, terkadang direpresentasikan dengan $x = y = 0$ (yang tidak memenuhi persamaan kurva eliptik, tetapi ini adalah kasus terpisah yang mudah diperiksa). Ada beberapa kasus khusus yang menjelaskan perlunya titik di tak terhingga.

  * Dalam beberapa kasus (misalnya, jika $P\_1$ dan $P\_2$ memiliki nilai x yang sama tetapi nilai y yang berbeda), garisnya akan persis vertikal, dalam hal ini $P\_3 =$ titik di tak terhingga.

  * Jika $P\_1$ adalah titik di tak terhingga, maka $P\_1 + P\_2 = P\_2$. Demikian pula, jika $P\_2$ adalah titik di tak terhingga, maka $P\_1 + P\_2 = P\_1$. Ini menunjukkan bagaimana titik di tak terhingga memainkan peran yang sama seperti nol dalam aritmetika "normal".

Ternyata `+` bersifat asosiatif, yang berarti $(A + B) + C = A + (B + C)$. Ini berarti kita dapat menulis $A + B + C$ (tanpa tanda kurung) tanpa ambiguitas.

Sekarang setelah kita mendefinisikan penjumlahan, kita dapat mendefinisikan perkalian dengan cara standar yang memperluas penjumlahan. Untuk sebuah titik $P$ pada kurva eliptik, jika $k$ adalah bilangan bulat, maka $k \* P = P + P + P + … + P$ ($k$ kali). Perhatikan bahwa $k$ kadang-kadang (mungkin membingungkan) disebut sebagai “eksponen” dalam kasus ini.

## Menghasilkan Kunci Publik

Dimulai dengan kunci privat dalam bentuk angka yang dihasilkan secara acak, $k$, kita mengalikannya dengan titik yang telah ditentukan sebelumnya pada kurva yang disebut **titik generator $G$** untuk menghasilkan titik lain di tempat lain pada kurva, yang merupakan kunci publik $K$ yang sesuai:

$$K = k*G$$

Titik generator ditentukan sebagai bagian dari standar `secp256k1`; ia sama untuk semua implementasi `secp256k1`, dan semua kunci yang berasal dari kurva tersebut menggunakan titik $G$ yang sama. Karena titik generator selalu sama untuk semua pengguna Ethereum, kunci privat $k$ yang dikalikan dengan $G$ akan selalu menghasilkan kunci publik $K$ yang sama. Hubungan antara $k$ dan $K$ adalah tetap, tetapi hanya dapat dihitung dalam satu arah, dari $k$ ke $K$. Itulah mengapa alamat Ethereum (yang diturunkan dari $K$) dapat dibagikan dengan siapa pun dan tidak mengungkapkan kunci privat pengguna ($k$).

Seperti yang kami jelaskan di bagian sebelumnya, perkalian $k \* G$ setara dengan penjumlahan berulang, yaitu $G + G + G + … + G$, diulang sebanyak $k$ kali. Singkatnya, untuk menghasilkan kunci publik $K$ dari kunci privat $k$, kita menambahkan titik generator $G$ ke dirinya sendiri, sebanyak $k$ kali.

> **Kunci privat dapat diubah menjadi kunci publik, tetapi kunci publik tidak dapat diubah kembali menjadi kunci privat, karena matematikanya hanya bekerja satu arah.**

Mari kita terapkan perhitungan ini untuk menemukan kunci publik untuk kunci privat spesifik yang kami tunjukkan di “Private Keys” di halaman 62:
$K = \\text{f8f8a2f43c8376ccb0871305060d7b27b0554d2cc72bccf41b2705608452f315} \* G$

Sebuah pustaka kriptografi dapat membantu kita menghitung $K$, menggunakan perkalian kurva eliptik. Kunci publik $K$ yang dihasilkan didefinisikan sebagai titik:
$K = (x, y)$

di mana:
$x = \\text{6e145ccef1033dea239875dd00dfb4fee6e3348b84985c92f103444683bae07b}$
$y = \\text{83b5c38e5e2b0c8529d7fa3f64d46daa1ece2d9ac14cab9477d042c84c32ccd0}$

Di Ethereum, Anda mungkin melihat kunci publik direpresentasikan sebagai serialisasi dari 130 karakter heksadesimal (65 byte). Ini diadopsi dari format serialisasi standar yang diusulkan oleh konsorsium industri Standards for Efficient Cryptography Group (SECG), yang didokumentasikan dalam Standards for Efficient Cryptography (SEC1). Standar ini mendefinisikan empat kemungkinan awalan yang dapat digunakan untuk mengidentifikasi titik pada kurva eliptik, yang tercantum dalam Tabel 4-1.

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-4.1.png" alt="gambar" width="580"/>
</p>

Ethereum hanya menggunakan kunci publik yang tidak terkompresi; oleh karena itu satu-satunya awalan yang relevan adalah (hex) `04`. Serialisasi ini menggabungkan koordinat `x` dan `y` dari kunci publik:

`04 + koordinat-x (32 byte/64 hex) + koordinat-y (32 byte/64 hex)`

Oleh karena itu, kunci publik yang kita hitung sebelumnya diserialisasikan sebagai:
`046e145ccef1033dea239875dd00dfb4fee6e3348b84985c92f103444683bae07b83b5c38e5e2b0c8529d7fa3f64d46daa1ece2d9ac14cab9477d042c84c32ccd0`

## Pustaka (Library) Kurva Eliptik

Ada beberapa implementasi dari kurva eliptik `secp256k1` yang digunakan dalam proyek-proyek terkait mata uang kripto:

  * **OpenSSL** `https://www.openssl.org/`
    Pustaka OpenSSL menawarkan seperangkat primitif kriptografi yang komprehensif, termasuk implementasi penuh `secp256k1`. Misalnya, untuk menurunkan kunci publik, fungsi `EC_POINT_mul` dapat digunakan.

  * **libsecp256k1** `https://github.com/bitcoin-core/secp256k1`
    `libsecp256k1` dari Bitcoin Core adalah implementasi bahasa C dari kurva eliptik `secp256k1` dan primitif kriptografi lainnya. Ini ditulis dari awal untuk menggantikan OpenSSL dalam perangkat lunak Bitcoin Core, dan dianggap lebih unggul baik dalam kinerja maupun keamanan.

## Fungsi Hash Kriptografis

Fungsi hash kriptografis digunakan di seluruh Ethereum. Faktanya, fungsi hash digunakan secara ekstensif di hampir semua sistem kriptografi—sebuah fakta yang ditangkap oleh kriptografer Bruce Schneier, yang berkata, “Jauh lebih dari algoritma enkripsi, fungsi hash satu arah adalah pekerja keras kriptografi modern.”

Di bagian ini kita akan membahas fungsi hash, menjelajahi properti dasarnya, dan melihat bagaimana properti tersebut membuatnya begitu berguna di begitu banyak area kriptografi modern. Kami membahas fungsi hash di sini karena mereka adalah bagian dari transformasi kunci publik Ethereum menjadi alamat. Mereka juga dapat digunakan untuk membuat sidik jari digital, yang membantu dalam verifikasi data.

Secara sederhana, **fungsi hash** adalah "fungsi apa pun yang dapat digunakan untuk memetakan data berukuran sembarang ke data berukuran tetap." Input ke fungsi hash disebut *pre-image*, *pesan*, atau просто *data input*. Outputnya disebut *hash*. **Fungsi hash kriptografis** adalah subkategori khusus yang memiliki properti spesifik yang berguna untuk platform aman, seperti Ethereum.

Fungsi hash kriptografis adalah **fungsi hash satu arah** yang memetakan data berukuran sembarang ke string bit berukuran tetap. Sifat "satu arah" berarti secara komputasi tidak memungkinkan untuk membuat ulang data input jika seseorang hanya mengetahui hash outputnya. Satu-satunya cara untuk menentukan input yang mungkin adalah dengan melakukan pencarian *brute-force*, memeriksa setiap kandidat untuk output yang cocok; mengingat ruang pencarian yang hampir tak terbatas, mudah untuk memahami ketidakmungkinan praktis dari tugas tersebut. Bahkan jika Anda menemukan beberapa data input yang menciptakan hash yang cocok, itu mungkin bukan data input asli: fungsi hash adalah fungsi "banyak-ke-satu". Menemukan dua set data input yang menghasilkan hash output yang sama disebut menemukan **tabrakan hash (hash collision)**. Secara kasar, semakin baik fungsi hash, semakin jarang tabrakan hash terjadi. Untuk Ethereum, hal ini secara efektif tidak mungkin.

Mari kita lihat lebih dekat properti utama dari fungsi hash kriptografis. Ini termasuk:

  * **Deterministik**
    Pesan input yang diberikan selalu menghasilkan output hash yang sama.

  * **Dapat Diverifikasi (Verifiability)**
    Menghitung hash dari sebuah pesan itu efisien (kompleksitas linear).

  * **Non-korelasi**
    Perubahan kecil pada pesan (misalnya, perubahan 1-bit) harus mengubah output hash secara ekstensif sehingga tidak dapat dikorelasikan dengan hash dari pesan asli.

  * **Tidak dapat dibalik (Irreversibility)**
    Menghitung pesan dari hash-nya tidak memungkinkan, setara dengan pencarian *brute-force* melalui semua kemungkinan pesan.

  * **Perlindungan terhadap tabrakan (Collision protection)**
    Seharusnya tidak memungkinkan untuk menghitung dua pesan berbeda yang menghasilkan output hash yang sama.

Ketahanan terhadap tabrakan hash sangat penting untuk menghindari pemalsuan tanda tangan digital di Ethereum.

Kombinasi dari properti-properti ini membuat fungsi hash kriptografis berguna untuk berbagai aplikasi keamanan, termasuk:

  * Sidik jari data (Data fingerprinting)
  * Integritas pesan (deteksi kesalahan)
  * Proof of work
  * Otentikasi (hashing kata sandi dan peregangan kunci)
  * Generator angka pseudo-acak
  * Komitmen pesan (mekanisme commit-reveal)
  * Pengidentifikasi unik

Kita akan menemukan banyak dari ini di Ethereum saat kita maju melalui berbagai lapisan sistem.

## Fungsi Hash Kriptografis Ethereum: Keccak-256

Ethereum menggunakan fungsi hash kriptografis **Keccak-256** di banyak tempat. Keccak-256 dirancang sebagai kandidat untuk Kompetisi Fungsi Hash Kriptografis SHA-3 yang diadakan pada tahun 2007 oleh National Institute of Science and Technology (NIST). Keccak adalah algoritma pemenang, yang menjadi standar sebagai Federal Information Processing Standard (FIPS) 202 pada tahun 2015.

Namun, selama periode ketika Ethereum dikembangkan, standardisasi NIST belum final. NIST menyesuaikan beberapa parameter Keccak setelah penyelesaian proses standar, yang diduga untuk meningkatkan efisiensinya. Ini terjadi pada saat yang sama ketika pelapor pelanggaran (whistleblower) heroik Edward Snowden mengungkapkan dokumen yang menyiratkan bahwa NIST mungkin telah dipengaruhi secara tidak semestinya oleh National Security Agency (NSA) untuk sengaja melemahkan standar generator angka acak Dual\_EC\_DRBG, yang secara efektif menempatkan *backdoor* di dalam standar generator angka acak tersebut. Hasil dari kontroversi ini adalah reaksi keras terhadap perubahan yang diusulkan dan penundaan yang signifikan dalam standardisasi SHA-3. Pada saat itu, Ethereum Foundation memutuskan untuk mengimplementasikan algoritma Keccak asli, seperti yang diusulkan oleh para penemunya, daripada standar SHA-3 yang dimodifikasi oleh NIST.

> **Meskipun Anda mungkin melihat "SHA-3" disebutkan di seluruh dokumen dan kode Ethereum, banyak jika tidak semua contoh tersebut sebenarnya merujuk pada Keccak-256, bukan standar FIPS-202 SHA-3 yang sudah final.** Perbedaan implementasinya kecil, berkaitan dengan parameter *padding*, tetapi signifikan karena Keccak-256 menghasilkan output hash yang berbeda dari FIPS-202 SHA-3 untuk input yang sama.

### Fungsi Hash Mana yang Saya Gunakan?

Bagaimana Anda bisa tahu jika pustaka perangkat lunak yang Anda gunakan mengimplementasikan FIPS-202 SHA-3 atau Keccak-256, jika keduanya mungkin disebut "SHA-3"?

Cara mudah untuk mengetahuinya adalah dengan menggunakan *test vector*, yaitu output yang diharapkan untuk input tertentu. Tes yang paling umum digunakan untuk fungsi hash adalah input kosong. Jika Anda menjalankan fungsi hash dengan string kosong sebagai input, Anda akan melihat hasil berikut:

`Keccak256("") = c5d2460186f7233c927e7db2dcc703c0e500b653ca82273b7bfad8045d85a470`

`SHA3("") = a7ffc6f8bf1ed76651c14756a061d662f580ff4de43b49fa82d80a4b80f8434a`

Terlepas dari apa nama fungsinya, Anda dapat mengujinya untuk melihat apakah itu Keccak-256 asli atau standar NIST final FIPS-202 SHA-3 dengan menjalankan tes sederhana ini. Ingat, Ethereum menggunakan Keccak-256, meskipun sering disebut SHA-3 dalam kode.

> Karena kebingungan yang diciptakan oleh perbedaan antara fungsi hash yang digunakan di Ethereum (Keccak-256) dan standar yang sudah final (FIP-202 SHA-3), ada upaya yang sedang berlangsung untuk mengganti nama semua instansi `sha3` di semua kode, *opcode*, dan pustaka menjadi `keccak256`. Lihat ERC59 untuk detailnya.

Selanjutnya, mari kita periksa aplikasi pertama Keccak-256 di Ethereum, yaitu untuk menghasilkan alamat Ethereum dari kunci publik.

## Alamat Ethereum

Alamat Ethereum adalah pengidentifikasi unik yang diturunkan dari kunci publik atau kontrak menggunakan fungsi hash satu arah Keccak-256.

Dalam contoh kita sebelumnya, kita mulai dengan kunci privat dan menggunakan perkalian kurva eliptik untuk mendapatkan kunci publik:

**Kunci privat k:**
`k = f8f8a2f43c8376ccb0871305060d7b27b0554d2cc72bccf41b2705608452f315`

**Kunci publik K** (koordinat x dan y digabungkan dan ditampilkan sebagai hex):
`K = 6e145ccef1033dea239875dd00dfb4fee6e3348b84985c92f103444683bae07b83b5c38e5e...`

> Perlu dicatat bahwa kunci publik tidak diformat dengan awalan (hex) `04` saat alamat dihitung.

Kita menggunakan Keccak-256 untuk menghitung hash dari kunci publik ini:

`Keccak256(K) = 2a5bc342ed616b5ba5732269001d3f1ef827552ae1114027bd3ecf1f086ba0f9`

Kemudian kita hanya menyimpan 20 byte terakhir (byte yang paling tidak signifikan), yang merupakan alamat Ethereum kita:

`001d3f1ef827552ae1114027bd3ecf1f086ba0f9`

Paling sering Anda akan melihat alamat Ethereum dengan awalan `0x` yang menunjukkan bahwa mereka dikodekan dalam heksadesimal, seperti ini:

`0x001d3f1ef827552ae1114027bd3ecf1f086ba0f9`

## Format Alamat Ethereum

Alamat Ethereum adalah angka heksadesimal, pengidentifikasi yang diturunkan dari 20 byte terakhir dari hash Keccak-256 dari kunci publik.

Tidak seperti alamat Bitcoin, yang dikodekan di antarmuka pengguna semua klien untuk menyertakan *checksum* bawaan untuk melindungi dari kesalahan pengetikan alamat, alamat Ethereum disajikan sebagai heksadesimal mentah tanpa *checksum* apa pun.

Alasan di balik keputusan itu adalah bahwa alamat Ethereum pada akhirnya akan disembunyikan di balik abstraksi (seperti layanan nama) di lapisan yang lebih tinggi dari sistem dan *checksum* harus ditambahkan di lapisan yang lebih tinggi jika perlu.

Pada kenyataannya, lapisan-lapisan yang lebih tinggi ini dikembangkan terlalu lambat dan pilihan desain ini menyebabkan sejumlah masalah di masa-masa awal ekosistem, termasuk hilangnya dana karena kesalahan pengetikan alamat dan kesalahan validasi input. Selain itu, karena layanan nama Ethereum dikembangkan lebih lambat dari yang diperkirakan, pengkodean alternatif diadopsi dengan sangat lambat oleh pengembang dompet. Kita akan melihat beberapa opsi pengkodean selanjutnya.

### Inter exchange Client Address Protocol (ICAP)

Inter exchange Client Address Protocol (ICAP) adalah pengkodean alamat Ethereum yang sebagian kompatibel dengan pengkodean International Bank Account Number (IBAN), menawarkan pengkodean yang serbaguna, memiliki *checksum*, dan dapat dioperasikan untuk alamat Ethereum. Alamat ICAP dapat mengkodekan alamat Ethereum atau nama umum yang terdaftar di registri nama Ethereum. Anda dapat membaca lebih lanjut tentang ICAP di Wiki Ethereum.

IBAN adalah standar internasional untuk mengidentifikasi nomor rekening bank, sebagian besar digunakan untuk transfer kawat. Ini diadopsi secara luas di Area Pembayaran Euro Tunggal Eropa (SEPA) dan sekitarnya. IBAN adalah layanan terpusat dan sangat teregulasi. ICAP adalah implementasi yang terdesentralisasi namun kompatibel untuk alamat Ethereum.

IBAN terdiri dari string hingga 34 karakter alfanumerik (tidak peka huruf besar-kecil) yang terdiri dari kode negara, *checksum*, dan pengidentifikasi rekening bank (yang spesifik untuk negara).

ICAP menggunakan struktur yang sama dengan memperkenalkan kode negara non-standar, "XE," yang merupakan singkatan dari "Ethereum," diikuti oleh *checksum* dua karakter dan tiga kemungkinan variasi pengenal akun:

  * **Direct**
    Sebuah integer *big-endian base-36* yang terdiri dari hingga 30 karakter alfanumerik, mewakili 155 bit paling tidak signifikan dari sebuah alamat Ethereum. Karena pengkodean ini kurang dari 160 bit penuh dari alamat Ethereum umum, ini hanya berfungsi untuk alamat Ethereum yang dimulai dengan satu atau lebih byte nol. Keuntungannya adalah kompatibel dengan IBAN, dalam hal panjang bidang dan *checksum*.
    Contoh: `XE60HAMICDXSV5QXVJA7TJW47Q9CHWKJD` (panjang 33 karakter).

  * **Basic**
    Sama seperti pengkodean Direct, kecuali panjangnya 31 karakter. Hal ini memungkinkannya untuk mengkodekan alamat Ethereum apa pun, tetapi membuatnya tidak kompatibel dengan validasi bidang IBAN.
    Contoh: `XE18CHDJBPLTBCJ03FE9O2NS0BPOJVQCU2P` (panjang 35 karakter).

  * **Indirect**
    Mengkodekan pengidentifikasi yang mengarah ke alamat Ethereum melalui penyedia registri nama. Ini menggunakan 16 karakter alfanumerik, terdiri dari pengidentifikasi aset (mis., ETH), layanan nama (mis., XREG), dan nama 9 karakter yang dapat dibaca manusia (mis., KITTYCATS).
    Contoh: `XE##ETHXREGKITTYCATS` (panjang 20 karakter), di mana `##` harus diganti dengan dua karakter *checksum* yang dihitung.

Kita dapat menggunakan alat baris perintah `helpeth` untuk membuat alamat ICAP. Mari kita coba dengan kunci privat contoh kita (diawali dengan `0x` dan diteruskan sebagai parameter ke `helpeth`):

```bash
$ helpeth keyDetails \
 -p 0xf8f8a2f43c8376ccb0871305060d7b27b0554d2cc72bccf41b2705608452f315

Address: 0x001d3f1ef827552ae1114027bd3ecf1f086ba0f9
ICAP: XE60 HAMI CDXS V5QX VJA7 TJW4 7Q9C HWKJ D
Public key: 0x6e145ccef1033dea239875dd00dfb4fee6e3348b84985c92f103444683bae07b...
```

Perintah `helpeth` membuat alamat Ethereum heksadesimal serta alamat ICAP untuk kita. Alamat ICAP untuk kunci contoh kita adalah:
`XE60HAMICDXSV5QXVJA7TJW47Q9CHWKJD`

Karena alamat Ethereum contoh kita kebetulan dimulai dengan byte nol, ia dapat dikodekan menggunakan metode pengkodean ICAP Direct yang valid dalam format IBAN. Anda bisa tahu karena panjangnya 33 karakter.

Jika alamat kita tidak dimulai dengan nol, itu akan dikodekan dengan pengkodean Basic, yang akan memiliki panjang 35 karakter dan tidak valid sebagai IBAN.

> **Peluang alamat Ethereum apa pun dimulai dengan byte nol adalah 1 banding 256.** Untuk menghasilkan yang seperti itu, rata-rata akan membutuhkan 256 percobaan dengan 256 kunci privat acak yang berbeda sebelum kita menemukan satu yang berfungsi sebagai alamat ICAP yang dikodekan "Direct" yang kompatibel dengan IBAN.

Saat ini, ICAP sayangnya hanya didukung oleh beberapa dompet.

### Pengkodean Hex dengan Checksum dalam Kapitalisasi (EIP-55)

Karena lambatnya penerapan ICAP dan layanan nama, sebuah standar diusulkan oleh Ethereum Improvement Proposal 55 (EIP-55). EIP-55 menawarkan *checksum* yang kompatibel ke belakang untuk alamat Ethereum dengan memodifikasi kapitalisasi alamat heksadesimal. Idenya adalah bahwa alamat Ethereum tidak peka huruf besar-kecil dan semua dompet seharusnya menerima alamat Ethereum yang diekspresikan dalam karakter huruf besar atau kecil, tanpa perbedaan interpretasi.

Dengan memodifikasi kapitalisasi karakter alfabet dalam alamat, kita dapat menyampaikan *checksum* yang dapat digunakan untuk melindungi integritas alamat terhadap kesalahan pengetikan atau pembacaan. Dompet yang tidak mendukung *checksum* EIP-55 hanya mengabaikan fakta bahwa alamat tersebut mengandung kapitalisasi campuran, tetapi yang mendukungnya dapat memvalidasinya dan mendeteksi kesalahan dengan akurasi 99,986%.

Pengkodean kapitalisasi campuran ini halus dan Anda mungkin tidak menyadarinya pada awalnya. Alamat contoh kita adalah:
`0x001d3f1ef827552ae1114027bd3ecf1f086ba0f9`

Dengan *checksum* kapitalisasi campuran EIP-55, menjadi:
`0x001d3F1ef827552Ae1114027BD3ECF1f086bA0F9`

Bisakah Anda melihat perbedaannya? Beberapa karakter alfabet (A–F) dari alfabet pengkodean heksadesimal sekarang menjadi huruf besar, sementara yang lain huruf kecil.

EIP-55 cukup sederhana untuk diimplementasikan. Kita mengambil hash Keccak-256 dari alamat heksadesimal huruf kecil. Hash ini bertindak sebagai sidik jari digital dari alamat, memberi kita *checksum* yang nyaman. Setiap perubahan kecil pada input (alamat) akan menyebabkan perubahan besar pada hash yang dihasilkan (*checksum*), memungkinkan kita mendeteksi kesalahan secara efektif. Hash dari alamat kita kemudian dikodekan dalam kapitalisasi alamat itu sendiri.

Mari kita uraikan, langkah demi langkah:

1.  Hash alamat huruf kecil, tanpa awalan `0x`:
    `Keccak256("001d3f1ef827552ae1114027bd3ecf1f086ba0f9") = 23a69c1653e4ebbb619b0b2cb8a9bad49892a8b9695d9a19d8f673ca991deae1`

2.  Kapitalkan setiap karakter alfabet alamat jika digit heksadesimal yang sesuai dari hash lebih besar dari atau sama dengan `0x8`. Ini lebih mudah ditunjukkan jika kita menyejajarkan alamat dan hash:

    ```
    Alamat: 001d3f1ef827552ae1114027bd3ecf1f086ba0f9
    Hash  : 23a69c1653e4ebbb619b0b2cb8a9bad49892a8b9...
    ```

    Alamat kita mengandung karakter alfabet `d` di posisi keempat. Karakter keempat dari hash adalah `6`, yang lebih kecil dari 8. Jadi, kita biarkan `d` tetap huruf kecil. Karakter alfabet berikutnya di alamat kita adalah `f`, di posisi keenam. Karakter keenam dari hash heksadesimal adalah `c`, yang lebih besar dari 8. Oleh karena itu, kita mengkapitalkan `F` di alamat, dan seterusnya. Seperti yang Anda lihat, kita hanya menggunakan 20 byte pertama (40 karakter hex) dari hash sebagai *checksum*, karena kita hanya memiliki 20 byte (40 karakter hex) di alamat untuk dikapitalkan dengan tepat.

Periksa sendiri alamat kapitalisasi campuran yang dihasilkan dan lihat apakah Anda dapat mengetahui karakter mana yang dikapitalkan dan karakter mana yang sesuai dengannya di hash alamat:

```
Alamat: 001d3F1ef827552Ae1114027BD3ECF1f086bA0F9
Hash  : 23a69c1653e4ebbb619b0b2cb8a9bad49892a8b9...
```

#### Mendeteksi kesalahan pada alamat yang dikodekan EIP-55

Sekarang, mari kita lihat bagaimana alamat EIP-55 akan membantu kita menemukan kesalahan. Mari kita asumsikan kita telah mencetak alamat Ethereum, yang dikodekan EIP-55:
`0x001d3F1ef827552Ae1114027BD3ECF1f086bA0F9`

Sekarang mari kita buat kesalahan dasar dalam membaca alamat itu. Karakter sebelum yang terakhir adalah huruf `F` besar. Untuk contoh ini, mari kita asumsikan kita salah membacanya sebagai huruf `E` besar, dan kita mengetik alamat berikut (yang salah) ke dompet kita:
`0x001d3F1ef827552Ae1114027BD3ECF1f086bA0E9`

Untungnya, dompet kita sesuai dengan EIP-55\! Dompet memperhatikan kapitalisasi campuran dan mencoba memvalidasi alamat tersebut. Dompet mengubahnya menjadi huruf kecil, dan menghitung hash *checksum*:

`Keccak256("001d3f1ef827552ae1114027bd3ecf1f086ba0e9") = 5429b5d9460122fb4b11af9cb88b7bb76d8928862e0a57d46dd18dd8e08a6927`

Seperti yang Anda lihat, meskipun alamat hanya berubah satu karakter (faktanya, hanya satu bit, karena `e` dan `f` berbeda satu bit), hash alamat telah berubah secara radikal. Itulah properti dari fungsi hash yang membuatnya sangat berguna untuk *checksum*\!

Sekarang, mari kita sejajarkan keduanya dan periksa kapitalisasinya:

```
Alamat: 001d3F1ef827552Ae1114027BD3ECF1f086bA0E9
Hash  : 5429b5d9460122fb4b11af9cb88b7bb76d892886...
```

Semuanya salah\! Beberapa karakter alfabet dikapitalkan secara tidak benar. Ingat bahwa kapitalisasi adalah pengkodean dari *checksum* yang benar.

Kapitalisasi alamat yang kita masukkan tidak cocok dengan *checksum* yang baru saja dihitung, yang berarti ada sesuatu yang telah berubah di alamat, dan sebuah kesalahan telah terjadi.

## Kesimpulan

Dalam bab ini kami memberikan survei singkat tentang kriptografi kunci publik dan berfokus pada penggunaan kunci publik dan privat di Ethereum serta penggunaan alat kriptografi, seperti fungsi hash, dalam pembuatan dan verifikasi alamat Ethereum. Kami juga melihat tanda tangan digital dan bagaimana mereka dapat menunjukkan kepemilikan kunci privat tanpa mengungkapkan kunci privat tersebut. Di Bab 5, kita akan menyatukan ide-ide ini dan melihat bagaimana dompet dapat digunakan untuk mengelola koleksi kunci.

---

# BAB 5
## Dompet (Wallets)

Kata “dompet” atau *"wallet"* digunakan untuk mendeskripsikan beberapa hal yang berbeda di Ethereum.

Pada tingkat tinggi, **dompet adalah aplikasi perangkat lunak yang berfungsi sebagai antarmuka pengguna utama ke Ethereum**. Dompet mengontrol akses ke uang pengguna, mengelola kunci dan alamat, melacak saldo, serta membuat dan menandatangani transaksi. Selain itu, beberapa dompet Ethereum juga dapat berinteraksi dengan kontrak, seperti token ERC20.

Lebih sempit lagi, dari perspektif seorang pemrogram, kata dompet merujuk pada **sistem yang digunakan untuk menyimpan dan mengelola kunci pengguna**. Setiap dompet memiliki komponen manajemen kunci. Bagi beberapa dompet, hanya itu saja yang ada. Dompet lain adalah bagian dari kategori yang jauh lebih luas, yaitu *browser*, yang merupakan antarmuka untuk aplikasi terdesentralisasi berbasis Ethereum, atau DApps, yang akan kita periksa lebih detail di Bab 12. Tidak ada garis pemisah yang jelas antara berbagai kategori yang digabungkan di bawah istilah dompet.

Dalam bab ini kita akan melihat dompet sebagai wadah untuk kunci privat, dan sebagai sistem untuk mengelola kunci-kunci ini.

### Tinjauan Teknologi Dompet

Di bagian ini kami merangkum berbagai teknologi yang digunakan untuk membangun dompet Ethereum yang ramah pengguna, aman, dan fleksibel.

Salah satu pertimbangan utama dalam merancang dompet adalah menyeimbangkan **kenyamanan dan privasi**. Dompet Ethereum yang paling nyaman adalah yang memiliki satu kunci privat dan alamat yang Anda gunakan kembali untuk semuanya. Sayangnya, solusi seperti itu adalah mimpi buruk privasi, karena siapa pun dapat dengan mudah melacak dan menghubungkan semua transaksi Anda. Menggunakan kunci baru untuk setiap transaksi adalah yang terbaik untuk privasi, tetapi menjadi sangat sulit untuk dikelola. Keseimbangan yang tepat sulit dicapai, tetapi itulah mengapa desain dompet yang baik sangat penting.

Kesalahpahaman umum tentang Ethereum adalah bahwa dompet Ethereum berisi ether atau token. Faktanya, secara tegas, **dompet hanya menyimpan kunci**. Ether atau token lainnya dicatat di blockchain Ethereum. Pengguna mengontrol token di jaringan dengan menandatangani transaksi menggunakan kunci di dompet mereka. Dalam arti tertentu, **dompet Ethereum adalah sebuah gantungan kunci**. Meskipun demikian, mengingat bahwa kunci yang dipegang oleh dompet adalah satu-satunya hal yang diperlukan untuk mentransfer ether atau token kepada orang lain, dalam praktiknya perbedaan ini tidak terlalu relevan. Perbedaan ini menjadi penting dalam mengubah pola pikir dari berurusan dengan sistem terpusat perbankan konvensional (di mana hanya Anda, dan bank, yang dapat melihat uang di rekening Anda, dan Anda hanya perlu meyakinkan bank bahwa Anda ingin memindahkan dana untuk melakukan transaksi) ke sistem terdesentralisasi platform blockchain (di mana semua orang dapat melihat saldo ether sebuah akun, meskipun mereka mungkin tidak tahu siapa pemilik akun tersebut, dan semua orang perlu diyakinkan bahwa pemilik ingin memindahkan dana agar transaksi dapat diberlakukan). Dalam praktiknya ini berarti ada cara independen untuk memeriksa saldo akun, tanpa memerlukan dompetnya. Selain itu, Anda dapat memindahkan penanganan akun Anda dari dompet saat ini ke dompet yang berbeda, jika Anda mulai tidak menyukai aplikasi dompet yang Anda gunakan pada awalnya.

> Dompet Ethereum berisi kunci, bukan ether atau token. Dompet ibarat gantungan kunci yang berisi pasangan kunci privat dan publik. Pengguna menandatangani transaksi dengan kunci privat, dengan demikian membuktikan bahwa mereka memiliki ether tersebut. Ether disimpan di blockchain.

Ada dua jenis utama dompet, dibedakan berdasarkan apakah kunci yang dikandungnya saling berhubungan atau tidak.

Tipe pertama adalah **dompet non-deterministik**, di mana setiap kunci dibuat secara independen dari nomor acak yang berbeda. Kunci-kunci tersebut tidak saling berhubungan. Jenis dompet ini juga dikenal sebagai **dompet JBOK**, dari frasa “Just a Bunch of Keys” (Hanya Sekumpulan Kunci).

Tipe kedua adalah **dompet deterministik**, di mana semua kunci diturunkan dari satu kunci utama tunggal, yang dikenal sebagai **seed**. Semua kunci dalam jenis dompet ini saling berhubungan dan dapat dibuat kembali jika seseorang memiliki *seed* asli. Ada sejumlah metode derivasi kunci yang berbeda yang digunakan dalam dompet deterministik. Metode derivasi yang paling umum digunakan menggunakan struktur seperti pohon, seperti yang dijelaskan dalam “Dompet Deterministik Hirarkis (BIP-32/BIP-44)” di halaman 82.

Untuk membuat dompet deterministik sedikit lebih aman terhadap kecelakaan kehilangan data, seperti ponsel Anda dicuri atau jatuh ke toilet, *seed* sering dikodekan sebagai daftar kata (dalam bahasa Inggris atau bahasa lain) untuk Anda tulis dan gunakan jika terjadi kecelakaan. Ini dikenal sebagai **kata-kata kode mnemonic** dompet. Tentu saja, jika seseorang mendapatkan kata-kata kode mnemonic Anda, maka mereka juga dapat membuat ulang dompet Anda dan dengan demikian mendapatkan akses ke ether dan kontrak pintar Anda. Oleh karena itu, berhati-hatilah dengan daftar kata pemulihan Anda\! **Jangan pernah menyimpannya secara elektronik**, dalam sebuah file, di komputer atau ponsel Anda. Tuliskan di atas kertas dan simpan di tempat yang aman dan terlindungi.

Beberapa bagian berikutnya memperkenalkan masing-masing teknologi ini pada tingkat tinggi.

### Dompet Non-Deterministik (Acak)

Di dompet Ethereum pertama (yang diproduksi untuk pra-penjualan Ethereum), setiap file dompet menyimpan satu kunci privat yang dibuat secara acak. Dompet semacam itu digantikan dengan dompet deterministik karena dompet "gaya lama" ini dalam banyak hal lebih rendah. Misalnya, dianggap praktik yang baik untuk menghindari penggunaan kembali alamat Ethereum sebagai bagian dari memaksimalkan privasi Anda saat menggunakan Ethereum—yaitu, menggunakan alamat baru (yang memerlukan kunci privat baru) setiap kali Anda menerima dana. Anda bisa melangkah lebih jauh dan menggunakan alamat baru untuk setiap transaksi, meskipun ini bisa menjadi mahal jika Anda banyak berurusan dengan token. Untuk mengikuti praktik ini, dompet non-deterministik perlu secara teratur menambah daftar kuncinya, yang berarti Anda perlu membuat cadangan secara teratur. Jika Anda kehilangan data (kegagalan disk, kecelakaan minuman, ponsel dicuri) sebelum Anda berhasil mencadangkan dompet Anda, Anda akan kehilangan akses ke dana dan kontrak pintar Anda. Dompet non-deterministik "tipe 0" adalah yang paling sulit untuk ditangani, karena mereka membuat file dompet baru untuk setiap alamat baru secara “just in time”.

Meskipun demikian, banyak klien Ethereum (termasuk geth) menggunakan file **keystore**, yang merupakan file berenkode JSON yang berisi satu kunci privat (yang dibuat secara acak), dienkripsi dengan *passphrase* untuk keamanan ekstra. Isi file JSON terlihat seperti ini:

```json
{
"address": "001d3f1ef827552ae1114027bd3ecf1f086ba0f9",
"crypto": {
"cipher": "aes-128-ctr",
"ciphertext":
"233a9f4d236ed0c13394b504b6da5df02587c8bf1ad8946f6f2b58f055507ece",
"cipherparams": {
"iv": "d10c6ec5bae81b6cb9144de81037fa15"
},
"kdf": "scrypt",
"kdfparams": {
"dklen": 32,
"n": 262144,
"p": 1,
"r": 8,
"salt":
"99d37a47c7c9429c66976f643f386a61b78b97f3246adca89abe4245d2788407"
},
"mac": "594c8df1c8ee0ded8255a50caf07e8c12061fd859f4b7c76ab704b17c957e842"
},
"id": "4fcb2ba4-ccdb-424f-89d5-26cce304bf9c",
"version": 3
}
```

Format keystore menggunakan **key derivation function (KDF)**, juga dikenal sebagai algoritma peregangan kata sandi (*password stretching*), yang melindungi dari serangan *brute-force*, kamus, dan *rainbow table*. Secara sederhana, kunci privat tidak dienkripsi oleh *passphrase* secara langsung. Sebaliknya, *passphrase* diregangkan, dengan melakukan hashing berulang kali. Fungsi hashing diulang sebanyak 262.144 putaran, yang dapat dilihat di JSON keystore sebagai parameter `crypto.kdfparams.n`. Penyerang yang mencoba melakukan *brute-force* pada *passphrase* harus menerapkan 262.144 putaran hashing untuk setiap *passphrase* yang dicoba, yang memperlambat serangan secukupnya untuk membuatnya tidak mungkin dilakukan untuk *passphrase* dengan kompleksitas dan panjang yang memadai.

Ada sejumlah pustaka perangkat lunak yang dapat membaca dan menulis format keystore, seperti pustaka JavaScript `keythereum`.

> Penggunaan dompet non-deterministik tidak disarankan untuk apa pun selain tes sederhana. Dompet ini terlalu merepotkan untuk dicadangkan dan digunakan untuk situasi apa pun kecuali yang paling dasar. Sebaliknya, gunakan dompet HD berbasis standar industri dengan *seed* mnemonic untuk pencadangan.

### Dompet Deterministik (Berbasis Seed)

Dompet deterministik atau "berbasis *seed*" adalah dompet yang berisi kunci privat yang semuanya diturunkan dari satu kunci utama tunggal, atau **seed**. *Seed* adalah angka yang dihasilkan secara acak yang dikombinasikan dengan data lain, seperti nomor indeks atau “kode rantai” (*chain code*) (lihat “Kunci publik dan privat yang diperluas” di halaman 93), untuk mendapatkan sejumlah kunci privat.

Dalam dompet deterministik, *seed* sudah cukup untuk memulihkan semua kunci yang diturunkan, dan oleh karena itu satu cadangan tunggal, pada saat pembuatan, sudah cukup untuk mengamankan semua dana dan kontrak pintar di dalam dompet. *Seed* juga cukup untuk ekspor atau impor dompet, memungkinkan migrasi yang mudah dari semua kunci di antara implementasi dompet yang berbeda. Desain ini membuat keamanan *seed* menjadi yang paling penting, karena hanya *seed* yang diperlukan untuk mendapatkan akses ke seluruh dompet. Di sisi lain, kemampuan untuk memfokuskan upaya keamanan pada satu bagian data dapat dilihat sebagai keuntungan.

### Dompet Deterministik Hirarkis (BIP-32/BIP-44)

Dompet deterministik dikembangkan untuk memudahkan penurunan banyak kunci dari satu *seed* tunggal. Saat ini, bentuk paling canggih dari dompet deterministik adalah **dompet deterministik hirarkis (HD)** yang didefinisikan oleh standar BIP-32 Bitcoin. Dompet HD berisi kunci yang diturunkan dalam struktur pohon, sedemikian rupa sehingga kunci induk dapat menurunkan urutan kunci anak, yang masing-masing dapat menurunkan urutan kunci cucu, dan seterusnya. Struktur pohon ini diilustrasikan pada Gambar 5-1.

\<p align="center"\>
  \<img src="images/books-07-mastering\_ethereum/figure-5.1.png" alt="gambar" width="580"/\>
\</p\>

Dompet HD menawarkan beberapa keuntungan utama dibandingkan dompet deterministik yang lebih sederhana. Pertama, **struktur pohon dapat digunakan untuk mengekspresikan makna organisasi tambahan**, seperti ketika cabang subkunci tertentu digunakan untuk menerima pembayaran masuk dan cabang yang berbeda digunakan untuk menerima kembalian dari pembayaran keluar. Cabang kunci juga dapat digunakan dalam pengaturan perusahaan, mengalokasikan cabang yang berbeda ke departemen, anak perusahaan, fungsi spesifik, atau kategori akuntansi.

Keuntungan kedua dari dompet HD adalah bahwa **pengguna dapat membuat urutan kunci publik tanpa memiliki akses ke kunci privat yang sesuai**. Ini memungkinkan dompet HD digunakan di server yang tidak aman atau dalam kapasitas hanya-tonton (*watch-only*) atau hanya-terima (*receive-only*), di mana dompet tidak memiliki kunci privat yang dapat membelanjakan dana.

### Seed dan Kode mnemonic (BIP-39)

Ada banyak cara untuk mengkodekan kunci privat untuk pencadangan dan pemulihan yang aman. Metode yang saat ini lebih disukai adalah menggunakan **urutan kata** yang, bila diambil bersama-sama dalam urutan yang benar, dapat secara unik membuat ulang kunci privat. Ini kadang-kadang dikenal sebagai **mnemonic**, dan pendekatan ini telah distandarisasi oleh BIP-39. Saat ini, banyak dompet Ethereum (serta dompet untuk mata uang kripto lainnya) menggunakan standar ini, dan dapat mengimpor dan mengekspor *seed* untuk pencadangan dan pemulihan menggunakan mnemonic yang dapat dioperasikan.

Untuk melihat mengapa pendekatan ini menjadi populer, mari kita lihat sebuah contoh:

```
FCCF1AB3329FD5DA3DA9577511F8F137

wolf juice proud gown wool unfair
wall cliff insect more detail hub
```

Secara praktis, kemungkinan kesalahan saat menulis urutan heksadesimal sangat tinggi. Sebaliknya, daftar kata yang diketahui cukup mudah untuk ditangani, terutama karena ada tingkat redundansi yang tinggi dalam penulisan kata (terutama kata-kata bahasa Inggris). Jika “inzect” tercatat secara tidak sengaja, dapat dengan cepat ditentukan, saat pemulihan dompet diperlukan, bahwa “inzect” bukan kata bahasa Inggris yang valid dan bahwa “insect” harus digunakan sebagai gantinya. Kita berbicara tentang menulis representasi *seed* karena itu adalah praktik yang baik saat mengelola dompet HD: *seed* diperlukan untuk memulihkan dompet jika terjadi kehilangan data (baik karena kecelakaan atau pencurian), jadi menyimpan cadangan sangat bijaksana. Namun, *seed* harus dijaga sangat privat, jadi cadangan digital harus dihindari dengan hati-hati; oleh karena itu saran sebelumnya untuk mencadangkan dengan pena dan kertas.

Singkatnya, penggunaan daftar kata pemulihan untuk mengkodekan *seed* untuk dompet HD menjadi cara termudah untuk mengekspor, menyalin, mencatat di atas kertas, membaca tanpa kesalahan, dan mengimpor satu set kunci privat ke dompet lain dengan aman.

### Praktik Terbaik Dompet (Wallet Best Practices)

Seiring dengan matangnya teknologi dompet mata uang kripto, standar industri umum tertentu telah muncul yang membuat dompet dapat dioperasikan secara luas, mudah digunakan, aman, dan fleksibel. Standar-standar ini juga memungkinkan dompet untuk menurunkan kunci untuk berbagai mata uang kripto yang berbeda, semuanya dari satu mnemonic tunggal. Standar umum ini adalah:

  * Kata-kata kode mnemonic, berdasarkan **BIP-39**
  * Dompet HD, berdasarkan **BIP-32**
  * Struktur dompet HD multiguna, berdasarkan **BIP-43**
  * Dompet multikurensi dan multiakun, berdasarkan **BIP-44**

Standar-standar ini mungkin berubah atau menjadi usang oleh perkembangan di masa depan, tetapi untuk saat ini mereka membentuk seperangkat teknologi yang saling terkait yang telah menjadi standar dompet de facto untuk sebagian besar platform blockchain dan mata uang kripto mereka.

Standar-standar tersebut telah diadopsi oleh berbagai macam dompet perangkat lunak dan perangkat keras, membuat semua dompet ini dapat dioperasikan. Pengguna dapat mengekspor mnemonic yang dibuat di salah satu dompet ini dan mengimpornya ke dompet lain, memulihkan semua kunci dan alamat.

Beberapa contoh dompet perangkat lunak yang mendukung standar ini termasuk (diurutkan berdasarkan abjad) **Jaxx, MetaMask, MyCrypto, dan MyEtherWallet (MEW)**. Contoh dompet perangkat keras yang mendukung standar ini termasuk **Keepkey, Ledger, dan Trezor**.

Bagian-bagian berikut memeriksa masing-masing teknologi ini secara detail.

> Jika Anda mengimplementasikan dompet Ethereum, dompet tersebut harus dibangun sebagai dompet HD, dengan *seed* yang dikodekan sebagai kata kode mnemonic untuk pencadangan, mengikuti standar BIP-32, BIP-39, BIP-43, dan BIP-44, seperti yang dijelaskan di bagian berikut.

### Kata-Kata Kode mnemonic (BIP-39)

Kata-kata kode mnemonic adalah urutan kata yang mengkodekan nomor acak yang digunakan sebagai *seed* untuk menurunkan dompet deterministik. Urutan kata sudah cukup untuk membuat ulang *seed*, dan dari sana membuat ulang dompet dan semua kunci yang diturunkan. Aplikasi dompet yang mengimplementasikan dompet deterministik dengan kata-kata mnemonic akan menunjukkan kepada pengguna urutan 12 hingga 24 kata saat pertama kali membuat dompet. Urutan kata itu adalah cadangan dompet, dan dapat digunakan untuk memulihkan dan membuat ulang semua kunci di aplikasi dompet yang sama atau yang kompatibel. Seperti yang kami jelaskan sebelumnya, daftar kata mnemonic memudahkan pengguna untuk mencadangkan dompet, karena mudah dibaca dan disalin dengan benar.

> Kata-kata mnemonic sering disalahartikan dengan “brainwallets.” Keduanya tidak sama. Perbedaan utamanya adalah *brainwallet* terdiri dari kata-kata yang dipilih oleh pengguna, sedangkan kata-kata mnemonic dibuat secara acak oleh dompet dan disajikan kepada pengguna. Perbedaan penting ini membuat kata-kata mnemonic jauh lebih aman, karena manusia adalah sumber keacakan yang sangat buruk. Mungkin yang lebih penting, menggunakan istilah “brainwallet” menyiratkan bahwa kata-kata tersebut harus dihafal, yang merupakan ide yang buruk, dan resep untuk tidak memiliki cadangan Anda saat Anda membutuhkannya.

Kode mnemonic didefinisikan dalam BIP-39. Perhatikan bahwa BIP-39 adalah salah satu implementasi dari standar kode mnemonic. Ada standar yang berbeda, dengan seperangkat kata yang berbeda, yang digunakan oleh dompet Bitcoin Electrum dan mendahului BIP-39. BIP-39 diusulkan oleh perusahaan di balik dompet perangkat keras Trezor dan tidak kompatibel dengan implementasi Electrum. Namun, BIP-39 kini telah mencapai dukungan industri yang luas di puluhan implementasi yang dapat dioperasikan dan harus dianggap sebagai standar industri de facto. Selanjutnya, BIP-39 dapat digunakan untuk menghasilkan dompet multikurensi yang mendukung Ethereum, sedangkan *seed* Electrum tidak bisa.

BIP-39 mendefinisikan pembuatan kode mnemonic dan *seed*, yang kami jelaskan di sini dalam sembilan langkah. Untuk kejelasan, prosesnya dibagi menjadi dua bagian: langkah 1 hingga 6 ditunjukkan di “Menghasilkan kata-kata mnemonic” di halaman 86 dan langkah 7 hingga 9 ditunjukkan di “Dari mnemonic ke seed”.

### Menghasilkan kata-kata mnemonic

Kata-kata mnemonic dihasilkan secara otomatis oleh dompet menggunakan proses terstandarisasi yang didefinisikan dalam BIP-39. Dompet dimulai dari sumber entropi (sumber keacakan), menambahkan *checksum*, lalu memetakan entropi tersebut ke daftar kata:

1.  Buat urutan acak secara kriptografis ($S$) dengan panjang 128 hingga 256 bit.
2.  Buat *checksum* dari $S$ dengan mengambil bit-bit pertama dari hash SHA-256 dari $S$. Jumlah bit yang diambil adalah `(panjang S) / 32`.
3.  Tambahkan *checksum* ke akhir urutan acak $S$.
4.  Bagi gabungan urutan-dan-*checksum* menjadi beberapa bagian yang masing-masing panjangnya 11 bit.
5.  Petakan setiap nilai 11-bit ke sebuah kata dari kamus yang telah ditentukan sebelumnya yang berisi 2.048 kata.
6.  Buat kode mnemonic dari urutan kata-kata tersebut, dengan tetap mempertahankan urutannya.

Gambar 5-2 menunjukkan bagaimana entropi digunakan untuk menghasilkan kata-kata mnemonic.

Tabel 5-1 menunjukkan hubungan antara ukuran data entropi dan panjang kode mnemonic dalam jumlah kata.

<p align="center">
  <img src="images/books-07-mastering_ethereum/tabel-5.1.png" alt="gambar" width="580"/>
</p>

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-5.2.png" alt="gambar" width="580"/>
</p>

### Dari mnemonic ke seed

Kata-kata mnemonic merepresentasikan entropi dengan panjang 128 hingga 256 bit. Entropi tersebut kemudian digunakan untuk menurunkan *seed* yang lebih panjang (512-bit) melalui penggunaan **fungsi peregangan kunci (key-stretching function) PBKDF2**. *Seed* yang dihasilkan digunakan untuk membangun dompet deterministik dan menurunkan kunci-kuncinya.

Fungsi peregangan kunci mengambil dua parameter: **mnemonic** dan **salt**. Tujuan dari *salt* dalam fungsi peregangan kunci adalah untuk menyulitkan pembuatan tabel pencarian (*lookup table*) yang memungkinkan serangan *brute-force*. Dalam standar BIP-39, *salt* memiliki tujuan lain: memungkinkan pengenalan *passphrase* yang berfungsi sebagai faktor keamanan tambahan yang melindungi *seed*, seperti yang akan kami jelaskan lebih detail di “Passphrase opsional dalam BIP-39” di halaman 90.

Proses yang dijelaskan dalam langkah 7 hingga 9 berlanjut dari proses yang dijelaskan di bagian sebelumnya:

7.  Parameter pertama untuk fungsi peregangan kunci PBKDF2 adalah mnemonic yang dihasilkan pada langkah 6.
8.  Parameter kedua untuk fungsi peregangan kunci PBKDF2 adalah *salt*. *Salt* terdiri dari konstanta string `"mnemonic"` yang digabungkan dengan *passphrase* opsional yang disediakan pengguna.
9.  PBKDF2 meregangkan parameter mnemonic dan *salt* menggunakan 2.048 putaran hashing dengan algoritma HMAC-SHA512, menghasilkan nilai 512-bit sebagai output akhirnya. Nilai 512-bit itulah yang menjadi **seed**.

Gambar 5-3 menunjukkan bagaimana sebuah mnemonic digunakan untuk menghasilkan *seed*.

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-5.3.png" alt="gambar" width="580"/>
</p>

> Fungsi peregangan kunci, dengan 2.048 putaran hashing-nya, merupakan perlindungan yang cukup efektif terhadap serangan *brute-force* terhadap mnemonic atau *passphrase*. Hal ini membuatnya mahal (secara komputasi) untuk mencoba lebih dari beberapa ribu kombinasi *passphrase* dan mnemonic, sementara jumlah kemungkinan *seed* yang diturunkan sangat besar ($2^{512}$, atau sekitar $10^{154}$)—jauh lebih besar dari jumlah atom di alam semesta yang terlihat (sekitar $10^{80}$).

Tabel 5-2, 5-3, dan 5-4 menunjukkan beberapa contoh kode mnemonic dan *seed* yang dihasilkannya.

**Tabel 5-2. Kode mnemonic entropi 128-bit, tanpa passphrase, menghasilkan seed**
| | |
|---|---|
|**Input Entropi (128 bit)**|`0c1e24e5917779d297e14d45f14e1a1a`|
|**mnemonic (12 kata)**|`army van defense carry jealous true garbage claim echo media make crunch`|
|**Passphrase**| (tidak ada) |
|**Seed (512 bit)**|`5b56c417303faa3fcba7e57400e120a0ca83ec5a4fc9ffba757fbe63fbd77a89a1a3be4c67196f57c39a88b76373733891bfaba16ed27a813ceed498804c0570`|

**Tabel 5-3. Kode mnemonic entropi 128-bit, dengan passphrase, menghasilkan seed**
| | |
|---|---|
|**Input Entropi (128 bit)**|`0c1e24e5917779d297e14d45f14e1a1a`|
|**mnemonic (12 kata)**|`army van defense carry jealous true garbage claim echo media make crunch`|
|**Passphrase**|`SuperDuperSecret`|
|**Seed (512 bit)**|`3b5df16df2157104cfdd22830162a5e170c0161653e3afe6c88defeefb0818c793dbb28ab3ab091897d0715861dc8a18358f80b79d49acf64142ae57037d1d54`|

**Tabel 5-4. Kode mnemonic entropi 256-bit, tanpa passphrase, menghasilkan seed**
| | |
|---|---|
|**Input Entropi (256 bit)**|`2041546864449caff939d32d574753fe684d3c947c3346713dd8423e74abcf8c`|
|**Mnemonic (24 kata)**|`cake apple borrow silk endorse fitness top denial coil riot stay wolf luggage oxygen faint major edit measure invite love trap field dilemma oblige`|
|**Passphrase**| (tidak ada) |
|**Seed (512 bit)**|`3269bce2674acbd188d4f120072b13b088a0ecf87c6e4cae41657a0bb78f5315b33b3a04356e53d062e55f1e0deaa082df8d487381379df848a6ad7e98798404`|

### Passphrase opsional dalam BIP-39

Standar BIP-39 memungkinkan penggunaan *passphrase* opsional dalam derivasi *seed*. Jika tidak ada *passphrase* yang digunakan, mnemonic diregangkan dengan *salt* yang terdiri dari string konstan `"mnemonic"`, menghasilkan *seed* 512-bit spesifik dari mnemonic tertentu. Jika *passphrase* digunakan, fungsi peregangan menghasilkan *seed* yang berbeda dari mnemonic yang sama. Faktanya, dengan satu mnemonic, setiap *passphrase* yang mungkin akan menghasilkan *seed* yang berbeda. Intinya, tidak ada *passphrase* yang “salah”. Semua *passphrase* valid dan semuanya mengarah ke *seed* yang berbeda, membentuk sekumpulan besar kemungkinan dompet yang belum diinisialisasi. Kumpulan dompet yang mungkin sangat besar ($2^{512}$) sehingga tidak ada kemungkinan praktis untuk melakukan *brute-forcing* atau menebak secara tidak sengaja salah satu yang sedang digunakan, selama *passphrase* memiliki kompleksitas dan panjang yang cukup.

> Tidak ada *passphrase* yang “salah” dalam BIP-39. Setiap *passphrase* mengarah ke beberapa dompet, yang kecuali sebelumnya digunakan akan kosong.

*Passphrase* opsional menciptakan dua fitur penting:

  * **Faktor kedua** (sesuatu yang dihafal) yang membuat mnemonic tidak berguna jika berdiri sendiri, melindungi cadangan mnemonic dari kompromi oleh pencuri.
  * Bentuk **penyangkalan yang masuk akal (*plausible deniability*)** atau “dompet paksaan (*duress wallet*)”, di mana *passphrase* yang dipilih mengarah ke dompet dengan sejumlah kecil dana, digunakan untuk mengalihkan perhatian penyerang dari dompet “asli” yang berisi sebagian besar dana.

Namun, penting untuk dicatat bahwa penggunaan *passphrase* juga membawa risiko kehilangan:

  * Jika pemilik dompet tidak mampu atau meninggal dan tidak ada orang lain yang tahu *passphrase*-nya, *seed* menjadi tidak berguna dan semua dana yang disimpan di dompet akan hilang selamanya.
  * Sebaliknya, jika pemilik mencadangkan *passphrase* di tempat yang sama dengan *seed*, itu mengalahkan tujuan dari faktor kedua.

Meskipun *passphrase* sangat berguna, mereka hanya boleh digunakan dalam kombinasi dengan proses yang direncanakan dengan cermat untuk pencadangan dan pemulihan, dengan mempertimbangkan kemungkinan ahli waris yang masih hidup dari pemilik dapat memulihkan mata uang kripto tersebut.

### Bekerja dengan kode mnemonic

BIP-39 diimplementasikan sebagai pustaka dalam banyak bahasa pemrograman yang berbeda. Sebagai contoh:

  * **python-mnemonic**
    Implementasi referensi standar oleh tim SatoshiLabs yang mengusulkan BIP-39, dalam Python.
  * **ConsenSys/eth-lightwallet**
    Dompet JS Ethereum ringan untuk *node* dan *browser* (dengan BIP-39).
  * **npm/bip39**
    Implementasi JavaScript dari Bitcoin BIP-39: Kode mnemonic untuk menghasilkan kunci deterministik.

Ada juga generator BIP-39 yang diimplementasikan dalam halaman web mandiri (Gambar 5-4), yang sangat berguna untuk pengujian dan eksperimen. Mnemonic Code Converter menghasilkan mnemonic, *seed*, dan kunci privat yang diperluas. Ini dapat digunakan secara luring di browser, atau diakses secara daring.

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-5.4.png" alt="gambar" width="580"/>
</p>

### Membuat Dompet HD dari Seed

Dompet HD dibuat dari satu **root seed**, yang merupakan angka acak 128-, 256-, atau 512-bit. Paling umum, *seed* ini dihasilkan dari mnemonic seperti yang dijelaskan di bagian sebelumnya.

Setiap kunci di dompet HD diturunkan secara deterministik dari *root seed* ini, yang memungkinkan untuk membuat ulang seluruh dompet HD dari *seed* tersebut di dompet HD lain yang kompatibel. Hal ini memudahkan untuk mengekspor, mencadangkan, memulihkan, dan mengimpor dompet HD yang berisi ribuan atau bahkan jutaan kunci dengan hanya mentransfer mnemonic dari mana *root seed* diturunkan.

### Dompet HD (BIP-32) dan Path (BIP-43/44)

Sebagian besar dompet HD mengikuti standar BIP-32, yang telah menjadi standar industri de facto untuk pembuatan kunci deterministik.

Kami не akan membahas semua detail BIP-32 di sini, hanya komponen yang diperlukan untuk memahami bagaimana ia digunakan di dompet. Aspek penting utama adalah hubungan hirarkis seperti pohon yang dapat dimiliki oleh kunci-kunci turunan, seperti yang dapat Anda lihat di Gambar 5-1. Penting juga untuk memahami gagasan tentang kunci yang diperluas (*extended keys*) dan kunci yang diperkeras (*hardened keys*), yang dijelaskan di bagian berikut.

Ada puluhan implementasi BIP-32 yang dapat dioperasikan yang ditawarkan di banyak pustaka perangkat lunak. Sebagian besar dirancang untuk dompet Bitcoin, yang mengimplementasikan alamat dengan cara yang berbeda, tetapi berbagi implementasi derivasi kunci yang sama dengan dompet Ethereum yang kompatibel dengan BIP-32. Gunakan yang dirancang untuk Ethereum, atau adaptasi dari Bitcoin dengan menambahkan pustaka pengkodean alamat Ethereum.

Ada juga generator BIP-32 yang diimplementasikan sebagai halaman web mandiri yang sangat berguna untuk pengujian dan eksperimen dengan BIP-32.

> Generator BIP-32 mandiri bukanlah situs HTTPS. Itu untuk mengingatkan Anda bahwa penggunaan alat ini tidak aman. Ini hanya untuk pengujian. Anda tidak boleh menggunakan kunci yang dihasilkan oleh situs ini dengan dana nyata.

#### Kunci publik dan privat yang diperluas (Extended)

Dalam terminologi BIP-32, kunci dapat “diperluas” (*extended*). Dengan operasi matematika yang tepat, kunci “induk” yang diperluas ini dapat digunakan untuk menurunkan kunci “anak”, sehingga menghasilkan hirarki kunci dan alamat yang dijelaskan sebelumnya. Kunci induk tidak harus berada di puncak pohon. Ia dapat dipilih dari mana saja dalam hirarki pohon.

Memperluas kunci melibatkan pengambilan kunci itu sendiri dan menambahkan **chain code** khusus padanya. *Chain code* adalah string biner 256-bit yang dicampur dengan setiap kunci untuk menghasilkan kunci anak.

Jika kuncinya adalah kunci privat, ia menjadi **kunci privat yang diperluas** yang dibedakan dengan awalan `xprv`:
`xprv9s21ZrQH143K2JF8RafpqtKiTbsbaxEeUaMnNHsm5o6wCW3z8ySyH4UxFVSfZ8n7ESu7fgir8i...`

**Kunci publik yang diperluas** dibedakan dengan awalan `xpub`:
`xpub661MyMwAqRbcEnKbXcCqD2GT1di5zQxVqoHPAgHNe8dv5JP8gWmDproS6kFHJnLZd23tWevhdn...`

Karakteristik yang sangat berguna dari dompet HD adalah kemampuan untuk menurunkan kunci publik anak dari kunci publik induk, tanpa memiliki kunci privat. Ini memberi kita dua cara untuk menurunkan kunci publik anak: baik langsung dari kunci privat anak, atau dari kunci publik induk.

Kunci publik yang diperluas dapat digunakan, oleh karena itu, untuk menurunkan semua kunci publik (dan hanya kunci publik) di cabang struktur dompet HD tersebut.

Jalan pintas ini dapat digunakan untuk membuat penyebaran hanya-kunci-publik yang sangat aman, di mana server atau aplikasi memiliki salinan kunci publik yang diperluas, tetapi tidak ada kunci privat sama sekali. Jenis penyebaran seperti itu dapat menghasilkan jumlah kunci publik dan alamat Ethereum yang tak terbatas, tetapi tidak dapat membelanjakan uang apa pun yang dikirim ke alamat-alamat tersebut. Sementara itu, di server lain yang lebih aman, kunci privat yang diperluas dapat menurunkan semua kunci privat yang sesuai untuk menandatangani transaksi dan membelanjakan uang.

Salah satu aplikasi umum dari metode ini adalah menginstal kunci publik yang diperluas di server web yang melayani aplikasi *e-commerce*. Server web dapat menggunakan fungsi derivasi kunci publik untuk membuat alamat Ethereum baru untuk setiap transaksi (misalnya, untuk keranjang belanja pelanggan), dan tidak akan memiliki kunci privat apa pun yang rentan terhadap pencurian. Tanpa dompet HD, satu-satunya cara untuk melakukan ini adalah dengan menghasilkan ribuan alamat Ethereum di server aman terpisah dan kemudian memuatnya di server *e-commerce*. Pendekatan itu merepotkan dan memerlukan pemeliharaan terus-menerus untuk memastikan bahwa server не kehabisan kunci, oleh karena itu preferensi untuk menggunakan kunci publik yang diperluas dari dompet HD.

Aplikasi umum lain dari solusi ini adalah untuk *cold-storage* atau dompet perangkat keras. Dalam skenario itu, kunci privat yang diperluas dapat disimpan di dompet perangkat keras, sementara kunci publik yang diperluas dapat disimpan secara daring. Pengguna dapat membuat alamat “terima” sesuka hati, sementara kunci privat disimpan dengan aman secara luring. Untuk membelanjakan dana, pengguna dapat menggunakan kunci privat yang diperluas di klien Ethereum penandatangan luring, atau menandatangani transaksi di perangkat dompet perangkat keras.

#### Derivasi kunci anak yang diperkeras (Hardened)

Kemampuan untuk menurunkan cabang kunci publik dari kunci publik yang diperluas, atau `xpub`, sangat berguna, tetapi datang dengan risiko potensial. Akses ke `xpub` tidak memberikan akses ke kunci privat anak. Namun, karena `xpub` berisi *chain code* (digunakan untuk menurunkan kunci publik anak dari kunci publik induk), jika kunci privat anak diketahui, atau entah bagaimana bocor, ia dapat digunakan dengan *chain code* untuk menurunkan semua kunci privat anak lainnya. Satu kunci privat anak yang bocor, bersama dengan *chain code* induk, mengungkapkan semua kunci privat dari semua anak. Lebih buruk lagi, kunci privat anak bersama dengan *chain code* induk dapat digunakan untuk menyimpulkan kunci privat induk.

Untuk mengatasi risiko ini, dompet HD menggunakan fungsi derivasi alternatif yang disebut **derivasi yang diperkeras (hardened derivation)**, yang “memutus” hubungan antara kunci publik induk dan *chain code* anak. Fungsi derivasi yang diperkeras menggunakan kunci privat induk untuk menurunkan *chain code* anak, alih-alih kunci publik induk. Ini menciptakan “firewall” dalam urutan induk/anak, dengan *chain code* yang tidak dapat digunakan untuk mengkompromikan kunci privat induk atau saudara.

Secara sederhana, jika Anda ingin menggunakan kemudahan `xpub` untuk menurunkan cabang kunci publik tanpa mengekspos diri Anda pada risiko *chain code* yang bocor, Anda harus menurunkannya dari induk yang diperkeras, bukan induk normal. Praktik terbaik adalah memiliki anak-anak tingkat-1 dari kunci master selalu diturunkan dengan derivasi yang diperkeras, untuk mencegah kompromi kunci master.

#### Nomor indeks untuk derivasi normal dan hardened

Jelas diinginkan untuk dapat menurunkan lebih dari satu kunci anak dari kunci induk tertentu. Untuk mengelola ini, nomor indeks digunakan. Setiap nomor indeks, ketika dikombinasikan dengan kunci induk menggunakan fungsi derivasi anak khusus, memberikan kunci anak yang berbeda. Nomor indeks yang digunakan dalam fungsi derivasi induk-ke-anak BIP-32 adalah integer 32-bit. Untuk dengan mudah membedakan antara kunci yang diturunkan melalui fungsi derivasi normal (tidak diperkeras) versus kunci yang diturunkan melalui derivasi yang diperkeras, nomor indeks ini dibagi menjadi dua rentang. Nomor indeks antara 0 dan $2^{31}–1$ (0x0 hingga 0x7FFFFFFF) hanya digunakan untuk derivasi normal. Nomor indeks antara $2^{31}$ dan $2^{32}–1$ (0x80000000 hingga 0xFFFFFFFF) hanya digunakan untuk derivasi yang diperkeras. Oleh karena itu, jika nomor indeks kurang dari $2^{31}$, anaknya normal, sedangkan jika nomor indeks sama dengan atau di atas $2^{31}$, anaknya diperkeras.

Untuk membuat nomor indeks lebih mudah dibaca dan ditampilkan, nomor indeks untuk anak yang diperkeras ditampilkan mulai dari nol, tetapi dengan simbol prima (apostrof). Kunci anak normal pertama oleh karena itu ditampilkan sebagai `0`, sedangkan anak yang diperkeras pertama (indeks 0x80000000) ditampilkan sebagai `0'`. Secara berurutan, maka, kunci yang diperkeras kedua akan memiliki indeks 0x80000001 dan akan ditampilkan sebagai `1'`, dan seterusnya. Ketika Anda melihat indeks dompet HD `i'`, itu berarti $2^{31} + i$.

#### Pengidentifikasi kunci dompet HD (path)

Kunci dalam dompet HD diidentifikasi menggunakan konvensi penamaan “path”, dengan setiap tingkat pohon dipisahkan oleh karakter garis miring (`/`) (lihat Tabel 5-5). Kunci privat yang diturunkan dari kunci privat master dimulai dengan `m`. Kunci publik yang diturunkan dari kunci publik master dimulai dengan `M`. Oleh karena itu, kunci privat anak pertama dari kunci privat master adalah `m/0`. Kunci publik anak pertama adalah `M/0`. Cucu kedua dari anak pertama adalah `m/0/1`, dan seterusnya.

“Silsilah” sebuah kunci dibaca dari kanan ke kiri, hingga Anda mencapai kunci master dari mana ia diturunkan. Misalnya, pengidentifikasi `m/x/y/z` menjelaskan kunci yang merupakan anak ke-`z` dari kunci `m/x/y`, yang merupakan anak ke-`y` dari kunci `m/x`, yang merupakan anak ke-`x` dari `m`.

<p align="center">
  <img src="images/books-07-mastering_ethereum/tabel-5.5.png" alt="gambar" width="580"/>
</p>

#### Menavigasi struktur pohon dompet HD

Struktur pohon dompet HD sangat fleksibel. Sisi lain dari ini adalah bahwa ia juga memungkinkan kompleksitas tanpa batas: setiap kunci yang diperluas induk dapat memiliki 4 miliar anak: 2 miliar anak normal dan 2 miliar anak yang diperkeras. Masing-masing anak tersebut dapat memiliki 4 miliar anak lagi, dan seterusnya. Pohon bisa sedalam yang Anda inginkan, dengan jumlah generasi yang berpotensi tak terbatas. Dengan semua potensi itu, bisa menjadi cukup sulit untuk menavigasi pohon-pohon yang sangat besar ini.

Dua BIP menawarkan cara untuk mengelola kompleksitas potensial ini dengan menciptakan standar untuk struktur pohon dompet HD. **BIP-43** mengusulkan penggunaan indeks anak yang diperkeras pertama sebagai pengidentifikasi khusus yang menandakan “tujuan” (*purpose*) dari struktur pohon. Berdasarkan BIP-43, dompet HD harus menggunakan hanya satu cabang tingkat-1 dari pohon, dengan nomor indeks mendefinisikan tujuan dompet dengan mengidentifikasi struktur dan ruang nama dari sisa pohon. Lebih spesifik, dompet HD yang hanya menggunakan cabang `m/i'/…` dimaksudkan untuk menandakan tujuan tertentu dan tujuan itu diidentifikasi oleh nomor indeks `i`.

Memperluas spesifikasi itu, **BIP-44** mengusulkan struktur multikurensi dan multiakun yang ditandai dengan menetapkan nomor “tujuan” ke `44'`. Semua dompet HD yang mengikuti struktur BIP-44 diidentifikasi oleh fakta bahwa mereka hanya menggunakan satu cabang pohon: `m/44'/*`.

BIP-44 menetapkan struktur sebagai terdiri dari lima tingkat pohon yang telah ditentukan sebelumnya:
`m / purpose' / coin_type' / account' / change / address_index`

  * Tingkat pertama, **purpose'**, selalu diatur ke `44'`.
  * Tingkat kedua, **coin\_type'**, menentukan jenis koin mata uang kripto, memungkinkan dompet HD multikurensi di mana setiap mata uang memiliki sub-pohonnya sendiri di bawah tingkat kedua. Ada beberapa mata uang yang didefinisikan dalam dokumen standar yang disebut SLIP0044; misalnya, Ethereum adalah `m/44'/60'`, Ethereum Classic adalah `m/44'/61'`, Bitcoin adalah `m/44'/0'`, dan Testnet untuk semua mata uang adalah `m/44'/1'`.
  * Tingkat ketiga dari pohon adalah **account'**, yang memungkinkan pengguna untuk membagi dompet mereka menjadi sub-akun logis terpisah untuk tujuan akuntansi atau organisasi. Misalnya, dompet HD mungkin berisi dua “akun” Ethereum: `m/44'/60'/0'` dan `m/44'/60'/1'`. Setiap akun adalah akar dari sub-pohonnya sendiri.
  * Karena BIP-44 awalnya dibuat untuk Bitcoin, ia berisi “keanehan” yang tidak relevan di dunia Ethereum. Pada tingkat keempat dari path, **change**, dompet HD memiliki dua sub-pohon: satu untuk membuat alamat penerima dan satu untuk membuat alamat kembalian. Hanya path “terima” yang digunakan di Ethereum, karena tidak ada keharusan untuk alamat kembalian seperti yang ada di Bitcoin. Perhatikan bahwa sementara tingkat sebelumnya menggunakan derivasi yang diperkeras, tingkat ini menggunakan derivasi normal. Ini untuk memungkinkan tingkat akun dari pohon mengekspor kunci publik yang diperluas untuk digunakan di lingkungan yang tidak aman.
  * Alamat yang dapat digunakan diturunkan oleh dompet HD sebagai anak-anak dari tingkat keempat, menjadikan tingkat kelima dari pohon sebagai **address\_index**. Misalnya, alamat penerima ketiga untuk pembayaran Ethereum di akun utama akan menjadi `M/44'/60'/0'/0/2`.

Tabel 5-6 menunjukkan beberapa contoh lagi.

<p align="center">
  <img src="images/books-07-mastering_ethereum/tabel-5.6.png" alt="gambar" width="580"/>
</p>

### Kesimpulan

Dompet adalah fondasi dari setiap aplikasi blockchain yang menghadap pengguna. Mereka memungkinkan pengguna untuk mengelola koleksi kunci dan alamat. Dompet juga memungkinkan pengguna untuk menunjukkan kepemilikan mereka atas ether, dan mengotorisasi transaksi, dengan menerapkan tanda tangan digital, seperti yang akan kita lihat di Bab 6.

---

# BAB 6
## Transaksi

**Transaksi** adalah pesan yang ditandatangani yang berasal dari akun milik eksternal (*externally owned account* - EOA), ditransmisikan oleh jaringan Ethereum, dan dicatat di blockchain Ethereum. Definisi dasar ini menyembunyikan banyak detail yang mengejutkan dan menarik. Cara lain untuk melihat transaksi adalah sebagai satu-satunya hal yang dapat memicu perubahan keadaan (*state*), atau menyebabkan sebuah kontrak dieksekusi di EVM. Ethereum adalah mesin keadaan tunggal (*singleton state machine*) global, dan transaksi adalah apa yang membuat mesin keadaan itu "berdetak," mengubah keadaannya.

Kontrak tidak berjalan sendiri. Ethereum tidak berjalan secara otonom. Semuanya dimulai dengan sebuah transaksi.

Dalam bab ini, kita akan membedah transaksi, menunjukkan cara kerjanya, dan memeriksa detailnya. Perhatikan bahwa sebagian besar bab ini ditujukan bagi mereka yang tertarik mengelola transaksi mereka sendiri pada tingkat rendah, mungkin karena mereka sedang menulis aplikasi dompet; Anda tidak perlu khawatir tentang ini jika Anda senang menggunakan aplikasi dompet yang ada, meskipun Anda mungkin menemukan detailnya menarik\!

### Struktur Transaksi

Pertama, mari kita lihat struktur dasar sebuah transaksi, sebagaimana ia diserialisasi dan ditransmisikan di jaringan Ethereum. Setiap klien dan aplikasi yang menerima transaksi yang diserialisasi akan menyimpannya di dalam memori menggunakan struktur data internalnya sendiri, mungkin dihiasi dengan metadata yang tidak ada dalam transaksi yang diserialisasi di jaringan itu sendiri. Serialisasi jaringan adalah satu-satunya bentuk standar dari sebuah transaksi.

Transaksi adalah pesan biner yang diserialisasi yang berisi data berikut:

  * **Nonce**
    Nomor urut, yang dikeluarkan oleh EOA asal, digunakan untuk mencegah pemutaran ulang pesan (*message replay*).
  * **Harga gas (Gas price)**
    Harga gas (dalam wei) yang bersedia dibayar oleh pengirim.
  * **Batas gas (Gas limit)**
    Jumlah maksimum gas yang bersedia dibeli oleh pengirim untuk transaksi ini.
  * **Penerima (Recipient)**
    Alamat tujuan Ethereum.
  * **Nilai (Value)**
    Jumlah ether yang akan dikirim ke tujuan.
  * **Data**
    Muatan data biner (*binary data payload*) dengan panjang variabel.
  * **v,r,s**
    Tiga komponen dari tanda tangan digital ECDSA dari EOA asal.

Struktur pesan transaksi diserialisasi menggunakan skema pengkodean **Recursive Length Prefix (RLP)**, yang dibuat khusus untuk serialisasi data yang sederhana dan sempurna-per-byte (*byte-perfect*) di Ethereum. Semua angka di Ethereum dikodekan sebagai integer *big-endian*, dengan panjang yang merupakan kelipatan 8 bit.

Perhatikan bahwa label bidang (*to, gas limit*, dll.) ditampilkan di sini untuk kejelasan, tetapi bukan bagian dari data transaksi yang diserialisasi, yang berisi nilai-nilai bidang yang dikodekan dengan RLP. Secara umum, RLP tidak mengandung pembatas bidang atau label apa pun. Awalan panjang RLP digunakan untuk mengidentifikasi panjang setiap bidang. Apa pun di luar panjang yang ditentukan menjadi milik bidang berikutnya dalam struktur.

Meskipun ini adalah struktur transaksi aktual yang ditransmisikan, sebagian besar representasi internal dan visualisasi antarmuka pengguna memperindahnya dengan informasi tambahan, yang berasal dari transaksi atau dari blockchain.

Misalnya, Anda mungkin memperhatikan tidak ada data "from" di alamat yang mengidentifikasi EOA asal. Itu karena kunci publik EOA dapat diturunkan dari komponen `v,r,s` dari tanda tangan ECDSA. Alamat, pada gilirannya, dapat diturunkan dari kunci publik. Ketika Anda melihat transaksi yang menunjukkan bidang "from", itu ditambahkan oleh perangkat lunak yang digunakan untuk memvisualisasikan transaksi tersebut. Metadata lain yang sering ditambahkan ke transaksi oleh perangkat lunak klien termasuk nomor blok (setelah ditambang dan dimasukkan ke dalam blockchain) dan ID transaksi (hash yang dihitung). Sekali lagi, data ini berasal dari transaksi, dan bukan merupakan bagian dari pesan transaksi itu sendiri.

### Nonce Transaksi

Nonce adalah salah satu komponen transaksi yang paling penting dan paling sedikit dipahami. Definisi dalam *Yellow Paper* (lihat “Bacaan Lebih Lanjut”) berbunyi:

> **nonce**: Nilai skalar yang sama dengan jumlah transaksi yang dikirim dari alamat ini atau, dalam kasus akun dengan kode terkait, jumlah pembuatan kontrak yang dibuat oleh akun ini.

Secara tegas, nonce adalah atribut dari alamat asal; artinya, ia hanya memiliki makna dalam konteks alamat pengirim. Namun, nonce tidak disimpan secara eksplisit sebagai bagian dari keadaan akun di blockchain. Sebaliknya, ia dihitung secara dinamis, dengan menghitung jumlah transaksi terkonfirmasi yang berasal dari suatu alamat.

Ada dua skenario di mana keberadaan nonce penghitung transaksi menjadi penting: fitur kegunaan dari transaksi yang dimasukkan dalam urutan pembuatan, dan fitur vital perlindungan duplikasi transaksi. Mari kita lihat skenario contoh untuk masing-masing skenario ini:

1.  Bayangkan Anda ingin melakukan dua transaksi. Anda memiliki pembayaran penting sebesar 6 ether, dan juga pembayaran lain sebesar 8 ether. Anda menandatangani dan menyiarkan transaksi 6-ether terlebih dahulu, karena itu yang lebih penting, lalu Anda menandatangani dan menyiarkan transaksi kedua, 8-ether. Sayangnya, Anda mengabaikan fakta bahwa akun Anda hanya berisi 10 ether, jadi jaringan tidak dapat menerima kedua transaksi: salah satunya akan gagal. Karena Anda mengirim yang lebih penting 6-ether terlebih dahulu, Anda tentu berharap yang itu akan berhasil dan yang 8-ether akan ditolak. Namun, dalam sistem terdesentralisasi seperti Ethereum, *node* dapat menerima transaksi dalam urutan apa pun; tidak ada jaminan bahwa *node* tertentu akan menerima satu transaksi sebelum yang lain. Dengan demikian, hampir pasti akan ada beberapa *node* yang menerima transaksi 6-ether terlebih dahulu dan yang lain menerima transaksi 8-ether terlebih dahulu. Tanpa nonce, akan acak mana yang diterima dan mana yang ditolak. Namun, dengan nonce disertakan, transaksi pertama yang Anda kirim akan memiliki nonce, katakanlah, 3, sedangkan transaksi 8-ether memiliki nilai nonce berikutnya (yaitu, 4). Jadi, transaksi itu akan diabaikan sampai transaksi dengan nonce dari 0 hingga 3 telah diproses, bahkan jika diterima lebih dulu. Fiuh\!

2.  Sekarang bayangkan Anda memiliki akun dengan 100 ether. Fantastis\! Anda menemukan seseorang secara daring yang akan menerima pembayaran dalam ether untuk *widget-mcguffin* yang sangat ingin Anda beli. Anda mengirim mereka 2 ether dan mereka mengirimi Anda *widget-mcguffin*. Bagus sekali. Untuk melakukan pembayaran 2-ether itu, Anda menandatangani transaksi yang mengirim 2 ether dari akun Anda ke akun mereka, lalu menyiarkannya ke jaringan Ethereum untuk diverifikasi dan dimasukkan ke dalam blockchain. Sekarang, tanpa nilai nonce dalam transaksi, transaksi kedua yang mengirim 2 ether ke alamat yang sama untuk kedua kalinya akan terlihat persis sama dengan transaksi pertama. Ini berarti bahwa siapa pun yang melihat transaksi Anda di jaringan Ethereum (yang berarti semua orang, termasuk penerima atau musuh Anda) dapat "memutar ulang" transaksi itu berulang kali sampai semua ether Anda habis hanya dengan menyalin dan menempel transaksi asli Anda dan mengirimkannya kembali ke jaringan. Namun, dengan nilai nonce yang disertakan dalam data transaksi, setiap transaksi menjadi unik, bahkan saat mengirim jumlah ether yang sama ke alamat penerima yang sama beberapa kali. Jadi, dengan memiliki nonce yang bertambah sebagai bagian dari transaksi, tidak mungkin bagi siapa pun untuk "menduplikasi" pembayaran yang telah Anda lakukan.

Singkatnya, penting untuk dicatat bahwa penggunaan nonce sebenarnya vital untuk protokol berbasis akun, berbeda dengan mekanisme “Unspent Transaction Output” (UTXO) dari protokol Bitcoin.

#### Melacak Nonce

Secara praktis, nonce adalah hitungan terkini dari jumlah transaksi yang telah dikonfirmasi (yaitu, *on-chain*) yang berasal dari sebuah akun. Untuk mengetahui berapa nonce saat ini, Anda dapat menanyakannya ke blockchain, misalnya melalui antarmuka web3.

Buka konsol JavaScript di browser dengan MetaMask berjalan, atau gunakan perintah `truffle console` untuk mengakses pustaka JavaScript web3, lalu ketik:

```javascript
> web3.eth.getTransactionCount("0x9e713963a92c02317a681b9bb3065a8249de124f")
40
```

> Nonce adalah penghitung berbasis nol, artinya transaksi pertama memiliki nonce 0. Dalam contoh ini, kita memiliki jumlah transaksi 40, yang berarti nonce 0 hingga 39 telah terlihat. Nonce transaksi berikutnya harus 40.

Dompet Anda akan melacak nonce untuk setiap alamat yang dikelolanya. Cukup sederhana untuk melakukannya, selama Anda hanya memulai transaksi dari satu titik. Katakanlah Anda sedang menulis perangkat lunak dompet Anda sendiri atau aplikasi lain yang memulai transaksi. Bagaimana Anda melacak nonce?

Saat Anda membuat transaksi baru, Anda menetapkan nonce berikutnya dalam urutan. Tetapi sampai transaksi itu dikonfirmasi, itu tidak akan dihitung dalam total `getTransactionCount`.

> Berhati-hatilah saat menggunakan fungsi `getTransactionCount` untuk menghitung transaksi yang tertunda (*pending*), karena Anda mungkin mengalami beberapa masalah jika Anda mengirim beberapa transaksi secara berurutan.

Mari kita lihat sebuah contoh:

```javascript
> web3.eth.getTransactionCount("0x9e713963a92c02317a681b9bb3065a8249de124f", "pending")
40
> web3.eth.sendTransaction({from: web3.eth.accounts[0], to: "0xB0920c523d582040f2BCB1bD7FB1c7C1ECEbdB34", value: web3.toWei(0.01, "ether")});
> web3.eth.getTransactionCount("0x9e713963a92c02317a681b9bb3065a8249de124f", "pending")
41
> web3.eth.sendTransaction({from: web3.eth.accounts[0], to: "0xB0920c523d582040f2BCB1bD7FB1c7C1ECEbdB34", value: web3.toWei(0.01, "ether")});
> web3.eth.getTransactionCount("0x9e713963a92c02317a681b9bb3065a8249de124f", "pending")
41
> web3.eth.sendTransaction({from: web3.eth.accounts[0], to: "0xB0920c523d582040f2BCB1bD7FB1c7C1ECEbdB34", value: web3.toWei(0.01, "ether")});
> web3.eth.getTransactionCount("0x9e713963a92c02317a681b9bb3065a8249de124f", "pending")
41
```

Seperti yang Anda lihat, transaksi pertama yang kami kirim meningkatkan jumlah transaksi menjadi 41, menunjukkan transaksi yang tertunda. Tetapi ketika kami mengirim tiga transaksi lagi secara berurutan, panggilan `getTransactionCount` tidak menghitungnya. Itu hanya menghitung satu, meskipun Anda mungkin berharap ada tiga yang tertunda di *mempool*. Jika kita menunggu beberapa detik agar komunikasi jaringan stabil, panggilan `getTransactionCount` akan mengembalikan angka yang diharapkan. Tetapi sementara itu, ketika ada lebih dari satu transaksi yang tertunda, itu mungkin tidak membantu kita.

Ketika Anda membangun aplikasi yang membuat transaksi, ia tidak dapat mengandalkan `getTransactionCount` untuk transaksi yang tertunda. Hanya ketika jumlah transaksi tertunda dan terkonfirmasi sama (semua transaksi yang beredar telah dikonfirmasi), Anda dapat mempercayai output `getTransactionCount` untuk memulai penghitung nonce Anda. Setelah itu, lacak nonce di aplikasi Anda sampai setiap transaksi dikonfirmasi.

Antarmuka JSON RPC Parity menawarkan fungsi `parity_nextNonce`, yang mengembalikan nonce berikutnya yang harus digunakan dalam sebuah transaksi. Fungsi `parity_nextNonce` menghitung nonce dengan benar, bahkan jika Anda membuat beberapa transaksi secara berurutan tanpa mengonfirmasinya:

```bash
$ curl --data '{"method":"parity_nextNonce", \
"params":["0x9e713963a92c02317a681b9bb3065a8249de124f"],\
"id":1,"jsonrpc":"2.0"}' -H "Content-Type: application/json" -X POST \
localhost:8545
{"jsonrpc":"2.0","result":"0x32","id":1}
```

> Parity memiliki konsol web untuk mengakses antarmuka JSON RPC, tetapi di sini kami menggunakan klien HTTP baris perintah untuk mengaksesnya.

#### Kesenjangan Nonce, Nonce Duplikat, dan Konfirmasi

Penting untuk melacak nonce jika Anda membuat transaksi secara terprogram, terutama jika Anda melakukannya dari beberapa proses independen secara bersamaan.

Jaringan Ethereum memproses transaksi secara berurutan, berdasarkan nonce. Itu berarti jika Anda mengirimkan transaksi dengan nonce 0 dan kemudian mengirimkan transaksi dengan nonce 2, transaksi kedua tidak akan dimasukkan ke dalam blok mana pun. Ia akan disimpan di *mempool*, sementara jaringan Ethereum menunggu nonce yang hilang muncul. Semua *node* akan berasumsi bahwa nonce yang hilang hanya tertunda dan transaksi dengan nonce 2 diterima di luar urutan.

Jika Anda kemudian mengirimkan transaksi dengan nonce yang hilang yaitu 1, kedua transaksi (nonce 1 dan 2) akan diproses dan dimasukkan (jika valid, tentu saja). Setelah Anda mengisi celah tersebut, jaringan dapat menambang transaksi di luar urutan yang disimpannya di *mempool*.

Artinya, jika Anda membuat beberapa transaksi secara berurutan dan salah satunya tidak secara resmi dimasukkan ke dalam blok mana pun, semua transaksi berikutnya akan "terjebak", menunggu nonce yang hilang. Sebuah transaksi dapat menciptakan "celah" yang tidak disengaja dalam urutan nonce karena tidak valid atau memiliki gas yang tidak mencukupi. Untuk membuat semuanya bergerak lagi, Anda harus mengirimkan transaksi yang valid dengan nonce yang hilang. Anda juga harus ingat bahwa setelah transaksi dengan nonce yang "hilang" divalidasi oleh jaringan, semua transaksi yang disiarkan dengan nonce berikutnya akan secara bertahap menjadi valid; tidak mungkin untuk "menarik kembali" sebuah transaksi\!

Jika, di sisi lain, Anda secara tidak sengaja menduplikasi nonce, misalnya dengan mengirimkan dua transaksi dengan nonce yang sama tetapi penerima atau nilai yang berbeda, maka salah satunya akan dikonfirmasi dan salah satunya akan ditolak. Mana yang dikonfirmasi akan ditentukan oleh urutan kedatangan mereka di *node* validasi pertama yang menerimanya—yaitu, akan cukup acak.

Seperti yang Anda lihat, melacak nonce adalah perlu, dan jika aplikasi Anda tidak mengelola proses itu dengan benar, Anda akan mengalami masalah. Sayangnya, segalanya menjadi lebih sulit jika Anda mencoba melakukan ini secara bersamaan, seperti yang akan kita lihat di bagian berikutnya.

#### Konkurensi, Pembuatan Transaksi, dan Nonce

Konkurensi adalah aspek kompleks dalam ilmu komputer, dan terkadang muncul secara tak terduga, terutama dalam sistem waktu-nyata yang terdesentralisasi dan terdistribusi seperti Ethereum.

Secara sederhana, konkurensi adalah ketika Anda memiliki komputasi simultan oleh beberapa sistem independen. Ini bisa terjadi dalam program yang sama (mis., *multithreading*), pada CPU yang sama (mis., *multiprocessing*), atau di komputer yang berbeda (yaitu, sistem terdistribusi). Ethereum, menurut definisinya, adalah sistem yang memungkinkan konkurensi operasi (*node*, klien, DApps) tetapi memberlakukan keadaan tunggal melalui konsensus.

Sekarang, bayangkan Anda memiliki beberapa aplikasi dompet independen yang menghasilkan transaksi dari alamat atau alamat yang sama. Salah satu contoh situasi seperti itu adalah bursa yang memproses penarikan dari *hot wallet* bursa (dompet yang kuncinya disimpan secara daring, berbeda dengan *cold wallet* di mana kuncinya tidak pernah daring). Idealnya, Anda ingin memiliki lebih dari satu komputer yang memproses penarikan, sehingga tidak menjadi hambatan atau satu titik kegagalan. Namun, ini dengan cepat menjadi masalah, karena memiliki lebih dari satu komputer yang menghasilkan penarikan akan menghasilkan beberapa masalah konkurensi yang rumit, salah satunya adalah pemilihan nonce. Bagaimana beberapa komputer yang menghasilkan, menandatangani, dan menyiarkan transaksi dari akun *hot wallet* yang sama berkoordinasi?

Anda bisa menggunakan satu komputer untuk menetapkan nonce, berdasarkan *first-come first-served*, ke komputer yang menandatangani transaksi. Namun, komputer ini sekarang menjadi satu titik kegagalan. Lebih buruk lagi, jika beberapa nonce ditetapkan dan salah satunya tidak pernah digunakan (karena kegagalan di komputer yang memproses transaksi dengan nonce itu), semua transaksi berikutnya menjadi macet.

Pendekatan lain adalah dengan menghasilkan transaksi, tetapi tidak menetapkan nonce padanya (dan karena itu membiarkannya tidak ditandatangani—ingat bahwa nonce adalah bagian integral dari data transaksi dan oleh karena itu perlu dimasukkan dalam tanda tangan digital yang mengotentikasi transaksi). Anda kemudian bisa mengantrekannya ke satu *node* yang menandatanganinya dan juga melacak nonce. Sekali lagi, ini akan menjadi titik hambat dalam proses: penandatanganan dan pelacakan nonce adalah bagian dari operasi Anda yang kemungkinan akan menjadi padat di bawah beban, sedangkan pembuatan transaksi yang tidak ditandatangani adalah bagian yang tidak terlalu perlu Anda paralelisasi. Anda akan memiliki beberapa konkurensi, tetapi akan kurang di bagian kritis dari proses tersebut.

Pada akhirnya, masalah konkurensi ini, di atas kesulitan melacak saldo akun dan konfirmasi transaksi dalam proses independen, memaksa sebagian besar implementasi untuk menghindari konkurensi dan menciptakan hambatan seperti proses tunggal yang menangani semua transaksi penarikan di bursa, atau menyiapkan beberapa *hot wallet* yang dapat bekerja sepenuhnya secara independen untuk penarikan dan hanya perlu diseimbangkan kembali secara berkala.

### Gas Transaksi

Kami telah membahas sedikit tentang gas di bab-bab sebelumnya, dan kami akan membahasnya lebih detail di “Gas” di halaman 314. Namun, mari kita bahas beberapa dasar tentang peran komponen `gasPrice` dan `gasLimit` dari sebuah transaksi.

Gas adalah bahan bakar Ethereum. Gas bukan ether—ini adalah mata uang virtual terpisah dengan nilai tukarnya sendiri terhadap ether. Ethereum menggunakan gas untuk mengontrol jumlah sumber daya yang dapat digunakan oleh sebuah transaksi, karena akan diproses di ribuan komputer di seluruh dunia. Model komputasi yang terbuka (*Turing-complete*) memerlukan beberapa bentuk pengukuran untuk menghindari serangan *denial-of-service* atau transaksi yang secara tidak sengaja menghabiskan sumber daya.

Gas terpisah dari ether untuk melindungi sistem dari volatilitas yang mungkin timbul seiring dengan perubahan cepat nilai ether, dan juga sebagai cara untuk mengelola rasio penting dan sensitif antara biaya berbagai sumber daya yang dibayar oleh gas (yaitu, komputasi, memori, dan penyimpanan).

Bidang `gasPrice` dalam sebuah transaksi memungkinkan pengirim transaksi untuk menetapkan harga yang bersedia mereka bayar sebagai ganti gas. Harga diukur dalam wei per unit gas. Misalnya, dalam contoh transaksi di Bab 2, dompet Anda menetapkan `gasPrice` menjadi 3 gwei (3 gigawei atau 3 miliar wei).

> Situs populer **ETH Gas Station** menyediakan informasi tentang harga gas saat ini dan metrik gas relevan lainnya untuk jaringan utama Ethereum.

Dompet dapat menyesuaikan `gasPrice` dalam transaksi yang mereka mulai untuk mencapai konfirmasi transaksi yang lebih cepat. Semakin tinggi `gasPrice`, semakin cepat transaksi kemungkinan akan dikonfirmasi. Sebaliknya, transaksi dengan prioritas lebih rendah dapat membawa harga yang lebih rendah, menghasilkan konfirmasi yang lebih lambat. Nilai minimum yang dapat diatur untuk `gasPrice` adalah nol, yang berarti transaksi bebas biaya. Selama periode permintaan ruang di blok rendah, transaksi semacam itu mungkin saja akan ditambang.

> `gasPrice` minimum yang dapat diterima adalah nol. Itu berarti dompet dapat menghasilkan transaksi yang sepenuhnya gratis. Tergantung pada kapasitas, ini mungkin tidak pernah dikonfirmasi, tetapi tidak ada dalam protokol yang melarang transaksi gratis. Anda dapat menemukan beberapa contoh transaksi semacam itu yang berhasil dimasukkan ke dalam blockchain Ethereum.

Antarmuka web3 menawarkan saran `gasPrice`, dengan menghitung harga median di beberapa blok (kita bisa menggunakan konsol truffle atau konsol web3 JavaScript mana pun untuk melakukannya):

```javascript
> web3.eth.getGasPrice(console.log)
> null BigNumber { s: 1, e: 10, c: [ 10000000000 ] }
```

Bidang penting kedua yang terkait dengan gas adalah `gasLimit`. Secara sederhana, `gasLimit` memberikan jumlah maksimum unit gas yang bersedia dibeli oleh pengirim transaksi untuk menyelesaikan transaksi tersebut. Untuk pembayaran sederhana, yaitu transaksi yang mentransfer ether dari satu EOA ke EOA lain, jumlah gas yang dibutuhkan ditetapkan sebesar **21.000 unit gas**. Untuk menghitung berapa biaya ether yang akan dikeluarkan, Anda mengalikan 21.000 dengan `gasPrice` yang bersedia Anda bayar. Contohnya:

```javascript
> web3.eth.getGasPrice(function(err, res) {console.log(res*21000)} )
> 210000000000000
```

Jika alamat tujuan transaksi Anda adalah sebuah kontrak, maka jumlah gas yang dibutuhkan dapat diperkirakan tetapi tidak dapat ditentukan dengan akurat. Itu karena sebuah kontrak dapat mengevaluasi kondisi yang berbeda yang mengarah ke jalur eksekusi yang berbeda, dengan total biaya gas yang berbeda. Kontrak mungkin hanya mengeksekusi komputasi sederhana atau yang lebih kompleks, tergantung pada kondisi yang berada di luar kendali Anda dan tidak dapat diprediksi. Untuk mendemonstrasikan ini, mari kita lihat sebuah contoh: kita bisa menulis kontrak pintar yang menaikkan penghitung setiap kali dipanggil dan menjalankan *loop* tertentu sejumlah kali sama dengan jumlah panggilan. Mungkin pada panggilan ke-100 ia memberikan hadiah khusus, seperti lotre, tetapi perlu melakukan komputasi tambahan untuk menghitung hadiah. Jika Anda memanggil kontrak 99 kali, satu hal terjadi, tetapi pada panggilan ke-100, sesuatu yang sangat berbeda terjadi. Jumlah gas yang akan Anda bayar tergantung pada berapa banyak transaksi lain yang telah memanggil fungsi itu sebelum transaksi Anda dimasukkan ke dalam blok. Mungkin perkiraan Anda didasarkan pada menjadi transaksi ke-99, tetapi tepat sebelum transaksi Anda dikonfirmasi, orang lain memanggil kontrak untuk ke-99 kalinya. Sekarang Anda adalah transaksi ke-100 yang memanggil, dan upaya komputasi (dan biaya gas) jauh lebih tinggi.

Meminjam analogi umum yang digunakan di Ethereum, Anda dapat menganggap `gasLimit` sebagai kapasitas tangki bahan bakar di mobil Anda (mobil Anda adalah transaksi). Anda mengisi tangki dengan bahan bakar sebanyak yang Anda pikir akan dibutuhkan untuk perjalanan (komputasi yang diperlukan untuk memvalidasi transaksi Anda). Anda dapat memperkirakan jumlahnya sampai batas tertentu, tetapi mungkin ada perubahan tak terduga pada perjalanan Anda, seperti pengalihan (jalur eksekusi yang lebih kompleks), yang meningkatkan konsumsi bahan bakar.

Namun, analogi dengan tangki bahan bakar agak menyesatkan. Sebenarnya lebih seperti akun kredit untuk perusahaan pom bensin, di mana Anda membayar setelah perjalanan selesai, berdasarkan berapa banyak gas yang sebenarnya Anda gunakan. Saat Anda mengirimkan transaksi Anda, salah satu langkah validasi pertama adalah memeriksa bahwa akun asalnya memiliki cukup ether untuk membayar biaya `gasPrice * gasLimit`. Tetapi jumlahnya tidak benar-benar dikurangi dari akun Anda sampai transaksi selesai dieksekusi. Anda hanya ditagih untuk gas yang benar-benar dikonsumsi oleh transaksi Anda, tetapi Anda harus memiliki saldo yang cukup untuk jumlah maksimum yang bersedia Anda bayar sebelum Anda mengirim transaksi Anda.

### Penerima Transaksi

Penerima transaksi ditentukan dalam bidang `to`. Bidang ini berisi alamat Ethereum 20-byte. Alamat tersebut bisa berupa EOA atau alamat kontrak.

Ethereum tidak melakukan validasi lebih lanjut pada bidang ini. Nilai 20-byte apa pun dianggap valid. Jika nilai 20-byte sesuai dengan alamat tanpa kunci privat yang sesuai, atau tanpa kontrak yang sesuai, transaksi tersebut tetap valid. Ethereum tidak memiliki cara untuk mengetahui apakah sebuah alamat diturunkan dengan benar dari kunci publik (dan karena itu dari kunci privat) yang ada.

> Protokol Ethereum tidak memvalidasi alamat penerima dalam transaksi. Anda dapat mengirim ke alamat yang tidak memiliki kunci privat atau kontrak yang sesuai, dengan demikian "membakar" (*burning*) ether tersebut, membuatnya tidak dapat dibelanjakan selamanya. Validasi harus dilakukan di tingkat antarmuka pengguna.

Mengirim transaksi ke alamat yang salah kemungkinan besar akan membakar ether yang dikirim, membuatnya tidak dapat diakses selamanya (tidak dapat dibelanjakan), karena sebagian besar alamat tidak memiliki kunci privat yang diketahui dan oleh karena itu tidak ada tanda tangan yang dapat dihasilkan untuk membelanjakannya. Diasumsikan bahwa validasi alamat terjadi di tingkat antarmuka pengguna (lihat “Pengkodean Hex dengan Checksum dalam Kapitalisasi (EIP-55)” di halaman 76). Faktanya, ada sejumlah alasan yang valid untuk membakar ether—misalnya, sebagai disinsentif untuk berbuat curang di *payment channel* dan kontrak pintar lainnya—dan karena jumlah ether terbatas, membakar ether secara efektif mendistribusikan nilai yang dibakar ke semua pemegang ether (sebanding dengan jumlah ether yang mereka pegang).

### Nilai dan Data Transaksi

"Muatan" utama dari sebuah transaksi terkandung dalam dua bidang: `value` (nilai) dan `data`. Transaksi dapat memiliki keduanya, hanya nilai, hanya data, atau tidak keduanya. Keempat kombinasi tersebut valid.

Sebuah transaksi yang hanya memiliki **nilai** adalah **pembayaran**. Sebuah transaksi yang hanya memiliki **data** adalah **pemanggilan (invocation)**. Sebuah transaksi yang memiliki **keduanya** adalah **pembayaran sekaligus pemanggilan**. Sebuah transaksi yang tidak memiliki **keduanya**—yah itu mungkin hanya pemborosan gas\! Tetapi itu tetap mungkin dilakukan.

Mari kita coba semua kombinasi ini. Pertama, kita akan mengatur alamat sumber dan tujuan dari dompet kita, agar demo lebih mudah dibaca:

```javascript
src = web3.eth.accounts[0];
dst = web3.eth.accounts[1];
```

Transaksi pertama kita hanya berisi nilai (pembayaran), dan tidak ada muatan data:

```javascript
web3.eth.sendTransaction({from: src, to: dst, value: web3.toWei(0.01, "ether"), data: ""});
```

Dompet kita menampilkan layar konfirmasi yang menunjukkan nilai yang akan dikirim, seperti yang ditunjukkan pada Gambar 6-1.

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-6.1.png" alt="gambar" width="580"/>
</p>

Contoh berikutnya menentukan baik nilai maupun muatan data:

```javascript
web3.eth.sendTransaction({from: src, to: dst, value: web.toWei(0.01, "ether"), data: "0x1234"});
```

Dompet kita menampilkan layar konfirmasi yang menunjukkan nilai yang akan dikirim serta muatan datanya, seperti yang ditunjukkan pada Gambar 6-2.

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-6.2.png" alt="gambar" width="580"/>
</p>

Transaksi berikutnya menyertakan muatan data tetapi menentukan nilai nol:

```javascript
web3.eth.sendTransaction({from: src, to: dst, value: 0, data: "0x1234"});
```

Dompet kita menampilkan layar konfirmasi yang menunjukkan nilai nol dan muatan data, seperti yang ditunjukkan pada Gambar 6-3.

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-6.3.png" alt="gambar" width="580"/>
</p>

Terakhir, transaksi terakhir tidak menyertakan nilai untuk dikirim maupun muatan data:

```javascript
web3.eth.sendTransaction({from: src, to: dst, value: 0, data: ""});
```

Dompet kita menampilkan layar konfirmasi yang menunjukkan nilai nol, seperti yang ditunjukkan pada Gambar 6-4.

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-6.4.png" alt="gambar" width="580"/>
</p>

### Mengirim Nilai ke EOA dan Kontrak

Ketika Anda membuat transaksi Ethereum yang berisi nilai (*value*), itu setara dengan sebuah pembayaran. Transaksi semacam itu berperilaku berbeda tergantung pada apakah alamat tujuannya adalah sebuah kontrak atau bukan.

Untuk alamat **EOA**, atau lebih tepatnya untuk alamat mana pun yang tidak ditandai sebagai kontrak di blockchain, Ethereum akan mencatat perubahan keadaan (*state change*), menambahkan nilai yang Anda kirim ke saldo alamat tersebut. Jika alamat tersebut belum pernah terlihat sebelumnya, ia akan ditambahkan ke representasi internal klien dari keadaan dan saldonya akan diinisialisasi dengan nilai pembayaran Anda.

Jika alamat tujuan (`to`) adalah sebuah **kontrak**, maka EVM akan mengeksekusi kontrak tersebut dan akan mencoba memanggil fungsi yang disebutkan dalam muatan data (*data payload*) transaksi Anda. Jika tidak ada data dalam transaksi Anda, EVM akan memanggil **fungsi fallback** dan, jika fungsi tersebut bersifat **payable**, akan mengeksekusinya untuk menentukan apa yang harus dilakukan selanjutnya. Jika tidak ada fungsi fallback, maka efek dari transaksi tersebut adalah meningkatkan saldo kontrak, persis seperti pembayaran ke sebuah dompet.

Sebuah kontrak dapat menolak pembayaran yang masuk dengan melemparkan pengecualian (*throwing an exception*) segera setelah sebuah fungsi dipanggil, atau sebagaimana ditentukan oleh kondisi yang dikodekan dalam sebuah fungsi. Jika fungsi berakhir dengan sukses (tanpa pengecualian), maka keadaan kontrak diperbarui untuk mencerminkan peningkatan saldo ether kontrak.

### Mengirim Muatan Data ke EOA atau Kontrak

Ketika transaksi Anda berisi data, kemungkinan besar transaksi itu ditujukan ke alamat kontrak. Itu tidak berarti Anda tidak dapat mengirim muatan data ke EOA—itu sepenuhnya valid dalam protokol Ethereum. Namun, dalam kasus itu, interpretasi data terserah pada dompet yang Anda gunakan untuk mengakses EOA tersebut. Hal ini **diabaikan oleh protokol Ethereum**. Sebagian besar dompet juga mengabaikan data apa pun yang diterima dalam transaksi ke EOA yang mereka kontrol. Di masa depan, mungkin saja standar akan muncul yang memungkinkan dompet untuk menginterpretasikan data seperti yang dilakukan kontrak, sehingga memungkinkan transaksi untuk memanggil fungsi yang berjalan di dalam dompet pengguna. Perbedaan kritisnya adalah bahwa setiap interpretasi muatan data oleh EOA **tidak tunduk pada aturan konsensus Ethereum**, tidak seperti eksekusi kontrak.

Untuk saat ini, mari kita asumsikan transaksi Anda mengirimkan data ke alamat kontrak. Dalam kasus itu, data akan diinterpretasikan oleh EVM sebagai pemanggilan kontrak (*contract invocation*). Sebagian besar kontrak menggunakan data ini secara lebih spesifik sebagai **pemanggilan fungsi (*function invocation*)**, memanggil fungsi yang disebutkan dan meneruskan argumen yang dikodekan ke fungsi tersebut.

Muatan data yang dikirim ke kontrak yang kompatibel dengan ABI (yang dapat Anda asumsikan dimiliki oleh semua kontrak) adalah pengkodean heksadesimal dari:

  * **Selektor fungsi (*Function selector*)**
    4 byte pertama dari hash Keccak-256 dari prototipe fungsi. Ini memungkinkan kontrak untuk secara tidak ambigu mengidentifikasi fungsi mana yang ingin Anda panggil.
  * **Argumen fungsi (*The function arguments*)**
    Argumen fungsi, yang dikodekan sesuai dengan aturan untuk berbagai tipe dasar yang didefinisikan dalam spesifikasi ABI.

Dalam Contoh 2-1, kami mendefinisikan sebuah fungsi untuk penarikan:

```solidity
function withdraw(uint withdraw_amount) public {
```

**Prototipe** sebuah fungsi didefinisikan sebagai string yang berisi nama fungsi, diikuti oleh tipe data dari setiap argumennya, diapit dalam tanda kurung dan dipisahkan oleh koma. Nama fungsinya di sini adalah `withdraw` dan ia mengambil satu argumen yaitu `uint` (yang merupakan alias untuk `uint256`), jadi prototipe dari `withdraw` adalah:
`withdraw(uint256)`

Mari kita hitung hash Keccak-256 dari string ini:

```javascript
> web3.sha3("withdraw(uint256)");
'0x2e1a7d4d13322e7b96f9a57413e1525c250fb7a9021cf91d1540d5b69f16a49f'
```

**4 byte pertama** dari hash adalah `0x2e1a7d4d`. Itulah nilai "selektor fungsi" kita, yang akan memberi tahu kontrak fungsi mana yang ingin kita panggil.

Selanjutnya, mari kita hitung nilai untuk diteruskan sebagai argumen `withdraw_amount`. Kita ingin menarik 0,01 ether. Mari kita kodekan itu menjadi integer 256-bit tak bertanda *big-endian* yang diserialisasi dalam heksadesimal, dalam denominasi wei:

```javascript
> withdraw_amount = web3.toWei(0.01, "ether");
'10000000000000000'
> withdraw_amount_hex = web3.toHex(withdraw_amount);
'0x2386f26fc10000'
```

Sekarang, kita tambahkan selektor fungsi ke jumlah tersebut (di-padding hingga 32 byte):
`2e1a7d4d000000000000000000000000000000000000000000000000002386f26fc10000`

Itulah muatan data untuk transaksi kita, memanggil fungsi `withdraw` dan meminta 0,01 ether sebagai `withdraw_amount`.

### Transaksi Khusus: Pembuatan Kontrak

Satu kasus khusus yang harus kita sebutkan adalah transaksi yang membuat kontrak baru di blockchain, menyebarkannya untuk penggunaan di masa depan. Transaksi pembuatan kontrak dikirim ke alamat tujuan khusus yang disebut **alamat nol (*zero address*)**; bidang `to` dalam transaksi pendaftaran kontrak berisi alamat `0x0`. Alamat ini tidak mewakili EOA (tidak ada pasangan kunci privat-publik yang sesuai) maupun kontrak. Alamat ini tidak akan pernah bisa membelanjakan ether atau memulai transaksi. Ia hanya digunakan sebagai tujuan, dengan makna khusus "buat kontrak ini."

Meskipun alamat nol hanya ditujukan untuk pembuatan kontrak, terkadang ia menerima pembayaran dari berbagai alamat. Ada dua penjelasan untuk ini: entah karena kecelakaan, yang mengakibatkan hilangnya ether, atau itu adalah **pembakaran ether (*ether burn*)** yang disengaja (sengaja menghancurkan ether dengan mengirimkannya ke alamat dari mana ia tidak akan pernah bisa dibelanjakan). Namun, jika Anda ingin melakukan pembakaran ether yang disengaja, Anda harus menjelaskan niat Anda ke jaringan dan menggunakan alamat bakar yang ditunjuk secara khusus:
`0x000000000000000000000000000000000000dEaD`

> Ether apa pun yang dikirim ke alamat bakar yang ditunjuk akan menjadi tidak dapat dibelanjakan dan hilang selamanya.

Transaksi pembuatan kontrak hanya perlu berisi muatan data yang berisi *bytecode* terkompilasi yang akan membuat kontrak. Satu-satunya efek dari transaksi ini adalah untuk membuat kontrak. Anda dapat menyertakan jumlah ether di bidang `value` jika Anda ingin mengatur kontrak baru dengan saldo awal, tetapi itu sepenuhnya opsional. Jika Anda mengirim nilai (ether) ke alamat pembuatan kontrak tanpa muatan data (tanpa kontrak), maka efeknya sama dengan mengirim ke alamat bakar—tidak ada kontrak untuk dikreditkan, jadi ether tersebut hilang.

Sebagai contoh, kita dapat membuat kontrak `Faucet.sol` yang digunakan di Bab 2 dengan secara manual membuat transaksi ke alamat nol dengan kontrak di muatan data. Kontrak perlu dikompilasi menjadi representasi *bytecode*. Ini dapat dilakukan dengan kompiler Solidity:

```bash
$ solc --bin Faucet.sol

Binary:
6060604052341561000f57600080fd5b60e58061001d6000396000f30060606040526004361060...
```

Informasi yang sama juga dapat diperoleh dari kompiler daring Remix.

Sekarang kita dapat membuat transaksinya:

```javascript
> src = web3.eth.accounts[0];
> faucet_code = "0x6060604052341561000f57600080fd5b60e58061001d6000396000f300606...f0029";
> web3.eth.sendTransaction({from: src, to: 0, data: faucet_code, gas: 113558, gasPrice: 200000000000});
"0x7bcc327ae5d369f75b98c0d59037eec41d44dfae75447fd753d9f2db9439124b"
```

Merupakan praktik yang baik untuk selalu menentukan parameter `to`, bahkan dalam kasus pembuatan kontrak alamat-nol, karena biaya kehilangan ether Anda selamanya karena tidak sengaja mengirimkannya ke `0x0` terlalu besar. Anda juga harus menentukan `gasPrice` dan `gasLimit`.

Setelah kontrak ditambang, kita dapat melihatnya di penjelajah blok Etherscan, seperti yang ditunjukkan pada Gambar 6-5.

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-6.5.png" alt="gambar" width="580"/>
</p>

Kita dapat melihat **resi (*receipt*)** dari transaksi untuk mendapatkan informasi tentang kontrak:

```javascript
> eth.getTransactionReceipt("0x7bcc327ae5d369f75b98c0d59037eec41d44dfae75447fd753d9f2db9439124b");

{
  blockHash: "0x6fa7d8bf982490de6246875deb2c21e5f3665b4422089c060138fc3907a95bb2",
  blockNumber: 3105256,
  contractAddress: "0xb226270965b43373e98ffc6e2c7693c17e2cf40b",
  cumulativeGasUsed: 113558,
  from: "0x2a966a87db5913c1b22a59b0d8a11cc51c167a89",
  gasUsed: 113558,
  logs: [],
  logsBloom: "0x00000000000000000000000000000000000000000000000000...00000",
  status: "0x1",
  to: null,
  transactionHash: "0x7bcc327ae5d369f75b98c0d59037eec41d44dfae75447fd753d9f2db9439124b",
  transactionIndex: 0
}
```

Resi ini mencakup alamat kontrak, yang dapat kita gunakan untuk mengirim dana ke dan menerima dana dari kontrak seperti yang ditunjukkan di bagian sebelumnya:

```javascript
> contract_address = "0xb226270965b43373e98ffc6e2c7693c17e2cf40b"

> web3.eth.sendTransaction({from: src, to: contract_address, value: web3.toWei(0.1, "ether"), data: ""});
"0x6ebf2e1fe95cc9c1fe2e1a0dc45678ccd127d374fdf145c5c8e6cd4ea2e6ca9f"

> web3.eth.sendTransaction({from: src, to: contract_address, value: 0, data: "0x2e1a7d4d000000000000000000000000000000000000000000000000002386f26fc10000"});
"0x59836029e7ce43e92daf84313816ca31420a76a9a571b69e31ec4bf4b37cd16e"
```

Setelah beberapa saat, kedua transaksi tersebut terlihat di Etherscan, seperti yang ditunjukkan pada Gambar 6-6.

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-6.6.png" alt="gambar" width="580"/>
</p>

### Tanda Tangan Digital

Sejauh ini, kita belum mendalami detail apa pun tentang tanda tangan digital. Di bagian ini, kita akan melihat cara kerja tanda tangan digital dan bagaimana tanda tangan tersebut dapat digunakan untuk menyajikan bukti kepemilikan kunci privat tanpa mengungkapkan kunci privat tersebut.

#### Algoritma Tanda Tangan Digital Kurva Eliptik (Elliptic Curve Digital Signature Algorithm)

Algoritma tanda tangan digital yang digunakan di Ethereum adalah **Elliptic Curve Digital Signature Algorithm (ECDSA)**. Algoritma ini didasarkan pada pasangan kunci privat-publik kurva eliptik, seperti yang dijelaskan dalam “Penjelasan Kriptografi Kurva Eliptik” di halaman 65.

Tanda tangan digital melayani tiga tujuan di Ethereum (lihat *sidebar* berikut). Pertama, tanda tangan membuktikan bahwa pemilik kunci privat, yang secara implisit adalah pemilik akun Ethereum, telah **mengizinkan** pembelanjaan ether, atau eksekusi sebuah kontrak. Kedua, ia menjamin **non-repudiasi**: bukti otorisasi tidak dapat disangkal. Ketiga, tanda tangan membuktikan bahwa data transaksi **tidak telah dan tidak dapat diubah** oleh siapa pun setelah transaksi ditandatangani.

> #### Definisi Tanda Tangan Digital dari Wikipedia
>
> Tanda tangan digital adalah skema matematis untuk menyajikan keaslian pesan atau dokumen digital. Tanda tangan digital yang valid memberi penerima alasan untuk percaya bahwa pesan tersebut dibuat oleh pengirim yang dikenal (**autentikasi**), bahwa pengirim tidak dapat menyangkal telah mengirim pesan tersebut (**non-repudiasi**), dan bahwa pesan tersebut tidak diubah dalam perjalanan (**integritas**).
>
> Sumber: [https://en.wikipedia.org/wiki/Digital\_signature](https://en.wikipedia.org/wiki/Digital_signature)

#### Cara Kerja Tanda Tangan Digital

Tanda tangan digital adalah skema matematis yang terdiri dari dua bagian. Bagian pertama adalah algoritma untuk **membuat tanda tangan**, menggunakan kunci privat (kunci penandatangan), dari sebuah pesan (yang dalam kasus kita adalah transaksi). Bagian kedua adalah algoritma yang memungkinkan siapa pun untuk **memverifikasi tanda tangan** hanya dengan menggunakan pesan dan kunci publik.

##### Membuat tanda tangan digital

Dalam implementasi ECDSA di Ethereum, "pesan" yang ditandatangani adalah transaksi, atau lebih akuratnya, hash Keccak-256 dari data yang dikodekan RLP dari transaksi tersebut. Kunci penandatangan adalah kunci privat EOA. Hasilnya adalah tanda tangan:

$Sig = F\_{sig}(F\_{keccak256}(m), k)$

di mana:

  * $k$ adalah kunci privat penandatangan.
  * $m$ adalah transaksi yang dikodekan RLP.
  * $F\_{keccak256}$ adalah fungsi hash Keccak-256.
  * $F\_{sig}$ adalah algoritma penandatanganan.
  * $Sig$ adalah tanda tangan yang dihasilkan.

Fungsi $F\_{sig}$ menghasilkan tanda tangan $Sig$ yang terdiri dari dua nilai, yang biasa disebut sebagai $r$ dan $s$:

$Sig = (r, s)$

##### Memverifikasi Tanda Tangan

Untuk memverifikasi tanda tangan, seseorang harus memiliki tanda tangan ($r$ dan $s$), transaksi yang diserialisasi, dan kunci publik yang sesuai dengan kunci privat yang digunakan untuk membuat tanda tangan. Pada dasarnya, verifikasi tanda tangan berarti "hanya pemilik kunci privat yang menghasilkan kunci publik ini yang dapat menghasilkan tanda tangan ini pada transaksi ini."

Algoritma verifikasi tanda tangan mengambil pesan (yaitu, hash dari transaksi untuk penggunaan kita), kunci publik penanda tangan, dan tanda tangan (nilai $r$ dan $s$), dan mengembalikan `true` jika tanda tangan tersebut valid untuk pesan dan kunci publik ini.

#### Matematika ECDSA

Seperti yang disebutkan sebelumnya, tanda tangan dibuat oleh fungsi matematis $F\_{sig}$ yang menghasilkan tanda tangan yang terdiri dari dua nilai, $r$ dan $s$. Di bagian ini kita akan melihat fungsi $F\_{sig}$ secara lebih detail.

Algoritma penandatanganan pertama-tama menghasilkan kunci privat *ephemeral* (sementara) dengan cara yang aman secara kriptografis. Kunci sementara ini digunakan dalam perhitungan nilai $r$ dan $s$ untuk memastikan bahwa kunci privat asli pengirim tidak dapat dihitung oleh penyerang yang mengamati transaksi yang ditandatangani di jaringan Ethereum.

Seperti yang kita ketahui dari “Kunci Publik” di halaman 64, kunci privat *ephemeral* digunakan untuk menurunkan kunci publik yang sesuai (*ephemeral*), jadi kita memiliki:

  * Angka acak yang aman secara kriptografis $q$, yang digunakan sebagai kunci privat *ephemeral*.
  * Kunci publik *ephemeral* yang sesuai $Q$, yang dihasilkan dari $q$ dan titik generator kurva eliptik $G$.

Nilai **$r$** dari tanda tangan digital kemudian adalah koordinat x dari kunci publik *ephemeral* $Q$.

Dari sana, algoritma menghitung nilai **$s$** dari tanda tangan, sedemikian rupa sehingga:

$s \\equiv q^{-1} (\\text{Keccak256}(m) + r \\cdot k) \\pmod{p}$

di mana:

  * $q$ adalah kunci privat *ephemeral*.
  * $r$ adalah koordinat x dari kunci publik *ephemeral*.
  * $k$ adalah kunci privat penandatangan (pemilik EOA).
  * $m$ adalah data transaksi.
  * $p$ adalah orde prima dari kurva eliptik.

**Verifikasi** adalah kebalikan dari fungsi pembuatan tanda tangan, menggunakan nilai $r$ dan $s$ serta kunci publik pengirim untuk menghitung nilai $Q$, yang merupakan sebuah titik pada kurva eliptik (kunci publik *ephemeral* yang digunakan dalam pembuatan tanda tangan). Langkah-langkahnya adalah sebagai berikut:

1.  Periksa semua input terbentuk dengan benar.
2.  Hitung $w = s^{-1} \\pmod{p}$.
3.  Hitung $u\_1 = \\text{Keccak256}(m) \\cdot w \\pmod{p}$.
4.  Hitung $u\_2 = r \\cdot w \\pmod{p}$.
5.  Terakhir, hitung titik pada kurva eliptik $Q \\equiv u\_1 \\cdot G + u\_2 \\cdot K \\pmod{p}$.

di mana:

  * $r$ dan $s$ adalah nilai tanda tangan.
  * $K$ adalah kunci publik penanda tangan (pemilik EOA).
  * $m$ adalah data transaksi yang ditandatangani.
  * $G$ adalah titik generator kurva eliptik.
  * $p$ adalah orde prima dari kurva eliptik.

Jika koordinat x dari titik $Q$ yang dihitung sama dengan $r$, maka verifikator dapat menyimpulkan bahwa tanda tangan tersebut valid.

Perhatikan bahwa dalam memverifikasi tanda tangan, kunci privat tidak diketahui maupun diungkapkan.

> ECDSA tentu saja merupakan matematika yang cukup rumit; penjelasan lengkap berada di luar cakupan buku ini. Sejumlah panduan hebat secara daring akan memandu Anda langkah demi langkah: cari "ECDSA explained" atau coba yang ini: [http://bit.ly/2r0HhGB](http://bit.ly/2r0HhGB).

#### Praktik Penandatanganan Transaksi

Untuk menghasilkan transaksi yang valid, pengirim harus menandatangani pesan secara digital, menggunakan Elliptic Curve Digital Signature Algorithm. Ketika kita mengatakan "menandatangani transaksi", kita sebenarnya bermaksud "menandatangani hash Keccak-256 dari data transaksi yang diserialisasi RLP."
**Tanda tangan diterapkan pada hash dari data transaksi, bukan pada transaksi itu sendiri.**

Untuk menandatangani transaksi di Ethereum, pengirim harus:

1.  Membuat struktur data transaksi, yang berisi sembilan bidang: `nonce`, `gasPrice`, `gasLimit`, `to`, `value`, `data`, `chainID`, `0`, `0`.
2.  Menghasilkan pesan serial yang dikodekan RLP dari struktur data transaksi.
3.  Menghitung hash Keccak-256 dari pesan serial ini.
4.  Menghitung tanda tangan ECDSA, menandatangani hash dengan kunci privat EOA asal.
5.  Menambahkan nilai $v$, $r$, dan $s$ dari tanda tangan ECDSA ke transaksi.

Variabel tanda tangan khusus **$v$** menunjukkan dua hal: ID rantai (*chain ID*) dan pengidentifikasi pemulihan (*recovery identifier*) untuk membantu fungsi `ECDSArecover` memeriksa tanda tangan. Nilai ini dihitung sebagai salah satu dari 27 atau 28, atau sebagai ID rantai dikalikan dua ditambah 35 atau 36. Untuk informasi lebih lanjut tentang ID rantai, lihat “Pembuatan Transaksi Mentah dengan EIP-155” di halaman 120. Pengidentifikasi pemulihan (27 atau 28 dalam tanda tangan "gaya lama", atau 35 atau 36 dalam transaksi gaya Spurious Dragon penuh) digunakan untuk menunjukkan paritas komponen y dari kunci publik (lihat “Nilai Awalan Tanda Tangan (v) dan Pemulihan Kunci Publik” di halaman 120 untuk detail lebih lanjut).

> Pada blok \#2.675.000, Ethereum mengimplementasikan *hard fork* "Spurious Dragon", yang, di antara perubahan lainnya, memperkenalkan skema penandatanganan baru yang mencakup perlindungan pemutaran ulang transaksi (*replay protection*), mencegah transaksi yang ditujukan untuk satu jaringan diputar ulang di jaringan lain. Skema penandatanganan baru ini ditentukan dalam EIP-155. Perubahan ini memengaruhi bentuk transaksi dan tanda tangannya, jadi perhatian harus diberikan pada variabel tanda tangan pertama dari tiga (yaitu, v), yang mengambil salah satu dari dua bentuk dan menunjukkan bidang data yang termasuk dalam pesan transaksi yang di-hash.

#### Pembuatan dan Penandatanganan Transaksi Mentah

Di bagian ini kita akan membuat transaksi mentah dan menandatanganinya, menggunakan pustaka `ethereumjs-tx`. Ini menunjukkan fungsi-fungsi yang biasanya digunakan di dalam dompet, atau aplikasi yang menandatangani transaksi atas nama pengguna. Kode sumber untuk contoh ini ada di file `raw_tx_demo.js` di repositori GitHub buku ini:

```javascript
// Muat persyaratan terlebih dahulu:
//
// npm init
// npm install ethereumjs-tx
//
// Jalankan dengan: $ node raw_tx_demo.js

const ethTx = require('ethereumjs-tx');

const txData = {
  nonce: '0x0',
  gasPrice: '0x09184e72a000',
  gasLimit: '0x30000',
  to: '0xb0920c523d582040f2bcb1bd7fb1c7c1ecebdb34',
  value: '0x00',
  data: '',
  v: "0x1c", // ID rantai utama Ethereum
  r: 0,
  s: 0
};

tx = new ethTx(txData);
console.log('Tx Terenkode RLP: 0x' + tx.serialize().toString('hex'))

txHash = tx.hash(); // Langkah ini mengkodekan ke RLP dan menghitung hash
console.log('Hash Tx: 0x' + txHash.toString('hex'))

// Tandatangani transaksi
const privKey = Buffer.from(
  '91c8360c4cb4b5fac45513a7213f31d4e4a7bfcb4630e9fbf074f42a203ac0b9', 'hex');

tx.sign(privKey);

serializedTx = tx.serialize();
rawTx = 'Transaksi Mentah yang Ditandatangani: 0x' + serializedTx.toString('hex');
console.log(rawTx)
```

Menjalankan kode contoh menghasilkan hasil berikut:

```bash
$ node raw_tx_demo.js
Tx Terenkode RLP: 0xe6808609184e72a0008303000094b0920c523d582040f2bcb1bd7fb1c7c1...
Hash Tx: 0xaa7f03f9f4e52fcf69f836a6d2bbc7706580adce0a068ff6525ba337218e6992
Transaksi Mentah yang Ditandatangani: 0xf866808609184e72a0008303000094b0920c523d582040f2bcb1...
```

#### Pembuatan Transaksi Mentah dengan EIP-155

Standar EIP-155 "Perlindungan Serangan Pemutaran Ulang Sederhana" menentukan pengkodean transaksi yang dilindungi dari serangan pemutaran ulang, yang mencakup pengidentifikasi rantai (*chain identifier*) di dalam data transaksi, sebelum penandatanganan. Ini memastikan bahwa transaksi yang dibuat untuk satu blockchain (mis., jaringan utama Ethereum) tidak valid di blockchain lain (mis., Ethereum Classic atau jaringan uji Ropsten). Oleh karena itu, transaksi yang disiarkan di satu jaringan tidak dapat diputar ulang di jaringan lain, sesuai dengan nama standar tersebut.

EIP-155 menambahkan tiga bidang ke enam bidang utama dari struktur data transaksi, yaitu **pengidentifikasi rantai, 0, dan 0**. Tiga bidang ini ditambahkan ke data transaksi sebelum dikodekan dan di-hash. Oleh karena itu, mereka mengubah hash transaksi, yang kemudian diterapkan tanda tangan. Dengan menyertakan pengidentifikasi rantai dalam data yang ditandatangani, tanda tangan transaksi mencegah perubahan apa pun, karena tanda tangan menjadi tidak valid jika pengidentifikasi rantai diubah. Oleh karena itu, EIP-155 membuat tidak mungkin sebuah transaksi diputar ulang di rantai lain, karena validitas tanda tangan bergantung pada pengidentifikasi rantai.

Bidang pengidentifikasi rantai mengambil nilai sesuai dengan jaringan yang dituju oleh transaksi, seperti yang diuraikan dalam Tabel 6-1.

<p align="center">
  <img src="images/books-07-mastering_ethereum/tabel-6.1.png" alt="gambar" width="580"/>
</p>

Struktur transaksi yang dihasilkan dikodekan dengan RLP, di-hash, dan ditandatangani. Algoritma tanda tangan sedikit dimodifikasi untuk mengkodekan pengidentifikasi rantai di awalan `v` juga. Untuk detail lebih lanjut, lihat spesifikasi EIP-155.

### Nilai Awalan Tanda Tangan (v) dan Pemulihan Kunci Publik

Seperti yang disebutkan dalam “Struktur Transaksi” di halaman 99, pesan transaksi tidak menyertakan bidang "from". Itu karena kunci publik pengirim dapat dihitung langsung dari tanda tangan ECDSA. Setelah Anda memiliki kunci publik, Anda dapat menghitung alamatnya dengan mudah. Proses memulihkan kunci publik penanda tangan disebut **pemulihan kunci publik (*public key recovery*)**.

Dengan nilai $r$ dan $s$ yang dihitung dalam “Matematika ECDSA” di halaman 116, kita dapat menghitung dua kemungkinan kunci publik.

Pertama, kita menghitung dua titik kurva eliptik, $R$ dan $R'$, dari nilai koordinat x yaitu $r$ yang ada di tanda tangan. Ada dua titik karena kurva eliptik simetris terhadap sumbu x, sehingga untuk setiap nilai x ada dua kemungkinan nilai yang sesuai dengan kurva, satu di setiap sisi sumbu x.

Dari $r$ kita juga menghitung $r^{-1}$, yang merupakan invers perkalian dari $r$.

Terakhir, kita menghitung $z$, yang merupakan bit terendah `n` dari hash pesan, di mana `n` adalah orde kurva eliptik.

Dua kemungkinan kunci publik tersebut adalah:

$K_1 = r^{-1} (sR – zG)$

dan:

$K_2 = r^{-1} (sR' – zG)$

di mana:
* $K_1$ dan $K_2$ adalah dua kemungkinan untuk kunci publik penanda tangan.
* $r^{-1}$ adalah invers perkalian dari nilai $r$ tanda tangan.
* $s$ adalah nilai $s$ tanda tangan.
* $R$ dan $R'$ adalah dua kemungkinan untuk kunci publik *ephemeral* $Q$.
* $z$ adalah bit terendah `n` dari hash pesan.
* $G$ adalah titik generator kurva eliptik.

Untuk membuat segalanya lebih efisien, tanda tangan transaksi menyertakan nilai awalan **$v$**, yang memberi tahu kita mana dari dua kemungkinan nilai $R$ yang merupakan kunci publik *ephemeral*. Jika $v$ **genap**, maka $R$ adalah nilai yang benar. Jika $v$ **ganjil**, maka itu adalah $R'$. Dengan begitu, kita hanya perlu menghitung satu nilai untuk $R$ dan hanya satu nilai untuk $K$.

### Memisahkan Penandatanganan dan Transmisi (Penandatanganan Luring)

Setelah sebuah transaksi ditandatangani, ia siap untuk dikirim ke jaringan Ethereum. Tiga langkah membuat, menandatangani, dan menyiarkan transaksi biasanya terjadi sebagai satu operasi tunggal, misalnya menggunakan `web3.eth.sendTransaction`. Namun, seperti yang Anda lihat di “Pembuatan dan Penandatanganan Transaksi Mentah” di halaman 119, Anda dapat membuat dan menandatangani transaksi dalam dua langkah terpisah. Setelah Anda memiliki transaksi yang ditandatangani, Anda kemudian dapat mengirimkannya menggunakan `web3.eth.sendSignedTransaction`, yang mengambil transaksi yang dikodekan heksadesimal dan ditandatangani lalu mentransmisikannya di jaringan Ethereum.

Mengapa Anda ingin memisahkan penandatanganan dan transmisi transaksi? Alasan paling umum adalah **keamanan**. Komputer yang menandatangani transaksi harus memiliki kunci privat yang tidak terkunci yang dimuat di memori. Komputer yang melakukan transmisi harus terhubung ke internet (dan menjalankan klien Ethereum). Jika kedua fungsi ini berada di satu komputer, maka Anda memiliki kunci privat di sistem daring, yang cukup berbahaya. Memisahkan fungsi penandatanganan dan transmisi dan melakukannya di mesin yang berbeda (masing-masing di perangkat luring dan daring) disebut **penandatanganan luring (*offline signing*)** dan merupakan praktik keamanan yang umum.

Gambar 6-7 menunjukkan prosesnya:
1.  Buat transaksi yang belum ditandatangani di komputer daring di mana keadaan akun saat ini, terutama nonce saat ini dan dana yang tersedia, dapat diambil.
2.  Transfer transaksi yang belum ditandatangani ke perangkat luring yang terisolasi (*air-gapped*) untuk penandatanganan transaksi, mis., melalui kode QR atau USB flash drive.
3.  Kirim transaksi yang sudah ditandatangani (kembali) ke perangkat daring untuk disiarkan di blockchain Ethereum, mis., melalui kode QR atau USB flash drive.

<p align="center">
  <img src="images/books-07-mastering_ethereum/figure-6.7.png" alt="gambar" width="580"/>
</p>

