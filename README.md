# Dompet Harian

Aplikasi pencatat pengeluaran harian — 100% offline, single-file engine.
Saldo multi-dompet (Tunai, DANA, GoPay, OVO, Bank), batas belanja harian,
target ojol + streak, anggaran bulanan per kategori, target nabung,
utang/piutang, transaksi berulang, arsip bulanan, export CSV + backup JSON.

Dibangun dengan Capacitor v6 (web app + WebView Android). Folder native
`android/` tidak ikut ter-commit — folder itu di-generate di CI oleh
GitHub Actions (`npx cap add android` + `npx cap sync android`).

## Build APK

Setiap push ke `main` menjalankan workflow **Build Android APK** (file
`.github/workflows/build-android-apk.yml` — file ini tidak bisa di-push
oleh aplikasi GitHub, jadi ditambahkan manual lewat GitHub web).
Hasilnya: file `dompet-harian-v1.0.apk` (Debug APK, sudah ter-sign
keystore debug sehingga langsung bisa di-install) di tab Actions →
Artifacts. Push dengan tag juga membuat GitHub Release.
