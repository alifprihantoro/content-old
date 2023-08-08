# Node JS
Node.js adalah platform yang memungkinkan Anda menjalankan kode JavaScript di sisi server. Dengan Node.js, Anda dapat membuat aplikasi web yang cepat dan efisien. Node.js memiliki pustaka server sendiri sehingga Anda tidak perlu menggunakan program server web seperti Nginx dan Apache.

untuk menjalankan kode tentunya kita sering menggunakan alat bantu, baik hanya untuk proses development maupun production, seperti typescript, tailwind, ataupun framewor seperti react js. Karena kita tidak mungkin melakukan clone repo dan build satu satu devtools, maka kita memerlukan package manager untuk menangani hal itu.

## apa itu node package manager ?
NPM adalah pengelola package JavaScript yang secara default ada di Node.js. Dengan NPM, Anda bisa men-download berbagai package JavaScript untuk mempercepat pembuatan aplikasi. NPM juga berfungsi sebagai command line interface (CLI) yang memungkinkan Anda mengetikkan perintah untuk mengelola, mengunduh, dan meng-upload package JavaScript. Selain NPM ada juga yarn dan pnpm. yang mana ketiganya memiliki kelebihan dan kekurangannya masing-masing.

## NPM VS YARN VS PNPM
Berikut adalah beberapa kelebihan dan kekurangan antara NPM, Yarn, dan pnpm:
- NPM:
  - Kelebihan:
    - Sudah terpasang secara default ketika menginstall Node.js.
    - Memiliki banyak package yang tersedia.
  - Kekurangan:
    - Lebih lambat dibandingkan dengan Yarn dan pnpm².
- Yarn:
  - Kelebihan:
    - Lebih cepat daripada NPM².
    - Memiliki fitur caching yang dapat mempercepat instalasi dan build berikutnya.
    - Instalasi yang konsisten dan deterministik yang menjamin struktur dari library yang diinstal selalu sama.
  - Kekurangan:
    - Memiliki beberapa masalah kompatibilitas dengan beberapa package.
- pnpm:
  - Kelebihan:
    - Lebih cepat dan efisien daripada NPM³.
    - Menggunakan symlink untuk mempercepat proses instalasi dan pengelolaan dependensi³.
  - Kekurangan:
    - Masih kurang populer dibandingkan dengan NPM dan Yarn³.
## list artikel dan video
- NPM :
  - video :
    - [programmer zaman now](https://youtu.be/7t7CJwQlmGc)
    - [wpu unpas](https://youtu.be/7t7CJwQlmGc)
  - article :
    - https://www.dicoding.com/blog/node-package-manager/
- YARN :
  - https://appkey.id/pembuatan-website/teknologi-web/yarn-adalah/
  - https://www.hostinger.co.id/tutorial/cara-install-yarn
- PNPM :
  - https://medium.com/javascript-indonesia-community/mengenal-pnpm-package-manager-d62caf9a643

- JavaScript Package Managers: NPM Vs YARN Vs PNPM - Atatus. https://www.atatus.com/blog/npm-vs-yarn-vs-pnpm/.
- JavaScript package managers compared: npm, Yarn, or pnpm?. https://blog.logrocket.com/javascript-package-managers-compared/.
- Perbandingan npm, npx, pnpm, dan yarn Perangkat Pengelolaan Paket untuk .... https://www.codepolitan.com/blog/perbandingan-npm-npx-pnpm-dan-yarn-perangkat-pengelolaan-paket-untuk-ekosistem-javascript.
- npm vs Yarn - Package Manager mana yang harus Anda gunakan?. https://www.matawebsite.com/blog/npm-vs-yarn-package-manager-mana-yang-harus-anda-gunakan.
- Apa Itu NPM? Ini Pengertian dan Cara Instalnya! Niagahoster Blog. https://www.niagahoster.co.id/blog/npm/.
- NPM Adalah: Panduan Lengkap Beserta Cara Kerjanya - IDwebhost. https://idwebhost.com/blog/npm-adalah-panduan-lengkap-beserta-cara-kerjanya/.
- Apa itu Node Package Manager (NPM)? Fungsi & Cara Installnya. https://www.jagoanhosting.com/blog/npm-adalah/.
- Apa itu Node Package Manager: Tutorial NPM dan JavaScript. https://www.dicoding.com/blog/node-package-manager/.
- Apa Itu npm (Node Package Manager): Panduan untuk Pemula - Hostinger. https://www.hostinger.co.id/tutorial/apa-itu-npm.
