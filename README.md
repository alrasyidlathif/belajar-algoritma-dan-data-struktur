# belajar-algoritma-dan-data-struktur

Kompleksitas atau big-O pada array untuk perintah-perintah dasar seperti read, search, insert, dan delete.

## Definisi:
- Big-O adalah ukuran yang mengatakan berapa banyak step yang diperlukan komputer untuk melakukan suatu pekerjaan.
- array adalah sebuah struktur data yang memungkinkan kita menyimpan data, dianalogikan dalam bentuk seperti rak sepatu.
Dimana satu ruang hanya dapat digunakan untuk menyimpan 1 item, dan item pertama yang kita simpan akan disimpan dalam rak index ke-0, dst.

## Pembahasan:
- [x] Perintah read: perintah read memiliki nilai big-O 1, karena saat read komputer sudah tau index dari item yang mau kita read.
- [x] Perintah search: perintah search memiliki nilai big-O N, karena saat search komputer akan mengecek 1-per-1 dari semua item yang ada pada array.
Jika item yang dicari ada pada array index terakhir maka akan butuh N, panjang array, step untuk melakukan pencarian tersebut.
- [x] Perintah insert: perintah insert memiliki nilai big-O N+1, karena saat insert item pada array index ke-0 komputer harus menggeser item-item yang ada terlebih dahulu ke kanan satu-per-satu dimulai dari item yang paling kanan. Kemudian setelah index ke-0 kosong, item yang baru bisa diinsert.
- [x] Perintah delete: perintah delete memiliki nilai big-O N, karena saat delete item pada array index ke-0, setelah menghapus item komputer harus menggeser semua sisa item satu-per-satu ke kiri, untuk mengisi ruang kosong yang ditinggalkan oleh item yang dihapus.

## Definisi:
- Struktur data lain: ordered array, adalah array yang item-itemnya diurutkan, dari kecil ke besar atau sebaliknya.
Saat hendak melakukan insert ke ordered array, komputer harus mengecek dulu item mana yang lebih besar dari item baru, maka item baru harus ditempatkan tepat sebelum item tersebut.
Insert pada ordered array memiliki kompleksitas yang lebih tinggi dibandingkan pada array biasa, karena sebelum melakukan insert harus dilakukan search dan penggeseran item terlebih dahulu. Terlepas dari kekurangan tersebut, ordered array mmiliki banyak keuntungan saat search dibandingkan dengan array biasa, sebagai berikut.

## Pembahasan:
- [x] Perintah search pada ordered array: memiliki banyak keuntungan dibandingkan pada array biasa. Pada array biasa search dilakukan sampai pada semua item hingga ketemu, sedangkan pada ordered array search dilakukan hingga pada item yang lebih besar daripada item yang dicari, jika tidak ketemu, ya sudah, abaikan sisa item karena pasti juga tidak ada.
- [x] Algoritma pencarian pada ordered array, struktur data pada ordered array memungkinkan adanya algoritma pencarian yang lain. Algoritma pencarian biasa yang sudah dibahas, yang mengecek satu-per-satu item dari awal, disebut dengan linear search. Linear search memiliki nilai big-O N artinya setiap bertambahnya 1 data, tingkat kompleksitas akan naik satu.
- [x] Algoritma yang lain adalah binary search, binary search akan mencari langsung mulai dari tengah, jika item sebelah kiri lebih besar dari item yang dicari maka binary search akan menuju ke bagian kiri dan melakukan pembagian lagi. Sebaliknya jika item sebelah kiri masih lebih kecil maka binary search akan melihat item sebelah kanan, jika item tersebut juga lebih kecil, maka binary search akan menuju ke bagian kanan dan melakukan pembagian lagi. Namun, jika item sebelah kiri lebih kecil dan item sebelah kanan lebih besar, maka dapat dipastikan item yang dicari tidak ditemukan. Binary search memiliki nilai big-O log N, karena setiap data naik "dua kali lipat", tingkat kompleksitas binary search hanya naik satu.

