# Bahasa keluaran

Aturan pokok: **kerangka ditulis dalam bahasa yang dipakai user**, kecuali user meminta
lain. Kalau user menulis campuran (lazim di Indonesia: kalimat Indonesia dengan istilah
Inggris), ikuti bahasa kalimatnya, bukan bahasa istilahnya.

Struktur kerangka tidak berubah karena bahasa. Yang berubah hanya label, penanda, dan
beberapa kebiasaan retoris.

## Penanda isian

| Bahasa | Perlu diisi user | Perlu diverifikasi | Tidak ada di berkas |
|---|---|---|---|
| Indonesia | `[ISI: ...]` | `[CEK: ...]` | `[TIDAK ADA DI BERKAS: ...]` |
| Inggris | `[FILL: ...]` | `[VERIFY: ...]` | `[NOT IN SOURCE: ...]` |
| Bahasa lain | pakai padanan setempat, **konsisten satu bentuk** di seluruh keluaran | | |

Untuk bahasa yang tidak punya padanan mapan, pakai bentuk Inggris (`[FILL]`/`[VERIFY]`)
dan jelaskan sekali di awal. Jangan mencampur dua bahasa penanda dalam satu keluaran.

## Label bagian

| id | en | Keterangan |
|---|---|---|
| Peta inti | Core map | |
| Kerangka | Outline | |
| Hasil cek | Check | |
| Opsi judul | Title options | |
| Yang perlu kamu lengkapi | What you need to supply | |
| Tugas / Isi / Bukti / Panjang | Job / Content / Evidence / Length | field tiap bagian |

Untuk bahasa lain, terjemahkan keenam label itu dan keempat nama field; sisanya
mengikuti.

## Arah tulisan dan aksara

- **Arab, Ibrani, Persia, Urdu (RTL)** — keluaran Markdown tetap berfungsi; jangan
  menyisipkan penanda arah. Nomor bab tetap angka; hindari tabel yang terlalu lebar
  karena campuran RTL/LTR sulit dibaca.
- **Tionghoa, Jepang, Korea** — hitung panjang dalam **karakter**, bukan kata
  (padanan kasar: 1 kata Inggris ≈ 1,5–2 karakter Tionghoa; 1 halaman Jepang ≈ 400
  karakter dalam genkō yōshi).
- **Thai, Khmer, Lao** — tidak memakai spasi antarkata; panjang dihitung dalam karakter
  atau halaman, jangan dalam kata.
- **Bahasa daerah Indonesia** (Jawa, Sunda, Bugis, Makassar, Bali, dll.) — dipakai di
  beberapa prodi sastra daerah; sering disertai kewajiban abstrak dalam bahasa Indonesia
  dan Inggris, dan kadang aksara daerah. `[CEK: aksara dan jumlah bahasa abstrak]`.
- **Transliterasi Arab-Latin** di PTKIN mengikuti pedoman SKB Menag & Mendikbud;
  halaman pedoman transliterasi masuk bagian awal. `[CEK: versi transliterasi]`.

## Kebiasaan retoris yang berbeda antarbahasa

Ini mengubah **urutan**, jadi penting untuk kerangka:

| Tradisi | Kebiasaan |
|---|---|
| Inggris akademik | klaim di depan (*topic sentence first*); tesis dinyatakan di akhir pendahuluan |
| Indonesia akademik | pengantar melingkar dulu, klaim di akhir paragraf — tetap sah, tapi penguji makin sering menuntut ketegasan di awal |
| Prancis | *problématique* + rencana dua/tiga bagian simetris, diumumkan di akhir pendahuluan |
| Jerman | *Forschungsstand* (status penelitian) sebagai bagian tersendiri sebelum pertanyaan penelitian |
| Jepang | *ki-shō-ten-ketsu* di tulisan umum; naskah ilmiah tetap IMRaD |
| Arab | pembukaan (*muqaddimah*) lebih panjang; pujian pembuka lazim dan tidak dihitung sebagai isi |

Kalau user menulis untuk penguji Indonesia tetapi dalam bahasa Inggris, pakai struktur
pedoman kampusnya dan gaya retoris Inggris — sebut pilihan itu sekali.

## Istilah yang tidak diterjemahkan

Nama dokumen dan tahapan akademik Indonesia dipertahankan walau keluarannya berbahasa
Inggris, dengan penjelasan sekali di kemunculan pertama:

`skripsi` (undergraduate final thesis) · `KKP/KP/PKL` (internship / field practice) ·
`sempro`, `semhas` · `munaqasyah` · `pedoman penulisan` (writing guidelines) ·
`SK` (decree) · `LPJ` (accountability report) · `AD/ART` (statutes and bylaws).

Sebaliknya, istilah teknis Inggris yang sudah mapan di naskah Indonesia
(*machine learning*, *black box testing*, *user acceptance test*) tetap Inggris dan
ditulis miring, sesuai aturan istilah asing di `uajm-format.md`.

## Cek bahasa

| Kode | Cek |
|---|---|
| B1 | Seluruh keluaran memakai satu bahasa, tidak berganti di tengah? |
| B2 | Satu bentuk penanda isian saja dipakai? |
| B3 | Panjang dihitung dengan satuan yang cocok untuk aksaranya? |
| B4 | Istilah dokumen lokal dipertahankan dan dijelaskan sekali? |
| B5 | Kalau bahasa naskah ≠ bahasa pedoman, pilihan gaya retoris disebutkan? |
