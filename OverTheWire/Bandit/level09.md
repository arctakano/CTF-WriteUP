# Level 8 -> 9

Level Goal: Kata sandi untuk level berikutnya tersimpan dalam file `data.txt` dan merupakan satu-satunya baris teks yang hanya muncul sekali.

## The Prosess

Langkah pertama adalah melakukan koneksi remote menggunakan protokol SSH ke server OverTheWire.

```bash
$ ssh bandit8@bandit.labs.overthewire.org -p 2220
```
Gunakan kombinasi [pipa](https://ryanstutorials.net/linuxtutorial/piping.php) (piping) antara `sort` dan `uniq -u`:

```bash
$ sort data.txt | uniq -u
[Top_Secret]
$ exit
```
Setelah menjalankan perintah `sort data.txt | uniq -u`, password level berikutnya akan tercetak di terminal. Salin string tersebut untuk login ke `bandit9`.

