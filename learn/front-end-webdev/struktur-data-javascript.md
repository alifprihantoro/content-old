Array, HashMap, dan Object adalah tiga struktur data yang berbeda dalam bahasa pemrograman JavaScript. Berikut adalah penjelasan dan contoh penggunaan masing-masing:

1. Array
Array adalah tipe data yang digunakan untuk menyimpan kumpulan nilai atau objek dalam satu variabel. Nilai atau objek dalam array dapat diakses melalui indeks numerik. Contoh:
```javascript
const fruits = ['apple', 'banana', 'orange'];
console.log(fruits[0]); // output: 'apple'
```
Fungsi array antara lain untuk:

- Menyimpan data dalam jumlah yang banyak.
- Mengurutkan data.
- Mengelola data secara dinamis.
2. HashMap
HashMap (atau Map) adalah tipe data yang digunakan untuk menyimpan kumpulan nilai atau objek dengan pasangan kunci-nilai. Kunci harus unik dan digunakan untuk mengakses nilai terkait. Contoh:
```javascript
const student = new Map();
student.set('name', 'John');
student.set('age', 20);
console.log(student.get('name')); // output: 'John'
```
Fungsi HashMap antara lain untuk:

- Menyimpan data dengan pasangan kunci-nilai.
- Mengelola data dengan cara yang lebih efisien dan mudah dibaca.
3. Object
Object adalah tipe data yang digunakan untuk menyimpan kumpulan properti atau metode dalam satu variabel. Properti dapat diakses melalui nama properti. Contoh:
```javascript
const person = {name: 'John', age: 20};
console.log(person.name); // output: 'John'
```
Fungsi Object antara lain untuk:

- Mengelola data dengan cara yang lebih kompleks dan fleksibel.
- Mengorganisir data dalam sebuah objek yang berkaitan dengan fungsi-fungsi tertentu.

Dalam ringkasan, Array digunakan untuk menyimpan data dalam jumlah besar dengan pengaksesan melalui indeks, HashMap digunakan untuk menyimpan data dalam pasangan kunci-nilai, dan Object digunakan untuk mengelola data yang lebih kompleks dan fleksibel dengan properti dan metode.
