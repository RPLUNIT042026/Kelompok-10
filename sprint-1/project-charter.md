<div align="center">

# PROJECT CHARTER — SKILL SWAP

![Doc](https://img.shields.io/badge/DOCUMENT-PROJECT%20CHARTER-FFAA00?style=for-the-badge)
![Version](https://img.shields.io/badge/VERSION-1.0%20(SPRINT%201)-55FF55?style=for-the-badge)
![Scope](https://img.shields.io/badge/STATUS-APPROVED%20BY%20TEAM-55FFFF?style=for-the-badge)

> Dokumen piagam proyek resmi yang mendefinisikan visi, ruang lingkup kerja, pembagian peran, jadwal sprint, analisis risiko, dan kriteria keberhasilan pengembangan aplikasi **Skill Swap**.

</div>

---

## 1. Informasi & Otorisasi Proyek

| Parameter | Keterangan |
| :--- | :--- |
| **Nama Proyek** | **Skill Swap** — Platform Pertukaran Keahlian Antarmahasiswa |
| **Kode Proyek** | `RPL-SKILLSWAP-2026` |
| **Project Manager** | Muhammad Al Khaliq (`240504109`) |
| **Tim Pengembang** | 4 Anggota (PM/QA, UI/UX & Frontend, Backend/Auth/Matching, Database/Profil) |
| **Teknologi Utama** | React, Node.js, Express, MySQL, JWT |
| **Tanggal Penyusunan** | Sprint 1 — Fase Inisiasi Proyek |

---

## 2. Tujuan Proyek (*Project Objectives*)

Proyek **Skill Swap** bertujuan menghasilkan perangkat lunak berbasis web yang memenuhi sasaran terukur berikut:

1. **Membangun Platform Pertukaran Keahlian:** Menyediakan aplikasi web fungsional yang memungkinkan mahasiswa mendaftarkan keahlian yang dikuasai dan keahlian yang ingin dipelajari.
2. **Mengimplementasikan Algoritma *Skill Matching*:** Menghadirkan sistem rekomendasi partner belajar otomatis berbasis kecocokan dua arah (*bidirectional matching*) dengan waktu respons pencarian di bawah $1$ detik.
3. **Menjamin Keamanan & Alur Transaksi Jelas:** Menerapkan autentikasi berbasis **JWT** serta siklus status pertukaran keahlian yang tervalidasi dari pengajuan hingga pemberian ulasan.
4. **Menyelesaikan Seluruh Siklus SDLC:** Menghasilkan dokumentasi perangkat lunak lengkap, kode sumber terstruktur di GitHub, serta aplikasi yang lolos pengujian fungsional (*Black-Box Testing*).

---

## 3. Ruang Lingkup Proyek (*Project Scope*)

Untuk menjaga fokus pengerjaan agar selesai tepat waktu dalam satu semester, ruang lingkup sistem ditetapkan sebagai berikut:

### Dalam Ruang Lingkup (*In-Scope*)
* Registrasi akun baru, login pengguna, dan manajemen sesi menggunakan **JWT**.
* Manajemen profil mahasiswa beserta daftar keahlian yang ditawarkan (*Skills Offered*) dan dicari (*Skills Wanted*).
* Fitur pencarian pengguna berdasarkan nama/kategori keahlian.
* Mesin rekomendasi partner otomatis menggunakan algoritma **Bidirectional Skill Matching**.
* Alur pengajuan permintaan *swap*, persetujuan/penolakan permintaan, dan penyelesaian sesi.
* Sistem pemberian *rating* (bintang $1$–$5$) dan ulasan tertulis pasca-pertukaran.

### Di Luar Ruang Lingkup (*Out-of-Scope*)
* Fitur panggilan video (*video conference*) atau papan tulis virtual terintegrasi di dalam aplikasi (koordinasi sesi belajar dilakukan melalui kontak yang disepakati partner).
* Integrasi gerbang pembayaran (*payment gateway*), karena platform murni mengusung konsep barter keahlian gratis.
* Pengembangan aplikasi *mobile* native (Android/iOS); aplikasi berfokus pada web responsif.

---

## 4. Struktur Organisasi Tim (4 Anggota)

| Peran Proyek | Nama Anggota | NIM | Tanggung Jawab Utama |
| :--- | :--- | :---: | :--- |
| **Project Manager, Dokumentasi & QA** | Muhammad Al Khaliq | `240504109` | Koordinasi sprint, dokumentasi RPL, manajemen GitHub, dan pengujian sistem (*testing*). |
| **UI/UX Designer & Frontend Dev** | Muhammad Syahlulalbar | `240504118` | Desain antarmuka pengguna (*wireframe/mockup*) dan implementasi klien menggunakan **React**. |
| **Backend, Auth & Matching Dev** | Riska Lestari | `250504008` | Pengembangan *REST API* (**Node.js + Express**), autentikasi **JWT**, dan logika **Skill Matching**. |
| **Database & Profile System Dev** | Ridka Putri | `250504010` | Desain skema **MySQL**, pengelolaan profil, inventori keahlian, fitur pencarian, dan ulasan. |

---

## 5. Jadwal Pengerjaan (*Sprint Roadmap*)

Pengembangan dibagi menjadi **4 Sprint** terstruktur:

| Tahap | Fokus Utama | Luaran Utama (*Deliverables*) |
| :--- | :--- | :--- |
| **Sprint 1** | **Inisiasi & Perencanaan** | Setup repository GitHub, *Profil Kelompok*, *Profil Project*, dan *Project Charter*. |
| **Sprint 2** | **Analisis, Desain UI & Database** | Diagram sistem (*Use Case*, *Activity*, *ERD*), *wireframe* UI, dan struktur tabel **MySQL**. |
| **Sprint 3** | **Pengembangan Fitur Inti** | API Autentikasi **JWT**, manajemen profil & keahlian, antarmuka **React**, dan mesin **Skill Matching**. |
| **Sprint 4** | **Transaksi Swap, Testing & Finalisasi** | Fitur pengajuan/persetujuan *swap*, *rating* & ulasan, *Black-Box Testing*, dan dokumentasi akhir. |

---

## 6. Analisis Risiko & Rencana Mitigasi

| No | Potensi Risiko | Tingkat Dampak | Strategi Mitigasi |
| :---: | :--- | :---: | :--- |
| 1 | **Konflik kode (*merge conflict*)** saat anggota melakukan `push` bersamaan ke GitHub. | Sedang | Menerapkan pembagian folder/modul kerja per anggota serta mewajibkan `git pull` sebelum `git push`. |
| 2 | **Ketidaksesuaian format data API** antara tim *Frontend* (React) dan *Backend* (Express). | Tinggi | Menyepakati kontrak *endpoint* JSON (struktur *request* dan *response*) di awal Sprint 3 sebelum integrasi. |
| 3 | **Kompleksitas kueri pencocokan** saat data keahlian pengguna bertambah banyak. | Sedang | Mengoptimalkan indeks pada tabel relasi `user_skills` di MySQL dan membatasi hasil rekomendasi teratas (*Top-N*). |
| 4 | **Keterlambatan jadwal** akibat bentrok dengan tugas mata kuliah lain. | Tinggi | Melakukan evaluasi progres mingguan oleh Project Manager dan memprioritaskan fitur MVP terlebih dahulu. |

---

## 7. Kriteria Keberhasilan (*Definition of Done*)

Proyek dinyatakan berhasil apabila memenuhi seluruh indikator berikut:
* [x] **Sprint 1:** Repository GitHub aktif dan seluruh anggota tercatat melakukan `commit` serta `push`.
* [ ] **Fungsionalitas:** Seluruh 8 fitur utama dan fitur unggulan *Skill Matching* berjalan tanpa *error* fatal.
* [ ] **Keamanan:** Rute privat terlindungi dengan validasi token JWT dan kata sandi tersimpan dalam bentuk terenkripsi (*hashed*).
* [ ] **Pengujian:** Seluruh skenario uji pada dokumen pengujian lulus verifikasi QA.

---

## 8. Lembar Pengesahan Tim

Dengan ini seluruh anggota tim menyepakati ruang lingkup, pembagian peran, dan komitmen pengerjaan proyek **Skill Swap**:

| No | Nama Lengkap | NIM | Peran | Status Persetujuan |
| :---: | :--- | :---: | :--- | :---: |
| 1 | Muhammad Al Khaliq | `240504109` | Project Manager, Dokumentasi & QA | Disetujui |
| 2 | Muhammad Syahlulalbar | `240504118` | UI/UX Designer & Frontend Developer | Disetujui |
| 3 | Riska Lestari | `250504008` | Backend, Auth & Matching Developer | Disetujui |
| 4 | Ridka Putri | `250504010` | Database & Profile System Developer | Disetujui |