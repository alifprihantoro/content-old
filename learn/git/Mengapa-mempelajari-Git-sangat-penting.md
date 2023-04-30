# Belajar Git
Halo semua, selamat datang di MuryP! Apakah kalian pernah mendengar tentang Git? Git adalah sistem pengontrol versi yang sangat berguna bagi para pengembang perangkat lunak. Dengan Git, Anda bisa melacak perubahan kode sumber dan bekerja secara kolaboratif dengan tim Anda dengan mudah. Di kelas ini, kita akan mempelajari dasar-dasar Git, seperti bagaimana menginstal dan mengkonfigurasinya, membuat repositori, melakukan commit, dan banyak lagi. Mari kita mulai belajar Git dan tingkatkan kemampuan pengembangan perangkat lunak kita bersama-sama!
## Alasan mengapa belajar Git
Ada banyak alasan mengapa penting untuk mempelajari Git sebagai pengembang perangkat lunak. Berikut beberapa alasan mengapa Anda harus mempelajari Git:

- Melacak Perubahan Kode Sumber: Git memungkinkan Anda melacak setiap perubahan yang terjadi pada kode sumber proyek. Ini sangat berguna ketika bekerja dengan tim atau jika Anda perlu memulihkan kode sumber ke versi sebelumnya.
- Kolaborasi yang Efektif: Dalam proyek perangkat lunak yang besar, kolaborasi dan koordinasi dengan tim sangat penting. Dengan Git, Anda dapat bekerja secara bersamaan pada kode sumber yang sama, menggabungkan perubahan, dan memecahkan konflik dengan mudah.
- Versi Kontrol: Git memungkinkan Anda untuk bekerja dengan beberapa versi kode sumber yang berbeda secara bersamaan. Dengan membuat cabang (branch) pada Git, Anda dapat mengembangkan kode sumber baru tanpa mengganggu kode sumber utama.
- Mengelola Proyek: Dengan Git, Anda dapat mengelola proyek Anda dengan lebih efisien. Anda dapat memantau kemajuan proyek, melacak masalah (issues), mengatasi konflik kode sumber, dan memastikan setiap anggota tim memiliki versi terbaru dari kode sumber.
- Populer dan Mendukung Industri: Git adalah alat pengontrol versi yang paling populer digunakan oleh pengembang perangkat lunak di seluruh dunia. Banyak perusahaan besar, termasuk Google, Facebook, dan Microsoft, menggunakan Git sebagai alat pengontrol versi mereka.
- Dengan alasan tersebut, tidak mengherankan bahwa Git menjadi alat yang sangat penting bagi pengembang perangkat lunak. Jadi, mari kita mulai belajar Git dan tingkatkan kemampuan pengembangan perangkat lunak kita bersama-sama!
## Cara menginstall Git
Jika pengguna menggunakan sistem operasi berbasis Debian seperti Ubuntu, Debian, atau Linux Mint, mereka dapat menggunakan utilitas manajemen paket apt (Advanced Packaging Tool) untuk menginstal Git. Berikut adalah langkah-langkah yang dapat diikuti oleh pengguna yang menggunakan apt:

- Buka terminal dengan menekan tombol Ctrl+Alt+T.

- Perbarui daftar paket dengan perintah: sudo apt update.

- Instal Git dengan perintah: sudo apt install git.

- Verifikasi instalasi Git dengan memeriksa versi Git: git --version.

Sedangkan untuk pengguna sistem operasi berbasis RPM seperti Fedora, CentOS, atau Red Hat, mereka dapat menggunakan utilitas manajemen paket yum atau dnf. Berikut adalah langkah-langkah yang dapat diikuti oleh pengguna yang menggunakan yum:

- Buka terminal dengan menekan tombol Ctrl+Alt+T.

- Perbarui daftar paket dengan perintah: sudo yum update.

- Instal Git dengan perintah: sudo yum install git.

- Verifikasi instalasi Git dengan memeriksa versi Git: git --version.

Sedangkan untuk pengguna sistem operasi berbasis pkg seperti FreeBSD atau macOS, mereka dapat menggunakan utilitas manajemen paket pkg. Berikut adalah langkah-langkah yang dapat diikuti oleh pengguna yang menggunakan pkg:

- Buka terminal dengan menekan tombol Command+Space, lalu ketik "Terminal" dan tekan Enter.

- Perbarui daftar paket dengan perintah: sudo pkg update.

- Instal Git dengan perintah: sudo pkg install git.

- Verifikasi instalasi Git dengan memeriksa versi Git: git --version.

Itulah cara instalasi Git pada beberapa sistem operasi dengan menggunakan utilitas manajemen paket yang berbeda-beda. Setelah Git terinstal, pengguna dapat memulai penggunaan Git untuk mengelola kode sumber proyek mereka.

## Contoh Penggunaan Git
Berikut ini adalah beberapa perintah dasar Git dan fungsinya:

- git init: digunakan untuk membuat repositori Git baru pada direktori yang ditunjuk.

- git add: digunakan untuk menambahkan file atau direktori yang sudah diubah pada staging area sebelum melakukan commit.

- git commit: digunakan untuk menyimpan snapshot dari perubahan yang telah dilakukan pada repositori.

- git status: digunakan untuk melihat status perubahan pada repositori, seperti file apa saja yang telah diubah atau ditambahkan.

- git diff: digunakan untuk melihat perubahan pada file yang belum ditambahkan ke staging area.

- git log: digunakan untuk melihat riwayat commit pada repositori.

- git branch: digunakan untuk membuat cabang baru pada repositori atau melihat daftar cabang yang ada.

- git checkout: digunakan untuk beralih antara cabang atau memulihkan file yang sudah dihapus.

- git merge: digunakan untuk menggabungkan cabang ke cabang utama.

- git remote: digunakan untuk menambah atau menghapus remote repository.

- git pull: digunakan untuk mengambil perubahan terbaru dari remote repository dan menggabungkannya dengan repositori lokal.

- git push: digunakan untuk mengunggah perubahan pada repositori lokal ke remote repository.

Itulah beberapa perintah dasar Git dan fungsinya. Dengan memahami dan menguasai perintah-perintah ini, pengguna dapat memulai penggunaan Git untuk mengelola proyek perangkat lunak mereka dengan lebih efisien dan efektif.

## Mengunggah hasil kode
Setelah melakukan di local kita ingin kode kita bisa dilihat dan diedit orang lain. Nah untuk mengunggah hasil kode yang telah Anda buat menggunakan Git, Anda dapat menggunakan layanan remote seperti GitHub, GitLab, atau Bitbucket. Layanan remote ini memungkinkan Anda untuk menyimpan repositori kode sumber Anda secara online dan berkolaborasi dengan tim Anda. Dengan menggunakan layanan remote, Anda juga dapat memantau kemajuan proyek, mengelola masalah (issues), dan memfasilitasi review kode sumber dari tim Anda. Anda juga dapat membuat repositori pribadi atau publik, tergantung pada kebutuhan Anda. Untuk memulai, Anda dapat mendaftar di layanan remote pilihan Anda dan mengikuti panduan mereka untuk mulai mengunggah kode sumber Anda. Jangan ragu untuk menjelajahi berbagai fitur yang ditawarkan oleh layanan remote tersebut untuk mengoptimalkan penggunaan Git dan meningkatkan kolaborasi dengan tim Anda!

## Penutup
Sekian kelas dasar Git yang telah kita pelajari hari ini. Semoga dengan mempelajari dasar-dasar Git ini, kita dapat lebih efisien dalam mengelola proyek perangkat lunak kita. Selain itu, kita juga dapat bekerja dengan tim dengan lebih mudah dan kolaboratif menggunakan Git. Ingatlah untuk selalu berlatih dan mengembangkan keterampilan Git kita, karena Git merupakan keterampilan penting yang sangat dicari dalam dunia industri perangkat lunak saat ini. Terima kasih telah mengikuti kelas ini, semoga sukses selalu!
