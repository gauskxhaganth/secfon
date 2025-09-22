# JAM 1
## Gambaran Umum Jaringan Komputer

**Apa yang Akan Anda Pelajari dalam Jam Ini:**
* Definisi jaringan komputer
* Mengapa kita membutuhkan jaringan komputer
* Komponen-komponen sebuah jaringan
* Berbagai jenis jaringan
* Pentingnya Internet

Jaringan komputer telah menjadi bagian dari kehidupan kita sehari-hari. Kita menggunakannya untuk mengambil uang tunai dari ATM lokal. Setiap kali kita mengirim email atau menjelajahi Web, kita mengandalkan jaringan komputer terbesar di dunia, Internet, untuk menjadi tukang pos elektronik kita. Para *telemarketer*, biasanya saat jam makan malam, menggunakan jaringan komputer untuk menjual barang dagangan mereka kepada kita. Stasiun televisi kabel kita bergantung pada jaringan komputer untuk menyalurkan program ke layar TV kita. Apa contoh paling nyata dari kehadiran mereka dalam hidup kita? Tanpa jaringan komputer, ponsel kita tak lebih dari sekadar baterai yang menyalakan layar tanpa arti.

Untuk menyediakan layanan-layanan luar biasa ini, jaringan komputer mentransfer data ke dan dari perangkat TV, komputer pribadi, ponsel, dan mesin modern lainnya. Data ini kemudian diterjemahkan oleh aplikasi menjadi gambar video TV, ikon di layar PC, dan pesan teks di ponsel. Tugas-tugas jaringan ini hanya memakan waktu sekitar satu detik (seringkali kurang) untuk diselesaikan—bahkan jika jaringan harus mengambil data dari seluruh dunia. Mengapa menonton film fiksi ilmiah? Jaringan komputer sama mengesankannya.

Meskipun jaringan data, seperti halnya komputer, telah menjadi bagian tak terpisahkan dari hidup kita, kebanyakan orang menganggap jaringan komputer sebagai subjek yang terlalu rumit bahkan untuk dipertimbangkan untuk dibuat. Biasanya, kita meminta bantuan "pasukan ahli" terdekat, atau kita mendatangkan spesialis dari departemen jaringan perusahaan kita.

Tapi mari kita bocorkan sebuah rahasia—satu hal yang para "pakar" teknis ini tidak ingin diketahui: Jaringan komputer tidaklah serumit itu. Tidak memerlukan keanggotaan dalam perkumpulan rahasia. Kecuali jika Anda memilih untuk menjadi seorang programmer perangkat lunak atau perancang perangkat keras, kecuali jika Anda memilih untuk membangun jaringan dari awal, Anda tidak perlu mengabdikan bertahun-tahun studi untuk dapat mengatur dan mengelola jaringan Anda sendiri.

Di masa lalu, mengelola jaringan memang membutuhkan pengalaman dan pelatihan yang mendalam. Dan jangan salah: Buku ini tidak akan memberi Anda informasi yang cukup untuk mengelola Internet! Tapi sekarang, dengan menjamurnya jutaan jaringan dan pengguna jaringan, industri menyediakan alat untuk memungkinkan Anda tidak hanya memahami jaringan komputer tetapi juga untuk mengatur dan mengelolanya secara efektif.

Memperoleh kemampuan untuk membuat jaringan komputer memerlukan pemahaman tentang beberapa konsep fundamental, yaitu dasar-dasar komunikasi data. Ditambah dengan akal sehat—dan membaca buku ini—Anda dapat merakit jaringan Anda sendiri.

> **Tahukah Anda?**
>
> **Membaca untuk Mempelajari Lebih Lanjut**
>
> Semakin banyak Anda membaca tentang konsep jaringan dan isu-isu yang berkaitan dengan jaringan komputer, akan semakin mudah untuk mengimplementasikan dan memelihara jaringan Anda sendiri. Situs web `www.informit.com` adalah cara yang baik untuk memulai. Setelah membaca buku ini, kunjungi situs tersebut. Anda mungkin akan terkejut mengetahui betapa akrabnya konsep-konsep tersebut bagi Anda.
>
> Selain itu, saya merekomendasikan entri Wikipedia tentang subjek ini di `http://wikipedia.org`.
>
> Untuk pembaca yang lebih mahir, saya sarankan untuk mempelajari spesifikasi Internet, yang tersedia di `http://www.isoc.org`.

### Apa Itu Jaringan? Apa Itu Berjejaring (*Networking*)?

Dalam istilah yang paling sederhana, sebuah **jaringan komputer** terdiri dari dua atau lebih komputer yang terhubung. Koneksi ini ada dua macam: (a) **fisik**, melalui kabel, kawat, dan media nirkabel (atmosfer, misalnya pada ponsel), dan (b) **logis**, melalui pengangkutan data melintasi media fisik tersebut. Kita akan membahas komponen yang diperlukan untuk membuat koneksi fisik di beberapa bagian buku ini; terutama, pada Jam ke-4, 10, dan 23. Koneksi logis akan dibahas di seluruh buku ini.

Dalam konteks buku ini, apa itu *networking*? Jika saya berkata kepada seseorang, "Saya sedang *networking*!", apa arti pernyataan ini? Sebagai permulaan, itu tidak berarti saya sedang bersosialisasi dengan rekan kerja atau berbaur dengan orang tua di pertemuan komite sekolah setempat. Itu berarti saya sedang duduk di depan komputer, berkomunikasi dengan seseorang atau sesuatu melalui jaringan komputer. Tentu, tetapi Anda tidak perlu membaca selama 24 jam untuk mengajari Anda cara duduk di depan terminal dan bermain Scrabble online.

Dengan demikian, *Sams Teach Yourself Networking in 24 Hours* adalah judul singkat untuk mengajari Anda cara membangun jaringan sehingga Anda nantinya dapat melakukan *networking* (berjejaring).

Seperti yang telah disinggung, menghubungkan komputer lebih dari sekadar konektor fisik, seperti colokan listrik di dinding dan porta di PC. Beberapa aturan dasar harus diikuti agar komputer dapat saling bertukar data.

* Mesin-mesin dalam jaringan harus menggunakan prosedur yang sama untuk mengirim dan menerima data. Prosedur ini disebut **protokol komunikasi**. Jika perangkat-perangkat ini tidak (atau tidak bisa) menggunakan protokol yang sama, konversi harus dilakukan, biasanya dengan layanan yang disebut **konverter protokol**. Idenya mirip dengan seseorang yang menerjemahkan antara orang yang berbicara bahasa Spanyol dan orang yang berbicara bahasa Inggris. Untuk jaringan komputer, saya bisa mengirim email kepada anak saya dari komputer berbasis kabel saya ke ponselnya yang terhubung ke Internet.¹ Agar anak saya (Tommy) dapat membaca pesan ini, konversi dilakukan di tingkat fisik (gambar berbasis kabel menjadi gambar berbasis nirkabel) dan di tingkat logis (format email menjadi format teks). Untungnya, Anda tidak perlu berurusan dengan konverter protokol. Mereka disediakan untuk Anda secara otomatis.
* Data harus dikirimkan **tanpa kerusakan**. Artinya, jika saya mengetik "Halo, Tommy" di email saya, pesan itu harus (dan akan) diterima di ponselnya sebagai, "Halo, Tommy," dan bukan, katakanlah, "Halo, Mommy."
* Harus ada metode di mana komputer penerima (Ngomong-ngomong, ponsel modern mengandung setidaknya satu komputer) dapat **mengonfirmasi penerimaan data** yang tidak rusak dan memberitahu komputer pengirim jika data memang diterima dengan kesalahan. Jadi, jika perangkat Tommy menerima "Halo, Mommy," Tommy tidak akan pernah melihat kesalahan ini muncul di layarnya. Tanpa sepengetahuan Tommy, sebuah perangkat lunak akan memeriksa data dan mengirim pesan kembali ke komputer saya untuk meminta pengiriman ulang. Saya juga tidak akan tahu tentang layanan luar biasa ini. Terlebih lagi, karena semua dialog ini berlangsung begitu cepat (dalam beberapa sepersekian detik), Tommy dan saya tidak menyadari adanya penundaan singkat dalam dialog kami yang sedang berlangsung.
* Komputer di dalam jaringan harus mampu **menentukan asal dan tujuan** dari sebuah informasi, seperti email atau pesan teks. Lagi pula, jika Tommy ingin mengirim balasan kepada saya, jaringan harus dapat merutekannya ke komputer saya, dan perangkat Tommy harus memberikan alamat tersebut ke jaringan. Sekali lagi, Anda biasanya tidak perlu khawatir dengan tugas-tugas ini. Alamat sering kali diberikan kepada Anda secara otomatis. Seperti yang akan kita lihat, ini adalah layanan lain yang disediakan bagi pengguna jaringan.
* Tentu saja, **alamat yang terstandardisasi** diperlukan untuk pertukaran data yang benar antar komputer. Karena jutaan komputer di seluruh dunia dapat terhubung dalam jaringan, alamat-alamat ini harus "dapat diskalakan" (*scalable*) untuk mengakomodasi populasi komputer yang besar.
* Untuk keamanan dan manajemen, harus ada metode untuk **mengidentifikasi dan memverifikasi** perangkat yang terhubung ke jaringan. Peretas harus dicegah dari merusak komputer dan file.

Daftar ini bukanlah serangkaian persyaratan jaringan yang lengkap dan, seperti yang telah disebutkan, untuk mendapatkan sebagian besar layanan ini, Anda tidak perlu mengangkat satu jari pun ke keyboard atau keypad Anda. Kami mencantumkannya untuk memberi Anda gambaran tentang beberapa masalah yang dihadapi ketika para ahli jaringan komputer menangani tugas pertukaran dan berbagi data antar komputer. Seperti yang terlihat sebelumnya, agar transfer data antar komputer dapat terjadi, aturan harus diikuti. Jika tidak, prosesnya mirip dengan orang-orang yang mencoba berbicara satu sama lain dalam bahasa yang berbeda.

Jaringan bisa sesederhana koneksi titik-ke-titik (*point-to-point*) antara dua komputer yang saling mentransfer file. Jaringan juga bisa sangat kompleks. Salah satu contoh yang terlintas dalam pikiran adalah sistem Federal Reserve, yang memungkinkan kita mentransfer dana secara elektronik antar rekening. Contoh lainnya adalah jaringan seluler. Jaringan ini melacak kita saat kita bergerak melintasi suatu wilayah dan menyerahkan koneksi kita ke menara nirkabel berikutnya di "sel" tempat kita baru saja pindah.

Meskipun contoh titik-ke-titik jauh lebih sederhana daripada contoh perbankan dan seluler, masing-masing harus mengikuti aturan dasar yang sama untuk memungkinkan pengguna berkomunikasi satu sama lain. Kita akan menjelajahi jaringan sederhana dan kompleks dalam buku ini. Namun, sebelum kita mendalami detail jaringan komputer dan cara mengaturnya, kita harus berhenti sejenak dan menjawab pertanyaan ini: Mengapa kita ingin membangun jaringan? Saya menduga Anda punya jawaban sendiri; jika tidak, Anda tidak akan membaca buku ini. Izinkan saya memberikan beberapa pemikiran tentang masalah ini; mungkin sama dengan pemikiran Anda.

### Mengapa Membangun Jaringan?

Jika kita puas dengan menerima atau mengirim informasi secara manual, kita bisa menggunakan layanan pos. Tapi korespondensi dalam bentuk cetak disebut "surat siput" (*snail-mail*) karena alasan yang bagus. Terlalu lambat di dunia yang serba cepat saat ini. Pada saat surat tiba, isinya sering kali sudah menjadi berita basi.

* Sebaliknya, jaringan komputer memungkinkan **komunikasi yang lebih cepat** antar pihak. Dengan demikian, hal itu mengarah pada penggunaan waktu yang lebih efisien.
* Dengan berbagi data elektronik di antara mungkin ribuan orang, jaringan komputer mendorong (mengharuskan!) penggunaan **kebijakan dan prosedur standar**. Bagaimanapun, komputer pribadi kita dan ponsel kita yang mahir berkirim pesan teks tidak memiliki daya inferensi seperti kita manusia. Kita bisa saja merespons dengan, "Tolong ulangi lagi," jika kita tidak mengerti suatu transmisi. Tetapi jaringan komputer harus diprogram dengan susah payah untuk melakukan satu tugas sederhana ini. Namun, sekali lagi, prosedur standar ini mengarah pada komunikasi yang lebih efisien.
* Jaringan menyediakan dukungan **cadangan (*backup*) dan pemulihan (*recovery*)** untuk data kita. Jika truk surat layanan pos mogok, surat kita mungkin tertunda selama sehari—setidaknya. Tidak demikian halnya dengan jaringan komputer. Jaringan dirancang untuk memberikan pemulihan yang hampir seketika dari kegagalan—semua tanpa kehilangan satu karakter atau angka pun dalam surat (elektronik) kita.
* "Saya kehilangan file itu!" "Saya kehilangan surat itu!" Keluhan ini tidak lagi berlaku dengan jaringan komputer. Jika jaringan dirancang dengan benar, mudah untuk **menyimpan salinan data kita**. Baik itu surat, foto, file, atau video, kita dapat menyimpan salinannya dengan aman di komputer lain di bagian lain negara—jika kita meluangkan waktu untuk menginstruksikan jaringan untuk melakukannya.
* **Sumber daya bersama** (*shared resources*) menghasilkan komunikasi yang lebih murah. Ambil contoh Internet. Ini adalah jaringan publik yang mahal (pada kenyataannya, jutaan jaringan yang saling terhubung), tetapi kita menggunakannya hanya dengan beberapa dolar sebulan, dan kinerjanya sedemikian rupa sehingga kita mungkin menganggapnya sebagai jaringan pribadi kita sendiri. Artinya, kita berpikir kita memiliki jaringan ini untuk diri kita sendiri, padahal tidak. Istilah untuk menggambarkan layanan baik ini adalah **jaringan privat virtual** (*virtual private network*).

Ada banyak alasan untuk menggunakan jaringan komputer sebanyak orang yang membagikannya dan organisasi yang membangunnya. Seseorang mungkin memiliki banyak komputer di rumah—satu untuknya, satu untuk suaminya, beberapa untuk anak-anak. Dia mungkin ingin menghubungkan semua komputer agar keluarga dapat memiliki kalender dan email bersama, yang, seperti kita tahu, akan lebih mudah dibaca oleh anak-anak daripada catatan di kulkas. Orang lain mungkin ingin menghubungkan kantor kecil atau jaringan rumahnya ke Internet untuk menggunakan Web. Orang lain lagi di Texas mungkin ingin bermain Texas Hold'em dengan teman-temannya yang tinggal di New Jersey.

Jaringan komputer telah mengubah cara kita bekerja dan bermain. Baik atau buruk, mereka telah mengubah hidup kita. Saya percaya bahwa Anda berpikir perubahan itu menjadi lebih baik. Saya pun demikian. Tapi kita sudah cukup banyak bicara tentang mengapa kita menggunakan jaringan komputer. Mari sekarang kita lihat bagaimana mereka digunakan, dan lebih tepatnya, bagaimana kita dapat menggunakannya untuk meningkatkan kehidupan pribadi dan profesional kita.

### Bagaimana Jaringan Disusun

Untuk mengulangi poin penting, jika kita memecah jaringan menjadi komponen-komponennya yang paling sederhana, komponen-komponen ini akan diidentifikasi sebagai salah satu dari dua kategori. Salah satunya adalah **jaringan fisik**. Ini terdiri dari kabel atau media nirkabel; kartu jaringan di dalam komputer yang berinteraksi dengan "colokan" di komputer; dan, tentu saja, komputer itu sendiri (yang mungkin berupa server email, server file, dan mesin lain yang akan dibahas nanti). Kategori lainnya adalah **bagian logis** dari jaringan. Biasanya diimplementasikan dalam perangkat lunak, ini menyediakan sarana untuk membangun bagian-bagian jaringan yang menjadi "antarmuka" kita. Contohnya adalah email, pesan teks, halaman web, video, dan gambar di layar komputer kita. Kami akan memperkenalkan komponen-komponen ini selama jam ini, dan akan dibahas lebih detail di jam-jam berikutnya.

### Arsitektur Jaringan: Menggabungkan Komponen Fisik dan Logis

Ketika komputer terhubung, kita harus memilih **arsitektur jaringan**, yang merupakan kombinasi dari semua komponen fisik dan logis. Komponen-komponen tersebut diatur (semoga) sedemikian rupa sehingga memberikan kita sistem transportasi dan penyimpanan yang efisien untuk data kita. Arsitektur jaringan yang kita pilih menentukan **topologi fisik** dan **pengaturan logis** dari sistem. Sebagai contoh, jika saya berkata, "Saya sedang membangun jaringan Switched Ethernet," pernyataan ini menyiratkan arsitektur keseluruhan dari jaringan masa depan saya. Mari kita sekarang memeriksa komponen fisik dan logis ini.

#### Jaringan Fisik

Jaringan fisik mudah dipahami karena biasanya terlihat. Terutama, ini terdiri dari perangkat keras: kabel, colokan seperti porta komputer, printer, server email, dan perangkat lain yang memproses dan menyimpan data kita. Jaringan fisik juga mencakup sinyal-sinyal penting (baca: vital) yang merepresentasikan data pengguna. Contohnya adalah level tegangan dan pulsa cahaya untuk merepresentasikan citra biner dari angka 1 dan 0—dirangkai bersama dalam banyak kombinasi untuk menggambarkan data kita.

Saya mengatakan "biasanya terlihat" karena kita tidak bisa melihat koneksi nirkabel. Meskipun lebih etereal daripada koneksi kabel tembaga, koneksi nirkabel tetaplah fisik, dalam bentuk gelombang radio elektromagnetik.

Sangat jarang hanya beberapa tahun yang lalu, jaringan nirkabel seperti Wi-Fi sekarang sudah umum. Jika Anda memiliki koneksi *broadband* di rumah Anda, kemungkinan besar komputer Anda terhubung ke perangkat keras *broadband* Anda dengan pengaturan nirkabel. Cara kita menjelaskan tata letak (juga disebut **topologi**) dari jaringan nirkabel tidak berbeda dari jaringan berbasis kabel.

#### Tata Letak Fisik—Topologi Jaringan

Seperti yang disebutkan, aspek fisik dari jaringan terdiri dari komponen-komponen yang mendukung koneksi fisik antar komputer. Dalam jaringan saat ini, empat topologi digunakan: (a) **bintang** (*star*), (b) **cincin** (*ring*), (c) **bus**, dan (d) **sel** (*cell*). Mereka digambarkan pada Gambar 1.1.

<p align="center">
  <img src="images/book-sams_teach_yourself_networking/figure-1.1.png" alt="gambar" width="580"/>
</p>

* **Bintang (*Star*)**—Topologi bintang menggunakan titik koneksi pusat, yang disebut **router**, **hub**, **bridge**, atau **switch**. Komputer-komputer di jaringan menyebar keluar dari titik ini, seperti yang terlihat pada Gambar 1.1(a). Tugas dari titik pusat ini adalah untuk mengalihkan (*switch*) atau menyampaikan (*relay*) data pengguna antar mesin pengguna dan mungkin ke titik koneksi pusat lainnya. Istilah *router*, *hub*, *bridge*, atau *switch* digunakan secara bergantian oleh beberapa orang. Umumnya, istilah *hub* dan *bridge* dikaitkan dengan perangkat yang kapasitasnya agak terbatas. Istilah *switch* secara historis dikaitkan dengan jaringan telepon (dengan pengecualian *message switch* pada jaringan komputer tahun 1970-an dan *packet switch* pada tahun 1980-an). Istilah *router* masuk ke dalam industri pada tahun 1980-an dan sekarang lebih sering digunakan daripada istilah lainnya. Apapun sebutan kita untuk mesin-mesin ini, mereka mengelola lalu lintas di jaringan dan menyampaikan lalu lintas ini bolak-balik di antara komputer kita.

* **Cincin (*Ring*)**—Topologi cincin, yang ditunjukkan pada Gambar 1.1(b), menghubungkan komputer-komputer melalui sebuah kawat atau kabel. Saat data (biasanya disebut **paket**) berjalan mengelilingi cincin, setiap komputer memeriksa alamat tujuan di dalam *header* paket (konsepnya mirip dengan alamat "kepada" pada amplop surat) dan menyalin data tersebut jika alamat komputer cocok dengan alamat tujuan. Jika tidak, komputer hanya meneruskan paket tersebut kembali ke cincin ke komputer berikutnya (sering disebut *node* berikutnya). Ketika paket tiba di *node* asal, *node* tersebut akan menghapus paket dari cincin dengan tidak meneruskannya.
    Topologi cincin adalah contoh pertama dari **jaringan siar (*broadcast network*)**: *Node-node* di dalam jaringan menerima semua lalu lintas di jaringan tersebut. Apakah sebuah *node* memilih untuk menerima paket atau tidak tergantung pada alamat tujuan di dalam *header* paket.

* **Bus**—Topologi bus ditunjukkan pada Gambar 1.1(c). Topologi ini terdiri dari sebuah kabel dengan cabang-cabang (*taps*) di sepanjang kabel tempat komputer terhubung. Ini juga merupakan jaringan siar (*broadcast network*) karena semua *node* menerima lalu lintas. *Node* pengirim mentransmisikan paket ke kedua arah di bus. *Node* penerima akan menyalin citra paket jika alamat tujuan cocok dengan alamat *node* tersebut. Paket merambat dengan cepat melalui bus, di mana kemudian "dihentikan" (*terminated*) di kedua ujung bus. Seperti yang mungkin sudah Anda duga, paket-paket yang berjalan di sepanjang bus ini dapat saling mengganggu jika *node-node* mengirimkan paket ke bus pada waktu yang hampir bersamaan. Topologi bus menangani situasi ini dengan prosedur **deteksi tabrakan (*collision detection*)**. Sebuah *node* akan terus mengirim sampai mendeteksi bahwa transmisinya telah terjadi tanpa gangguan (dengan memeriksa transmisinya sendiri).

* **Seluler (*Cellular*)**—Topologi seluler digunakan dalam jaringan nirkabel, sebuah susunan yang ditunjukkan pada Gambar 1.1(d). Jaringan seluler menggunakan protokol siar (*broadcast*); semua *node* (ponsel) mampu menerima transmisi pada **saluran kontrol (*control channel*)** dari sebuah situs pusat. Sebuah *node* kontrol nirkabel (disebut **base station**) menggunakan saluran umum ini untuk mengarahkan sebuah *node* agar terkunci pada **saluran (pengguna) spesifik** untuk koneksinya. Selama koneksi berlangsung, ponsel secara bersamaan berkomunikasi dengan *base station* melalui tautan kontrol (*control link*) dan tautan pengguna (*user link*).

### Jaringan Logis

Bagian sebelumnya menjelaskan tata letak fisik jaringan, seperti topologi bintang. Dalam menjelaskan bagaimana paket lalu lintas pengguna dipindahkan melintasi topologi-topologi ini, kita juga telah menjelaskan aspek-aspek **logis** dari sebuah jaringan. Sekali lagi, bagian logis dari jaringan komputer melibatkan penggunaan perangkat lunak untuk "mendorong" paket melintasi media fisik dan menerimanya di ujung lain.

Berbeda dengan jaringan fisik, jaringan logis tidak terlihat. Ia menggunakan jaringan fisik untuk transportasi data. Kami menunda penjelasan detail tentang jaringan logis di sini, karena akan dijelaskan secara ekstensif di hampir setiap jam berikutnya.

### Dua Jenis Jaringan: Area Lokal dan Area Luas

Topologi jaringan komputer adalah fitur penting dari komposisinya. Fitur lainnya adalah komposisi geografis: **cakupan jaringan**. Artinya, seberapa jauh jangkauannya? Rentang sebuah jaringan—lingkup fisiknya—sering kali menentukan bagaimana cara jaringan itu mengirim, menerima, dan mengelola data.

> **Kata "Link" Digunakan dalam Dua Cara**
>
> Sering kali, kata "link" (tautan) digunakan untuk menggambarkan saluran komunikasi jaringan komputer, seperti *satellite link* (tautan satelit) atau *cellular telephone link* (tautan telepon seluler). Kata lain untuk *link* adalah *line* (jalur) dan *channel* (saluran). Perlu diketahui bahwa penggunaan "link" di Web berbeda. Untuk Web, "link" berarti koneksi ke sesuatu yang lain, seperti halaman web lain atau situs web lain.

#### LAN

**Jaringan Area Lokal (*Local Area Network* atau LAN)** dinamakan demikian karena *node-node*-nya berada dalam jarak yang berdekatan satu sama lain, biasanya di dalam satu gedung atau di dalam rumah. Di masa lalu, prosedur (protokol) yang digunakan untuk mengelola LAN bergantung pada kedekatan *node-node*—sekitar satu kilometer atau kurang. Topologi bus Ethernet yang lebih tua adalah contoh dari ide yang terbatas pada jarak ini. Cara lain untuk menggambarkan LAN adalah bahwa biasanya LAN merupakan **jaringan privat**. Jaringan ini dimiliki, dioperasikan, dan digunakan oleh sebuah perusahaan atau individu, dengan mengecualikan perusahaan dan individu lain.

Selain itu, di masa lalu (beberapa dekade yang lalu), LAN dikenal karena kapasitasnya yang "berkecepatan tinggi" (*high-speed*). LAN Ethernet asli mengirim dan menerima data dengan kecepatan 10 juta bit per detik (bps)—tingkat transfer yang fenomenal pada masa itu. Saat ini, kapasitas ini dan bahkan lebih besar lagi dapat dinikmati oleh LAN maupun **jaringan area luas (*Wide Area Networks* atau WAN)**, yang akan dibahas selanjutnya.

> **Jaringan "Kecepatan Tinggi" Tidak Lebih Cepat dari Jaringan "Kecepatan Rendah"**
>
> Semua jaringan komputer beroperasi pada kecepatan yang sama. Mereka mengirim dan menerima data dengan kecepatan sekitar 186.000 mil per detik. Jadi, apa yang membuat koneksi Internet "broadband" yang luar biasa itu terasa begitu "cepat"? Bagaimanapun, kecepatan transmisi dibatasi oleh hukum fisika. Jawabannya adalah jaringan komputer menggunakan berbagai metode untuk merepresentasikan data pada tautan komunikasi. Sebagai contoh, karakter "U" dalam nama saya mungkin dapat direpresentasikan oleh kode delapan bit (angka biner 0 dan 1).
>
> Namun, untuk tautan "berkecepatan tinggi", data dikodekan dan dikompres sedemikian rupa sehingga aliran data yang besar direpresentasikan oleh jumlah bit yang jauh lebih sedikit. Oleh karena itu, tautan *broadband*, yang beroperasi pada jutaan bit per detik, menggunakan teknik pengkodean dan kompresi yang cerdas untuk menempatkan lebih banyak bit per detik ke dalam sebuah saluran komunikasi.
>
> Istilah "kecepatan" untuk menggambarkan (1) sistem berkapasitas tinggi yang (2) menawarkan waktu respons yang cepat sudah sangat tepat. Kecepatan dalam konteks ini menggambarkan laju di mana data ditransmisikan atau pengukuran berapa lama waktu yang dibutuhkan untuk suatu fungsi dilakukan.

#### WAN

Seperti namanya, **jaringan area luas (*Wide Area Networks* atau WAN)** tersebar secara geografis. Mereka biasanya terhubung ke jaringan lokal dengan sebuah **router**. Mesin ini menyampaikan paket antar komputer, yang sering kali berada di LAN, seperti yang terlihat pada Gambar 1.2. Akses ke WAN diperoleh dengan jalur telepon *dial-up* atau dengan tautan *broadband*, seperti *Digital Subscriber Line* (DSL), tautan TV kabel, atau tautan satelit. Opsi *dial-up*, meskipun banyak digunakan, kapasitasnya cukup terbatas, mungkin hanya beroperasi pada 56.000 bps. Sebaliknya, tautan *broadband* mentransfer data dalam rentang megabit per detik (Mbps). Begitu Anda menggunakan *broadband*, Anda kemungkinan besar tidak akan senang dengan *dial-up*. Mengunduh halaman web dengan jalur *dial-up* mungkin memakan waktu beberapa menit, berbeda dengan tautan *broadband* yang hanya memakan waktu beberapa detik.

FIGURE 1.2
LANs and WANs

<p align="center">
  <img src="images/book-sams_teach_yourself_networking/figure-1.2.png" alt="gambar" width="580"/>
</p>

Istilah "broadband" bisa membingungkan. Sebenarnya, istilah ini mengacu pada spektrum frekuensi dengan pita frekuensi yang lebar, tetapi juga menggambarkan jaringan atau tautan komunikasi yang mengirim dan menerima data pada laju bit yang tinggi, seperti 4.000.000 bps. Jika delapan bit digunakan untuk membentuk sebuah karakter, seperti huruf A, tautan *broadband* ini dapat menampung 1/2 juta karakter alfabet per detik ($4.000.000/8 = 500.000$). Mudah dipahami mengapa *broadband* begitu populer.

WAN sering kali merupakan jaringan publik. Artinya, jaringan tersebut tersedia bagi siapa saja yang ingin menggunakannya dan membayar untuk penggunaannya. Sistem telepon adalah fasilitas jaringan publik WAN. Begitu juga dengan Internet. Beberapa WAN adalah jaringan privat, yang dimiliki dan dioperasikan oleh perusahaan atau entitas lain. Contoh WAN privat adalah jaringan ATM sebuah bank. Biasanya, bank menyewa tautan komunikasi dari operator komunikasi, seperti AT&T, dan kemudian memasang mesin ATM dan *router* miliknya sendiri, mengkonfigurasinya untuk kebutuhan unik mereka. Sebagai nasabah bank, kita bisa menggunakan jaringan ATM, tetapi kita tidak bisa menghubungkan komputer kita ke dalamnya. Dalam hal ini, ini adalah jaringan privat.

### Contoh Topologi Jaringan, LAN, dan WAN

Sejauh mungkin, kami telah menghindari penggunaan jargon untuk menggambarkan topologi jaringan. Mungkin akan membantu untuk mengasosiasikan nama-nama spesifik dengan topologi-topologi ini, tetapi Anda dapat melewati bagian ini jika Anda mau. Berikut adalah daftar jaringan komputer umum dan topologi terkaitnya; semuanya akan dibahas pada jam-jam berikutnya:

* **Jaringan Bintang (*Star*)**—Switched Ethernet (LAN); Asynchronous Transfer Mode (ATM) (LAN atau WAN); Frame Relay (WAN); Internet (WAN); Synchronous Optical Network (SONET) (WAN)
* **Jaringan Cincin (*Ring*)**—Token Ring (LAN); IBM Token Ring (LAN); Fiber Distributed Data Interface (FDDI) (LAN); Synchronous Optical Network (SONET) (WAN)
* **Jaringan Bus**—Ethernet Bus (LAN); Token Bus (LAN)
* **Jaringan Seluler (*Cellular*)**—Jaringan ponsel (WAN); Bluetooth (LAN); Wi-Fi (LAN)

### Bagaimana Internet Berhubungan dengan Jaringan Anda

Jaringan data yang paling banyak digunakan di dunia adalah Internet, yang merupakan sebuah WAN publik. Kita mendapatkan akses ke sana dengan membayar biaya bulanan kepada **penyedia layanan Internet (*Internet service provider* atau ISP)** seperti AOL atau Verizon. Antarmuka kita dengan ISP adalah melalui tautan *dial-up* atau koneksi *broadband*. Para ISP memiliki perjanjian kontraktual satu sama lain untuk tujuan pertukaran lalu lintas dengan pelanggan mereka masing-masing.

Internet berawal dari upaya rintisan Departemen Pertahanan AS. Selama tahun 1960-an, **Advanced Research Projects Agency (ARPA)** ditugaskan untuk menciptakan jaringan pemerintah untuk memfasilitasi pertukaran informasi antara berbagai lembaga dan universitas. Akhirnya, ARPANET berevolusi menjadi Internet saat ini. Jaringan luar biasa ini terdiri dari jutaan jaringan yang terhubung, seperti LAN di rumah atau kantor Anda. Menurut `www.internetworldstats.com/stats.htm`, 1,5 miliar orang sekarang menggunakan Internet (kadang-kadang disingkat Net).

Para ISP mengelola bagian Internet mereka masing-masing dengan *router*, *server*, dan *firewall* dan memainkan peran penting dalam memberitahukan jaringan dan penyedia lain tentang pelanggan mereka. Prosedur ini sangat sederhana. Sebuah ISP "mengiklankan" pelanggannya ke Internet dengan mengirimkan informasi. Sebagai contoh, sebuah paket, yang dikirim ke hampir semua ISP di dunia, menyatakan, "Uyless Black dapat dihubungi melalui saya." Dengan melakukan itu, ISP mengiklankan nama saya (seperti UylessBlack.com) dan sebuah alamat untuk mencapai saya (seperti ID jaringan dan ID pengguna akhir).

> **Tahukah Anda?**
>
> **Alamat Email Bukanlah sebuah Alamat**
>
> Ketika kita berkata, "Kirimkan saya alamat email Anda," kita tidak bermaksud seperti yang kita katakan. Yang kita sebut alamat email sebenarnya adalah **nama email**. Salah satu milik saya adalah UylessBlack.com. Tugas ISP adalah menghubungkan nama ini menjadi sebuah alamat yang dapat dirutekan. Kemungkinan Anda pernah menemukan alamat Internet. Mungkin terlihat seperti `192.99.3.4`, misalnya. Alamat Internet secara konsep mirip dengan alamat pos (jalan, kota, negara bagian, dan kode pos) dan dijelaskan dalam Jam ke-3, "Mengirim Data dari Sini ke Sana: Cara Kerja Jaringan."

### Menghubungkan ke Internet

Hingga beberapa tahun yang lalu, metode yang umum untuk terhubung ke Internet adalah melalui **POTS (*plain old telephone services* atau layanan telepon biasa)**. Koneksi *dial-up* ini masih populer, tetapi kapasitasnya terbatas. Semakin banyak pengguna Internet beralih ke layanan *broadband* yang disediakan oleh perusahaan telepon dan TV kabel, serta perusahaan satelit dan seluler.

Gambar 1.3 menunjukkan contoh sebuah mesin yang dapat menghubungkan komputer pengguna ke Internet. Mesin ini disebut dengan berbagai nama karena menyediakan banyak layanan. Pertama, ini adalah sebuah **modem**. Sebuah modem (dari **modulator/demodulator**) menyediakan transmisi fisik untuk koneksi, seperti tegangan dan frekuensi. Kedua, ia bertindak sebagai **firewall**; yaitu, ia mencoba memblokir pengunjung yang tidak diinginkan agar tidak menyusup ke komputer dan file pengguna. Ketiga, ia melakukan fungsi **router**. Sebagai contoh, mesin ini dapat mendukung sesi Internet beberapa komputer dengan komputer jarak jauh maupun lokal. Ia "merutekan" lalu lintas bolak-balik dengan memeriksa alamat di setiap paket. Keempat, ini adalah mesin **nirkabel (seluler)**. Antena dan komponen terkait di dalam mesin mengirim dan menerima lalu lintas di dalam sebuah LAN—dalam situasi ini, rumah atau kantor kita.

FIGURE 1.3
A router and
attached links

<p align="center">
  <img src="images/book-sams_teach_yourself_networking/figure-1.3.png" alt="gambar" width="580"/>
</p>

### Mengapa Internet Itu Penting

Dengan risiko menyatakan hal yang sudah jelas, Internet telah mengubah cara kita berbisnis. Sebelum kemunculannya, cukup sulit untuk mentransfer data dari satu komputer ke komputer lain—kecuali jika komputer tersebut patuh dan menggunakan prosedur proprietary yang sama dengan mesin pengirim. Sebagai contoh, IBM memasarkan rangkaian protokolnya sendiri, begitu pula vendor lain. Tak satu pun dari mereka dapat berkomunikasi satu sama lain. Industri komunikasi data beroperasi dalam Menara Babel. Industri ini menderita masalah kompatibilitas yang serius, yang mengakibatkan hilangnya produktivitas.

Patut diakui, banyak organisasi internasional memiliki standar yang digunakan oleh vendor perangkat keras dan perangkat lunak. Standar modem dan faks, yang diterbitkan oleh **International Telecommunications Union (ITU)**, diadaptasi oleh semua produsen modem dan faks. Tetapi ini tidak terjadi pada protokol komunikasi data. Sebagai contoh, protokol **Open Systems Interconnection (OSI)** dari ITU tidak pernah populer. Protokol OSI menderita karena kerumitan yang tidak perlu dan dari fakta bahwa standar (dokumen-dokumennya) "dimiliki" oleh ITU. Namun, seperti yang dibahas pada Jam ke-3, model OSI itu sendiri masih banyak digunakan dan dikutip oleh industri.

Sebaliknya, protokol Internet dirancang untuk kesederhanaan. Terlebih lagi, protokol-protokol tersebut "terbuka." Siapa pun dapat menggunakan spesifikasi Internet tanpa membayar sepeser pun. Standar-standar ini dikodifikasikan dalam **Request for Comments (RFCs)**. RFC adalah Kitab Suci-nya Internet dan landasan dari jaringan komunikasi data.

Nantinya kita akan membahas beberapa protokol komunikasi data Internet. Saya menduga Anda sudah sering menjumpai banyak di antaranya. Apakah TCP/IP terdengar akrab? Anda mungkin tidak tahu, tetapi protokol komunikasi ini berjalan di komputer Anda setiap kali Anda masuk ke Internet. Kita tidak akan mendahului pembahasan tetapi akan kembali ke topik Internet beberapa kali dalam buku ini.

### Intranet, Ekstranet, dan internet

**Internet** (huruf I kapital) adalah jaringan publik yang kita gunakan untuk mengirim email dan menjelajahi Web. Jika kita menggunakan protokol Internet (seperti TCP/IP) dalam sebuah jaringan privat, kita telah menciptakan sebuah **internet** (perhatikan huruf i kecil). Beberapa vendor dan literatur terkait menggunakan istilah **intranet** untuk menggambarkan sebuah jaringan privat yang menggunakan protokol Internet. (Istilah lain adalah **ekstranet**.)

Saat ini, banyak bisnis menggunakan Internet untuk menghubungkan internet mereka dengan pelanggan, pemasok, dan mitra bisnis mereka. Ketika diimplementasikan dengan langkah-langkah keamanan yang tepat, asosiasi Internet-internet memberikan nilai yang luar biasa bagi sebuah organisasi. Mereka secara dramatis mengurangi biaya "melakukan" jejaring (*networking*). Standar Internet yang terbuka dan tidak berhak cipta telah menjadi berkah teknis dan finansial yang luar biasa bagi industri komunikasi data dan bagi dunia kita yang terhubung. **Jaringan privat virtual (*virtual private network*)**, yang diperkenalkan sebelumnya, ada berkat Internet.

### Ringkasan

Dalam jam ini, kita telah mempelajari tentang apa itu jaringan komputer dan bagaimana cara kerjanya. Kita juga telah sedikit mengenal tentang bit, *bandwidth*, dan bit per detik (bps). Kita telah menjelajahi topologi jaringan, jaringan area lokal dan area luas, serta Internet dan internet.

---


