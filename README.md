# Pertemuan 06: Nested Loop Python

**Mata Kuliah:** Algoritma dan Pemrograman
**Materi:** Nested Loop, Pola, Akumulasi, dan Pencacahan

**Nama:** Farid Ardiansah
**NIM:** 2225250125
**Kelas:** 3E

## 1. Tujuan

Tujuan praktikum ini adalah:

* Memahami penggunaan nested loop atau perulangan bersarang dalam Python.
* Membuat tabel perkalian menggunakan nested loop.
* Menghitung jumlah seluruh hasil perkalian.
* Menghitung banyaknya hasil perkalian yang genap.
* Menghitung jumlah hasil perkalian pada setiap baris.
* Memvalidasi input agar nilai `n` merupakan bilangan bulat positif.

## 2. Cara Menjalankan Program

Buka terminal pada folder proyek, kemudian jalankan perintah berikut:

```bash
python3 tugas/tabel_perkalian_dan_statistik.py
```

Masukkan bilangan bulat positif ketika program meminta input `n`. Jika nilai `n` kurang dari atau sama dengan nol, program akan meminta pengguna memasukkan nilai kembali.

## 3. Algoritma Tugas 3

Program membuat tabel perkalian berukuran `n × n` dan menghitung statistik hasil perkalian.

Peran setiap bagian algoritma:

1. **Loop luar (`for i`)**
   Mengatur baris tabel perkalian dari 1 sampai `n`.

2. **Loop dalam (`for j`)**
   Mengatur kolom tabel perkalian dari 1 sampai `n` pada setiap baris.

3. **Akumulator (`total_baris` dan `total_semua`)**
   `total_baris` menjumlahkan hasil perkalian dalam satu baris, sedangkan `total_semua` menjumlahkan seluruh hasil perkalian.

4. **Counter (`count_genap`)**
   Menghitung banyaknya hasil perkalian yang genap menggunakan kondisi `hasil % 2 == 0`.

5. **Validasi input (`while`)**
   Memastikan nilai `n` lebih besar dari nol sebelum tabel perkalian dibuat.

## 4. Hasil Pengujian

| Input `n` | Hasil yang Diharapkan       | Keluaran Aktual             | Status   |
| --------- | --------------------------- | --------------------------- | -------- |
| 1         | Total = 1, hasil genap = 0  | Total = 1, hasil genap = 0  | Berhasil |
| 2         | Total = 9, hasil genap = 3  | Total = 9, hasil genap = 3  | Berhasil |
| 3         | Total = 36, hasil genap = 5 | Total = 36, hasil genap = 5 | Berhasil |

Catatan: Jalankan program untuk memastikan keluaran aktual sesuai dengan hasil yang diharapkan.

## 5. Analisis Efisiensi

Loop luar berjalan sebanyak `n` kali. Untuk setiap iterasi loop luar, loop dalam juga berjalan sebanyak `n` kali.

Jadi, badan loop dalam berjalan sebanyak:

**n × n = n² kali**

Contoh:

* `n = 1`: 1 kali.
* `n = 2`: 4 kali.
* `n = 3`: 9 kali.
* `n = 5`: 25 kali.

Kompleksitas waktu program adalah **O(n²)** karena jumlah iterasi bergantung pada kuadrat nilai `n`.

## 6. Refleksi

Salah satu kesalahan yang dapat terjadi saat menggunakan nested loop adalah kesalahan indentasi. Jika perintah tidak diletakkan pada tingkat indentasi yang benar, program dapat mengalami kesalahan atau menghasilkan keluaran yang tidak sesuai.

Cara memperbaikinya adalah memastikan loop dalam berada di dalam loop luar. Perintah untuk menampilkan jumlah baris harus berada di luar loop dalam, tetapi tetap di dalam loop luar.

Selain itu, variabel `total_baris` harus diatur kembali menjadi nol pada awal setiap baris agar hasil penjumlahan tidak tercampur dengan baris sebelumnya.

## 7. Kesimpulan

Nested loop dapat digunakan untuk membuat tabel perkalian berukuran `n × n`. Akumulator digunakan untuk menghitung jumlah setiap baris dan total keseluruhan, sedangkan counter digunakan untuk menghitung banyaknya hasil perkalian genap. Validasi input memastikan program hanya memproses nilai `n` yang positif.
