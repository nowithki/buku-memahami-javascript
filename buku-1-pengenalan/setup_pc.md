# Memahami Javascript

# Setup PC

Untuk bisa mengikuti pembelajaran di buku ini, jika kamu belum familiar dengan pemrograman maka kamu perlu melakukan beberapa hal.

1. Install Code Editor. Code Editor adalah sebuah perangkat lunak pemrosesan kata yang didesain khusus untuk menulis sumber kode (source code). Salah satu yang saya sarankan untuk kamu install adalah Visual Studio Code yang dapat kamu install di [sini](http://code.visualstudio.com)
2. Install Browser (bisa chrome ataupun firefox).
3. Download repository ini. [klik disini](https://github.com/hanipcode/buku-memahami-javascript). lalu tekan tombol hijau bertuliskan `Clone or download`. lalu pilih `Download Zip`.
4. Kita akan menggunakan file di folder tutorials.

## Contoh

pertama, lakukan step setup pc seperti diatas. Jika sudah, maka extract file hasil download kamu kemudian masuk ke folder `tutorials` lalu masuk ke folder `01`.

Kamu akan menemukan 2 file yaitu file `index.html` dan file `ini_file.js`.

Langkah pertama adalah membuka file `index.html` di browser. kamu bisa melakukan drag and drop file tersebut ke browser atau dengan klik kanan file tersebut lalu buka dengan browser pilihan kamu.

Ketika kamu membuka browser maka kamu akan menjumpai tulisan 'Hello'.

Sekarang saatnya kita masuk kedalam magic dunia pemrograman. Buka file `ini_file.js` di code editor kamu (misal Visual Studio Code). Kamu akan menemukan

```javascript
function Hello() {
  return 'Hello';
}
```

Ubah text di file tersebut menjadi

```js
function Hello() {
  return 'Hello World !';
}
```

Lalu save file tersebut (ctrl + S). Kemudian buka kembali browser kamu, lalu refresh (Ctrl + R atau F5) maka kamu akan menemukan tulisan di halaman browser tersebut berubah menjadi `Hello World !`.

Jika kamu berhasil sampai sini, kamu siap untuk memulai ke [Chapter 1](./chapter_01.md)
