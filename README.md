# Program Rekap dan Analisis Nilai Matematika Kelas

## Identitas

**Nama:** Vanisya Nur Khalimah  
**NIM:** 2225250201  
**Kelas:** 3B

---

## 1. Deskripsi Program

Program Rekap dan Analisis Nilai Matematika Kelas merupakan aplikasi sederhana yang dikembangkan menggunakan bahasa pemrograman Python untuk membantu proses pengolahan data nilai siswa. Program ini membaca data dari file teks, kemudian melakukan pemeriksaan, pengolahan, serta penyajian informasi nilai secara otomatis.

Melalui program ini, pengguna dapat mengetahui berbagai informasi penting, seperti rata-rata nilai kelas, nilai tertinggi, nilai terendah, jumlah siswa yang memenuhi kriteria ketuntasan, serta jumlah siswa yang belum tuntas. Selain itu, program juga mampu mengidentifikasi data yang tidak sesuai sehingga dapat mengurangi kemungkinan kesalahan dalam proses pengolahan nilai.

---

## 2. Tujuan Program

Program ini dibuat dengan tujuan sebagai berikut:

1. Membaca data siswa yang berisi NIM dan nilai dari file teks.
2. Memastikan data yang diproses telah memenuhi aturan validasi yang ditentukan.
3. Menghasilkan informasi statistik nilai siswa secara otomatis.
4. Mengelompokkan siswa berdasarkan status ketuntasan belajar.
5. Menampilkan hasil analisis dan menyimpannya ke dalam file keluaran.

---

## 3. Ketentuan Program

Agar proses pengolahan data berjalan dengan benar, program menerapkan beberapa aturan berikut:

1. Nilai yang dapat diproses berada pada rentang 0 sampai 100.
2. Nilai minimum ketuntasan ditetapkan sebesar 60.
3. Siswa dengan nilai 60 atau lebih dinyatakan **Tuntas**.
4. Siswa dengan nilai di bawah 60 dinyatakan **Belum Tuntas**.
5. Data yang tidak memenuhi format atau ketentuan akan diabaikan dalam proses perhitungan.
6. Program akan menampilkan pesan kesalahan apabila file tidak ditemukan atau tidak terdapat data yang valid untuk dianalisis.

---

## 4. Struktur Folder

```text
program-rekap-nilai/
├── data/
│   ├── nilai_contoh.txt
│   └── hasil_rekap.txt
├── hasil/
│   └── .gitkeep
├── main.py
├── analisis.py
├── data_io.py
├── utilitas.py
├── proposal.md
├── test_case.md
├── README.md
├── .gitignore
└── .gitkeep
```

### Penjelasan Struktur

- `main.py` berfungsi sebagai pusat kontrol yang menjalankan seluruh proses program.
- `analisis.py` berisi fungsi-fungsi untuk menghitung statistik nilai dan menentukan status ketuntasan siswa.
- `data_io.py` menangani proses pembacaan data masukan dan penyimpanan hasil pengolahan.
- `utilitas.py` menyediakan fungsi pendukung seperti validasi nilai dan penentuan status siswa.
- `data/nilai_contoh.txt` digunakan sebagai file input yang berisi data nilai siswa.
- `data/hasil_rekap.txt` digunakan untuk menyimpan hasil rekapitulasi nilai.
- `hasil/.gitkeep` berfungsi agar folder kosong tetap dapat disimpan dalam repositori Git.
- `proposal.md` berisi rancangan dan deskripsi proyek.
- `test_case.md` memuat skenario pengujian program.
- `.gitignore` digunakan untuk menentukan file atau folder yang tidak perlu dilacak oleh Git.

> **Catatan:** File `hasil_rekap.txt` akan terbentuk setelah proses penyimpanan berhasil dilakukan. Sementara itu, file `.gitkeep` dapat dihapus apabila folder terkait telah berisi file lain.

---

## 5. Format Data Masukan

Data nilai disimpan dalam file `data/nilai_contoh.txt` dengan format berikut:

```text
A001,85
A002,78
A003,92
A004,abc
A005,60
A006,50
A007,75
A008,88
A009,45
A010,100
```

Setiap baris terdiri atas pasangan NIM dan nilai yang dipisahkan menggunakan tanda koma (`,`). Pada contoh tersebut, data `A004,abc` dianggap tidak valid karena nilai yang diberikan bukan berupa angka.

---

## 6. Cara Menjalankan Program

### Persyaratan

Sebelum menjalankan program, pastikan bahwa:

1. Python versi 3 atau yang lebih baru telah terinstal pada komputer.
2. Semua file program tersimpan sesuai dengan struktur folder yang telah ditentukan.
3. File input tersedia pada lokasi yang digunakan oleh program.

### Langkah Menjalankan

1. Buka folder proyek menggunakan Visual Studio Code atau editor lain yang mendukung Python.
2. Akses terminal pada direktori utama proyek.
3. Jalankan perintah berikut:

```bash
python main.py
```

Apabila sistem menggunakan konfigurasi yang berbeda, perintah berikut dapat digunakan:

```bash
python3 main.py
```

Pastikan seluruh modul yang diperlukan telah diimpor dengan benar ke dalam `main.py` sebelum program dijalankan.

---

## 7. Contoh Hasil yang Diharapkan

Berdasarkan data contoh yang digunakan, terdapat sembilan data yang valid dan satu data yang tidak memenuhi syarat.

| Komponen | Hasil |
|-----------|-------:|
| Jumlah siswa valid | 9 |
| Total nilai | 673 |
| Rata-rata nilai | 74,78 |
| Nilai tertinggi | 100 |
| Nilai terendah | 45 |
| Jumlah siswa tuntas | 7 |
| Jumlah siswa belum tuntas | 2 |
| Data tidak valid | 1 |

Hasil tersebut menunjukkan bahwa sebagian besar siswa telah mencapai batas ketuntasan yang ditentukan. Bentuk tampilan hasil di terminal dapat berbeda tergantung pada cara implementasi program.

---

## 8. Pengujian Program

Proses pengujian dilakukan untuk memastikan seluruh fitur program berjalan sesuai kebutuhan dan menghasilkan keluaran yang benar.

Beberapa aspek yang diuji meliputi:

1. Validasi nilai agar berada pada rentang yang diperbolehkan.
2. Penentuan kategori ketuntasan siswa secara tepat.
3. Kemampuan membaca data dari file teks.
4. Penanganan data kosong maupun data yang tidak valid.
5. Perhitungan statistik seperti rata-rata, nilai maksimum, dan nilai minimum.
6. Penanganan kondisi ketika file input tidak ditemukan.
7. Proses penyimpanan hasil rekap ke file keluaran.

Program dinyatakan berhasil apabila hasil yang diperoleh sesuai dengan hasil yang diharapkan pada setiap skenario pengujian.

---

## 9. Analisis Efisiensi

Jika jumlah data siswa dinyatakan sebagai **n**, maka:

- **Kompleksitas waktu (Time Complexity): O(n)** karena setiap data siswa harus dibaca dan diproses setidaknya satu kali.
- **Kompleksitas ruang (Space Complexity): O(n)** karena informasi yang telah dibaca perlu disimpan sementara dalam memori untuk keperluan analisis.

Dengan kompleksitas tersebut, program cukup efisien untuk digunakan pada pengolahan data nilai kelas yang berukuran kecil maupun menengah.

---

## 10. Kesimpulan

Program Rekap dan Analisis Nilai Matematika Kelas memberikan solusi yang praktis dalam proses pengolahan data nilai siswa. Melalui pemanfaatan Python, proses pembacaan data, validasi, analisis statistik, hingga pembuatan rekap dapat dilakukan secara otomatis dan lebih terorganisir dibandingkan perhitungan manual.

Ke depan, program ini masih dapat dikembangkan dengan menambahkan berbagai fitur, seperti pencarian data siswa, pengurutan berdasarkan nilai, antarmuka grafis yang lebih interaktif, serta kemampuan ekspor data ke format CSV maupun Excel untuk mempermudah pengelolaan dan pelaporan data nilai.
