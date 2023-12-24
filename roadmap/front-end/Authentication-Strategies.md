# Jenis-Jenis Autentikasi

Autentikasi adalah proses untuk memverifikasi identitas pengguna yang ingin mengakses suatu sistem atau aplikasi. Autentikasi biasanya dilakukan dengan membandingkan kredensial pengguna (seperti username dan password) dengan data yang tersimpan di server. Ada berbagai jenis autentikasi yang dapat digunakan, tergantung pada kebutuhan dan tingkat keamanan yang diinginkan. Berikut ini adalah beberapa jenis autentikasi yang umum digunakan:

## Basic Authentication

Basic Authentication adalah jenis autentikasi yang paling sederhana dan mudah diimplementasikan. Basic Authentication menggunakan username dan password yang dikirimkan dalam header HTTP dengan format `Authorization: Basic base64(username:password)`. Server kemudian akan mendekode nilai base64 dan membandingkan username dan password dengan data yang tersimpan di server. Jika cocok, maka server akan memberikan akses kepada pengguna.

Kelebihan dari Basic Authentication adalah simpel dan tidak memerlukan mekanisme tambahan seperti cookie atau token. Namun, kekurangan dari Basic Authentication adalah kurang aman karena username dan password dapat terlihat oleh siapa saja yang dapat mengintip lalu lintas jaringan. Selain itu, Basic Authentication juga tidak memiliki mekanisme untuk mengakhiri sesi atau mengatur masa berlaku kredensial. Oleh karena itu, Basic Authentication hanya cocok digunakan untuk sistem atau aplikasi yang tidak memerlukan tingkat keamanan yang tinggi¹.

## Session Based Authentication

Session Based Authentication adalah jenis autentikasi yang menggunakan cookie untuk menyimpan informasi tentang sesi pengguna. Cookie adalah data kecil yang dikirimkan oleh server ke browser pengguna dan disimpan di sana. Cookie dapat berisi informasi seperti sessionId, waktu kadaluarsa, atau data lainnya yang relevan dengan sesi pengguna.

Session Based Authentication bekerja dengan cara sebagai berikut:

- Ketika pengguna pertama kali mengirimkan username dan password, server akan memverifikasi kredensial tersebut dan membuat sebuah sessionId yang unik untuk pengguna tersebut. Server kemudian akan menyimpan sessionId tersebut beserta data pengguna lainnya di dalam memori server.
- Server akan mengirimkan sessionId tersebut ke browser pengguna dalam bentuk cookie dengan header `Set-Cookie: sessionId=...`.
- Browser pengguna akan menyimpan cookie tersebut dan mengirimkannya kembali ke server setiap kali melakukan permintaan dengan header `Cookie: sessionId=...`.
- Server akan mencocokkan sessionId yang diterima dengan data yang tersimpan di memori server. Jika cocok, maka server akan memberikan akses kepada pengguna. Jika tidak cocok atau sudah kadaluarsa, maka server akan menolak permintaan tersebut.

Kelebihan dari Session Based Authentication adalah lebih aman daripada Basic Authentication karena username dan password tidak perlu dikirimkan setiap kali melakukan permintaan. Selain itu, Session Based Authentication juga dapat mengatur masa berlaku dan mengakhiri sesi pengguna dengan mudah. Namun, kekurangan dari Session Based Authentication adalah memerlukan ruang penyimpanan di sisi server untuk menyimpan data sesi pengguna. Hal ini dapat menjadi masalah jika jumlah pengguna sangat banyak atau jika sistem menggunakan arsitektur terdistribusi atau mikroservis².

## Token Based Authentication

Token Based Authentication adalah jenis autentikasi yang menggunakan token sebagai bukti identitas pengguna. Token adalah string acak yang dibuat oleh server dan dikirimkan ke browser pengguna setelah kredensial pengguna diverifikasi. Token biasanya berisi informasi seperti identitas pengguna, waktu kadaluarsa, atau klaim lainnya yang relevan dengan akses pengguna.

Token Based Authentication bekerja dengan cara sebagai berikut:

- Ketika pengguna pertama kali mengirimkan username dan password, server akan memverifikasi kredensial tersebut dan membuat sebuah token untuk pengguna tersebut. Server kemudian akan mengirimkan token tersebut ke browser pengguna dalam bentuk header, cookie, atau body response.
- Browser pengguna akan menyimpan token tersebut dan mengirimkannya kembali ke server setiap kali melakukan permintaan dengan header `Authorization: Bearer token` atau cara lainnya sesuai dengan konvensi yang digunakan.
- Server akan memvalidasi token yang diterima dengan cara memeriksa tanda tangan, waktu kadaluarsa, atau klaim lainnya yang terkandung dalam token. Jika valid, maka server akan memberikan akses kepada pengguna. Jika tidak valid atau sudah kadaluarsa, maka server akan menolak permintaan tersebut.

Kelebihan dari Token Based Authentication adalah tidak memerlukan ruang penyimpanan di sisi server untuk menyimpan data pengguna. Hal ini membuat Token Based Authentication lebih cocok untuk sistem yang menggunakan arsitektur terdistribusi atau mikroservis. Selain itu, Token Based Authentication juga dapat memfasilitasi integrasi dengan sistem lain yang menggunakan standar token yang sama. Namun, kekurangan dari Token Based Authentication adalah lebih sulit untuk mengatur masa berlaku dan mengakhiri sesi pengguna karena token tidak dapat dibatalkan secara langsung².

## JWT Authentication

JWT Authentication adalah jenis Token Based Authentication yang menggunakan JSON Web Token (JWT) sebagai format token. JWT adalah standar terbuka yang mendefinisikan cara untuk mengirimkan informasi antara dua pihak secara aman dengan menggunakan objek JSON yang ditandatangani secara kriptografis. JWT terdiri dari tiga bagian yang dipisahkan oleh titik, yaitu header, payload, dan signature.

Header adalah bagian yang berisi informasi tentang jenis token dan algoritma tanda tangan yang digunakan. Payload adalah bagian yang berisi informasi atau klaim yang ingin dikirimkan antara dua pihak. Signature adalah bagian yang berisi hasil enkripsi dari header dan payload dengan menggunakan kunci rahasia atau kunci publik-privat.

JWT Authentication bekerja dengan cara sebagai berikut:

- Ketika pengguna pertama kali mengirimkan username dan password, server akan memverifikasi kredensial tersebut dan membuat sebuah JWT untuk pengguna tersebut. Server kemudian akan mengirimkan JWT tersebut ke browser pengguna dalam bentuk header, cookie, atau body response.
- Browser pengguna akan menyimpan JWT tersebut dan mengirimkannya kembali ke server setiap kali melakukan permintaan dengan header `Authorization: Bearer JWT` atau cara lainnya sesuai dengan konvensi yang digunakan.
- Server akan memvalidasi JWT yang diterima dengan cara memeriksa signature, waktu kadaluarsa, atau klaim lainnya yang terkandung dalam JWT. Jika valid, maka server akan memberikan akses kepada pengguna. Jika tidak valid atau sudah kadaluarsa, maka server akan menolak permintaan tersebut.

Kelebihan dari JWT Authentication adalah sama dengan Token Based Authentication, yaitu tidak memerlukan ruang penyimpanan di sisi server dan dapat memfasilitasi integrasi dengan sistem lain yang menggunakan standar JWT. Selain itu, JWT Authentication juga memiliki kelebihan lain, yaitu dapat mengirimkan informasi tambahan dalam payload yang dapat digunakan untuk tujuan lain seperti otorisasi, audit, atau statistik. Namun, kekurangan dari JWT Authentication adalah sama dengan Token Based Authentication, yaitu lebih sulit untuk mengatur masa berlaku dan mengakhiri sesi pengguna karena JWT tidak dapat dibatalkan secara langsung²³.

## OAuth

OAuth adalah standar terbuka yang mendefinisikan cara untuk memberikan akses terbatas kepada sumber daya di sistem lain tanpa perlu memberikan kredensial pengguna. OAuth biasanya digunakan untuk skenario di mana pengguna ingin mengizinkan aplikasi atau situs web untuk mengakses sumber daya di sistem lain seperti media sosial, email, atau penyimpanan cloud.

OAuth bekerja dengan cara sebagai berikut:

- Ketika pengguna ingin mengizinkan aplikasi atau situs web (client) untuk mengakses sumber daya di sistem lain (resource server), client akan mengarahkan pengguna ke sistem lain (authorization server) untuk mendapatkan izin.
- Authorization server akan meminta pengguna untuk login dan memberikan persetujuan kepada client untuk mengakses sumber daya tertentu di resource server.
- Jika pengguna setuju, authorization server akan mengirimkan sebuah kode otorisasi kepada client melalui redirect URI yang telah ditentukan sebelumnya.
- Client kemudian akan menukar kode otorisasi tersebut dengan sebuah token akses di authorization server dengan menggunakan kredensial client sendiri.
- Client dapat menggunakan token akses tersebut untuk mengakses sumber daya di resource server dengan menyertakan token akses tersebut dalam header `Authorization: Bearer token` atau cara lainnya sesuai dengan konvensi yang digunakan.
- Resource server akan memvalidasi token akses tersebut dengan authorization server atau dengan cara lainnya sesuai dengan konvensi yang jika valid, maka server akan memberikan akses kepada pengguna. Jika tidak valid, maka server akan menolak permintaan tersebut.

## SSO
SSO adalah singkatan dari Single Sign-On, yaitu jenis autentikasi yang memungkinkan pengguna untuk login ke berbagai sistem atau aplikasi dengan menggunakan kredensial yang sama. SSO biasanya digunakan untuk skenario di mana pengguna ingin mengakses berbagai layanan yang disediakan oleh satu organisasi atau entitas.

SSO bekerja dengan cara sebagai berikut:

- Ketika pengguna ingin mengakses sistem atau aplikasi (service provider) yang membutuhkan autentikasi, service provider akan mengarahkan pengguna ke sistem lain (identity provider) yang bertanggung jawab untuk menyediakan kredensial pengguna.
- Identity provider akan meminta pengguna untuk login dengan menggunakan kredensial yang sama untuk semua layanan yang terhubung dengan identity provider tersebut.
- Jika pengguna berhasil login, identity provider akan mengirimkan sebuah token atau tiket kepada service provider melalui redirect URI yang telah ditentukan sebelumnya.
- Service provider akan memvalidasi token atau tiket tersebut dengan identity provider atau dengan cara lainnya sesuai dengan konvensi yang digunakan.
- Jika valid, maka service provider akan memberikan akses kepada pengguna. Jika tidak valid, maka service provider akan menolak permintaan tersebut.

Kelebihan dari SSO adalah dapat meningkatkan kenyamanan dan keamanan pengguna karena pengguna hanya perlu mengingat satu kredensial untuk mengakses berbagai layanan. Selain itu, SSO juga dapat mengurangi beban administrasi dan manajemen kredensial di sisi service provider. Namun, kekurangan dari SSO adalah dapat meningkatkan risiko kebocoran kredensial karena jika kredensial tersebut dicuri atau diretas, maka penyerang dapat mengakses semua layanan yang terhubung dengan kredensial tersebut.

# Kesimpulan

Dari artikel ini, kita dapat mengetahui bahwa ada berbagai jenis autentikasi yang dapat digunakan untuk memverifikasi identitas pengguna yang ingin mengakses suatu sistem atau aplikasi. Setiap jenis autentikasi memiliki kelebihan dan kekurangan masing-masing, tergantung pada kebutuhan dan tingkat keamanan yang diinginkan. Oleh karena itu, kita perlu memilih jenis autentikasi yang sesuai dengan karakteristik dan tujuan dari sistem atau aplikasi yang kita buat atau gunakan.

> Dikarenakan peraturan privacy, browser secara default kaan memblokir cokies pihak ketiga. untuk itu kita harus bisa mengakalinya. untuk bagaimana caranya, saya belum mendapatkan kasus seperti ini. Saya juga belum mendapatkan resource video mengenai hal ini dalam bahasa indonesia.

### materi yang bisa dipelajari
- https://youtu.be/_w9ixlwUsgg
- https://youtu.be/A-7_PWsi8Mg
- https://youtu.be/Ll_71n60vAM

Source: Conversation with Bing, 8/15/2023
(1) Is Basic Authentication a Session based authentication and why Jwt is .... https://stackoverflow.com/questions/59829580/is-basic-authentication-a-session-based-authentication-and-why-jwt-is-more-recom.
(2) Is basic authentication a token based authentication?. https://stackoverflow.com/questions/64303508/is-basic-authentication-a-token-based-authentication.
(3) undefined. https://www.base64encode.org/.
