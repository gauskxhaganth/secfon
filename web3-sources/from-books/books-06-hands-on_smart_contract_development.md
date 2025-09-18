# BAGIAN I
## Pengantar Blockchain Ethereum

Buku ini berfokus secara spesifik untuk membantu Anda belajar mengembangkan *smart contract* di Ethereum. Fokus ini mengharuskan kita untuk membahas sebagian dari protokol Ethereum, bahasa pemrograman Solidity, dan Ethereum Virtual Machine. Untuk pemahaman yang lebih mendalam dan komprehensif tentang Ethereum, kami merekomendasikan buku *Mastering Ethereum* oleh Andreas M. Antonopoulos dan Gavin Wood. Meskipun begitu, agar dapat mengembangkan *smart contract* secara efektif, sangat penting bagi Anda untuk memahami konsep-konsep dasar *smart contract* tertentu. Kami akan membahas konsep-konsep tersebut dengan detail yang sekadarnya agar kita tidak membuang waktu dan Anda bisa segera masuk ke mode membangun (*builder mode*). Kami ingin Anda segera men-*deploy* *smart contract* pertama Anda sesegera mungkin. Kami tahu pendekatan ini adalah cara yang paling andal bagi orang-orang untuk mempelajari teknologi baru.

---

# BAB 1
## Konsep-Konsep Blockchain

Pada dasarnya, **blockchain** adalah sebuah struktur data. Ia adalah sebuah *linked list*, atau rantai, dari “blok-blok” yang unik. Setiap blok menunjuk ke blok sebelumnya, dan blok itu sendiri merupakan sebuah daftar transaksi. Di atas struktur data daftar-di-dalam-daftar yang relatif sederhana ini, diletakkan inovasi kunci yang diberikan oleh *blockchain*: sebuah protokol tentang bagaimana blok ditambahkan ke dalam rantai tanpa adanya otoritas pusat. Gambar 1-1 mengilustrasikan struktur ini.

*Cryptocurrency* yang muncul bersama *blockchain* adalah sarana untuk mencapai tujuan, yaitu menyediakan insentif bagi orang-orang untuk menjalankan perangkat lunak yang mengamankan jaringan. Untuk pertama kalinya dalam sejarah, kita memiliki kemampuan untuk berbagi informasi digital tanpa perlu mempercayai individu, pemerintah, organisasi, atau perusahaan mana pun untuk memfasilitasi interaksi tersebut. Ethereum menyediakan platform yang aman secara kriptografis untuk menyimpan, memperbarui, dan menghapus data dari *blockchain* menggunakan apa yang disebut sebagai “*smart contract*”. Kita masih berada di masa-masa awal dalam mempelajari cara menggunakan *smart contract* untuk memperbaiki berbagai hal di dunia nyata, dan sulit untuk memprediksi bagaimana teknologi ini akan digunakan di masa depan. Mirip dengan “World Wide Web” pada tahun 1990-an, telah terjadi gelombang global para pemecah masalah yang inspiratif dan kreatif yang bekerja setiap hari untuk men-*deploy* **aplikasi terdesentralisasi (DApps)** yang mereka harap akan “memberi dampak di alam semesta” (*make a dent in the universe*).

<p align="center">
  <img src="images/books-06-hands-on_smart_contract_development/figure-1.1.png" alt="gambar" width="580"/>
</p>

