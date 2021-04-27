**ronde1**

Pada ronde ini, peserta diminta agar membuat rantai user(User A, User B) yang mana pemiliknya ada orang yang sama dan menghitung jumlah contact yang dimiliki masing-masing user.

Sebagai contoh, outnya nya adalah: {'1-2458-98519-115061-140081-165605-476346, 12'}
Pada contoh diatas, user ke 1, 2458, 98519, 115061, 140081, 165605, 476346 adalah orang yang sama. Hal ini dikarenakan entah itu email, nomer hp, order_id yang dimiliki memiliki kemiripan satu sama lain.

Dataset terdiri dari 500.000+ user, sehingga ukuran file tidak bisa diupload ke github karena terlalu besar (50 MB). Untuk melihatnya dapat mengunjungi link berikut:
https://drive.google.com/file/d/1CAWlpqmbRacKt05OX07UIbtXFUF3u_nR/view?usp=sharing

Pada kompetisi ini, tim saya mendapat akurasi 95.326% (dapat dilihat pada link kaggle yang saya berikan di folder sebelumnya), kesulitan pada tantangan ini adalah bagaimana cara agar proses yang dilakukan hanya memakan waktu yang sedikit. Jawabannya adalah dengan menggunakan tipe data Map.
