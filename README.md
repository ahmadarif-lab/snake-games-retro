# 🐍 Retro Snake // Obstacle Zone

Game **Snake** klasik bergaya **retro CRT** (layar hijau + scanline) yang dibuat murni dengan **HTML + CSS + JavaScript** dalam satu file `index.html`. Tanpa framework, tanpa build step, tanpa dependency eksternal — tinggal buka di browser.

![Retro Snake](https://img.shields.io/badge/HTML-Vanilla_JS-39ff8a?style=flat-square) ![No Dependencies](https://img.shields.io/badge/dependencies-0-2fa34d?style=flat-square)

## ✨ Fitur

- 🕹️ **Tampilan retro** — nuansa monitor CRT hijau lengkap dengan efek *scanline*, *glow*, dan *vignette*.
- 🧱 **Tembok batas + obstacle tengah** — seluruh sisi arena adalah tembok, plus halangan simetris di tengah yang menabraknya = kalah.
- 👾 **Musuh acak (random tapi valid)** — musuh berkeliaran ke sel yang selalu legal (tak menembus tembok/obstacle, tak menumpuk, tak menabrak ular). Musuh jadi **rintangan bergerak** — kamu kalah kalau *kamu* yang menabraknya.
- 📈 **Level & percepatan** — tiap 4 buah naik level: kecepatan bertambah dan musuh baru muncul (maks 8).
- 🏆 **High score** tersimpan di `localStorage`.
- ⏸️ **Pause**, overlay start/game-over, dan dukungan **swipe** untuk layar sentuh.

## 🎮 Cara Main

| Aksi | Tombol |
|------|--------|
| Gerak | `↑ ↓ ← →` atau `W A S D` |
| Jeda / lanjut | `Space` |
| Mulai / ulang | `Enter` (atau klik layar) |
| Sentuh (HP/tablet) | *Swipe* ke arah tujuan |

**Tujuan:** makan buah kuning untuk tumbuh & menambah skor. Hindari tembok, obstacle, tubuh sendiri, dan musuh merah.

## 🚀 Menjalankan Secara Lokal

Cukup buka `index.html` langsung di browser. Atau jalankan lewat server statis kecil:

```bash
# Python
python3 -m http.server 8000
# lalu buka http://localhost:8000
```

## 🌐 Deploy ke GitHub Pages

Karena ini file statis mandiri, cukup:

1. Push repo ini ke GitHub.
2. Buka **Settings → Pages → Source: Deploy from a branch → Branch: `main` / `/(root)`**.
3. Game live di `https://<username>.github.io/snake-games-retro/`.

File `.nojekyll` sudah disertakan agar GitHub Pages menyajikan file apa adanya.

## 🛠️ Teknologi

- HTML5 `<canvas>` untuk render grid game.
- Vanilla JavaScript (game loop `requestAnimationFrame` dengan *fixed timestep* + clamp `dt`).
- CSS murni untuk seluruh tampilan retro.

## 📁 Struktur

```
.
├── index.html   # seluruh game (HTML + CSS + JS)
├── .nojekyll    # pengaman GitHub Pages
└── README.md
```

## 📄 Lisensi

Bebas digunakan dan dimodifikasi (MIT).
