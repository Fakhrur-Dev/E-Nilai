# AI_CONTEXT.md

## Project
E-Nilai

## Purpose
Bangun aplikasi web profesional untuk guru sesuai PROJECT_CONTEXT.md.

## Framework
- React
- TypeScript
- Vite
- Material UI

## Backend
- Firebase Authentication
- Firebase Realtime Database

## Storage
Google Drive pengguna.

## Coding Rules
- TypeScript strict mode.
- Maksimal ±300 baris per file jika memungkinkan.
- Pisahkan UI, Services, Hooks, Types, dan Utils.
- Jangan akses Firebase langsung dari halaman; gunakan Service Layer.
- Semua konfigurasi di folder config.
- Gunakan environment (.env).
- Komponen harus reusable.
- Responsive mobile-first.

## UX Rules
- Input nilai seperti spreadsheet.
- Batch save.
- Tampilkan peringatan bila ada perubahan yang belum disimpan.
- Hindari dialog yang mengganggu alur guru.

## License Rules
Periksa lisensi saat login.
FREE:
- 1 mapel
- 3 kelas
- tanpa sinkronisasi nilai pengayaan

PREMIUM:
- semua fitur aktif

## Database Awal
/users
/tokens
/licenses
/logs
/devices
/workspaces


Selalu baca PROJECT_CONTEXT.md sebelum membuat atau mengubah kode.
