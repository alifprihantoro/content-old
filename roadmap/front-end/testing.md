# Testing
Testing pada front end adalah melakukan pengujian yang memeriksa antarmuka grafis pengguna (GUI), fungsionalitas, dan kegunaan aplikasi web secara otomatis. Tujuan dari testing adalah untuk memastikan bahwa lapisan presentasi aplikasi web atau perangkat lunak bebas dari cacat dengan pembaruan yang berkelanjutan.

Ada beberapa alasan mengapa front end testing penting untuk dilakukan, antara lain:

- Mengidentifikasi Masalah Kinerja: Aplikasi web memiliki tiga lapisan fungsional, yaitu klien, server, dan sumber daya (atau sistem informasi). Front end testing menangani lapisan klien, yaitu bagian dari perangkat lunak yang disajikan kepada pengguna. Tidak jarang para pengembang fokus pada lapisan server dan sumber daya, karena mereka adalah dasar dari pembangunan perangkat lunak. Namun, front end testing penting untuk menganalisis perilaku perangkat lunak dari perspektif pengguna akhir. Mendeteksi masalah kinerja di sisi klien yang dapat mengganggu alur kerja kritis dan berkontribusi pada pengalaman pengguna yang tidak diinginkan adalah hal yang perlu dilakukan¹².
- Memverifikasi Fungsionalitas Lintas-Browser dan Lintas-Perangkat: Aspek penting dari front end testing adalah memverifikasi perilaku situs web dan aplikasi pada berbagai browser, versi browser, dan perangkat (mobile dan desktop). Ini termasuk fitur dan responsivitas pada layar dengan berbagai ukuran dan resolusi.

## Jenis-Jenis Front End Testing

Ada beberapa jenis front end testing yang dapat dilakukan, antara lain:

- Unit Testing: Unit testing adalah pengujian fungsionalitas modul atau "unit" terkecil dari aplikasi. Unit testing biasanya dilakukan oleh para pengembang dengan menggunakan kerangka kerja seperti Jest, Mocha, Jasmine, dll.
- Visual Regression Testing: Visual regression testing adalah pengujian perubahan tampilan visual dari aplikasi akibat pembaruan atau modifikasi. Visual regression testing biasanya dilakukan dengan menggunakan alat seperti Percy, Applitools, BackstopJS, dll.
- Cross Browser Testing: Cross browser testing adalah pengujian perilaku aplikasi pada berbagai browser dan versi browser. Cross browser testing bertujuan untuk memastikan bahwa aplikasi dapat berfungsi dengan baik dan konsisten pada semua browser yang didukung. Cross browser testing biasanya dilakukan dengan menggunakan alat seperti playwright, BrowserStack, LambdaTest, Selenium Grid, dll.
- Accessibility Testing: Accessibility testing adalah pengujian kemudahan akses dan penggunaan aplikasi oleh orang-orang dengan berbagai kemampuan dan keterbatasan. Accessibility testing bertujuan untuk memastikan bahwa aplikasi memenuhi standar aksesibilitas web seperti WCAG 2.0 atau 2.1. Accessibility testing biasanya dilakukan dengan menggunakan alat seperti axe, Lighthouse, WAVE, dll.
- Usability Testing: Usability testing adalah pengujian kepuasan dan efektivitas pengguna dalam menggunakan aplikasi. Usability testing melibatkan pengujian dengan partisipan manusia yang mewakili pengguna akhir aplikasi. Usability testing bertujuan untuk mendapatkan umpan balik tentang desain, navigasi, konten, dan fitur aplikasi. Usability testing biasanya dilakukan dengan menggunakan alat seperti UserTesting, UserZoom, Userlytics, dll.
- Performance Testing: Performance testing adalah pengujian kecepatan dan stabilitas aplikasi di bawah berbagai kondisi beban dan stres. Performance testing bertujuan untuk mengukur metrik seperti waktu muat halaman, waktu respons server, jumlah permintaan per detik, dll. Performance testing biasanya dilakukan dengan menggunakan alat seperti LoadRunner, JMeter, Gatling, dll.

## testing yang saya gunakan
- untuk e2e test saya menggunakan playwright
- untuk test lainnya saya menggunakan storybook js
### mengapa playwright
karena mudah digunakan, memiliki fitur yang banyak, sudah menggunakan typescript, mudah untuk testing diberbagai browser dan viewport.
### mengapa storybook js
karena kita bisa melakukan testing sekaligus mendokumentasikan. Dimana storybook memiliki hasil outpu berupa browser yang didalamnya berisi ui yang kita buat, menautkan ke figma, melakukan manipulasi (seperti mengganti warna dll) dan integrasi dengan github PR, dimana kita bisa mengecek perubahan dalam bentuk ui. Dan masih banyak lagi.

Source:
- Front End Testing: A Beginner's Guide | BrowserStack. https://www.browserstack.com/guide/front-end-testing.
- Front End Testing: A Complete Conceptual Overview. https://www.testim.io/blog/front-end-testing-complete-overview/.
- What is Front End Testing? - Guru99. https://www.guru99.com/frontend-testing.html.
- Front-end testing - Modern tools and possible alternatives. https://www.clickworker.com/customer-blog/front-end-testing-of-websites/.
- Front-end Testing: Tools, Frameworks, and Methods - NG Logic. https://nglogic.com/front-end-testing/.
