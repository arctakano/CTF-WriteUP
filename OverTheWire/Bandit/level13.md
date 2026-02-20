# Level 12 -> 13

Level Goal: Kata sandi untuk level berikutnya tersimpan dalam file `data.txt`, yang merupakan hexdump dari file yang telah dikompresi berulang kali. Untuk level ini, mungkin berguna untuk membuat direktori di bawah /tmp tempat Anda dapat bekerja. Gunakan mkdir dengan nama direktori yang sulit ditebak. Atau lebih baik, gunakan perintah “mktemp -d”. Kemudian salin file data menggunakan cp, dan ganti namanya menggunakan mv (baca halaman manualnya!).

## The Prosess

Langkah pertama adalah melakukan koneksi remote menggunakan protokol SSH ke server OverTheWire.

```bash
$ ssh bandit12@bandit.labs.overthewire.org -p 2220
```

### Hint <sup> 💡 </sup>
- **Persiapan:** Buat direktori sementara di `/tmp` menggunakan perintah mktemp `-d` dan salin file ke direktori tersebut dengan `cp ~/data.txt /tmp/nama_direktori_sementara`.
- **Reverse Hexdump:** Masuk ke direktori sementara dengan cd `/tmp/nama_direktori_sementara` dan ubah kembali ke file biner dengan `xxd -r data.txt > data`.
- **Identifikasi:** Gunakan perintah file data untuk melihat jenis kompresinya.
- **Ekstraksi:**
  -  Jika Gzip: `mv data data.gz && gunzip data.gz`
  -  Jika Bzip2: `mv data data.bz2 && bzip2 -d data.bz2`
  -  Jika Tar: `mv data data.tar && tar -xf data.tar`
- Ulangi langkah ini sampai mendapatkan file yang diindentifikasi sebagai ASCII text[.](https://github.com/setyanoegraha/overthewire-writeups/blob/main/bandit/bandit13.md)

```bash
$ cat data8
The password is [Top_Secret]
$ exit
```

sudah mendapatkan password untuk level selanjutnya? Untuk menjalankan level selanjutnya jalankan perintah `exit` untuk melanjutkan level senjutnya
