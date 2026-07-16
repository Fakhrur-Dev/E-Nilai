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
- Firebase Authentication
- Firebase Realtime Database
- Google Drive API
- Google Sheets API

## Lisensi
### Free
- Maksimal 1 mata pelajaran
- Maksimal 3 kelas
- Tidak dapat menyimpan nilai pengayaan ke Google Drive

### Premium
- Tanpa batas mapel
- Tanpa batas kelas
- Seluruh fitur aktif menggunakan Token

## Penyimpanan
Google Drive pengguna adalah penyimpanan utama.
Firebase hanya menyimpan metadata pengguna, lisensi, token, dan konfigurasi.

## Master Data
- Tahun Ajaran
- Semester
- Sekolah
- Guru
- Kelas
- Mata Pelajaran
- Siswa (NIS sebagai ID utama, NISN sebagai identitas nasional)

## Filosofi Input Nilai
- Semudah spreadsheet.
- Tidak ada kompleksitas yang tidak diperlukan.
- Nilai disimpan per kelas (batch save).
- Perubahan nilai rapor dicatat di belakang layar tanpa mengganggu guru.

## Roadmap
v0.1 Foundation
v0.2 Workspace Google Drive
v0.3 Master Data
v0.4 Input Nilai
v0.5 Laporan
v1.0 Stable
