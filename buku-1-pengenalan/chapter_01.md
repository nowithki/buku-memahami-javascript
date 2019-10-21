# Memahami Javascript

# Variabel dan Tipe Data

## Sebelum Memulai

jika kamu ingin mengikuti juga pemrograman pada buku ini, kamu perlu mengikuti bab [Setup PC](./setup_pc.md). jika kamu belum memiliki pengalaman pemrograman sebelumnya, saya sangat merekomendasikan untuk mengikuti bab tersebut terlebih dahulu.

## Selayang Pandang Pemrograman

Saya tidak akan terlalu memberi pembuka tentang pemrograman dalam buku ini karena saya akan lebih fokus pada aspek teknis daripada definisi.

Namun bagi saya, Pemrograman adalah tentang memberi tahu mesin X apa yang harus mereka lakukan. ubah X menjadi platform atau device apapun, entah itu PC, Android, iOS, dan lain sebagainya.

Di awal buku saya sempat menyinggung bahwa javascript umumnya digunakan untuk pemrograman web. maka berdasar definisi diatas, Memrogram javascript (secara sempit) berati memberi tau mesin Web (dalam hal ini Browser seperti Google Chrome, Firefox) apa yang harus mereka lakukan atau tampilkan.

Contohnya, ketika kamu mengikuti bab [Setup PC](./setup_pc.md) ketika kita melakukan sebuah perubahan pada file `ini_file.js` maka apa yang ditampilkan ketika membuka `index.html` pun ikut berubah dari `Hello` menjadi `Hello World !`.

Disini kita melakukan aktivitas pemrograman atau aktivitas mengubah sebuah perintah di dalam file program. Ada berbagai jenis bahasa pemrograman, dari tingkat rendah sampai tingkat tinggi.

tingkat ini dibagi berdasarkan kefamiliaranya dengan bahasa manusia. semakin rendah tingkat maka semakin bahasa tersebut lebih mendekati bahasa mesin ketimbang bahasa manusia. Seperti yang bisa teman teman tebak javascript ini termasuk bahasa tingkat tinggi dimana kita menemukan kata kunci kata kunci yang familiar seperti `function` dan `return` yang ada pada bahasa manusia.

Lalu apa saja komponen dalam sebuah bahasa pemrograman ?

## Variable

dalam matematika di sekolah dulu kita mengenal formulaa yang melibatkan huruf **X** dan **Y**. semisal dengan format berikut

```
Jika ada sebuah persamaan  x = y + 5 , dimana y bernilai 3. maka nilai x adalah ?
```

tentu kita dapat menjawab dengan sangat cepat bahwa x bernilai 8. tapi darimana ? dari menggantikan nilai y dengan nilai 3. atau dalam bahasa yang lebih matematis dapat disusun demikian

```
y = 3
x = y + 5
x = ?
```

ada bagian `y = 3`. nah y dan x inilah yang disebut variable. atau sebuah peenyimpan nilai. kita simpan nilai 3 di Variable **y** kemudian ketika disebut **y** di persamaan berikutnya, kita dapat menggantikan nya dengan angka 3.

Nah dalam pemrograman, seorang programmer juga hampir selalu menggunakan variabel untuk menyimpan nilai. karena penyimpanan sebuah nilai dalam variable juga memberikan konteks atau makna terhadap angka tersebut. misal persamaan diatas diganti

```
indomie_yang_dibeli_budi = 3
total_indomie_budi = y + 5
total_indomie_budi = ?
```

dengan pemberian nama yang lebih bermakna tersebut kita langsung mengetahui bahwa proses hitung tersebut adalaah proses menghitung indomie budi setelah budi membeli indomie.

sekarang kita akan mencoba melakukan perubahan pada file `ini_file.js`. misal kita rubah menjadi seperti demikian

```javascript
function Hello() {
  const textYangDitampilkan = 'Tampilkan Teks Ini !';
  return textYangDitampilkan;
}
```

ketika kamu save lalu refresh browser mu yang menampilkan file `index.html` maka sekarang tulisan di browser akan bertuliskan `Tampilkan Teks Ini !`.

> const textYangDitampilkan = 'Tampilkan Teks Ini !';

di baris ini kita mendefinisikan sebuah variabel dengan nama textYangDiitampilkan, kemudian memasukkan teks 'Tampilkan Teks Ini !' ke dalam variabel tersebut.
dalam pemrograman javaascript mendefinisikan variabel bisa diawali dengan 2 keyword yaitu `const` ataupun `let`. bisa juga baris diatas diubah menjadi

> let textYangDitampilkan = 'Tampilkan Teks Ini !';

lalu kapan menggunakan const dan kapan menggunakan let ? intinya adalah gunakan const ketika kamu yakin bahwa nilai dalam variabel tersebut tidak dapat berubah atau kependekan dari constanta. dan gunakan `let` ketika nilai variabel dapat berubah.
apa? nilai variabel dapat berubah ? ya, nilai dalam sebuah variabel dapat berubah. misalkan ubah file `ini_file.js` menjadi seperti berikut

```javascript
function Hello() {
  let textYangDitampilkan = 'Teks Awal';
  textYangDitampilkan = 'Teks Telah Dirubah !'; // ini baris ke 3
  return textYangDitampilkan;
}
```

save kemudian refresh browser kamu. maka tulisan yang muncul adalah `Teks Telah Dirubah!` karena pada baris ke 3 variabel textYangDitampilkan telah diganti dengan nilai baru tersebut, dan seperti juga terlihat pada baris kode diatas, untuk mengganti nilai variabel kita tinggal memasukan nilai baru namun tanpa diawali dengan `let` ataupun `const`.

## Comment

lihat teks `// ini baris ke 3` diatas ? bagian tersebut dalam sumber kode dikenal dengan sebutan Comment

dalam dunia pemrograman dikenal istilah Comment atau komentar. yaitu sebaris atau lebih teks dalam sumber kode yang tidak dieksekusi oleh mesin. Jadi Comment adalah rangkaian teks yang hanya bisa dibaca oleh kita dan tidak oleh mesin.

Apa gunanya ? Dunia pemrograman adalah dunia kolaborasi. apa yang kita kerjakan mungkin akan dilempar ke programmer lain untuk dilanjutkan. bukan hanya hari ini atau besok, mungkin juga beberapa tahun kemudian akan ada seorang programmer yang melihat kode yang kita tulis hari ini. lalu bagaimana ketika ada baris baris yang sulit di mengerti dalam baris kode kita. maka bagaimana kita memastikan orang yang melanjutkan program kita beberapa waktu mendatang bisa mengerti tentang baris yang sulit tersebut ? salah satunya adaalah dengan memberikan Comment

**fun fact**: Seseorang dalam paragraf diatas bisa jadi kita sendiri lho. bisa jadi kita menulis program sulit hari ini tanpa komentar, lalu beberapa bulan kemudian kita mau lanjutkan, eh sudah lupa baris tersebut untuk apa.

### Berlebihan itu tidak baik

Oh ya, tapi alangkah baiknya mengutamakan pemberian nama variable yang baik dan mewakili konteks didahulukan daripada menuliskan Comment. kode dengan bahasa tingkat tinggi seperti javascript kan cenderung mudah dibaca oleh manusia. gunakan Comment lebih ke untuk menjelaskan hal yang benar benar sulit. misal kalau kita menulis ulang kode diatas menjadi:

```javascript
function FX() {
  let z = 'Teks Awal';
  z = 'Teks Telah Dirubah !';
  return z;
}
```

Program kita akan jadi sulit untuk dibaca. mungkin kita akan terpikir untuk menambahkan comment:

```javascript
// Menampilkan tulisan di halaman depan
function FX() {
  // teks awal yang ditampilkan
  let z = 'Teks Awal';
  z = 'Teks Telah Dirubah !';
  // tampilkan teks awal
  return z;
}
```

orang mungkin akan paham apa maksud kode kita. namun bukankah:

```javascript
function Hello() {
  let textYangDitampilkan = 'Teks Awal';
  textYangDitampilkan = 'Teks Telah Dirubah !';
  return textYangDitampilkan;
}
```

itu cukup membuat orang paham tanpa harus menuliskan komentar, dan tentunya lebih terlihat elegan ?. ya, kode yang baik adalah kode yang mampu terjelaskan tanpa Comment.

Namun Comment tetap diperlukan di situasi tertentu misalkan kita punya rumus matematika atau algoritma khusus dalam baris kode kita. maka mungkin ada baiknya kita menuliskan komentar menjelaskan baris kode atau algoritma tersebut.

### Penulisan Comment

Comment dalam javascript memiliki dua aturan penulisan. yaitu dengan simbol `// ini komentar` seperti diatas dan dengan simbol `/* ini komentar */`.
apa bedanya ? syntaks `// ini komentar` hanya dapat untuk menuliskan komentar 1 baris. jadi biasanya digunakan untuk komentar komentar singkat seperti:

```javascript
function Hello() {
  let textYangDitampilkan = 'Teks Awal';
  textYangDitampilkan = 'Teks Telah Dirubah !'; // ini baris ke 3
  return textYangDitampilkan;
}
```

sedangkan aturan penulisan `/* */` disebut juga Multiline Comment atau komentar multibaris. sesuai namanya dia dapat untuk menulis Comment yang lebih dari satu baris. biaasanya digunakan untuk menjelaskan sesuatu secara panjang atau memberi tahu informasi tentang sumber kode semisal

```javascript
/*
 * Author: Muhammad Hanif
 * License: MIT
 * this library is for numbers algorithm
 */
```

dengan melihat informasi seperti itu dalam sebuah file sumber kode misalnya, kita akan pahaam bahwa file tersebut berisikan fungsi fungsi yang berkaitan dengan angka.

## Tipe Data

Dalam pembahasan variabel kita mengetahui bahwa kita dapat memasukkan nilai kedalam sebuah variabel. Nah dalam pemrograman, variabel dan nilai tersebut memiliki tipe. dalam kehidupan sehari hari kita mengenal teks dan angka misalnya, dan dalam otak kita, kita mengerti perbedaan kumpulan teks dan kumpulan angka.
sehari hari kita membaca (jenis data) teks dan menghitung (jenis data) angka. Nah javascript pun mengenal Tipe Data dengan kegunaan yang berbeda beda pula.

### number

Number, sesuai namanya adalah tipe data berupa angka. semisal `1`,`2`,`3`, dan seterusnya. oh ya, `1` dan `"1"`. `1` adalah Number dan `"1"` adalah String. kita bisa mengoperasikan angka di javascript layaknya mengoperasikan angka di matematika. misal membuat rumus segitiga

```js
const alas = 12;
const tinggi = 5;
const luasSegittiga = (alas * tinggi) / 2; // bernilai 30
```

12 dan 5 adalah tipe data number. dan hasil dari `(alas * tinggi)/2` juga memiliki tipe data number yang kemudian kita masukkan kedalam variabel `luasSegitiga`

### String

String adalah kumpulan huruf dan angka yang biasa kita sebut teks. penulisan string diawali dengan quote(') ataupun double-quote("). misalkan seperti

```javascript
function Hello() {
  const textYangDitampilkan = 'Tampilkan Teks Ke-1 Ini !';
  return textYangDitampilkan;
}
```

`'Tampilkan Teks Ke-1 Ini !'` adalah string. notice meskipun ada angka 1 disitu karena dia berada dalam quote maka dia juga bagian dari string. itulah mengapa

```javascript
const angka = 2;
const teks = '2';
```

berbeda dalam javascript. `2` adalah angka dan `'2'` adalah string.

### boolean

Tipe data Boolean adalah tipe data yang bernilai benar/salah `true/false`. Variabel ini biasanya digunakan untuk mengecek nilai kebeneran semisal

```javascript
let tinggiAir = 0;
const sedangHujan = true;
if (sedangHujan) {
  tinggiAir = 10;
}
const tinggiTembokDibutuhkan = tinggiAir * 3; // 30
```

kita memberi nilai true pada variabel dengan namaa `sedangHujan` dan melakukan pengecekan di baris selanjutnya. karena `sedangHujan` bernilai benar (true), maka baris setelah if dijalankan

### array

Array adalah kumpulan data dalam javascript yang dimasukkan menjadi variabel. misalkan kita punya variabel `nilaiMuridKelasB`. secara deskriptif data tersebut berupa kumpulana nilai. maka kita akan menggunakan tipe data array dan cara penulisanya adalah sebagai berikut

```javascript
const nilaiMuridKelasB = [10, 8, 10, 7, 9, 5, 6, 8];
```

Penulisanya adalah dengan kurung kotak kemudian setiap nilai di tambah dengan Koma(`,`). kita bisa mengakses nilai didalam array dengan mengakses `index` atau urutan nya. oh ya dalam pemrograman biasanya nilai urutan selalu dimulai dari 0 dan bukan 1. misal kita ingin mengakses angka 7 dalam array diatas maka kita mengakses `nilaiMuridKelasB[3]` karena

```js
const nilaiMuridKelasB = [10, 8, 10, 7, 9, 5, 6, 8];
nilaiMuridKelasB[0] === 10;
nilaiMuridKelasB[1] === 8;
nilaiMuridKelasB[2] === 10;
nilaiMuridKelasB[3] === 7;
// dan seterusnya..
```

### object

Object adalah kumpulan data yang memiliki label atau `key` pada setiap nilaiinya. misalkan dalam `nilaiMuridKelasB` kita ingin menandai siapa yang mendapat nilai berapa. maka tipe data Object akan lebih tepat daripada array dan penulisanya menjadi demikian

```javascript
const nilaiMuridKelasB = {
  budi: 10,
  ani: 5,
  andi: 9,
  rohman: 1,
  toni: 5,
};
```

ada dua cara mengakses object, yaitu deengan menggunakan titik semisal

```javascript
const nilaiMuridKelasB = {
  budi: 10,
  ani: 5,
  andi: 9,
  rohman: 1,
  toni: 5,
};

nilaiMuridKelasB.budi; // bernilai 10
nilaiMuridKelasB.toni; // bernilai 5
const nilaiRerataBudiToni =
  (nilaiMuridKelasB.budi + nilaiMuridKelasB.toni) / 2; // bernilai 7.5
```

atau dengan mengakses key nya

```javascript
const nilaiMuridKelasB = {
  budi: 10,
  ani: 5,
  andi: 9,
  rohman: 1,
  toni: 5,
};

nilaiMuridKelasB['budi']; // bernilai 10
nilaiMuridKelasB['toni']; // bernilai 5
const nilaiRerataBudiToni =
  (nilaiMuridKelasB['budi'] + nilaiMuridKelasB['toni']) / 2; // bernilai 7.5
```

bedanya adalah nilai didalam kotak tersebut diievaluasi oleh program. maka dari itu kita harus menggunakana notasi string. jika kita menuliskan `nilaiMuridKelasB[budi]` tanpa string, makaa program tersebut akan error karena mencoba menganggap budi sebagai variabel. Ya, benar, kita bisa masukkan variabel di dalam kotak setelah nama object semisal

```javascript
const nilaiMuridKelasB = {
  budi: 10,
  ani: 5,
  andi: 9,
  rohman: 1,
  toni: 5,
};

const namaBudi = 'budi';
const namaToni = 'toni';

nilaiMuridKelasB[namaBudi] === nilaiMuridKelasB['budi']; // bernilai 10
nilaiMuridKelasB[namaToni] === nilaiMuridKelasB['toni']; // bernilai 5
const nilaiRerataBudiToni =
  (nilaiMuridKelasB[namaBudi] +
    nilaiMuridKelasB[namaToni]) /
  2; // bernilai 7.5
```

## Operators

Javascript mengenal Operators. apa itu Operators ? Operators adalah simbol seperti dalam matematika semisal `+ (Tambah)` `/ (Pembagi)` `* (Perkalian)`. selain simbol simbol matetmatika yang umum javascript juga mengenal beberapa simbol lainya seperti:

### Modulo (%)

Modulo berarti sisa bagi. biasanya digunakan untuk mencari tahu apakah Y habis dibagi X. misalkan.

```javascript
const bilangan1 = 5;
const bilangan2 = 25;
const bilangan3 = 8;
const bilangan4 = 29;
const modulo1 = bilangan1 % 5; // bernilai 0 karena 5 habis dibagi 5
const modulo2 = bilangan2 % 5; // bernilai 0 karena 25 habis dibagi 5
const modulo3 = bilangan3 % 5; // bernilai 3 karena jika 8 dibagi 5 maka akan bernilai 1 3/5. ambil nilai 3 (3 dari 5).
const modulo4 = bilangan4 % 5; // bernilai 4 karena 29 dibagi 5 maka akan bernilai 5 4/5. ambil nilai 4 (4 dari 5).
```

### Pangkat (`**`)

di javascript operasi pangkat menggunakan simbol `**` semisal `5 ** 2` berarti 5 pangkat 2.
