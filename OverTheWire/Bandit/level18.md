# Level 17 -> 18

Level Goal: Terdapat 2 file di direktori utama: `passwords.old dan passwords.new`. Kata sandi untuk level berikutnya ada di `passwords.new` dan merupakan satu-satunya baris yang telah diubah antara `passwords.old dan passwords.new`.

## The Prosess

Langkah pertama adalah melakukan koneksi remote menggunakan protokol SSH ke server OverTheWire dengan menggunakan `Private.key` dari level sebelumnya.

```bash
$ ssh -i private.key bandit17@bandit.labs.overthewire.org -p 2220
$ ssh -i private.key bandit17@localhost -p 2220
```

```bash
$ diff passwords.old passwords.new
42c42
< pGozC8kOHLkBMOaL0ICPvLV1IjQ5F1VA
---
> [Top_Secret]
$ exit
```
sudah mendapatkan password untuk level selanjutnya? Untuk menjalankan level selanjutnya jalankan perintah `exit` untuk melanjutkan level senjutnya

