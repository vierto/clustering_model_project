# Project Clustering Model (MySkill.id) by Vendly

The algorithms used for clustering the data are K-Means and K-Medoids.

## Problem Statement

FundFusion adalah sebuah institusi bank yang ingin mengembangkan upaya pelayanan marketingnya terhadap nasabah <i>existing</i> maupun nasabah baru, tetapi FundFusion belum memiliki strategi yang tepat untuk menawarkan jenis produk yang sesuai dengan segmen calon nasabah yang akan direkrut. Tujuan dari bisnis strategi yang baru adalah agar dapat meningkatkan nasabah baru dengan cara menawarkan produk yang tepat sesuai dengan kriteria calon nasabah yang akan dihubungi. Analisa yang dilakukan yaitu dengan membuat sebuah model <i>Clustering</i> untuk mengetahui kepemilikan produk berdasarkan demografi nasabah yang saat ini sudah menggunakan layanan FundFusion.

## Objective

Membuat sebuah model <i>clustering</i> untuk mengetahui kepemilikan produk berdasarkan demografi nasabah yang saat ini sudah menggunakan layanan FundFusion dengan <i>Silhouette Score</i> > 0.7

## Variabel yang Tersedia

Dari dataset yang dimiliki terdapat beberapa data yang tersedia:
1. <b>GCIF:</b> Unique identifier nasabah
2. <b>Area:</b> Lokasi nasabah (Jakarta, Bogor, Bandung, Surabaya, Jogja, Solo)
3. <b>Jalur_Pembukaan:</b> Touch points nasabah membuka produk -> cabang, telemarketing, aplikasi digital, internet banking
4. <b>Vintage:</b> Durasi menjadi nasabah (sejak membuka akun)
5. <b>Usia:</b> Usia nasabah
6. <b>Jenis_Kelamin:</b> Laki-laki (1) & perempuan (0)
7. <b>Status_Perkawinan:</b> Belum menikah (0), menikah (1), cerai (2), janda/duda (3)
8. <b>Jumlah_anak:</b> Jumlah anak nasabah (numerik)
9. <b>Pendidikan:</b> Status pendidikan terakhir -> tidak memiliki pendidikan formal (0), SD (1), SMP (2), SMA (3), Sarjana (4), Magister (5), Doktor (6)
10. <b>Produk_Tabungan:</b> Status kepemilikan produk (Yes/1, No/0)
11. <b>Produk_Deposito:</b> Status kepemilikan produk (Yes/1, No/0)
12. <b>Produk_Kartu_Kredit:</b> Status kepemilikan produk (Yes/1, No/0)
13. <b>Produk_Kredit_Rumah:</b> Status kepemilikan produk (Yes/1, No/0)
14. <b>Produk_Kredit_Kendaraan:</b> Status kepemilikan produk (Yes/1, No/0)
15. <b>Produk_Kredit_Dana_Tunai:</b> Status kepemilikan produk (Yes/1, No/0)
16. <b>Total_Kepemilikan_Produk:</b> Jumlah produk yang dimiliki (penjumlahan dari produk2)
17. <b>Pendapatan_Tahunan:</b> Rata-rata pendapatan dalam setahun
18. <b>Total_Relationship_Balance:</b> Total asset nasabah dalam cutooff bulan observasi

## Eksperimen

Point of View:
1. Dikelompokkan berdasarkan demografis untuk dicari <i>pattern</i> kepemilikan produk
2. Dikelompokkan berdasarkan kepemilikan produk untuk dicari <i>pattern</i> berdasarkan demografisnya

## Kesimpulan

Dari semua model, rata-rata memiliki <i>silhouette score</i> di bawah 70% yaitu sekitar 30% hingga 50%. Maka dari itu berdasarkan data <i>silhouette score</i>, FundFusion masih belum memiliki strategi yang tepat untuk menawarkan jenis produk yang sesuai dengan segmen calon nasabah yang akan direkrut. Sehingga bisa disampaikan bahwa dalam iterasi pembangunan model ini masih belum mencapai <i>objective</i> yang diinginkan. Solusi pengembangan selanjutnya yang dapat dilakukan diantaranya yaitu bisa dengan menambahkan variabel seperti balance per <i>product</i> yang tersedia dalam FundFusion agar data yang tersedia dapat semakin jelas dan bisa diketahui nasabah lebih banyak menyimpan dananya dimana, seperti di tabungan atau deposito, atau hanya menggunakan untuk kredit, bisa saja nasabah memiliki pinjaman yang banyak tetapi tabungannya kecil. Maka dari itu strategi yang dapat dilakukan selanjutnya yaitu menambahkan data agar train model menggunakan algoritma K-Means dan juga K-Medoids bisa memiliki <i>silhouette score</i> lebih baik.
