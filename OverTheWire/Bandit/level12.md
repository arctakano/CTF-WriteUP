#Level 11 -> 12

Level Goal: Kata sandi untuk level berikutnya tersimpan dalam file `data.txt`, di mana semua huruf kecil (a-z) dan huruf besar (A-Z) telah diputar sebanyak 13 posisi.

## The Prosess

Langkah pertama adalah melakukan koneksi remote menggunakan protokol SSH ke server OverTheWire.

```bash
$ ssh bandit11@bandit.labs.overthewire.org -p 2220
```

### Hint <sup> 💡 </sup>
Ini adalah teknik kriptografi klasik bernama `ROT13`. Karena alfabet memiliki 26 huruf, menggeser 13 posisi dua kali akan mengembalikan teks ke aslinya.

```bash
$ cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
The password is [Top_Secret]
$ exit
```

sudah mendapatkan password untuk level selanjutnya? Untuk menjalankan level selanjutnya jalankan perintah `exit` untuk melanjutkan level senjutnya

