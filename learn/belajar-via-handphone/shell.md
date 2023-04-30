# Command shell pada termux
Termux merupakan emulator, yang sebagian besar penggunaanya menggunakan shell command. Walaupun tidak semua command linux berjalan semestinya. Shell sendiri adalah program antarmuka yang digunakan untuk berinteraksi dengan sistem operasi dan mengelola perintah dan aplikasi pada lingkungan Linux. Ada beberapa jenis shell yang tersedia, termasuk Bash, Zsh, dan Fish. Ketiganya memiliki fitur dan kemampuan yang berbeda, sehingga memilih shell yang tepat bisa menjadi kunci untuk meningkatkan produktivitas dan efisiensi dalam bekerja dengan sistem Linux.

## Perbedaan antara bash, zsh dan fish
- Bash (Bourne-Again SHell) adalah shell standar pada sebagian besar sistem Linux. Bash adalah shell yang cukup sederhana dan mudah digunakan untuk pemula dan ahli. Namun, Bash kurang fleksibel dalam hal konfigurasi dan penyesuaian.

- Zsh (Z SHell) adalah shell yang lebih kuat dan lebih fleksibel daripada Bash. Zsh memiliki banyak fitur bawaan yang tidak dimiliki oleh Bash, seperti penyelesaian otomatis, manajemen riwayat perintah yang lebih baik, dan banyak lagi. Zsh juga mudah dikonfigurasi dan dapat disesuaikan dengan preferensi pengguna.

- Fish (Friendly Interactive SHell) adalah shell yang lebih modern dan intuitif daripada Bash atau Zsh. Fish menawarkan banyak fitur yang berguna, seperti penyelesaian otomatis yang sangat canggih, koreksi kesalahan, dan tampilan warna yang menarik. Namun, karena kekuatan dan fleksibilitasnya yang besar, Fish mungkin membutuhkan waktu yang lebih lama untuk dipelajari bagi pemula.

Pilihan shell mana yang harus digunakan tergantung pada preferensi dan kebutuhan pengguna. Jika Anda seorang pemula atau tidak memerlukan banyak fitur tambahan, Bash dapat menjadi pilihan yang tepat. Namun, jika Anda memerlukan fitur yang lebih canggih dan lebih fleksibilitas dalam konfigurasi, Zsh atau Fish dapat menjadi pilihan yang lebih baik.

## configurasi shell untuk menyingkat command dan otomisasi
Dalam penggunaan sehari-hari, mungkin kita sering menjumpai kebutuhan akan penyederhanaan perintah. Seperti contohnya, ketika kalain menggunakan sebuah aplikas, terkadang aplikasi tersebut memiliki flag yang panjang. Maka untuk mempersingkat hal itu kita bisa menggunakan alias atau function agar tidak perlu menulis baris kode yang begitu panjang.

### contoh penggunaan alias
- Membuat alias untuk perintah ls -al menjadi lsa
```bash
alias lsa="ls -al"
```
- penggunaan alias dan function untuk melakukan pencarian dengan fuzzy finder
```bash
FILEFUZZY(){
vim_w_fzf=$(FZF --preview)
while [ "$vim_w_fzf" != "" ]
do 
$1 $vim_w_fzf
break
done
}
# lvim
alias vf='FILEFUZZY nvim'
```

Setelah membuat alias, pengguna dapat memanggil perintah yang sesuai dengan alias yang telah ditetapkan dengan mengetikkan alias yang diberikan di terminal. Misalnya, untuk menggunakan alias lsa yang telah kita buat, cukup mengetikkan lsa pada terminal, dan shell akan mengeksekusi perintah ls -al.

Namun, perlu diingat bahwa alias hanya berlaku pada shell yang sama dengan dimana alias tersebut dibuat. Alias tidak akan tersedia saat shell ditutup atau ketika pengguna beralih ke shell yang berbeda. Untuk membuat alias yang tersedia setiap kali shell dimulai, pengguna dapat menambahkan alias ke dalam file konfigurasi shell seperti .bashrc.

### kelebihan dan kekurangan alias dan function
Alias dan function adalah fitur yang sangat berguna di shell Linux. Namun, kedua fitur ini memiliki kelebihan dan kekurangan masing-masing. Berikut adalah beberapa kelebihan dan kekurangan penggunaan alias dan function di shell Linux:

#### Kelebihan Alias:

- Membuat perintah yang lebih mudah diingat dengan menetapkan alias yang lebih pendek.
- Mempercepat waktu kerja dengan menghemat waktu ketik dengan mengganti perintah yang lebih panjang menjadi alias yang lebih pendek.
- Menghindari kesalahan pengetikan dengan mengganti perintah yang rumit atau panjang menjadi alias yang lebih sederhana.
##### Kekurangan Alias:

- Tidak dapat menampung argumen tambahan seperti yang bisa dilakukan oleh function.
- Tidak dapat dijalankan secara interaktif dan tidak dapat dipanggil dari dalam skrip bash.

##### Kelebihan Function:

- Dapat menampung argumen tambahan dan menjalankan fungsi yang lebih kompleks dibandingkan dengan alias.
- Dapat dipanggil dari dalam skrip bash dan dijalankan secara interaktif.

##### Kekurangan Function:

- Fungsi yang rumit dan kompleks dapat membuat kode sulit dibaca dan dipahami oleh orang lain.
- Memerlukan sedikit usaha untuk membuat dan mengedit function dibandingkan dengan alias.

Penggunaan alias dan function dapat meningkatkan produktivitas dan efisiensi kerja pengguna di lingkungan shell Linux. Pengguna harus mengevaluasi kebutuhan mereka dan memilih fitur yang paling cocok untuk pekerjaan mereka.

> contoh configurasi yang saya gunakan https://github.com/muryp/cli-config

## Penutup

Dalam artikel ini, kita telah membahas tentang shell Linux, yaitu Bash, Zsh, dan Fish. Kita telah mengetahui apa itu shell dan beberapa perintah yang sering digunakan dalam penggunaan shell. Selain itu, kita juga telah mempelajari penggunaan alias dan function untuk mempercepat dan mempermudah pekerjaan di shell Linux.

Untuk artikel selanjutnya, kita akan membahas tentang nvim, yaitu editor teks yang sangat populer di Linux. Dalam artikel tersebut, kita akan membahas fitur-fitur yang disediakan oleh nvim dan bagaimana cara menggunakannya untuk meningkatkan produktivitas pengguna. Jangan lewatkan artikel selanjutnya dan terus ikuti kami, untuk mendapatkan informasi dan tips terbaru seputar teknologi.
