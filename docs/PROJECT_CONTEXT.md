# PROJECT_CONTEXT.md

# E-Nilai (Cloud Academic Assessment System)

## Tagline
**Sederhana untuk Guru, Cerdas untuk Data**

## Visi
Membangun sistem entri nilai berbasis web yang sederhana, cepat, responsif, dan aman, dengan seluruh data akademik tersimpan di Google Drive milik pengguna.

## Prinsip Utama
- Data tetap milik guru.
- Developer tidak menyimpan data nilai siswa.
- UI dibuat sesederhana spreadsheet.
- Penyimpanan dilakukan secara batch saat tombol **Simpan** ditekan.
- Responsif di Desktop, Tablet, Android, dan iPhone.

## Teknologi
- React + TypeScript + Vite
- Material UI
- AG Grid Community (untuk input nilai bergaya spreadsheet)
- Firebase Authentication
- Firebase Realtime Database
- Cloud Firestore

# Authentication

Menggunakan Firebase Authentication.
Halaman Login terdiri dari:
- Nama Guru (saat registrasi)
- Email
- Password
- Login
- Daftar
- Lupa Password

# User Profile

Setiap user memiliki data:

- uid
- nama guru
- email
- sekolah
- license
- token
- status
- createdAt
- lastLogin
- appVersion

# Welcome
Selamat Datang (Nama Guru)
dan lain-lain
## Informasi Lisensi Pertahun
### Free
- Maksimal 1 mata pelajaran
- Maksimal 3 kelas
- Tidak dapat menyimpan nilai pengayaan ke Google Drive

### Premium
- Tanpa batas mapel
- Tanpa batas kelas
- Seluruh fitur diaktifkan menggunakan Token License.
- Token dibuat oleh Developer melalui google sheet dengan akses role khusus ke firebase
- Saat aktivasi token, Firebase akan memperbarui status lisensi user berdasarkan waktu (1 Tahun).

## Penyimpanan
Firestrore adalah penyimpanan nilai utama.
Firebase hanya menyimpan metadata pengguna, lisensi, token, dan konfigurasi.

## Master Data
- Tahun Ajaran
- Semester
- Sekolah
- Guru
- Kelas
- Mata Pelajaran
- TP atau Materi tiap mapel terdiri 9 TP (dinamis, jik guru hanya mengisi 3 TP,  3 TP yang kolomya tampil) Tiap jenjang kelas dan mapel beda TP
- Siswa (NIS sebagai ID utama, NISN sebagai identitas nasional)

## Filosofi Input Nilai
- Semudah spreadsheet seindah aplikasi.
- Tidak ada kompleksitas yang tidak diperlukan.
- Nilai disimpan per kelas (batch save).
- Perubahan nilai rapor dicatat di belakang layar tanpa mengganggu guru.

## Urutan kerja guru:
  Pilih:
  Halaman Pertama
- Tahun (dropdown) otomatis; Baca tahun sistem
- Semester (dropdown) otomatis; bulan juli-desember semester 1. bulan januari sampai juni semester 2
- Bobot Nilai Harian default Rata-Rata TP yang ada keterangannya, nilainya dirata2 dikali 60%, Bobot Ujian Rata-Rata STS dan SAS dikali 40% (Kolom Bobot bisa dirubah dan disimpan sesuai Tahun Ajaran, Semester, Mapel dan Kelas)
- Download Master Template excel (Mata Pelajaran,Kelas, NIS, NISN, NAMA SISWA/i)
- Upload dan Simpan ke Firestore
Halaman Kedua
- Tahun (dropdown)
- Semester (dropdown)
- Mata Pelajarn (dopdown yang diisi dari template Master)
- Isi KKM KKTP (isi manual, diingat sistem ketika disimpan tampil pada Tahun AJaran, Semester, Mapel dan Kelas yang sama seebagaimana diinput disimpan)
- Silahkan ISI TP/ Materi, contoh:
  1. Menganlisa Pernikahan dalam Islam
  2. Menjelaskan Hukum Waris
  3. dst (tergatung input user)
- Tombol Simpan
Halaman Ketiga
- Pilih Tahun
- Pilih Semester
- Pilih Kelas
- Pilih Mapel
- Isi NIlai P1 - P9 ( kolom P yang tampil tergatung P yang diisi user) STS, SAS, Nilai Raport (otomatis terkalulasi dari Bobot yag sudah diinput di halaman pertama.
- Tombol Simpan ke memori internal (bisa dipiih) dalam format excel lengkap (Nama Guru, Nama MApel, Kelas, Siswa, P!-P9 STS SAS Nilai Raport dan keterangan capaiannya berdasarkan TP.
- Tombol Kirim via WA/ Telegram dalam bentuk text NAMA GURU, NAMA MAPEL, NAMA KELAS, NAMA SISWA, P1 (60) P3 (50) dst (yang ditampilkan P yang di bawah KKM.
Halaman Keempat
- Pilih Tahun
- Pilih Semester
- Pilih Kelas
- Pilih Mapel
- Tampilkan Nilai yang sudah diinput
- Halaman Bawah ada kolom (Batas bawah dan Batas atas) yang bisa diisi dan dirubah, defaultya nilai MIN dan MAX Kelas tersebut.
- Jika diklik tombol Distribusi Nilai maka Nilai Raport siswa kelas tersebut mengikuti batas bawah dan batas atas itu, demikian juga niai-niai P nya menyesuaikan sehingga jika di rata-rata Rata-rata P x bobot harian + Rata Rata STS & SAS x bobot ujian sama dengan nilai yag sudah dikatrol tersebut.
- Tomnol simpan untuk mengunduh dalam format excel ke memori internal (bisa dipilih kemana mau disimpan). Formatnya ( NAMA GURU, NAMA MAPEL, NAMA KELAS, NAMA SISWA, P1 (60) P3 (50) dst Rata-Rata Ujian (STS & SAS) disatukan kolomnya) dan Rata-rata Raport yang sudah dikatrol.
Halaman Terakhir
Update versi (untuk update)
Agregat berapa banyak guru sekolah yang sedang aktif dan info masa berlakunya Lisensi
Jika waktu telah genap 1 tahun maka ada peringatan harus beli token lagi via Ozi 085196406495 dan berakhir lisensi tidak menyebabkan data menjadi hilang hanya peringatan donasi dan konsekuensi tidak bisa mengupdate dan membackup nilai ke database sentral.

Jangan lupa navigasi antar halaman di bawah

