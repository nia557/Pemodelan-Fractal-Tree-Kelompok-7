content = """# Pemodelan Fractal Tree Menggunakan Algoritma Rekursif

## Informasi Proyek

**Mata Kuliah:** Matematika Diskrit  
**Program Studi:** Matematika  
**Kelompok:** 7  
**Bahasa Pemrograman:** MATLAB  

**Judul Proyek:**  
Pemodelan Fractal Tree Menggunakan Algoritma Rekursif

## Anggota Kelompok

1. Allya Vinice Jelita
2. Emeline Joan Sigalingging
3. Naila Fadila
4. Nia Fadila
5. Marhasil Marbun

## Deskripsi

Proyek ini membahas pemodelan Fractal Tree menggunakan algoritma rekursif sebagai penerapan konsep Matematika Diskrit. Fractal Tree merupakan bentuk yang menyerupai pohon dengan pola percabangan yang berulang. Setiap cabang dapat menghasilkan cabang baru dengan panjang yang semakin kecil sehingga membentuk pola yang menyerupai struktur fraktal.

Pada proyek ini, algoritma rekursif diterapkan melalui fungsi `fractalTree` yang memanggil dirinya sendiri untuk membentuk percabangan. Proses tersebut dilakukan sampai mencapai tingkat kedalaman yang telah ditentukan. Implementasi dan visualisasi model dilakukan menggunakan MATLAB.

## Tujuan

Proyek ini dilakukan untuk:

1. Menerapkan konsep rekursi dalam Matematika Diskrit.
2. Membentuk pola Fractal Tree menggunakan algoritma rekursif.
3. Mengetahui pengaruh tingkat kedalaman rekursi terhadap jumlah percabangan.
4. Mengimplementasikan algoritma rekursif menggunakan MATLAB.
5. Menampilkan hasil pemodelan Fractal Tree dalam bentuk visualisasi.

## Konsep Algoritma

Program menggunakan fungsi `fractalTree` sebagai fungsi rekursif. Pada setiap pemanggilan, program menentukan koordinat ujung batang, menggambar batang menggunakan `plot()`, mengurangi panjang cabang berdasarkan faktor `r`, membentuk cabang kiri dan kanan, kemudian memanggil kembali fungsi `fractalTree`.

Proses berhenti ketika nilai `depth` mencapai 0. Kondisi tersebut merupakan *base case* yang digunakan untuk menghentikan proses rekursif.

## Parameter Program

| Parameter | Nilai | Keterangan |
|---|---:|---|
| `L` | 100 | Panjang batang awal |
| `theta` | 90° | Sudut awal |
| `depth` | 1–5 | Kedalaman rekursi |
| `r` | 0,7 | Faktor pengecilan panjang cabang |
| `alpha` | 25° | Sudut percabangan |

## Model Matematis

Panjang cabang pada tingkat ke-`n` dapat dinyatakan dengan:

$$
L_n = L_0r^n
$$

dengan:

- `L₀` sebagai panjang batang awal;
- `r` sebagai faktor pengecilan;
- `n` sebagai tingkat percabangan.

Jumlah garis teoritis pada kedalaman `d` dinyatakan dengan:

$$
G(d) = 2^d - 1
$$

Berdasarkan persamaan tersebut, jumlah garis teoritis untuk setiap nilai kedalaman adalah:

| `depth` | Jumlah Garis |
|---:|---:|
| 1 | 1 |
| 2 | 3 |
| 3 | 7 |
| 4 | 15 |
| 5 | 31 |

Nilai `depth` yang semakin besar menghasilkan jumlah percabangan yang semakin banyak sehingga pola Fractal Tree menjadi semakin kompleks.

## Implementasi MATLAB

Program utama dibuat menggunakan MATLAB dengan parameter sebagai berikut:

```matlab
clc;
clear;
close all;

L = 100;
theta = 90;
depth = 5;
r = 0.7;
alpha = 25;

figure;
hold on;
axis equal;
grid on;

title('Pemodelan Fractal Tree Menggunakan Algoritma Rekursif');
xlabel('Sumbu X');
ylabel('Sumbu Y');

fractalTree(0,0,L,theta,depth,r,alpha);
```

Fungsi `fractalTree` digunakan untuk menghitung koordinat, menggambar batang, memperkecil panjang cabang, serta melakukan pemanggilan fungsi secara rekursif.

## Pengujian

Pengujian dilakukan dengan menggunakan nilai `depth` dari 1 sampai 5, sedangkan parameter lainnya dipertahankan.

| Pengujian | `depth` | Jumlah Garis Teoritis |
|---|---:|---:|
| 1 | 1 | 1 |
| 2 | 2 | 3 |
| 3 | 3 | 7 |
| 4 | 4 | 15 |
| 5 | 5 | 31 |

Pengujian dilakukan untuk melihat hubungan antara tingkat kedalaman rekursi dengan jumlah percabangan yang terbentuk. Semakin besar nilai `depth`, semakin banyak percabangan yang dihasilkan dan semakin kompleks bentuk Fractal Tree.

## Cara Menjalankan Program

1. Buka MATLAB.
2. Buka file `fractalTree.m`.
3. Pastikan fungsi yang diperlukan tersedia.
4. Tentukan nilai `depth` yang ingin diuji.
5. Jalankan program dengan memilih **Run**.
6. Hasil Fractal Tree akan ditampilkan pada jendela *Figure*.
7. Ulangi pengujian menggunakan nilai `depth` 1 sampai 5.

## Struktur File

```text
Pemodelan-Fractal-Tree-Kelompok-7/
│
├── README.md
├── Laporan Proyek Fractal Tree.pdf
├── fractalTree.m
├── Dokumentasi Hasil/
└── Link Video Presentasi.txt
```

## Video Presentasi

**Judul:** Pemodelan Fractal Tree Menggunakan Algoritma Rekursif – Kelompok 7

**Link YouTube:**  
https://youtu.be/s_-BTuo07lY?si=JvL1YVFNeffNQQ-A

## Kesimpulan

Proyek ini menunjukkan penerapan algoritma rekursif untuk membentuk pola Fractal Tree menggunakan MATLAB. Rekursi memungkinkan pembentukan cabang dilakukan secara berulang sampai mencapai kondisi dasar yang telah ditentukan.

Berdasarkan pengujian, peningkatan nilai `depth` menyebabkan jumlah garis dan percabangan bertambah. Dengan demikian, tingkat kedalaman rekursi berpengaruh terhadap kompleksitas pola Fractal Tree yang dihasilkan.

## Referensi

1. Rosen, K. H. (2019). *Discrete Mathematics and Its Applications* (8th ed.). McGraw-Hill Education.

2. MathWorks. (n.d.). *Plot: 2-D line plot*. MATLAB Documentation.  
   https://www.mathworks.com/help/matlab/ref/plot.html

3. MathWorks. (n.d.). *Trigonometric functions*. MATLAB Documentation.  
   https://www.mathworks.com/help/matlab/trigonometry.html

4. Swarthmore College. (2010). *CS 21 Lab 9: Fractal Tree*.

5. Swarthmore College. (2017). *CS21 Recursion Extra Challenge: Fractal Tree*.
"""
path = "/mnt/data/README.md"
with open(path, "w", encoding="utf-8") as f:
    f.write(content)
print(path)

