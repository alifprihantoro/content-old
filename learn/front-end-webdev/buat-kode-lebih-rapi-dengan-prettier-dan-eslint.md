# buat kode lebih rapi dengan prettier dan eslint
Halo teman-teman pembaca yang hebat! Apakah kalian pernah merasa frustasi karena kode yang kalian tulis terlihat berantakan dan sulit dibaca? Atau mungkin kalian sering membuang waktu hanya untuk mengatur tata letak kode secara manual? Jangan khawatir, karena kami memiliki solusi yang sempurna untuk kalian!

Dalam artikel kali ini, kami akan membahas tentang dua alat yang akan membuat kode kalian lebih rapi dan mudah dibaca: Prettier dan ESLint. Dengan menggunakan kedua alat ini, kalian tidak hanya akan menghemat waktu, tetapi juga meningkatkan kualitas kode kalian dengan standar yang telah ditetapkan secara otomatis.

## Penjelasan
ESLint dan Prettier adalah alat-alat yang digunakan dalam pengembangan perangkat lunak untuk meningkatkan kualitas kode.

ESLint adalah alat untuk memeriksa kode JavaScript dan memastikan bahwa kode tersebut memenuhi standar yang telah ditetapkan, serta memeriksa adanya kesalahan atau bug pada kode. Sementara itu, Prettier adalah alat untuk memformat kode dan membuatnya terlihat lebih rapi dan mudah dibaca.

Kedua alat ini dapat digunakan secara bersamaan untuk memastikan bahwa kode yang ditulis terlihat rapi, memenuhi standar, dan tidak mengandung kesalahan. Hubungan antara keduanya adalah bahwa ESLint dapat dikonfigurasi untuk menjalankan Prettier setiap kali ada kode yang harus diformat, sehingga keduanya dapat bekerja bersama-sama untuk meningkatkan kualitas kode secara keseluruhan.

## Mengapa Penting Menggunalan Eslint dan Prettier
### jika kita tidak menggunakan prettier atau eslint :
#### Positif :
- Tidak perlu menghabiskan waktu untuk mengatur konfigurasi atau mempelajari aturan penulisan kode yang spesifik
Dapat menulis kode dengan gaya penulisan yang bebas, tanpa harus mengikuti standar tertentu

#### Negative :
- Kode akan sulit dibaca dan rapi, khususnya jika ada beberapa penulis kode yang berbeda yang bekerja pada proyek yang sama
- Lebih sulit untuk menemukan dan memperbaiki kesalahan pada kode
- Tidak ada jaminan bahwa kode yang ditulis memenuhi standar dan kualitas yang baik
- Tidak konsisten dengan praktik terbaik dan standar industri dalam penulisan kode
#### kesimpulan
Kesimpulannya, meskipun menggunakan ESLint dan Prettier memerlukan waktu dan usaha, kelebihan dari penggunaannya jauh lebih besar daripada ketidaknyamanan yang dihadapi saat mengatur konfigurasi atau mempelajari aturan penulisan kode yang spesifik. Tidak menggunakan ESLint dan Prettier dapat menghasilkan kode yang sulit dibaca dan sulit dipelihara, dan juga menghilangkan jaminan bahwa kode memenuhi standar dan kualitas yang baik.

## Bagaimana mengintegrasikan ESLint dan Prettier?
- Install ESLint dan Prettier melalui npm dengan menggunakan perintah `npm install eslint prettier --save-dev`
- Install plugin Prettier untuk ESLint dengan perintah `npm install eslint-config-prettier --save-dev`
- Buat file konfigurasi .eslintrc.js dan konfigurasi ESLint untuk menggunakan plugin Prettier dengan menambahkan "prettier" pada extends dan "prettier/prettier": "error" pada rules. Berikut contohnya:
```javascript
module.exports = {
  env: {
    browser: true,
    es2021: true,
  },
  extends: [
    'eslint:recommended',
    'plugin:prettier/recommended', // plugin Prettier
  ],
  parserOptions: {
    ecmaVersion: 12,
    sourceType: 'module',
  },
  rules: {
    'prettier/prettier': 'error', // aturan Prettier
  },
};
```
- Buat file konfigurasi .prettierrc.js dan konfigurasi Prettier sesuai dengan preferensi penulisan kode Anda. Berikut contohnya:
```javascript
module.exports = {
  semi: true,
  trailingComma: 'es5',
  singleQuote: true,
  printWidth: 120,
  tabWidth: 2,
};
```
- Konfigurasikan editor kode Anda agar menjalankan Prettier setiap kali ada file yang disimpan. Ini akan memastikan bahwa kode di-format secara otomatis setiap kali disimpan. Untuk mengkonfigurasi editor, Anda dapat mencari plugin atau ekstensi Prettier untuk editor kode Anda.

Setelah langkah-langkah di atas selesai, Anda sudah berhasil mengintegrasikan ESLint dan Prettier pada proyek Anda. Dengan demikian, setiap kali kode ditulis, ESLint akan memeriksa adanya kesalahan dan memastikan kode memenuhi standar, sedangkan Prettier akan memastikan kode terlihat rapi dan mudah dibaca.
## resource pembelajaran
- https://youtu.be/4AsOTDdmx_I
- https://eslint.org/
- https://youtu.be/ArsfTWCiBhM
## penutup
Dalam artikel ini, kita telah membahas tentang dua alat penting dalam pengembangan perangkat lunak, yaitu ESLint dan Prettier. ESLint digunakan untuk memeriksa kesalahan dalam kode dan memastikan kode memenuhi standar tertentu, sedangkan Prettier digunakan untuk memformat kode agar terlihat rapi dan mudah dibaca. Integrasi antara keduanya dapat memberikan banyak manfaat bagi pengembang, seperti kode yang lebih mudah dibaca dan dipelihara, serta meningkatkan efisiensi dalam pengembangan perangkat lunak.

Namun, seperti halnya dengan semua alat dalam pengembangan perangkat lunak, ESLint dan Prettier memiliki kelebihan dan kekurangan masing-masing. Penting bagi pengembang untuk mempertimbangkan kelebihan dan kekurangan ini sebelum memutuskan apakah akan menggunakannya dalam proyek mereka.

Kesimpulannya, dengan mengintegrasikan ESLint dan Prettier pada proyek pengembangan perangkat lunak, kita dapat meningkatkan kualitas dan kebersihan kode yang ditulis, serta membuat pengembangan perangkat lunak lebih efisien dan produktif. Dengan memahami cara mengintegrasikan ESLint dan Prettier, pengembang dapat dengan mudah mengadopsi alat-alat ini dalam proyek mereka dan meningkatkan kualitas kode mereka.
