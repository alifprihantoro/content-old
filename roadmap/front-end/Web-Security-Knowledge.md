## keamanan dalam web
Keamanan di dalam web adalah suatu hal yang sangat penting untuk melindungi data, server, dan fungsi situs web dari ancaman dan serangan yang bisa dilakukan oleh penjahat dunia maya atau hacker. Ada banyak cara untuk meningkatkan keamanan web, seperti:

- **Memperbarui perangkat lunak secara berkala**. Ini termasuk sistem operasi, CMS, plugin, dan dependensi perangkat lunak lainnya yang digunakan di situs web. Perbaruan perangkat lunak biasanya mengandung patch keamanan yang bisa menutup celah yang bisa dimanfaatkan oleh hacker²³.
- **Menggunakan HTTPS dengan SSL**. HTTPS adalah protokol yang mengenkripsi komunikasi antara browser dan server, sehingga data yang dikirim tidak bisa dibaca atau dimodifikasi oleh pihak ketiga. SSL adalah sertifikat yang memverifikasi identitas situs web dan memungkinkan penggunaan HTTPS. Dengan HTTPS dan SSL, situs web bisa menunjukkan bahwa mereka menganggap serius keamanan web dan melindungi privasi pengunjung².
- **Mencegah injeksi SQL dan serangan XSS**. Injeksi SQL adalah teknik yang memanfaatkan kelemahan di input data untuk mengeksekusi perintah SQL di database situs web. Serangan XSS adalah teknik yang memanfaatkan kelemahan di output data untuk menyisipkan skrip jahat di halaman situs web. Kedua teknik ini bisa menyebabkan kerusakan data, pencurian informasi, atau pengambilalihan sesi. Untuk mencegahnya, situs web harus melakukan validasi dan sanitasi data di sisi server dan klien, serta menggunakan parameterisasi query³.
- **Berhati-hati terhadap error message**. Error message adalah pesan yang ditampilkan ketika ada kesalahan di situs web, seperti halaman tidak ditemukan, koneksi gagal, atau input salah. Error message bisa memberikan informasi berguna bagi pengguna, tetapi juga bisa memberikan informasi sensitif bagi hacker, seperti detail database, lokasi file, atau versi perangkat lunak. Untuk itu, situs web harus menghindari menampilkan error message yang terlalu spesifik atau rinci, dan menggunakan pesan generik atau ramah pengguna³.
- **Melakukan perubahan kata sandi secara berkala**. Kata sandi adalah kunci untuk mengakses akun atau fitur tertentu di situs web, seperti panel admin, email, atau FTP. Kata sandi yang lemah atau tidak berubah bisa menjadi sasaran empuk bagi hacker yang ingin masuk ke dalam sistem. Untuk itu, situs web harus menggunakan kata sandi yang kuat dan unik, serta mengubahnya secara berkala³⁴.

## OWASP
OWASP adalah singkatan dari **Open Web Application Security Project**, yaitu sebuah organisasi nirlaba yang berfokus pada meningkatkan kesadaran dan pengetahuan tentang keamanan aplikasi web. OWASP menyediakan berbagai sumber daya yang bisa diakses secara gratis oleh siapa saja, seperti standar, dokumentasi, alat, proyek, dan komunitas¹.

Salah satu sumber daya yang paling terkenal dari OWASP adalah **OWASP Top 10**, yaitu sebuah dokumen yang menjelaskan sepuluh risiko keamanan aplikasi web paling kritis yang harus diperhatikan oleh pengembang dan praktisi keamanan. OWASP Top 10 dibuat berdasarkan konsensus luas dari para ahli keamanan di seluruh dunia, dan diperbarui secara berkala untuk mengikuti perkembangan teknologi dan ancaman².

OWASP Top 10 edisi 2021 adalah sebagai berikut²:

- A01:2021-Broken Access Control
- A02:2021-Cryptographic Failures
- A03:2021-Injection
- A04:2021-Insecure Design
- A05:2021-Security Misconfiguration
- A06:2021-Vulnerable and Outdated Components
- A07:2021-Identification and Authentication Failures
- A08:2021-Software and Data Integrity Failures
- A09:2021-Security Logging and Monitoring Failures
- A10:2021-Server-Side Request Forgery

Anda bisa membaca penjelasan lebih lengkap tentang masing-masing risiko, termasuk contoh, dampak, cara deteksi, dan cara pencegahan di situs web resmi [OWASP](https://owasp.org/Top10/id/).

### artikel yang membahas owasp 10 risk
Berikut adalah beberapa link artikel yang membahas 10 risiko OWASP secara mendalam:

- [OWASP Top 10 Risks and How to Prevent Them - Bright Security](https://brightsec.com/blog/owasp-top-10/). Artikel ini menjelaskan setiap risiko dengan contoh, dampak, dan cara pencegahan yang praktis dan mudah dipahami.
- [OWASP Top 10:2021](https://owasp.org/Top10/). Artikel ini adalah sumber resmi dari OWASP yang memberikan penjelasan singkat tentang setiap risiko, termasuk data, CWE, dan CVE yang terkait. Artikel ini juga tersedia dalam bahasa Indonesia⁴.
- [OWASP Top Ten | OWASP Foundation](https://owasp.org/www-project-top-ten/). Artikel ini adalah sumber resmi dari OWASP yang memberikan penjelasan lebih rinci tentang setiap risiko, termasuk contoh skenario serangan, cara deteksi, cara pencegahan, dan referensi tambahan³.

## CSP
Content Security Policy (CSP) adalah sebuah mekanisme keamanan tambahan yang membantu mendeteksi dan mencegah beberapa jenis serangan, seperti Cross-Site Scripting (XSS) dan data injection. Serangan-serangan ini bisa digunakan untuk mencuri data, merusak situs web, atau menyebarkan malware. CSP dirancang untuk kompatibel dengan browser yang tidak mendukungnya, dengan menggunakan standar same-origin policy untuk konten web¹.

Untuk mengaktifkan CSP, Anda perlu mengonfigurasi server web Anda untuk mengembalikan header HTTP Content-Security-Policy. Header ini berisi nilai-nilai yang mengontrol sumber daya apa saja yang boleh dimuat oleh user agent (browser) untuk halaman tertentu. Misalnya, Anda bisa menentukan domain-domain yang diizinkan untuk menyediakan skrip, gaya, gambar, font, dll. Anda juga bisa menentukan protokol yang diizinkan, seperti HTTPS.

Contoh header Content-Security-Policy:

```http
Content-Security-Policy: default-src 'self'; script-src 'self' https://example.com; style-src 'self' https://cdn.example.com; img-src 'self' data:; font-src 'self' https://cdn.example.com;
```

Header di atas berarti:

- Hanya sumber daya dari domain yang sama dengan halaman (`'self'`) yang boleh dimuat secara default.
- Hanya skrip dari domain yang sama dengan halaman atau https://example.com yang boleh dieksekusi.
- Hanya gaya dari domain yang sama dengan halaman atau https://cdn.example.com yang boleh diterapkan.
- Hanya gambar dari domain yang sama dengan halaman atau data URI (`data:`) yang boleh ditampilkan.
- Hanya font dari domain yang sama dengan halaman atau https://cdn.example.com yang boleh digunakan.

Anda bisa membaca lebih lanjut tentang sintaks dan direktif-direktif CSP [di sini](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP).

### link
- checklist : https://github.com/0xRadi/OWASP-Web-Checklist#Information
- cheatsheet : https://cheatsheetseries.owasp.org/cheatsheets/AJAX_Security_Cheat_Sheet.html
- zap step : https://youtube.com/playlist?list=PLH8n_ayg-60J9i3nsLybper-DR3zJw6Z5

## CORS
CORS (Cross-Origin Resource Sharing) adalah sebuah mekanisme yang memungkinkan sumber daya yang dibatasi pada sebuah halaman web untuk diakses dari domain lain selain domain yang menyediakan halaman tersebut. Sebuah halaman web bisa dengan bebas menyematkan sumber daya lintas asal, seperti gambar, gaya, skrip, iframe, dan video. Namun, permintaan HTTP tertentu yang berasal dari skrip, seperti XMLHttpRequest atau Fetch API, dibatasi oleh kebijakan same-origin untuk alasan keamanan. CORS menentukan cara di mana browser dan server bisa berinteraksi untuk menentukan apakah aman untuk mengizinkan permintaan lintas asal.

Untuk menerapkan CORS, server harus mengembalikan header HTTP Access-Control-Allow-Origin (ACAO) yang menunjukkan domain-domain mana yang diizinkan untuk mengakses sumber daya tersebut. Misalnya, jika server mengembalikan header berikut:

```http
Access-Control-Allow-Origin: https://example.com
```

Maka hanya permintaan dari https://example.com yang boleh mengakses sumber daya tersebut. Jika server mengembalikan header berikut:

```http
Access-Control-Allow-Origin: *
```

Maka semua permintaan dari domain manapun boleh mengakses sumber daya tersebut.

Selain itu, untuk permintaan HTTP yang bisa menyebabkan efek samping pada data server (seperti metode selain GET atau POST dengan tipe MIME tertentu), spesifikasi CORS mengharuskan browser untuk melakukan "preflight" request, yaitu permintaan dengan metode OPTIONS untuk meminta izin dari server sebelum mengirimkan permintaan sebenarnya. Dalam preflight request, browser mengirimkan header-header yang menunjukkan metode HTTP dan header-header yang akan digunakan dalam permintaan sebenarnya¹².

Anda bisa membaca lebih lanjut tentang sintaks dan proses CORS [di sini](https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS).

Source: 
- Conversation with Bing, 7/9/2023
- Content Security Policy (CSP) - HTTP | MDN - MDN Web Docs. https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP.
- Content-Security-Policy (CSP) Header Quick Reference. https://content-security-policy.com/.
- Content-Security-Policy - HTTP | MDN - MDN Web Docs. https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Content-Security-Policy.
- Cross-Origin Resource Sharing (CORS) - HTTP | MDN. https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS.
- Cross-origin resource sharing - Wikipedia. https://en.wikipedia.org/wiki/Cross-origin_resource_sharing.
- Cross Origin Resource Sharing (CORS) - GeeksforGeeks. https://www.geeksforgeeks.org/cross-origin-resource-sharing-cors/.
- Beranda - OWASP Top 10:2021 - OWASP Foundation. https://owasp.org/Top10/id/.
- OWASP Top Ten | OWASP Foundation. https://owasp.org/www-project-top-ten/.
- OWASP Top 10 Risks and How to Prevent Them - Bright Security. https://brightsec.com/blog/owasp-top-10/.
- OWASP Top 10:2021. https://owasp.org/Top10/.
- OWASP Foundation, the Open Source Foundation for Application Security .... https://owasp.org/.
- OWASP Top Ten | OWASP Foundation. https://owasp.org/www-project-top-ten/.
- OWASP Top 10:2021. https://owasp.org/Top10/.
- Keamanan Situs Web - Lindungi Situs Anda dengan GoDaddy. https://www.godaddy.com/id-id/pengamanan-web/keamanan-website.
- 9 Tips Menjaga Keamanan Web (Web Security) | WEBAPP | APPKEY. https://appkey.id/pembuatan-website/teknologi-web/keamanan-web/.
- Ini 10 Cara Meningkatkan Keamanan Website!. https://www.exabytes.co.id/blog/cara-meningkatkan-keamanan-website/.
- Mengapa Keamanan Sangat Penting Bagi Suatu Website?. https://www.hitekno.com/internet/2020/12/22/100119/mengapa-keamanan-sangat-penting-bagi-suatu-website.
- 15 Cara Meningkatkan Keamanan Website, Wajib Tahu! - Jagoan Hosting. https://www.jagoanhosting.com/blog/keamanan-website/.
