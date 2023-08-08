# Module Bundler
Modul bundler di JavaScript adalah alat yang digunakan untuk menggabungkan banyak file kode JavaScript menjadi satu file. Modul bundler digunakan ketika proyek Anda menjadi terlalu besar untuk satu file atau ketika Anda bekerja dengan pustaka yang memiliki banyak dependensi. Salah satu tools modul bundler yang sering digunakan adalah Webpack, vite, esbuild, etc. 

## Contoh Module bundler
### Webpack
Webpack adalah modul bundler JavaScript yang paling populer saat ini. Webpack dapat menangani berbagai jenis aset, termasuk JavaScript, CSS, font, dan gambar. Webpack mendukung code-splitting dan hot module replacement (HMR). Namun, kompleksitas konfigurasi Webpack dapat menjadi tantangan bagi pengembang pemula.

### Turbopack
Turbopack dibangun sebagai penerus Webpack, ditulis dari awal dalam Rust, berfokus pada kinerja sambil tetap fleksibel dan dapat diperluas. Turbopack mendukung hot module reloading out of the box dan out-of-the-box support untuk modern JavaScript (termasuk CommonJS dan ES Module imports) dan TypeScript.

### Parcel
Parcel memasarkan dirinya sebagai bundler tanpa konfigurasi nol, semakin populer karena kemudahannya. Parcel cepat karena kompilasi multi-core dan memiliki HMR yang cepat.

### Rollup
Rollup adalah bundler yang lebih ringan dan lebih cepat daripada Webpack. Rollup mendukung tree-shaking untuk menghilangkan kode yang tidak digunakan.

### Esbuild
Esbuild adalah bundler yang sangat cepat dan mudah digunakan. Esbuild mendukung TypeScript dan tree-shaking.

### Vite
Vite adalah bundler yang dirancang untuk pengembangan cepat dan ringan. Vite menyediakan server pengembangan penuh dan perintah build yang dioptimalkan menggunakan Rollup.

## Kelebihan dan kekurangan
### Webpack
Kelebihan:
- Dapat menangani berbagai jenis aset.
- Mendukung code-splitting dan hot module replacement (HMR).
- Memiliki plugin ecosystem yang luas dan dukungan komunitas yang luas.

Kekurangan:
- Konfigurasi yang kompleks dapat menjadi tantangan bagi pengembang pemula.
- Waktu build yang lambat pada proyek yang lebih besar.

### Turbopack
Kelebihan:
- Mendukung hot module reloading out of the box.
- Out-of-the-box support untuk modern JavaScript (termasuk CommonJS dan ES Module imports) dan TypeScript.
- Lebih cepat daripada Webpack.

Kekurangan:
- Tidak mendukung banyak plugin Webpack.

### Parcel
Kelebihan:
- Tidak memerlukan konfigurasi.
- Lebih cepat daripada Webpack.

Kekurangan:
- Tidak mendukung banyak plugin Webpack.

### Rollup
Kelebihan:
- Lebih ringan dan lebih cepat daripada Webpack.
- Mendukung tree-shaking untuk menghilangkan kode yang tidak digunakan.

Kekurangan:
- Tidak mendukung code-splitting dan HMR.

### Esbuild
Kelebihan:
- Sangat cepat dan mudah digunakan.
- Mendukung TypeScript dan tree-shaking.

Kekurangan:
- Tidak mendukung banyak plugin Webpack.

### Vite
Kelebihan:
- Dirancang untuk pengembangan cepat dan ringan.
- Menyediakan server pengembangan penuh dan perintah build yang dioptimalkan menggunakan Rollup.

Kekurangan:
- Masih dalam tahap pengembangan aktif.

## mana yang bagus ?
### Webpack
Jika proyek Anda besar dan kompleks, Webpack mungkin menjadi pilihan yang lebih baik karena dapat menangani berbagai jenis aset dan memiliki dukungan plugin yang luas. Namun, konfigurasi yang kompleks dapat menjadi tantangan bagi pengembang pemula.

### Turbopack
Jika kinerja adalah faktor penting dalam proyek Anda, Turbopack mungkin menjadi pilihan yang lebih baik karena sangat cepat dan mendukung hot module reloading out of the box. Terutama jika anda menggunakan next js.

### Parcel
Jika proyek Anda kecil dan Anda ingin bundler tanpa konfigurasi, Parcel mungkin menjadi pilihan yang lebih baik.

### Rollup
Jika proyek Anda besar dan kompleks tetapi Anda ingin bundler yang lebih ringan dan lebih cepat daripada Webpack, Rollup mungkin menjadi pilihan yang lebih baik.

### Esbuild
Jika kinerja adalah faktor penting dalam proyek Anda dan Anda ingin bundler yang sangat cepat dan mudah digunakan, Esbuild mungkin menjadi pilihan yang lebih baik.

### Vite
Jika Anda pemula dalam pengembangan web dan ingin bundler yang mudah digunakan dan tidak memerlukan konfigurasi yang rumit, Vite mungkin menjadi pilihan yang lebih baik.

## Apa yang saya pilih ?
Untuk saat ini saya memilih vite dan turbopack, dikarenakan framework yang saya gunakan menggunakan kedua hal tersebut. Yang mana kemungkinan pilihan ini bisa berubah sesuai kebutuhan.

## video dan artikel yang membahas package manager
- webpack :
  - https://youtube.com/playlist?list=PLFIM0718LjIWP4HvnehF19e1kzV-7wa3i
  - https://www.dumetschool.com/blog/Mengenal-Webpack-Dependensi-Manajer-ntuk-React
  - https://www.dicoding.com/blog/membuat-module-bundler-sendiri-ala-front-end-engineer-line/

> untuk video lainnya silahkan dicari, dikarenakan sumber lain yang saya pelajari menggunaka bahasa inggris. 

Source: Conversation with Bing, 8/8/2023
(1) Membuat Module Bundler Sendiri ala Front-end Engineer LINE. https://www.dicoding.com/blog/membuat-module-bundler-sendiri-ala-front-end-engineer-line/.
(2) JavaScript Bundlers: In-Depth Guide - Snipcart. https://snipcart.com/blog/javascript-module-bundler.
(3) Berkenalan Dengan Webpack. Webpack? | by Adiatma Kamarudin - Medium. https://medium.com/tutorjs/berkenalan-dengan-webpack-7a82e274b211.
