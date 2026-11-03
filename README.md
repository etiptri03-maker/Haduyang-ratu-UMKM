[README.md](https://github.com/user-attachments/files/34311841/README.md)
# Haduyang Ratu Market — Marketplace Produk Desa (MVP)

Aplikasi web MVP interaktif, responsif, dan siap demo untuk platform perdagangan komoditas desa yang dikelola oleh **BUMDes Desa Haduyang Ratu, Kabupaten Lampung Utara**.

Dibangun berdasarkan dokumen spesifikasi **Product Requirements Document (PRD) v1.0**.

---

## 🌾 Panduan Membuka & Menjalankan Aplikasi

Aplikasi ini dirancang *zero-install* dan *self-contained*:
1. Buka file [index.html](file:///d:/Kuis_eti%20putri%20astuti/index.html) langsung dengan mengklik dua kali (*double click*) di file explorer, atau buka melalui browser apa saja (Google Chrome, Microsoft Edge, Firefox).
2. Anda juga dapat menjalankannya melalui ekstensi *Live Server* di VS Code / Antigravity jika diinginkan.
3. Seluruh data transaksi, mutasi stok barang, dan profil penjual tersimpan secara persisten di **LocalStorage** browser.

---

## ⚡ Fitur Utama (Berdasarkan PRD MVP P0)

### 1. Floating Role-Switcher (Demo Bar Bawah Layar)
Beralih peran secara instan dengan 1-klik untuk mengevaluasi seluruh perspektif pengguna:
- **Pembeli:** Ibu Rina (Konsumen Desa & Pelaku Kuliner)
- **Penjual:** Pak Arif (Petani Kebun Dusun 1 Haduyang Ratu)
- **Admin:** Pengelola BUMDes Haduyang Ratu
- **Tombol Reset:** Kembalikan data uji coba ke setelan awal pabrik kapan saja.

### 2. Sisi Pembeli (Buyer Experience)
- **Katalog & Kategori:** Hasil Pertanian, Sayuran Segar, Makanan Olahan Desa, dan Kerajinan UMKM.
- **Pencarian & Filter:** Live search nama produk, filter kategori, dan rentang harga.
- **Validasi Stok Real-Time:** Kuantitas pesanan tidak dapat melebihi stok yang ada. Jika stok habis, tombol dinonaktifkan otomatis.
- **Keranjang & Checkout:**
  - Pilihan metode: **Ambil Mandiri di Toko** atau **Antar Desa ke Rumah**.
  - *Price Snapshot:* Harga terkunci saat transaksi disimpan.
  - Nomor pesanan unik berformat `HDR-YYYYMMDD-XXX`.
- **Riwayat & Lacak Pesanan:** Timeline status (*Menunggu Konfirmasi ➜ Diproses ➜ Siap Diambil/Dikirim ➜ Selesai*).
- **Pembatalan:** Pembeli dapat membatalkan pesanan yang masih berstatus menunggu konfirmasi.

### 3. Sisi Penjual (Pak Arif - Kebun Dusun 1)
- **Dashboard Omzet & Statistik:** Total penjualan berstatus selesai, badge notifikasi pesanan baru, dan jumlah produk aktif.
- **Manajemen Pesanan:**
  - Terima dan siapkan panen.
  - Tolak pesanan dengan modal input alasan wajib (sesuai FR-06).
  - Tandai pesanan siap diambil/dikirim dan konfirmasi penyelesaian.
- **Manajemen Produk (CRUD):** Tambah komoditas baru lengkap dengan foto, satuan, harga, dan stok awal; edit cepat stok; serta toggle aktif/nonaktif.

### 4. Sisi Admin BUMDes (Supervisi & Governance)
- **Monitoring GMV:** Menampilkan akumulasi Gross Merchandise Value dan total volume transaksi.
- **Visualisasi Komposisi:** Grafik estimasi volume komoditas unggulan desa.
- **Ekspor CSV:** Unduh berkas laporan transaksi lengkap (`.csv`) yang memuat rincian pembeli, item, dan total transaksi.
- **Cetak Struk:** Pratinjau dan pencetakan struk transaksi resmi BUMDes.
- **Moderasi Katalog:** Admin berhak menyembunyikan/menonaktifkan produk yang melanggar kebijakan.
- **Audit Log:** Pencatatan otomatis setiap tindakan administratif dan transaksi.

---

## 📦 Data Awal (Seed Data)
- **Mitra Penjual:** Kebun Pak Arif (Dusun 1), Dapur Olahan Bu Darmi (Dusun 3), Kopi Barokah Lampung (Dusun 2).
- **Komoditas Awal:** Pisang Cavendish Haduyang, Kopi Robusta Sangrai Lampung, Keripik Pisang Cokelat, Sayur Bayam Organik, Cabai Rawit Merah, Telur Ayam Kampung, Madu Hutan Liar, Besek Bambu.
- **Contoh Transaksi:** 4 sampel pesanan dengan berbagai status (Pending, Processing, Completed) untuk mempermudah demonstrasi.
