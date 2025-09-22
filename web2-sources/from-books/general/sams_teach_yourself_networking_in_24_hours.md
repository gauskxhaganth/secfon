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

