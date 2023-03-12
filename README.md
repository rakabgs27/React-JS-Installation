# 02.1 Your First Component

Komponen adalah salah satu konsep inti dari React. Mereka adalah dasar untuk membangun antarmuka pengguna (UI), sehingga membuatnya menjadi tempat yang tepat untuk memulai perjalanan React!

# Defining Component
Secara tradisional, ketika membuat halaman web, pengembang web menandai konten mereka dan kemudian menambahkan interaksi dengan menambahkan sedikit JavaScript. Ini berfungsi dengan baik ketika interaksi hanyalah kebutuhan yang bagus di web. Sekarang interaksi diharapkan untuk banyak situs dan semua aplikasi. React menempatkan interaktivitas terlebih dahulu sambil tetap menggunakan teknologi yang sama: komponen React adalah fungsi JavaScript yang dapat Anda tambahkan markup-nya.<br>
```
export default function Profile() {
  return (
    <img
      src="https://i.imgur.com/MK3eW3Am.jpg"
      alt="Katherine Johnson"
    />
  )
}
```
## Hasil 
![image](https://user-images.githubusercontent.com/95867776/224523860-919fb1b5-564b-40b6-bbdb-dc0d12dc8ecc.png) <br><br>
Cara Membuat Component : 
# Step 01 : Export the component
Awalan "export default" adalah sintaks standar JavaScript (tidak spesifik untuk React). Ini memungkinkan Anda menandai fungsi utama dalam sebuah file sehingga Anda dapat mengimpornya dari file lain di kemudian hari. 

# Step 02 : Define the function
Dengan function Profile() { } Anda mendefinisikan sebuah fungsi JavaScript dengan nama Profile.

NB : 
Komponen React adalah fungsi JavaScript biasa, tetapi nama mereka harus diawali dengan huruf kapital atau mereka tidak akan berfungsi!

# Step 03 : Add markup
Komponen mengembalikan tag <img /> dengan atribut src dan alt. <img /> ditulis seperti HTML, tetapi sebenarnya itu adalah JavaScript di bawah kap, sintaks ini disebut JSX, dan memungkinkan Anda menyematkan markup di dalam JavaScript.

Pernyataan return dapat ditulis dalam satu baris, seperti dalam komponen ini:
```
return <img src="https://i.imgur.com/MK3eW3As.jpg" alt="Katherine Johnson" />;
```
Tetapi jika markup Anda tidak semuanya berada dalam satu baris dengan kata kunci return, Anda harus membungkusnya dalam sepasang tanda kurung seperti ini:
```
return (
  <div>
    <img src="https://i.imgur.com/MK3eW3As.jpg" alt="Katherine Johnson" />
  </div>
);
```
NB : Tanpa tanda kurung, kode apapun pada baris setelah return akan diabaikan!

# Using Component
Sekarang setelah Anda telah mendefinisikan komponen Profile Anda, Anda dapat menempatkannya di dalam komponen lain. Misalnya, Anda dapat mengekspor komponen Galeri yang menggunakan beberapa komponen Profile:
```
function Profile() {
  return (
    <img
      src="https://i.imgur.com/MK3eW3As.jpg"
      alt="Katherine Johnson"
    />
  );
}

export default function Gallery() {
  return (
    <section>
      <h1>Amazing scientists</h1>
      <Profile />
      <Profile />
      <Profile />
    </section>
  );
}
```
## Hasil
![image](https://user-images.githubusercontent.com/95867776/224524156-a653c2f1-381b-46f7-8d89-d32fc7fce13c.png)<br><br>


## What the browser sees
Perhatikan perbedaan pada huruf besar kecilnya:

tag section ditulis dengan huruf kecil, sehingga React tahu bahwa kita mengacu pada tag HTML.<br>
tag Profile diawali dengan huruf kapital P, sehingga React tahu bahwa kita ingin menggunakan komponen kita yang bernama Profile.<br>
Dan Profile berisi bahkan lebih banyak HTML: <img />. Pada akhirnya, inilah yang dilihat oleh browser:
```
 <section>
  <h1>Amazing scientists</h1>
  <img src="https://i.imgur.com/MK3eW3As.jpg" alt="Katherine Johnson" />
  <img src="https://i.imgur.com/MK3eW3As.jpg" alt="Katherine Johnson" />
  <img src="https://i.imgur.com/MK3eW3As.jpg" alt="Katherine Johnson" />
</section>
```
