# Product Requirements Document (PRD)

## Sistem Informasi Penyewaan Peralatan Camping Berbasis Website dengan Manajemen Inventaris menggunakan QR-Code

|             |                       |
| ----------- | --------------------- |
| **Versi**   | 0.1 (Draft)           |
| **Tanggal** | 27 November 2026      |
| **Pembuat** | Randie Syaeful Azahli |
| **Status**  | Draft                 |

---

## 1. Ringkasan Produk

Sistem ini adalah aplikasi web untuk usaha rental alat camping skala kecil. Aplikasi ini menggabungkan katalog alat, booking online, pencatatan keuangan sederhana, dashboard terpusat untuk staf, dan pelacakan aset per unit menggunakan QR-Code.

Sistem ini menggantikan alur manual yang sekarang berjalan lewat story Instagram, WhatsApp, dan telepon, dengan satu platform terpusat yang mencatat stok, transaksi, DP, serah terima, pengembalian, serta pemasukan dan pengeluaran usaha secara akurat.

## 2. Latar Belakang & Masalah

Minat camping di Bandung dan sekitarnya (Lembang, Ciwidey, Bandung Selatan) mendorong tumbuhnya rental alat camping kecil. Mayoritas masih beroperasi konvensional:

- Promosi hanya lewat story Instagram atau grup WhatsApp yang bersifat sementara.
- Stok dan transaksi tidak terdigitalisasi.
- Pesanan masuk dari banyak kanal sekaligus, terutama saat long weekend dan libur semester.
- Serah terima dan pengembalian dicatat manual, sehingga rawan human error.
- Pemasukan dan pengeluaran tidak dicatat rapi, sehingga pemilik sulit mengetahui untung atau rugi yang sebenarnya.
- DP, pelunasan, denda keterlambatan, dan ganti rugi kerusakan tidak dipisahkan dengan jelas dalam pencatatan.
- Calon penyewa tidak dapat melihat pengalaman penyewa sebelumnya, padahal kepercayaan sangat menentukan keputusan menyewa.

### 2.1 Daftar Masalah

| ID  | Masalah                                                                         | Dampak                                                                              |
| --- | ------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| P1  | Promosi hanya lewat story Instagram yang bersifat sementara                     | Jangkauan calon penyewa terbatas                                                    |
| P2  | Ketersediaan alat sulit dipantau secara akurat dan terkini                      | Salah informasi stok saat musim ramai                                               |
| P3  | Pesanan dari banyak kanal sulit dikelola bersamaan                              | Pesanan terlewat atau tertukar                                                      |
| P4  | Tidak ada rekap otomatis pendapatan dan alat terlaris                           | Keputusan bisnis tanpa data                                                         |
| P5  | Penyewa tidak bisa cek ketersediaan tanpa bertanya ke pemilik                   | Friksi dan beban chat staf                                                          |
| P6  | Penyewa tidak tahu kondisi alat sebelum booking                                 | Kekecewaan dan sengketa                                                             |
| P7  | Booking manual via chat memicu dobel booking                                    | Konflik jadwal alat yang sama                                                       |
| P8  | Tidak ada bukti transaksi yang jelas                                            | Potensi sengketa                                                                    |
| P9  | DP dan pelunasan dicatat manual                                                 | Lupa menagih sisa pembayaran atau terjadi selisih                                   |
| P10 | Riwayat pelanggan tidak tercatat rapi                                           | Sulit memberi perlakuan khusus ke pelanggan tetap                                   |
| P11 | Serah terima dan pengembalian dicatat manual                                    | Human error dan memakan waktu                                                       |
| P12 | Kondisi dan riwayat per unit sulit dilacak                                      | Tidak ada jejak pemakaian individual                                                |
| P13 | Pemasukan dan pengeluaran usaha tidak tercatat rapi                             | Pemilik tidak tahu untung atau rugi yang sebenarnya                                 |
| P14 | Tidak ada laporan surplus/defisit                                               | Tidak ada dasar untuk mengevaluasi dan merencanakan usaha                           |
| P15 | Denda keterlambatan dan ganti rugi kerusakan tidak tercatat atau tidak tertagih | Pendapatan bocor, biaya ditanggung pemilik                                          |
| P16 | DP, pelunasan, denda, dan ganti rugi tidak dipisahkan dalam pencatatan          | Sulit melihat sewa yang sudah dibayar, sisa yang harus dilunasi, dan biaya tambahan |
| P17 | Biaya perawatan tidak tercatat per unit                                         | Tidak diketahui unit mana yang boros biaya                                          |
| P18 | Calon penyewa tidak punya referensi pengalaman penyewa lain                     | Kepercayaan sulit dibangun, keputusan menyewa ragu-ragu                             |

## 3. Tujuan Produk

| ID  | Tujuan                                                                 | Masalah yang dijawab |
| --- | ---------------------------------------------------------------------- | -------------------- |
| G1  | Status ketersediaan alat yang akurat dan terkini                       | P2, P5               |
| G2  | Semua pesanan terkumpul dalam satu dashboard                           | P3                   |
| G3  | Laporan pendapatan dan alat terlaris otomatis                          | P4                   |
| G4  | Booking online yang mencegah dobel booking                             | P7                   |
| G5  | Bukti transaksi digital (invoice)                                      | P8                   |
| G6  | Pencatatan status DP dan pelunasan yang transparan                     | P9                   |
| G7  | QR-Code per unit alat untuk pelacakan status dan riwayat               | P12                  |
| G8  | Serah terima dan pengembalian lewat scan QR-Code                       | P11                  |
| G9  | Katalog digital yang selalu dapat diakses                              | P1, P6               |
| G10 | Riwayat penyewaan per pelanggan                                        | P10                  |
| G11 | Pemasukan (sewa, denda, ganti rugi) tercatat otomatis dari transaksi   | P13, P15             |
| G12 | Pengeluaran tercatat per kategori                                      | P13                  |
| G13 | Laporan bulanan pemasukan, pengeluaran, dan surplus/defisit            | P14                  |
| G14 | Denda dan ganti rugi dicatat pada booking terkait                      | P15                  |
| G15 | DP, pelunasan, dan biaya tambahan (denda, ganti rugi) dicatat terpisah | P16                  |
| G16 | Biaya perawatan dan pendapatan per unit dapat dilihat                  | P17                  |
| G17 | Ulasan per alat dari penyewa yang benar-benar pernah menyewa           | P18                  |

## 4. Pengguna & Persona

### 4.1 Penyewa (Pengunjung)

Mahasiswa atau masyarakat urban yang membutuhkan alat camping untuk kegiatan outdoor. Kebutuhannya: cek ketersediaan sendiri, melihat kondisi alat sebelum booking, booking tanpa menunggu balasan chat, mendapat bukti transaksi serta kepastian status DP, dan membaca ulasan penyewa lain.

Kasir, petugas gudang, dan pemilik/manager toko disebut bersama sebagai **staf**. Pembagian hak akses ketiganya ada di bagian 6.12.

### 4.2 Kasir

Melayani penyewa di konter. Kebutuhannya: melihat pesanan masuk, menerima atau menolak booking, mengonfirmasi DP dan pelunasan, mencatat denda atau ganti rugi, menerima dan mengembalikan jaminan KTP, dan memutuskan pengajuan pembatalan.

### 4.3 Petugas Gudang

Mengelola alat fisik. Kebutuhannya: serah terima dan pengembalian yang cepat lewat scan QR-Code, pencatatan kondisi tiap unit, serta pengelolaan data alat dan unit.

### 4.4 Pemilik/Manager Toko

Penanggung jawab usaha. Kebutuhannya: mengawasi seluruh pesanan, mencatat pengeluaran, melihat laporan keuangan (surplus/defisit), mengelola akun staf, dan memiliki akses ke seluruh fitur.

### 4.5 Sistem (Layanan Pendukung)

Bukan aktor manusia. Sistem bertugas generate QR-Code, membaca QR lewat kamera, mengunci ketersediaan saat booking dibuat dan melepasnya saat booking dibatalkan, ditolak, atau tidak diproses kasir dalam 7 x 24 jam, serta merekap data transaksi.

## 5. Ruang Lingkup

### 5.1 Dalam Lingkup (MVP)

- Katalog alat dan booking online.
- Invoice digital serta pelacakan DP dan pelunasan.
- Dashboard staf: pesanan, inventaris, laporan.
- Generate, cetak, dan scan QR-Code per unit.
- Riwayat pemakaian per unit dan riwayat penyewaan per pelanggan.
- Pencatatan keuangan sederhana: pemasukan, pengeluaran, denda/ganti rugi, dan laporan surplus/defisit bulanan.
- Ulasan per alat dari penyewa (rating dan komentar singkat).
- Autentikasi staf dengan tiga peran tetap (kasir, petugas gudang, pemilik/manager) dan pembatasan hak akses per peran.

### 5.2 Di Luar Lingkup (Tahap Lanjutan)

| Item                                                   | Keterangan                                                                         |
| ------------------------------------------------------ | ---------------------------------------------------------------------------------- |
| Payment gateway otomatis                               | Misalnya Midtrans; pembayaran DP dan pelunasan online tanpa konfirmasi manual      |
| Notifikasi otomatis                                    | WhatsApp atau email, misalnya pengingat tenggat pengembalian                       |
| Multi-tenant                                           | Beberapa usaha rental dalam satu platform                                          |
| Face recognition / YOLO                                | Verifikasi identitas penyewa saat serah terima                                     |
| Laporan keuangan formal                                | Neraca (laporan posisi keuangan) dan catatan atas laporan keuangan sesuai SAK EMKM |
| Penyusutan aset dan EBIT                               | Membutuhkan keputusan metode penyusutan dan masa manfaat tiap alat                 |
| Perhitungan pajak, rekonsiliasi bank, jurnal akuntansi | Di luar kebutuhan pencatatan sederhana pada MVP                                    |
| Pengaturan hak akses kustom per pengguna               | Pada MVP hanya ada tiga peran tetap                                                |

Pada MVP, pembayaran DP dan pelunasan dikonfirmasi manual oleh kasir.

## 6. Requirements Fungsional

Prioritas: **P0** = wajib MVP, **P1** = penting, **P2** = nice-to-have.

### 6.1 Katalog Alat (FR-01)

| ID      | Requirement                                                                                                           | Prioritas |
| ------- | --------------------------------------------------------------------------------------------------------------------- | --------- |
| FR-01.1 | Penyewa dapat melihat daftar alat beserta foto, deskripsi, kondisi, kapasitas, dan harga sewa per hari                | P0        |
| FR-01.2 | Katalog dapat diakses tanpa login                                                                                     | P0        |
| FR-01.3 | Penyewa dapat mencari alat berdasarkan nama                                                                           | P0        |
| FR-01.4 | Penyewa dapat memfilter berdasarkan kategori (Tenda, Carrier & Tas, Memasak, Pendakian, dll.) dan status ketersediaan | P1        |
| FR-01.5 | Halaman detail alat menampilkan galeri foto, spesifikasi, dan kondisi                                                 | P0        |

### 6.2 Booking Online (FR-02)

| ID       | Requirement                                                                                                                                               | Prioritas |
| -------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- |
| FR-02.1  | Sistem menampilkan status ketersediaan alat (tersedia/tidak tersedia) untuk rentang tanggal yang dipilih penyewa, tanpa tampilan kalender                 | P0        |
| FR-02.2  | Penyewa memilih tanggal mulai dan selesai; sistem menghitung durasi dan total harga                                                                       | P0        |
| FR-02.3  | Penyewa yang sudah login dapat membuat booking tanpa menghubungi staf toko lewat chat                                                                     | P0        |
| FR-02.4  | Sistem mengunci ketersediaan alat saat booking dibuat sesuai BR-01, sehingga tidak ada dobel booking                                                      | P0        |
| FR-02.5  | Sistem menolak booking yang bentrok dengan jadwal yang sudah terkunci, termasuk saat dua permintaan masuk hampir bersamaan                                | P0        |
| FR-02.6  | Kasir (atau pemilik/manager) dapat menerima atau menolak booking sesuai BR-03 dan BR-08; booking yang ditolak melepas alat (BR-02)                        | P0        |
| FR-02.7  | Penyewa dapat membatalkan booking miliknya sendiri sesuai BR-04; alat yang terkunci langsung dilepas (BR-02)                                              | P0        |
| FR-02.8  | Penyewa dapat mengajukan pembatalan sesuai BR-04; kasir (atau pemilik/manager) menyetujui atau menolak pengajuan, dan alat dilepas bila disetujui (BR-02) | P0        |
| FR-02.9  | Sistem melepas otomatis booking yang belum diproses kasir sesuai BR-03 (status expired); alat kembali tersedia (BR-02)                                    | P0        |
| FR-02.10 | Halaman booking dan invoice memberi tahu penyewa bahwa KTP asli wajib dibawa saat serah terima (BR-10)                                                    | P1        |

### 6.3 Invoice & Bukti Transaksi (FR-03)

| ID      | Requirement                                                                                                                                               | Prioritas |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- |
| FR-03.1 | Setiap booking menghasilkan halaman konfirmasi atau invoice digital berisi rincian alat, tanggal sewa, harga, dan DP                                      | P0        |
| FR-03.2 | Penyewa dapat melihat kembali invoice dari riwayat booking                                                                                                | P0        |
| FR-03.3 | Invoice dapat dicetak atau diunduh                                                                                                                        | P2        |
| FR-03.4 | Setelah pengembalian, invoice diperbarui menjadi rincian akhir: biaya sewa, DP yang sudah dibayar, sisa pelunasan, serta denda atau ganti rugi (bila ada) | P1        |

### 6.4 Manajemen DP & Pelunasan (FR-04)

| ID      | Requirement                                                                                                                                                | Prioritas |
| ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- |
| FR-04.1 | Setiap booking memiliki status DP: belum dibayar, menunggu verifikasi, terkonfirmasi, dikembalikan                                                         | P0        |
| FR-04.2 | Kasir (atau pemilik/manager) dapat mengonfirmasi pembayaran DP dan mengubah status DP (BR-03, BR-08)                                                       | P0        |
| FR-04.3 | Penyewa dapat melihat status DP pada booking miliknya                                                                                                      | P0        |
| FR-04.4 | Sistem membedakan pembayaran DP (saat booking), pelunasan (saat pengembalian), dan pembayaran tambahan berupa denda atau ganti rugi sesuai BR-07 dan BR-09 | P0        |
| FR-04.5 | Setiap booking memiliki status pelunasan: belum lunas, lunas; kasir mengonfirmasi pelunasan saat pengembalian                                              | P0        |
| FR-04.6 | Penyewa dapat membayar DP sesuai BR-07                                                                                                                     | P0        |
| FR-04.7 | Penyewa dapat mengunggah bukti pembayaran DP; status DP menjadi menunggu verifikasi sampai kasir memeriksanya                                              | P1        |

### 6.5 Dashboard (FR-05)

| ID      | Requirement                                                                                                                                                            | Prioritas |
| ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------- |
| FR-05.1 | Staf melihat daftar seluruh pesanan masuk beserta statusnya (pending, accepted, active, returned, cancelled, rejected, cancel_requested, expired) dalam satu tampilan  | P0        |
| FR-05.2 | Dashboard menampilkan ringkasan: total pesanan dan alat sedang keluar (semua staf); pemasukan, pengeluaran, dan surplus/defisit bulan berjalan (hanya pemilik/manager) | P0        |
| FR-05.3 | Staf dapat melihat pesanan terbaru dan memfilter berdasarkan status                                                                                                    | P1        |

### 6.6 Manajemen Inventaris (FR-06)

| ID      | Requirement                                                                                                       | Prioritas |
| ------- | ----------------------------------------------------------------------------------------------------------------- | --------- |
| FR-06.1 | Petugas gudang dan pemilik/manager dapat menambah, mengubah, dan menghapus data alat (jenis/model)                | P0        |
| FR-06.2 | Petugas gudang dan pemilik/manager dapat mengelola unit fisik di bawah tiap alat (stok per unit, kondisi, status) | P0        |
| FR-06.3 | Status unit: tersedia, disewa, dikembalikan (dan kondisi terakhir)                                                | P0        |
| FR-06.4 | Petugas gudang dan pemilik/manager dapat mengunggah foto alat                                                     | P0        |

### 6.7 QR-Code per Unit (FR-07)

| ID      | Requirement                                                                                    | Prioritas |
| ------- | ---------------------------------------------------------------------------------------------- | --------- |
| FR-07.1 | Sistem menghasilkan QR-Code unik untuk setiap unit saat unit didaftarkan                       | P0        |
| FR-07.2 | Petugas gudang dan pemilik/manager dapat mencetak QR-Code untuk ditempelkan pada unit fisik    | P0        |
| FR-07.3 | Kode unit memiliki format terbaca manusia (contoh: `TENT-MSR-001`) sehingga bisa dicari manual | P0        |

### 6.8 Scan QR-Code: Serah Terima & Pengembalian (FR-08)

| ID      | Requirement                                                                                                                             | Prioritas |
| ------- | --------------------------------------------------------------------------------------------------------------------------------------- | --------- |
| FR-08.1 | Halaman scanner membaca QR-Code lewat kamera perangkat                                                                                  | P0        |
| FR-08.2 | Alternatif input manual ID unit bila kamera tidak tersedia atau QR rusak                                                                | P0        |
| FR-08.3 | Hasil scan menampilkan nama alat, ID unit, dan nama penyewa (order terkait)                                                             | P0        |
| FR-08.4 | Petugas gudang (atau pemilik/manager) dapat mengonfirmasi serah terima dan pengembalian; status unit dan order diperbarui otomatis      | P0        |
| FR-08.5 | Setiap scan tercatat sebagai event pada riwayat unit                                                                                    | P0        |
| FR-08.6 | Sistem menolak aksi yang tidak valid (mis. serah terima unit yang tidak terkait order, atau pengembalian unit yang tidak sedang disewa) | P1        |
| FR-08.7 | Sistem menolak serah terima yang melanggar BR-06                                                                                        | P1        |
| FR-08.8 | Kasir (atau pemilik/manager) mencatat penerimaan jaminan KTP sebelum serah terima dan pengembaliannya setelah pelunasan (BR-10)         | P0        |

### 6.9 Riwayat Pemakaian & Kondisi per Unit (FR-09)

| ID      | Requirement                                                                                    | Prioritas |
| ------- | ---------------------------------------------------------------------------------------------- | --------- |
| FR-09.1 | Staf dapat melihat riwayat pemakaian tiap unit (siapa, kapan, event serah terima/pengembalian) | P0        |
| FR-09.2 | Petugas gudang (atau pemilik/manager) dapat mencatat kondisi unit saat pengembalian            | P1        |

### 6.10 Laporan (FR-10)

| ID      | Requirement                                                                | Prioritas |
| ------- | -------------------------------------------------------------------------- | --------- |
| FR-10.1 | Laporan pendapatan harian dan bulanan dari catatan pemasukan (lihat FR-13) | P0        |
| FR-10.2 | Daftar alat terlaris (paling sering disewa) harian dan bulanan             | P0        |
| FR-10.3 | Ekspor laporan (CSV/PDF)                                                   | P2        |

### 6.11 Riwayat Penyewaan per Pelanggan (FR-11)

| ID      | Requirement                                                                                                    | Prioritas |
| ------- | -------------------------------------------------------------------------------------------------------------- | --------- |
| FR-11.1 | Sistem menyimpan riwayat transaksi tiap penyewa                                                                | P0        |
| FR-11.2 | Kasir dan pemilik/manager dapat melihat daftar pelanggan dan riwayatnya untuk mengidentifikasi pelanggan tetap | P1        |
| FR-11.3 | Penyewa dapat melihat riwayat penyewaannya sendiri                                                             | P0        |

### 6.12 Autentikasi & Hak Akses (FR-12)

| ID      | Requirement                                                                                                                  | Prioritas |
| ------- | ---------------------------------------------------------------------------------------------------------------------------- | --------- |
| FR-12.1 | Staf (kasir, petugas gudang, pemilik/manager) dapat login dan logout                                                         | P0        |
| FR-12.2 | Setiap akun staf memiliki tepat satu peran: kasir, petugas gudang, atau pemilik/manager                                      | P0        |
| FR-12.3 | Halaman dan aksi dashboard hanya dapat diakses sesuai matriks hak akses di bawah; akses di luar peran ditolak di sisi server | P0        |
| FR-12.4 | Pemilik/manager dapat menambah, menonaktifkan, dan menetapkan peran akun staf                                                | P0        |
| FR-12.5 | Penyewa wajib registrasi akun (nama, email, nomor WhatsApp, dan kata sandi) dan login sebelum membuat booking (BR-05)        | P0        |
| FR-12.6 | Penyewa dapat login, logout, dan mengatur ulang kata sandi                                                                   | P1        |

**Matriks hak akses (asumsi awal, lihat Open Question 6):**

| Fitur / Aksi                                                                               | Kasir | Petugas Gudang | Pemilik/Manager |
| ------------------------------------------------------------------------------------------ | :---: | :------------: | :-------------: |
| Melihat daftar dan detail pesanan                                                          |   ✓   |       ✓        |        ✓        |
| Menerima atau menolak booking, dan memutuskan pengajuan pembatalan (FR-02.6, FR-02.8)      |   ✓   |       –        |        ✓        |
| Mengonfirmasi DP dan pelunasan (FR-04)                                                     |   ✓   |       –        |        ✓        |
| Mencatat jaminan KTP, penerimaan dan pengembalian (FR-08.8)                                |   ✓   |       –        |        ✓        |
| Mencatat denda dan ganti rugi (FR-13.2)                                                    |   ✓   |       –        |        ✓        |
| Scan QR serah terima dan pengembalian (FR-08)                                              |   –   |       ✓        |        ✓        |
| Mencatat kondisi unit saat pengembalian (FR-09.2)                                          |   –   |       ✓        |        ✓        |
| Melihat riwayat pemakaian unit (FR-09.1)                                                   |   ✓   |       ✓        |        ✓        |
| Mengelola alat, unit, foto, dan mencetak QR (FR-06, FR-07)                                 |   –   |       ✓        |        ✓        |
| Melihat daftar pelanggan dan riwayatnya (FR-11.2)                                          |   ✓   |       –        |        ✓        |
| Mencatat dan mengubah pengeluaran (FR-13.3)                                                |   –   |       –        |        ✓        |
| Mencatat harga beli unit (FR-13.9)                                                         |   –   |       –        |        ✓        |
| Laporan pendapatan, alat terlaris, dan laporan keuangan (FR-10, FR-13.5, FR-13.6, FR-13.8) |   –   |       –        |        ✓        |
| Ringkasan keuangan di dashboard (FR-05.2)                                                  |   –   |       –        |        ✓        |
| Menyembunyikan ulasan (FR-14.6)                                                            |   –   |       –        |        ✓        |
| Mengelola akun staf (FR-12.4)                                                              |   –   |       –        |        ✓        |

### 6.13 Pencatatan Keuangan (FR-13)

Pencatatan sederhana atas uang yang benar-benar masuk dan keluar, untuk kebutuhan operasional pemilik. Bukan sistem akuntansi formal (lihat bagian 5.2).

Kategori pemasukan dan pengeluaran mengikuti BR-12.

| ID      | Requirement                                                                                                                                           | Prioritas |
| ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- | --------- |
| FR-13.1 | Pemasukan sewa tercatat otomatis dari booking sesuai BR-11                                                                                            | P0        |
| FR-13.2 | Kasir (atau pemilik/manager) dapat mencatat denda keterlambatan dan biaya ganti rugi kerusakan pada booking terkait; keduanya masuk sebagai pemasukan | P0        |
| FR-13.3 | Pemilik/manager dapat menambah, mengubah, dan menghapus catatan pengeluaran (tanggal, nominal, kategori, keterangan)                                  | P0        |
| FR-13.4 | Sistem mencatat DP, pelunasan, denda, dan ganti rugi sebagai pemasukan terpisah sesuai BR-11                                                          | P0        |
| FR-13.5 | Laporan bulanan menampilkan total pemasukan, total pengeluaran per kategori, dan surplus/defisit (hanya dapat dilihat pemilik/manager)                | P0        |
| FR-13.6 | Laporan menampilkan total DP dari booking yang belum dikembalikan sebagai informasi terpisah                                                          | P1        |
| FR-13.7 | Pengeluaran perawatan/perbaikan dapat dikaitkan ke unit tertentu                                                                                      | P1        |
| FR-13.8 | Detail unit menampilkan total biaya perawatan dan total pendapatan sewa unit tersebut (hanya terlihat oleh pemilik/manager)                           | P1        |
| FR-13.9 | Pemilik/manager dapat mencatat harga beli per unit                                                                                                    | P1        |

### 6.14 Ulasan Alat (FR-14)

Ulasan melekat pada jenis alat (bukan unit fisik) dan bersifat opsional per alat.

| ID      | Requirement                                                                                                    | Prioritas |
| ------- | -------------------------------------------------------------------------------------------------------------- | --------- |
| FR-14.1 | Penyewa dapat memberi ulasan untuk alat yang ia sewa sesuai BR-15                                              | P1        |
| FR-14.2 | Ulasan opsional per alat; penyewa memilih alat mana yang ingin diulas                                          | P1        |
| FR-14.3 | Sistem membatasi satu ulasan per alat per booking (BR-15)                                                      | P1        |
| FR-14.4 | Ulasan berisi rating 1 sampai 5 dan komentar singkat                                                           | P1        |
| FR-14.5 | Halaman detail alat menampilkan rating rata-rata dan daftar ulasan; kartu katalog menampilkan rating rata-rata | P1        |
| FR-14.6 | Pemilik/manager dapat menyembunyikan ulasan yang tidak pantas                                                  | P1        |

## 7. Alur Utama (User Flow)

### 7.1 Booking oleh Penyewa

1. Penyewa membuka katalog, mencari atau memfilter alat.
2. Penyewa membuka detail alat.
3. Penyewa memilih tanggal; sistem menghitung durasi dan total harga.
4. Penyewa melakukan booking (jika belum login, diminta registrasi atau login terlebih dahulu); sistem memvalidasi ketersediaan dan langsung mengunci alat; booking berstatus pending.
5. Sistem menampilkan konfirmasi dan invoice digital.
6. Penyewa membayar DP, saat membuat booking atau setelahnya, dan dapat mengunggah bukti pembayaran.
7. Kasir memeriksa pembayaran DP, lalu menerima atau menolak booking dalam 7 x 24 jam sejak booking dibuat; DP yang terkonfirmasi tercatat sebagai pemasukan sewa.
8. Penyewa dapat membatalkan booking sendiri dalam 6 jam setelah dibuat; setelah itu penyewa mengajukan pembatalan yang diputuskan kasir.
9. Jika booking dibatalkan, ditolak, atau tidak diproses kasir dalam 7 x 24 jam (expired), alat yang terkunci dilepas dan kembali tersedia.

### 7.2 Serah Terima

1. Penyewa datang mengambil alat.
2. Kasir menerima KTP penyewa sebagai jaminan dan mencatatnya.
3. Petugas gudang membuka halaman QR Scan dan memindai QR pada unit.
4. Sistem menampilkan alat, ID unit, dan penyewa terkait.
5. Petugas gudang menekan _Konfirmasi Serah Terima_; status unit menjadi **disewa**, order menjadi **active**, event tercatat di riwayat unit.

### 7.3 Pengembalian

1. Penyewa mengembalikan alat.
2. Petugas gudang memindai QR unit dan menekan _Konfirmasi Pengembalian_.
3. Petugas gudang mencatat kondisi unit; status unit menjadi **tersedia/dikembalikan**, order menjadi **returned**.
4. Jika ada keterlambatan atau kerusakan, kasir mencatat denda atau ganti rugi pada booking tersebut.
5. Penyewa membayar pelunasan (total sewa dikurangi DP) dan pembayaran tambahan berupa denda atau ganti rugi, bila ada; kasir mengonfirmasi pembayaran dan pemasukan tercatat.
6. Setelah pembayaran selesai, kasir mengembalikan KTP jaminan dan mencatat pengembaliannya.

### 7.4 Pencatatan Pengeluaran & Laporan Bulanan

1. Pemilik/manager mencatat pengeluaran (perawatan, pembelian alat, operasional) lengkap dengan kategori; untuk perawatan, dapat memilih unit terkait.
2. Pemilik/manager membuka laporan bulanan untuk melihat total pemasukan, pengeluaran per kategori, dan surplus/defisit.

### 7.5 Memberi Ulasan

1. Setelah booking berstatus **returned**, penyewa membuka riwayat booking miliknya.
2. Penyewa memilih alat yang ingin diulas, lalu mengisi rating 1 sampai 5 dan komentar singkat.
3. Ulasan tampil di halaman detail alat dan memperbarui rating rata-rata.
4. Pemilik/manager dapat menyembunyikan ulasan yang tidak pantas.

## 8. Model Data (Konseptual)

| Entitas             | Atribut utama                                                                                                                | Relasi                                          |
| ------------------- | ---------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------- |
| **User**            | id, nama, email, role (kasir/petugas_gudang/pemilik_manager/penyewa), kontak, aktif                                          | punya banyak Booking                            |
| **Category**        | id, nama                                                                                                                     | punya banyak Equipment                          |
| **Equipment**       | id, category_id, nama, deskripsi, kapasitas, harga_per_hari, foto                                                            | punya banyak Unit, Review                       |
| **EquipmentUnit**   | id, equipment_id, kode_unit (unik), qr_payload, status, kondisi, harga_beli (opsional)                                       | punya banyak UnitEvent, FinancialRecord         |
| **Booking**         | id, user_id, tanggal_mulai, tanggal_selesai, total_harga, status, status_pelunasan, invoice_no, dibuat_pada                  | punya banyak BookingItem, satu DP, satu Jaminan |
| **BookingItem**     | id, booking_id, equipment_id, unit_id (nullable sampai serah terima), qty, harga                                             | milik Booking; punya satu Review (opsional)     |
| **DP**              | id, booking_id, jumlah, bukti_pembayaran (opsional), status (belum dibayar/menunggu verifikasi/terkonfirmasi/dikembalikan)   | milik Booking                                   |
| **Jaminan**         | id, booking_id, jenis (KTP), status (diterima/dikembalikan), waktu_diterima, waktu_dikembalikan, staf_id                     | milik Booking                                   |
| **UnitEvent**       | id, unit_id, booking_id, tipe (handover/return), kondisi, catatan, waktu, staf_id                                            | milik EquipmentUnit                             |
| **FinancialRecord** | id, tipe (pemasukan/pengeluaran), kategori, nominal, tanggal, keterangan, booking_id (nullable), unit_id (nullable), staf_id | opsional milik Booking dan EquipmentUnit        |
| **Review**          | id, booking_item_id (unik), equipment_id, user_id, rating (1–5), komentar, disembunyikan (boolean), waktu                    | milik BookingItem dan Equipment                 |

Aturan data penting:

- `kode_unit` harus unik dan stabil karena dicetak di QR.
- Pengecekan bentrok jadwal dilakukan di level database/transaksi, bukan hanya di UI.
- Satu BookingItem hanya punya satu Review (batasan data untuk BR-15).
- Aturan bisnis yang memengaruhi data (status booking, pencatatan keuangan, ulasan) ada di bagian 11.

## 9. Requirements Non-Fungsional

| ID     | Kategori           | Requirement                                                                                                                                                                                                   |
| ------ | ------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| NFR-01 | Integritas data    | Tidak boleh terjadi dobel booking pada alat dan rentang tanggal yang sama, termasuk saat akses konkuren                                                                                                       |
| NFR-02 | Keamanan           | Rute staf dilindungi autentikasi dan otorisasi berbasis peran (kasir, petugas gudang, pemilik/manager); hak akses diperiksa di sisi server, bukan hanya disembunyikan di tampilan; input divalidasi di server |
| NFR-03 | Usability          | Antarmuka user-friendly; alur booking dan scan dapat diselesaikan tanpa pelatihan khusus                                                                                                                      |
| NFR-04 | Responsif          | Katalog, booking, dan scanner dapat dipakai di ponsel; scanner untuk petugas gudang harus ramah perangkat mobile                                                                                              |
| NFR-05 | Akurasi            | Scan QR memperbarui status unit dengan benar; diuji dalam skenario uji akurasi scan                                                                                                                           |
| NFR-06 | Performa           | Halaman katalog dan dashboard termuat dalam waktu wajar pada koneksi seluler umum                                                                                                                             |
| NFR-07 | Ketersediaan data  | Status ketersediaan selalu mencerminkan data terbaru setelah booking, pembatalan, penolakan, kedaluwarsa, dan scan                                                                                            |
| NFR-08 | Dokumentasi        | Tersedia panduan instalasi dan penggunaan                                                                                                                                                                     |
| NFR-09 | Akurasi nilai uang | Nominal disimpan dengan tipe yang akurat (bukan floating point) agar total laporan tidak meleset                                                                                                              |

## 10. Rekomendasi Stack Teknis

Proposal belum menetapkan teknologi. Berikut rekomendasi stack yang dapat disesuaikan:

| Lapisan           | Pilihan                                                                        |
| ----------------- | ------------------------------------------------------------------------------ |
| Backend           | Laravel (Eloquent, Fortify untuk autentikasi)                                  |
| Frontend          | Inertia.js + React + TypeScript                                                |
| Styling/UI        | Tailwind CSS v4 + shadcn/ui                                                    |
| Routing type-safe | Laravel Wayfinder                                                              |
| Validasi          | Zod (frontend), Form Request (backend)                                         |
| Database          | MySQL/PostgreSQL                                                               |
| QR generate       | Library generator QR sisi server atau klien                                    |
| QR scan           | Library scanner berbasis kamera di browser, plus input manual sebagai fallback |

Prinsip: gunakan solusi paling sederhana yang cukup untuk MVP, tanpa abstraksi berlebih. Tipe data dijaga ketat lewat TypeScript.

## 11. Aturan Bisnis

Aturan bisnis adalah kebijakan usaha yang menentukan kapan dan bagaimana fungsi sistem boleh dipakai. Requirements fungsional (bagian 6) merujuk ke aturan ini dengan kode BR. Jika sebuah aturan berubah (misalnya batas 6 jam), cukup ubah di sini.

### 11.1 Booking dan Ketersediaan

| ID    | Aturan                                                                                                                                                                           |
| ----- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BR-01 | Alat terkunci saat booking dibuat, tanpa menunggu pembayaran. Satu alat tidak dapat dibooking dua kali pada rentang tanggal yang bentrok.                                        |
| BR-02 | Alat yang terkunci dilepas dan kembali tersedia jika booking dibatalkan, ditolak, atau expired.                                                                                  |
| BR-03 | Kasir (atau pemilik/manager) memiliki waktu 7 x 24 jam sejak booking dibuat untuk menerima atau menolak booking. Booking yang belum diproses dalam waktu itu berstatus expired.  |
| BR-04 | Penyewa dapat membatalkan booking sendiri dalam 6 jam sejak booking dibuat. Setelah itu penyewa hanya dapat mengajukan pembatalan, yang diputuskan kasir (atau pemilik/manager). |
| BR-05 | Penyewa wajib memiliki akun dan login untuk membuat booking. Katalog dapat dilihat tanpa login.                                                                                  |
| BR-06 | Serah terima hanya dapat dilakukan untuk booking berstatus accepted dan setelah KTP jaminan diterima.                                                                            |

### 11.2 Pembayaran dan Keuangan

| ID    | Aturan                                                                                                                                                                                                                                                                                                                                    |
| ----- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BR-07 | Saat booking hanya DP (uang muka, sebagian dari biaya sewa) yang dibayar. DP dapat dibayar saat membuat booking atau setelahnya, selama booking masih berstatus pending.                                                                                                                                                                  |
| BR-08 | Kasir memeriksa pembayaran DP sebelum menerima atau menolak booking.                                                                                                                                                                                                                                                                      |
| BR-09 | Pelunasan adalah total biaya sewa dikurangi DP, dibayar saat pengembalian dan dikonfirmasi kasir. Denda keterlambatan dan ganti rugi kerusakan (bila ada) menjadi pembayaran tambahan di luar pelunasan.                                                                                                                                  |
| BR-10 | Penyewa wajib membawa KTP asli dan menyerahkannya sebagai jaminan saat serah terima; tanpa KTP, serah terima tidak dapat dilakukan. KTP dikembalikan saat pengembalian, setelah pelunasan dan pembayaran tambahan (bila ada) selesai. Sistem hanya mencatat status KTP (diterima atau dikembalikan), tanpa menyimpan foto atau nomor KTP. |
| BR-11 | Pemasukan sewa dicatat sebesar DP saat DP dikonfirmasi, dan sebesar sisa pelunasan saat pelunasan dikonfirmasi. Denda dan ganti rugi dicatat sebagai pemasukan tambahan pada booking terkait saat dibayar.                                                                                                                                |
| BR-12 | Kategori pemasukan: sewa, denda keterlambatan, ganti rugi kerusakan. Kategori pengeluaran: perawatan/perbaikan, pembelian alat, operasional, lainnya.                                                                                                                                                                                     |
| BR-13 | Pendapatan dan surplus/defisit dihitung dari catatan keuangan (FinancialRecord). Alat terlaris dihitung dari booking berstatus returned.                                                                                                                                                                                                  |
| BR-14 | DP dibayar lewat transfer manual dengan unggah bukti pembayaran. Pelunasan dan pembayaran tambahan dibayar saat pengembalian, secara tunai atau transfer di toko. Semuanya dikonfirmasi kasir; MVP tidak memakai payment gateway.                                                                                                         |

### 11.3 Ulasan dan Hak Akses

| ID    | Aturan                                                                                                                                                            |
| ----- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| BR-15 | Ulasan hanya dapat dibuat setelah booking berstatus returned. Satu alat dalam satu booking hanya boleh diulas satu kali (rating 1 sampai 5 dan komentar singkat). |
| BR-16 | Rating rata-rata alat dihitung dari ulasan yang tidak disembunyikan.                                                                                              |
| BR-17 | Setiap staf memiliki tepat satu peran, dan hak aksesnya mengikuti matriks di bagian 6.12.                                                                         |

### 11.4 Status Booking

| Status           | Arti                                                                        |
| ---------------- | --------------------------------------------------------------------------- |
| pending          | Booking dibuat, alat terkunci; menunggu pembayaran DP dan pemeriksaan kasir |
| accepted         | Diterima kasir, DP terkonfirmasi; siap diambil                              |
| active           | Serah terima sudah dilakukan; alat sedang disewa                            |
| returned         | Alat sudah dikembalikan                                                     |
| cancelled        | Dibatalkan penyewa dalam 6 jam, atau pengajuan pembatalan disetujui         |
| cancel_requested | Penyewa mengajukan pembatalan setelah 6 jam; menunggu keputusan kasir       |
| rejected         | Ditolak kasir                                                               |
| expired          | Tidak diproses kasir dalam 7 x 24 jam                                       |

## 12. Open Questions

Hal-hal yang belum dijelaskan di proposal dan perlu diputuskan sebelum atau selama implementasi:

1. **Penentuan unit saat booking:** booking dibuat per jenis alat (qty), lalu unit fisik ditetapkan saat serah terima lewat scan? Model data di atas mengasumsikan demikian.
2. **Kebijakan DP:** berapa besarnya (persentase dari total sewa atau nominal tetap)? Bagaimana tarif denda keterlambatan dan penentuan nominal ganti rugi kerusakan?
3. **Pembatalan dan perubahan booking:** aturan dasar sudah ditetapkan (penyewa membatalkan sendiri dalam 6 jam, setelahnya lewat pengajuan). Belum ditentukan: siapa yang memutuskan pengajuan (kasir atau pemilik/manager), apakah DP dikembalikan penuh saat booking dibatalkan, dan apakah booking boleh diubah (tanggal atau alat) tanpa dibatalkan.
4. **Keterlambatan pengembalian:** belum ada aturan denda atau status "terlambat".
5. **Mockup menampilkan kolom dan menu tambahan** (Customers, Settings, tombol "Tambah ke Tas", harga spesial). Perlu diputuskan mana yang masuk MVP.
6. **Hak akses per peran:** matriks di bagian 6.12 adalah asumsi awal (mis. pengeluaran dan laporan keuangan hanya untuk pemilik/manager; kasir tidak mengelola inventaris). Perlu dikonfirmasi, termasuk apakah kasir boleh mencatat pengeluaran operasional kecil dan apakah petugas gudang perlu melihat ringkasan pesanan.
7. **DP yang sudah dibayar tetapi booking kedaluwarsa:** jika penyewa sudah membayar DP tetapi kasir tidak memproses dalam 7 x 24 jam, bagaimana perlakuan uang DP tersebut (dikembalikan otomatis, atau kasir wajib menyelesaikannya secara manual)?

## 13. Kriteria Keberhasilan

- Seluruh fitur P0 pada bagian 6 berfungsi dan terintegrasi.
- Uji fungsi booking: tidak ada dobel booking pada skenario uji, termasuk dua permintaan hampir bersamaan.
- Uji akurasi scan: scan QR memperbarui status unit dan riwayat dengan benar pada skenario serah terima dan pengembalian.
- Dashboard menampilkan rekap pesanan, laporan pendapatan, alat terlaris, dan riwayat per unit.
- Laporan bulanan menampilkan total pemasukan, pengeluaran per kategori, dan surplus/defisit yang sesuai dengan data uji; DP, pelunasan, denda, dan ganti rugi tercatat terpisah dengan jumlah yang benar.
- Hak akses sesuai peran terverifikasi: kasir dan petugas gudang tidak dapat membuka laporan keuangan atau mengubah catatan pengeluaran, dan akses ditolak di sisi server.
- Ulasan hanya dapat dibuat setelah booking berstatus returned, dan rating rata-rata tampil benar di halaman detail alat dan katalog.
- Dokumentasi teknis (panduan instalasi dan penggunaan) dan laporan akhir PKL tersedia.

## 14. Target Output

1. Aplikasi web sistem penyewaan alat camping berbasis QR-Code (katalog, booking online, pengelolaan inventaris) yang fungsional.
2. Dashboard staf dengan hak akses per peran: rekap pesanan, laporan pendapatan, alat terlaris, riwayat pemakaian dan kondisi per unit, serta laporan keuangan bulanan (pemasukan, pengeluaran, surplus/defisit).
3. Dokumentasi teknis (instalasi dan penggunaan).
4. Laporan akhir PKL.

## 15. Pengembangan Tahap Lanjutan (Roadmap)

1. Integrasi payment gateway (Midtrans) untuk DP dan pelunasan.
2. Notifikasi dan pengingat otomatis via WhatsApp/email.
3. Multi-tenant untuk beberapa usaha rental dalam satu platform.
4. Face recognition atau object detection (YOLO) untuk verifikasi identitas penyewa.
5. Laporan keuangan formal sesuai SAK EMKM (neraca dan catatan atas laporan keuangan), penyusutan aset, dan EBIT.
