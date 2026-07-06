# Aplikasi Buku Klapper Data Dapodik Siswa

Aplikasi Streamlit sederhana untuk membuat Buku Klapper/Klaper siswa SD, SMP, dan SMA.

## Fitur

- Pilih jenjang SD/SMP/SMA.
- SD otomatis memakai kolom kelas 1-6.
- SMP/SMA otomatis memakai kolom kelas 1-3.
- Judul sekolah bisa diubah, misalnya `SD NEGERI 1 SELAT` atau `SMA NEGERI 1 SELAT`.
- Input data melalui upload Excel `.xlsx` atau input manual di tabel.
- Data dapat diurutkan otomatis berdasarkan No Urut, No Induk, NISN, atau Nama siswa.
- Hasil download Excel dibuat seperti format Buku Klapper: judul, header bertingkat, merge cell, border, ukuran kolom, dan ukuran baris tetap.

## Cara Menjalankan

```bash
pip install -r requirements.txt
streamlit run app.py
```

## Format Upload

Aplikasi menerima dua format:

1. Format Buku Klapper seperti template, dengan header `Nomor`, `Urut`, `Induk`, `NISN`, `Nama siswa`, dan seterusnya.
2. Format data biasa dengan baris pertama sebagai nama kolom.

Kolom utama:

- No Urut
- No Induk
- NISN
- Nama siswa
- L/P
- Tempat Tanggal Lahir
- Nama Orang Tua
- Kelas 1 sampai Kelas 6 untuk SD
- Kelas 1 sampai Kelas 3 untuk SMP/SMA
- Tanggal Keluar Sekolah
- Catatan

