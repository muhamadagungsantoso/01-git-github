# Instalasi Git

Sebelum melakukan instalasi Git dengan sistem operasi windows pastikan sudah terinstall text editor untuk keberhasilan instalasi dan nantinya akan digunakan sebagai text editor default Git yang akan diinstal.

Berikut adalah langkah-langkah instalasi git dengan sistem operasi Windows:

1. Download Aplikasi Git di [website resmi](https://git-scm.com/downloads), pilih sistem operasi windows yang sesuai
2. Buka file yang telah didownload, akan muncul setup untuk instalasi Git, klik next
3. Pilih lokasi penyimpanan instalasi Git, secara default akan tersimpan di *C:\Program Files\Git*, klik next
4. Pada *Select Components* biarkan secara default, klik next
5. Pilih Start Menu Folder, secara default folder yang digunakan bernama Git, ubah namanya jika ingin mengubah, klik next
6. Pilih text editor sesuai dengan text editor yang ada pada komputer anda, klik next
7. Pada *Adjusting your PATH environment* pilih pilihan *Use Git from the Windows Command Prompt* supaya Git bisa berjalan pada Git bash dan Command Prompt di Windows, klik next
8. Pilih *Use the OpenSSL library* untuk mengakses repo di GitHub atau repo repo lainnya, klik next
9. Pilih pilihan pertama untuk konversi CRLF
10. Pilih MinTTY untuk memilih terminal yang digunakan untuk mengakses Git Bash, klik next
11. Pilih *Enable file system caching* dan *Enable Git Credencial Manager*, klik Install
12. Tunggu proses instalasi selesai lalu klik Finish
13. Git sudah terinstall di komputer anda berupa Git Bash dan Git GUI

# Konfigurasi Git

Konfigurasi Git bisa dilakukan melalui Git Bash. Konfigurasi pada Git adalah memberitahukan username dan email yang digunakan untuk mendaftarkan akun GitHub, jadi hal pertama yang harus dilakukan adalah membuat akun GitHub terlebih dahulu sebelum konfigurasi Git. Setelah membuka aplikasi Git Bash anda bisa melakukan konfigurasi Git dengan mengetikkan perintah berikut:

```bash
git config --global user.name "Nama Github anda"
git config --global user.email email@test.com
```

Untuk mengecek konfigurasi Git bisa menggunakan perintah:

```bash
git config --list
```

Konfigurasi dilakukan sekali saja kecuali jika ingin mengubah nama dan email.

# Mengelola repositori

Berikut adalah tahap-tahap mengelola atau repo:

## Membuat Repo
Membuat repo dilakukan di GitHub dengan cara:

1. Pada halaman setelah login, klik tanda +, lalu klik New repository
2. Isikan nama repo, deskripsi, dan lisensi jika diperlukan
3. Klik `Create Repository` untuk membuat repo

## Clone Repo
`Clone` adalah proses menduplikasi remote dan isi dari repo di GitHub ke komputer lokal. Caranya dengan mengetikkan perintah `git clone https://github.com/username/namarepo` pada Git Bash

## Perintah-perintah untuk mengelola Repo
Berikut adalah perintah-perintah untuk mengelola repo di Git:

### Mengubah nama branch
Secara default nama branch di git adalah master, untuk mengubahnya kita harus berpindah dulu ke repo yang ingin diubah nama branch lalu ketikkan perintah `git branch -m main`. Ubah menjadi main supaya sama dengan branch di GitHub.

### Mengubah isi repo tanpa branching dan merging
Jika terdapat perubahan pada isi repo kita harus menandai perubahan tersebut dengan melakukan commit.

Buka folder repo ke text editor, lalu tambahkan file beri nama `README.md`. Lalu ketikkan perintah:

```bash
git add .
git commit -m "menambahkan file README.md"
```

### Push Repo
`Push` adalah proses mengupload perubahan atau isi repo dari komputer lokal ke GitHub. Push repo bisa menggunakan perintah `git push origin main`