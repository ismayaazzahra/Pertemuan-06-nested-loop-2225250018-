# Pertemuan 06 Nested Loop Python

## Identitas

Nama: ISMAYA CATUR DEWI AZZAHRA
NIM: 2225250018
Kelas: 3A

## Tujuan

Menggunakan nested loop, pola, akumulasi, dan pencacahan untuk membentuk tabel perkalian n x n, menghitung jumlah setiap baris, jumlah seluruh hasil perkalian, dan banyaknya hasil yang genap.

## Cara Menjalankan

python3 tugas/tabel_perkalian_dan_statistik.py

Di Windows gunakan python. Masukkan bilangan bulat positif n. Jika n <= 0, program meminta input lagi sampai valid.

## Algoritma Tugas 3

Loop luar (i = 1..n): mengatur baris. Di awal tiap baris total_baris direset ke 0.
Loop dalam (j = 1..n): mengatur kolom. Pada tiap pasangan dihitung hasil = i * j lalu dicetak.
Akumulator total_baris: jumlah per baris, diinisialisasi di dalam loop luar sebelum loop dalam.
Akumulator total_semua: jumlah seluruh hasil, diinisialisasi sekali sebelum kedua loop.
Counter count_genap: bertambah 1 hanya jika hasil % 2 == 0.
while: validasi input n.

Langkah:

1. Baca n, ulangi selama n <= 0.
2. Set total_semua = 0 dan count_genap = 0.
3. Ulangi i dari 1 sampai n.
4. Set total_baris = 0.
5. Ulangi j dari 1 sampai n.
6. Hitung hasil = i * j dan cetak.
7. Tambahkan hasil ke total_baris dan total_semua.
8. Jika hasil genap, tambah count_genap.
9. Setelah loop dalam, cetak jumlah baris.
10. Setelah kedua loop, cetak total keseluruhan dan banyak hasil genap.

## Hasil Pengujian

Input n	Jumlah pasangan	Total semua (diharapkan)	Genap (diharapkan)	Total semua (aktual)	Genap (aktual)	Status
1	1	1	0	1	0	Lulus
2	4	9	3	9	3	Lulus
3	9	36	5	36	5	Lulus
0 lalu 2	4	9	3	9	3	Lulus

Contoh keluaran n = 3:

Tabel Perkalian dan Statistik
n: 3
   1   2   3 | jumlah baris = 6
   2   4   6 | jumlah baris = 12
   3   6   9 | jumlah baris = 18
Total seluruh hasil = 36
Banyak hasil genap = 5

Tracing manual n = 2:

i	j	hasil	total_baris	total_semua	count_genap
1	1	1	1	1	0
1	2	2	3	3	1
2	1	2	2 (direset)	5	2
2	2	4	6	9	3

## Analisis Efisiensi

Loop luar berjalan n kali dan untuk setiap iterasinya loop dalam berjalan n kali, sehingga badan loop dalam dieksekusi n x n = n^2 kali (begitu juga hasil = i * j). Semua iterasi diperlukan karena tabel harus menampilkan n x n hasil, dan tidak ada perhitungan berulang yang tidak perlu. Bagian yang paling banyak melakukan operasi saat n membesar adalah badan loop dalam.

## Refleksi

Kesalahan yang saya temukan: pada percobaan awal total_baris = 0 saya taruh sebelum loop luar, sehingga jumlah baris 2 menjadi 9 (terbawa dari baris 1), padahal seharusnya 6. Saya menemukannya dari tracing manual n = 2. Perbaikannya: memindahkan total_baris = 0 ke dalam loop luar sebelum loop dalam.