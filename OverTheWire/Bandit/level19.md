# Level 18 -> 19

Level Goal: Kata sandi untuk level berikutnya tersimpan dalam file `readme` di direktori home. Sayangnya, seseorang telah memodifikasi `.bashrc` untuk mengeluarkan Anda dari sesi saat Anda masuk menggunakan SSH.

### Hint <sup> 💡 </sup>
SSH memungkinkan kita mengirim perintah secara langsung tanpa harus masuk ke shell interaktif sepenuhnya.

## The Prosess

Langkah selanjutnya adalah melakukan koneksi menggunakan protokol SSH ke server OverTheWire. Untuk mendapatkan `readme` ada dua cara:

```bash
$ ssh bandit18@bandit.labs.overthewire.org -p 2220 cat ./readme
[Top_Secret]
$ exit
```
Atau

```bash
$ ssh bandit18@bandit.labs.overthewire.org -p 2220 bash
$ ls
$ cat reedme
[Top_Secret]
$ exit
```
sudah mendapatkan password untuk level selanjutnya? Untuk menjalankan level selanjutnya jalankan perintah `exit` untuk melanjutkan level senjutnya
