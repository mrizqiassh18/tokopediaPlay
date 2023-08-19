# tokopediaPlay
File Backend terdapat pada Branch backend
File Frontend terdapat pada Branch frontend

1. Berikut ini adalah link program yang sudah dideploy
https://tokopedia-play-frontend-five.vercel.app/

2. Berikut ini link repository github untuk program yang dideploy (hanya terdapat perbedaan di host)
3. Frontend : https://github.com/mrizqiassh18/tokopediaPlay_Frontend.git
4. Backend : https://github.com/mrizqiassh18/tokopediaPlay_Backend.git

# Introduction
1. Project Name : Tokopedia Play Clone
2. Description : Aplikasi ini adalah clone dari website Tokopedia Play

# Features
Pada aplikasi ini kita dapat melakukan komentar pada setiap video yang ada

# How To Install and Run API
1. Buka folder backend pada Visual Studio Code
2. Buka terminal, lalu ketik npm install
3. Setelah selesai, pada terminal ketikan npm install nodemon -g (untuk install nodemon secara global), atau jika sudah ada nodemon, gunakan nodemon index.js
4. Selesai

# How To Install and Run React App
1. Buka folder frontend pada Visual Studio Code
2. Buka terminal,  lalu ketik npm install
3. Setelah selesai, ketikan npm start
4. Selesai, program sudah bisa dijalankan

# Scema Database
Pada database tokopediaPlay terdapat 3 collection yang diantaranya :
1. video_thumbnail yang memiliki property sebagai berikut :
   a. url : String (url gambar)
   b. title : String (judul gambar)
   c. youtubeId : String (youtube id yang digunakan untuk menampilkan video pada setiap index)
2. product_list yang memiliki property sebagai berikut :
   a. link_product : String (link tokopedia untuk item yang dituju)
   b. title : String (judul product)
   c. price : Number (harga barang)
   d. product_img : String (link gambar product)
   e. videoId : ObjectId (referensi id video)
3. comments yang memiliki property sebagai berikut:
   a. videoId : ObjectId (referensi id video)
   b. username : String (nama komentator)
   c. comment : String (komentar)
   d. created_at : timestamp (waktu dibuatnya komentar)

# API Structure
Terdapat dua pemanggilan method get dan penggunaan method post
1. router.get('/videos', getVideo); yang digunakan untuk memanggil data video_thumbnail dan menampilkannya pada HomePage.
2. router.get('/videos/:videoId', getVideoById); yang digunakan untuk memanggil tiga data berdasarkan id parameter video yaitu video_thumbnail, comments dan product_list dan menampilkannya pada halaman VideoDetailPage.
3. router.post('/videos/:videoId/comments', saveComment); yang digunakan untuk melakukan pengiriman form komentar dari component InputComment.
