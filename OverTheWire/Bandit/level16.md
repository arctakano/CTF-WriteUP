# Level 15 -> 16

Level Goal: Kata sandi untuk level berikutnya dapat diperoleh dengan mengirimkan kata sandi level saat ini ke `port 30001 di localhost` menggunakan enkripsi [SSL/TLS](https://en.wikipedia.org/wiki/Transport_Layer_Security).

**LOGS & FINDINGS<sup> 💡 </sup>:** Mendapatkan pesan "DONE", “RENEGOTIATING” atau “KEYUPDATE”? Baca bagian “CONNECTED COMMANDS” di halaman manual.

## The Prosess

Langkah pertama adalah melakukan koneksi remote menggunakan protokol SSH ke server OverTheWire.

```bash
$ ssh bandit15@bandit.labs.overthewire.org -p 2220
```
### Hint <sup> 💡 </sup>
Netcat biasa tidak bisa menangani enkripsi SSL. Jika kita menggunakan `nc`, koneksi akan ditolak atau tidak terbaca. Kita harus menggunakan perintah `ncat --ssl` versi modern dari `nc` (netcat) yang dibuat oleh Nmap.

```bash
$ ncat -ssl localhost 30001
depth=0 CN = SnakeOil
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = SnakeOil
verify return:1
---
[Private Key Content]
---
read R BLOCK
---
[Private Key Content]
---
read R BLOCK
{masukan key/password dari level sebelumnya}
[REDACTED]
Correct!
[Top_Secret]

closed
$ exit
```

sudah mendapatkan password untuk level selanjutnya? Untuk menjalankan level selanjutnya jalankan perintah `exit` untuk melanjutkan level senjutnya

