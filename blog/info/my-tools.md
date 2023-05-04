# List Tools yang saya gunakan
Dalam dunia pengembangan perangkat lunak, ada banyak alat dan perangkat lunak yang dapat membantu meningkatkan produktivitas dan efisiensi dalam menulis kode, bekerja dengan repository, dan melakukan manajemen sistem. Di antara alat-alat ini, ada beberapa alat yang sangat berguna dan sering digunakan oleh pengembang perangkat lunak. Dalam artikel ini, kita akan membahas enam alat teratas yang digunakan oleh para pengembang, yaitu fzf, nvim, git, GitHub CLI, tmux, dan ssh.

## fzf
fzf adalah alat pencarian perintah baris yang cepat dan efisien. Dengan fzf, Anda dapat mencari file, direktori, dan bahkan string di seluruh proyek Anda dengan sangat cepat. fzf sangat berguna ketika Anda bekerja dengan berbagai proyek dan membutuhkan cara yang cepat dan mudah untuk menavigasi antara file dan direktori. fzf juga terintegrasi dengan banyak alat dan perangkat lunak, termasuk Vim, Tmux, dan Zsh, sehingga sangat mudah digunakan.
### Link
- Repo: https://github.com/junegunn/fzf
- Dokumen: https://github.com/junegunn/fzf#usage
### Cara Install:
```bash
# Untuk Linux/MacOS
$ git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf
$ ~/.fzf/install

# Untuk Windows (dengan PowerShell)
git clone --depth 1 https://github.com/junegunn/fzf.git $env:USERPROFILE\.fzf
$env:USERPROFILE\.fzf\install
```

## nvim
nvim adalah pengembangan dari Vim, editor teks yang sangat populer di kalangan pengembang perangkat lunak. nvim menyediakan banyak fitur canggih untuk pengembang, termasuk dukungan untuk banyak bahasa pemrograman, dukungan untuk banyak plugin, dan dukungan untuk pengaturan berkas konfigurasi yang sangat fleksibel. nvim juga dapat dijalankan di terminal atau mode grafis, yang memungkinkan pengguna untuk memilih lingkungan yang paling sesuai dengan preferensi mereka.
### Link
- Repo: https://github.com/neovim/neovim
- Dokumen: https://neovim.io/doc/user/
### Cara Install:
```bash
# Untuk Linux/MacOS
$ sudo apt-get install neovim    # Debian/Ubuntu
$ sudo pacman -S neovim          # Arch/Manjaro
$ brew install neovim            # MacOS
```
> Untuk Windows Download installer dari https://neovim.io/

## git
git adalah alat pengendali versi yang sangat populer yang digunakan oleh para pengembang perangkat lunak. Dengan git, Anda dapat melakukan manajemen versi pada kode Anda, membuat branch, merge kode, dan banyak lagi. git juga terintegrasi dengan banyak platform hosting seperti GitHub dan GitLab, yang memungkinkan pengembang untuk berkolaborasi dengan mudah pada proyek bersama.
### Link
- Repo: https://github.com/git/git
- Dokumen: https://git-scm.com/docs
### Cara Install:
```bash
# Untuk Linux/MacOS
$ sudo apt-get install git     # Debian/Ubuntu
$ sudo pacman -S git           # Arch/Manjaro
$ brew install git             # MacOS
```
> Untuk Windows Download installer dari https://git-scm.com/downloads

## GitHub CLI
GitHub CLI adalah alat baris perintah yang memungkinkan pengguna untuk mengelola repository mereka di GitHub dari terminal. Dengan GitHub CLI, Anda dapat membuat repository baru, membuat issue, menambahkan kolaborator, dan bahkan melakukan merge pull request, semuanya dari terminal. Ini sangat berguna ketika Anda ingin berinteraksi dengan GitHub tetapi tidak ingin meninggalkan terminal.
### Link
- Repo: https://github.com/cli/cli
- Dokumen: https://cli.github.com/manual/
### Cara Install:
```bash
# Untuk Linux/MacOS
$ sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-key C99B11DEB97541F0
$ sudo apt-add-repository https://cli.github.com/packages
$ sudo apt update
$ sudo apt install gh
```
> Untuk Windows Download installer dari https://cli.github.com/

## tmux
tmux adalah alat multiplexer terminal yang memungkinkan pengguna untuk mengatur dan mengelola beberapa session terminal dalam satu window. Dengan tmux, Anda dapat membuka beberapa tab dan jendela terminal dalam satu window, menjadikannya sangat efisien dan memungkinkan pengguna untuk melakukan banyak tugas sekaligus. tmux juga terintegrasi dengan banyak alat lain, termasuk fzf dan nvim, sehingga sangat mudah digunakan oleh para pengembang.
### Link
- Repo: https://github.com/tmux/tmux
- Dokumen: https://man.tmux.io/
### Cara Install:
```bash
# Untuk Linux/MacOS
$ sudo apt-get install tmux   # Debian/Ubuntu
$ sudo pacman -S tmux         # Arch/Manjaro
$ brew install tmux           # MacOS
```
> Untuk Windows Download installer dari https://github.com/AlexanderOMara/WSL-TTY/releases

## ssh
ssh adalah protokol jaringan yang digunakan untuk mengakses shell remote secara aman. Dengan ssh, pengguna dapat mengakses mesin remote dari jarak jauh dan menjalankan perintah shell di mesin tersebut. Ini sangat berguna ketika Anda ingin mengakses mesin jarak jauh atau server dan melakukan tugas-tugas administratif pada mesin tersebut, seperti instalasi perangkat lunak atau konfigurasi sistem. ssh juga digunakan secara luas dalam deployment otomatis dan pengelolaan sistem, karena memungkinkan pengguna untuk mengakses mesin jarak jauh dan menjalankan perintah dari jarak jauh.
### Link
- Dokumen: https://man.openbsd.org/ssh.1
### Cara Install:
SSH sudah terinstal secara default pada kebanyakan sistem operasi modern, namun jika belum, dapat diinstal dengan cara yang sama seperti fzf.

## bat
bat adalah pengganti cat, perintah baris untuk membaca isi berkas. Perintah ini memberikan fitur yang lebih baik seperti sintaksis warna untuk berbagai jenis berkas, tampilan nomor baris, dan kemampuan untuk membaca isi berkas ZIP. Dengan bat, pengembang dapat dengan mudah membaca isi berkas tanpa perlu membuka editor teks.
### Link
- Repo: https://github.com/sharkdp/bat
- Dokumen: https://github.com/sharkdp/bat#usage
### Cara Install:
```bash
# Untuk Linux/MacOS
$ sudo apt-get install bat     # Debian/Ubuntu
$ sudo pacman -S bat           # Arch/Manjaro
$ brew install bat             # MacOS
```
> Untuk Windows Download installer dari https://github.com/sharkdp/bat/releases

## lsd
lsd (LSDeluxe) adalah alternatif yang lebih baik dari perintah ls pada sistem operasi Linux dan macOS. lsd menampilkan isi direktori dengan tampilan yang lebih baik, seperti ikon dan warna. Ini membuat pengguna lebih mudah dalam membaca dan memahami struktur direktori, terutama ketika bekerja dengan banyak file dan direktori.
### Link
- Repo: https://github.com/Peltoche/lsd
- Dokumen: https://github.com/Peltoche/lsd#usage
### Cara Install
```bash
# Untuk Linux/MacOS
$ sudo apt-get install lsd     # Debian/Ubuntu
$ sudo pacman -S lsd           # Arch/Manjaro
$ brew install lsd             # MacOS

```
> Untuk Windows Download installer dari https://github.com/Peltoche/lsd/releases

## zsh
zsh (Z Shell) adalah shell yang lebih canggih daripada shell standar pada sistem operasi seperti Bash. zsh menawarkan banyak fitur dan kemampuan, termasuk pengayaan sintaksis untuk memudahkan penulisan perintah, dukungan untuk tema dan konfigurasi yang fleksibel, dan banyak lagi. zsh juga mudah digunakan dan dapat dikonfigurasi dengan mudah oleh pengembang.
### Link
- Repo: https://github.com/zsh-users/zsh
- Dokumen: https://www.zsh.org/doc/
### Cara Install:
```bash
# Untuk Linux/MacOS
$ sudo apt-get install zsh     # Debian/Ubuntu
$ sudo pacman -S zsh           # Arch/Manjaro
$ brew install zsh             # MacOS

```
> Untuk Windows Download installer dari https://www.zsh.org/

## powerlevel10k
powerlevel10k adalah tema Zsh yang sangat populer dan membantu dalam meningkatkan produktivitas pengembang. powerlevel10k menyediakan tampilan terminal yang indah dan beragam, termasuk kemampuan untuk menampilkan status sistem, fitur pencarian perintah, dan banyak lagi. powerlevel10k dapat dengan mudah dikustomisasi dan disesuaikan dengan preferensi pengembang.
### Link
- Repo: https://github.com/romkatv/powerlevel10k
- Dokumen: https://github.com/romkatv/powerlevel10k#quick-installation
### Cara Install:
```bash
# Instal Oh My Zsh
$ sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

# Install Powerlevel10k
$ git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/.oh-my-zsh/themes/powerlevel10k
$ echo 'source ~/.oh-my-zsh/themes/powerlevel10k/powerlevel10k.zsh-theme' >> ~/.zshrc
```

## live server
live server adalah alat pengembangan web yang memungkinkan pengembang untuk melihat perubahan pada halaman web secara real-time saat mengedit kode HTML, CSS, atau JavaScript. Dengan live server, pengembang dapat mengedit kode dan melihat perubahan pada halaman web dengan cepat tanpa perlu memuat ulang halaman secara manual.
### Link
- Repo: https://github.com/ritwickdey/vscode-live-server
- Dokumen: https://github.com/ritwickdey/vscode-live-server#usage
### Cara Install:
Install melalui ekstensi pada Visual Studio Code atau dapat juga diinstal secara global dengan npm:
```bash
$ npm install -g live-server
```

## Kesimpulan
Dalam dunia pengembangan perangkat lunak, ada banyak alat dan perangkat lunak yang dapat membantu meningkatkan produktivitas dan efisiensi. Dalam artikel ini, kita telah membahas enam alat yang sangat berguna dan sering digunakan oleh para pengembang, seerti tools yang saya gunakan di atas. Dengan menggunakan alat-alat ini, para pengembang dapat meningkatkan efisiensi dan produktivitas mereka dalam menulis kode, bekerja dengan repository, dan melakukan manajemen sistem. Semua alat ini sangat mudah digunakan dan tersedia secara gratis di berbagai platform dan sistem operasi.
