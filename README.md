# ILZA Beauty — E-Commerce Portfolio

Website e-commerce demo yang menampilkan produk kecantikan (makeup & skincare) dengan fitur belanja lengkap, demo login, dan pembayaran simulasi.

## 📋 Daftar Fitur

### Core Features
- ✅ **Beranda (index.html)** — Landing page dengan featured products & hero section
- ✅ **Daftar Produk (produk.html)** — Katalog lengkap dengan toggle deskripsi per-produk
- ✅ **Keranjang Belanja (cart.html)** — Manajemen cart dengan qty, remove, clear, dan checkout
- ✅ **Demo Checkout** — Simulasi pembayaran dengan nomor pesanan sementara
- ✅ **Halaman Sukses (success.html)** — Tampilkan ringkasan order setelah checkout
- ✅ **Halaman Kontak (kontak.html)** — Form kontak dengan pesan sukses
- ✅ **Tentang Kami (tentang.html)** — Informasi perusahaan, visi & misi
- ✅ **Testimoni (testimoni.html)** — Review & rating dari pelanggan
- ✅ **Demo Login (login.html)** — Sistem autentikasi client-side
- ✅ **Admin Dashboard (admin.html)** — Halaman admin terlindungi

### Storage & State Management
- **localStorage** — Menyimpan keranjang belanja (`ilza_cart`)
- **sessionStorage** — Menyimpan session login (`ilza_logged_in`, `ilza_user`) dan order (`ilza_order`)

### UI/UX Enhancements
- 🎨 **Tema Maroon (#995656)** — Warna brand konsisten di seluruh halaman
- 📱 **Responsive Design** — Bootstrap 5.3.3 untuk mobile-first layout
- 🔄 **Sticky Navbar** — Navigasi selalu terlihat saat scroll
- 🎯 **Tombol Interaktif** — Feedback visual (toggle desc, add to cart, checkout)
- 💳 **Badge Cart Counter** — Real-time update jumlah item di keranjang

---

## 🚀 Cara Menggunakan

### Setup Lokal

1. **Clone atau download repository**
   ```bash
   git clone https://github.com/ainunhusnulsadiah-oss/ainunhusnulsadiah-oss.github.io.git
   cd ainunhusnulsadiah-oss/pertemuan\ 16
   ```

2. **Jalankan server lokal** (penting untuk localStorage/sessionStorage bekerja optimal)
   ```bash
   # Menggunakan Python 3
   python -m http.server 8000
   
   # Atau gunakan Python 2
   python -m SimpleHTTPServer 8000
   ```

3. **Buka browser** dan kunjungi:
   ```
   http://localhost:8000/index.html
   ```

### Skenario Demo

#### A) Berbelanja & Checkout
1. Buka `index.html` (Beranda)
2. Klik "Tambah ke Keranjang" pada produk pilihan
3. Buka `cart.html` (Keranjang) dari navbar
4. Lihat ringkasan, ubah jumlah jika perlu, lalu klik `Checkout`
5. Konfirmasi pembayaran → akan dialihkan ke `success.html` dengan ringkasan order

#### B) Login & Admin
1. Buka `login.html` dari navbar
2. Masukkan:
   - Username: `admin`
   - Password: `ilza123`
3. Klik `Login` → akan dialihkan ke `admin.html` (halaman admin terlindungi)
4. Klik `Logout` untuk keluar

#### C) Kontak
1. Buka `kontak.html` dari navbar
2. Isi form dengan nama, email, subject, dan pesan
3. Klik `Kirim Pesan` → akan muncul pesan sukses dan form direset

#### D) Eksplorasi Produk
1. Buka `produk.html` (Produk)
2. Klik `Tampilkan Deskripsi` untuk melihat detail produk
3. Klik `Tambah ke Keranjang` untuk memasukkan ke cart
4. Badge keranjang akan otomatis terupdate

---

## 🏗️ Struktur Proyek

```
pertemuan 16/
├── index.html          # Beranda dengan featured products
├── produk.html         # Katalog produk lengkap
├── cart.html           # Halaman keranjang belanja
├── success.html        # Halaman konfirmasi pembayaran
├── kontak.html         # Form kontak
├── tentang.html        # Tentang perusahaan
├── testimoni.html      # Review pelanggan
├── login.html          # Halaman login demo
├── admin.html          # Dashboard admin (terlindungi)
├── README.md           # Dokumentasi ini
└── assets/
    └── custom.css      # CSS custom tambahan (jika ada)
```

---

## 💾 Data & Storage

### localStorage
- **Key**: `ilza_cart`
- **Format**: JSON array
- **Struktur Item**:
  ```json
  {
    "id": "medicube-95000",
    "title": "MEDICUBE",
    "price": 95000,
    "qty": 2,
    "img": "produk 1.jpg"
  }
  ```

### sessionStorage
- **Key**: `ilza_logged_in` → nilai `'1'` jika login
- **Key**: `ilza_user` → username yang login
- **Key**: `ilza_order` → detail pesanan setelah checkout
  ```json
  {
    "id": "ORD123456",
    "items": [...],
    "total": 380000,
    "date": "2025-12-09T10:30:00Z"
  }
  ```

---

## 🔐 Keamanan (Demo)

⚠️ **Catatan Penting**:
- Login menggunakan hardcoded credentials (`admin` / `ilza123`) — hanya untuk demo client-side
- Checkout tidak melakukan pembayaran nyata — hanya simulasi
- Untuk produksi, gunakan:
  - Backend API dengan session management & JWT
  - Payment gateway terintegrasi (Stripe, Midtrans, dll)
  - Database untuk menyimpan order & user

---

## 📱 Responsive & Browser Support

- ✅ Desktop (1920px, 1366px, 1024px)
- ✅ Tablet (768px, 834px)
- ✅ Mobile (375px, 414px, 480px)
- ✅ Chrome, Firefox, Safari, Edge (versi terbaru)

---

## 🎨 Color Palette

| Warna | Kode | Penggunaan |
|-------|------|-----------|
| **Primary Maroon** | `#995656` | Navbar, tombol CTA, hover |
| **Primary Dark** | `#8e5151` | Hover state |
| **Secondary Salmon** | `#E68D8D` | Hero section, footer |
| **Text Dark** | `#333` | Body text |
| **Text Light** | `#fff` | White text on dark bg |
| **Background Light** | `#f7f7f7` | Subtle bg |

---

## 🛠️ Tech Stack

| Kategori | Teknologi |
|----------|-----------|
| **Frontend** | HTML5, CSS3, JavaScript (Vanilla) |
| **Framework** | Bootstrap 5.3.3 (CDN) |
| **Icons** | Font Awesome 6.5.2 (CDN) |
| **Storage** | localStorage, sessionStorage |
| **Version Control** | Git & GitHub |
| **Hosting** | GitHub Pages |

---

## 📊 Features Breakdown

### 1. Product Catalog (index.html & produk.html)
- Tampilkan produk dalam grid responsive
- Toggle deskripsi per-produk
- Harga dengan format Rupiah
- Tombol "Beli Sekarang" (link ke kontak)
- Tombol "Tambah ke Keranjang" (add to localStorage)

### 2. Shopping Cart (cart.html)
- Tampilkan list item dari `localStorage.ilza_cart`
- Update qty dengan tombol +/-
- Hapus item individual
- Kosongkan seluruh cart
- Hitung subtotal & total otomatis
- Tombol checkout → redirect ke success.html

### 3. Order Confirmation (success.html)
- Baca order dari `sessionStorage.ilza_order`
- Tampilkan nomor pesanan, tanggal, list item, total
- Tombol "Lanjut Belanja" (link ke index)

### 4. Contact Form (kontak.html)
- Input: Full Name, Email, Subject, Message
- Submit → show success alert + reset form
- Auto-hide alert setelah 5 detik

### 5. Login & Admin (login.html & admin.html)
- Login form dengan hardcoded creds
- Set sessionStorage untuk session tracking
- Admin page memeriksa sessionStorage untuk akses
- Logout button → clear session & redirect ke login

### 6. Navigation
- Sticky navbar di semua halaman
- Logo link ke home
- Menu items: Beranda, Tentang, Produk, Testimoni, Kontak, Login, Keranjang
- Cart badge menampilkan jumlah item real-time

---

## 🚢 Deployment (GitHub Pages)

Repo sudah terhubung dengan GitHub Pages:
- **URL**: https://ainunhusnulsadiah-oss.github.io/pertemuan%2016/index.html
- **Branch**: `master`
- **Auto-deploy**: Push ke master → auto-publish dalam 1-2 menit

### Push Changes
```bash
cd "d:\CLASS INDUSTRI 2025\pertemuan 16"
git add .
git commit -m "Feat: [deskripsi singkat]"
git push origin master
```

---

## 📝 Changelog

### v1.0.0 (2025-12-09)
- ✅ Struktur dasar e-commerce
- ✅ Keranjang belanja dengan localStorage
- ✅ Demo login & admin dashboard
- ✅ Form kontak dengan feedback
- ✅ Simulasi checkout & order success page
- ✅ Responsive design dengan Bootstrap
- ✅ Consistent maroon theme

---

## 🤝 Kontribusi & Pengembangan

Ide untuk fitur tambahan:
- [ ] Wishlist / Favorit produk
- [ ] Rating & review produk
- [ ] Search & filter produk (by category, price range)
- [ ] User profile & riwayat pembelian
- [ ] Coupon/discount code
- [ ] Payment gateway integration
- [ ] Email notification
- [ ] Admin panel untuk manage produk
- [ ] Dark mode toggle

---

## 📧 Kontak

- **Email**: [tanyakan ke pemilik]
- **WhatsApp**: +62 887-8XXXX
- **Instagram**: [@ilza.beauty]

---

## 📄 Lisensi

Proyek ini adalah portfolio/demo untuk tujuan pembelajaran dan presentasi.

---

**Happy Shopping! 🛍️**

Terakhir diupdate: 9 Desember 2025
