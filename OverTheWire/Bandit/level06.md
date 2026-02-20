# Level 5 -> 6

Level Goal: Kata sandi untuk level berikutnya disimpan dalam sebuah file di suatu tempat di bawah direktori `inhere` dan memiliki semua properti berikut: dapat dibaca manusia, berukuran 1033 byte, dan tidak dapat dieksekusi

## The Prosess

Langkah pertama adalah melakukan koneksi remote menggunakan protokol SSH ke server OverTheWire.

```bash
$ ssh bandit5@bandit.labs.overthewire.org -p 2220
```

Manfaatkan perintah find dengan filter yang presisi:

```bash
$ find . -type f -size 1033c ! -executable -ls
$ cat inhere/maybehere07/.file2\
[Top_Secret]
$ exit
```

Setelah menjalankan perintah `cat inhere/maybehere07/.file2`, password level berikutnya akan tercetak di terminal. Salin string tersebut untuk login ke `bandit6`.
