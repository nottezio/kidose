# 💊 KIDOSE — Kalkulator Dosis Pediatri

<div align="center">

![KIDOSE Banner](https://img.shields.io/badge/KIDOSE-v2.0-059669?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0id2hpdGUiIGQ9Ik0xMiAydjIwTTIgMTJoMjAiLz48L3N2Zz4=)
![Language](https://img.shields.io/badge/Bahasa-Indonesia-blue?style=for-the-badge)
![Stack](https://img.shields.io/badge/Stack-HTML%20%2B%20Tailwind%20%2B%20Vanilla%20JS-38bdf8?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Zero Dependencies](https://img.shields.io/badge/Dependencies-Zero-emerald?style=for-the-badge)

**Kalkulator dosis obat pediatri berbasis berat badan untuk tenaga kesehatan Indonesia.**  
Ringan, offline-capable, dan langsung berjalan dari satu file HTML.

[🚀 Demo Langsung](#cara-pakai) · [📋 Daftar Obat](#database-obat) · [🤝 Kontribusi](#kontribusi)

</div>

---

## ✨ Fitur Utama

| Fitur | Deskripsi |
|-------|-----------|
| ⚡ **Kalkulasi Real-time** | Dosis dihitung otomatis saat input BB/usia diketik |
| 🔍 **Smart Search** | Cari obat berdasarkan nama, indikasi, atau rute pemberian |
| 💊 **61 Obat** | Mencakup 12 kategori dari antipiretik hingga emergensi ICU |
| 📐 **Rentang Dosis** | Menampilkan *min–max* jika ada rentang dosis (mis: `100 – 150 mg`) |
| 🧪 **Konversi Sediaan** | Otomatis konversi mg → ml untuk sirup, drops, injeksi |
| ⚠️ **Validasi Klinis** | Peringatan jika BB/usia di luar nalar pediatri |
| 📱 **Mobile-First** | Dioptimalkan untuk penggunaan di IGD via smartphone |
| 🌐 **Zero Dependencies** | Tidak butuh internet setelah file diunduh (kecuali Tailwind CDN) |
| 📁 **Single File** | Seluruh app ada di satu file `.html` — mudah disimpan & dibagikan |

---

## 🖥️ Screenshot

```
┌─────────────────────────────────────────────────┐
│  ✚  KIDOSE                              v2.0    │
│     Kalkulator Dosis Pediatri Lengkap           │
├─────────────────────────────────────────────────┤
│  Usia — Tahun  │ Usia — Bulan │  Berat Badan   │
│  [ 2 ] thn     │ [ 3 ] bln    │  [ 12.5 ] kg   │
├─────────────────────────────────────────────────┤
│  🔍 Cari obat, indikasi, atau rute...           │
├─────────────────────────────────────────────────┤
│  🌡️ Antipiretik & Analgesik            5 obat  │
│  ⚡ Antikonvulsan & Sedatif             5 obat  │
│  💊 Antibiotik                         10 obat  │
│  🚨 Emergensi & Resusitasi            11 obat  │
│  ...                                            │
└─────────────────────────────────────────────────┘
```

---

## 🚀 Cara Pakai

### Opsi 1 — Buka Langsung (Termudah)
```bash
# Clone repo
git clone https://github.com/username/kidose.git

# Buka file di browser — tidak perlu server!
open kidose_v2.html        # macOS
start kidose_v2.html       # Windows
xdg-open kidose_v2.html    # Linux
```

### Opsi 2 — Unduh Satu File
Unduh `kidose_v2.html` dari halaman [Releases](../../releases) → simpan ke HP / komputer → buka di browser.

### Opsi 3 — Host di GitHub Pages
```bash
# Push ke branch gh-pages
git checkout -b gh-pages
git add kidose_v2.html
git commit -m "Deploy KIDOSE"
git push origin gh-pages
```
Akses via: `https://username.github.io/kidose/kidose_v2.html`

---

## ⚙️ Cara Menggunakan Aplikasi

```
1. Isi usia pasien (Tahun + Bulan secara terpisah)
   → Contoh: 2 tahun 3 bulan

2. Isi berat badan dalam kg (desimal didukung)
   → Contoh: 12.5

3. Kalkulasi otomatis berjalan → buka accordion kategori obat

4. Untuk mencari obat spesifik → ketik di Search Bar
   → Contoh: "paracetamol", "kejang", "syok", "asma"
```

---

## 💊 Database Obat

**Total: 61 obat** dalam 12 kategori

### A 🌡️ Antipiretik & Analgesik
| Obat | Rute | Sediaan |
|------|------|---------|
| Paracetamol | Oral / IV / Supp | Sirup 120mg/5ml, Drops, Forte, Tab 500mg |
| Ibuprofen | Oral | Sirup 100mg/5ml, Forte 200mg/5ml |
| Ketorolac | IV / IM | Injeksi 30mg/ml |
| Tramadol | Oral / IV | Sirup 50mg/5ml, Injeksi |
| Morphine | IV / SC | Injeksi 10mg/ml, Infus kontinu |

### B ⚡ Antikonvulsan & Sedatif
| Obat | Rute | Catatan |
|------|------|---------|
| Diazepam | IV / Rektal | Capped max 10 mg/dosis |
| Fenitoin | IV Loading | Max 1000 mg, rate ≤ 1 mg/kg/mnt |
| Midazolam | IV / Bukal / Nasal | Antidot: Flumazenil |
| Phenobarbital | IV Loading / Oral | ≤ 1 mg/kg/mnt |
| Levetiracetam | IV / Oral | Loading 20–60 mg/kgBB |

### C 💊 Antibiotik
| Obat | Rute | Indikasi Utama |
|------|------|----------------|
| Ampicillin + Gentamicin | IV | Sepsis neonatus |
| Ceftriaxone / Cefotaxime | IV | Empiris sepsis, meningitis |
| Amoxicillin-Clavulanate | Oral | ISPA, otitis media, ISK |
| Cefixime | Oral | ISK, demam tifoid |
| Azithromycin | Oral | Pneumonia atipikal, pertusis |
| Cotrimoxazole (TMP-SMX) | Oral | ISK, PCP profilaksis |
| Metronidazole | Oral / IV | Ameba, anaerob, Giardia |
| Meropenem | IV | Sepsis berat / MDR |
| Vancomycin | IV | MRSA, gram positif resisten |
| Clindamycin | Oral / IV | Anaerob, selulitis, osteomielitis |

### D 💧 Cairan Rumatan & Resusitasi
| Obat | Formula |
|------|---------|
| Cairan Rumatan | Holiday-Segar: 100/50/20 ml/kg + rate jam + tpm |
| Cairan Resusitasi | Bolus RL/NS 20 ml/kgBB |
| Gastroenteritis & Dehidrasi | Oralit 75 ml/kg + Zinc + Rencana WHO A/B/C |

### E 🫁 Respiratori & Nebulisasi
| Obat | Catatan |
|------|---------|
| Salbutamol / Ipratropium ± Budesonide | Dropdown derajat: Ringan / Sedang / Berat |
| Ambroxol | Mukolitik oral, konversi sirup |
| Montelukast | Berbasis **usia** (bukan BB) |

### F 🛡️ Kortikosteroid
Dexamethasone · Methylprednisolone — dosis per indikasi (croup, asma, meningitis)

### G 🤢 Antiemetik & Antihistamin
Ondansetron (capping otomatis per usia) · Domperidone · Cetirizine (berbasis usia) · CTM

### H 🛑 Gastroprotektor
Ranitidine · Omeprazole · Sucralfate

### I 🚨 Emergensi & Resusitasi *(Kategori Baru v2.0)*
| Obat | Indikasi |
|------|----------|
| **Epinephrine (Adrenalin)** | Anafilaksis IM + RJP IV/IO + Nebu croup |
| **Atropine** | Bradikardia, pre-anestesi, organofosfor |
| **Ketamine** | Sedasi prosedural IV + anestesi IM |
| **Dopamine** | Syok — Rule of 6 drip preparation |
| **Dobutamine** | Gagal jantung / syok kardiogenik |
| **Adenosine** | SVT — rapid IV push |
| **Sodium Bikarbonat** | Asidosis metabolik berat |
| **Calcium Gluconate** | Hipokalsemia, hiperkalemia |
| **Dextrose** | Hipoglikemia — D10%/D25% |
| **Naloxone** | Overdosis opioid |
| **Magnesium Sulfate** | Asma berat, hipomagnesemia |

### J 🔬 Antijamur, Antiparasit & Antivirus *(Kategori Baru v2.0)*
Fluconazole · Nystatin · Acyclovir · Albendazole · Mebendazole · Pyrantel Pamoate

### K ❤️ Kardiovaskular & Diuretik *(Kategori Baru v2.0)*
Furosemide · Spironolactone · Captopril · Propranolol · Digoxin (TDD berbasis usia)

### L 🌿 Suplemen & Nutrisi *(Kategori Baru v2.0)*
Vitamin A · Ferosulfat (Fe) · Vitamin D · Asam Folat

---

## 🔍 Fitur Smart Search

Ketik kata kunci apa pun di search bar untuk memfilter:

```
"paracetamol"  → menampilkan Paracetamol
"kejang"       → menampilkan Diazepam, Fenitoin, Midazolam, Phenobarbital, Levetiracetam
"asma"         → menampilkan Salbutamol, Dexamethasone, Methylpred, Ketamine, MgSO₄
"syok"         → menampilkan Epinephrine, Dopamine, Dobutamine, Cairan Resusitasi
"cacing"       → menampilkan Albendazole, Mebendazole, Pyrantel Pamoate
"iv"           → semua obat dengan rute intravena
```

**Behavior saat search aktif:**
- ✅ Kategori yang memiliki hasil → **auto-expand**
- 🔴 Kategori tanpa hasil → auto-collapse
- 🟢 Obat yang cocok → highlighted dengan border hijau
- ⬜ Obat yang tidak cocok → dimmed (opacity rendah)

---

## 🏗️ Arsitektur Teknis

```
kidose_v2.html
├── <head>
│   ├── Tailwind CSS (CDN)
│   └── <style> — custom CSS (accordion, dose-table, search states)
├── <body>
│   ├── Header (sticky)
│   ├── Data Pasien Card (dual age input + BB)
│   ├── Search Bar + Result Banner
│   ├── Category Accordions (dinamis dari JS)
│   └── Disclaimer Footer
└── <script>
    ├── STATE          — { weight, ageYears, ageMonthsInput, ageMonths }
    ├── HELPERS        — fmtRange(), mgToMl(), tRow(), tTable(), tSection()
    ├── DC {}          — 61 drug calculator functions
    ├── categories[]   — data obat + keywords + flags
    ├── renderCategories()
    ├── toggleAccordion() / setAccordion()
    ├── doSearch()     — filter + highlight + auto-expand
    ├── checkWarnings()
    ├── recalculate()  — main engine, real-time
    └── DOMContentLoaded init
```

### Drug Entry Schema
```javascript
{
  id:          'paracetamol',        // unik, dipakai sbg DOM id
  name:        'Paracetamol',        // nama tampil
  sub:         'Antipiretik lini 1', // deskripsi singkat
  fn:          'paracetamol',        // key ke DC object
  needsAge:    false,                // true jika kalkulasi butuh usia
  bbOptional:  false,                // true jika bisa hitung tanpa BB
  hasSeverity: false,                // true jika ada dropdown ringan/sedang/berat
  keywords:    ['demam','nyeri','sirup','iv']  // untuk search matching
}
```

### Dose Table Helper Pattern
```javascript
// Semua output obat menggunakan pola ini:
tTable(
  tRow('🎯', 'Label', 'Nilai', true) +   // true = highlight (baris utama)
  tSection('Sub-header') +               // pemisah bagian
  tRow('💧', 'Label', 'Nilai'),
  'Catatan kaki opsional di bawah tabel'
)
```

---

## 📐 Logika Kalkulasi

### Input Usia
```javascript
// Bulan boleh > 11 (tidak ada carry-over)
state.ageMonths = (ageYears * 12) + ageMonthsInput
// Contoh: 2 thn 3 bln → 27 bulan
// Contoh: 0 thn 18 bln → 18 bulan (valid)
```

### Cairan Rumatan (Holiday-Segar)
```
BB ≤ 10 kg  → 100 ml/kg
BB 10–20 kg → 1000 ml + 50 ml/kg (untuk setiap kg di atas 10)
BB > 20 kg  → 1500 ml + 20 ml/kg (untuk setiap kg di atas 20)
```

### Dopamine/Dobutamine Drip (Rule of 6)
```
Tambahkan (6 × BB) mg obat ke dalam 100 ml D5%
→ 1 ml/jam = 1 mcg/kgBB/menit
```

### Dosis Capped Otomatis
```javascript
// Contoh: Epinephrine anafilaksis
const imDose = cap(0.01 * bb, 0.5);  // max 0.5 mg

// Contoh: Fenitoin loading
const hiLoad = cap(20 * bb, 1000);   // max 1000 mg
```

---

## ✅ Validasi & Peringatan

| Kondisi | Peringatan |
|---------|-----------|
| BB ≤ 0 | BB tidak valid |
| BB < 1 kg | BB sangat rendah |
| BB > 50 kg | Di luar nalar pediatri |
| Usia > 18 tahun | Melebihi rentang pediatri |
| BB << estimasi usia | Kemungkinan gizi buruk |
| BB >> estimasi usia | Verifikasi / pertimbangkan obesitas |
| Obat butuh usia, tapi tidak diisi | Warning per obat |

---

## 🛠️ Stack Teknologi

| Komponen | Detail |
|----------|--------|
| **HTML5** | Struktur, semantik, SVG favicon inline |
| **Tailwind CSS v3** | Via CDN — utility-first styling |
| **Vanilla JavaScript ES6+** | Tidak ada framework, tidak ada build step |
| **CSS Custom** | Accordion, dose-table, search highlight state |

**Tidak dibutuhkan:**
- ❌ Node.js / npm
- ❌ Build process (webpack, vite, dsb.)
- ❌ Backend / database
- ❌ Internet (setelah Tailwind CDN di-cache browser)

---

## ⚠️ Disclaimer Medis

> **KIDOSE adalah alat bantu klinis, BUKAN pengganti penilaian klinis.**
>
> - Selalu verifikasi dosis dengan formularium resmi: **IDAI**, **BNF for Children**, **WHO Essential Medicines for Children**
> - Pertimbangkan kondisi klinis individual, fungsi ginjal/hepar, dan interaksi obat
> - Pengembang tidak bertanggung jawab atas penggunaan klinis langsung tanpa verifikasi
> - Data dosis berdasarkan literatur pediatri standar per tanggal rilis

---

## 🗺️ Roadmap

- [ ] Mode PWA (installable ke homescreen)
- [ ] Export hasil kalkulasi ke PDF
- [ ] Mode gelap (dark mode)
- [ ] Kalkulator dosis loading + maintenance terpisah
- [ ] Kalkulator tetes infus interaktif
- [ ] Multi-bahasa (EN/ID toggle)
- [ ] Tambahan: Insulin, TPN, Heparin
- [ ] Offline-first dengan Service Worker

---

## 🤝 Kontribusi

Kontribusi sangat disambut! Terutama:

- 🐛 **Bug fix** — kalkulasi yang salah / tampilan yang rusak
- 💊 **Tambah obat** — buka Issue dengan format:
  ```
  Nama obat:
  Kategori:
  Dosis (mg/kgBB):
  Sediaan yang tersedia:
  Referensi (IDAI/BNF/WHO):
  ```
- 🌐 **Terjemahan** — struktur sudah siap untuk i18n
- 📱 **UI/UX** — saran desain untuk mobile

### Cara Berkontribusi
```bash
# 1. Fork repo ini
# 2. Buat branch baru
git checkout -b feat/tambah-obat-baru

# 3. Edit kidose_v2.html
# 4. Test di browser lokal
# 5. Commit & push
git commit -m "feat: tambah Amlodipine ke kategori kardiovaskular"
git push origin feat/tambah-obat-baru

# 6. Buat Pull Request
```

---

## 📄 Lisensi

Didistribusikan di bawah **MIT License**. Lihat [`LICENSE`](LICENSE) untuk detail.

---

## 🙏 Referensi

- **IDAI** — Ikatan Dokter Anak Indonesia, Formularium Spesialistik
- **BNF for Children** — British National Formulary for Children
- **WHO** — Essential Medicines for Children, Pocket Book of Hospital Care
- **Harriet Lane Handbook** — Johns Hopkins Hospital
- **Taketomo CK, et al.** — Pediatric & Neonatal Dosage Handbook

---

<div align="center">

Dibuat dengan ❤️ untuk tenaga kesehatan anak Indonesia

*"The right dose makes the medicine."*

</div>
