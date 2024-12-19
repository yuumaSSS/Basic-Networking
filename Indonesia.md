# Networking (Indonesia)
"Jaringan itu seperti komunikasi antar-tetangga yang memiliki banyak rasa. Terkadang harmonis, bahagia, dan damai. Tetapi bisa juga menjadi sumber kericuhan dan kegaduhan karena perasaan iri dan dengki sebagai sumber awalnya."

+yuumaSSS+

## Model OSI
Model OSI (Open Systems Interconnection) adalah model jaringan teoretis-konseptual komunikasi antara perangkat melalui jaringan. Tidak ada implementasi praktis dari model OSI, akan tetapi model OSI berguna untuk memahami bagaimana aplikasi dapat bekerja melalui jaringan.

Model OSI memiliki 7 layer yang menggambarkan bagaimana perangkat berkomunikasi. Dari sisi pengirim, data akan berjalan dari layer ketujuh sampai layer pertama. Lalu dari sisi penerima, data akan berjalan dari layer pertama ke layer ketujuh.

- Application layer (layer ke-7)

  Layer yang berinteraksi langsung dengan data dari pengguna. Pada layer ini, permintaan data akan disiapkan untuk  dikirim melalui jaringan. Layer ini berisi protokol, header, dan cookie.

- Presentation layer (layer ke-6)
  
  Layer yang mengonversi data agar sistem menggunakan format data yang berbeda tetap dapat bertukar informasi. Layer ini bertugas untuk misalnya encryption-decryption, compression-decompression, dan encoding-decoding.
  
- Session layer (layer ke-5)

  Layer yang bertanggung jawab membuka, menjaga, dan menutup session. Session adalah pertukaran informasi sementara dan interaktif antara dua atau lebih perangkat yang saling berkomunikasi. Layer ini membantu implementasi autentikasi, otorisasi, dan sinkronisasi bekerja dengan baik.

- Transport layer (layer ke-4)

  Layer yang memastikan data yang dikirim tidak corrupt (rusak), jika corrupt maka akan dikirm ulang. Layer ini memecah data menjadi bentuk kecil yang dinamakan segment. selain itu, layer ini mencatat source port dan destination port ke setiap segment. Protokol yang beroperasi adalah TCP dan UDP.

- Network layer (layer ke-3)

  Layer yang memecah segment menjadi bentuk lebih kecil lagi yang dinamakan packet. Pakcet memiliki dua bagian yaitu header (informasi packet) dan body (data). Header berisi informasi seperti IP address, ukuran total packet, indikasi apakah packet telah dipecah menjadi bagian yang lebih kecil lagi, dan hitungan berapa banyak jaringan yang telah dilalui packet. IP address sederhananya adalah alamat yang digunakan untuk mengidentifikasi koneksi komputer ke jaringan secara unik. IP address ibarat alamat rumah.

- Data link layer (layer ke-2)

  Layer yang memecah packet menjadi bentuk lebih kecil lagi yang dinamakan frame. Frame berisi informasi source MAC address dan destination MAC address. MAC address adalah pengidentifikasi unik yang tertanam dalam network card atau network interface control untuk digunakan sebagai alamat jaringan. MAC address ibarat data privasi rumah. Protokol yang umum dikenal di layer ini yaitu ethernet dan WiFi.

- Physical layer (layer ke-1)

  Layer yang melibatkan semua perangkat keras seperti router, kabel, dan switch. Layer ini mengubah frame menjadi aliran bit (boolean 1 dan 0) dan kemudian dikirim ke penerima atau menerima dari penerima.

## Model TCP/IP
Model TCP/IP (Transmission Control Protocol/Internet Protocol) adalah model jaringan komunikasi antara perangkat melalui jaringan yang menjadi standar komunitas internet saat ini. Model ini dinilai lebih praktis dan hanya memiliki 5 layer (Awalnya hanya memiliki 4 layer, tetapi link layer dipecah menjadi data link layer dan physical layer karena dinilai tidak efisien untuk teknologi saat ini).

Sama dengan model OSI, urutan dari sisi pengirim yaitu dari layer kelima sampai layer pertama. Sedangkan dari sisi penerima yaitu dari layer pertama sampai layer kelima.

- Application layer (layer ke-5)

  Layer yang menggambungkan sebagian besar fungsi presentation layer dan session layer dari model OSI. 

- Transport layer (layer ke-4)

  Sama seperi penjelasan pada model OSI.

- Network layer (layer ke-3)

  Sama seperti penjelasan pada model OSI.

- Data link layer (layer ke-2)

  Sama seperti penjelasan pada model OSI.

- Physical layer (layer ke-1)

  Sama seperti penjelasan pada model OSI.

Untuk memahami lebih sederhana dan mudah diingat, kamu bisa mengandaikannya seperti ini:
- Physical layer = Pesawat/Mobil/Motor/Sepeda POS (media pengantar paket) dan jalan raya
- Data link layer = Membantu pengantaran paket untuk berpindah dari satu persimpangan ke persimpangan berikutnya
- Network layer = Membantu navigasi pengantaran paket
- Transport layer = Memastikan alamat yang benar
- Application layer = Isi paket

## Protokol Jaringan Application Layer
- HTTP

  HTTP (Hypertext Transfer Protocol) digunakan untuk mentransfer data antarperangkat. Hypertext adalah sistem dokumentasi yang terkelola dengan baik menggunakan hyperlink untuk menghubungkan halaman-halaman dalam dokumen teks. HTTP adalah protokol stateless (tidak menyimpan histori informasi dari client).
  
- HTTPS

  Mirip seperti HTTP, tetapi HTTP tidak terenkripsi sehingga hacker bisa mencegat HTTP message dan membacanya. HTTPS (HTTP Secure) merupakan gabungan antara HTTP dan TLS. TLS (Transport Layer Security) adalah protokol yang digunakan untuk proses enkripsi pesan HTTP. TLS disebut juga SSL (Secure Sockets Layer).

- SMTP

  SMTP (Simple Mail Transfer Protocol) digunakan untuk mentransfer email dari suatu pengguna ke pengguna lainnya. Tugas ini dilakukan melalui email client software (Mail User Agent) yang digunakan pengguna. User Agent membantu pengguna untuk mengetik dan memformat email serta menyimpannya sampai internet tersedia. Ketika email dikirim, proses pengiriman akan ditangani oleh Message Transfer Agent yang biasanya disertakan dalam email client software. Message Transfer Agent menggunakan SMTP untuk meneruskan email ke Message Transfer Agent yang lain (sisi server).

- DNS

  DNS (Domain Name System) adalah sistem penamaan yang memetakan nama domain ke IP address. DNS berfungsi untuk memudahkan manusia menghafal nama domain ketimbang IP addressnya yang isinya hanya angka dan titik.

- FTP

  FTP (File Transfer Protocol) adalah sebuah protokol internet yang digunakan untuk mengirim file melalui jaringan dari satu komputer ke komputer lain.

- SSH

  SSH (Secure Shell) adalah sebuah protokol jaringan kriptografi untuk komunikasi data yang aman, login dan eksekusi perintah jarak jauh, serta layanan jaringan lainnya antara dua jaringan komputer.

## Protokol Jaringan Transport Layer
- TCP

  TCP (Transmission Control Protocol) adalah protokol yang connection-oriented yaitu berorientasi koneksi. TCP memastikan bisa membuat koneksi ke perangkat penerima jika memungkinkan. TCP memastikan packet sampai pada penerima, jika belum sampai TCP tidak akan memutus koneksi kecuali terjadi kesalahan yang tidak dapat dikendalikan. Pertukaran informasi pada TCP dinamakan three-way handshake yaitu pengirim mengirim segment SYN (Synchronize), lalu penerima mengembalikan segment SYN/ACK (Synchronize/Acknowledge), terakhir pengirim akan mengirim ACK pada penerima.

- UDP

  UDP (User Datagram Protocol) adalah protokol yang connectionless yaitu tidak berorientasi. UDP tidak memverifikasi koneksi antara komputer pengirim dan komputer penerima. Aplikasi yang menggunakan UDP memiliki prinsip fire and forget, artinya UDP tidak peduli apakah packet benar-benar sampai atau tidak. Akan tetapi, hal ini menguntungkan bagi aplikasi yang membutuhkan protokol cepat seperti aplikasi streaming.
