# Level 9 -> 10

Level Goal: Kata sandi untuk level berikutnya disimpan dalam file `data.txt` dalam salah satu dari sedikit string yang dapat dibaca manusia, diawali dengan beberapa karakter '='.

## The Prosess

Langkah pertama adalah melakukan koneksi remote menggunakan protokol SSH ke server OverTheWire.

```bash
$ ssh bandit9@bandit.labs.overthewire.org -p 2220
```

### Hint <sup> 💡 </sup>
Perintah cat akan menampilkan karakter aneh (mojibake) jika digunakan pada file biner. Kita membutuhkan alat yang hanya mengekstrak karakter yang bisa dibaca manusia.

```bash
$ strings data.txt | grep "=="
========== the
========== password
E========== is
5========== [Top_Secret]
$ exit
```

Setelah menjalankan perintah `strings data.txt | grep "=="`, password level berikutnya akan tercetak di terminal. Salin string tersebut untuk login ke `bandit10`.
