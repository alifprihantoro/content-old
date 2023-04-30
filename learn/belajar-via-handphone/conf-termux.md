# Cara Konfigurasi Termux untuk Pengguna Android
Selamat datang kembali! Pada artikel sebelumnya kita telah membahas mengenai Termux, sebuah aplikasi terminal emulator untuk perangkat Android yang dapat digunakan untuk menjalankan perintah terminal Linux pada perangkat mobile. Pada artikel kali ini, kita akan membahas lebih lanjut mengenai bagaimana melakukan konfigurasi pada Termux.

## Konfigurasi Default pada Termux
Untuk melakukan konfigurasi pada Termux, pertama-tama pengguna dapat membuka aplikasi Termux, kemudian masuk ke menu pengaturan dengan mengetikkan perintah termux-setup-storage. Setelah itu, pengguna dapat mengubah beberapa pengaturan default seperti ukuran font, warna tema, dan keyboard eksternal.

untuk melakukan hal tersebut, hal pertama yang kalian butuhkan ialah `termux style` yang bisa di download di f-droid. Jika sudah diinstall. Tahan pada layar sampai muncul pop up. Lalu pilih style. Dan silahkan atur sesuai prefrensi kalian. Kalian juga bisa menambahkan prefensi kalian di `~/.termux/font.ttf` atau `~/.termux/colors.properties`.

## Menambahkan Paket Tambahan pada Termux
Pengguna juga dapat menginstal paket tambahan pada Termux seperti aplikasi text editor atau bahasa pemrograman. Untuk melakukan hal ini, pengguna dapat menggunakan package manager bawaan Termux dengan mengetikkan perintah `pkg install <nama-pkg>`. 
contoh install pkg :
```bash
apk update -y
apk upgrade -y
apk install bat nodejs neovim python gh git wget openssh zsh lsd fzf tmux ripgrep termux-api proot proot-distro
```

## Mengonfigurasi Shortcut Keyboard
Untuk memudahkan penggunaan Termux, pengguna juga dapat mengonfigurasi shortcut keyboard untuk menjalankan perintah tertentu secara cepat. Hal ini dapat dilakukan dengan mengedit file `.termux/termux.properties` dan menambahkan baris kode yang sesuai dengan perintah yang diinginkan.

contoh configurasi yang saya terapkan :
```bash
### Uncomment to let Termux start in full screen mode.
fullscreen = true

### Cursor blink rate. Values 0, 100 - 2000.
terminal-cursor-blink-rate = 500

# Open a new terminal with ctrl + 3 (volume down + t)
shortcut.create-session = ctrl + 3

# Go one session down with (for example) ctrl + 3
shortcut.next-session = ctrl + 2

# Go one session up with (for example) ctrl + 1
shortcut.previous-session = ctrl + 1

# delete this if <C-Space> already works
ctrl-space-workaround = true
### Two rows with more keys
extra-keys = [[\
{macro: "CTRL a CTRL k", display: ↑}, \
{macro: "CTRL a CTRL j", display: ↓}, \
{macro: "CTRL a c", display: +}, \
{macro: "CTRL a :", display: cmd}, \
'DEL',\
'KEYBOARD',\
'DRAWER'\
]]
### Force black colors for drawer and dialogs
# use-black-ui = true
allow-external-apps = true
```

## Mengaktifkan Akses Root pada Termux
> tidak disarankan untuk melakukan root, tanpa pengetahuan mengenai root itu sendiri. resiko ditanggung kalian.

Dalam beberapa kasus, pengguna Termux mungkin perlu menggunakan akses root pada perangkat Android mereka. Untuk mengaktifkan akses root pada Termux, pengguna dapat menggunakan aplikasi "Magisk" yang dapat diunduh melalui Google Play Store.

## bebetapa sumber belajar termux
- [termux wiki](https://wiki.termux.com/wiki/Main_Page)
- [video orang](https://youtube.com/playlist?list=PLghZgCW9sgucSyW3eqx3CEZAzAR3KIsMG)

## penutup
Melalui artikel ini, diharapkan pembaca dapat memahami cara melakukan konfigurasi pada aplikasi Termux dan dapat memanfaatkannya dengan optimal. Meskipun konfigurasi yang telah dijelaskan dalam artikel ini hanya bersifat dasar, namun pembaca dapat terus mengembangkan pengetahuan dan keterampilan mereka dengan mempelajari lebih lanjut tentang aplikasi ini.

Dengan semakin banyaknya fitur dan penggunaan aplikasi mobile pada saat ini, aplikasi seperti Termux dapat menjadi alternatif yang sangat berguna untuk menjalankan perintah terminal Linux pada perangkat mobile. Oleh karena itu, mari terus belajar dan mengembangkan kemampuan kita dalam memanfaatkan teknologi yang ada untuk meningkatkan efisiensi dan produktivitas kita. Terima kasih telah membaca artikel ini!
