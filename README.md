LAPORAN PRAKTIKUM 3 PEMROGRAMAN WEB

NAMA    : Eka Sari Praditya
NIM     : 31210021
KELAS   : I253A

# 1 Membuat Dokumen HTML
![Gambar 1](screenshot/ss%20membuat%20dokumen%20html.png)
# 2 Mendeklarasikan CSS Internal
![Gambar 2](screenshot/ss%20mendeklarasikan%20css%20internal.png)
# 3 menambahkan Inline CSS
![Gambar 3](screenshot/ss%20menambahkan%20inline%20css.png)
# 4 Membuat CSS Eksternal
![Gambar 4](screenshot/ss%20membuat%20css%20eksternal.png)
# 5 Menambahkan CSS Selektor
![Gambar 5](screenshot/ss%20menambahkan%20css%20selektor.png)

Pertanyaan dan Tugas!
1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS
dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.
2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan
penjelasannya!
3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline
CSS pada elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser?
Berikan penjelasan dan contohnya!
4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector
tersebut terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada

browser? Berikan penjelasan dan contohnya! ( <p id="paragraf-1" class="text-
paragraf"> )

Jawaban!

1. Eksperimen mengubah dan menambah properti CSS
Eksperimen dilakukan dengan mengubah nilai properti CSS untuk melihat perubahan tampilan pada halaman web, seperti warna, ukuran teks, jarak, dan warna latar belakang.

body {
    background-color: lightgray;
    font-family: Arial, sans-serif;
}

h1 {
    color: green;
    font-size: 32px;
    text-align: center;
}

p {
    color: black;
    font-size: 18px;
    line-height: 1.5;
    background-color: white;
    padding: 10px;
}

2. Perbedaan selector h1 { ... } dengan #intro h1 { ... }
Selector h1 digunakan untuk memberikan gaya pada semua elemen HTML <h1> yang ada di halaman web.

Sementara itu, selector #intro h1 digunakan untuk memberikan gaya hanya pada elemen <h1> yang berada di dalam elemen yang memiliki ID intro.

# Contoh HTML: 
h1 Judul Pertama /h1

div id="intro"
    h1 Judul Kedua /h1
/div

# Contoh CSS: 
h1 {
    color: blue;
}

#intro h1 {
    color: red;
}

*Judul Pertama akan berwarna biru.
*Judul Kedua akan berwarna merah karena berada di dalam elemen dengan ID intro. Selector #intro h1 memiliki tingkat spesifisitas lebih tinggi daripada selector h1, sehingga deklarasi tersebut berlaku pada Judul Kedua.

3. Prioritas CSS internal, eksternal, dan inline
CSS internal ditulis menggunakan tag <style> di dalam file HTML. CSS eksternal ditulis dalam file terpisah dengan ekstensi .css, sedangkan inline CSS ditulis langsung pada atribut style di elemen HTML.

# Contoh CSS internal:
style>
    p {
        color: blue;
    }
/style>
# Contoh CSS eksternal (style.css):
p {
    color: green;
}
# Contoh HTML dengan inline CSS:
p style="color: red;">Belajar CSS /p>

Hasil yang ditampilkan: Teks Belajar CSS akan berwarna merah karena inline CSS memiliki prioritas lebih tinggi daripada deklarasi internal dan eksternal biasa, selama tidak ada aturan prioritas khusus yang mengubah hasilnya, seperti !important.

Namun, jika ketiga deklarasi memiliki tingkat kepentingan yang sama dan selector yang sama, CSS internal atau eksternal yang ditulis paling akhir akan menang di antara keduanya. Posisi penulisan dan spesifisitas juga perlu diperhatikan.

4. Prioritas selector ID dan Class
Apabila sebuah elemen HTML memiliki ID dan Class sekaligus, selector ID memiliki tingkat spesifisitas lebih tinggi daripada selector Class.

# Contoh HTML:
p id="paragraf-1" class="text-paragraf">
    Ini adalah contoh paragraf.
/p>
# Contoh CSS:
#paragraf-1 {
    color: red;
}

.text-paragraf {
    color: blue;
}
gi
Hasil yang ditampilkan: Teks paragraf akan berwarna merah karena selector ID (#paragraf-1) memiliki tingkat spesifisitas lebih tinggi daripada selector Class (.text-paragraf).
Urutan spesifisitas dasar CSS dari yang lebih tinggi ke lebih rendah adalah:
1. Inline CSS.
2. Selector ID, misalnya #paragraf-1.
3. Selector Class, misalnya .text-paragraf.
4. Selector elemen, misalnya p.
Urutan tersebut berlaku untuk deklarasi normal dengan kondisi yang setara. Aturan !important, asal stylesheet, dan beberapa aturan khusus lainnya dapat memengaruhi hasil akhir.