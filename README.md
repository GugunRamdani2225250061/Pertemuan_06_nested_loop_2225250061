# Pertemuan 06 Nested Loop Python

- Nama: Gugun Ramdani  
- NIM: 2225250061  
- Kelas: 3A

## Tujuan

Menggunakan nested loop, pola, akumulasi, dan pencacahan.

## Struktur Folder

Pertemuan_06_nested_loop_2225250061/
# latihan/
- 01_pasangan_indeks.py
- 02_pola_segitiga.py
- 03_jumlah_per_baris.py
- 04_hitung_pasangan.py
# tugas/
- tabel_perkalian_dan_statistik.py
# .gitignore
# kuis formatif_pertemuan 06.docx
# README.md

## Cara Menjalankan

Latihan 1:
```bash
python3 latihan/01_pasangan_indeks.py
```
Latihan 2:
```bash
python3 latihan/02_pola_segitiga.py
```
Latihan 3:
```bash
python3 latihan/03_jumlah_per_baris.py
```
Latihan 4:
```bash
python3 latihan/04_hitung_pasangan.py
```
Tugas 3:
```bash
python3 tugas/tabel_perkalian_dan_statistik.py
```
## Algoritma Tugas 3

1. Meminta input bilangan positif `n`.
2. Jika `n <= 0`, program meminta input kembali.
3. Membuat variabel `total_semua = 0` untuk menyimpan jumlah seluruh hasil perkalian.
4. Membuat variabel `count_genap = 0` untuk menghitung banyak hasil perkalian yang genap.
5. Loop luar menggunakan `i` dari 1 sampai `n` untuk menentukan baris.
6. Pada setiap baris, `total_baris` diatur kembali menjadi 0.
7. Loop dalam menggunakan `j` dari 1 sampai `n` untuk menentukan kolom.
8. Menghitung `hasil = i * j`.
9. Menambahkan `hasil` ke `total_baris`.
10. Menambahkan `hasil` ke `total_semua`.
11. Jika `hasil` habis dibagi 2, `count_genap` ditambah 1.
12. Setelah loop dalam selesai, program menampilkan jumlah pada baris tersebut.
13. Setelah semua baris selesai, program menampilkan total seluruh hasil dan banyak hasil genap.

### Peran Loop

- **Loop luar:** mengatur baris tabel perkalian.
- **Loop dalam:** mengatur kolom dan menghitung setiap perkalian.
- **Akumulator:** `total_baris` dan `total_semua`.
- **Counter:** `count_genap`.

## Hasil Pengujian

| Input | Total Seluruh Hasil | Banyak Hasil Genap | Status |
|---|---:|---:|---|
| n = 1 | 1 | 0 | Berhasil |
| n = 2 | 9 | 3 | Berhasil |
| n = 3 | 36 | 5 | Berhasil |

## Analisis Efisiensi

Untuk input `n`, loop luar berjalan sebanyak `n` kali.

Pada setiap satu kali loop luar, loop dalam berjalan sebanyak `n` kali.

Jadi badan loop dalam dijalankan sebanyak:
```text
n × n = n²
```
Dengan demikian, kompleksitas waktu program adalah:
```text
O(n²)
```
## Refleksi

Kesalahan yang dapat terjadi ketika menggunakan nested loop adalah meletakkan variabel `total_baris` di luar loop utama. Jika hal tersebut dilakukan, nilai jumlah baris sebelumnya akan ikut terbawa ke baris berikutnya.

Cara memperbaikinya adalah dengan menginisialisasi kembali:
```python
total_baris = 0
```
di dalam loop luar sebelum loop dalam dijalankan.
Dengan demikian, setiap baris memiliki perhitungan jumlah yang dimulai dari nol.

## Kesimpulan

Pada pertemuan ini saya mempelajari penggunaan nested loop pada Python. Nested loop digunakan ketika sebuah perulangan berada di dalam perulangan lainnya. Selain itu, saya mempelajari penggunaan pola, akumulator untuk menjumlahkan nilai, serta counter untuk menghitung banyaknya kejadian yang memenuhi kondisi tertentu.
