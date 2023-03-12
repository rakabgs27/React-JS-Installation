# 01.2. Add React to a Website

React telah dirancang dari awal untuk adopsi bertahap. Sebagian besar situs web tidak (dan tidak perlu) dibangun sepenuhnya dengan React. Panduan ini menunjukkan bagaimana menambahkan beberapa "sprinkles of interactivity" ke halaman HTML yang sudah ada.

# Step 01 : Add a toot HTML tag
![image](https://user-images.githubusercontent.com/95867776/224518917-799cb2c8-d723-464e-a855-4b941df62ebd.png) <br>
Istilah "root" digunakan karena di sinilah pohon React akan dimulai. Anda dapat menempatkan tag HTML "root" seperti ini di mana saja di dalam tag <body>. Biarkan kosong karena React akan menggantikan isinya dengan komponen React Anda.

# Step 02 : Add the script tags
![image](https://user-images.githubusercontent.com/95867776/224519043-415d0620-1ec5-46f0-a29e-3ea82f5969ef.png)
Pada halaman HTML, tepat sebelum tag penutup </body>, tambahkan tiga tag <script> untuk file-file berikut:

react.development.js memungkinkan Anda untuk mendefinisikan komponen React. <br>
react-dom.development.js memungkinkan React merender elemen HTML ke DOM. <br>
like-button.js adalah tempat di mana Anda akan menulis komponen pada langkah berikutnya! <br>

# Step 03 : Create a React Component
Anda diminta untuk membuat sebuah file bernama like-button.js di samping file HTML Anda dan menambahkan potongan kode berikut, lalu menyimpan file tersebut. Potongan kode ini mendefinisikan sebuah komponen React yang disebut LikeButton. <br>
![image](https://user-images.githubusercontent.com/95867776/224519824-04c49b1a-a5ad-4475-9e4b-5af04c07dc68.png)

# Step 04 : Add your React component to the page
Terakhir, tambahkan tiga baris kode pada akhir file like-button.js. Baris kode ini akan mencari <div> yang telah Anda tambahkan pada langkah pertama di file HTML, membuat sebuah root React, dan menampilkan komponen React "Like" button di dalamnya. <br>
![image](https://user-images.githubusercontent.com/95867776/224519856-6e041d85-bcd6-4cab-b93b-2ab5dcf5148a.png)
