# Lab4Web
Nur Laila
(312310149)
TI 23 A1

# Laporan Praktikum
## 1 buat lab4_box.html 
```sh
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Box Element</title>
</head>
<body>
<header>
<h1>Box Element</h1>
</header>
</body>
</html>
```
![image](https://github.com/user-attachments/assets/1bd8e36b-a8a2-4081-9c6d-2077d977a9a9)   
berikut perintah untuk membuat dokumen HTML dengan nama file Lab4_box.html
## 2 Membuat Box Element
```sh
<section>
  <div class="div1">Div 1</div>
  <div class="div2">Div 2</div>
  <div class="div3">Div 3</div>
</section>
```
### CSS Float Property
```sh
<style>
div {
    float:left;
    padding: 10px;
}
.div1 {
    background: red;
}
.div2 {
    background: yellow;
}
.div3 {
    background: green;
}
```
![Screenshot 2024-10-22 092212](https://github.com/user-attachments/assets/5d6d3372-f128-49c0-8a2c-38604807b79f)  
tiga kotak (`div1`, `div2`, `div3`) dibuat dengan warna merah, kuning, dan hijau, lalu diatur agar sejajar secara horizontal menggunakan properti float.     
## 3 Mengatur Clearfix Element  
```sh
<section>
  <div class="div1">Div 1</div>
  <div class="div2">Div 2</div>
  <div class="div3">Div 3</div>
  <div class="div4">Div 4</div>
</section>
 CSS:
.div4 {
  background-color: blue;
  clear: left;
  float: none;
}
```
![Screenshot 2024-10-22 093151](https://github.com/user-attachments/assets/19b3d7b5-d0d0-4c58-8884-4135b8750bf7)   
menambahkan kotak keempat (`div4`) dengan warna biru yang diatur menggunakan properti clear
untuk memutuskan efek float dari elemen sebelumnya sehingga muncul di bawahnya,
bukan di sebelahnya. Ini digunakan untuk mengelola aliran tata letak dalam desain halaman.  
# Membuat Layout Sederhana
Buat folder baru dengan nama lab4_layout, kemudian buatlah file baru didalamnya dengan nama
home.html, dan file css dengan nama style.css.   
```sh
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout Sederhana</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
```
Kemudian buat kerangka layout dengan semantics element  
```sh
<header>
<h1>Layout Sederhana</h1>
</header>
<nav>
  <a href="home.html" class="active">Home</a>
  <a href="artikel.html">Artikel</a>
  <a href="about.html">About</a>
  <a href="kontak.html">Kontak</a>
</nav>
<section id="hero"></section>
<section id="wrapper">
  <section id="main"></section>
  <aside id="sidebar"></aside>
</section>
<footer>
  <p>&copy; 2021 - Universitas Pelita Bangsa</p>
</footer>
```
![Screenshot 2024-10-22 093648](https://github.com/user-attachments/assets/cd4ad371-4aaf-4ac3-8dae-8b99c92d9f8b)
Di dalam file HTML, elemen-elemen semantik seperti `<header>`, `<nav>`, <section>, dan `<footer>` digunakan untuk membuat kerangka dasar tata letak halaman. Elemen `<nav>` berfungsi untuk navigasi, sementara `<section>` digunakan untuk menempatkan konten utama (`#main`) dan sidebar (`#sidebar`). Elemen ini membantu menjaga struktur halaman tetap bersih dan terorganisir.   
## Menambahkan kode CSS untuk membuat layoutnya
```sh
/* import google font */
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0,300;0,700;1,300&display=swap');

/* Reset CSS */
* {
    margin: 0;
    padding: 0;
}
body {
    line-height:1;
    font-size:100%;
    font-family:'Open Sans', sans-serif;
    color:#5a5a5a;
}

#container {
    width: 980px;
    margin: 0 auto;
    box-shadow: 0 0 1em #cccccc;
}

/* header */
header {
    padding: 20px;
}
header h1 {
    margin: 20px 10px;
    color: #b5b5b5;
}
```
![Screenshot 2024-10-22 094226](https://github.com/user-attachments/assets/359f8efe-a583-4489-8a35-fd4c72a85a99)   
mengimpor font Google Open Sans untuk digunakan di seluruh halaman. Kemudian, menggunakan "Reset CSS" untuk menghapus margin dan padding default dari semua elemen, sehingga memberikan kontrol penuh atas tata letak. Properti `body` mengatur font dasar, ukuran teks, dan warna default teks. Bagian `#container` mengatur lebar halaman menjadi `980px`, dipusatkan dengan margin otomatis, dan diberi efek bayangan halus. Untuk header, padding ditambahkan, dan warna teks pada judul (`h1`) diatur menjadi abu-abu terang (`#b5b5b5`), membuat tampilannya bersih dan rapi. 
## Membuat Navigasi 
```sh
/* navigasi */
nav {
    display: block;
    background-color: #1f5faa;
}
nav a {
    padding: 15px 30px;
    display: inline-block;
    color: #ffffff;
    font-size: 14px;
    text-decoration: none;
    font-weight: bold;
}
nav a.active,
nav a:hover {
    background-color: #2b83ea;
}
```
![Screenshot 2024-10-22 094404](https://github.com/user-attachments/assets/2a6537e7-3f57-4a96-bee6-9cd557422f4d)   
Kode ini mengatur gaya untuk elemen navigasi. Navigasi diberi latar belakang biru gelap (`#1f5faa`), dengan tautan (link) yang tampil sebagai blok inline, diberi padding, dan teks putih. Ketika tautan aktif atau di-hover, latar belakangnya berubah menjadi biru yang lebih terang (`#2b83ea`) untuk memberikan efek interaktif.  
## Membuat Hero Panel
```sh
<section id="hero">
<h1>Hello World!</h1>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
elit, iaculis innisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
pretium ac.</p>
<a href="home.html" class="btn btn-large">Learn more &raquo;</a>
</section>
```
CSS:
```sh
/* Hero Panel */
#hero {
    background-color: #e4e4e5;
    padding: 50px 20px;
    margin-bottom: 20px;
}
#hero h1 {
    margin-bottom: 20px;
    font-size: 35px;
}
#hero p {
    margin-bottom: 20px;
    font-size: 18px;
    line-height: 25px;
}
```
![Screenshot 2024-10-22 100446](https://github.com/user-attachments/assets/a68f1c0d-81f8-4277-af08-00e68783d038)   
Kode ini membuat Hero Panel, sebuah elemen yang menonjol di halaman web. Bagian HTML menggunakan elemen `<section>` dengan ID hero, berisi judul besar, paragraf, dan tombol "Learn more". Pada CSS, panel ini diberi latar belakang abu-abu terang (`#e4e4e5`), dengan padding lebar untuk ruang, dan margin bawah untuk memisahkannya dari elemen lain.  
## Mengatur Layout Main dan Sidebar 
```sh
/* main content */
#wrapper {
    margin: 0;
}
#main {
    float: left;
    width: 640px;
    padding: 20px;
}
/* sidebar area */
#sidebar {
    float: left;
    width: 260px;
    padding: 20px;
}
```
### Membuat Sidebar Widget
```sh
<aside id="sidebar">
  <div class="widget-box">
    <h3 class="title">Widget Header</h3>
    <ul>
      <li><a href="#">Widget Link</a></li>
      <li><a href="#">Widget Link</a></li>
      <li><a href="#">Widget Link</a></li>
      <li><a href="#">Widget Link</a></li>
      <li><a href="#">Widget Link</a></li>
    </ul>
  </div>
  <div class="widget-box">
    <h3 class="title">Widget Text</h3>
    <p>Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt
    arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer
    pharetra est nunc, nec pretium nunc pretium ac.</p>
  </div>
</aside>
```
Menambahkan CSS 
```sh
/* widget */
.widget-box {
    border:1px solid #eee;
    margin-bottom:20px;
}
.widget-box .title {
    padding:10px 16px;
    background-color:#428bca;
    color:#fff;
}
.widget-box ul {
    list-style-type:none;
}
.widget-box li {
    border-bottom:1px solid #eee;
}
.widget-box li a {
    padding:10px 16px;
    color:#333;
    display:block;
    text-decoration:none;
}
.widget-box li:hover a {
    background-color:#eee;
}
.widget-box p {
    padding:15px;
    line-height:25px;
}
```
![Screenshot 2024-10-22 100850](https://github.com/user-attachments/assets/34c521dd-179c-41df-86a4-0c4e0b607df5)  
Kode ini membuat sebuah Sidebar Widget yang terdiri dari dua bagian. Bagian pertama adalah daftar tautan (links) dengan header Widget Header, dan bagian kedua adalah teks deskriptif dengan header Widget Text. Pada CSS, setiap widget diberi batas tipis (`1px solid #eee`) dan margin bawah untuk memisahkan widget secara visual. Header widget (`.title`) diberi latar belakang biru `(#428bca)` dan teks putih, sementara tautan diatur dengan padding dan warna abu-abu. Saat di-hover, tautan berubah latar belakang menjadi abu-abu muda untuk efek interaktif. 
## Mengatur Footer 
```sh
/* footer */
footer {
  clear:both;
  background-color:#1d1d1d;
  padding:20px;
  color:#eee;
}
```
![image](https://github.com/user-attachments/assets/6893d874-94a7-4d61-a6c3-68376503f898)   

## Menambahkan Elemen lainnya pada Main Content 
```sh
<section id="main">
                <div class="row">
                    <div class="box">
                        <img src="https://dummyimage.com/120/db7d25/fff.png" alt="" class="image-circle">
                        <h3>Heading</h3>
                        <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                        <a href="#" class="btn btn-default">View detail</a>
                    </div>
                    <div class="box">
                        <img src="https://dummyimage.com/120/3e73e6/fff.png" alt="" class="image-circle">
                        <h3>Heading</h3>
                        <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                        <a href="#" class="btn btn-default">View detail</a>
                    </div>
                    <div class="box">
                        <img src="https://dummyimage.com/120/71e6d4/fff.png" alt="" class="image-circle">
                        <h3>Heading</h3>
                        <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
                        <a href="#" class="btn btn-default">View detail</a>
                    </div>
                </div>
            </section>
```
Kemudian tambahkan CSS.
```sh
/* box */
.box {
  display:block;
  float:left;
  width:33.333333%;
  box-sizing:border-box;
  -moz-box-sizing:border-box;
  -webkit-box-sizing:border-box;
  padding:0 10px;
  text-align:center;
}
.box h3 {
  margin: 15px 0;
}
.box p {
  line-height: 20px;
  font-size: 14px;
  margin-bottom: 15px;
}
box img {
  border: 0;
  vertical-align: middle;
}
.image-circle {
  border-radius: 50%;
}
.row {
  margin: 0 -10px;
  box-sizing: border-box;
  -moz-box-sizing: border-box;
  -webkit-box-sizing: border-box;
}
.row:after, .row:before,
.entry:after, .entry:before {
  content:'';
  display:table;
}
.row:after,
.entry:after {
  clear:both;
}
```
![Screenshot (459)](https://github.com/user-attachments/assets/e71482f5-a2c7-4df4-b697-6858432073fe)   

Kode ini menambahkan elemen tambahan pada Main Content berupa tiga box yang berisi gambar, judul, paragraf, dan tombol tautan. Setiap box memiliki layout yang diatur dalam satu baris, dengan gambar berbentuk lingkaran `(.image-circle)` dan konten yang diatur rapi dalam proporsi sepertiga dari lebar kontainer. CSS memastikan tata letak responsif menggunakan properti `float`, `box-sizing`, dan pengaturan margin untuk menjaga jarak antar elemen. Setiap box memiliki teks yang rata tengah dan tombol yang disesuaikan untuk navigasi.    
## Menambahkan Content Artikel 
```sh
 <hr class="divider" />
        <article class="entry">
            <h2>First featurette heading.</h2>
            <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
                elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
                vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
                pretium ac.</p>
        </article>
        <hr class="divider" />
        <article class="entry">
            <h2>First featurette heading.</h2>
            <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="" class="right-img">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
                elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
                vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
                pretium ac.</p>
        </article>
 <hr class="divider" />
        <article class="entry">
            <h2>First featurette heading.</h2>
            <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="" class="right-img">
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
                elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
                vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
                pretium ac.</p>
        </article>
```
Kemudian Tambahkan CSS 
```sh
.divider {
    border:0;
    border-top:1px solid #eeeeee;
    margin:40px 0;
    }
    /* entry */
    .entry {
    margin: 15px 0;
    }
    .entry h2 {
    margin-bottom: 20px;
}
.entry p {
    line-height: 25px;
}
.entry img {
    float: left;
    border-radius: 5px;
    margin-right: 15px;
}
.entry .right-img {
    float: right;
}
```
![Screenshot 2024-10-22 101453](https://github.com/user-attachments/assets/f4264147-4d34-479c-8670-05a06171cee5)   
Kode ini menambahkan konten artikel ke dalam layout dengan tiga elemen artikel (`<article>`) yang masing-masing berisi judul, gambar, dan paragraf. Setiap artikel dipisahkan oleh garis horizontal (`<hr>`) yang diatur menggunakan kelas divider untuk memberikan tampilan yang bersih. Gambar dalam artikel diatur untuk mengalir di kiri atau kanan teks, dengan CSS yang mengatur margin dan `border-radius`, menciptakan tampilan yang rapi dan terorganisir. Desain ini memastikan teks dapat dibaca dengan baik berkat pengaturan `line-height` dan margin yang tepat pada elemen teks.

# Jawaban dan Tugas
## 1 Tambahkan Layout untuk menu About
=> Menambahkan layout yang berisi deskripsi, portfolio, dll
```sh
        <section id="about">
            <h2>Who We Are</h2>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Proin auctor lacus nec sapien malesuada, at viverra purus malesuada. Phasellus scelerisque nulla sit amet turpis vestibulum tincidunt.</p>

            <h2>Our Portfolio</h2>
            <div class="portfolio">
                <div class="portfolio-item">
                    <img src="https://dummyimage.com/150/3e73e6/fff.png" alt="Portfolio Item">
                    <h3>Project 1</h3>
                    <p>Description of the project.</p>
                </div>
                <div class="portfolio-item">
                    <img src="https://dummyimage.com/150/db7d25/fff.png" alt="Portfolio Item">
                    <h3>Project 2</h3>
                    <p>Description of the project.</p>
                </div>
                <div class="portfolio-item">
                    <img src="https://dummyimage.com/150/71e6d4/fff.png" alt="Portfolio Item">
                    <h3>Project 3</h3>
                    <p>Description of the project.</p>
                </div>
            </div>
        </section>

        <footer>
            <p>&copy; 2021 - Universitas Pelita Bangsa</p>
        </footer>
    </div>
</body>
</html>
```
membuat CSS 
```sh
/* About section */
#about {
    padding: 20px;
}
.portfolio {
    display: flex; /* Menjadikan container fleksibel */
    justify-content: space-between; /* Menyebar item secara merata */
    margin-top: 20px;
    flex-wrap: wrap; /* Memungkinkan item membungkus jika terlalu banyak */
}
.portfolio-item {
    width: calc(33.333% - 20px); /* Mengatur lebar setiap item, mengurangi margin */
    text-align: center;
    margin-bottom: 20px; /* Menambahkan jarak antar item */
}
.portfolio-item img {
    width: 100%;
    border-radius: 5px;
    margin-bottom: 10px;
}
```
hasil yang didapat akan tertampil seperti ini
![image](https://github.com/user-attachments/assets/c7944efc-3856-4857-bcd5-7f196a826308)  
Terdapat bagian deskripsi dan portfolio dengan gambar proyek.  
Menggunakan layout tiga kolom untuk portfolio item.    

## 2 Membuat Layout Contatc
=> yang berisi form isian: nama, email, message, dll  
```sh
 <section id="contact">
            <h2>Get In Touch</h2>
            <form action="#" method="post">
                <label for="name">Name:</label>
                <input type="text" id="name" name="name" required>

                <label for="email">Email:</label>
                <input type="email" id="email" name="email" required>

                <label for="message">Message:</label>
                <textarea id="message" name="message" required></textarea>

                <button type="submit">Send Message</button>
            </form>
        </section>
```
Menambahkan Style CSS:
```sh
/* Contact form */
#contact {
    padding: 20px;
}
#contact form {
    display: flex;
    flex-direction: column;
    width: 100%;
    max-width: 500px;
    margin: 0 auto;
}
#contact form label {
    margin-top: 10px;
    font-weight: bold;
}
#contact form input,
#contact form textarea {
    padding: 10px;
    margin-top: 5px;
    border: 1px solid #ddd;
    border-radius: 5px;
}
#contact form button {
    padding: 10px;
    background-color: #1f5faa;
    color: #ffffff;
    border: none;
    margin-top: 20px;
    cursor: pointer;
    border-radius: 5px;
}
#contact form button:hover {
    background-color: #2b83ea;
}
```
![image](https://github.com/user-attachments/assets/b478228f-0661-4de8-86f6-d500c0950b00)
Form kontak dengan field untuk nama, email, dan pesan.  
Tombol "Send Message" yang berfungsi untuk mengirim form.  


















