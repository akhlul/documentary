# Review Pelatihan Pascal #1

## Ringkasan
Pelatihan pascal pada pertemuan kali ini (5/4/2016) membahas mengenai :

 - Sintaks Dasar
 - Operand
 - Input & Output
 - If..then..else..


## Sintaks Dasar
untuk membuat suatu program dasar dalam pascal, setidaknya mengetahui bentuk dasar nya. mari kita contohkan dengan membuat program *Hello World*. aturan mainnya setiap perintah harus ditutup dengan sebuah `;`.

```{pascal}
program helloworld;
uses crt;

begin
  write('hello');
  writeln(' world');
end.
```

#### Penjelasan

 - `program` : memberi nama program tersebut, nama program tidak boleh menggunakan karakter `-`
 - `uses` : fungsi menggunakan suatu library di pascal
 - `begin ... end` : sebuah blok perintah, dalam kasus diatas merupakan suatu perintah utama oleh karena itu harus ditutup dengan sebuah titik

> #### beda `write` dengan `writeln`
> kalau `write` cuma nulis di parameternya aja (parameter ntu yang ada didalem tanda kurung suatu perintah) sedangkan `writeln` setelah nulis bakalan nge-**enter** gitu.


## Variabel
setiap variabel harus dideklarasikan terlebih dahulu karena pascal itu *strong-typed programming language*, gak bisa ngedetect sendiri. contohnya yang gk perlu kita tentuin tipenya dlu sebelum buat variabel itu **Javascript** & **Python**. setidaknya ada 4 tipe variabel yang bakalan sering dipake (subjektif penulis) yakni kayak contoh dibawah :

```{pascal}
program variabeldasar;
uses crt;

var
  q : integer;
  w : real;
  r : char;
  t : string;

begin
  q := 12;
  w := 144.44;
  e := 'k';
  t := 'selamat datang di alfamidi';
  { perintah pertama }
  writeln(q, ' ', w, ' ', r);
  writeln(t);
  { perintah kedua }
  writeln(q, ' ', w:0:2, ' ', r, ' ', t);
  writeln(t:50);
end.
```

coba *inspeksi* apa perbedaan pada perintah pertama dan perintah kedua dalam program `variabeldasar`? **jawaban ada diakhir ya**

tipe variabel yang lengkapnya sih bisa liat gambar ini :


## Operator
operator yang dimaksut adalah operator dalam perhitungan *(kali bagi tambah kurang dan sebagainya)*. tabelnya sebagai berikut :


jelas kayaknya bagian yg ini :D


## Input & Output
setiap bahasa kayaknya pasti ada beginiannya, cus liat contohnya aja :

```{pascal}
program inout;
uses crt;

var 
  y, x : string;

begin
  writeln('halo, saya robot kakaktua kembar, bakal mengulangi setiap input kalimat kamu!');
  write('masukkan input : ');
  readln(x, y);
  writeln('kakaktua 1 : ',x);
  writeln('kakaktua 2 : ',y);
end.
```

> `read` atau `readln` bakalan menunggu input masuk dari ketikan user. adapun beda `read` dan `readln` adalah penggunaan pemisah antara inputnya. kalo `read` inputnya dapat dipisahkan dengan enter atau spasi, sedangkan `readln` inputnya cuma dapat dipisahkan dengan enter saja.

nah bedain program `inout` dengan `inout2` dibawah!!!  

```{pascal}
program inout2;
uses crt;

var 
  y, x : integer;

begin
  writeln('halo, saya robot kakaktua kembar, bakal mengulangi setiap input angka kamu!');
  write('masukkan input : ');
  readln(x, y);
  writeln('kakaktua 1 : ',x);
  writeln('kakaktua 2 : ',y);
end.
```


## Flow Control (If)
untuk ngatur logika suatu program maka kita perlu suatu perintah tertentu, nah salah satunya yakni `if .. then .. ;` ini. adapun perintah ini dalam pascal merupakan satu kesatuan perintah. bentuk lainnya yakni `if .. then .. else .. ;`.

#### 2 Bentuk Umum 
```{pascal}
1.  if [condition] then [true statement];

2.  if [condition] them [true statement] else [false statement];
```
