# Kontribusi Kelompok – UTS Deep Learning 2026

**Mata Kuliah:** Deep Learning (S1 Teknik Komputer, Fakultas Teknik Elektro, Universitas Telkom)
**Repositori Utama:** https://github.com/monicafebyana-wq/DL-UTS-2026
**Fork Anggota 1:** https://github.com/cheyzaamanda/DL-UTS-2026

## 1. Anggota Kelompok dan Pembagian Peran

### A. Cheyza Amanda Syafira (NIM: 101032300081 | GitHub: @cheyzaamanda)

- Pengerjaan **Task 1 – Klasifikasi Multimodal** (cacat produk dari gambar dan sensor): pemeriksaan integritas dan EDA data (distribusi kelas, sensor hilang, perbedaan lini A dan B), preprocessing dan pembagian data stratified kelas × lini, perancangan image encoder (CNN 2D), signal encoder (CNN 1D), dan fusion concat/gated, pelatihan dan perbandingan image-only, sensor-only, dan fusion, analisis label tidak sempurna, domain shift antar-lini, ketahanan terhadap sensor hilang (modality dropout), sanity check, ensemble tiga seed, dan pembuatan `prediksi_klasifikasi.csv`.
- Pengerjaan **Task 3 – Clustering Multimodal, bagian gambar (Anggota 1)**: EDA gambar mikrostruktur, preprocessing gambar, representation learning gambar (contrastive encoder), dan pembuatan `embedding_gambar.npz` (D = 64).
- Penyusunan bagian Task 1 dan bagian gambar Task 3 pada laporan.

### B. Monica Febyana (NIM: 101032330068 | GitHub: @monicafebyana-wq)

- Pengerjaan **Task 2 – Time-Series Regression (Remaining Useful Life)**: EDA data mesin, normalisasi per regime operasi, penanganan spike dan nilai hilang, seleksi fitur, pelabelan RUL, sliding window, pemodelan (baseline dan model sekuens), evaluasi dengan RMSE dan skor asimetris, estimasi ketidakpastian, dan pembuatan `prediksi_rul.csv`.
- Pengerjaan **Task 3 – Clustering Multimodal, bagian spektrum (Anggota 2)**: EDA, preprocessing, dan representation learning spektrum, integrasi embedding gambar, fusi multimodal, clustering (KMeans, GMM, DEC), penentuan jumlah cluster, visualisasi, evaluasi, dan pembuatan `cluster.csv`.
- Penyusunan bagian Task 2 dan bagian spektrum, fusi, dan clustering pada Task 3 di laporan.

### Laporan

Laporan disusun berdua: setiap anggota menulis bagian dari task yang dikerjakannya, kemudian kedua anggota saling meninjau dan menyatukan laporan menjadi satu dokumen.

## 2. Daftar Pull Request (PR) Kontribusi

Pengembangan dilakukan melalui fork dan branch masing-masing sebelum digabungkan ke branch `main` repositori utama.

- **PR #1 – Integrasi Task 1, Task 3 bagian gambar, dan dokumentasi laporan** (oleh @cheyzaamanda): https://github.com/monicafebyana-wq/DL-UTS-2026/pull/1
  Ringkasan: Menambahkan notebook dan implementasi Task 1 (klasifikasi multimodal), integrasi Task 3 Anggota 1 dan Anggota 2, serta dokumentasi laporan UTS. Di-merge oleh @monicafebyana-wq ke `main`.
- **PR #2 – Penghapusan dokumentasi laporan sementara** (oleh @cheyzaamanda): https://github.com/monicafebyana-wq/DL-UTS-2026/pull/2
  Ringkasan: Merapikan repositori dengan menghapus berkas dokumentasi laporan yang ditambahkan pada PR #1.
- **PR #3 – Task 2 (RUL), Task 3 bagian Spektrum & Clustering, dan dokumentasi** (oleh @monicafebyana-wq): https://github.com/monicafebyana-wq/DL-UTS-2026/pull/3
  Ringkasan: Menambahkan pembaruan akhir implementasi Task 2 (`prediksi_rul.csv`), Task 3 bagian spektrum, fusi multimodal, dan clustering (`cluster.csv`), serta pembaruan dokumen laporan dan `kontribusi.md`.
- **Komitmen langsung pada branch `main` dan Review PR** (oleh @monicafebyana-wq): Inisialisasi struktur repositori utama, implementasi awal Task 2 dan Task 3 bagian spektrum, serta peninjauan dan penggabungan (merge) PR dari kontributor.

## 3. Deklarasi Penggunaan AI Tools

Dalam pengerjaan tugas ini, kelompok kami menggunakan bantuan AI tools secara terbatas dan bertanggung jawab sesuai ketentuan akademik.

**AI Tools yang Digunakan:** ChatGPT dan Claude.

**Bagian yang Dibantu:**

- **Pemahaman konsep:** diskusi konseptual mengenai fusion multimodal (concat dan gated), modality dropout, domain shift antar-lini, contrastive learning untuk representasi gambar dan spektrum, serta metrik evaluasi (Macro-F1, skor asimetris RUL, silhouette).
- **Bantuan teknis pemrograman dan debugging:** membantu menyusun kerangka fungsi modular Python/PyTorch, memperbaiki error kode dan kompatibilitas library, serta mengecek kesesuaian notebook dengan rubrik penilaian.
- **Penulisan:** membantu perapihan struktur dan bahasa laporan dan `kontribusi.md`.

**Cara Kelompok Memverifikasi Output:**

- **Eksekusi dan pengujian mandiri:** seluruh kode yang disarankan AI tidak disalin mentah, melainkan dijalankan dan diuji pada dataset resmi dengan seed tetap (SEED = 42).
- **Validasi logika dan anti-leakage:** statistik preprocessing dihitung dari data latih saja, pembagian data diperiksa agar tidak ada irisan, dan seluruh keluaran CSV (`prediksi_klasifikasi.csv`, `prediksi_rul.csv`, `cluster.csv`) diperiksa bebas dari NaN/Inf dan sesuai format yang diminta.
- **Pemeriksaan konsistensi angka:** seluruh metrik, tabel, dan grafik di laporan dicocokkan langsung dengan keluaran eksekusi notebook final sehingga dapat direproduksi oleh setiap anggota kelompok.

## 4. Pernyataan Persetujuan Anggota

Kami menyatakan bahwa seluruh informasi pembagian peran, tautan kontribusi GitHub, dan deklarasi penggunaan AI tools di atas adalah benar, telah disetujui bersama oleh seluruh anggota kelompok, dan setiap anggota mampu menjelaskan serta mereproduksi seluruh hasil pekerjaan kelompok pada saat penilaian atau tanya jawab.

Disetujui oleh:

- Cheyza Amanda Syafira (101032300081)
- Monica Febyana (101032330068)
