# Level 6 -> 7

Level Goal: Kata sandi untuk level berikutnya tersimpan `di suatu tempat di server` dan memiliki semua properti berikut: dimiliki oleh pengguna `bandit7`, dimiliki oleh grup `bandit6`, dan berukuran 33 byte

## The Prosess

Langkah pertama adalah melakukan koneksi remote menggunakan protokol SSH ke server OverTheWire.

```bash
$ ssh bandit0@bandit.labs.overthewire.org -p 2220
```

Gunakan pencarian dari direktori root (`/`) dan alihkan pesan error "Permission Denied" agar output tetap bersih:

```bash
$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null -ls
$ cat /var/lib/dpkg/info/bandit7.password
[Top_Secret]
$ exit
```
Setelah menjalankan perintah `cat /var/lib/dpkg/info/bandit7`.password, password level berikutnya akan tercetak di terminal. Salin string tersebut untuk login ke `bandit7`.
