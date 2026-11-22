<div align="center">

# 🕹️ PROFIL KELOMPOK — SKILL SWAP

![Guild](https://img.shields.io/badge/PROJECT-SKILL%20SWAP-55FF55?style=for-the-badge&logo=minecraft&logoColor=white)
![Party](https://img.shields.io/badge/PARTY%20SIZE-4%20PLAYERS-55FFFF?style=for-the-badge)
![Quest](https://img.shields.io/badge/QUEST-SPRINT%201-FFAA00?style=for-the-badge)
![Method](https://img.shields.io/badge/METHOD-AGILE%20SCRUM-FF55FF?style=for-the-badge)

> *"Satu keahlian yang dibagikan akan melahirkan dua keahlian baru — membangun ekosistem belajar kolaboratif antarmahasiswa, blok demi blok."*

</div>

---

## 📋 Identitas Tim & Proyek

| Atribut | Detail Informasi |
| :--- | :--- |
| **Nama Proyek** | **Skill Swap** — Platform Pertukaran Keahlian Antarmahasiswa |
| **Mata Kuliah** | Rekayasa Perangkat Lunak (RPL) |
| **Repository Utama** | `skill-swap` |
| **Jumlah Anggota** | 4 Mahasiswa (Full Co-Op Squad) |
| **Metodologi Kerja** | Agile Scrum (Iterative Sprint) |
| **Status Saat Ini** | `Sprint 1` — Inisiasi Proyek, Analisis & Perencanaan |

---

## ⚔️ Roster Tim Pengembang (*Player Select*)

Berikut adalah formasi lengkap keempat anggota tim pengembang beserta peran utama dan akun GitHub yang digunakan untuk kolaborasi:

| Slot | Player | Nama Lengkap | NIM | Class / Peran Utama | Akun GitHub |
| :---: | :---: | :--- | :---: | :--- | :--- |
| `01` | 🟨 **Player 01** | **Muhammad Al Khaliq** | `240504109` | **Project Manager**, Dokumentasi & QA Testing | [@Al-khaliq](https://github.com/Al-khaliq) |
| `02` | 🟩 **Player 02** | **Muhammad Syahlulalbar** | `240504118` | **UI/UX Designer** & Frontend Developer | [@Sya521](https://github.com/Sya521) |
| `03` | 🟪 **Player 03** | **Riska Lestari** | `250504008` | **Backend Developer**, Auth & Matching Engine | [@riskalestari1015](https://github.com/riskalestari1015) |
| `04` | 🟦 **Player 04** | **Riska Aulia Putri** | `250504010` | **Database Architect** & Manajemen Profil | [@riskauliaputri10-wq](https://github.com/riskauliaputri10-wq) |

---

## 🛠️ Matriks Pembagian Tugas & Tanggung Jawab

Seluruh kebutuhan pengembangan sistem **Skill Swap** dibagi secara merata dan terukur ke dalam empat peran inti:

### 🟨 Player 01 — Muhammad Al Khaliq
> **Role:** *Project Manager, Dokumentasi & Quality Assurance (QA)*
* **Manajemen Proyek:** Menyusun jadwal pengerjaan (*timeline* sprint), membagi daftar tugas (*backlog*), dan memantau progres mingguan tim.
* **Dokumentasi Sistem:** Menyusun dan memelihara seluruh dokumen RPL (*Profil Kelompok*, *Profil Project*, *Project Charter*, serta laporan akhir).
* **Quality Assurance & Testing:** Menyusun skenario pengujian (*test case*), melakukan *Black-Box Testing* pada setiap fitur sebelum rilis, dan memastikan repository GitHub selalu terorganisir.

### 🟩 Player 02 — Muhammad Syahlulalbar
> **Role:** *UI/UX Designer & Frontend Developer (React)*
* **Perancangan UI/UX:** Membuat *user flow*, *wireframe*, dan desain antarmuka modern yang intuitif untuk proses pencarian serta pertukaran keahlian.
* **Pengembangan Frontend:** Membangun antarmuka aplikasi berbasis **React** (halaman Login/Register, Dashboard Profil, Katalog Keahlian, Rekomendasi Partner, Inbox Permintaan Swap, dan Ulasan).
* **Integrasi API:** Menghubungkan komponen antarmuka dengan *endpoint REST API* dari server serta menangani validasi form di sisi pengguna.

### 🟪 Player 03 — Riska Lestari
> **Role:** *Backend Developer, Authentication & Skill Matching Engine*
* **Arsitektur Server & API:** Membangun *RESTful API* menggunakan **Node.js + Express** untuk seluruh alur bisnis aplikasi.
* **Keamanan & Autentikasi:** Mengimplementasikan sistem registrasi, login, enkripsi kata sandi, dan proteksi rute menggunakan **JWT (*JSON Web Token*)**.
* **Algoritma Skill Matching:** Merancang dan mengkodekan logika pencocokan dua arah (*mutual skill matching*) untuk menghasilkan daftar rekomendasi partner belajar terbaik, serta mengelola alur pengajuan dan persetujuan pertukaran keahlian.

### 🟦 Player 04 — Riska Aulia Putri
> **Role:** *Database Architect & Manajemen Profil / Pencarian*
* **Perancangan Basis Data:** Membuat *Entity Relationship Diagram* (ERD) dan struktur tabel relasional di **MySQL** (`users`, `skills`, `user_skills`, `swap_requests`, `reviews`).
* **Manajemen Profil & Keahlian:** Mengembangkan fitur pengelolaan biodata mahasiswa, daftar keahlian yang dikuasai (*Skills Offered*), dan keahlian yang ingin dipelajari (*Skills Wanted*).
* **Pencarian & Sistem Ulasan:** Mengimplementasikan kueri pencarian pengguna berdasarkan keahlian serta pencatatan skor *rating* dan ulasan setelah sesi pertukaran selesai.

---

## 🔄 Protokol Kolaborasi Git & GitHub

Agar setiap kontribusi anggota tercatat secara transparan di riwayat repository:

```text
[git pull origin main] ──▶ [Kerjakan Tugas Bagian] ──▶ [git add .] ──▶ [git commit -m "..."] ──▶ [git push origin main]
```

| Prefix Commit | Kegunaan | Contoh Penggunaan |
| :--- | :--- | :--- |
| `docs:` | Penambahan atau pembaruan dokumentasi | `docs: menambahkan dokumen profil kelompok` |
| `feat:` | Pembuatan fitur atau halaman baru | `feat: membuat endpoint algoritma skill matching` |
| `ui:` | Perancangan tampilan atau komponen React | `ui: membuat kartu rekomendasi partner swap` |
| `db:` | Perubahan struktur tabel atau kueri MySQL | `db: membuat skema tabel user_skills dan swap_requests` |
| `fix:` | Perbaikan *bug* atau penyesuaian alur | `fix: memperbaiki validasi token JWT pada rute profil` |