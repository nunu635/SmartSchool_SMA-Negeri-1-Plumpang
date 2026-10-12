# SmartSchool Premium — Student Workspace

Proyek tugas akhir jurusan IT berupa prototipe sistem informasi akademik dengan HTML, CSS, dan JavaScript murni. Antarmuka dirancang minimalis premium, responsif, dan dapat dijalankan tanpa proses build.

## Fitur

- Dashboard akademik dengan ringkasan nilai, kehadiran, kelas hari ini, dan tugas.
- Jadwal mingguan interaktif (Senin–Minggu), status kelas berlangsung/berikutnya, tambah/edit/hapus kelas (hari, jam, mata pelajaran, guru, ruangan), dan validasi bentrok waktu.
- Pengelolaan tugas: tambah, edit, hapus, cari, filter, prioritas, status selesai.
- Rekap nilai: grafik batang, rata-rata otomatis, edit nilai, ekspor JSON.
- Rekap kehadiran: tambah, edit, hapus catatan (Hadir/Terlambat/Izin/Alpha), statistik otomatis, filter bulan, dan ekspor JSON.
- Catatan belajar: tambah, edit, hapus, dan pencarian.
- Profil dan pengaturan tema terang/gelap.
- Ekspor data JSON dan pemulihan data contoh.
- Penyimpanan lokal menggunakan `localStorage`.

## Menjalankan di VS Code

1. Ekstrak ZIP.
2. Buka folder `SmartSchool-Premium` di VS Code.
3. Disarankan pasang ekstensi **Live Server**.
4. Klik kanan `index.html` → **Open with Live Server**.
5. Tidak perlu `npm install`, server backend, atau API key.

Bisa juga membuka `index.html` langsung di browser. Namun Live Server lebih disarankan agar perilaku penyimpanan browser konsisten.

## Struktur

```text
SmartSchool-Premium/
├── index.html
├── style.css
├── script.js
└── README.md
```

## Akun demo

Prototipe ini tidak menggunakan login, karena fokus versi ini adalah workspace siswa yang dapat langsung diuji. Semua data yang dapat diedit tersimpan di browser yang sama.

## Catatan akademik dan keamanan

Versi ini adalah **prototipe front-end**, bukan sistem produksi. `localStorage` menyimpan data pada browser/perangkat yang digunakan; data tidak otomatis tersinkron antarperangkat dan bukan database server. Jangan memasukkan informasi pribadi yang sensitif.

Untuk versi produksi, tambahkan backend (misalnya Node.js + Express), database relasional (misalnya MySQL/PostgreSQL), autentikasi server-side, kontrol akses berbasis peran, validasi di server, serta mekanisme backup.

## Ide alur presentasi

1. Jelaskan tujuan SmartSchool: satu workspace untuk jadwal, tugas, nilai, kehadiran, dan catatan.
2. Tunjukkan dashboard dan ringkasan akademik.
3. Pilih hari di halaman jadwal; tambahkan kelas dan coba masukkan jam yang bentrok untuk memperlihatkan validasi.
4. Tambahkan tugas, ubah statusnya menjadi selesai, lalu perhatikan progress dashboard.
5. Edit nilai dan lihat rata-rata berubah.
6. Buat catatan, cari catatan, lalu hapus jika perlu.
7. Ubah tema, edit profil, dan ekspor data JSON.
8. Jelaskan batasan `localStorage` serta rencana pengembangan backend dan database.

## Teknologi yang dipakai

- **HTML5** — struktur semantik dan form.
- **CSS3** — design system, layout grid/flex, responsive breakpoints, tema gelap.
- **JavaScript ES6+** — render UI, event delegation, CRUD lokal, pencarian/filter, validasi jadwal, ekspor JSON.
- **Web Storage API** — persistensi data pada browser.

Referensi konsep penyimpanan browser: [MDN — Window.localStorage](https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage).
