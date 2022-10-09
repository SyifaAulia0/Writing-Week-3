# Writing-Week-3
## Array
- Array di js mampu menyimpan banyak data dan tipe data apapun
```js
//script.js
let arr = ["hallo", 1, true]
```
- Index array dimulai dari nol
```js
//script.js
let arr = ["hallo", 1, true]
console.log(arr[0]) //hallo
console.log(arr[1]) //1
console.log(arr[2]) //true
```
### Property array 
- .length : melihat berapa banyak data dalam array
```js
let arr = ["hallo", 1, true]
console.log(arr.length); //3
```
- .push : menambah data baru pada akhir array
```js
let arrBuah = [
  "jeruk", 
  "semangka", 
  "pepaya", 
  "rambutan",
  "melon",
  "belimbing"
]
arrBuah.push("duku") //jeruk, semangka, pepaya, rambutan, melon, belimbing, duku
```
- .unshift : menambah data baru pada awal array
```js
arrBuah.unshift("anggur") //anggur, jeruk, semangka, pepaya, rambutan, melon, belimbing
```
- .pop : menghapus data terakhir di array
```js
arrBuah.pop()  //jeruk, semangka, pepaya, rambutan, melon
```
- .shift : menghapus data awal di array
```js
arrBuah.shift() //semangka, pepaya, rambutan, melon, belimbing
```
- .splice : menghapus data di tengah array, merubah data arraynya, dan mereturn nilai
```js
arrBuah.splice(2, 0, "buah naga") //jeruk, semangka, buah naga, rambutan, melon, belimbing
```
- .slice : mengamil dengan cara mengcopy datanya
```js
let slice = arrBuah.slice(2, 4) //buah naga, pepaya
```
### looping array	
```js
let arrBuah = [
  "jeruk", 
  "semangka",
  "buah naga",
  "pepaya", 
  "rambutan",
  "melon",
  "belimbing"
]
```
- for
```js
for (let i = 0; i < arrBuah.length; i++) {
  console.log(arrBuah[i]) //jeruk, semangka, buah naga, pepaya, rambutan, melon, belimbing
} 
```
```js
for (let i = arrBuah.length - 1; i >= 0; i--) {
  console.log(arrBuah[i])
} //untuk melooping dari akhir ke awal
//belimbing, melon, rambutan, pepaya, buah naga, semangka, jeruk
```
- for.of 
```js
for (let buah of arrBuah){
console.log(buah)
} //jeruk, semangka, buah naga, pepaya, rambutan, melon, belimbing
```
- forEach 
```js
arrBuah.forEach((item) => {
  console.log(item)
}) //jeruk, semangka, buah naga, pepaya, rambutan, melon, belimbing

//jika ingin mencari dengan index
arrBuah.forEach((item, index){
console.log(index, item)})
if(index%2 == 1) //untuk mencari data dengan index ganjil
```
- .map : improvement dari forEach. Bisa mereturn dalam bentuk array
```js
let buahSegar = arrBuah.map((item) => {
  return item + " " + "segar"
})
console.log(buahSegar) //jeruk segar, semangka segar, buah naga segar, pepaya segar, rambutan segar, melon segar, belimbing segar
```
- .map = membuat angka decimal menjadi angka persen
```js
let angkaDes = [
  0.45,
  0.67,
  0.23,
  0.76,
]

let angkaPersenMap = angkaDes.map((item) => {
  return item * 100 + "%"
})
console.log(angkaPersenMap); // '45%', '67%', '23%', '76%'
```
- forEach
```js
let angkaPersenForEach = []
angkaDes.forEach((item) => {
  angkaPersenForEach.push(item * 100 + "%")
})
console.log(angkaPersenForEach) //'45%', '67%', '23%', '76%'
```
- .multi : array muulti dimensi
```js
let arrMulti = [
  ["nama", "alpha"],
  ["umur", 17],
  ["kelas", "JS"],
]

console.log(arrMulti[0][1]); //alpha
console.log(arrMulti[2][1]) //JS

arrMulti[2][1] = "CSS"
console.log(arrMulti); //
```
## Objects
- Object adalah sebuah tempat penyimpanan data
- membuat obj 
```js
let nama_obj={
key1: "value",
key2: "value2"
};
```
```js
let siswa = {
  nama: "terra",
  umur: 17,
  hobi: "memancing",
  "nomor handphone": 082367599,
};

console.log(siswa);
```
### Cara akses object
- akses object ada 2 cara :
1. dot notation console.log(siswa.nama)
```js
let siswa = {
  nama: "terra",
  umur: 17,
  hobi: "memancing",
  "nomor handphone": 182367599,
};

console.log(siswa.nama); //terra
```
2. bracket console.log(siswa["nama"])
```js
console.log(siswa["nama"]); //terra
console.log(siswa["nomor handphone"]); //182367599
```
- memanggil nama object dengan properti
```js
let properti = "umur";
console.log(siswa[properti]); //17
```
### CreateKey
- Menambahkan property baru ke dalam object
```js
let buku = {
  judul: "mantan jadi manten",
  penulis: "hayati",
  "jumlah halaman": 250,
};

console.log(buku); //judul: 'mantan jadi manten', penulis: 'hayati', 'jumlah halaman': 250

buku.tahun = 2022;
buku.terjual = 3000;
console.log(buku);

buku["penerbit"] = "gramedia"; 
console.log(buku); //judul: 'mantan jadi manten', penulis: 'hayati', 'jumlah halaman': 250, penerbit: "gramedia, tahun: 2022, terjual: 3000
```
### assign js
- Mengganti property 
```js
let hewan = {
  nama: "kucing",
  kaki: 4,
  warna: "putih",
};

console.log(hewan); //nama:'kucing', kaki:4, warna: 'putih'

hewan.nama = "kelinci";
hewan.warna = "kuning";
console.log(hewan); //nama: 'kelinci', kaki: 4, warna: 'putih'
```
### delete js
- Menghapus salah satu isi object
```js
let hewan = {
  nama: "kucing",
  kaki: 4,
  warna: "putih",
};
console.log(hewan); //nama:'kucing', kaki:4, warna: 'putih'

delete hewan.warna;
console.log(hewan); //nama:'kucing', kaki:4
```
### method js
```js
const greeting = {
  welcome: function () {
    return "halo selamat datang";
  },
  afterPay: function () {
    return "Terimakasih sudah membeli produk kami";
  },
};

console.log(greeting.welcome()); //halo selamat datang
console.log(greeting.afterPay()); //Terimakasih sudah membeli produk kami
```
- Keys
```js
let siswa = {
  nama: "dila",
  umur: 17,
  hobi: "membaca",
};

console.log(siswa); //nama: 'dila', umur: 17, hobi: 'membaca'

console.log(Object.keys(siswa)); //[nama, umur, hobi]
```
- values
```js
console.log(Object.values(siswa)); //['dila, 17, 'membaca'
```
### NestedObject
- Nested object : menyimpan object di dalam object
```js
let buku = {
  judul: "tips jago javascript",
  tahun: 2022,
  penulis: {
    penulis1: {
      nama: "Reyhan",
      umur: 28,
      kota: "jakarta",
    },
    penulis2: {
      nama: "aby",
      umur: 25,
      kota: "bandung",
    },
  },
};

console.log(buku); //judul: 'tips jago javascript', penulis: {penulis1:{..}, penulis2:{..}}, tahun: 2022
console.log(buku.penulis.penulis1.nama); //Rayhan
```
### loop object
```js
let siswa = {
  nama: "Reyhan",
  umur: 22,
  asal: "jakarta"
};

for (let key in siswa) {
  console.log(siswa[key]); 
  console.log(key, ": ini dari key"); //Reyhan nama: ini dari key, 22 umur: ini dari key, jakarta asal: ini dari key
}
```
### array object
```js
let users = [
  {
    nama: "dila",
    umur: 17,
    alamat: "bandung",
  },

  {
    nama: "audzan",
    umur: 18,
    alamat: "jakarta",
  },
  {
    nama: "dolton",
    umur: 16,
    alamat: "sulawesi",
  },
];

console.log(users);

let data = users.map((el) => {
  // console.log(el.nama);
  el.status = "aktif";
  return el; //dila, audzan, dolton
});
```
## JavaScript Modules
- JS Modules adalah cara untuk memisahkan kode ke file yang berbeda
- Keuntungan : 
1. mudah untuk mengelola kode
2. kode ga numpuk di satu file

- Cara :
1. tambah type="module" pada script utama
2. siapkan script ke-2 untuk melakukan export
3. lakukan import pada script utama
- Export : barang keluar
- Import : barang masuk
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  
  <!-- file yg ada disini cuma bisa melakukan import -->
  <script src="./indonesia.js" type="module"></script>

</body>
</html>
```
```js
//file jepang.js
export let motor =["suzuki", "yamaha", "honda"]
```
```js
//file indonesia.js
import {motor} from './indonesia.js';
console.log(motor); //['suzuki', 'yamaha', 'honda']
```
- export dapat dilakukan pada variable, function, class
- kata kunci "export" dapat melakukan banyak export
- "export" di tangkap (import) menggunakan kurung kurawal
- "export default" cuma bisa 1 aja yg di export
- "export default" ditangkap tanpa kurung kurawal
## Recursive
### function recursive
- function recursive punya : 
1. base case -> titik paling kecil (berhenti)
2. recursion case -> titik dia manggil diri dia sendiri
```js
function deretAngka(n){
  if (n == 1) {
    console.log(n)
  } else {
    deretAngka(n-1)
    console.log(n);
  }
} // deretAngka(7)
```
## JS single thread, non-blocking, asyncronus
### Single thread (1 jalur) 
- single thread, ada 2:
1. blocking : menunggu proses pertama selesai, baru bisa dilanjut ke proses kedua dan begitu seterusnya
2. non-blocking : ketika proses pertama belum selesai dilakukan, kita bisa melanjutkan ke proses kedua tidak perlu menunggu proses pertama selesai
### syncronus
- syncronus : dilakukan secara berurutan
### asyncronus
- asyncronus : urutan perintah yang acak karena harus memanggilperintah yang belum selesai
- asyncronus ada 3 :
1. callback
```js
//contoh callback
console.log("A")
butuh waktu 100ms -> console.log("B")
console.log("C") //A C B
```
2. promises : ketika proses sudah direncanakan/dijadwalkan, kemudian dipending dan ada 2 pilihan antara prosesnya di cancel atau buat jadwal proses baru
3. asyncommit


