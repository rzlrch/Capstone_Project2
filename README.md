Capstone Project Module 2


Sebuah Supermarket, ingin merekrut data scientist untuk memecahkan permasalahan selling dan marketing. Supermarket ini sudah memiliki banyak customer tetapi hanya sebagian saja yang sering berbelanja kembali.

Data Cleansing
Secara umum, kita bisa melihat bahwa:

Dataset Supermarket Customers memiliki 29 kolom dan 2.240 baris.
Kolom ID memiliki error input '\n', akan kita perbaiki.
Kolom Income memiliki data kosong sebanyak 24. Data kosong pada kolom tersebut diwakili dengan data NaN.
Pada Kolom Income terdapat anomali inputan yang dimana nilai maksimal dari data Income adalah 666.666, kemungkinan ini adalah kesalahan input data jadi akan kita hapus
Kolom Z_CostContact dan Z_Revenue tidak ada di penjelasan pdf dan hanya terdapat 1 value saja sehingga kita asumsikan kedua kolom tersebut tidak digunakan sehingga bisa dihapus saja
Kolom Education penulisan 2n Cycle kita ubah menjadi Master
Kolom Marital Status, terdapat Alone, Absurd, dan YOLO yang akan kita gabungkan menjadi Single dan status Together akan kita ubah menjadi Married. Sehingga hasil akhir dari kolom Martial hanya ada 4 opsi yaitu : Single, Married, Divorced, Widow
Kolom Year_Birth ada 3 inputan berisi 1893,1899,1900. Dimana artinya kemungkinan ada kesalahan input saat pendaftaran customer. Hal ini akan kita lihat lagi kedepannya akankah berpengaruh terhadap data yang kita olah (opsional)
###Penambahan 3 kolom Baru :

Recency_Group yang isinya pengelompokan dari Recency per 10 hari
Total_Promotion yang diikuti oleh customer, isinya penjumlahan dari AcceptedCmp1 sampai AcceptedCmp5 dan Response.
Ikut_Promo untuk mempermudah pengelompokan customer yang pernah ikut promo dan yang tidak pernah ikut promo

Data Analysis
Link Tableau Dashboard : https://public.tableau.com/app/profile/muhammad.khairulrizal.rachmatullah/viz/MKhairulrizalR_CapstoneProject2/CapstoneProjectDash_?publish=yes

Kesimpulan dan Rekomendasi
Dari analisis yang telah dilakukan, kita bisa membuat kesimpulan untuk menaikan angka Recency Customer :

Dari 2,215 data customer yang kita miliki, hanya 685 customer saja yang kembali berbelanja di supermarket dalam 30 hari terakir. (asumsi 30 hari karena biasanya dalam sebulan setidaknya customer berbelanja di supermarket 1x (belanja bulanan))
Ditemukan seiring banyaknya customer yang mengikuti promo campaign, maka biasanya customer tersebut semakin sering berbelanja dalam waktu dekat.
Customer dengan Marital_Status Married memiliki populasi terbanyak disusul oleh Single, Divorced, dan yang terakir Widow
Customer dengan Education Graduation memiliki populasi terbanyak disusul oleh Master, PhD, dan yang terakir Basic. Tetapi kolom Education tidak terlalu berpengaruh terhadap custome yang pernah ikut promo campaign atau tidak.
##Rekomendasi

Semakin banyaknya customer yang ikut promo campaign, maka semakin sering juga customer tersebut berbelanja di supermarket. Sehingga untuk menaikan frekuensi customer berbelanja disupermarket kita bisa fokus dengan promo campaign terlebih dahulu.
Customer dengan Marital_Status Married memiliki populasi terbanyak dan juga paling banyak yang belum pernah mengikuti promo campaign. Kita bisa fokus di customer yang memiliki Marital_Status Married.
Customer Marital_Status Married mereka memiliki beberapa favorit produk yang secara proporsi paling banyak di beli oleh Customer dengan status Married. Produk tersebut adalah MntWines dan MntFish.
Sehingga untuk menaikan frekuensi customer belanja di supermarket, kita bisa fokus kepada jumlah customer yang mengikuti promo. Kita fokus ke customer yang memiliki kuantitas dengan Marital_Status terbanyak yaitu Married dan favorit produk mereka adalah MntWines dan MntFish.

Rekomendasi finalnya kita bisa menaikan jumlah frekuensi belanja customer dengan fokus terhadap promo campaign khususnya ditujukan kepada customer dengan Marital Status Married yang memiliki populasi terbanyak dan favorit produk mereka MntWines dan MntFish. Diharapkan analisis ini bisa membantu supermarket membuat promo campaign yang lebih efisien dan terarah agar frekuensi belanja customer meningkat.
