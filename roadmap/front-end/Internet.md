# Belajar Sekilas Internet
## apa itu internet
Internet adalah kumpulan jaringan yang luas, dimana semuanya terhubung satu sama lain. Berkat komputer yang terhubung ke dalam jaringan, jaringan tersebut juga terhubung satu sama lain². Cara kerja internet apabila dijelaskan secara sederhana adalah proses menyalurkan informasi-informasi tersebut melalui router dengan menggunakan protokol TCP/IP antar komputer yang terhubung dalam jaringan global¹.
## Cara kerja Internet
Ketika Anda mengetikkan alamat situs web di browser Anda, browser mengirim permintaan ke server DNS untuk menerjemahkan alamat tersebut menjadi alamat IP. Setelah mendapatkan alamat IP, browser kemudian mengirim permintaan ke server yang memiliki alamat IP tersebut untuk mengambil halaman web yang diminta.
Server kemudian merespons dengan mengirimkan data halaman web kembali ke komputer Anda melalui ISP Anda. Data tersebut kemudian ditampilkan di browser Anda sebagai halaman web.
Proses ini terjadi setiap kali Anda mengakses halaman web di internet. Semua data yang dikirimkan antara komputer Anda dan server di internet dikirimkan dalam bentuk paket data melalui protokol TCP/IP.
## apa itu IP
IP adalah singkatan dari Internet Protocol. IP adalah protokol yang digunakan untuk mengirim data melalui internet. Setiap perangkat yang terhubung ke internet memiliki alamat IP yang unik, yang digunakan untuk mengidentifikasi perangkat tersebut di internet.

Alamat IP terdiri dari empat blok angka yang dipisahkan oleh titik, seperti 192.168.1.1. Setiap blok angka dapat berkisar dari 0 hingga 255.

Ketika Anda mengakses sebuah situs web, browser Anda mengirim permintaan ke server DNS untuk menerjemahkan nama domain situs web menjadi alamat IP. Setelah mendapatkan alamat IP, browser kemudian mengirim permintaan ke server yang memiliki alamat IP tersebut untuk mengambil halaman web yang diminta.

## TCP/IP
TCP/IP adalah singkatan dari Transmission Control Protocol/Internet Protocol. Seperti namanya, TCP/IP merupakan sebuah protokol standar dalam jaringan komputer untuk menjembatani pertukaran data antar perangkat dalam jaringan tersebut. Tugas TCP/IP adalah untuk mengatur bagaimana semua pengguna bisa saling mengirim dan menerima data dengan tepat dan aman dalam jaringan komputer atau internet².

Cara kerja protokol TCP/IP dimulai ketika pengguna internet mengirimkan teks atau data lainnya ke perangkat tujuan. TCP membagi teks menjadi beberapa paket data kecil, kemudian menambah beberapa informasi agar datanya tetap aman hingga sampai ke perangkat tujuan. Setiap paket kecil tersebut dikirimkan kepada tujuan yang sama, tetapi menggunakan jalur komunikasi yang berbeda¹.
## UDP
UDP adalah singkatan dari User Datagram Protocol. UDP adalah salah satu protokol yang menjadi lapisan transport TCP/IP yang mendukung atau memungkinkan terjadinya komunikasi yang tidak andal (unreliable), tanpa adanya koneksi antar host jaringan yang menggunakan TCP/IP².

Cara kerja UDP menyederhanakan pengiriman data dengan mengirimkan paket yang disebut datagram ke komputer target. UDP tidak mengindikasi perintah transmisi untuk datagram tersebut serta tidak mengkonfirmasi proses penerimaannya³.

## UDP vs TCP/IP
TCP (Transmission Control Protocol) dan UDP (User Datagram Protocol) adalah dua protokol yang digunakan untuk mengirim data melalui internet. Keduanya merupakan bagian dari keluarga protokol internet (TCP/IP), tetapi mereka memiliki perbedaan dalam cara mereka mengirim data.

TCP adalah protokol yang berorientasi koneksi, yang berarti bahwa ia menjamin pengiriman data yang andal dan teratur. Ketika Anda mengirim data menggunakan TCP, data tersebut dibagi menjadi beberapa paket dan dikirimkan satu per satu ke tujuan. Setiap paket diberi nomor urut, sehingga penerima dapat merakit kembali paket-paket tersebut dalam urutan yang benar. Jika salah satu paket hilang atau rusak selama pengiriman, penerima akan meminta pengirim untuk mengirim ulang paket tersebut.

UDP, di sisi lain, adalah protokol yang tidak berorientasi koneksi, yang berarti bahwa ia tidak menjamin pengiriman data yang andal atau teratur. Ketika Anda mengirim data menggunakan UDP, data tersebut dikirim sebagai satu paket tunggal, tanpa ada pengecekan apakah paket tersebut telah diterima dengan benar atau tidak. Jika paket hilang atau rusak selama pengiriman, tidak ada mekanisme untuk meminta pengirim untuk mengirim ulang paket tersebut.

Karena sifatnya yang tidak menjamin pengiriman data yang andal, UDP biasanya digunakan untuk aplikasi yang membutuhkan kecepatan tinggi dan dapat mentolerir kehilangan beberapa data, seperti streaming video atau audio. Sementara itu, TCP lebih cocok untuk aplikasi yang membutuhkan pengiriman data yang andal, seperti transfer file atau email.

## Website
Web adalah sistem yang memungkinkan Anda untuk mengakses informasi di internet melalui halaman web. Halaman web adalah dokumen yang dibuat dengan menggunakan bahasa markup seperti HTML, yang dapat menampilkan teks, gambar, video, dan elemen interaktif lainnya.

Ketika Anda mengetikkan alamat situs web di browser Anda dan menekan enter, browser mengirim permintaan ke server web yang menyimpan halaman web tersebut. Server kemudian merespons dengan mengirimkan data halaman web kembali ke browser Anda. Data tersebut kemudian ditampilkan di browser Anda sebagai halaman web.

Halaman web dapat berisi tautan ke halaman web lainnya, yang memungkinkan Anda untuk menavigasi dari satu halaman ke halaman lainnya dengan mudah. Halaman web juga dapat berisi formulir yang memungkinkan Anda untuk mengirimkan informasi ke server, seperti saat Anda melakukan pencarian di mesin pencari atau mengisi formulir pendaftaran.

Web bekerja dengan menggunakan protokol HTTP (Hypertext Transfer Protocol) untuk mentransfer data antara browser dan server. HTTP adalah protokol yang digunakan untuk mengirim permintaan dari browser ke server dan menerima respons dari server.
## HTTP
HTTP (Hypertext Transfer Protocol) adalah protokol yang digunakan untuk mentransfer data antara browser dan server di web. Protokol ini bekerja dengan menggunakan sistem permintaan dan respons.

Ketika Anda mengetikkan alamat situs web di browser Anda dan menekan enter, browser mengirim permintaan HTTP ke server yang menyimpan halaman web tersebut. Permintaan ini berisi informasi tentang halaman web yang ingin Anda akses, serta informasi lainnya seperti jenis browser yang Anda gunakan dan preferensi bahasa Anda.

Setelah menerima permintaan HTTP dari browser, server kemudian memproses permintaan tersebut dan mengirimkan respons kembali ke browser. Respons ini berisi data halaman web yang diminta, serta informasi lainnya seperti status respons (misalnya, apakah halaman berhasil dimuat atau tidak) dan tipe konten yang dikirimkan (misalnya, teks/html untuk halaman web).

Browser kemudian memproses respons dari server dan menampilkan data halaman web di layar Anda. Jika halaman web berisi elemen interaktif seperti formulir atau tautan, browser juga akan memproses elemen-elemen tersebut sehingga Anda dapat berinteraksi dengan halaman tersebut.

HTTP adalah protokol yang tidak berorientasi koneksi, yang berarti bahwa setiap permintaan dan respons diperlakukan sebagai transaksi yang terpisah. Setelah server mengirimkan respons ke browser, koneksi antara keduanya ditutup. Jika Anda mengklik tautan di halaman web untuk mengakses halaman lainnya, browser akan membuka koneksi baru dengan server untuk mengirim permintaan baru.

## lalu apa bedanya dengan HTTPS
HTTPS (Hypertext Transfer Protocol Secure) adalah versi yang lebih aman dari protokol HTTP. HTTPS menggunakan enkripsi untuk mengamankan data yang dikirimkan antara browser dan server, sehingga informasi yang Anda kirimkan melalui web (seperti kata sandi atau informasi kartu kredit) tidak dapat dibaca oleh pihak ketiga yang tidak berwenang.

Ketika Anda mengakses situs web yang menggunakan HTTPS, browser Anda akan memulai proses yang disebut "handshake" dengan server. Selama proses ini, browser dan server akan menegosiasikan parameter keamanan dan bertukar kunci enkripsi untuk mengamankan komunikasi antara keduanya.

Setelah handshake selesai, browser dan server dapat mengirim data satu sama lain dengan aman menggunakan enkripsi. Data yang dikirimkan antara keduanya tidak dapat dibaca oleh pihak ketiga yang tidak berwenang, bahkan jika mereka berhasil mencegat data tersebut.

Selain menyediakan keamanan tambahan, HTTPS juga dapat membantu memastikan bahwa Anda terhubung ke situs web yang benar dan bukan situs phishing yang meniru situs asli. Situs web yang menggunakan HTTPS harus memiliki sertifikat SSL (Secure Sockets Layer) yang valid, yang menunjukkan bahwa situs tersebut adalah situs yang sah dan bukan situs phishing.

## DNS
DNS (Domain Name System) adalah sistem yang digunakan untuk menerjemahkan nama domain menjadi alamat IP. Nama domain adalah alamat yang mudah diingat untuk situs web, seperti "google.com". Alamat IP, di sisi lain, adalah alamat numerik yang digunakan oleh komputer untuk mengidentifikasi satu sama lain di internet.

Ketika Anda mengetikkan nama domain di browser Anda dan menekan enter, browser mengirim permintaan ke server DNS untuk menerjemahkan nama domain tersebut menjadi alamat IP. Setelah mendapatkan alamat IP, browser kemudian mengirim permintaan ke server yang memiliki alamat IP tersebut untuk mengambil halaman web yang diminta.

Server DNS adalah komputer khusus yang menyimpan database nama domain dan alamat IP yang terkait. Ketika server DNS menerima permintaan untuk menerjemahkan nama domain, ia akan mencari nama domain tersebut di database-nya. Jika ditemukan, server akan mengirimkan alamat IP yang terkait kembali ke browser.

DNS memungkinkan Anda untuk menggunakan nama domain yang mudah diingat untuk mengakses situs web, daripada harus mengingat alamat IP yang sulit diingat. Tanpa DNS, Anda harus mengetikkan alamat IP secara langsung di browser untuk mengakses situs web.

## Domain Name
Domain name adalah alamat yang mudah diingat untuk situs web, seperti "google.com". Domain name memungkinkan pengguna untuk mengakses situs web tanpa harus mengingat alamat IP yang sulit diingat.

Domain name terdiri dari dua bagian: nama domain dan ekstensi domain. Nama domain adalah bagian yang unik, seperti "google" dalam contoh di atas. Ekstensi domain adalah bagian akhir dari domain name yang menunjukkan jenis situs web, seperti ".com" untuk situs web komersial.

Domain name bekerja dengan menggunakan sistem DNS (Domain Name System) untuk menerjemahkan nama domain menjadi alamat IP. Ketika Anda mengetikkan nama domain di browser Anda dan menekan enter, browser mengirim permintaan ke server DNS untuk menerjemahkan nama domain tersebut menjadi alamat IP. Setelah mendapatkan alamat IP, browser kemudian mengirim permintaan ke server yang memiliki alamat IP tersebut untuk mengambil halaman web yang diminta.

Perbedaan antara domain name dan DNS adalah bahwa domain name adalah alamat yang mudah diingat untuk situs web, sedangkan DNS adalah sistem yang digunakan untuk menerjemahkan nama domain menjadi alamat IP. Domain name memungkinkan pengguna untuk mengakses situs web dengan mudah, sedangkan DNS memungkinkan browser untuk menemukan server yang menyimpan halaman web tersebut.
## Hosting
Hosting adalah layanan yang memungkinkan individu atau organisasi untuk menyimpan dan menjalankan situs web di internet. Hosting menyediakan ruang di server untuk menyimpan file-file situs web, serta teknologi dan layanan yang diperlukan untuk menjalankan situs web.

Ketika Anda membuat situs web, Anda harus mengunggah file-file situs web ke server hosting. Server hosting kemudian akan menjalankan situs web Anda dan membuatnya dapat diakses oleh pengguna di internet.

Ada banyak perusahaan yang menawarkan layanan hosting, dengan berbagai pilihan paket dan fitur yang berbeda. Beberapa contoh perusahaan hosting yang populer adalah Bluehost, HostGator, dan GoDaddy.

Pemilihan hosting yang tepat tergantung pada kebutuhan situs web Anda. Faktor-faktor yang perlu dipertimbangkan saat memilih hosting antara lain kapasitas penyimpanan, bandwidth, keandalan, dukungan pelanggan, dan harga.

## browser
Browser adalah perangkat lunak yang digunakan untuk mengakses dan menampilkan halaman web di internet. Beberapa contoh browser yang populer adalah Google Chrome, Mozilla Firefox, dan Microsoft Edge.

Ketika Anda mengetikkan alamat situs web di browser dan menekan enter, browser akan mengirim permintaan ke server web yang menyimpan halaman web tersebut. Server kemudian merespons dengan mengirimkan data halaman web kembali ke browser. Data tersebut kemudian ditampilkan di browser sebagai halaman web.

Browser juga bertanggung jawab untuk menafsirkan kode HTML, CSS, dan JavaScript yang digunakan untuk membuat halaman web. Kode-kode ini memberi tahu browser bagaimana menampilkan teks, gambar, dan elemen lainnya di halaman web. Browser juga dapat menjalankan kode JavaScript untuk menambahkan interaktivitas ke halaman web.

Web menggunakan browser karena browser menyediakan antarmuka yang mudah digunakan untuk mengakses dan menampilkan halaman web. Tanpa browser, Anda harus menggunakan perangkat lunak lain yang lebih rumit untuk mengakses dan menampilkan halaman web.

Standar untuk web dan browser dikembangkan oleh organisasi-organisasi seperti World Wide Web Consortium (W3C) dan Internet Engineering Task Force (IETF). Organisasi-organisasi ini terdiri dari para ahli dari seluruh dunia yang bekerja sama untuk mengembangkan standar yang memungkinkan web berfungsi dengan baik.

## Memilih Hosting
Ada beberapa tipe hosting yang umum digunakan, antara lain:

1. Shared Hosting: Shared hosting adalah tipe hosting di mana beberapa situs web berbagi satu server dan sumber daya server. Kelebihan shared hosting adalah harganya yang terjangkau, menjadikannya pilihan yang baik untuk situs web kecil atau baru. Namun, kekurangannya adalah bahwa kinerja situs web Anda dapat dipengaruhi oleh situs web lain yang berbagi server yang sama.

2. Virtual Private Server (VPS) Hosting: VPS hosting adalah tipe hosting di mana setiap situs web memiliki sumber daya server yang terpisah, tetapi masih berbagi satu server fisik dengan situs web lain. Kelebihan VPS hosting adalah bahwa Anda memiliki kontrol lebih besar atas sumber daya server dan kinerja situs web Anda tidak akan dipengaruhi oleh situs web lain. Namun, harganya lebih mahal daripada shared hosting.

3. Dedicated Hosting: Dedicated hosting adalah tipe hosting di mana Anda menyewa seluruh server untuk situs web Anda sendiri. Kelebihan dedicated hosting adalah bahwa Anda memiliki kontrol penuh atas server dan sumber daya server, serta kinerja yang optimal untuk situs web Anda. Namun, harganya jauh lebih mahal daripada shared atau VPS hosting.

4. Cloud Hosting: Cloud hosting adalah tipe hosting di mana situs web Anda dijalankan di sekelompok server yang terhubung melalui jaringan cloud. Kelebihan cloud hosting adalah skalabilitas yang tinggi, karena Anda dapat menambah atau mengurangi sumber daya server sesuai dengan kebutuhan. Namun, harganya bisa bervariasi tergantung pada penggunaan sumber daya.

Pemilihan tipe hosting yang tepat tergantung pada kebutuhan dan anggaran situs web Anda. Shared hosting cocok untuk situs web kecil atau baru dengan lalu lintas rendah, sedangkan VPS atau dedicated hosting cocok untuk situs web yang lebih besar dengan lalu lintas tinggi. Cloud hosting bisa menjadi pilihan yang baik untuk situs web dengan lalu lintas yang bervariasi atau tidak dapat diprediksi.

## free hosting untul uji coba atau portfolio
Tentu saja, berikut adalah beberapa penyedia hosting gratis yang dapat digunakan oleh developer untuk menguji coba atau menampilkan portfolio mereka tanpa harus mengeluarkan biaya:

1. GitHub Pages: GitHub Pages memungkinkan Anda untuk meng-host situs web statis secara gratis menggunakan repositori GitHub Anda. Layanan ini cocok untuk menampilkan portfolio atau proyek-proyek open source.

2. Netlify: Netlify adalah platform yang memungkinkan Anda untuk meng-host situs web statis dan aplikasi web secara gratis. Layanan ini menawarkan fitur-fitur canggih seperti integrasi dengan sistem kontrol versi dan dukungan untuk berbagai kerangka kerja front-end.

3. Vercel: Vercel adalah platform yang memungkinkan Anda untuk meng-host situs web statis dan aplikasi web secara gratis. Layanan ini menawarkan fitur-fitur canggih seperti integrasi dengan sistem kontrol versi, dukungan untuk berbagai kerangka kerja front-end, dan fungsi serverless.

4. Supabase: Supabase adalah platform yang memungkinkan Anda untuk meng-host aplikasi web secara gratis dengan fitur-fitur canggih seperti database real-time, penyimpanan file, dan autentikasi pengguna.

5. AWS dan GCP: Amazon Web Services (AWS) dan Google Cloud Platform (GCP) adalah platform cloud yang menawarkan free tier untuk beberapa layanan mereka. Ini memungkinkan Anda untuk meng-host aplikasi web secara gratis dengan batasan tertentu.

Namun, perlu diingat bahwa layanan hosting gratis biasanya memiliki batasan tertentu, seperti kapasitas penyimpanan yang terbatas atau lalu lintas yang dibatasi. Jika situs web Anda berkembang dan membutuhkan sumber daya yang lebih besar, Anda mungkin perlu beralih ke layanan hosting berbayar.

## dibalik browser
Beberapa teknologi browser yang umum digunakan adalah:

- **JavaScript**: Perangkat lunak yang bertanggung jawab untuk mengeksekusi kode JavaScript di halaman web. Contoh mesin JavaScript adalah V8 (Chrome), SpiderMonkey (Firefox), Chakra (Edge), dan Nitro (Safari).
- **CSS**: Perangkat lunak yang bertanggung jawab untuk mengurai dan menerapkan gaya CSS ke elemen HTML di halaman web. Contoh mesin CSS adalah Blink (Chrome), Gecko (Firefox), EdgeHTML (Edge), dan WebKit (Safari).
- **Image processor**: Perangkat lunak yang bertanggung jawab untuk memuat, menampilkan, dan memanipulasi gambar di halaman web. Contoh image processor adalah Skia (Chrome), Cairo (Firefox), Direct2D (Edge), dan Core Graphics (Safari).
- **layout**: Perangkat lunak yang bertanggung jawab untuk menghitung posisi dan ukuran elemen HTML di halaman web. Contoh mesin layout adalah Blink (Chrome), Gecko (Firefox), EdgeHTML (Edge), dan WebKit (Safari).
- **rendering**: Perangkat lunak yang bertanggung jawab untuk menggambar elemen HTML ke layar perangkat. Contoh mesin rendering adalah Blink (Chrome), Gecko (Firefox), EdgeHTML (Edge), dan WebKit (Safari).


source :
- bing ai
- Memahami Perbedaan Antara TCP & UDP - Ara-Gen Riset. https://www.ara-genriset.com/2021/12/memahami-perbedaan-antara-tcp-udp.html.
- Kapan tepat menggunakan UDP dan bukan TCP? [Tutup] - QA Stack. https://qastack.id/programming/1099672/when-is-it-appropriate-to-use-udp-instead-of-tcp.
- Perbedaan UDP dan TCP | NordVPN. https://nordvpn.com/id/blog/perbedaan-udp-dan-tcp/.
- Mengenal Perbedaan UDP dan TCP dalam Jaringan Komputer. https://qwords.com/blog/perbedaan-udp-dan-tcp/.
- Pengertian dan Cara Kerja UDP (User Datagram Protocol). https://qwords.com/blog/udp-adalah/.
- UDP - Pengertian, Cara Kerja, dan Penggunaannya - Teknogram. https://teknogram.id/kamus/udp/.
- Pengertian, Fungsi dan Cara Kerja Protokol TCP/UDP. https://lamnesia.com/pengertian-fungsi-dan-cara-kerja-protokol-tcp-udp/.
- BAKTI - Mengenal Tentang UDP: Pengertian, Fungsi, Cara Kerja, serta .... https://baktikominfo.id/en/informasi/pengetahuan/mengenal_tentang_udp_pengertian_fungsi_cara_kerja_serta_kelebihan_dan_kelemahannya-697.
- Apa Itu TCP/IP? Fungsi, Layer, dan Cara Kerjanya - IDCloudHost. https://idcloudhost.com/panduan/protokol-jaringan-tcp-ip/.
- Apa itu TCP/IP dan Cara Kerjanya - Cloudmatika. https://cloudmatika.co.id/blog-detail/apa-itu-tcp-ip.
- TCP/IP: Pengertian, Cara Kerja, Fungsi, Layer & Keuntungannya - Qwords. https://qwords.com/blog/pengertian-jaringan-tcp-ip/.
- Apa Itu Internet dan Bagaimana Cara Kerjanya? - IDN Times. https://www.idntimes.com/tech/trend/andri-andreas-1/apa-itu-internet-c1c2.
- Bagaimana sih Cara Kerja Internet - Asaljeplak.com. https://asaljeplak.com/internet/cara-kerja-internet/.
- Bagaimana Internet Bekerja? - Penjelasan Simple Cara Kerja Internet. https://www.nadagitar.net/2020/12/bagaimana-internet-bekerja-penjelasan.html.
- Pengertian Internet, Cara Kerja & Cara Mengaksesnya | MORHANS. https://morhans.com/pengertian-internet-dan-cara-kerjanya/.
- 10+ Web Browser Terbaik & Tercepat yang Bisa Anda Coba - Niagahoster. https://www.niagahoster.co.id/blog/browser-terbaik/.
- Web Browser Adalah: Pengertian, Fungsi, Cara Kerja, Jenisnya - Niagahoster. https://www.niagahoster.co.id/blog/apa-itu-web-browser/.
- Web Browser: Pengertian, Fungsi, dan Jenisnya - Dewaweb. https://www.dewaweb.com/blog/apa-itu-web-browser/.
