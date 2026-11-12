# Kasku

Pencatat keuangan pribadi berbasis PWA. Data tersimpan di perangkat (localStorage), bisa diekspor/diimpor sebagai JSON, dan jalan offline.

Status: **Tahap 5**. Dompet, kategori, pencatatan transaksi, daftar per bulan, analisis (peringkat kategori, tren 6 bulan), dan budget per kategori sudah jalan. Goal tabungan serta hutang dan piutang juga sudah jalan. Tahap 5 menambah pencarian, filter, dan ekspor CSV.

## Pasang ke GitHub Pages

1. Buat akun di github.com dan aktifkan 2FA.
2. Klik **New repository**, beri nama (mis. `kasku`), pilih **Public**, lalu **Create repository**.
3. Di halaman repo klik **uploading an existing file**, seret **isi folder ini** (semua file, tanpa folder), lalu **Commit changes**.
4. Buka **Settings > Pages**. Pada *Build and deployment*, pilih **Deploy from a branch**, branch **main**, folder **/ (root)**, lalu **Save**.
5. Tunggu 1 sampai 2 menit. Alamatnya: `https://NAMA-AKUN.github.io/kasku/`.
6. Buka alamat itu di Chrome Android, ketuk menu ⋮, lalu **Instal aplikasi** (atau tombol **Pasang** di Pengaturan).

## Penting

- Jangan pernah mengunggah file ekspor cadangan (`kasku-cadangan-*.json`) ke repo. Isinya data keuanganmu.
- Update aplikasi: unggah ulang file yang berubah. Versi baru muncul setelah aplikasi dibuka dua kali.
- Data hilang jika kamu membersihkan data browser. Ekspor cadangan secara berkala.

## Struktur data (skema v1)

`wallets`, `categories`, `transactions`, `budgets`, `goals`, `debts`, ditambah `meta` dan `settings`. Detail field ada di komentar fungsi `fresh()` pada `index.html`.
