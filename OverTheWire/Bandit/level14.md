# Level 13 -> 14 

Level Goal: Kata sandi untuk level berikutnya tersimpan di `/etc/bandit_pass/bandit14` dan hanya dapat `dibaca oleh pengguna bandit14`. Untuk level ini, Anda tidak mendapatkan kata sandi berikutnya, tetapi Anda mendapatkan kunci SSH pribadi yang dapat digunakan untuk masuk ke level berikutnya. Lihat perintah yang Anda gunakan untuk masuk ke level bandit sebelumnya, dan cari tahu cara menggunakan kunci untuk level ini.

### Hint <sup> 💡 </sup>
Selama ini kita login menggunakan password. Namun, dalam dunia profesional, penggunaan kunci kriptografi jauh lebih aman dan umum digunakan.

## The Prosess

Langkah pertama adalah melakukan koneksi remote menggunakan protokol SSH ke server OverTheWire.

```bash
$ scp -P 2220 bandit13@bandit.labs.overthewire.org:sshkey.private .
$ chmod 600 sshkey.private
$ ssh -i sshkey.private bandit14@bandit.labs.overthewire.org -p 2220
$ cat /etc/bandit_pass/bandit14
[Top_Secret]
$ exit
```

sudah mendapatkan password untuk level selanjutnya? Untuk menjalankan level selanjutnya jalankan perintah `exit` untuk melanjutkan level senjutnya
