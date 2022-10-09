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

