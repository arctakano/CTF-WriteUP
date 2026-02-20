# Level 0 -> 1

Level Goal: Kata sandi untuk level berikutnya tersimpan dalam file bernama `readme` yang terletak di direktori home. Gunakan kata sandi ini untuk masuk ke bandit1 menggunakan SSH. Setiap kali Anda menemukan kata sandi untuk suatu level, gunakan SSH (pada port 2220) untuk masuk ke level tersebut dan melanjutkan permainan.

## The Prosess

Langkah pertama adalah melakukan koneksi remote menggunakan protokol SSH ke server OverTheWire.

```bash
$ ssh bandit0@bandit.labs.overthewire.org -p 2220
```

Setelah melakukan log pada remote server. jalankan perintah `cat readme` untuk mendapatkan password untuk level selanjutnya. **Jangan lupa untuk salin password di tempat lain**, karena sekali tidak tersimpan anda harus mengulang dari **awal**

```bash
$ ls -la
$ cat readme
Congratulations on your first steps into the bandit game!!
Please make sure you have read the rules at https://overthewire.org/rules/
If you are following a course, workshop, walkthrough or other educational activity,
please inform the instructor about the rules as well and encourage them to
contribute to the OverTheWire community so we can keep these games free!

The password you are looking for is: [Top_Secret]
```

sudah mendapatkan password untuk level selanjutnya? Untuk menjalankan level selanjutnya jalankan perintah `exit` untuk melanjutkan level senjutnya

```bash
$ exit
```
