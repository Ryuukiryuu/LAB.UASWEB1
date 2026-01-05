#  Sistem Informasi Penjualan Motor (Dealer Online)

![PHP](https://img.shields.io/badge/PHP-7.4+-777BB4?style=flat&logo=php&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-8.0+-4479A1?style=flat&logo=mysql&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-5.3-7952B3?style=flat&logo=bootstrap&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green.svg)

> Project UAS Pemrograman Web - Aplikasi dealer motor berbasis web dengan fitur CRUD, pencarian, pagination, sistem transaksi, dan multi-role authentication.

##  Daftar Isi

- [Tentang Project](#-tentang-project)
- [Fitur Utama](#-fitur-utama)
- [Demo & Screenshot](#-demo--screenshot)
- [Teknologi](#-teknologi)
- [Instalasi](#-instalasi)
- [Struktur Database](#-struktur-database)
- [Struktur Project](#-struktur-project)
- [Cara Penggunaan](#-cara-penggunaan)
- [API Endpoints](#-api-endpoints)
- [Testing](#-testing)
- [Dokumentasi Tambahan](#-dokumentasi-tambahan)
- [Author](#-author)
- [Lisensi](#-lisensi)

---

##  Tentang Project

**Dealer Motor Online** adalah aplikasi web untuk manajemen penjualan motor yang dibangun menggunakan PHP Native dengan arsitektur MVC (Model-View-Controller) dan konsep OOP (Object-Oriented Programming). Aplikasi ini memiliki dua role utama: **Admin** untuk mengelola data motor dan transaksi, serta **User** untuk melihat katalog dan melakukan pembelian motor.

###  Informasi Akademik
- **Nama**: Wahyu Andika
- **Nim**: 312410182
- **Mata Kuliah**: Pemrograman Web 1
- **Jenis**: Project UAS
- **Dosen Pengampu**: [Nama Dosen]

---

##  Fitur Utama

###  Admin Panel
-  **CRUD Motor Lengkap** - Create, Read, Update, Delete data motor
-  **Upload & Manage Gambar** - Kelola gambar motor dengan preview
-  **Manajemen Transaksi** - Lihat dan kelola semua transaksi
-  **Update Status Transaksi** - Pending → Diproses → Selesai → Dibatalkan
-  **Dashboard Statistik** - (Coming soon) Overview penjualan dan stok
-  **Search & Filter Motor** - Cari motor berdasarkan merk/model
-  **Pagination** - Tampilan data per halaman untuk performa optimal

###  User Panel
-  **Katalog Motor Responsive** - Tampilan grid modern dengan Bootstrap 5
-  **Detail Motor Lengkap** - Spesifikasi, harga, dan gambar detail
-  **Sistem Pembelian** - Form pembelian dengan validasi
-  **Riwayat Transaksi** - Lihat semua pembelian dengan status real-time
-  **Print Invoice** - Cetak bukti transaksi dalam format PDF
-  **Search Motor** - Pencarian cepat berdasarkan keyword
-  **Filter Harga** - (Coming soon) Filter berdasarkan range harga

###  Autentikasi & Keamanan
-  **Multi-Role System** - Admin dan User dengan hak akses berbeda
-  **Password Hashing** - Enkripsi password dengan bcrypt
-  **Session Management** - Manajemen sesi login yang aman
-  **CSRF Protection** - Proteksi dari Cross-Site Request Forgery
-  **SQL Injection Prevention** - Prepared statements dengan PDO
-  **XSS Protection** - Sanitasi input dengan htmlspecialchars

###  UI/UX
-  **Responsive Design** - Mobile-first approach dengan Bootstrap 5
-  **Clean URL** - SEO-friendly URLs dengan .htaccess routing
-  **Loading States** - Feedback visual untuk user experience
-  **Alert Notifications** - Success/error messages yang informatif
-  **Print-Friendly** - Invoice dapat dicetak dengan layout khusus

---

##  Demo & Screenshot

###  Video Demo
[![Video Demo](https://img.shields.io/badge/YouTube-Watch%20Demo-red?style=for-the-badge&logo=youtube)](https://youtube.com/your-demo-link)

#### 1. Halaman Home (Katalog Motor)
![Home Page](screenshots/home.png)
- Hero section dengan CTA (Call-to-Action)
- Grid katalog motor dengan card design
- Search bar dan pagination

#### 2. Detail Motor
![Detail Motor](screenshots/detail.png)
- Gambar motor beresolusi tinggi
- Spesifikasi lengkap (merk, model, tahun, harga, transmisi, CC)
- Button "Beli Sekarang" (user) atau "Edit" (admin)
- Deskripsi detail motor

#### 3. Form Pembelian
![Form Pembelian](screenshots/form-beli.png)
- Preview motor yang dibeli
- Form data pembeli (nama, telepon, alamat)
- Pilihan metode pembayaran (Cash/Kredit)
- Kalkulasi total harga real-time

#### 4. Riwayat Pembelian (User)
![Riwayat User](screenshots/riwayat-user.png)
- Card view dengan status transaksi (Pending/Diproses/Selesai)
- Filter berdasarkan status
- Button detail transaksi

#### 5. Invoice / Bukti Transaksi
![Invoice](screenshots/invoice.png)
- Header dealer profesional
- Detail lengkap motor dan pembeli
- Status transaksi dengan badge warna
- Print-friendly layout

#### 6. Admin - Manajemen Motor
![Admin Motor](screenshots/admin-motor.png)
- Tabel responsif dengan action buttons
- Quick search
- Pagination
- Button tambah motor baru

#### 7. Admin - Form Tambah/Edit Motor
![Admin Form](screenshots/admin-form.png)
- Form lengkap dengan validasi
- Upload gambar dengan preview
- Input spesifikasi motor

#### 8. Admin - Manajemen Transaksi
![Admin Transaksi](screenshots/admin-transaksi.png)
- Tabel semua transaksi
- Update status dengan modal
- Filter dan search transaksi
- Total revenue statistik

#### 9. Login & Register
![Auth Pages](screenshots/auth.png)
- Form login dengan demo credentials
- Form register user baru
- Validation messages

#### 10. Mobile Responsive
![Mobile View](screenshots/mobile.png)
- Layout mobile-first
- Bottom navigation
- Touch-friendly buttons
---

###  Untuk User (Pembeli)

#### 1. Register & Login
```
1. Buka http://localhost/dealer-motor/
2. Klik "Register" di navbar
3. Isi form registrasi (username, email, password, nama lengkap)
4. Setelah berhasil, login dengan credentials yang dibuat
```

#### 2. Melihat Katalog Motor
```
1. Setelah login, lihat halaman home
2. Gunakan search bar untuk cari motor
3. Klik "Detail" pada motor yang diminati
```

#### 3. Membeli Motor
```
1. Di halaman detail motor, klik "Beli Sekarang"
2. Isi form pembelian:
   - Jumlah motor (max sesuai stok)
   - Nama pembeli (auto-fill dari profile)
   - No. telepon
   - Alamat lengkap
   - Metode pembayaran (Cash/Kredit)
   - Catatan (opsional)
3. Cek total harga (otomatis dihitung)
4. Klik "Konfirmasi Pembelian"
5. Transaksi berhasil, dapat kode transaksi
```

#### 4. Melihat Riwayat Pembelian
```
1. Klik "Riwayat Pembelian" di navbar
2. Lihat semua transaksi dengan status:
   - Pending (menunggu konfirmasi)
   - Diproses (sedang diproses admin)
   - Selesai (transaksi selesai)
   - Dibatalkan (dibatalkan)
3. Klik "Lihat Detail" untuk invoice lengkap
```

#### 5. Cetak Invoice
```
1. Buka detail transaksi
2. Klik "Cetak / Download PDF"
3. Browser akan buka print dialog
4. Pilih "Save as PDF" atau "Microsoft Print to PDF"
5. PDF tersimpan tanpa navbar dan tombol
```

---

###  Untuk Admin

#### 1. Login Admin
```
Username: admin
Password: password

Setelah login, akan redirect ke admin panel
```

#### 2. Manajemen Motor (CRUD)

**Create (Tambah Motor)**
```
1. Klik "Manajemen Motor" di navbar
2. Klik tombol "Tambah Motor"
3. Isi form:
   - Merk (Honda, Yamaha, Suzuki, dll)
   - Model (Vario 160, NMAX, dll)
   - Tahun (2000-2030)
   - Harga (dalam rupiah)
   - Stok (jumlah unit)
   - Warna
   - Transmisi (Manual/Matic)
   - Kapasitas mesin (cc)
   - Upload gambar (JPG/PNG, max 2MB)
   - Deskripsi lengkap
4. Klik "Simpan"
5. Motor baru muncul di katalog
```

**Read (Lihat Motor)**
```
1. Di halaman admin motor, lihat tabel semua motor
2. Ada thumbnail gambar, merk/model, tahun, harga, stok
3. Gunakan search untuk cari motor spesifik
4. Navigasi dengan pagination
```

**Update (Edit Motor)**
```
1. Klik tombol "Edit" (icon pensil) pada motor
2. Form akan terisi dengan data motor
3. Ubah data yang diperlukan
4. Upload gambar baru (opsional)
5. Klik "Update"
6. Motor ter-update di database
```

**Delete (Hapus Motor)**
```
1. Klik tombol "Delete" (icon trash) pada motor
2. Konfirmasi penghapusan
3. Motor dan gambarnya terhapus dari sistem
```

#### 3. Manajemen Transaksi

**Lihat Semua Transaksi**
```
1. Klik "Transaksi" di navbar
2. Lihat tabel semua transaksi dari semua user
3. Info yang ditampilkan:
   - Kode transaksi
   - Tanggal
   - Nama pembeli
   - Motor yang dibeli
   - Jumlah & total harga
   - Status transaksi
```

**Update Status Transaksi**
```
1. Klik tombol "Edit" (icon pensil) pada transaksi
2. Modal akan muncul
3. Pilih status baru:
   - Pending → Diproses (admin mulai proses)
   - Diproses → Selesai (motor sudah dikirim)
   - Any → Dibatalkan (jika ada masalah)
4. Klik "Update"
5. Status ter-update, user akan lihat di riwayat
```

**Lihat Detail Transaksi**
```
1. Klik tombol "Detail" (icon eye)
2. Lihat invoice lengkap dengan:
   - Data motor & gambar
   - Data pembeli lengkap
   - Info user (nama, email)
   - Status transaksi
3. Bisa cetak untuk arsip
```
