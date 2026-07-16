# ARCHITECTURE.md

# E-Nilai Architecture v0.1

## Tujuan
Membangun aplikasi web pengelolaan nilai yang sederhana, modular, cepat, dan seluruh data akademik disimpan di Google Drive milik pengguna.

## Arsitektur

```text
Browser
   │
React + TypeScript + Material UI
   │
Service Layer
   │
Firebase Auth ─ Firebase RTDB
   │
Google Drive API
   │
Google Sheets
```

## Layer

### Presentation
- Pages
- Layouts
- Components

### Business
- AuthService
- LicenseService
- WorkspaceService
- MasterDataService
- GradeService

### Data
- Firebase
- Google Drive
- Google Sheets

## Folder

```text
src/
 app/
 assets/
 components/
 config/
 firebase/
 hooks/
 layouts/
 pages/
 routes/
 services/
 store/
 theme/
 types/
 utils/
```

## Authentication Flow
1. Login Google
2. Firebase Authentication
3. Cek user
4. Cek lisensi
5. Dashboard

## Workspace Flow
Guru → Buat Workspace → Folder Google Drive → Spreadsheet otomatis → Siap digunakan.

## Penyimpanan
- Firebase = metadata
- Google Drive = file
- Google Sheets = master & nilai

## Prinsip
- Mobile First
- Responsive
- Batch Save
- Offline draft
- Spreadsheet experience
- Modular
- Service Layer
