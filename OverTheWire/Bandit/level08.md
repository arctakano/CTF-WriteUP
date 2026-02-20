# Level 7 -> 8

Level Goal: Kata sandi untuk level berikutnya tersimpan dalam `file data.txt` di sebelah kata `millionth`.

## The Prosess

Langkah pertama adalah melakukan koneksi remote menggunakan protokol SSH ke server OverTheWire.

```bash
$ ssh bandit0@bandit.labs.overthewire.org -p 2220
```

Gunakan perintah grep untuk menyaring baris tertentu:

```bash
$ grep "millionth" data.txt
millionth       [Top_Secret]
$ exit
```

Setelah menjalankan perintah `grep "millionth" data.txt`, password level berikutnya akan tercetak di terminal. Salin string tersebut untuk login ke `bandit8`.
