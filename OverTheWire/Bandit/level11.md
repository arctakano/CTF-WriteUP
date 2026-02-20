# Level 10 -> 11

Level Goal: Kata sandi untuk level berikutnya tersimpan dalam file `data.txt`, yang berisi data yang dikodekan `base64`.

## The Prosess

Langkah pertama adalah melakukan koneksi remote menggunakan protokol SSH ke server OverTheWire.

```bash
$ ssh bandit0@bandit.labs.overthewire.org -p 2220
```

### Hint <sup> 💡 </sup>
Base64 adalah skema pengkodean biner-ke-teks. Ini bukan enkripsi, melainkan cara merepresentasikan data biner dalam format teks ASCII.

```bash
$  base64 -d data.txt
The password is [Top_Secret]
$ exit
```

sudah mendapatkan password untuk level selanjutnya? Untuk menjalankan level selanjutnya jalankan perintah `exit` untuk melanjutkan level senjutnya
