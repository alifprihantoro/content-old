Setiap kali kita membuat sebuah proyek, salah satu aspek yang sangat penting adalah struktur direktori dan penamaan file/folder. Hal ini karena struktur dan penamaan yang tepat dapat memudahkan kita untuk mengelola dan mengorganisir proyek kita dengan lebih baik.

Dalam proyek front end, struktur direktori yang baik dapat membantu memudahkan proses pengembangan dan memudahkan kolaborasi dengan anggota tim yang lain. Selain itu, penamaan file/folder yang konsisten dapat membantu kita untuk lebih mudah memahami dan mengelola proyek secara keseluruhan.

## Atomic Design
Atomic design adalah suatu metodologi desain yang dikembangkan oleh Brad Frost. Metodologi ini mengusulkan pendekatan hierarkis dalam membangun suatu komponen atau elemen dalam suatu aplikasi dengan memecahnya menjadi bagian yang lebih kecil yang dikenal sebagai atom. Atom kemudian dapat digabungkan menjadi molekul, organisme, template, dan halaman.

Konsep atomic design adalah membangun desain yang skalabel, terstruktur dengan baik, dan mudah dikembangkan kembali. Dengan menggunakan konsep atomic design, tim desain dan pengembangan dapat bekerja secara terstruktur dan efisien, dengan memperhatikan kebutuhan bisnis dan pengguna.

Pada tingkat atom, desain melibatkan elemen-elemen terkecil dari aplikasi, seperti warna, ikon, dan teks. Molekul kemudian menggabungkan beberapa atom untuk membentuk komponen seperti tombol dan input. Organisme memadukan beberapa molekul untuk membentuk suatu bagian yang lebih besar seperti header atau footer. Template adalah komponen yang menentukan struktur visual dari halaman dan halaman terakhir adalah kumpulan dari beberapa template yang saling berinteraksi.

Dengan pendekatan atomic design, tim desain dan pengembang dapat membangun suatu aplikasi dengan lebih terstruktur dan efisien, dengan mempertimbangkan kebutuhan bisnis dan pengguna. Hal ini juga dapat mempermudah proses pemeliharaan kode, pengembangan ulang, dan perubahan desain di masa depan.

### Contoh Atomic Design
Berikut adalah contoh struktur direktori kompleks yang menerapkan konsep atomic design pada proyek front end:
```bash
src/
|-- assets/
|   |-- images/
|       |-- logo.png
|   |-- styles/
|       |-- base/
|           |-- _variables.scss
|           |-- _base.scss
|       |-- components/
|           |-- _button.scss
|           |-- _input.scss
|       |-- layout/
|           |-- _header.scss
|           |-- _sidebar.scss
|           |-- _footer.scss
|       |-- pages/
|           |-- _home.scss
|           |-- _products.scss
|           |-- _checkout.scss
|
|-- components/
|   |-- atoms/
|       |-- Button/
|           |-- index.js
|           |-- Button.scss
|       |-- Input/
|           |-- index.js
|           |-- Input.scss
|   |-- molecules/
|       |-- ProductCard/
|           |-- index.js
|           |-- ProductCard.scss
|   |-- organisms/
|       |-- Header/
|           |-- index.js
|           |-- Header.scss
|       |-- Sidebar/
|           |-- index.js
|           |-- Sidebar.scss
|       |-- Footer/
|           |-- index.js
|           |-- Footer.scss
|   |-- templates/
|       |-- Home/
|           |-- index.js
|           |-- Home.scss
|       |-- Products/
|           |-- index.js
|           |-- Products.scss
|       |-- Checkout/
|           |-- index.js
|           |-- Checkout.scss
|
|-- layouts/
|   |-- Header/
|       |-- index.js
|       |-- Header.scss
|   |-- Sidebar/
|       |-- index.js
|       |-- Sidebar.scss
|   |-- Footer/
|       |-- index.js
|       |-- Footer.scss
|
|-- pages/
|   |-- Home/
|       |-- index.js
|       |-- Home.scss
|   |-- Products/
|       |-- index.js
|       |-- Products.scss
|   |-- Checkout/
|       |-- index.js
|       |-- Checkout.scss
|
|-- services/
|   |-- Firebase/
|       |-- Authentication.js
|       |-- Firestore.js
|   |-- IndexDB/
|       |-- db.js
|       |-- productService.js
|
|-- utils/
|   |-- date.js
|   |-- string.js
|
|-- data/
|   |-- navigation.js
|
|-- App.js
|-- index.js
```
Dalam contoh struktur direktori di atas, kita dapat melihat bahwa proyek dibagi menjadi beberapa folder dan file, yaitu:

- Folder assets/ - folder ini berisi semua aset seperti gambar, video, dan font yang digunakan dalam proyek.
- Folder components/ - folder ini berisi semua komponen yang digunakan dalam proyek, seperti atoms, molecules, dan organisms.
  - Subfolder atoms/ - folder ini berisi komponen terkecil dalam proyek, seperti tombol atau input.
  - Subfolder molecules/ - folder ini berisi gabungan beberapa komponen atoms, seperti form.
  - Subfolder organisms/ - folder ini berisi gabungan beberapa komponen molecules dan/atau atoms, seperti header dan footer.
- Folder pages/ - folder ini berisi file HTML, CSS, dan JavaScript untuk setiap halaman dalam proyek.
- Folder styles/ - folder ini berisi file CSS yang terbagi menjadi beberapa subfolder, yaitu:
  - Subfolder base/ - folder ini berisi file CSS yang berfungsi untuk mereset tampilan dan mengatur typografi pada proyek.
  - Subfolder utils/ - folder ini berisi file CSS yang berisi variabel, mixin, atau fungsi

### informasi yang saya pahami

