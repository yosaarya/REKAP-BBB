# Handoff Sesi: Rekap Bongkaran Armada Bukit

Catatan serah terima untuk melanjutkan pekerjaan rekap bongkaran di chat baru tanpa menjelaskan ulang dari awal.

## Cara pakai

1. Buka chat baru.
2. Tempel blok **Aturan Umum** di pesan pertama.
3. Tempel blok tugas yang dibutuhkan (Tugas 1, 2, atau 3).
4. Lampirkan file `BONGKARAN_BUKIT_*.xlsx` terbaru dan `Contoh_Aja.xlsx` versi terakhir.
5. Untuk Tugas 3, lampirkan juga gambar rekap Agustus 2026 sebagai contoh tampilan.

---

## Aturan Umum

```text
Saya admin di PT. Bukit Berkat Bersama. Saya merekap ritase/volume truk dari file BONGKARAN_BUKIT_*.xlsx. Balas dalam bahasa Indonesia.

Struktur file BONGKARAN: sheet JO 3 ADD TC9, JO 5 TC9, JO 7 TC9, JO 8 TC9 (sheet "Rekap ..." diabaikan). Satu baris = satu ritase. Kolom: NO SJ (B), NOPOL (C), VOLUME (H), SUPPLIER (I), USER (K), TIME (L, format dd/mm/yyyy jj.mm.dd). Tanggal diambil dari TIME. JO diambil dari sheet tempat baris berada.

Aturan:
- Baris yang NO SJ-nya dicoret (strikethrough) = dibatalkan/belum upload, jangan dihitung. Baris "Total ..." di dasar sheet juga dilewati.
- Supplier sering salah input, jadi truk Bukit ditentukan dari PLAT, bukan kolom supplier. Daftar plat Bukit = header sheet bulan berjalan di Contoh_Aja.xlsx (58 plat).
- B 9433 JYV dan B 9412 JYV adalah armada baru: dihitung hanya kalau supplier-nya BUKIT. Plat yang benar B 9529 JYT (bukan JYV).
- Plat bertulis BUKIT tapi bukan armada Bukit tidak dihitung (September: H 9774 OH, B 9791 TA, B 9716 JYT, AA 8452 OK, H 9846 JQ, dan plat H. HERI Z 9434 HB, N 9463 UN).
- H. HERI dan HCB juga ditentukan dari plat (supplier mayoritas per plat), bukan dari label per baris. H 9815 OH = HCB, B 9435 JYV = Bukit, Z 9434 HB dan N 9463 UN = H. HERI.
- Kalau ada file BONGKARAN yang lebih baru untuk tanggal yang sama, pakai yang terbaru dan GANTI isi tanggal itu (jangan dijumlah, karena baris yang sama bisa pindah sheet JO).
- Kalau ada plat baru muncul dengan supplier BUKIT, cek dulu ke saya sebelum dihitung.
- Setiap kali selesai, sebutkan file apa yang berubah dan lokasinya. Berikan file lengkap, bukan potongan.
```

---

## Tugas 1: Rekap ritase Bukit (`Contoh_Aja.xlsx`)

```text
Tugas: isi rekap ritase+volume Bukit per plat per hari di Contoh_Aja.xlsx (satu sheet per bulan: Aug2026, Sep2026, dst.).

Layout sheet: baris 1-2 header (baris 2 = nama plat), baris 3-32 = tanggal 1-30 (kolom B = tanggal), baris 33 = total.
Kolom C:BH = volume (m³) per plat, BI = TOTAL volume, BJ kosong, BK:DP = ritase per plat (urutan plat sama), DQ = TOTAL ritase. Total pakai rumus SUM.

Urutan plat: 10 plat pertama tetap (DN 8451 DU, DN 8957 DU, DN 8950 DU, DN 8992 DU, W 8695 UD, B 9254 TIT, B 9613 SYU, B 9108 UYW, B 9344 BYV, DN 8978 DU). Mulai B 9398 JYV sampai akhir diurutkan dari kecil ke besar (kalau ada plat baru, sisipkan sesuai urutan di kedua blok).

Aug2026 jangan diubah. Sheet bulan baru dibuat mengikuti format Sep2026.

Status terakhir: Sep2026 terisi lengkap 1-30 Sep: 2.920 ritase, 72.115,36 m³.
```

---

## Tugas 2: Rekap ritase dan volume (Bukit, opsional HCB dan H. HERI)

```text
Tugas: atasan minta ritase dan volume Bukit (opsional HCB dan H. HERI) per tanggal dan per JO.

File yang dibuat:
a) Ritase_Bukit_dan_HHeri_Sep2026.xlsx, sheet:
   - "Ritase per Tanggal": Ritase Bukit/H. HERI/Total dan Volume m³ Bukit/H. HERI/Total, TOTAL di bawah.
   - "Ritase per JO": kolom Bukit & H. HERI untuk tiap JO + Total.
   - "Volume per JO": sama, isinya volume.
   - "Penyesuaian Salah Input": daftar baris yang supplier-nya tidak cocok dengan plat, plus volume.
b) Ritase_HCB_Sep2026.xlsx, sheet:
   - "Ritase per Tanggal": Ritase, Volume.
   - "Per JO": ritase dan volume per JO.
   - "Penyesuaian Salah Input".

Semua tanggal 1-30 ditampilkan (nol tetap ditulis), total pakai rumus, header berwarna, font Arial.

Hasil Sep 2026: Bukit 2.920 ritase / 72.115,36 m³; H. HERI 316 / 8.880,66 m³; HCB 374 / 10.197,64 m³.
```

---

## Tugas 3: Rekap kubikasi kwari Bukit (printable)

```text
Tugas: rekapan "Rekapan Kubikasi Kwari dan Bongkaran Periode <Bulan Tahun>", mirip gambar Agustus 2026 (akan saya lampirkan), harus printable.

Rumus: Kubikasi Kwari = Ritase x 24 (angka 24 ada di sel Q3, di luar area cetak). Kubikasi Bongkaran = volume aktual per plat. Ritase = jumlah ritase per plat selama sebulan.

Layout: sheet "Rekap <Bulan>" di Contoh_Aja.xlsx, setelah sheet bulannya.
- Bagian GMM = 10 plat pertama (baris Kubikasi Kwari, Kubikasi Bongkaran, Ritase + kolom Total).
- Bagian BBB = 48 plat sisanya, 4 blok x 12 plat; urutan baris di tiap blok: Kubikasi Kwari, Ritase, Kubikasi Bongkaran; kolom "Kuari: Sidomuncul".
- Di bawah ada tabel Total (GMM, BBB, GMM + BBB).
Isi sel pakai rumus INDEX/MATCH ke baris 33 sheet bulan (lookup by nama plat).

Cetak: A4 landscape, muat 1 halaman, area cetak A1:N(akhir), tanpa gridline, header abu-abu muda, volume #,##0.00, ritase #,##0. Buat juga PDF-nya (hanya sheet rekap).

Hasil Sep 2026: GMM 7.176 / 6.993,65 / 299; BBB 62.904 / 65.121,71 / 2.621; Total 70.080 / 72.115,36 / 2.920.
```

---

## Ringkasan hasil September 2026

| | Ritase | Volume (m³) |
|---|---|---|
| Bukit | 2.920 | 72.115,36 |
| H. HERI | 316 | 8.880,66 |
| HCB | 374 | 10.197,64 |

Rekap kubikasi kwari (Bukit):

| | Kubikasi Kwari | Kubikasi Bongkaran | Ritase |
|---|---|---|---|
| GMM | 7.176 | 6.993,65 | 299 |
| BBB | 62.904 | 65.121,71 | 2.621 |
| **Total** | **70.080** | **72.115,36** | **2.920** |
