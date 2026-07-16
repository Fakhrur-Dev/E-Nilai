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
Cloud Firestore
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
- Firestore

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

1. Firebase Authentication
3. Cek user
4. Cek masa lisensi
5. Dashboard


## Penyimpanan
- Firebase
- Firestore
- Memori Internal device

## Prinsip
- Mobile First
- Responsive
- Batch Save
- Offline draft
- Spreadsheet experience
- Modular
- Service Layer
