## apa itu linter
Linter JavaScript adalah alat yang dapat Anda gunakan untuk membantu Anda men-debug ode Anda. Mereka memindai skrip Anda untuk masalah dan kesalahan umum, dan memberi Anda laporan dengan nomor baris yang dapat Anda gunakan untuk memperbaiki hal-hal. Selain bug dan kesalahan sebenarnya, mereka juga memeriksa preferensi gaya yang subjektif. Manfaat menggunakan linter JavaScript antara lain:

- Mengurangi kesalahan di produksi. Penggunaan linter membantu mendiagnosis dan memperbaiki masalah teknis di kode. Akibatnya, lebih sedikit cacat yang masuk ke produksi.
- Kode yang mudah dibaca, dipelihara, dan lebih konsisten. Linter dapat membantu tim mencapai gaya yang lebih mudah dibaca dan konsisten, melalui penegakan aturannya.
- Lebih sedikit diskusi tentang gaya kode dan pilihan estetika selama tinjauan kode. Diskusi tinjauan kode tidak boleh dipenuhi dengan argumen tanpa akhir tentang preferensi gaya. Linter dapat mengambil topik-topik itu dari jalan.
- Pengukuran objektif kualitas kode. Diskusi tentang kualitas kode sering kali menyimpang ke subjektivitas. Linter memberikan penilaian objektif dan terukur tentang kualitas kode.
- Kode yang lebih aman dan berkinerja tinggi. Tidak semua linter menganalisis kode sumber terkait kinerja dan keamanannya, tetapi beberapa melakukannya.

Untuk menggunakan linter JavaScript, Anda perlu memilih linter yang sesuai dengan editor Anda. Misalnya, jika Anda menggunakan Visual Studio Code, Anda dapat menggunakan ESLint sebagai linter JavaScript. ESLint adalah alat analisis kode statis yang dapat menemukan dan memperbaiki masalah dengan kode JavaScript Anda. ESLint sepenuhnya dapat disesuaikan. Setiap aturan adalah plugin dan Anda dapat menambahkan lebih banyak saat runtime. Anda juga dapat menambahkan plugin, konfigurasi, dan parser komunitas untuk memperluas fungsionalitas ESLint.

## bagaimana cara setup
Untuk setup ESLint di Astro JS, Anda perlu melakukan beberapa langkah berikut:

- Install ESLint dan plugin Astro dengan menjalankan perintah `npm install --save-dev eslint eslint-plugin-astro`.
- Buat file konfigurasi ESLint dengan nama `.eslintrc.js` di direktori root proyek Anda.
- Tambahkan kode berikut ke file konfigurasi ESLint:

```javascript
module.exports = {
  // ...
  extends: [
    // ...
    "plugin:astro/recommended",
  ],
  rules: {
    'comma-dangle': ['error', 'always-multiline'],
    'prefer-template': ['error'],
    'no-multi-spaces': ['error', { ignoreEOLComments: false }],
    'no-multiple-empty-lines': ['error', { max: 1 }],
    'no-trailing-spaces': ['error'],
    'no-mixed-spaces-and-tabs': ['error'],
    'camelcase': ['error'],
    'indent': ['error', 2],
    'linebreak-style': [
      'error',
      'unix',
    ],
    'quotes': [
      'error',
      'single',
    ],
    'semi': [
      'error',
      'never',
    ],
    'no-console': ['warn'],
    'no-alert': ['warn'],
  },
  // ...
  overrides: [
    {
      // Define the configuration for `.astro` file.
      files: ["*.astro"],
      // Allows Astro components to be parsed.
      parser: "astro-eslint-parser",
      rules: {
        // override/add rules settings here, such as:
        // "astro/no-set-html-directive": "error"
      },
    },
    // ...
  ],
};
```

- Jika Anda menggunakan TypeScript di komponen Astro, Anda juga perlu menginstal parser `@typescript-eslint/parser` dan menambahkan konfigurasi berikut:

```javascript
// eslint-disable-next-line no-undef
module.exports = {
  'env': {
    'browser': true,
    'es2021': true,
  },
  'extends': [
    'eslint:recommended',
    'plugin:@typescript-eslint/recommended',
  ],
  parser: '@typescript-eslint/parser',
  'parserOptions': {
    'ecmaVersion': 'latest',
    'sourceType': 'module',
  },
  'plugins': ['@typescript-eslint'],
  rules: {
    'comma-dangle': ['error', 'always-multiline'],
    'prefer-template': ['error'],
    'no-multi-spaces': ['error', { ignoreEOLComments: false }],
    'no-multiple-empty-lines': ['error', { max: 1 }],
    'no-trailing-spaces': ['error'],
    'no-mixed-spaces-and-tabs': ['error'],
    'camelcase': ['error'],
    'indent': ['error', 2],
    'linebreak-style': [
      'error',
      'unix',
    ],
    'quotes': [
      'error',
      'single',
    ],
    'semi': [
      'error',
      'never',
    ],
    'no-console': ['warn'],
    'no-alert': ['warn'],
  },
  overrides: [
  // react (optional)
      {
      files: ['**/*.tsx'],
      'extends': [
        'eslint:recommended',
        'plugin:react/recommended',
        'plugin:@typescript-eslint/recommended',
      ],
      'plugins': ['react'],
      rules: {
        'react/react-in-jsx-scope': 0,
        'react/jsx-uses-react': 0,
      },
    },
    {
      files: ['*.astro'],
      parser: 'astro-eslint-parser',
      parserOptions: {
        parser: '@typescript-eslint/parser',
        extraFileExtensions: ['.astro'],
      },
      rules: {
      },
    },
  ],
}
```

- Jika Anda ingin menggunakan aturan untuk memeriksa aksesibilitas (A11Y), Anda juga perlu menginstal `eslint-plugin-jsx-a11y` tambahan:

```bash
npm install --save-dev eslint-plugin-jsx-a11y
```

- Jika Anda ingin menjalankan ESLint dari command line, pastikan Anda menyertakan ekstensi `.astro` menggunakan opsi `--ext` atau pola glob, karena ESLint hanya menargetkan file `.js` secara default. Contoh:

```bash
eslint --ext .js,.astro src
eslint "src/**/*.{js,astro}"
```

- Jika Anda menggunakan VS Code sebagai editor Anda, Anda dapat menginstal ekstensi Astro VS Code yang memberikan fitur-fitur seperti syntax highlighting, type information, dan Intellisense untuk file `.astro`.

Source: 
- eslint-plugin-astro - npm. https://www.npmjs.com/package/eslint-plugin-astro.
- ota-meshi/eslint-plugin-astro - Github. https://github.com/ota-meshi/eslint-plugin-astro.
- Editor Setup 🚀 Astro Documentation. https://docs.astro.build/en/editor-setup/.
- JavaScript Linters | Go Make Things. https://gomakethings.com/javascript-linters/.
- Find and fix problems in your JavaScript code - ESLint - Pluggable .... https://eslint.org/.
- Getting Started with ESLint - ESLint - Pluggable JavaScript Linter. https://eslint.org/docs/latest/use/getting-started.
- What Is a Linter? Here’s a Definition and Quick-Start Guide - Testim. https://www.testim.io/blog/what-is-a-linter-heres-a-definition-and-quick-start-guide/.
- Making Your Own JavaScript Linter (part 1) - Medium. https://medium.com/codex/making-your-own-javascript-linter-part-1-ee9f91dc49d8.
