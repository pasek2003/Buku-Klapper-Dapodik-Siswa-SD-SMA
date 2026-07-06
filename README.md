# README – Aplikasi Buku Klapper/Kliper Data Dapodik Siswa

Aplikasi ini dibuat menggunakan **Streamlit** untuk membantu pembuatan **Buku Klapper/Kliper Siswa** jenjang **SD, SMP, dan SMA**.  
Pengguna dapat memilih jenjang sekolah, mengisi nama sekolah, memasukkan data siswa melalui Excel atau input manual, lalu mengunduh hasil akhir dalam format **Excel `.xlsx`** dengan tampilan tabel seperti format Buku Klapper.

---

## 1. Fitur Aplikasi

Aplikasi ini memiliki beberapa fitur utama:

1. Memilih jenjang sekolah:
   - SD
   - SMP
   - SMA

2. Menyesuaikan kolom **Tanggal Naik/Masuk Kelas**:
   - SD menggunakan kelas **1 sampai 6**
   - SMP/SMA menggunakan kelas **1 sampai 3**

3. Mengisi judul/nama sekolah, misalnya:
   - SDN 1 Selat
   - SMPN 1 Selat
   - SMAN 1 Selat

4. Memasukkan data siswa melalui:
   - Upload file Excel `.xlsx`
   - Input manual langsung di aplikasi

5. Mengurutkan data secara otomatis berdasarkan:
   - Nomor urut
   - Nomor induk
   - Nama siswa

6. Mengunduh hasil akhir dalam bentuk Excel dengan format tabel rapi:
   - Judul di bagian atas
   - Header bertingkat
   - Kolom kelas otomatis sesuai jenjang
   - Border tabel
   - Ukuran kolom dan baris disesuaikan agar mudah dibaca

---

## 2. Struktur Folder Aplikasi

Pastikan isi folder aplikasi kurang lebih seperti berikut:

```text
klapper_dapodik_format/
│
├── app.py
├── requirements.txt
├── README.md
├── template_klapper_sd.xlsx
├── template_klapper_smp.xlsx
└── template_klapper_sma.xlsx
```

Keterangan:

- `app.py` adalah file utama aplikasi Streamlit.
- `requirements.txt` berisi daftar library yang dibutuhkan.
- `README.md` berisi panduan penggunaan aplikasi.
- File template Excel dapat digunakan sebagai contoh format data.

---

## 3. Persiapan Sebelum Menjalankan Aplikasi

Sebelum menjalankan aplikasi, pastikan laptop/komputer sudah memiliki:

1. Python
2. Pip
3. Koneksi internet untuk install library pertama kali

Disarankan menggunakan Python versi 3.10 ke atas.

Untuk mengecek apakah Python sudah terpasang, buka CMD/Terminal lalu jalankan:

```bash
python --version
```

Atau:

```bash
py --version
```

---

## 4. Cara Install Library

Buka CMD/Terminal pada folder aplikasi, lalu jalankan:

```bash
pip install -r requirements.txt
```

Jika perintah tersebut tidak berjalan, gunakan:

```bash
py -m pip install -r requirements.txt
```

Isi minimal `requirements.txt` adalah:

```text
streamlit
pandas
openpyxl
```

Keterangan:

- `streamlit` digunakan untuk membuat tampilan aplikasi.
- `pandas` digunakan untuk mengolah data siswa.
- `openpyxl` digunakan untuk membaca dan membuat file Excel `.xlsx`.

---

## 5. Cara Menjalankan Aplikasi

Setelah library berhasil di-install, jalankan aplikasi dengan perintah:

```bash
streamlit run app.py
```

Atau jika menggunakan perintah `py`:

```bash
py -m streamlit run app.py
```

Setelah itu, aplikasi akan terbuka otomatis di browser.

Jika tidak terbuka otomatis, biasanya akan muncul alamat seperti berikut di CMD:

```text
http://localhost:8501
```

Salin alamat tersebut, lalu buka di browser.

---

## 6. Cara Menggunakan Aplikasi

### Langkah 1 – Pilih Jenjang Sekolah

Pada bagian awal aplikasi, pilih jenjang sekolah yang ingin digunakan:

- SD
- SMP
- SMA

Pilihan ini akan menentukan jumlah kolom kelas pada bagian **Tanggal Naik/Masuk Kelas**.

Untuk SD, aplikasi akan membuat kolom kelas:

```text
1, 2, 3, 4, 5, 6
```

Untuk SMP dan SMA, aplikasi akan membuat kolom kelas:

```text
1, 2, 3
```

---

### Langkah 2 – Masukkan Nama Sekolah

Masukkan nama sekolah sesuai kebutuhan, misalnya:

```text
SD NEGERI 1 SELAT
```

atau:

```text
SMA NEGERI 1 SELAT
```

Nama sekolah ini akan muncul pada bagian judul file Excel hasil download.

---

### Langkah 3 – Pilih Cara Input Data

Terdapat dua cara memasukkan data siswa:

#### A. Upload File Excel

Gunakan fitur upload jika data siswa sudah tersedia dalam bentuk Excel.

Format file yang digunakan sebaiknya `.xlsx`.

Contoh kolom yang digunakan:

```text
Urut
Induk
Nama siswa
L/P
Tempat Tanggal Lahir
Nama Orang Tua
Kelas 1
Kelas 2
Kelas 3
Kelas 4
Kelas 5
Kelas 6
Tanggal Keluar Sekolah
Catatan
```

Untuk SMP/SMA, kolom kelas hanya sampai kelas 3.

#### B. Input Manual

Gunakan input manual jika data belum tersedia dalam bentuk Excel.

Pengguna dapat mengetik langsung data siswa pada tabel yang tersedia di aplikasi.

---

### Langkah 4 – Urutkan Data

Setelah data dimasukkan, pilih metode pengurutan data.

Data dapat diurutkan berdasarkan:

1. Nomor urut
2. Nomor induk
3. Nama siswa

Aplikasi akan mengurutkan data secara otomatis sesuai pilihan pengguna.

---

### Langkah 5 – Preview Data

Sebelum download, periksa kembali data pada bagian preview.

Pastikan:

- Nama siswa sudah benar
- Nomor induk sudah benar
- Jenjang sekolah sudah sesuai
- Tanggal naik/masuk kelas sudah sesuai
- Kolom catatan sudah benar jika digunakan

---

### Langkah 6 – Download Excel

Jika data sudah benar, klik tombol download Excel.

File yang diunduh akan berbentuk `.xlsx`.

Contoh nama file:

```text
buku_klapper_sd_negeri_1_selat.xlsx
```

File hasil download sudah memiliki format tabel seperti Buku Klapper, termasuk:

- Judul
- Nama sekolah
- Header bertingkat
- Kolom nomor urut dan induk
- Kolom tanggal naik/masuk kelas
- Kolom tanggal keluar sekolah
- Kolom catatan
- Border tabel
- Ukuran kolom yang disesuaikan

---

## 7. Format Upload Excel yang Disarankan

Agar data terbaca dengan baik oleh aplikasi, gunakan format tabel sederhana.

Baris pertama sebaiknya langsung berisi nama kolom.

Contoh format untuk SD:

| Urut | Induk | Nama siswa | L/P | Tempat Tanggal Lahir | Nama Orang Tua | Kelas 1 | Kelas 2 | Kelas 3 | Kelas 4 | Kelas 5 | Kelas 6 | Tanggal Keluar Sekolah | Catatan |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|

Contoh format untuk SMP/SMA:

| Urut | Induk | Nama siswa | L/P | Tempat Tanggal Lahir | Nama Orang Tua | Kelas 1 | Kelas 2 | Kelas 3 | Tanggal Keluar Sekolah | Catatan |
|---|---|---|---|---|---|---|---|---|---|---|

Catatan:

- Gunakan file `.xlsx`.
- Hindari merge cell pada file upload.
- Hindari judul besar di bagian atas file upload.
- Judul dan format rapi akan dibuat otomatis saat download.
- Kolom kosong boleh dibiarkan kosong.
- Nomor induk sebaiknya diketik sebagai teks agar angka nol di depan tidak hilang.

---

## 8. Contoh Data

Contoh data sederhana:

| Urut | Induk | Nama siswa | L/P | Tempat Tanggal Lahir | Nama Orang Tua | Kelas 1 | Kelas 2 | Catatan |
|---|---|---|---|---|---|---|---|---|
| 1 | 12345 | I Made Contoh | L | Karangasem, 12 Mei 2015 | I Made Ayah | 15/07/2021 | 20/06/2022 | Aktif |
| 2 | 12346 | Ni Kadek Contoh | P | Karangasem, 10 Juni 2015 | I Wayan Ayah | 15/07/2021 | 20/06/2022 | Aktif |

---

## 9. Error yang Sering Terjadi dan Solusinya

### Error: No module named 'openpyxl'

Penyebab:

Library `openpyxl` belum ter-install.

Solusi:

```bash
pip install openpyxl
```

Atau:

```bash
py -m pip install openpyxl
```

---

### Error: No module named 'streamlit'

Penyebab:

Library `streamlit` belum ter-install.

Solusi:

```bash
pip install streamlit
```

Atau install semua kebutuhan aplikasi:

```bash
pip install -r requirements.txt
```

---

### Error: File Excel tidak terbaca

Kemungkinan penyebab:

1. File bukan `.xlsx`
2. File masih terbuka di Microsoft Excel
3. File memiliki format terlalu kompleks
4. Baris pertama tidak berisi nama kolom

Solusi:

- Tutup file Excel sebelum upload.
- Gunakan format `.xlsx`.
- Gunakan template Excel yang sudah disediakan.
- Pastikan baris pertama berisi nama kolom.

---

### Error: Perintah streamlit tidak dikenali

Solusi:

Gunakan perintah berikut:

```bash
py -m streamlit run app.py
```

Jika masih belum bisa, install Streamlit terlebih dahulu:

```bash
py -m pip install streamlit
```

---

## 10. Catatan Penggunaan

Aplikasi ini dibuat untuk membantu penyusunan Buku Klapper/Kliper siswa agar lebih mudah, cepat, dan rapi.

Data yang dimasukkan tetap perlu diperiksa kembali oleh pengguna sebelum file digunakan sebagai dokumen sekolah.

Pastikan data siswa yang digunakan sudah sesuai dengan data Dapodik atau arsip sekolah yang benar.

---

## 11. Penutup

Dengan aplikasi ini, pengguna dapat membuat Buku Klapper/Kliper siswa untuk jenjang SD, SMP, dan SMA secara lebih praktis.  
Pengguna cukup memilih jenjang, memasukkan nama sekolah, menginput atau mengupload data siswa, lalu mengunduh hasil akhirnya dalam bentuk Excel yang sudah rapi dan siap digunakan.
