# 📖 Panduan Penggunaan Instagram Relationship Checker

Panduan langkah demi langkah untuk mengunduh data resmi Instagram dari Meta dan menggunakannya di aplikasi **Instagram Relationship Checker**.

---

## 📑 Daftar Isi
- [Cara Mengunduh Data JSON dari Instagram](#-cara-mengunduh-data-json-dari-instagram)
- [Cara Jalankan & Gunakan Aplikasi](#-cara-jalankan--gunakan-aplikasi)
- [Pertanyaan yang Sering Diajukan (FAQ)](#-pertanyaan-yang-sering-diajukan-faq)

---

## 📥 Cara Mengunduh Data JSON dari Instagram

Untuk menjaga privasi dan keamanan akun Anda, aplikasi ini tidak meminta *login* atau *password*. Sebagai gantinya, aplikasi menggunakan data resmi yang Anda unduh dari Meta.

### Langkah-langkah:

1. Buka aplikasi **Instagram** di HP atau akses [Instagram Web](https://www.instagram.com/).
2. Buka **Profil Anda** &rarr; ketuk **Menu (Ikon 3 Garis)** di kanan atas.
3. Masuk ke **Pusat Akun** (*Meta Accounts Center*).
4. Pilih **Informasi dan Izin Anda** (*Your Information and Permissions*).
5. Klik **Unduh Informasi Anda** (*Download Your Information*) &rarr; **Minta Unduhan** (*Request Download*).
6. Pilih **Sebagian Informasi** (*Select Types of Information*).
7. Gulir ke bawah dan centang opsi **Pengikut dan Mengikuti** (*Followers and Following*), lalu klik **Berikutnya**.
8. Atur parameter file sebagai berikut:
   - **Format**: Pilih `JSON` *(Wajib JSON, jangan pilih HTML)*.
   - **Kualitas Media**: Rendah *(opsional, agar file cepat siap)*.
   - **Rentang Waktu**: Pilih `Semua Waktu` (*All Time*).
9. Klik **Kirim Permintaan** (*Submit Request*).
10. Tunggu notifikasi atau email dari Meta (biasanya memakan waktu 5–15 menit).
11. Setelah siap, unduh file `.zip` tersebut dan **ekstrak di komputer/HP Anda**.
12. Buka folder hasil ekstraksi, lalu temukan dua file utama:
    - `followers_1.json` *(Lokasi: `connections/followers_and_following/`)*
    - `following.json` *(Lokasi: `connections/followers_and_following/`)*

---

## 🚀 Cara Jalankan & Gunakan Aplikasi

### Menjalankan Secara Lokal:
1. Buka file `index.html` dengan mengklik ganda (*double click*) file tersebut di komputer Anda. File akan terbuka otomatis di web browser (Chrome, Edge, Firefox, Safari, dll).
2. Pada form yang tersedia:
   - Unggah file `followers_1.json` pada kolom ke-1.
   - Unggah file `following.json` pada kolom ke-2.
3. Klik tombol **Proses & Bandingkan Data**.
4. Hasil analisis relasi akun Anda akan langsung ditampilkan dalam tabel.

### Menggunakan Fitur Aplikasi:
- **Tab Kategori**:
  - `Tidak Follow Back`: Menampilkan akun yang Anda ikuti tetapi tidak mengikuti balik Anda.
  - `Belum Anda Follow Back`: Menampilkan akun yang mengikuti Anda tetapi belum Anda ikuti balik.
- **Pencarian**: Gunakan *search bar* di bagian atas tabel untuk mencari *username* tertentu.
- **Sorting**: Klik menu *dropdown* urutan untuk memfilter data berdasarkan waktu (*Terbaru/Terlama*) atau alfabet (*A-Z / Z-A*).
- **Aksi Profil**: Klik tombol **Buka Profil ↗** pada baris tabel untuk langsung diarahkan ke profil Instagram akun yang bersangkutan.

---

## ❓ Pertanyaan yang Sering Diajukan (FAQ)

<details>
<summary><b>Apakah akun saya aman dari banned/block?</b></summary>
<b>100% Aman.</b> Aplikasi ini diproses sepenuhnya secara <i>client-side</i> (di dalam browser lokal Anda). Tidak ada koneksi API otomatis ke server Instagram dan tidak membutuhkan cookie/sessionid, sehingga tidak akan pernah memicu proteksi bot/spam dari Instagram.
</details>

<details>
<summary><b>Apakah data saya diunggah ke server lain?</b></summary>
<b>Tidak.</b> File JSON dibaca menggunakan API <code>FileReader</code> native browser di komputer Anda. Data tidak pernah dikirim ke internet, cloud, atau server mana pun.
</details>

<details>
<summary><b>Kenapa hasil pemrosesan menampilkan 0 data?</b></summary>
Pastikan file yang Anda unggah berformat <code>.json</code> (bukan <code>.html</code>) dan diambil dari rentang waktu unduhan "Semua Waktu" agar datanya lengkap.
</details>