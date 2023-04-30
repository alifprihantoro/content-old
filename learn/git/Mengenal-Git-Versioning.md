Halo! Apa kabar? Kali ini, kita akan membahas topik yang menarik yaitu Git Versioning. Apakah kamu pernah mengalami kesulitan saat mencari versi sebelumnya dari proyek atau ingin melihat perubahan yang telah dilakukan di antara versi-proyek kamu? Git Versioning adalah solusinya!

Dengan Git Versioning, kamu dapat dengan mudah membuat dan mengelola versi baru dari proyek kamu. Hal ini sangat penting jika kamu bekerja dalam tim atau pada proyek yang kompleks. Kamu akan mempelajari tentang tag, branch, dan commit serta bagaimana cara membuat versi baru, memperbarui versi yang sudah ada, dan bekerja dengan beberapa versi proyek secara bersamaan.

Jadi, mari kita pelajari lebih lanjut tentang Git Versioning bersama-sama! Jangan ragu untuk bertanya jika ada yang perlu kamu ketahui atau jika kamu ingin berbagi pengalaman tentang penggunaan Git Versioning di proyek kamu.

## Branch
Branch dalam Git Versioning adalah cara untuk membuat salinan dari kode sumber pada sebuah proyek. Saat kita membuat sebuah branch, kita dapat melakukan perubahan pada salinan kode sumber tersebut tanpa mempengaruhi kode sumber utama. Kita dapat menggunakan branch untuk mengembangkan fitur baru, memperbaiki bug, atau melakukan eksperimen pada proyek tanpa khawatir merusak kode sumber utama. Setelah kita selesai melakukan perubahan pada branch, kita dapat mengintegrasikannya kembali ke kode sumber utama melalui proses merge.

Sebagai contoh, bayangkan kamu bekerja pada proyek perangkat lunak untuk aplikasi e-commerce. Kamu ingin menambahkan fitur baru pada aplikasi tersebut, yaitu integrasi dengan sistem pembayaran baru. Sebelum kamu mulai menambahkan fitur baru tersebut ke kode sumber utama, kamu dapat membuat sebuah branch baru dengan nama "payment-system-integration". Kamu dapat membuat perubahan yang diperlukan pada branch tersebut dan melakukan uji coba. Setelah fitur tersebut sudah selesai dan berhasil diuji, kamu dapat mengintegrasikan branch tersebut ke kode sumber utama melalui proses merge. Dengan menggunakan branch, kamu dapat memisahkan pengembangan fitur baru dari kode sumber utama sehingga tidak akan ada pengaruh negatif pada proyek yang sedang berjalan.

Penamaan branch juga sangat penting dalam manajemen versi pada Git. Berikut adalah beberapa tips dalam penamaan branch yang baik:

Gunakan nama branch yang deskriptif dan mudah dipahami. Nama branch harus mewakili fitur atau tugas yang sedang dikerjakan.

Gunakan prefix pada nama branch untuk mengelompokkan branch. Contoh prefix yang umum digunakan antara lain "feature/", "bugfix/", "hotfix/", "release/", atau "refactor/". Prefix ini memungkinkan kita untuk mengelompokkan branch berdasarkan jenis perubahan yang sedang dilakukan.

Gunakan karakter "-" atau "_" untuk memisahkan kata-kata pada nama branch. Hindari penggunaan spasi atau karakter spesial lainnya.

Gunakan singkatan atau kode untuk nama branch yang terlalu panjang. Namun, pastikan singkatan atau kode tersebut mudah dipahami oleh anggota tim.

Contoh penamaan branch untuk tim kecil:

feature/user-registration
bugfix/login-validation
hotfix/database-connection
refactor/clean-up-code
Contoh penamaan branch untuk tim besar:

feature/US1234-user-registration
bugfix/BG1234-login-validation
hotfix/HF1234-database-connection
refactor/RF1234-clean-up-code
Dalam tim besar, penggunaan singkatan atau kode pada nama branch sangat penting untuk membedakan branch yang sedang dikerjakan oleh setiap anggota tim. Prefix juga dapat digunakan untuk memisahkan branch berdasarkan jenis perubahan dan memudahkan pengelompokkan branch.
## Commit
Commit dalam Git Versioning adalah tindakan untuk menyimpan perubahan pada kode sumber. Setiap kali kita melakukan perubahan pada kode sumber, kita harus melakukan commit untuk menyimpan perubahan tersebut. Commit berisi pesan deskriptif tentang perubahan yang telah kita lakukan pada kode sumber. Commit juga mencatat informasi tentang waktu dan siapa yang melakukan perubahan tersebut.

Sebagai contoh, bayangkan kamu sedang mengembangkan sebuah proyek perangkat lunak untuk sebuah perusahaan. Kamu menambahkan fitur baru pada aplikasi, yaitu tombol "logout" di halaman profil pengguna. Setelah menambahkan fitur tersebut, kamu dapat melakukan commit pada kode sumber dengan pesan "Menambahkan tombol logout di halaman profil pengguna". Dengan melakukan commit, kamu menyimpan perubahan pada kode sumber dan mencatat informasi tentang perubahan tersebut. Jika suatu saat nanti kamu ingin kembali ke versi sebelumnya dari kode sumber, kamu dapat menggunakan commit untuk melakukannya.

Penting untuk diingat bahwa setiap commit harus menyimpan satu perubahan pada kode sumber yang logis dan terkait dengan satu tugas atau masalah tertentu. Commit juga harus memiliki pesan yang jelas dan deskriptif sehingga mudah dipahami oleh orang lain yang mungkin akan melihat kode sumber kamu di masa depan.

### cara penamaan commit
Penamaan commit dapat dilakukan dengan menggunakan konvensi penamaan yang umum digunakan oleh pengembang. Beberapa konvensi penamaan tersebut antara lain:

- Feat: untuk menambahkan fitur baru pada kode sumber.
- Fix: untuk memperbaiki bug pada kode sumber.
- Refactor: untuk melakukan refaktor pada kode sumber tanpa mengubah perilaku fungsional.
- Style: untuk melakukan perubahan pada gaya tampilan atau formatting pada kode sumber.
- Docs: untuk melakukan perubahan pada dokumentasi pada kode sumber.
- Test: untuk melakukan perubahan pada tes atau testing pada kode sumber.

Dalam membuat commit, kita juga perlu memperhatikan beberapa hal, seperti menggunakan pesan yang jelas dan deskriptif, memisahkan perubahan yang terkait dengan masalah atau tugas tertentu, menghindari commit dengan perubahan yang terlalu besar, menggunakan bahasa yang konsisten, dan menggunakan perangkat bantu commit seperti GitKraken atau SourceTree. Dengan mengikuti konvensi penamaan dan tips-tips tersebut, kita dapat membuat commit yang lebih terstruktur dan informatif, sehingga memudahkan pengelolaan dan tracking perubahan pada kode sumber.

## Tags
Tag dalam Git Versioning adalah cara untuk memberikan label pada versi tertentu dari kode sumber pada proyek kita. Dengan tag, kita dapat mengidentifikasi versi kode sumber yang penting, seperti versi rilis atau versi yang telah diuji dengan baik. Tag dapat membantu kita dalam melacak dan mengelola versi kode sumber pada proyek kita.

Sebagai contoh, bayangkan kamu telah menyelesaikan pengembangan pada aplikasi perangkat lunak untuk sebuah perusahaan. Kamu telah menguji aplikasi tersebut dan merasa yakin bahwa versi aplikasi tersebut siap untuk dirilis ke publik. Kamu dapat menandai versi tersebut dengan tag "v1.0" untuk menandai bahwa ini adalah versi pertama dari aplikasi tersebut yang siap untuk dirilis ke publik.

Tag juga berguna untuk melacak versi kode sumber yang memiliki fitur atau perubahan tertentu. Sebagai contoh, kamu dapat menandai versi kode sumber dengan tag "feature-login" untuk menunjukkan bahwa versi kode sumber tersebut berisi fitur baru untuk halaman login.

Dengan menggunakan tag, kita dapat dengan mudah mengidentifikasi versi kode sumber yang penting dan melacak perubahan yang dilakukan pada proyek kita seiring waktu. Tag juga dapat membantu kita dalam menentukan mana yang merupakan versi stabil atau rilis dari proyek kita.

### Semantic Version

Semantic Versioning (semver) adalah sistem penomoran versi yang digunakan untuk menyatakan kompatibilitas antara kode sumber yang berbeda. Penomoran versi menggunakan tiga angka: MAJOR.MINOR.PATCH.

- MAJOR: untuk perubahan yang tidak kompatibel dengan versi sebelumnya.
- MINOR: untuk perubahan yang menambahkan fitur baru, tetapi masih kompatibel dengan versi sebelumnya.
- PATCH: untuk perbaikan bug atau perbaikan kecil lainnya, tetapi masih kompatibel dengan versi sebelumnya.

### otomasi menggunakan github action
Dalam automasi Github Actions, Semantic Versioning dapat digunakan untuk otomatisasi penomoran versi setiap kali ada perubahan pada kode sumber. Beberapa langkah yang dapat dilakukan dalam automasi menggunakan Github Actions antara lain:

- Membuat file konfigurasi untuk semver.
- Menambahkan langkah dalam workflow Github Actions untuk melakukan penomoran versi.
- Menambahkan tag pada commit dengan nomor versi yang baru.
- Memperbarui file konfigurasi untuk versi berikutnya.

#### contoh configursi
```yaml
name: Semantic Versioning

on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v2
      - name: Setup Node.js
        uses: actions/setup-node@v2
        with:
          node-version: '14.x'
      - name: Install Dependencies
        run: npm install
      - name: Versioning
        id: versioning
        uses: anothrNick/github-tag-action@v1.27.0
        with:
          github-token: ${{ secrets.GITHUB_TOKEN }}
          prefix: 'v'
      - name: Update Version
        run: |
          sed -i "s/\"version\": \".*\"/\"version\": \"$(echo ${ {steps.versioning.outputs.tag} } | cut -c 2-)\"/g" package.json
          git add package.json
          git commit -m "Bump version to ${ {steps.versioning.outputs.tag} }"
      - name: Push Changes
        uses: ad-m/github-push-action@master
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          branch: ${{ github.ref }}
      - name: Create Release
        id: create_release
        uses: actions/create-release@v1
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
        with:
          tag_name: ${{ steps.versioning.outputs.tag }}
          release_name: Release ${{ steps.versioning.outputs.tag }}
          body: Automated release created by Github Actions
          draft: false
          prerelease: false
```


##### Penjelasan dari konfigurasi ini adalah sebagai berikut:

1. Konfigurasi ini akan dijalankan setiap kali ada push pada branch "main".
2. Konfigurasi ini akan menjalankan job "build" pada sebuah virtual machine ubuntu-latest.
3. Job ini akan menjalankan beberapa langkah, antara lain:
- Checkout: clone kode sumber dari repository Github.
- Setup Node.js: menginstall Node.js pada virtual machine.
- Install Dependencies: menginstall dependensi pada proyek menggunakan NPM.
- Versioning: menggunakan aksi dari Github Marketplace untuk membuat tag berdasarkan nomor versi terbaru dan menyimpan tag tersebut dalam output.
- Update Version: melakukan update pada file package.json dengan nomor versi terbaru dan melakukan commit.
- Push Changes: melakukan push pada branch yang sedang aktif.
- Create Release: membuat rilis baru pada Github dengan tag yang telah dibuat.

Dalam konfigurasi ini, kita menggunakan aksi "anothrNick/github-tag-action" dari Github Marketplace untuk melakukan penomoran versi dan membuat tag pada commit. Setelah itu, kita melakukan update pada file package.json dengan nomor versi terbaru dan melakukan commit serta push pada branch yang sedang aktif. Terakhir, kita membuat rilis baru pada Github dengan tag yang telah dibuat.

Dengan menggunakan automasi Github Actions, kita dapat menghemat waktu dan memudahkan pengelolaan versi pada proyek kita. Setiap kali terjadi perubahan pada kode sumber, Github Actions akan secara otomatis menambahkan nomor versi dan tag pada commit, sehingga memudahkan tracking perubahan pada proyek kita.

## Perbedaan
Branch, commit, dan tag adalah tiga konsep penting dalam Git Versioning. Ketiga konsep ini memiliki fungsi yang berbeda dan saling melengkapi satu sama lain dalam mengelola kode sumber pada proyek.

Branch digunakan untuk memisahkan pengembangan fitur baru, memperbaiki bug, atau melakukan eksperimen pada kode sumber tanpa mempengaruhi kode sumber utama. Branch memungkinkan pengembang untuk bekerja secara terpisah pada kode sumber dan kemudian mengintegrasikan perubahan tersebut kembali ke kode sumber utama melalui proses merge.

Commit digunakan untuk menyimpan perubahan pada kode sumber. Setiap kali ada perubahan pada kode sumber, kita harus melakukan commit dengan pesan deskriptif tentang perubahan yang telah kita lakukan pada kode sumber. Commit memungkinkan kita untuk kembali ke versi sebelumnya dari kode sumber jika dibutuhkan.

Tag digunakan untuk memberikan label pada versi tertentu dari kode sumber pada proyek kita. Tag membantu kita dalam melacak dan mengelola versi kode sumber pada proyek kita, serta membantu kita dalam menentukan mana yang merupakan versi stabil atau rilis dari proyek kita.

Dengan menggunakan branch, commit, dan tag secara bijak, kita dapat mengelola kode sumber pada proyek dengan efektif dan efisien, serta memudahkan kolaborasi dan pengembangan kode sumber secara tim.
