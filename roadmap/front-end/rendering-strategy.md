# rendering strategy
Rendering adalah proses mengubah kode React menjadi HTML. Metode rendering yang Anda pilih tergantung pada data yang Anda kerjakan dan seberapa peduli Anda dengan kinerja. Berikut adalah penjelasan singkat tentang masing-masing metode:

- CSR (**Client Side Rendering**): Rendering dilakukan di sisi klien (browser) setelah halaman dimuat. Data diambil secara dinamis menggunakan API atau fungsi fetch. CSR cocok untuk halaman yang membutuhkan pembaruan data yang sering atau tidak perlu di-render sebelumnya.
- SSR (**Server Side Rendering**): Rendering dilakukan di sisi server sebelum halaman dikirim ke browser. Data diambil dari database jika diperlukan dan dikirim bersama dengan konten halaman. SSR cocok untuk halaman yang mengonsumsi data dinamis dan membutuhkan SEO yang baik.
- SSG (**Static Site Generation**): Rendering dilakukan saat proses build dan halaman statis dibuat untuk setiap rute. Data diambil dari sumber eksternal atau lokal dan disematkan ke dalam halaman. SSG cocok untuk halaman yang tidak berubah sering, seperti blog, profil perusahaan, atau situs portofolio.
- ISR (**Incremental Static Regeneration**): Rendering dilakukan secara statis saat proses build, tetapi halaman dapat diregenerasi secara bertahap setelah diterbitkan. Data diambil dari sumber eksternal atau lokal dan disematkan ke dalam halaman, tetapi dapat diperbarui secara berkala dengan menentukan interval waktu.

Semua metode rendering ini memiliki kelebihan dan kekurangan masing-masing, sehingga Anda harus memilih metode yang paling sesuai dengan kebutuhan Anda.

## kelebihan dan kekurangan
Berikut adalah kelebihan dan kekurangan masing-masing metode rendering:

- CSR (**Client Side Rendering**): 
  - Kelebihan: 
    - Halaman dapat di-render dengan cepat setelah halaman dimuat.
    - Cocok untuk aplikasi dengan banyak interaksi pengguna atau konten yang sangat dinamis.
    - Tidak membutuhkan server aplikasi, hanya server statis.
  - Kekurangan:
    - Tidak ramah SEO, karena mesin pencari tidak dapat mengindeks halaman yang kosong.
    - Membutuhkan lebih banyak sumber daya klien, karena JavaScript harus dijalankan di browser.
    - Data dapat menjadi usang jika tidak diperbarui secara berkala.

- SSR (**Server Side Rendering**):
  - Kelebihan:
    - Ramah SEO, karena mesin pencari dapat mengindeks halaman yang sudah di-render.
    - Memperbaiki pengalaman pengguna, karena halaman dapat ditampilkan lebih cepat tanpa menunggu JavaScript selesai dijalankan.
    - Data selalu terbaru, karena diambil dari database setiap kali ada permintaan halaman.
  - Kekurangan:
    - Membutuhkan server aplikasi, yang lebih mahal dan kompleks daripada server statis.
    - Membebani server, karena harus melakukan rendering setiap kali ada permintaan halaman.
    - Waktu render lebih lama daripada CSR, karena harus menunggu data dari database.

- SSG (**Static Site Generation**):
  - Kelebihan:
    - Halaman statis paling cepat dari semua metode rendering, karena sudah siap untuk disajikan.
    - Ramah SEO, karena mesin pencari dapat mengindeks halaman yang sudah di-render.
    - Tidak membutuhkan server aplikasi, hanya server statis.
  - Kekurangan:
    - Data dapat menjadi usang, karena hanya diambil saat proses build.
    - Tidak cocok untuk aplikasi dengan konten yang berubah sering, karena harus melakukan build ulang setiap kali ada perubahan data.
    - Waktu build lebih lama daripada CSR dan SSR, karena harus melakukan rendering untuk semua halaman.

- ISR (**Incremental Static Regeneration**):
  - Kelebihan:
    - Menggabungkan kelebihan SSG dan SSR, yaitu kecepatan halaman statis dan kemutakhiran data dinamis.
    - Ramah SEO, karena mesin pencari dapat mengindeks halaman yang sudah di-render.
    - Tidak membutuhkan server aplikasi, hanya server statis.
  - Kekurangan:
    - Data masih dapat menjadi usang, jika interval waktu regenerasi terlalu lama atau terlalu jarang.
    - Memerlukan konfigurasi tambahan untuk menentukan interval waktu regenerasi.

## contoh framework
- CSR (**Client Side Rendering**): 
  - [React.js](^1^)
  - [Angular.js](^2^)
  - [Vue.js](^3^)
  - [Svelte](^4^)
  - [Blazor](^5^)
  - [Alpine.js]
  - [Mithril]
  - [Lit JS]
  - [HTMX]
- SSR (**Server Side Rendering**):
  - [Laravel]
  - [Symfony]
  - [Django]
  - [Express]
  - [Next.js]
  - [Nuxt.js]
  - [Sapper]
  - [AdonisJS]
  - [Nest JS]
- SSG (**Static Site Generation**):
  - [Next.js]
  - [Gatsby]
  - [Nuxt.js]
  - [Hugo]
  - [Jekyll]
  - [Eleventy]
  - [Hexo]
  - [Astro]
- ISR (**Incremental Static Regeneration**):
  - [Next.js](14)

source :
- Mengenal Framework: Pengertian, Fungsi, Jenis dan Contohnya. https://www.exabytes.co.id/blog/pengertian-framework/.
- Apa Itu Framework? Pengertian, Fungsi, dan Contohnya - Hostinger. https://www.hostinger.co.id/tutorial/framework-adalah.
- Framework: Pengertian, Cara Kerja, dan Contohnya | Toffeedev. https://toffeedev.com/blog/framework-adalah/.
- Apa Itu Framework? Pengertian dan Jenisnya - Alterra Academy. https://academy.alterra.id/blog/apa-itu-framework/.
- Apa itu Framework? Developer Wajib Tahu - Dicoding Blog. https://www.dicoding.com/blog/apa-itu-framework/.
- Frontend Rendering: SSG vs SSR vs CSR vs ISR | Dexlock. https://dexlock.com/blog/frontend-rendering-ssg-vs-ssr-vs-csr-vs-isr/.
- Visual Explanation and Comparison of CSR, SSR, SSG and ISR. https://dev.to/pahanperera/visual-explanation-and-comparison-of-csr-ssr-ssg-and-isr-34ea.
- Memahami Metode Rendering Next.js: CSR, SSR, SSG, ISR | Ceriwit ID. https://ceriwit.my.id/nextjs-rendering-methods-csr-ssr-ssg-isr/.
- Understanding CSR, SSR, SSG, and ISR: A Next.js Perspective. https://bootcamp.uxdesign.cc/understanding-csr-ssr-ssg-and-isr-a-next-js-perspective-fcaf36686de6.
- Understanding Next.js Rendering Methods: CSR, SSR, SSG, ISR - MUO. https://www.makeuseof.com/nextjs-rendering-methods-csr-ssr-ssg-isr/.
- Web Rendering: What Is SSR, CSR, SSG, and ISR? | Fajarwz. https://fajarwz.com/blog/web-rendering-what-is-ssr-csr-ssg-and-isr/.
- Rendering Strategies - Basics of SSR, SSG, CSR & ISR. https://dev.to/josefine/rendering-strategies-basics-of-ssr-ssg-csr-isr-ll9.
- What is the difference between SSR, ISR, CSR, SSG. https://dev.to/mojodev/what-is-the-difference-between-ssr-isr-csr-ssg-2g9p.
