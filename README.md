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
[![Video Demo](https://img.shields.io/badge/YouTube-Watch%20Demo-red?style=for-the-badge&logo=youtube)](https://youtu.be/lX2pPxVPRhI?si=KpANEHiTu4dy9GfB)

#### 1. Halaman Home (Katalog Motor)

Home Page
<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/21e5fc35-234b-4200-81e2-0dd072566276" />

- Hero section dengan CTA (Call-to-Action)
- Grid katalog motor dengan card design
- Search bar dan pagination

#### 2. Detail Motor

Detail Motor
<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/36cba521-b44d-4177-812a-a959f7e8c53a" />

- Gambar motor beresolusi tinggi
- Spesifikasi lengkap (merk, model, tahun, harga, transmisi, CC)
- Button "Beli Sekarang" (user) atau "Edit" (admin)
- Deskripsi detail motor

#### 3. Form Pembelian

Form Pembelian
<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/b70515d2-c32a-4073-bf3e-af65dade4c2c" />
<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/ce014bd1-8fdc-4395-b04a-e9741d9855f6" />

- Preview motor yang dibeli
- Form data pembeli (nama, telepon, alamat)
- Pilihan metode pembayaran (Cash/Kredit)
- Kalkulasi total harga real-time

#### 4. Riwayat Pembelian (User)

Riwayat User
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/06fb65e2-6009-46de-bd85-29ddf8da08e3" />

- Card view dengan status transaksi (Pending/Diproses/Selesai)
- Filter berdasarkan status
- Button detail transaksi

#### 5. Invoice / Bukti Transaksi

Invoice
<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/c65a89b7-c0a2-4f62-a218-b900d59ec295" />

- Header dealer profesional
- Detail lengkap motor dan pembeli
- Status transaksi dengan badge warna
- Print-friendly layout

#### 6. Admin - Manajemen Motor

Admin Motor
<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/be90dc95-987e-4958-949c-f2ba03fe5b22" />

- Tabel responsif dengan action buttons
- Quick search
- Pagination
- Button tambah motor baru

#### 7. Admin - Form Tambah/Edit Motor

Admin Form
<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/9415bedd-dbc6-49d5-b223-9d06d5b34c53" />

- Form lengkap dengan validasi
- Upload gambar dengan preview
- Input spesifikasi motor

#### 8. Admin - Manajemen Transaksi

Admin Transaksi
<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/be81c62a-b433-4e18-8f67-ef7ef96a3ccb" />

- Tabel semua transaksi
- Update status dengan modal
- Filter dan search transaksi
- Total revenue statistik

#### 9. Login & Register
![Auth Pages
<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/1e442da8-f08f-4ce8-8c0d-f9760f888448" />
<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/192b71eb-db59-4381-b6a8-e61558c12419" />
<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/ae7228bc-5b3d-4448-a754-d2fdd4f2b80c" />

- Form login dengan demo credentials
- Form register user baru
- Validation messages

#### 10. Mobile Responsive
Mobile View
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/800e35e0-e794-4dd9-8efd-5311c6734a29" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/42b75a03-6d5e-419f-979f-c39fe3526ca2" />

- Layout mobile-first
- Bottom navigation
- Touch-friendly buttons
