# Level 14 -> 15 

Level Goal: Kata sandi untuk level berikutnya dapat diperoleh dengan mengirimkan kata sandi level saat ini ke `port 30000 di localhost`.

## The Prosess

Langkah pertama adalah melakukan koneksi remote menggunakan protokol SSH ke server OverTheWire.

```bash
$ ssh bandit14@bandit.labs.overthewire.org -p 2220
```

### Hint <sup> 💡 </sup>
Di dunia nyata, banyak layanan berkomunikasi melalui port tertentu. Kita menggunakan alat bernama `nc` (Netcat), yang sering disebut sebagai "Swiss-army knife" untuk jaringan.

```bash
$ cat /etc/bandit_pass/bandit14 | nc localhost 30000
Correct!
[Top_Secret]
$ exit
```

sudah mendapatkan password untuk level selanjutnya? Untuk menjalankan level selanjutnya jalankan perintah `exit` untuk melanjutkan level senjutnya
