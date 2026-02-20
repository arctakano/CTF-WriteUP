# Level 1 -> 2

Level Goal: Kata sandi untuk level berikutnya tersimpan dalam sebuah file bernama `-` yang terletak di direktori utama.

## The Prosess

Langkah pertama adalah melakukan koneksi remote menggunakan protokol SSH ke server OverTheWire.

```bash
$ ssh bandit1@bandit.labs.overthewire.org -p 2220
```

### Hint <sup> 💡 </sup>

- Karakter  `-` pada awal nama file sering kali disalahartikan oleh shell sebagai flag atau parameter perintah. Hal ini menyebabkan perintah seperti `cat` gagal mengeksekusi file tersebut karena dianggap sebagai argumen yang tidak valid.

Gunakan _path eksplisit_ (absolut atau relatif) agar sistem membacanya sebagai nama file, bukan sebagai argumen perintah:

```bash
$ cat ./-
[Top_Secret]
$ exit
```

sudah mendapatkan password untuk level selanjutnya? Untuk menjalankan level selanjutnya jalankan perintah `exit` untuk melanjutkan level senjutnya
