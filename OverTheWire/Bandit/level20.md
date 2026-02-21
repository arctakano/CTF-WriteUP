# Level 19 -> 20

Level Goal: Untuk mengakses level berikutnya, Anda harus menggunakan binary setuid di direktori home. Jalankan tanpa argumen untuk mengetahui cara menggunakannya. Kata sandi untuk level ini dapat ditemukan di tempat biasa (/etc/bandit_pass), setelah Anda menggunakan binary setuid.

## The Prosess

Langkah pertama adalah melakukan koneksi remote menggunakan protokol SSH ke server OverTheWire.

```bash
$ ssh bandit19@bandit.labs.overthewire.org -p 2220
```
### Hint <sup> 💡 </sup>
SetUID adalah izin khusus yang memungkinkan user menjalankan program dengan izin dari pemilik file tersebut (dalam hal ini, pemiliknya adalah bandit20).

```bash
$ ./bandit20-do cat /etc/bandit_pass/bandit20
[Top_Secret]
$ exit
```
sudah mendapatkan password untuk level selanjutnya? Untuk menjalankan level selanjutnya jalankan perintah `exit` untuk melanjutkan level senjutnya
