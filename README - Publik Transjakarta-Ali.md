# Publik Transjakarta

**Latar Belakang**

Transjakarta adalah mode transportasi berbasis Bus Rapid Transit (BRT) dan non-BRT yang sudah beroperasi sejak tahun 2004 di Jakarta. Transjakarta merupakan wujud dari pengelolaan transportasi publik di Jakarta yang terpadu dan bebas macet. Tidak hanya bertujuan untuk mengurai kemacetan, kemudahan akses Transjakarta sekaligus menjadikannya sebagai transportasi publik pilihan warga Jakarta.

Tidak hanya melayani perjalanan di dalam Kota Jakarta, Transjakarta kini sudah memiliki trayek hingga ke wilayah megapolitan Bodetabek (Bogor, Depok, Tangerang, dan Bekasi). Transjakarta memiliki jam operasional 24 Jam dengan jumlah 273 halte yang tersebar di 13 koridor. Jalur Transjakarta terbentang sepanjang 251.2km dan memiliki 260 halte yang tersebar di seluruh wilayah Jakarta dan sekitarnya.

Selain jalur khusus Transjakarta untuk layanan BRT (Bus Way), Transjakarta juga menggunakan jalur jalan biasa. Selain beberapa koridor dengan rute di atas, Transjakarta juga menyediakan rute tambahan di beberapa koridor.

Perusahaan ini melakukan pendataan tentang transaksi pelanggan yang melakukan perjalanan transportasi dengan bus. Perusahaan ingin mengetahui karakteristik pelanggan mana yang menaiki transportasi bus.

**Rumusan Masalah**

Dalam konteks ini, rumusan masalahnya adalah :

1. Perusahaan ingin mengetahui pelanggan mana saja yang memakai layanan transportasi publik transjakarta. Informasi ini akan membantu perusahaan untuk mengetahui kalangan umur, lokasi ramai pengunjung dan lain-lain yang relevan.
2. Bagaimana karakteristik pelanggan yang memakai layanan transportasi publik transjakarta untuk mengetahui potensi paling tinggi serta jumlah penumpang yang padat untuk dijadikan tujuan dalam pengembangan transportasi, apakah diperlukannya penambahan armada atau tidak di jalur tertentu sehingga dapat mengoptimalkan pelayanan??

**Tujuan Masalah**

Sebagai data analyst, saya akan mencari tahu untuk jawabannya

1. Mengetahui potensi paling tinggi serta jumlah penumpang untuk mengetahui apakah diperlukan penambahan armada atau tidak di jalur tertentu untuk mengoptimalkan pelayanan?
2. Mengetahui kelompok umur mana saja yang menjadi penumpang bus transjakarta?
3. Mengetahui secara geografis, koridor mana yang sering banyak dikunjungi?


Info dataset Transjakarta:

| No. | Fitur | Deskripsi | Detail |
|-|-|-|-|
| 1. | **transID** | Nomor ID transaksi unik untuk setiap transaksi pelanggan yang memakai layanan bus. | |
| 2. | **payCardID** | Identifikasi unik AirBNB untuk setiap listing. | |
| 3. | **payCardBank** | Nama atau metode pembayaran dari pelanggan. | |
| 4. | **payCardName** | Nama pelanggan yang tertera di kartu. | |
| 5. | **payCardSex** | Jenis kelamin pelanggan yang tertera di kartu. | |
| 6. | **payCardBirthDate** | Tanggal lahir pelanggan yang tertera di kartu. | |
| 7. | **corridorID** | Koridor ID / rute ID sebagai kunci untuk rute transportasi. | |
| 8. | **corridorName** |  Nama koridor / nama rute yang berisi tempat start dan finish untuk setiap rute. | |
| 9. | **direction** | Kode perjalanan bus, 0 untuk pergi, 1 untuk pulang, sebagai arah ke rute perjalanan. | Ketika pelanggan mau berangkat memakai bus, maka arah perjalanan bernilai 0, dan ketika pelanggan mau pulang naik bus, maka arah perjalanan akan bernilai 1. |
| 10. | **tapInStops** | Nomor ID untuk tap in (masuk) untuk identifikasi nama pemberhentian bus saat pelanggan menekan tombol tap in dan masuk ke bus. | |
| 11. | **tapInStopsName** | Nama lokasi halte untuk pelanggan yang menekan tombol tap in dan masuk ke bus. | |
| 12. | **tapInStopsLat** | Koordinat latitude dari halte saat pelanggan masuk ke bus. | Misalnya saat pelanggan berangkat dari Cibubur ke Ciputat, maka koordinat lokasi Cibubur akan menjadi latitude dari tapInStopsLat. |
| 13. | **tapInStopsLon** | Koordinat latitude dari halte saat pelanggan masuk ke bus. | Misalnya saat pelanggan berangkat dari Cibubur ke Ciputat, maka koordinat longitude lokasi Cibubur akan menjadi longitude dari tapInStopsLon. |
| 14. | **stopStartSeq** | Urutan pemberhentian saat bus pergi, yaitu pemberhentian pertama, pemberhentian kedua, dll yang berkaitan dengan arah. | |
| 15. | **tapInTime** | Waktu saat pelanggan menekan tombol tap in, berisi tanggal dan waktu. | |
| 16. | **tapOutStops** | Nomor ID untuk tap out (keluar) untuk identifikasi nama pemberhentian bus saat pelanggan menekan tombol tap out dan keluar dari bus. | |
| 17. | **tapOutStopsName** | Nama lokasi halte saat pelanggan menekan tombol tap out dan keluar ke bus. | Misalnya saat pelanggan berangkat dari Cibubur ke Ciputat, maka halte atau koridor Cibubur akan menjadi nama dari tapOutStopsName. |
| 18. | **tapOutStopsLat** | Koordinat latitude dari halte saat pelanggan menekan tombol Tap Out dan keluar dari bus. | Misalnya saat pelanggan berangkat dari Cibubur ke Ciputat, maka koordinat lokasi Ciputat akan menjadi latitude dari tapOutStopsLat. |
| 19. | **tapOutStopsLon** | Koordinat longitude dari halte saat pelanggan menekan tombol Tap Out dan keluar dari bus. | Misalnya saat pelanggan berangkat dari Cibubur ke Ciputat, maka koordinat lokasi Ciputat akan menjadi longitude dari tapOutStopsLon. |
| 20. | **stopEndSeq** | Urutan pemberhentian saat bus berhenti, yaitu pemberhentian pertama, pemberhentian kedua, dll yang berkaitan dengan arah. | |
| 21. | **tapOutTime** | Waktu saat pelanggan keluar dan menekan tombol tap out, berisi tanggal dan waktu. | |
| 22. | **payAmount** | Jumlah pembayaran pelanggan. Ada yang gratis dan berbayar. | |


**Kesimpulan**

Berdasarkan analisis yang telah dilakukan, berikut adalah kesimpulan yang dapat diambil untuk mengidentifikasi karakteristik pelanggan berdasarkan umur:

1. Koridor 1T merupakan koridor yang paling banyak dikunjungi dengan 1930 transaksi, lalu diikuti dengan koridor Cibubur dan Ciputat selama bulan April di tahun 2023.
2. Nilai statistik sebesar 80.695 merujuk pada nilai statistik dalam uji Kruskal-Wallis, dan nilai p-value adalah nilai probabilitas yang menunjukkan signifikansi statistik dari perbedaan antara ketiga kelompok. Dalam kasus ini, nilai p-value adalah 2.159e-09, maka tingkat signifikansi sebesar 2.159e-09 lebih kecil dari 0.05, maka ada cukup bukti untuk menerima hipotesis nol, yang berarti tidak ada perbedaan yang signifikan antara ketiga kelompok dalam hal jumlah transaksi pelanggan.

**Rekomendasi**

1. Dalam hasil Uji Kruskal-Wallis, nilai p-value adalah 2.159e-09 yaitu gagal tolak H0 maka tidak dibutuhkan penambahan armada pada trayek koridor Cibubur dan Ciputat. Akan tetapi jika ingin menaikkan profit agar koridor Cibubur dan Ciputat menyamai profit koridor 1T, maka perlu diberi promosi.
2. Belum bisa memberikan rekomendasi lebih mendalam, karena analisis berdasarkan top 3 koridor name dan umur belum cukup untuk menjawab pertanyaan-pertanyaan pada pertanyaan masalah. Maka dari itu, seharusnya dilakukan analisis secara mendalam.


**Link To Tableau Public**

https://public.tableau.com/app/profile/moh.fauzi/viz/PublikTransjakarta-Project2/DashboardPublikTransjakarta?publish=yes