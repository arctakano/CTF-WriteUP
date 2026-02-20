# Level 2 -> 3

Level Goal: Kata sandi untuk level berikutnya tersimpan dalam sebuah file bernama `--spaces in this filename--` yang terletak di direktori home.

## The Prosess

Langkah pertama adalah melakukan koneksi remote menggunakan protokol SSH ke server OverTheWire.

```bash
$ ssh bandit2@bandit.labs.overthewire.org -p 2220
```

### Hint <sup> 💡 </sup>
Terminal memisahkan argumen berdasarkan spasi. Jika kita mengetik `cat --spaces in...`, terminal akan mengira kita ingin membaca tiga file yang berbeda.

Gunakan tanda petik atau backslash escape (`\`) untuk menangani spasi pada nama file:

```bash
$ cat ./--spaces\ in\ this\ filename--
$ cat "./--spaces in this filename--"

[Top_Secret]

$ exit
```

Setelah menjalankan perintah `cat ./--spaces\ in\ this\ filename--` atau `cat "./--spaces in this filename--"`, password level berikutnya akan tercetak di terminal. Salin string tersebut untuk login ke `bandit3`.

