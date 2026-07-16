# DATABASE.md

# Firebase Realtime Database

```text
users/
  uid/
    email
    displayName
    provider
    guru
    sekolah
    license
    token
    status
    version
    createdAt
    lastLogin
    devices/

tokens/
  TOKEN123/
    status
    license
    sekolah
    guru
    activatedBy
    activatedAt

licenses/
  uid/
    type
    expiresAt
    activatedAt

logs/
  uid/
    login/
    activation/

workspaces/
  uid/
    workspaceId/
      tahunAjaran
      semester
      driveFolderId
      spreadsheetId
```

# Google Drive

```text
E-Nilai/
└── 2026-2027/
    ├── Semester Ganjil/
    │   ├── Master/
    │   ├── Nilai/
    │   └── Arsip/
    └── Semester Genap/
```

# Google Sheets

Master_Siswa
- NIS (Primary Key)
- NISN
- Nama
- Kelas

Master_Mapel
Master_Kelas

Nilai
- NIS
- TP
- Nilai
- Nilai Rapor

Riwayat_Perubahan
- NIS
- NISN
- Nama
- Nilai Sebelum
- Nilai Sesudah
- Waktu Simpan

# Aturan
- NIS adalah ID utama.
- NISN sebagai identitas nasional.
- Data semester yang sama dapat ditimpa.
- Semester berbeda menjadi arsip permanen.
