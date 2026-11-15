# Sitong Pintar

**Digital Twin Monitoring Tong Sampah Otomatis**

## Deskripsi

**Sitong Pintar** merupakan proyek yang membuat representasi digital dari tong sampah untuk menunjukkan kondisi tong sampah secara **real-time**, khususnya tingkat kepenuhan tong.

Sistem ini dirancang untuk membantu petugas memantau kondisi tong sampah tanpa harus melakukan pengecekan secara manual secara terus-menerus.

## Tujuan

Proyek ini bertujuan untuk:

* Menampilkan persentase kepenuhan tong sampah.
* Menentukan status kondisi tong sampah.
* Menampilkan representasi digital dari tong sampah.
* Memberikan informasi kondisi tong berdasarkan data sensor.
* Membantu petugas mengetahui tong yang perlu segera dikosongkan.

## Fitur Rencana

* Monitoring tingkat kepenuhan tong.
* Status **Normal**, **Hampir Penuh**, dan **Penuh**.
* Visualisasi **Digital Twin**.
* Notifikasi ketika tong penuh.
* Riwayat data monitoring *(pengembangan lanjutan)*.

## Struktur Proyek

```text
Sitong_Pintar/
│
├── Perancangan Proyek/
│   ├── Perhitungan Function Point.md
│   ├── Product Backlog & Sprint 1 backlog.md
│   └── Proyek Charter.md
│
├── Inisialisasi Kode Proyek/
│   └── Kerangka Proyek/
│
├── Desain Dan Arsitektur/
│   └── UX_UI_Sitong_Pintar/
│
└── README.md
```

## Status Proyek

**Sprint 1 — Perencanaan, Desain, dan Project Setup**

Kegiatan pada Sprint 1 meliputi:

* Perencanaan proyek.
* Penyusunan Project Charter.
* Penyusunan Product Backlog.
* Penyusunan Sprint 1 Backlog.
* Perhitungan awal Function Point.
* Perancangan UX/UI.
* Inisialisasi repository GitHub.
* Pembuatan kerangka awal proyek.

## Tim

| No. | Nama              | NIM       |
| --- | ----------------- | --------- |
| 1   | Sarah Tri Aulyah  | 240504065 |
| 2   | Siti Nabila Zuhra | 240504078 |
| 3   | Riska Shofiyah    | 240504093 |

## Teknologi Awal

> Teknologi berikut masih berupa **usulan awal** dan belum ditetapkan sebagai teknologi final.

| Bagian                | Usulan Awal                 | Catatan                                           |
| --------------------- | --------------------------- | ------------------------------------------------- |
| Sensor                | Sensor jarak / ultrasonik   | Disesuaikan dengan ukuran dan kondisi tong        |
| Mikrokontroler        | ESP32 atau perangkat setara | Dipilih berdasarkan konektivitas dan ketersediaan |
| Dashboard             | HTML, CSS, JavaScript       | Framework dapat ditentukan kemudian               |
| Visual Digital Twin   | Model 3D sederhana          | Tahap awal dapat menggunakan model statis         |
| Komunikasi & Database | Ditentukan kemudian         | Menyesuaikan perangkat dan kebutuhan sistem       |

## Alur Sistem

```text
Sensor Tong Sampah
        │
        ▼
Pengambilan Data
        │
        ▼
Pengiriman Data
        │
        ▼
Dashboard Sitong Pintar
        │
        ├── Persentase Kepenuhan
        │
        ├── Status Tong
        │
        └── Visualisasi Digital Twin
```

## Status Kondisi Tong

| Persentase | Status       | Keterangan                    |
| ---------- | ------------ | ----------------------------- |
| 0% – 69%   | Normal       | Tong masih memiliki kapasitas |
| 70% – 89%  | Hampir Penuh | Tong perlu diperhatikan       |
| 90% – 100% | Penuh        | Tong perlu segera dikosongkan |

> Batas persentase dapat disesuaikan kembali berdasarkan hasil pengujian dan kebutuhan sistem.

## Rencana Pengujian Awal

Pengujian awal dilakukan menggunakan **data simulasi** untuk memastikan dashboard dapat menampilkan kondisi tong dengan benar.

| No. | Skenario                         | Hasil yang Diharapkan                                                 |
| --- | -------------------------------- | --------------------------------------------------------------------- |
| 1   | Data simulasi 35%                | Dashboard menampilkan **35%** dan status **Normal**                   |
| 2   | Data simulasi 75%                | Dashboard menampilkan **75%** dan status **Hampir Penuh**             |
| 3   | Data simulasi 95%                | Dashboard menampilkan **95%** dan status **Penuh**                    |
| 4   | Data belum diperbarui            | Dashboard menampilkan waktu update terakhir / indikator data tertunda |
| 5   | Tong dikosongkan dan nilai turun | Status berubah mengikuti nilai terbaru                                |

**Catatan:** Pengujian di atas merupakan rencana pengujian tampilan menggunakan data simulasi. Pengujian menggunakan sensor fisik dilakukan setelah perangkat tersedia.

## Langkah Penggunaan Git

### 1. Membuat Repository

Buat repository GitHub dengan nama:

```text
Sitong_Pintar
```

Tambahkan anggota kelompok sebagai collaborator.

### 2. Menambahkan File

Simpan seluruh dokumentasi proyek pada repository sesuai struktur yang telah ditentukan.

### 3. Commit

Gunakan pesan commit yang jelas, contohnya:

```bash
git add .
git commit -m "Add Sprint 1 planning and design documents"
```

### 4. Push

Push perubahan ke repository GitHub:

```bash
git push origin main
```

### 5. Pemeriksaan Repository

Periksa kembali repository untuk memastikan seluruh file dapat dibuka dengan baik.

### 6. Pengumpulan

Salin tautan repository GitHub untuk dikumpulkan melalui Google Classroom.

## Dokumentasi Proyek

Dokumentasi proyek terdiri dari:

### Perancangan Proyek

* Perhitungan Function Point
* Product Backlog & Sprint 1 Backlog
* Proyek Charter

### Inisialisasi Kode Proyek

* Kerangka Proyek

### Desain dan Arsitektur

* UX/UI Sitong Pintar

## Pengembangan Selanjutnya

Pengembangan berikutnya dapat mencakup:

* Integrasi sensor fisik.
* Integrasi mikrokontroler.
* Pengiriman data sensor ke server.
* Dashboard monitoring secara real-time.
* Visualisasi Digital Twin yang lebih interaktif.
* Sistem notifikasi ketika tong penuh.
* Penyimpanan riwayat data.
* Monitoring beberapa tong sampah.

## Lisensi

Proyek ini dibuat untuk keperluan **pembelajaran dan pengembangan proyek akademik**.

---

**Sitong Pintar — Smart Monitoring for a Cleaner Environment.**
