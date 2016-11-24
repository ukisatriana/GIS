Pembahsan kali ini untuk melanjutkan dari pembahasan sebelumnya tentang manipulasi data geospasial. kali ini akan membahas tentang bagaimana cara membuat dan mengubah data geospasial menggunakan library pyshp


A. Cara Membuat Data Geospasial

Untuk membuat data geospasial, menggunakan library pyshp, dan untuk membuat data geospasial diperlukan file namafile.shp beserta namafile.dbf.

Adapun tahapannya sebagai berikut:

a. Import shapefile

b. Instanisasu writer method

    Sf = shapefile.Writer(param)

    Dimana param adalah pilih shapetype:

- shapeType = 1

- shapeType = 3

- shapeType = 5

c. Sama seperti read, kita lakukan method dbf dan shp.

 Shapefile (shp)

 Untuk menambahkan record tergantung dengan tipe ESRI-nya.

1. sf.point (x,y)

2. sf.line = (parts:[[x.y],[z.w],...])

3. sf.poly = (parts:[[x.y],z.w],...])

 Databasefile (dbf)

 Tahapannya adalah sebagai berikut:

a. Membuat atribut terlebih dahulu kemudian menambahkan record nya.

Contoh:

 sf.field('Nama Field','C','50')

 Dimana C adalah Character, dan 50 adalah length. Dalam arti nama atribut, nama field dengan panjang 50 karakter.

b. Tambahkan recird dibawah ini

 sf.record('Batam')

 sf. record('Batam','Sekupang')

c. Setelah selesai maka simpan, dengan perintah

 sf.save('namafile.shp')

B.Mengubah  Data Geospasial

Adapun dalam editing data geospasial hampir menyerupai langkah-langkah membuat data geospasial yang membedakannya adalah;

sf = shapefile.Writer(param)

diubah dengan

sf = shapefile.Editor(param)

dimana letak param adalah nama letak file.

Adapun operasi dalam editing pada shp dan dbf sama saja.



DELETE DATA GEOSPASIAL


Sf.delete(0)

a.shapes()[0].points [(10,0,10,0)]

sf.points [16,10,0,0]

sf.record(‘padang’)

sf.saver(‘wr.shp’)


Penutup

Kesimpulan

jadi pada pertemuan 5 ini , kita dapat mengetahui bagaimana cara membuat, mengedit, dan menghapus (CRUD) Data geospasial


Saran

Lebih banyak di pelajari lebih dalam lagi, dengan mencari referensi referensi di internet maupun di buku.


