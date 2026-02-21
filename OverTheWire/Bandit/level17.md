# Level 16 -> 17

Level Goal: Kredensial untuk level berikutnya dapat diperoleh dengan mengirimkan kata sandi level saat ini ke `port di localhost dalam rentang 31000 hingga 32000`. Pertama, cari tahu port mana yang memiliki server yang mendengarkan. Kemudian, cari tahu mana yang mendukung SSL/TLS dan mana yang tidak. Hanya ada 1 server yang akan memberikan kredensial berikutnya, server lainnya hanya akan mengirimkan kembali apa pun yang Anda kirimkan kepadanya.

**LOGS & FINDINGS<sup> 💡 </sup>:** Mendapatkan pesan “DONE”, “RENEGOTIATING” atau “KEYUPDATE”? Baca bagian “CONNECTED COMMANDS” di halaman manual.

## The Prosess

Langkah pertama adalah melakukan koneksi remote menggunakan protokol SSH ke server OverTheWire.

```bash
$ ssh bandit16@bandit.labs.overthewire.org -p 2220
```

### Hint <sup> 💡 </sup>
- **Scanning:** Gunakan `nmap -p 31000-32000 -sV localhost` untuk melihat port mana yang terbuka beserta servicenya.
- **Identification:** Coba lakukan koneksi ke port yang berstatus "open" dengan service status "ssl/unknown" menggunakan `ncat --ssl localhost [PORT]` (seperti Level 15).
- Capture Key: Salah satu port akan merespons dengan RSA Private Key. Simpan teks tersebut ke sebuah file, misalnya `private.key`.

```bash
$ ncat --ssl localhost 31790
{masukan key/password dari level sebelumnya}
Correct!
-----BEGIN RSA PRIVATE KEY-----
[Private Key Content]
-----END RSA PRIVATE KEY-----
$ exit
```

> **Note:** untuk `private rsa` bisa disimpan secara local (bandit16) ataupun secara mandiri. Setelah itu jangan lupa untuk mengubah izin agar bisa digunakan pada level selanjutnya. Contoh pengubahan izin `chmod 600 [file]`
