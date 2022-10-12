﻿# Praktikum Probabilitas dan Statistika Modul 1
Nama: Aryan Shafa Wardana\
NRP: 5025211031
 
## Nomor 1
Seorang penyurvei secara acak memilih orang-orang di jalan sampai dia bertemu dengan
seseorang yang menghadiri acara vaksinasi sebelumnya.
* ### a. Berapa peluang penyurvei bertemu x = 3 orang yang tidak menghadiri acara vaksinasi sebelum keberhasilan pertama ketika p = 0,20 dari populasi menghadiri acara vaksinasi ? (distribusi Geometrik)
  Pada soal ini diberikan `X = 3` yang merupakan jumlah orang yang tidak menghadiri acara vaksinasi dan `p = 0.20` yang merupakan peluang dari populasi menghadiri acara vaksinasi. Soal ini dapat diselesaikan dengan memanfaatkan fungsi `dgeom(x, prob)` yang menghitung probabilitas sejumlah kegagalan `x` sebelum keberhasilan pertama jika setiap percobaan memiliki peluang `prob`. Implementasi sebagai berikut.
  ![1a](https://user-images.githubusercontent.com/115603634/195280279-7bc04f84-c96d-4ab7-96c2-a03828f740c7.PNG)
  Fungsi cat akan mencetak hasil perhitungan dari `dgeom(x, p)` yaitu didapatkan hasil `Peluang = 0.1024`.
* ### b. Mean Distribusi Geometrik dengan 10000 data random , prob = 0,20 dimana distribusi geometrik acak tersebut X = 3 ( distribusi geometrik acak () == 3 )
  Pada soal ini diberikan data random `n = 10000`, `prob = 0.20`, dan `X = 3`. Soal ini dapat diselesaikan menggunakan fungsi `rgeom(n, p)` untuk menghasilkan data-data random yang menyatakan jumlah kegagalan sebelum keberhasilan dan fungsi `mean(data)` untuk menghitung rata-rata. Implementasi sebagai berikut
  ![1b](https://user-images.githubusercontent.com/115603634/195281586-a88450b7-060e-4a66-bda1-e623b5d3e748.PNG)
  Hasil yang didapatkan adalah `Mean = 0.1052` dan `Mean = 0.1011` pada percobaan pertama dan kedua.
* ### c. Bandingkan Hasil poin a dan b , apa kesimpulan yang bisa didapatkan?
  Pada poin A, nilai peluang selalu tetap, sedangkan pada poin B, mean dapat berubah-ubah karena menggunakan data-data yang random. Jadi, dapat disimpulkan bahwa nilai peluang pada poin A selalu tetap sedangkan mean pada poin B selalu berubah.
* ### d. Histogram Distribusi Geometrik , Peluang X = 3 gagal Sebelum Sukses Pertama
  Pada soal ini diminta untuk membuat histogram distribusi geometrik. Histogram dapat dibuat dengan fungsi `hist()`. Dengan memasukkan data hasil `rgeom(n, p)` dan memberi nama, warna kotak, dan label pada sumbu X maka didapat hasil sebagai berikut.
  ```
  hist(dist,
    main = "Histogram Distribusi Geometrik",
    col = "#a3c6f7",
    xlab = "X")
  ```
  ![image](https://user-images.githubusercontent.com/115603634/195283427-cf910e5d-2861-46e9-a45a-a6a0ae1356df.png)
 * ### e. Nilai Rataan (μ) dan Varian (σ²) dari Distribusi Geometrik.
   Pada soal ini diminta rataan dan varian dari distribusi geometrik. Rataan memiliki rumus `μ = 1 - p` dan varian memiliki rumus `σ^2 = (1 - p) / p^2`. Implementasi sebagai berikut.
   ![image](https://user-images.githubusercontent.com/115603634/195284684-51016a42-cd9e-4207-a7ef-7bc02a80ce15.png)
  Hasil yang didapatkan adalah `Rataan = 5` dan `Varian = 20`
