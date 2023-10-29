# Muhamad-Muhtar-Allawi-5311421027-Praktek-Modul-4
Teknik Pencarian Blind Search
Nama : Muhamad Muhtar Allawi
Nim : 5311421027
Prodi : Teknik Elektro

MODUL 4
TEKNIK PENCARIAN BLIND SEARCH

1.	Algoritma BFS di atas memulai pencarian dari node awal (dalam kasus ini, node 3) dan secara berurutan mengeksplorasi node-node dalam graf dalam urutan lebar. Oleh karena itu, untuk menentukan bagaimana algoritma BFS menemukan node 8, 6, dan 7, kita dapat melihat urutan langkah-langkah yang dilakukan selama pencarian:

-	Algoritma BFS dimulai dari node 3, karena node ini adalah node awal yang dipilih.
-	Algoritma memeriksa node tetangga dari node 3, yaitu node 4 dan node 2, dan menambahkannya ke dalam antrian (queue) untuk diproses selanjutnya.
-	Selanjutnya, algoritma mengambil node pertama dari antrian, yaitu node 4, dan memeriksa tetangga-tetangga node 4, yaitu node 3, 5, dan 6. Node 3 tidak akan dimasukkan lagi ke dalam antrian karena telah dikunjungi sebelumnya. Node 5 dan 6 ditambahkan ke dalam antrian.
-	Algoritma terus berlanjut dengan mengambil node-node dari antrian. Node 2 akan diambil selanjutnya, tetapi tidak memiliki tetangga yang belum dikunjungi, jadi algoritma hanya melanjutkan.
-	Node-node 5 dan 6 akan diambil secara berurutan. Node 5 memiliki tetangga 4 dan 6, tetapi 4 telah dikunjungi sebelumnya. Jadi, yang ditambahkan ke antrian adalah node 6.
-	Node 1 adalah tetangga dari node 6 yang akan diambil selanjutnya dan dimasukkan ke dalam antrian.
-	Node-node 7 dan 8 adalah tetangga dari node 6, dan keduanya akan dimasukkan ke dalam antrian untuk diproses.
-	Selanjutnya, algoritma akan terus mengambil node-node dari antrian dan memeriksa tetangga-tetangga mereka.

Dengan demikian, pada akhir proses BFS, node 8, 6, dan 7 telah ditemukan oleh algoritma, dan urutan penjelajahannya adalah 8 (jarak 3 dari node 3), 6 (jarak 2 dari node 3), dan 7 (jarak 3 dari node 3).

Jadi, algoritma BFS menentukan node 8, 6, dan 7 dengan mengunjungi dan memeriksa node-node secara berurutan sesuai dengan jarak relatif mereka dari node awal (node 3).
•	Hasil dari running code adalah sebagai berikut:
 
•	Graph hasil dari blind search adalah sebagai berikut:
 




2.	Program yang telah dibuat adalah implementasi algoritma Breadth-First Search (BFS) pada grafik yang direpresentasikan dalam bentuk adjacency list. Mari kita bahas cara program ini bekerja hingga menghasilkan output.

Inisialisasi Grafik:
-	Program dimulai dengan menginisialisasi grafik dalam objek `MyGraph`.

Menambahkan Edge:
-	Selanjutnya, program menambahkan edge (sisi) ke grafik dengan menggunakan metode `addEdge`. Ini menciptakan keterhubungan antara node-node dalam grafik.

Inisialisasi Node:
-	Seluruh node dalam grafik memiliki atribut seperti `data` (nomor node), `distance` (jarak dari node awal), `predecessor` (node sebelumnya dalam jalur terpendek), dan `colour` (status warna node).

Breadth-First Search (BFS):
-	Algoritma BFS dimulai dengan memberi warna semua node dalam grafik menjadi `WHITE` (belum dikunjungi), mengatur jarak awal dari semua node menjadi tak terbatas (`Integer.MAX_VALUE`), dan node pendahulu (predecessor) menjadi `null`.

-	Kemudian, program memilih node awal yang ingin dihitung jaraknya. Dalam kasus, node awal adalah node 5.

-	Node awal (node 5) diberi warna `GRAY` (sedang dikunjungi), jaraknya diatur ke 0 (karena ini adalah node awal), dan tidak memiliki pendahulu.

-	Program menggunakan antrian (queue) untuk menjelajahi node-node. Node awal (node 5) dimasukkan ke dalam antrian.

-	Selama antrian tidak kosong, program melakukan loop berikut:
-	Node pertama dari antrian dihapus.
-	Program memeriksa node-node yang terhubung ke node yang sedang diproses. Ini dilakukan dengan memeriksa adjacency list dari node yang sedang diproses.
-	Jika node-node tersebut memiliki warna `WHITE` (belum dikunjungi), maka program akan memperbarui warna menjadi `GRAY`, jaraknya dihitung dari node sebelumnya, dan pendahulunya diatur menjadi node sebelumnya. Kemudian, node tersebut dimasukkan ke dalam antrian.
-	Node yang sedang diproses diberi warna `BLACK` (sudah selesai dikunjungi) dan dicetak ke layar dengan jaraknya.

-	Algoritma BFS akan terus berjalan hingga antrian kosong. Selama proses ini, BFS akan menghitung jarak terpendek dari node awal (node 5) ke semua node lain dalam grafik.


Hasil Output:
Output yang dapat lihat adalah urutan node yang sudah dikunjungi dengan jarak masing-masing node dari node awal (node 5).
Karena program dijalankan dengan node awal adalah 5, hasilnya adalah urutan node yang dapat dicapai dari node 5 beserta jaraknya. Dalam contoh, dari node 5, program menemukan node-node 4, 3, 2, 1, dan 0 dengan jarak masing-masing node dari node 5.
Dalam struktur pohon yang dibentuk, BFS mampu menemukan Node 5 pada tahap awal pencarian karena Node 5 adalah tetangga langsung dari Node 1 yang telah dikunjungi setelah Node 4, sesuai dengan prinsip pencarian secara lebar yang diterapkan oleh BFS.
•	Hasil dari running code adalah sebagai berikut:
 




3.	Pada gambar 4.6 Tree 2 saya telah membuat source code untuk menjalankan algoritma BFS untuk dapat menemukan node 9. Berikut hasil yang telah didapat:
 

Dalam hasil ini: 
-	(9,d=0) menunjukkan bahwa node awal adalah n9, dan jaraknya dari dirinya sendiri adalah 0 (karena itulah node awal). 
-	(8,d=1), (7,d=1), (10,d=1), dan (11,d=1) adalah node-node yang jaraknya 1 langkah (satu tepian) dari node awal, yaitu n9. 
-	(6,d=2), (5,d=2), dan (12,d=2) adalah node-node yang jaraknya 2 langkah dari node awal. 
-	(4,d=3), (3,d=3), dan (2,d=3) adalah node-node yang jaraknya 3 langkah dari node awal. 
-	(1,d=4) adalah node yang terjauh dari node awal, yaitu n9, dengan jarak 4 langkah. 
Hasil ini mencerminkan bagaimana algoritma BFS bekerja dengan menjelajahi grafik dari node awal ke tetangga-tetangga dan kemudian ke tetangga-tetangga dari tetangga-tetangga, dan seterusnya, sehingga menghitung jarak antara node-node tersebut dari node awal.



4.	Pada Gambar 4.7 Tree 3 saya telah membuat source code untuk menjalankan algoritma BFS untuk dapat menemukan node C. Dimana kita akan menginisialisasikan huruf-huruf tersebut dengan angka, sebagai berikut:
A = 1
B = 2
C = 3
D = 4
E = 5 
F = 6 
G = 7
H = 8
I = 9

Dengan Hasil yang didapat adalah sebagai berikut:
 

-	Node C (3,d=0) adalah node awal (node 7) dengan jarak 0 dari dirinya sendiri. 
-	Node I  (9,d=1) memiliki jarak 1 dari node awal (node 7/C). 
-	Node D (4,d=1) memiliki jarak 1 dari node awal (node 7/C). 
-	Node E (5,d=1) memiliki jarak 1 dari node awal (node 7/C). 
-	Node H (8,d=1) memiliki jarak 1 dari node awal (node 7/C). 
-	Node A (1,d=2) memiliki jarak 2 dari node awal (node 7/C). 
-	Node G (7,d=2) adalah node awal yang kembali ke dirinya sendiri, yang mana memiliki jarak 2 dari node awal (node 7/C). 
-	Node B (2,d=2) memiliki jarak 2 dari node awal (node 7/C). 
-	Node F (6,d=3) memiliki jarak 3 dari node awal (node 7/C). 
Hasil ini mencerminkan bagaimana algoritma BFS bekerja untuk menemukan jarak antara node awal (node 7) dan semua node lain dalam graf. Node-node ditandai dengan warna sesuai dengan status warna yang digunakan dalam algoritma BFS: WHITE (belum dikunjungi), GRAY (sedang dalam antrian untuk dikunjungi), dan BLACK (sudah dikunjungi). Jarak dari setiap node terhadap node awal juga ditampilkan dalam format (data,distance).  Sebagai contoh, node 3, 9, 4, 5, dan 8 memiliki jarak 1 dari node awal, node 7. Node 1, 2, dan 7 memiliki jarak 2 dari node awal, dan node 6 memiliki jarak 3 dari node awal.
