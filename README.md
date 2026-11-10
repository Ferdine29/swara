# Swara

Aplikasi suara mesin untuk motor listrik. Aplikasi membaca kecepatan dari GPS HP, mengubahnya menjadi putaran mesin (RPM) dan gigi virtual 1 sampai 6, lalu membuat suara mesin motor besar secara sintetis. Suara diputar lewat speaker Bluetooth motor, misalnya speaker dual-channel bawaan Omoway Omo X.

Aplikasi ini berbentuk PWA (Progressive Web App): satu kode untuk Android dan iPhone, gratis, tanpa Play Store atau App Store, dan bisa dipasang ke layar utama seperti aplikasi biasa. Setelah dibuka sekali, aplikasi tetap jalan tanpa sinyal internet.

## Fitur

- 17 pilihan suara mesin: Inline-4 Supersport 600cc (lengkingan tinggi), Big Twin 2100cc, V-Twin 1800cc, L-Twin 1300cc, V-Twin 1350cc, Inline-4 1000cc (biasa, crossplane, supercharged), Inline-4 1400cc, V4 1100cc dan 1300cc, Triple 900cc dan 2500cc, Boxer 1300cc, Flat-6 1830cc, Inline-6 1650cc, dan V8 5700cc.
- Semua suara dibuat secara sintetis dari urutan pengapian tiap jenis mesin. Tidak memakai rekaman atau merek pabrikan mana pun.
- Pengaturan suara: volume, penguat (agar lebih keras di speaker kecil), bass, nada, kekasaran, dan letupan knalpot saat gas dilepas.
- Saat berhenti: langsam terus, langsam 10 detik lalu senyap, atau senyap. Volume langsam bisa diatur.
- Gaya perpindahan gigi: Santai atau Sport.
- Efek suara: klakson dua nada (tahan tombol), peringatan pejalan kaki di bawah 20 km/j, dan sapaan saat mesin dinyalakan.
- Mode Pameran: sirene wail, yelp, dan hi-lo yang hanya bisa dibunyikan saat motor diam dan mati otomatis saat motor bergerak. Sirene di jalan raya dilarang untuk kendaraan pribadi (UU 22/2009 Pasal 59 dan 287 ayat 4).
- Kecepatan maksimal motor bisa diatur. Bawaannya 113 km/j sesuai Omoway Omo X.
- Mode simulasi untuk mencoba suara tanpa berkendara.

## Cara pakai di motor

1. Nyalakan Omo X dan sambungkan HP ke speaker Bluetooth motor dari menu Bluetooth HP.
2. Buka aplikasi, pilih suara mesin, lalu tekan **Nyalakan mesin**.
3. Izinkan akses lokasi saat diminta.
4. Pasang HP di holder dengan layar tetap menyala. Aplikasi meminta layar tidak mati otomatis, tetapi jangan kunci layar karena browser menghentikan suara saat layar terkunci.

Catatan: GPS HP diperbarui sekitar sekali per detik, jadi aplikasi menghaluskan perubahan kecepatan. Speaker Bluetooth juga punya jeda sekitar 0,1 sampai 0,3 detik. Keduanya normal.

## Memasang ke layar utama

- **Android (Chrome):** buka alamat aplikasi, ketuk menu titik tiga, pilih **Tambahkan ke layar utama** atau **Instal aplikasi**.
- **iPhone (Safari):** buka alamat aplikasi, ketuk tombol Bagikan, pilih **Tambah ke Layar Utama**.

## Hosting gratis dengan GitHub Pages

1. Di repositori ini buka **Settings → Pages**.
2. Pada **Build and deployment**, pilih **Deploy from a branch**, branch `main`, folder `/ (root)`, lalu **Save**.
3. Setelah 1 sampai 2 menit, aplikasi bisa dibuka di `https://<username>.github.io/swara/`.

GPS di browser hanya jalan lewat HTTPS, dan GitHub Pages sudah HTTPS.

## Struktur file

- `src-app.html`: isi aplikasi (tampilan, mesin suara, GPS, gigi virtual). Edit file ini.
- `build.py`: membungkus `src-app.html` menjadi `index.html` lengkap. Jalankan `python3 build.py` setelah mengedit.
- `index.html`, `manifest.webmanifest`, `sw.js`, ikon: file PWA yang dihosting.

## Batasan

- Suara berhenti jika layar dikunci atau aplikasi ditutup. Untuk tetap bersuara saat layar mati perlu aplikasi native (Android .apk atau iOS), yang bisa dibuat nanti dari kode yang sama.
- Pakai dengan volume yang wajar dan patuhi aturan kebisingan setempat.
