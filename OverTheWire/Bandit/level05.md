# Level 4 -> 5

Level Goal: Kata sandi untuk level berikutnya tersimpan dalam satu-satunya file yang dapat dibaca manusia di direktori `inhere`. Tip: jika terminal Anda bermasalah, coba perintah "reset".


## The Prosess

Langkah pertama adalah melakukan koneksi remote menggunakan protokol SSH ke server OverTheWire.

```bash
$ ssh bandit4@bandit.labs.overthewire.org -p 2220
```

Gunakan perintah `file` untuk mengidentifikasi tipe konten dari setiap file dalam direktori:

```bash
$ cd inhere
$ file ./*
$ cat ./-file07
[Top_Secret]
$  exit
```

Setelah menjalankan perintah `cat ./-file07`, password level berikutnya akan tercetak di terminal pada `inhere/-file07`. Salin string tersebut untuk login ke `bandit5`.

