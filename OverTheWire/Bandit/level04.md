# Level 3 -> 4

Level Goal: Kata sandi untuk level berikutnya tersimpan dalam file tersembunyi di direktori `inhere`.

## The Prosess

Langkah pertama adalah melakukan koneksi remote menggunakan protokol SSH ke server OverTheWire.

```bash
$ ssh bandit3@bandit.labs.overthewire.org -p 2220
```

### Hint <sup> 💡 </sup>
Di Linux, file yang diawali dengan tanda titik (`.`) tidak akan muncul pada perintah `ls` biasa.

```bash
$ cd inhere
$ ls -la
$ cat ...Hiding-From-You
[Top_Secret]

$ exit
```

Setelah menjalankan perintah `cat ...Hiding-From-You`, password level berikutnya akan tercetak di terminal. Salin string tersebut untuk login ke `bandit4`.
