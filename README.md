<p align="center">
  <img src="https://img.shields.io/badge/Mahkamah%20Agung%20RI-Direktori%20Putusan-8B0000?style=for-the-badge&logo=scales&logoColor=white" alt="Mahkamah Agung RI">
  <img src="https://img.shields.io/badge/Pengadilan%20Negeri-PN%20Bengkalis-1F4E79?style=for-the-badge" alt="PN Bengkalis">
  <img src="https://img.shields.io/badge/Klasifikasi-Pidana%20Khusus%20Narkotika-0D6E6E?style=for-the-badge" alt="Narkotika">
</p>

<h1 align="center">⚖️ Dataset Putusan Pengadilan Negeri Bengkalis — Tindak Pidana Khusus Narkotika & Psikotropika (2024–2025)</h1>

<p align="center">
  <strong>Korpus Terbuka 50 Dokumen Putusan Pengadilan & Ringkasan Metadata Terstruktur untuk Domain Temu Kembali Informasi (Information Retrieval)</strong>
</p>

<p align="center">
  <a href="#tentang-dataset"><img src="https://img.shields.io/badge/Dokumen_PDF-50_Putusan-success?style=flat-square" alt="50 Putusan"></a>
  <a href="#statistik-korpus"><img src="https://img.shields.io/badge/Total_Halaman-1477_Halaman-blue?style=flat-square" alt="Total Halaman"></a>
  <a href="#kepatuhan-ketentuan-akuisi"><img src="https://img.shields.io/badge/Status_Putusan-Non_BHT_(Belum_Inkracht)-orange?style=flat-square" alt="Non BHT"></a>
  <a href="#struktur-repositori"><img src="https://img.shields.io/badge/Format-PDF_%26_XLSX-informational?style=flat-square" alt="Format"></a>
  <a href="#lisensi--keterbukaan-data"><img src="https://img.shields.io/badge/Lisensi-Open_Public_Legal_Document-brightgreen?style=flat-square" alt="Open Data"></a>
</p>

<p align="center">
  <a href="#tentang-dataset">Tentang Dataset</a> •
  <a href="#identitas-pengembang">Identitas</a> •
  <a href="#struktur-repositori">Struktur Direktori</a> •
  <a href="#spesifikasi--kepatuhan-akuisisi">Spesifikasi Akuisisi</a> •
  <a href="#skema-metadata-overviewxlsx">Skema Metadata</a> •
  <a href="#statistik-korpus">Statistik Korpus</a> •
  <a href="#katalog-lengkap-50-putusan">Katalog 50 Putusan</a> •
  <a href="#panduan-penggunaan-untuk-information-retrieval">Panduan Penggunaan</a>
</p>

---

## Tentang Dataset

Repositori **Dataset-Narkotika_023** menyediakan korpus terkurasi yang terdiri atas **50 dokumen putusan pengadilan tingkat pertama** dalam format asli (`*.pdf`) beserta rekapitulasi metadata dan ekstraksi entitas hukum terstruktur (`Overview/Overview.xlsx`). Seluruh dokumen diakuisisi dari **Direktori Putusan Mahkamah Agung Republik Indonesia** pada satuan kerja **Pengadilan Negeri Bengkalis (`PN Bengkalis`)** untuk direktori **Pidana Khusus** dengan klasifikasi **Narkotika dan Psikotropika**.

Dokumen putusan pengadilan merupakan sumber pengetahuan hukum terbuka (*open legal knowledge*) yang tidak terikat pembatasan Hak atas Kekayaan Intelektual (HaKI) sebagaimana diatur dalam **SK KMA Nomor 1-144/KMA/SK/I/2011** tentang Pedoman Pelayanan Informasi di Pengadilan. Dataset ini dirancang khusus untuk mendukung penelitian dan pengembangan sistem **Temu Kembali Informasi (*Information Retrieval* / TKI)**, meliputi:

- **Pengindeksan & Pencarian Teks Hukum (*Legal Document Indexing & Retrieval*)**: Pembangunan *inverted index*, pembobotan TF-IDF / BM25, serta *dense vector retrieval* pada naskah putusan pidana khusus.
- **Ekstraksi Informasi Hukum (*Legal Information Extraction*)**: Ekstraksi otomatis nomor putusan, barang bukti narkotika (jenis zat, jumlah paket, berat bersih/kotor, alat bukti komunikasi/transportasi), serta amar putusan (tuntutan pasal, pidana penjara, pidana denda, dan subsider).
- **Analisis Putusan & Prediksi Vonis (*Legal Judgment Analysis*)**: Pemodelan keterkaitan antara kuantitas/jenis barang bukti narkotika dengan lamanya pidana penjara dan besaran denda yang dijatuhkan majelis hakim.

---

## Identitas Pengembang

Dataset ini disusun untuk memenuhi **Ujian Tengah Semester (UTS) Ganjil 2026/2027** pada mata kuliah **Temu Kembali Informasi (TKI)**, Program Studi Informatika, Fakultas Teknik, **Universitas Muhammadiyah Malang (UMM)**:

| Komponen | Keterangan |
| :--- | :--- |
| **Mata Kuliah** | Temu Kembali Informasi (TKI) / *Information Retrieval* |
| **Dosen Pengampu** | Galih W. W |
| **Semester / Kelas** | Ganjil 2026/2027 — Semester 7 / Kelas A, D |
| **Nama & NIM Anggota 1** | **Muhammad Althof Taqiyyuddin** (`202310370311023`) |
| **Lembaga Peradilan Terpilih** | **Pengadilan Negeri Bengkalis (`PN Bengkalis`)** |
| **Kode Repositori** | `Dataset-Narkotika_023` |

---

## Struktur Repositori

Susunan direktori pada repositori ini mengikuti standar struktur penugasan UTS Temu Kembali Informasi:

```text
Dataset-Narkotika_023/
├── Dataset/
│   └── Narkotika.zip          # Arsip ZIP berisi 50 dokumen putusan asli berformat *.pdf
├── Overview/
│   └── Overview.xlsx          # Rekapitulasi terstruktur 50 putusan (No, No Putusan, Lembaga Peradilan, Barang Bukti, Amar Putusan)
└── README.md                  # Dokumentasi lengkap arsitektur, skema, dan katalog dataset
```

---

## Spesifikasi & Kepatuhan Akuisisi

Proses akuisisi dan kurasi data pada repositori ini telah diverifikasi terhadap seluruh ketentuan teknis penugasan:

1. **Sumber Resmi**: Seluruh dokumen diunduh dari portal resmi [Direktori Putusan Mahkamah Agung RI](https://putusan3.mahkamahagung.go.id/direktori/index/pengadilan/pn-bengkalis/kategori/narkotika-dan-psikotropika-1.html).
2. **Direktori & Klasifikasi**: Berasal dari direktori **Pidana Khusus** dengan sub-klasifikasi **Narkotika dan Psikotropika**.
3. **Satuan Kerja Pengadilan Negeri**: Seluruh 50 putusan berasal dari satu Pengadilan Negeri yang konsisten, yaitu **Pengadilan Negeri Bengkalis (`PN Bengkalis`)** (kode perkara `/Pid.Sus/2024/PN Bls` dan `/Pid.Sus/2025/PN Bls`).
4. **Rentang Tahun Putusan**: Berada dalam rentang tahun rekomendasi **2023 – 2025** (mencakup putusan tahun **2024** dan **2025**).
5. **Status Hukum Putusan**: **Tidak menggunakan putusan dengan status `BERKEKUATAN HUKUM TETAP`** (seluruh 50 dokumen telah diverifikasi tidak berlabel *Berkekuatan Hukum Tetap* pada metadata Direktori Putusan MA RI).
6. **Integritas Berkas PDF**: Seluruh 50 berkas `*.pdf` di dalam `Dataset/Narkotika.zip` telah melalui validasi *header* `%PDF-1.4` dan pemeriksaan keterbacaan teks per halaman.

---

## Skema Metadata (`Overview/Overview.xlsx`)

Berkas `Overview/Overview.xlsx` memuat tabel ringkasan 50 putusan dengan struktur 5 kolom standar:

| Kolom | Nama Atribut | Tipe Data | Deskripsi & Aturan Ekstraksi |
| :---: | :--- | :---: | :--- |
| **A** | `No` | Integer (`1–50`) | Nomor urut indeks dokumen di dalam dataset (berkorespondensi dengan prefiks nama file PDF di dalam `Narkotika.zip`). |
| **B** | `No Putusan` | String | Nomor registrasi perkara resmi pada Pengadilan Negeri Bengkalis (contoh: `450/Pid.Sus/2025/PN Bls`). |
| **C** | `Lembaga Peradilan` | String | Nama satuan kerja pengadilan tingkat pertama yang memutus perkara (`PN Bengkalis`). |
| **D** | `Barang Bukti` | Multiline Text | Daftar rinci barang bukti yang ditetapkan dalam amar putusan (jenis narkotika seperti sabu/ganja/ekstasi, jumlah paket/plastik klip, berat kotor/bersih dalam gram, timbangan digital, telepon genggam, maupun kendaraan). |
| **E** | `Amar Putusan` | Multiline Text | Bunyi lengkap diktum `MENGADILI` pada putusan: pernyataan kesalahan terdakwa beserta kualifikasi tindak pidana, masa pidana penjara, besaran pidana denda dan subsider kurungan, pengurangan masa tahanan, penetapan status barang bukti, serta pembebanan biaya perkara. |

### Contoh Cuplikan Isi `Overview/Overview.xlsx` (3 Data Pertama)

| No | No Putusan | Lembaga Peradilan | Barang Bukti | Amar Putusan |
|:--:|:-----------|:-----------------:|:-------------|:-------------|
| 1 | `450/Pid.Sus/2025/PN Bls` | PN Bengkalis | 1 (satu) paket narkotika jenis shabu yang terbungkus dalam plastik klep warna bening dan dibungkus kembali dengan 1 (satu) buah plastic klep warna bening;<br>1 (satu) buah plastic asoy warna hitam;<br>1 (satu) Unit Sepeda motor merk Suzuki ARASHI warna putih kombinasi hitam dengan Nomor Polisi BM 2124 XE dengan Nomor Rangka : MH8BF44WA6J118891 dan Nomor Mesin : P481-IDII8772;<br>1 (satu) unit Handphone merk OPPO A16 warna hitam dengan nomor IMEI (slot 1) : 866653056784712, IMEI (slot 2) : 866653056784704 dan Simcard Telkomsel terpasang 081371180664; | Menyatakan Terdakwa Suhendra Alias Indra Bin Mahsum telah terbukti secara sah dan meyakinkan bersalah melakukan tindak pidana ?Tanpa hak atau melawan hukum Menjadi Perantara Dalam Jual Beli Narkotika Golongan I bukan tanaman yang beratnya lebih dari 5 gram? sebagaimana dalam dakwaan Primer Penuntut Umum;<br>Menjatuhkan pidana kepada Terdakwa dengan pidana penjara selama 10(Sepuluh) tahun dan denda sejumlah Rp1.000.000.000,00(Satu Milyar Rupiah) dengan ketentuan apabila denda tersebut tidak dibayar diganti dengan pidana penjara selama 3(Tiga) bulan;<br>Menetapkan masa penangkapan dan penahanan yang telah dijalani Terdakwa dikurangkan seluruhnya dari pidana yang dijatuhkan;<br>Menetapkan Terdakwa tetap berada di dalam tahanan;<br>Menetapkan barang bukti berupa:<br>1 (satu) paket narkotika jenis shabu yang terbungkus dalam plastik klep warna bening dan dibungkus kembali dengan 1 (satu) buah plastic klep warna bening;<br>1 (satu) buah plastic asoy warna hitam;<br>dirampas untuk dimusnahkan<br>1 (satu) Unit Sepeda motor merk Suzuki ARASHI warna putih kombinasi hitam dengan Nomor Polisi BM 2124 XE dengan Nomor Rangka : MH8BF44WA6J118891 dan Nomor Mesin : P481-IDII8772;<br>1 (satu) unit Handphone merk OPPO A16 warna hitam dengan nomor IMEI (slot 1) : 866653056784712, IMEI (slot 2) : 866653056784704 dan Simcard Telkomsel terpasang 081371180664;<br>Dirampas untuk Negara<br>Membebankan kepada Terdakwa untuk membayar biaya perkara sebesar Rp5.000,00 (lima ribu rupiah); |
| 2 | `449/Pid.Sus/2025/PN Bls` | PN Bengkalis | 1 (Satu) Paket kecil Narkotika Jenis Sabu dalam Plastik Klep Warna Bening dengan berat bersih 0.10 gram;<br>2 (dua) Buah Mancis;<br>1 (Satu) Buah Kotak Rokok Merk OFO;<br>1 (Satu) Unit Hp Merk Xiaomi Redmi 5A warna gold;<br>1 (Satu) Unit Sepeda Motor merk Yamaha Vixion warna biru tanpa no.Pol; | Menyatakan Terdakwa Dedi Karmadi Alias Dedi Bin Isroi tidak terbukti melakukan tindak pidana sebagaimana dalam Dakwaan Primer Penuntut Umum;<br>Membebaskan Terdakwa oleh karena itu dari dakwaan primer Penuntut Umum tersebut;<br>Menyatakan Terdakwa Dedi Karmadi Alias Dedi Bin Isroi terbukti secara sah dan meyakinkan bersalah melakukan tindak pidana ?tanpa hak M enguasai Narkotika Golongan I bukan tanaman ? sebagaimana dalam Dakwaan subsidair Penuntut Umum;<br>Menjatuhkan pidana terhadap Terdakwa oleh karena itu dengan pidana penjara selama 5 (lima) tahun dan denda sejumlah Rp1.000.000.000,00 (satu miliar rupiah), apabila denda tidak dibayar maka diganti dengan pidana penjara selama 3 (tiga) bulan;<br>Menetapkan masa penangkapan dan penahanan yang telah dijalani oleh Terdakwa dikurangkan seluruhnya dari pidana yang dijatuhkan;<br>Menetapkan Terdakwa tetap ditahan;<br>Menyatakan agar barang bukti berupa :<br>1 (Satu) Paket kecil Narkotika Jenis Sabu dalam Plastik Klep Warna Bening dengan berat bersih 0.10 gram;<br>2 (dua) Buah Mancis;<br>1 (Satu) Buah Kotak Rokok Merk OFO;<br>Dirampas untuk dimusnahkan;<br>1 (Satu) Unit Hp Merk Xiaomi Redmi 5A warna gold;<br>1 (Satu) Unit Sepeda Motor merk Yamaha Vixion warna biru tanpa no.Pol;<br>Dirampas untuk Negara;<br>Membebankan kepada Terdakwa untuk membayar biaya perkara sejumlah Rp 5.000,00 (lima ribu rupiah); |
| 3 | `422/Pid.Sus/2025/PN Bls` | PN Bengkalis | 1 (satu) unit handphone merk Oppo warna hijau dengan nomor Imei 1 861536030196001 dan Imei 2 861536030196019;<br>2 (dua) buah mancis gas;<br>Uang hasil penjualan kepada Sdra SUDIRMAN Sebanyak Rp. 400.000 (Empat Ratus Ribu Rupiah);<br>3 (tiga) paket plastik klip yang berisikan narkotika jenis shabu-shabu dengan berat bersih 0,98 Gram;<br>1 (Satu) Unit HP Merk Infinix Hot511 Warna Hijau Dengan Nomor Imei 1 359955090521248 Dan Imei 2 359955090521255;<br>2 (Dua) Alat Hisap Sabu/Bong Lengkap Dengan Kaca Pirex;<br>2 (Dua) Tutup Botol Bekas Alat Hisap Sabu;<br>1 (Satu) Gunting Pres Warna Putih;<br>111 (Seratus Sebelas) Plastik Bening Berukuran Sedang;<br>2 (Dua) Buah Mancis Gas;<br>2 (Dua) Buah Mancis Gas;<br>2 (Dua) Buah Sendok Terbuat Dari Stiker;<br>Uang hasil penjualan kepada Sdra SUDIRMAN Sebanyak Rp. 400.000 (empat ratus ribu rupiah);<br>Dikembalikan kepada Penuntut Umum untuk dipergunakan pada berkas perkara atas nama saudara Adom;<br>6. Membebankan kepada Terdakwa membayar biaya perkara sejumlah Rp5.000,00 (lima ribu rupiah); | Menyatakan Terdakwa SUDIRMAN telah terbukti secara sah dan meyakinkan bersalah melakukan tindak pidana ?percobaan tanpa hak dan melawan hukum menjual Narkotika Golongan I bukan tanaman;<br>Menjatuhkan pidana kepada Terdakwa oleh karena itu dengan pidana penjara selama 7 (tujuh) tahun 6 (enam) bulan dan pidana denda sejumlah Rp1.000.000.000,00 (satu milyar rupiah) dengan ketentuan apabila pidana denda tersebut tidak dibayar diganti dengan pidana penjara selama 4 (empat) bulan ;<br>Menetapkan masa penangkapan dan penahanan yang telah dijalani Terdakwa dikurangkan seluruhnya dari pidana yang dijatuhkan;<br>Menetapkan Terdakwa tetap berada dalam tahanan;<br>Memerintahkan barang bukti berupa:<br>1 (satu) unit handphone merk Oppo warna hijau dengan nomor Imei 1 861536030196001 dan Imei 2 861536030196019;<br>2 (dua) buah mancis gas;<br>Uang hasil penjualan kepada Sdra SUDIRMAN Sebanyak Rp. 400.000 (Empat Ratus Ribu Rupiah);<br>3 (tiga) paket plastik klip yang berisikan narkotika jenis shabu-shabu dengan berat bersih 0,98 Gram;<br>1 (Satu) Unit HP Merk Infinix Hot511 Warna Hijau Dengan Nomor Imei 1 359955090521248 Dan Imei 2 359955090521255;<br>2 (Dua) Alat Hisap Sabu/Bong Lengkap Dengan Kaca Pirex;<br>2 (Dua) Tutup Botol Bekas Alat Hisap Sabu;<br>1 (Satu) Gunting Pres Warna Putih;<br>111 (Seratus Sebelas) Plastik Bening Berukuran Sedang;<br>2 (Dua) Buah Mancis Gas;<br>2 (Dua) Buah Mancis Gas;<br>2 (Dua) Buah Sendok Terbuat Dari Stiker;<br>Uang hasil penjualan kepada Sdra SUDIRMAN Sebanyak Rp. 400.000 (empat ratus ribu rupiah);<br>Dikembalikan kepada Penuntut Umum untuk dipergunakan pada berkas perkara atas nama saudara Adom;<br>6. Membebankan kepada Terdakwa membayar biaya perkara sejumlah Rp5.000,00 (lima ribu rupiah); |

---

## Statistik Korpus

Ringkasan kuantitatif dari 50 dokumen putusan Pengadilan Negeri Bengkalis di dalam `Dataset/Narkotika.zip`:

| Metrik Korpus | Nilai |
| :--- | :--- |
| **Total Dokumen Putusan (`*.pdf`)** | **50 Dokumen** |
| **Distribusi Tahun Putus** | Tahun **2025**: `40` putusan • Tahun **2024**: `10` putusan |
| **Total Halaman Keseluruhan** | **1477 Halaman** (rata-rata **29.5 halaman** per putusan) |
| **Ukuran Arsip `Dataset/Narkotika.zip`** | **~9,20 MB** (terkompresi dari 50 dokumen PDF asli) |
| **Tingkat Proses Peradilan** | Tingkat Pertama (*Pengadilan Negeri*) |
| **Undang-Undang Acuan Dominan** | UU RI Nomor 35 Tahun 2009 tentang Narkotika (Pasal 114 ayat (1)/(2), Pasal 112 ayat (1)/(2), Pasal 127 ayat (1) huruf a) |

---

## Katalog Lengkap 50 Putusan

Berikut adalah daftar lengkap 50 dokumen putusan pengadilan di dalam `Dataset/Narkotika.zip` dan `Overview/Overview.xlsx`:

| No | No Putusan | Tahun | Tanggal Dibacakan | Halaman PDF | File di `Narkotika.zip` | Tautan Direktori MA |
|:--:|:-----------|:-----:|:------------------|:-----------:|:------------------------|:-------------------:|
| 1 | `450/Pid.Sus/2025/PN Bls` | 2025 | 18 September 2025 | 26 hlm | `01_450_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107cda46927c94d5313235393434.html) |
| 2 | `449/Pid.Sus/2025/PN Bls` | 2025 | 18 September 2025 | 23 hlm | `02_449_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107cd70212ee81be313235393339.html) |
| 3 | `422/Pid.Sus/2025/PN Bls` | 2025 | 23 September 2025 | 23 hlm | `03_422_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107cced2b5a68897313235393235.html) |
| 4 | `421/Pid.Sus/2025/PN Bls` | 2025 | 23 September 2025 | 23 hlm | `04_421_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107ccdda51f4a912313235393234.html) |
| 5 | `415/Pid.Sus/2025/PN Bls` | 2025 | 24 September 2025 | 22 hlm | `05_415_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107cc1fc97fcbdda313235393034.html) |
| 6 | `375/Pid.Sus/2025/PN Bls` | 2025 | 24 September 2025 | 38 hlm | `06_375_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107cbfc362b8baeb313235393030.html) |
| 7 | `424/Pid.Sus/2025/PN Bls` | 2025 | 25 September 2025 | 29 hlm | `07_424_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c97343a3e9af5313235373532.html) |
| 8 | `423/Pid.Sus/2025/PN Bls` | 2025 | 25 September 2025 | 30 hlm | `08_423_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c96071c768237313235373530.html) |
| 9 | `472/Pid.Sus/2025/PN Bls` | 2025 | 25 September 2025 | 22 hlm | `09_472_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c9385bebc9d03313235373436.html) |
| 10 | `374/Pid.Sus/2025/PN Bls` | 2025 | 24 September 2025 | 43 hlm | `10_374_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c81fb92a28463313235373136.html) |
| 11 | `336/Pid.Sus/2025/PN Bls` | 2025 | 30 September 2025 | 40 hlm | `11_336_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c79ca0866ac37313235373033.html) |
| 12 | `335/Pid.Sus/2025/PN Bls` | 2025 | 30 September 2025 | 39 hlm | `12_335_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c75c1f31e80d6313235363536.html) |
| 13 | `501/Pid.Sus/2025/PN Bls` | 2025 | 2 Oktober 2025 | 21 hlm | `13_501_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c6a2417268928313235363336.html) |
| 14 | `441/Pid.Sus/2025/PN Bls` | 2025 | 6 Oktober 2025 | 40 hlm | `14_441_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c605be700869c313235363230.html) |
| 15 | `337/Pid.Sus/2025/PN Bls` | 2025 | 30 September 2025 | 47 hlm | `15_337_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c5f24162880c2313235363138.html) |
| 16 | `377/Pid.Sus/2025/PN Bls` | 2025 | 7 Oktober 2025 | 40 hlm | `16_377_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c5c3d538e834e313235363133.html) |
| 17 | `378/Pid.Sus/2025/PN Bls` | 2025 | 7 Oktober 2025 | 33 hlm | `17_378_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c5b088736abc8313235363131.html) |
| 18 | `376/Pid.Sus/2025/PN Bls` | 2025 | 7 Oktober 2025 | 44 hlm | `18_376_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c4d0c42c68873313235353437.html) |
| 19 | `429/Pid.Sus/2025/PN Bls` | 2025 | 8 Oktober 2025 | 31 hlm | `19_429_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c4819b4ec8c86313235353339.html) |
| 20 | `430/Pid.Sus/2025/PN Bls` | 2025 | 8 Oktober 2025 | 34 hlm | `20_430_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c46da9af6a367313235353337.html) |
| 21 | `462/Pid.Sus/2025/PN Bls` | 2025 | 8 Oktober 2025 | 23 hlm | `21_462_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c440e16e08259313235353332.html) |
| 22 | `461/Pid.Sus/2025/PN Bls` | 2025 | 8 Oktober 2025 | 22 hlm | `22_461_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c42fd01da9414313235353331.html) |
| 23 | `474/Pid.Sus/2025/PN Bls` | 2025 | 9 Oktober 2025 | 28 hlm | `23_474_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c3de2bbe087d9313235353232.html) |
| 24 | `471/Pid.Sus/2025/PN Bls` | 2025 | 9 Oktober 2025 | 26 hlm | `24_471_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c3ca5ccd694f6313235353230.html) |
| 25 | `470/Pid.Sus/2025/PN Bls` | 2025 | 9 Oktober 2025 | 23 hlm | `25_470_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c3b490894b54e313235353138.html) |
| 26 | `469/Pid.Sus/2025/PN Bls` | 2025 | 9 Oktober 2025 | 20 hlm | `26_469_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c340f0678b62a313235353036.html) |
| 27 | `381/Pid.Sus/2025/PN Bls` | 2025 | 14 Oktober 2025 | 27 hlm | `27_381_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c2d78ce66a03a313235343535.html) |
| 28 | `379/Pid.Sus/2025/PN Bls` | 2025 | 14 Oktober 2025 | 28 hlm | `28_379_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c2c4ad5169302313235343533.html) |
| 29 | `380/Pid.Sus/2025/PN Bls` | 2025 | 14 Oktober 2025 | 28 hlm | `29_380_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c2b18d4e096c7313235343531.html) |
| 30 | `442/Pid.Sus/2025/PN Bls` | 2025 | 6 Oktober 2025 | 38 hlm | `30_442_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c29f725088848313235343439.html) |
| 31 | `465/Pid.Sus/2025/PN Bls` | 2025 | 16 Oktober 2025 | 22 hlm | `31_465_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c1b2d679e9a71313235343234.html) |
| 32 | `476/Pid.Sus/2025/PN Bls` | 2025 | 16 Oktober 2025 | 20 hlm | `32_476_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107c1905977a9ac8313235343230.html) |
| 33 | `427/Pid.Sus/2025/PN Bls` | 2025 | 21 Oktober 2025 | 26 hlm | `33_427_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107904512568861d313233323137.html) |
| 34 | `332/Pid.Sus/2025/PN Bls` | 2025 | 22 Oktober 2025 | 35 hlm | `34_332_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf1107900bdb5ce9ce3313233323131.html) |
| 35 | `333/Pid.Sus/2025/PN Bls` | 2025 | 22 Oktober 2025 | 38 hlm | `35_333_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf11078fd4beddea8c1313233323035.html) |
| 36 | `334/Pid.Sus/2025/PN Bls` | 2025 | 22 Oktober 2025 | 35 hlm | `36_334_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf11078fbbf54888c8c313233323033.html) |
| 37 | `466/Pid.Sus/2025/PN Bls` | 2025 | 23 Oktober 2025 | 17 hlm | `37_466_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf11078e9fc4ce281d1313233313333.html) |
| 38 | `463/Pid.Sus/2025/PN Bls` | 2025 | 27 Oktober 2025 | 29 hlm | `38_463_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf11078e3e335f0b6ba313233313233.html) |
| 39 | `446/Pid.Sus/2025/PN Bls` | 2025 | 23 Oktober 2025 | 24 hlm | `39_446_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf11078ddf9e66686ef313233313133.html) |
| 40 | `420/Pid.Sus/2025/PN Bls` | 2025 | 28 Oktober 2025 | 35 hlm | `40_420_Pid.Sus_2025_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaf11078d4252c0e9687313233303536.html) |
| 41 | `509/Pid.Sus/2024/PN Bls` | 2024 | 3 Desember 2024 | 28 hlm | `41_509_Pid.Sus_2024_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaefd22b2dca50a09483313035333536.html) |
| 42 | `510/Pid.Sus/2024/PN Bls` | 2024 | 3 Desember 2024 | 30 hlm | `42_510_Pid.Sus_2024_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaefd22b2c5aa67095c2313035333534.html) |
| 43 | `633/Pid.Sus/2024/PN Bls` | 2024 | 3 Desember 2024 | 18 hlm | `43_633_Pid.Sus_2024_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaefd22b2ae901ce8311313035333531.html) |
| 44 | `615/Pid.Sus/2024/PN Bls` | 2024 | 3 Desember 2024 | 43 hlm | `44_615_Pid.Sus_2024_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaefd22b29c43c64a0a4313035333439.html) |
| 45 | `616/Pid.Sus/2024/PN Bls` | 2024 | 3 Desember 2024 | 41 hlm | `45_616_Pid.Sus_2024_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaefd22b283cab109735313035333437.html) |
| 46 | `614/Pid.Sus/2024/PN Bls` | 2024 | 5 Desember 2024 | 20 hlm | `46_614_Pid.Sus_2024_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaefd22b1f6c83708a73313035333332.html) |
| 47 | `684/Pid.Sus/2024/PN Bls` | 2024 | 9 Desember 2024 | 28 hlm | `47_684_Pid.Sus_2024_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaefd22b1be69fe2b926313035333236.html) |
| 48 | `685/Pid.Sus/2024/PN Bls` | 2024 | 9 Desember 2024 | 29 hlm | `48_685_Pid.Sus_2024_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaefd22b1a9e20ce8d3a313035333234.html) |
| 49 | `586/Pid.Sus/2024/PN Bls` | 2024 | 9 Desember 2024 | 22 hlm | `49_586_Pid.Sus_2024_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaefd22b19734a1c9f7d313035333232.html) |
| 50 | `590/Pid.Sus/2024/PN Bls` | 2024 | 9 Desember 2024 | 26 hlm | `50_590_Pid.Sus_2024_PN_Bls.pdf` | [Lihat Putusan](https://putusan3.mahkamahagung.go.id/direktori/putusan/zaefd22b14a1baa092a8313035333134.html) |

---

## Panduan Penggunaan untuk Information Retrieval

### 1. Mengekstrak Arsip PDF dan Membaca `Overview.xlsx` dengan Python

```python
import zipfile
import pandas as pd

# 1. Membaca rekapitulasi metadata dari Overview/Overview.xlsx
df = pd.read_excel("Overview/Overview.xlsx")
print(f"Total baris metadata: {len(df)}")
print(df[["No", "No Putusan", "Lembaga Peradilan"]].head())

# 2. Mengekstrak seluruh 50 dokumen PDF dari Dataset/Narkotika.zip
with zipfile.ZipFile("Dataset/Narkotika.zip", "r") as zf:
    zf.extractall("Dataset/extracted_pdfs")
    print(f"Berhasil mengekstrak {len(zf.namelist())} dokumen PDF.")
```

### 2. Ekstraksi Teks Penuh (*Full-Text Extraction*) untuk Indexing TKI

```python
import glob
import pymupdf  # PyMuPDF

corpus = {}
for pdf_file in sorted(glob.glob("Dataset/extracted_pdfs/*.pdf")):
    with pymupdf.open(pdf_file) as doc:
        corpus[pdf_file] = "\n".join(page.get_text("text") for page in doc)

print(f"Korpus siap diindeks: {len(corpus)} dokumen putusan PN Bengkalis.")
```

---

## Lisensi & Keterbukaan Data

Seluruh dokumen putusan pengadilan di dalam repositori ini merupakan dokumen publik resmi negara yang diterbitkan oleh **Mahkamah Agung Republik Indonesia** melalui Direktori Putusan (`putusan3.mahkamahagung.go.id`). Sesuai ketentuan perundang-undangan di Indonesia (UU No. 28 Tahun 2014 tentang Hak Cipta Pasal 43 huruf a dan SK KMA No. 1-144/KMA/SK/I/2011), putusan badan peradilan tidak memiliki pembatasan Hak Cipta dan terbuka untuk kepentingan pendidikan, penelitian akademik, serta pengembangan teknologi Temu Kembali Informasi.
