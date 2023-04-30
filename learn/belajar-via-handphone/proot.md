# Menggunakan prrot untuk pengganti root
Termux adalah aplikasi terminal emulator yang memungkinkan pengguna untuk menjalankan perintah Linux pada perangkat Android mereka. Dengan menggunakan Termux, pengguna dapat melakukan tugas-tugas seperti mengelola file, menginstal paket, dan menjalankan skrip pada perangkat Android mereka. Namun, ada beberapa batasan pada penggunaan Termux karena perangkat Android bukanlah sistem operasi desktop.

Untuk mengatasi batasan tersebut, Termux Proot hadir sebagai fitur tambahan pada aplikasi Termux. Termux Proot memungkinkan pengguna untuk menjalankan sistem operasi Linux pada perangkat Android mereka, dan mengakses perintah dan program yang tidak tersedia secara default di Termux.

Salah satu keuntungan penggunaan Termux Proot adalah kemampuannya untuk menjalankan beberapa aplikasi GUI pada perangkat Android, seperti Chromium, Firefox, dan GIMP. Pengguna dapat menjalankan aplikasi desktop pada perangkat Android mereka, sehingga dapat digunakan untuk tugas yang memerlukan antarmuka grafis.

Namun, penggunaan aplikasi GUI pada Termux Proot memerlukan sumber daya sistem yang lebih besar dibandingkan dengan menggunakan perintah terminal saja, sehingga dapat memengaruhi kinerja perangkat secara keseluruhan. Beberapa aplikasi GUI mungkin juga tidak dapat dijalankan dengan benar di lingkungan Termux Proot, terutama jika aplikasi tersebut memerlukan dukungan hardware khusus atau mengakses perangkat keras secara langsung.

Meskipun demikian, dengan menggunakan aplikasi GUI pada Termux Proot, pengguna dapat memperluas kemampuan perangkat.
## Memilih Proot Distro

Proot distro adalah sistem operasi Linux yang dijalankan menggunakan Termux Proot pada perangkat Android. Dengan menggunakan proot distro, pengguna dapat menjalankan sistem operasi Linux lengkap pada perangkat Android mereka, dan mengakses perintah dan program yang tidak tersedia secara default di Termux.

Beberapa proot distro yang populer digunakan pada Termux Proot antara lain:

- Debian: Proot distro Debian adalah sistem operasi Linux yang stabil dan populer di kalangan pengembang dan sistem administrator. Debian memiliki repositori paket yang kaya dan mendukung berbagai platform dan arsitektur.
 
- Ubuntu: Proot distro Ubuntu adalah sistem operasi Linux berbasis Debian yang juga populer di kalangan pengguna desktop. Ubuntu memiliki antarmuka pengguna yang mudah digunakan dan didukung oleh komunitas pengembang yang besar.
 
- Arch Linux: Proot distro Arch Linux adalah sistem operasi Linux rolling release yang didesain untuk pengguna yang ingin meng-customize sistem operasi mereka secara penuh. Arch Linux memiliki paket dan repositori yang sangat lengkap dan mendukung berbagai platform dan arsitektur.
 
- Kali Linux: Proot distro Kali Linux adalah sistem operasi Linux yang didesain khusus untuk pengujian penetrasi dan keamanan jaringan. Kali Linux memiliki paket dan repositori yang khusus untuk pengujian penetrasi dan keamanan jaringan.

Untuk perbedaan yang paling terasa saat menggunakan distro tersebut, ialah masalah repository. Untuk penggunaan sehari-hari, saya lebih prefer ke debian. Karena untuk proot distro di termux hanya disediakan kosongan (desktop, vnc install sendiri). Kecuali jika kalian menggunakan [officiall kali linux](https://www.kali.org/docs/nethunter/nethunter-rootless/), yang mana tools nya lengkap, dan sudah memiliki gui yang sudah di setting.

## install
- Buka aplikasi Termux dan jalankan perintah berikut untuk menginstal proot dan proot distro :
```bash
pkg update -y
pkg upgrade -y
pkg install proot proot-distro -y
```
- pilih distro yang ingin di install, contohnya saya akan menhinstall proot distro debian.
```bash
proot-distro install debian
```
- untuk melihat list distro, ktikkan
```bash
proot-distro list
```
- untuk informasi lebih lanjut silahkan ketik `proot-distro help` atau kunjungi official document proot [di sini](https://github.com/termux/proot-distro)
> untuk contoh configurasinya, kalian bisa lihat [di sini](https://github.com/muryp/cli-config)
## penutup

Dalam artikel ini, kita telah mempelajari tentang proot dan proot distro yang memungkinkan pengguna Android untuk memperluas kemampuan perangkat mereka. Namun, masih banyak lagi keterampilan dan pengetahuan teknologi yang perlu dipelajari untuk menghadapi tantangan masa depan. Salah satunya adalah front-end development, yang sangat penting dalam membuat tampilan dan interaksi pengguna yang menarik dan intuitif untuk aplikasi web dan seluler. Jika Anda ingin memperluas keterampilan front-end Anda, kunjungi [Belajar front End](/learn/front-end-webdev) untuk membaca artikel-artikel menarik dan berguna tentang pengembangan front-end dan teknologi lainnya. Teruslah belajar dan berkembang untuk meraih kesuksesan di masa depan!
