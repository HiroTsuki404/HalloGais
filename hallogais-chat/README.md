# HalloGais Chat Widget 💬

Widget live chat ringan yang bisa dikustomisasi via URL parameter — tanpa edit kode!

---

## 📁 Struktur Folder

```
hallogais-chat/
├── index.html              ← Landing page / katalog tema
├── preview-assets/         ← Screenshot tiap tema (opsional)
├── widget/
│   ├── chat.html           ← File widget chat utama
│   ├── assets/
│   │   └── logo.png        ← Logo/badge HalloGais
│   └── themes/
│       ├── clean-gais.css  ← Tema: Bersih & profesional (default)
│       ├── gaming-gais.css ← Tema: Dark mode / gaming neon
│       └── cute-gais.css   ← Tema: Pastel / kawaii
└── README.md
```

---

## 🚀 Cara Pakai

### 1. Buka Landing Page
Buka `index.html` di browser → pilih tema → klik **Demo Tema** untuk preview.

### 2. Generate Link untuk Pembeli
Di halaman `index.html`, scroll ke bagian **Link Generator**:
- Isi nama toko/channel
- Pilih tema yang diinginkan
- Link otomatis terbuat, klik **Salin**

### 3. Parameter URL Manual

| Parameter | Nilai | Keterangan |
|-----------|-------|------------|
| `theme`   | `clean-gais` / `gaming-gais` / `cute-gais` | Pilih desain |
| `store`   | Nama toko (teks) | Nama yang muncul di header chat |
| `color`   | Kode hex (encode `#` → `%23`) | Warna aksen custom |
| `badge`   | `1` atau `0` | Tampilkan / sembunyikan logo |

```
# Contoh URL lengkap:
widget/chat.html?theme=gaming-gais&store=GameZone&color=%2300FF87
```

---

## 🎨 Tema yang Tersedia

| Tema | File | Cocok untuk |
|------|------|-------------|
| **Clean Gais** | `clean-gais.css` | Toko umum, profesional, minimalis |
| **Gaming Gais** | `gaming-gais.css` | Toko gaming, aksesori, teknologi |
| **Cute Gais** | `cute-gais.css` | Fashion wanita, toko kawaii, kosmetik |

---

## ➕ Menambah Tema Baru

1. Buat file CSS baru di `widget/themes/`, misal: `dark-gais.css`
2. Copy variabel `:root` dari tema yang ada, ubah nilainya
3. Daftarkan di `widget/chat.html` pada array `allowedThemes`:
   ```js
   const allowedThemes = ['clean-gais', 'gaming-gais', 'cute-gais', 'dark-gais'];
   ```
4. Tambahkan kartu baru di `index.html` (bagian grid tema)

---

## 🖼️ Mengganti Logo

Ganti `widget/assets/logo.png` dengan logo toko kamu.
- Ukuran: **80×80px** atau lebih (persegi)
- Format: PNG dengan background transparan

---

## 📦 Embed ke Website

```html
<iframe
  src="https://domain-kamu.com/hallogais-chat/widget/chat.html?theme=clean-gais&store=NamaToko"
  style="position:fixed;bottom:0;right:0;width:420px;height:640px;border:none;z-index:9999;"
></iframe>
```

---

*Dibuat dengan ❤️ oleh HalloGais*
