MVC merupakan kependekan dari Model View Controller dan merupakan sebuah pola yang sudah teruji dalam pengembangan aplikasi. Awalnya, MVC digunakan untuk pengembangan GUI desktop, tapi kini telah banyak diadopsi oleh framework-framework aplikasi berbasis web. Jika kita mengembangkan aplikasi tanpa pola MVC, kita berkecenderungan untuk mencampur adukkan kode logika kita dengan kode tampilan serta kode untuk mengambil data ke database. Benar? Nah dengan MVC tidak begitu, karena dengan pola MVC, kita membagi komponen aplikasi kita menjadi 3 bagian yang terpisah namun saling berkaitan, yaitu Model, View dan Controller. Apa guna masing-masing komponen tersebut?

Model
Merupakan komponen dalam aplikasi kita yang bertanggungjawab mengelola akses langsung dengan sumber data dan logika pengelolaan data tersebut. Gampangnya, model berhubungan erat dengan database yang nanti akan digunakan.
View
Merupakan komponen dalam aplikasi kita yang bertanggungjawab untuk membuat tampilan / interface untuk pengguna. Sumber data didapat dari model yang didapatkan melalui controller. Tidak berinteraksi langsung dengan database. View juga menangkap interaksi dari pengguna yang akan diteruskan ke aplikasi.
Controller
Merupakan komponen dalam aplikasi kita yang bertanggungjawab untuk menerima input dan memberikan output, atau dalam dunia web kita lebih mengenal dengan istilah request dan response. Controller bertugas untuk menerima request, kemudian memprosesnya dengan memberikan response baik berupa data atau view berisi data dari model.

Peletakan MVC pada struktur folder di projek Laravel.
Berikut merupakan gambaran MVC pada Laravel.


Penjelasan:
1. - User mengakses website melalui route tertentu.
2. - Route tersebut akan mengarah / merujuk kepada controller action.
3. - Apabila terdapat data yang ingin diakses, maka controller akan menuju model. Bila tidak ada, controller langsung mengembalikan sebuah view tanpa data (langsung ke poin 5).
4. - Model ini akan berinteraksi dengan database untuk mendapatkan sebuah data, menyimpan, merubah, maupun menghapus data.
5. - Setelah berhasil mendapatkan data dari model, controller akan mengembalikan sebuah view beserta data jika ada.
6. - Proses terakhir dimana view dilihat oleh user.