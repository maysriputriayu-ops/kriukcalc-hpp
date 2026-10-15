# KriukCalc Enterprise — Cost Accounting & Pricing System

Aplikasi web interaktif berbasis **Full Costing** untuk menghitung Harga Pokok Produksi (HPP), rendemen bahan mentah ke produk matang, simulasi harga jual multi-tier (Distributor, Reseller, Eceran/Marketplace), serta analisis Titik Impas (*Break-Even Point* / BEP) bagi IKM Snack & Keripik.

## Fitur Utama
- **Kalkulator Rendemen & Kuota Kemasan**: Menghitung penyusutan berat bahan mentah ke hasil matang berbumbu serta jumlah kemasan (*standing pouch*) layak jual setelah toleransi QC.
- **Template BOM Standar IKM**: Tersedia preset siap pakai untuk *Keripik Singkong Balado*, *Keripik Pisang Cokelat*, *Basreng Daun Jeruk*, *Jamur Crispy*, serta lembar kosong (*Blank Sheet*).
- **4 Tabel Komponen Biaya Lengkap**:
  1. Bahan Baku Utama, Minyak & Bumbu (*Direct Materials*)
  2. Kemasan Standing Pouch, Label & Karton (*Packaging*)
  3. Tenaga Kerja Langsung (*Direct Labor / BTKL*)
  4. Overhead Pabrik & Utilitas (*Manufacturing Overhead / BOP*) dilengkapi **Kalkulator Penyusutan Alat Produksi**.
- **Simulasi Harga Jual 3-Tier & Curah**: Kalkulasi otomatis harga & margin untuk Distributor, Reseller, dan Eceran/D2C (termasuk potongan admin Marketplace) serta harga jual curah per kg/bal.
- **Analisis BEP & Katalog SKU**: Proyeksi laba bersih bulanan, penyimpanan katalog produk di browser (`localStorage`), ekspor ke CSV (Excel), salin ringkasan teks, dan cetak laporan.

## Struktur Proyek
```text
├── index.html      # Aplikasi utama (Single-Page Application)
├── vercel.json     # Konfigurasi routing & header untuk Vercel
├── .gitignore      # Daftar file yang diabaikan Git
└── README.md       # Dokumentasi proyek & panduan deployment
```

## Cara Deploy ke GitHub & Vercel

### 1. Upload ke GitHub
1. Buat repository baru di [GitHub](https://github.com/new) (misalnya `kriukcalc-hpp`).
2. Upload file `index.html`, `vercel.json`, `.gitignore`, dan `README.md` ke repository tersebut (bisa langsung lewat tombol **Add file → Upload files** di web GitHub, atau menggunakan Git CLI):
   ```bash
   git init
   git add .
   git commit -m "Initial commit: KriukCalc Enterprise HPP System"
   git branch -M main
   git remote add origin https://github.com/<username-anda>/kriukcalc-hpp.git
   git push -u origin main
   ```

### 2. Deploy ke Vercel
1. Masuk ke dashboard [Vercel](https://vercel.com/new) menggunakan akun GitHub Anda.
2. Pada bagian **Import Git Repository**, pilih repository `kriukcalc-hpp` lalu klik **Import**.
3. Biarkan pengaturan default (**Framework Preset**: *Other*, **Root Directory**: `./`, **Build Command**: kosongkan).
4. Klik **Deploy**. Dalam beberapa detik aplikasi Anda akan aktif dengan domain `.vercel.app` dan otomatis ter-update setiap kali ada perubahan di branch `main` GitHub.
