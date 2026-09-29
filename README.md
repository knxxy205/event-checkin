# Rsvply — Event Check-in Dashboard

Admin dashboard untuk mengelola tamu event, membuat QR pass unik, dan mencatat check-in tanpa duplikasi.

## Run

```bash
npm install
npm run dev -- --host 0.0.0.0 --port 3200
```

Buka `http://localhost:3200` atau IP server di jaringan lokal.

## Demo flow

1. Buka menu **QR codes**.
2. Download QR/PNG tamu.
3. Buka menu **Check-in** atau tombol **Open scanner**.
4. Masukkan kode `RSV-0828`.
5. Check-in kedua dengan kode sama akan ditolak.
6. Menu **Guests** menyediakan search/filter.
7. **Export** mengunduh CSV.

Demo state tersimpan di browser `localStorage`, bukan database production.

## Scope MVP

- Overview attendance.
- Guest list search/filter.
- QR unik per guest dengan `qrcode`.
- Download QR PNG.
- Manual code check-in dengan duplicate protection.
- CSV export.
- Responsive mobile drawer.

## Next production work

- Express API + SQLite/PostgreSQL.
- Admin authentication.
- Camera QR decoding.
- Server-side idempotent check-in constraint.
- Event and guest CRUD.

## Quality direction

UI follows local `DESIGN.md` and `anti-slop` rules from [miqdadbadjuber/anti-slop](https://github.com/miqdadbadjuber/anti-slop). It is used as a build/audit rulebook, not as a runtime dependency.
