# Rangka

[Situs & tutorial](https://rangka-skill.vercel.app) · [Unduh .zip](https://github.com/bryankwandou/rangka/archive/refs/heads/main.zip) · lisensi MIT

Skill untuk Claude (dan model lain) yang menyusun kerangka dokumen sebelum menulis:
skripsi, usulan tugas akhir, laporan KKP/magang, tesis, disertasi, proposal kegiatan,
LPJ, SK, AD/ART, laporan, landing page, brosur, README, naskah video, pitch deck,
sampai mind map belajar. Bisa juga membalik berkas yang sudah ada menjadi satu kerangka.

Alurnya sama untuk semua jenis tulisan:

1. **Peta inti** — seharusnya (Das Sollen) vs kenyataan (Das Sein), pembaca, klaim inti, bukti, tindakan.
2. **Kerangka** dari template genre — tiap bagian punya tugas, isi, bukti, dan panjang.
3. **Cek** — 12 butir universal plus butir khusus genre.
4. **Judul terakhir**, lalu daftar data yang harus dilengkapi pengguna.

Skill ini tidak mengarang data, responden, atau sumber. Yang belum ada ditulis `[ISI: ...]`,
yang belum pasti ditulis `[CEK: ...]`.

## Isi paket

```
rangka/
├── SKILL.md                      alur kerja dan aturan
├── references/
│   ├── genre-research.md         skripsi, proposal penelitian, jurnal
│   ├── genre-thesis.md           tesis (S2) dan disertasi (S3)
│   ├── genre-report.md           laporan bisnis, magang, policy brief, SOP
│   ├── genre-organizational.md   proposal kegiatan, LPJ, SK, AD/ART, surat, notulen
│   ├── genre-persuasion.md       landing page, website, brosur, pamflet, iklan, email, pitch deck
│   ├── genre-technical.md        README, spec/PRD, ADR, tutorial, API docs
│   ├── genre-timed.md            video pendek/panjang, podcast, presentasi, sidang
│   ├── genre-study.md            mind map, ringkasan bab, rencana belajar
│   ├── uajm-kkp.md               laporan KKP/magang, Atma Jaya Makassar FTI
│   ├── uajm-usulan-ta.md         usulan TA & ringkasan kapasitas diri, UAJM
│   ├── uajm-skripsi.md           skripsi Bab I–V + 15 komponen bagian awal, UAJM
│   ├── uajm-format.md            tata tulis, penomoran, gaya pustaka UAJM
│   ├── pedoman-adapter.md        14 variabel untuk pedoman kampus mana pun
│   ├── appendices.md             katalog lampiran dan cara merangkanya
│   ├── summarize-to-outline.md   membalik berkas penelitian jadi satu kerangka
│   ├── languages.md              aturan keluaran lintas bahasa dan aksara
│   ├── checklist.md              pemeriksaan universal
│   ├── sources.md                daftar sumber yang boleh dikutip
│   └── examples.md               tiga contoh keluaran
├── evals/evals.json              sembilan kasus uji
(sumber situs tutorial: github.com/bryankwandou/rangka-site)
    ├── index.html
    └── i18n/en.js es.js fr.js zh.js ar.js
```

## Pedoman kampus

Pedoman Universitas Atma Jaya Makassar (FTI) dimuat utuh di empat berkas `uajm-*.md`,
diturunkan dari *Pedoman KKP FTI 2015* dan *Pedoman Penulisan Skripsi Prodi Teknik
Informatika 2015*. Untuk kampus lain, `pedoman-adapter.md` mengisi empat belas variabel
yang benar-benar mengubah struktur — dari pedoman yang kamu berikan, bukan dari tebakan.
Butir yang belum dipastikan selalu keluar sebagai `[CEK: pedoman kampus]`.

## Pemasangan

**Claude Code** — salin folder ke direktori skills:

```bash
git clone https://github.com/bryankwandou/rangka ~/.claude/skills/rangka
```

**Claude.ai** — zip folder `rangka`, lalu unggah di Settings → Capabilities → Skills.

**Model lain (ChatGPT, Gemini, dsb.)** — tempel isi `SKILL.md` sebagai instruksi sistem,
lalu tempel file genre yang relevan dan `checklist.md`.

## Pasangan yang disarankan

Rangka berhenti di kerangka. Untuk menulis dan merapikan kalimat, pakai skill `lugas`.

## Asal

Dikembangkan dari draf lama `SKILL_kerangka_penelitian.md` (khusus penelitian RAG) dan
pola mind map → outline → checklist dari video pendek akun dafnisfaz_. Seluruh isi draf
lama dipertahankan di `genre-research.md`; yang ditambahkan adalah lima genre lain,
checklist universal, dan aturan anti-fabrikasi.
