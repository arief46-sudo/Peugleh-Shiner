# Peugleh Shiner

Website pemesanan jasa kebersihan kos dan rumah: pilih layanan, hitung estimasi harga, lalu checkout lewat WhatsApp.

- `index.html` — website utama (HTML + CSS + JavaScript dalam satu file, tanpa dependensi)
- `assets/logo.png` — logo brand
- `peugleh-shiner-website-pembayaran.html` — file versi lama (arsip, tidak dipakai)

## Menjalankan secara lokal

Buka `index.html` langsung di browser, atau jalankan server statis:

```bash
python3 -m http.server 3000
```

Lalu buka <http://localhost:3000>.

## Mengubah data

| Yang diubah | Lokasi |
| --- | --- |
| Nomor WhatsApp admin | `const WHATSAPP_NUMBER` di dalam `<script>` (format `62...`, tanpa `+` dan spasi) |
| Nomor DANA / rekening BSI | teks catatan pada field **Metode pembayaran** dan konstanta `PAYMENT_INFO` |
| Harga layanan | objek `services` di `<script>` dan opsi `<select id="service">` |
| Opsi ukuran area / tambahan | `<select id="size">` dan `<select id="extra">` |
| Logo | ganti file `assets/logo.png` |

## Publikasi di GitHub Pages

Semua file statis berada di root repo, jadi tidak butuh proses build:

1. Buka **Settings → Pages** pada repo ini.
2. Pada **Build and deployment → Source**, pilih **Deploy from a branch**.
3. Pilih branch `main` dan folder `/ (root)`, lalu **Save**.
4. Website tersedia di `https://arief46-sudo.github.io/Peugleh-Shiner/` setelah proses deploy selesai (± 1 menit).

Setelah aktif, setiap `git push` ke `main` akan memperbarui website secara otomatis.
