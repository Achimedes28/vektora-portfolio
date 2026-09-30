# Vektora Project — Portfolio Website

Website portfolio Vektora Project: statis (HTML/CSS/JS), tanpa build step, siap di-deploy ke GitHub Pages atau Cloudflare Pages.

## Fitur
- Palet brand Vektora (hitam, biru Vektora #014468, putih) dengan tipografi raksasa (Anton + Space Grotesk via Google Fonts)
- Animasi: preloader, reveal per kata, huruf raksasa naik, panel "liquid" SVG bergerak, marquee yang bereaksi pada kecepatan scroll, galeri karya horizontal ter-pin (desktop), mockup dashboard beranimasi, counter, kursor kustom, tombol magnetik, tilt 3D kartu
- Smooth scroll (Lenis) + GSAP ScrollTrigger via CDN. Jika CDN gagal dimuat, semua konten tetap tampil tanpa animasi.
- Responsif (mobile: galeri jadi vertikal, menu burger) dan menghormati `prefers-reduced-motion`
- Form kontak membuka WhatsApp dengan pesan terisi (tidak ada data yang disimpan)

## Struktur
```
index.html
css/style.css
js/main.js
assets/           logo-mark.png
```

## Menjalankan lokal
```bash
python3 -m http.server 8000
# buka http://localhost:8000
```

## Deploy
**GitHub Pages:** Settings → Pages → Source: *Deploy from a branch* → `main` / root.

**Cloudflare Pages:** Create project → Connect to Git → pilih repo ini → Framework preset: *None*, build command kosong, output directory `/`.

## Mengubah isi
- Karya ada di `index.html` bagian `<section class="works">` — setiap `<article class="card">` satu karya.
- Label jujur (`Dipakai operasional`, `Demo produk`, `Dalam pengembangan`) sengaja dipertahankan. Ganti dengan studi kasus klien hanya setelah ada izin tertulis dari klien.
- Kontak (email, WhatsApp, Instagram) ada di hero, footer, dan `js/main.js` (nomor WA untuk form).
