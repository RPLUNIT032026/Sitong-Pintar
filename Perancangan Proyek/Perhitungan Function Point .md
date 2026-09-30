DOKUMEN PERHITUNGAN FUNCTION POINT (FP)
	Function Point digunakan untuk memperkirakan ukuran fungsional aplikasi dari fungsi yang terlihat oleh pengguna. Karena kebutuhan masih tahap rancangan, perhitungan berikut adalah estimasi awal dan harus diperbarui setelah detail fitur, data, serta kompleksitas dikonfirmasi.
1. Identifikasi Fungsi

| NO. | Tipe | Fungsi yang diidentifikasi | Jumlah | Bobot Asumsi | Subtotal |
|---:|---|---|---:|---:|---:|
| 1 | EI | Penerimaan data sensor, pengelolaan tong, pengaturan batas kapasitas | 3 | 4 | 12 |
| 2 | EO | Melihat detail tong dan riwayat monitoring | 2 | 5 | 10 |
| 3 | EQ | Melihat detail/status tong | 2 | 4 | 8 |
| 4 | ILF | Data tong sampah dan data riwayat monitoring | 2 | 10 | 20 |
| 5 | EIF | Belum ada data eksternal yang dibaca | 0 | - | 0 |
| **Total** | **Count** |  |  |  | **50** |

2. Perhitungan Function Point (FP)
Count Total = 12 + 10 + 8 + 20 + 0 = 50
14 karakteristik penyesuaian (Fi) diasumsikan bernilai rata-rata 3.
ΣFi = 14 × 3 = 42
Faktor penyesuaian = 0,65 + (0,01 × 42) = 1,07
FP = Count Total × [0,65 + 0,01 × ΣFi]
FP = 50 × 1,07 = 53,5 Function Point
Hasil estimasi Sprint 1: 53,5 FP.
Catatan: angka ini belum merupakan ukuran final. Klasifikasi kompleksitas perlu divalidasi berdasarkan jumlah data element type (DET), file type referenced (FTR), dan record element type (RET) sesuai aturan Function Point yang digunakan dosen. Jika dosen meminta Adjusted Function Point, faktor penyesuaian dan dasar penilaiannya perlu ditambahkan.
