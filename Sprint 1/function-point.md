1. Langkah Perhitungan
Identifikasi fungsi data: ILF dan EIF.
Identifikasi fungsi transaksi: EI, EO, EQ.
Tentukan kompleksitas (Low / Average / High) berdasarkan DET, FTR, dan RET.
Hitung Unadjusted Function Point (UFP) dengan bobot standar.
Hitung Value Adjustment Factor (VAF) dari 14 General System Characteristics (GSC).
Hitung Adjusted FP.
Istilah:
Istilah	Arti
ILF	Internal Logical File: data yang dikelola oleh aplikasi
EIF	External Interface File: data yang hanya dibaca dari sistem lain
EI	External Input: proses memasukkan/mengubah data ke dalam sistem
EO	External Output: keluaran yang melibatkan perhitungan atau data turunan
EQ	External Inquiry: pengambilan data tanpa perhitungan atau data turunan
DET	Data Element Type: field unik yang dikenali pengguna
FTR	File Type Referenced: jumlah file (ILF/EIF) yang diakses oleh transaksi
RET	Record Element Type: subgrup data pengguna dalam satu file
Bobot Standar
Tipe	Low	Average	High
EI	3	4	6
EO	4	5	7
EQ	3	4	6
ILF	7	10	15
EIF	5	7	10
Matriks Kompleksitas
ILF / EIF (berdasarkan RET dan DET)
RET \ DET	1-19	20-50	51+
1	Low	Low	Average
2-5	Low	Average	High
6+	Average	High	High
EI (berdasarkan FTR dan DET)
FTR \ DET	1-4	5-15	16+
0-1	Low	Low	Average
2	Low	Average	High
3+	Average	High	High
EO dan EQ (berdasarkan FTR dan DET)
FTR \ DET	1-5	6-19	20+
0-1	Low	Low	Average
2-3	Low	Average	High
4+	Average	High	High
> Catatan: matriks EQ mengikuti bobot EQ (3/4/6). Sesuaikan dengan tabel yang dipakai dosen bila berbeda.
---
2. Identifikasi Fungsi Data (ILF dan EIF)
2.1 ILF
ID	Nama ILF	RET	DET (jumlah)	Daftar DET	Kompleksitas	Bobot
ILF-1	Data Tong Sampah	1	7	id_tong, nama_tong, lokasi, tinggi_tong, batas_kapasitas, status, tanggal_dibuat	Low	7
ILF-2	Riwayat Monitoring	1	5	id_riwayat, id_tong, tingkat_isi, persentase_isi, waktu_pencatatan	Low	7
				Total ILF		14
2.2 EIF
ID	Nama EIF	RET	DET	Kompleksitas	Bobot
-	Belum ada data eksternal yang dibaca	0	0	-	0
			Total EIF		0
---
3. Identifikasi Fungsi Transaksi (EI, EO, EQ)
3.1 External Input (EI)
Setiap proses elementer dihitung terpisah. Pengelolaan tong dipecah menjadi tambah, ubah, dan hapus.
ID	Fungsi	FTR	File yang diakses	DET	Daftar DET	Kompleksitas	Bobot
EI-1	Menerima data sensor	2	Data Tong, Riwayat Monitoring	4	id_tong, tingkat_isi, waktu, tombol/aksi simpan	Low	3
EI-2	Menambah tong	1	Data Tong	5	nama_tong, lokasi, tinggi_tong, batas_kapasitas, status	Low	3
EI-3	Mengubah tong	1	Data Tong	6	id_tong, nama_tong, lokasi, tinggi_tong, batas_kapasitas, status	Low	3
EI-4	Menghapus tong	2	Data Tong, Riwayat Monitoring	1	id_tong	Low	3
EI-5	Mengatur batas kapasitas	1	Data Tong	2	id_tong, batas_kapasitas	Low	3
					Total EI		15
3.2 External Output (EO)
ID	Fungsi	FTR	File yang diakses	DET	Daftar DET	Kompleksitas	Bobot
EO-1	Melihat riwayat monitoring (dengan persentase isi turunan)	2	Riwayat Monitoring, Data Tong	6	nama_tong, lokasi, waktu, tingkat_isi, persentase_isi, status	Average	5
EO-2	Melihat status kapasitas tong (status dihitung dari batas)	2	Data Tong, Riwayat Monitoring	6	nama_tong, lokasi, tingkat_isi_terakhir, persentase_isi, batas_kapasitas, status	Average	5
					Total EO		10
3.3 External Inquiry (EQ)
ID	Fungsi	FTR	File yang diakses	DET	Daftar DET	Kompleksitas	Bobot
EQ-1	Melihat daftar tong	1	Data Tong	4	id_tong, nama_tong, lokasi, status	Low	3
EQ-2	Melihat detail tong	1	Data Tong	7	id_tong, nama_tong, lokasi, tinggi_tong, batas_kapasitas, status, tanggal_dibuat	Low	3
					Total EQ		6
---
4. Unadjusted Function Point (UFP)
Tipe	Jumlah fungsi	Low	Average	High	Subtotal
EI	5	5 x 3 = 15	0	0	15
EO	2	0	2 x 5 = 10	0	10
EQ	2	2 x 3 = 6	0	0	6
ILF	2	2 x 7 = 14	0	0	14
EIF	0	0	0	0	0
Total (UFP)	11				45
```
UFP = EI + EO + EQ + ILF + EIF
UFP = 15 + 10 + 6 + 14 + 0 = 45
```
---
5. Faktor Penyesuaian (Value Adjustment Factor)
Setiap GSC dinilai 0 sampai 5:
0 = tidak berpengaruh, 1 = sedikit, 2 = cukup, 3 = sedang, 4 = signifikan, 5 = sangat kuat.
No	General System Characteristic	Nilai (Fi)	Alasan (asumsi)
1	Data communications	4	Data sensor dikirim dan diterima lewat jaringan
2	Distributed data processing	3	Pemrosesan terbagi antara perangkat sensor dan server
3	Performance	3	Data monitoring perlu tampil cukup cepat
4	Heavily used configuration	2	Konfigurasi perangkat tidak terlalu ketat
5	Transaction rate	3	Data sensor masuk secara berkala
6	On-line data entry	4	Data sensor dan data tong masuk secara daring
7	End-user efficiency	3	Antarmuka sederhana untuk melihat status tong
8	On-line update	3	Data tong dapat diubah langsung
9	Complex processing	2	Pemrosesan terbatas pada perhitungan persentase dan status
10	Reusability	2	Komponen belum dirancang untuk dipakai ulang
11	Installation ease	2	Instalasi relatif sederhana
12	Operational ease	3	Operasional harian cukup mudah
13	Multiple sites	2	Lokasi tong beragam, namun satu sistem
14	Facilitate change	3	Pengaturan batas kapasitas dapat diubah
	Total (ΣFi)	39	
```
VAF = 0,65 + (0,01 x ΣFi)
VAF = 0,65 + (0,01 x 39)
VAF = 1,04
```
---
6. Hasil Akhir (Adjusted Function Point)
```
FP = UFP x VAF
FP = 45 x 1,04
FP = 46,8 Function Point
```
Komponen	Nilai
UFP	45
ΣFi	39
VAF	1,04
Adjusted FP (Sprint 1)	46,8
---
7. Analisis Sensitivitas
Karena nilai Fi masih asumsi, berikut rentang hasil FP dengan UFP = 45:
Skenario	ΣFi	VAF	FP
Minimum (semua Fi = 0)	0	0,65	29,25
Semua Fi = 3 (asumsi awal)	42	1,07	48,15
Perhitungan detail (dokumen ini)	39	1,04	46,8
Maksimum (semua Fi = 5)	70	1,35	60,75
---
8. Perbandingan dengan Estimasi Awal
Aspek	Estimasi awal	Perhitungan detail
Jumlah fungsi EI	3 (bobot 4)	5 (bobot 3, dipecah per proses elementer)
Jumlah fungsi EO	2 (bobot 5)	2 (bobot 5)
Jumlah fungsi EQ	2 (bobot 4)	2 (bobot 3)
ILF	2 (bobot 10)	2 (bobot 7, hasil matriks RET/DET)
UFP	50	45
ΣFi / VAF	42 / 1,07	39 / 1,04
FP	53,5	46,8
Penurunan terutama berasal dari penentuan kompleksitas ILF dan EQ berdasarkan DET/RET/FTR (keduanya Low), bukan bobot asumsi Average.
---
9. Asumsi dan Catatan Validasi
Jumlah DET, FTR, dan RET di atas adalah asumsi dari rancangan awal dan perlu dicocokkan dengan desain basis data dan antarmuka final.
Fungsi "Melihat detail tong" pada estimasi awal dipisah menjadi EO-2 (status kapasitas turunan) dan EQ-2 (detail data master) agar tidak terhitung ganda. Jika dosen menganggap keduanya satu fungsi, kurangi satu transaksi.
Pengelolaan tong dihitung sebagai 3 EI (tambah, ubah, hapus). Jika dosen menghitungnya sebagai satu fungsi, UFP akan berkurang 6.
Notifikasi kapasitas penuh belum dimasukkan karena belum ada pada cakupan Sprint 1. Jika ditambahkan, hitung sebagai EO.
Nilai 14 GSC perlu disepakati dengan dosen atau tim. Gunakan nilai rata-rata 3 bila dosen menetapkan demikian (hasil FP = 48,15).
Dokumen ini harus diperbarui setelah kebutuhan terkonfirmasi.
