# Technical Document

## Pertemuan 1: Pengenalan JavaScript & Setup


| Field              | Detail                                                    |
| ------------------ | --------------------------------------------------------- |
| **Mata Pelajaran** | Pemrograman Web / JavaScript                              |
| **Kelas**          | XI – XII RPL                                              |
| **Pertemuan**      | #1 — Fase 1: JavaScript Core                              |
| **Durasi**         | 90 menit (2 JP)                                           |
| **Teknologi**      | HTML5 + JavaScript (Vanilla)                              |
| **Tipe Latihan**   | Individual                                                |
| **Prasyarat**      | HTML5 & CSS3 *(diasumsikan sudah dikuasai di kelas lain)* |
| **Versi Dokumen**  | 1.0                                                       |
| **Tanggal**        | Agustus 2026                                              |


---



## Daftar Isi

1. [Ringkasan Latihan](#1-ringkasan-latihan)
2. [Tujuan Pembelajaran](#2-tujuan-pembelajaran)
3. [Spesifikasi Teknis](#3-spesifikasi-teknis)
4. [Struktur File & Arsitektur](#4-struktur-file--arsitektur)
5. [Rencana Waktu (90 Menit)](#5-rencana-waktu-90-menit)
6. [Spesifikasi File](#6-spesifikasi-file)
7. [Panduan JavaScript (Referensi Lengkap)](#7-panduan-javascript-referensi-lengkap)
8. [Langkah Pengerjaan Step-by-Step](#8-langkah-pengerjaan-step-by-step)
9. [Clue & Penjelasan Kode per Bagian](#9-clue--penjelasan-kode-per-bagian)
10. [Checklist Penilaian](#10-checklist-penilaian)
11. [Troubleshooting](#11-troubleshooting)
12. [Referensi](#12-referensi)

---



## 1. Ringkasan Latihan

Siswa membuat **project Hello JavaScript** pertama — sebuah halaman HTML sederhana yang terhubung ke file JavaScript eksternal. Latihan ini dirancang agar siswa **memahami peran JavaScript di web** dan terbiasa menggunakan **Browser DevTools Console** sebagai alat debugging.

### Konsep Latihan

JavaScript adalah bahasa pemrograman yang membuat halaman web **interaktif**. Di pertemuan ini, fokus bukan tampilan visual — melainkan **menulis perintah JS** dan **melihat outputnya** di Console browser.

### Output yang Diharapkan

```
meet-1-latihan/
├── index.html          → Halaman HTML dengan tag <script>
└── js/
    └── main.js         → File JavaScript dengan 5+ perintah console
```



### Deliverable (Wajib Dikumpulkan)


| No  | Deliverable  | Keterangan                                     |
| --- | ------------ | ---------------------------------------------- |
| 1   | `index.html` | Halaman HTML valid dengan external script      |
| 2   | `js/main.js` | Minimal **5 perintah** `console.log()` berbeda |
| 3   | Screenshot   | DevTools Console menampilkan semua output      |


---



## 2. Tujuan Pembelajaran

Setelah menyelesaikan pertemuan ini, siswa diharapkan mampu:


| No  | Kompetensi                                                    |
| --- | ------------------------------------------------------------- |
| 1   | Menjelaskan peran JavaScript di ekosistem web (HTML, CSS, JS) |
| 2   | Menghubungkan file JavaScript ke HTML dengan tag `<script>`   |
| 3   | Membedakan **inline script** vs **external script**           |
| 4   | Menulis perintah `console.log()` untuk menampilkan output     |
| 5   | Membuka dan menggunakan **Browser DevTools Console**          |
| 6   | Membaca output dan error di Console                           |
| 7   | Menyusun struktur folder project JavaScript yang rapi         |


---



## 3. Spesifikasi Teknis



### 3.1 Aturan Wajib


| Aturan                  | Keterangan                                                     |
| ----------------------- | -------------------------------------------------------------- |
| **HTML5 Doctype**       | Wajib `<!DOCTYPE html>`                                        |
| **Bahasa dokumen**      | Wajib `<html lang="id">`                                       |
| **Encoding**            | Wajib `<meta charset="UTF-8">`                                 |
| **External script**     | JavaScript **WAJIB** di file terpisah `js/main.js`             |
| **Posisi script**       | Tag `<script>` **WAJIB** di akhir `<body>` (sebelum `</body>`) |
| **Minimal console.log** | **Minimal 5** perintah `console.log()` di `main.js`            |
| **Tanpa framework**     | Tidak boleh React, Vue, jQuery, atau library lain              |
| **Komentar JS**         | Minimal 3 komentar `//` atau `/* */` di `main.js`              |
| **DevTools Console**    | Semua output harus terlihat di Console (bukan `alert()`)       |




### 3.2 Perintah console.log Wajib

File `main.js` **WAJIB** memuat minimal output berikut:


| No  | Jenis Output             | Contoh                               | Wajib |
| --- | ------------------------ | ------------------------------------ | ----- |
| 1   | Teks/string              | `console.log("Hello, JavaScript!");` | ✓     |
| 2   | Angka                    | `console.log(2026);`                 | ✓     |
| 3   | Operasi matematika       | `console.log(10 + 5);`               | ✓     |
| 4   | Variabel (diperkenalkan) | `console.log(nama);`                 | ✓     |
| 5   | Kombinasi teks + angka   | `console.log("Tahun:", 2026);`       | ✓     |




### 3.3 Eksplorasi Console (Bonus)

Siswa **disarankan** mencoba perintah berikut langsung di Console DevTools (tidak wajib di file):


| Perintah                                         | Fungsi                       |
| ------------------------------------------------ | ---------------------------- |
| `console.warn("Peringatan!")`                    | Output peringatan (kuning)   |
| `console.error("Error!")`                        | Output error (merah)         |
| `console.table([{nama: "Budi"}, {nama: "Ani"}])` | Tampilkan data sebagai tabel |
| `clear()`                                        | Bersihkan Console            |


---



## 4. Struktur File & Arsitektur



### 4.1 Diagram Alur Eksekusi

```
┌─────────────────────────────────────────────────────────────┐
│                        Browser                               │
│                                                              │
│  1. Load index.html                                          │
│         │                                                    │
│         ▼                                                    │
│  2. Parse HTML → render halaman                              │
│         │                                                    │
│         ▼                                                    │
│  3. Temukan <script src="js/main.js">                        │
│         │                                                    │
│         ▼                                                    │
│  4. Download & jalankan main.js                              │
│         │                                                    │
│         ▼                                                    │
│  5. console.log() → output ke DevTools Console               │
│                                                              │
└─────────────────────────────────────────────────────────────┘
```



### 4.2 Peran HTML, CSS, dan JavaScript

```
┌──────────────┐   ┌──────────────┐   ┌──────────────┐
│     HTML     │   │     CSS      │   │  JavaScript  │
│  (Struktur)  │ + │  (Tampilan)  │ + │  (Interaksi) │
│              │   │              │   │              │
│  "Apa ada     │   │  "Seperti    │   │  "Apa yang   │
│   di halaman" │   │   apa bentuk │   │   terjadi    │
│              │   │   dan warna" │   │   saat klik"  │
└──────────────┘   └──────────────┘   └──────────────┘
       ↑                  ↑                    ↑
  (kelas lain)       (kelas lain)        (pertemuan ini)
```



### 4.3 Template Struktur Dasar

`index.html` **— skeleton wajib:**

```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="description" content="Latihan JavaScript Pertemuan 1">
    <meta name="author" content="Nama Siswa">
    <title>Hello JavaScript | Nama Siswa</title>
</head>
<body>

    <!-- Konten HTML di sini -->

    <script src="js/main.js"></script>
    <!-- CLUE: Script di AKHIR body agar HTML load dulu -->

</body>
</html>
```

`js/main.js` **— skeleton wajib:**

```javascript
// File: main.js
// Pertemuan 1 — Pengenalan JavaScript
// Nama: [Nama Siswa]

console.log("Hello, JavaScript!");
```

---



## 5. Rencana Waktu (90 Menit)


| Waktu             | Durasi   | Aktivitas                               | Output                                 |
| ----------------- | -------- | --------------------------------------- | -------------------------------------- |
| **00:00 – 00:15** | 15 menit | Pengenalan JS & demo Console            | Paham role JS, buka DevTools           |
| **00:15 – 00:30** | 15 menit | Setup folder & file project             | Folder + `index.html` + `js/main.js`   |
| **00:30 – 00:50** | 20 menit | Tulis 5+ console.log di main.js         | File JS dengan output beragam          |
| **00:50 – 01:10** | 20 menit | Eksperimen Console & inline vs external | Paham perbedaan cara load script       |
| **01:10 – 01:25** | 15 menit | Latihan mandiri & eksplorasi            | Tambah output, coba console.warn/error |
| **01:25 – 01:30** | 5 menit  | Review, checklist, pengumpulan          | Screenshot Console + file dikumpulkan  |


> **Tips:** Buka DevTools **sebelum** refresh halaman agar tidak ketinggalan output `console.log()` yang dieksekusi saat page load.

---



## 6. Spesifikasi File



### 6.1 `index.html` — Halaman Utama


| Section | Isi Wajib                              | Tag/Elemen Utama            |
| ------- | -------------------------------------- | --------------------------- |
| Head    | Meta, title deskriptif                 | `<meta>`, `<title>`         |
| Header  | Judul halaman + nama siswa             | `<header>`, `<h1>`, `<p>`   |
| Main    | Paragraf penjelasan singkat tentang JS | `<main>`, `<p>`             |
| Footer  | Copyright + pertemuan ke               | `<footer>`, `<small>`       |
| Script  | Link ke external JS                    | `<script src="js/main.js">` |




### 6.2 `js/main.js` — File JavaScript


| Section           | Isi Wajib                            | Sintaks Utama           |
| ----------------- | ------------------------------------ | ----------------------- |
| Header comment    | Nama file, pertemuan, nama siswa     | `//` atau `/* */`       |
| Hello World       | Output sapaan pertama                | `console.log("...")`    |
| Output angka      | Literal number & operasi             | `console.log(10+5)`     |
| Output variabel   | Deklarasi + tampilkan variabel       | `let` + `console.log`   |
| Output kombinasi  | String + angka dalam satu log        | `console.log("...", x)` |
| Komentar penjelas | Minimal 3 komentar di bagian penting | `//`                    |




### 6.3 Contoh Output Console yang Diharapkan

```
Hello, JavaScript!
2026
15
Budi Santoso
Tahun: 2026
Saya belajar JavaScript di pertemuan 1
```

*(Urutan dan isi boleh berbeda, asalkan 5+ baris output)*

---



## 7. Panduan JavaScript (Referensi Lengkap)



### 7.1 Apa itu JavaScript?


| Aspek              | Penjelasan                      | Clue untuk Siswa                              |
| ------------------ | ------------------------------- | --------------------------------------------- |
| **Definisi**       | Bahasa pemrograman untuk web    | Bukan HTML, bukan CSS — ini logic & interaksi |
| **Di mana jalan?** | Browser (Chrome, Firefox, Edge) | Tidak perlu install compiler di pertemuan 1   |
| **Versi**          | ES6+ (ECMAScript 2015+)         | Sintaks modern: `let`, arrow function, dll.   |
| **File extension** | `.js`                           | Simpan di folder `js/` untuk rapi             |




### 7.2 Tag `<script>` — Cara Load JavaScript


| Metode                          | Sintaks                               | Kapan Dipakai                            |
| ------------------------------- | ------------------------------------- | ---------------------------------------- |
| **External** *(wajib)*          | `<script src="js/main.js"></script>`  | Project nyata — file terpisah            |
| **Inline** *(demo saja)*        | `<script>console.log("hi");</script>` | Latihan cepat — **jangan** untuk project |
| **Di** `<head>`                 | `<script src="..." defer></script>`   | Advanced — nanti di pertemuan mendatang  |
| **Di akhir** `<body>` *(wajib)* | Sebelum `</body>`                     | **Best practice** untuk pemula           |


**Mengapa script di akhir body?**

```
HTML load dulu → user lihat konten → baru JS jalan
```

Kalau script di `<head>` tanpa `defer`, browser bisa "freeze" render halaman sambil menunggu JS selesai.

### 7.3 `console.log()` — Output ke Console


| Sintaks       | Contoh                         | Output di Console |
| ------------- | ------------------------------ | ----------------- |
| String        | `console.log("Halo");`         | `Halo`            |
| Number        | `console.log(42);`             | `42`              |
| Expression    | `console.log(7 * 6);`          | `42`              |
| Variable      | `console.log(nama);`           | nilai variabel    |
| Multiple args | `console.log("Umur:", 17);`    | `Umur: 17`        |
| String concat | `console.log("Halo " + nama);` | `Halo Budi`       |




### 7.4 Komentar JavaScript


| Jenis       | Sintaks                         | Clue untuk Siswa                                |
| ----------- | ------------------------------- | ----------------------------------------------- |
| Single-line | `// komentar satu baris`        | Paling sering dipakai                           |
| Multi-line  | `/* komentar beberapa baris */` | Untuk blok penjelasan                           |
| **Fungsi**  | Dokumentasi & non-aktifkan kode | Browser **abaikan** komentar — tidak dijalankan |




### 7.5 Variabel (Pengenalan Singkat)


| Keyword | Bisa diubah? | Contoh                | Clue                                         |
| ------- | ------------ | --------------------- | -------------------------------------------- |
| `let`   | Ya           | `let nama = "Budi";`  | Pakai jika nilai bisa berubah                |
| `const` | Tidak        | `const tahun = 2026;` | Pakai jika nilai tetap — **default pilihan** |


> **Catatan:** Topik variabel akan dibahas **lebih dalam di Pertemuan 2**. Di pertemuan 1 cukup pakai 1–2 variabel untuk demo `console.log`.



### 7.6 Browser DevTools Console


| Langkah             | Windows/Linux                 | Mac                |
| ------------------- | ----------------------------- | ------------------ |
| Buka DevTools       | `F12` atau `Ctrl + Shift + I` | `Cmd + Option + I` |
| Langsung ke Console | `Ctrl + Shift + J`            | `Cmd + Option + J` |
| Refresh halaman     | `F5` atau `Ctrl + R`          | `Cmd + R`          |
| Hard refresh        | `Ctrl + Shift + R`            | `Cmd + Shift + R`  |


**Panel Console — yang perlu dikenali:**

```
Console
├── ▶ Output console.log()     ← hijau/putih, normal
├── ⚠ console.warn()           ← kuning, peringatan
├── ✖ console.error()          ← merah, error
└── > _                        ← prompt: ketik JS langsung di sini
```

---



## 8. Langkah Pengerjaan Step-by-Step



### Step 1 — Buat Struktur Folder (5 menit)

```
1. Buat folder: meet-1-latihan/
2. Buat subfolder: js/
3. Buat file: index.html (di root folder)
4. Buat file: js/main.js
```



### Step 2 — Tulis Skeleton HTML (10 menit)

1. Copy template dari [Bagian 4.3](#43-template-struktur-dasar)
2. Ganti `[Nama Siswa]` dengan nama Anda
3. Tambahkan `<header>`, `<main>`, `<footer>` dengan konten singkat
4. Pastikan `<script src="js/main.js"></script>` ada **sebelum** `</body>`



### Step 3 — Tulis Hello World di main.js (10 menit)

```javascript
// File: main.js
// Pertemuan 1 — Pengenalan JavaScript
// Nama: Budi Santoso

console.log("Hello, JavaScript!");
```



### Step 4 — Buka di Browser & DevTools (5 menit)

1. Buka `index.html` di browser (double-click atau Live Server)
2. Tekan `F12` → klik tab **Console**
3. Pastikan muncul: `Hello, JavaScript!`
4. Jika tidak muncul → lihat [Troubleshooting](#11-troubleshooting)



### Step 5 — Tambah 4+ console.log Lainnya (20 menit)

Ikuti spesifikasi di [Bagian 3.2](#32-perintah-consolelog-wajib):

```javascript
console.log(2026);                  // angka
console.log(10 + 5);                // operasi
let nama = "Budi Santoso";          // variabel
console.log(nama);                  // output variabel
console.log("Tahun:", 2026);        // kombinasi
```



### Step 6 — Eksperimen Inline vs External (15 menit)

**A. External (sudah ada):**

```html
<script src="js/main.js"></script>
```

**B. Inline (coba sementara, lalu hapus):**

```html
<script>
    console.log("Ini inline script");
</script>
```

**Diskusi:** Mana yang lebih rapi untuk project besar? → **External**

### Step 7 — Eksplorasi Console Interaktif (15 menit)

Ketik langsung di prompt Console (bukan di file):

```javascript
2 + 2
"Hello" + " World"
console.warn("Ini peringatan")
console.error("Ini error contoh")
```



### Step 8 — Validasi & Pengumpulan (10 menit)

1. Refresh halaman — semua output muncul
2. Centang [Checklist Penilaian](#10-checklist-penilaian)
3. Screenshot Console
4. Kumpulkan folder `meet-1-latihan/`

---



## 9. Clue & Penjelasan Kode per Bagian



### 9.1 Clue: `index.html`

```html
<!DOCTYPE html>
<!-- CLUE: Baris pertama WAJIB. Memberi tahu browser "ini HTML5" -->
<html lang="id">
<!-- CLUE: lang="id" = bahasa Indonesia -->

<head>
    <meta charset="UTF-8">
    <!-- CLUE: UTF-8 support karakter Indonesia & emoji -->

    <meta name="description" content="Latihan JavaScript Pertemuan 1 - Hello JavaScript">
    <!-- CLUE: description untuk SEO, tidak tampil di halaman -->

    <meta name="author" content="Budi Santoso">
    <title>Hello JavaScript | Budi Santoso</title>
    <!-- CLUE: Judul tab browser -->
</head>

<body>

    <header>
        <h1>Hello JavaScript!</h1>
        <!-- CLUE: h1 = judul utama halaman -->

        <p>Latihan Pertemuan 1 — <strong>Budi Santoso</strong></p>
        <!-- CLUE: strong = teks penting (tebal) -->
    </header>

    <main>
        <!-- CLUE: main = konten utama, hanya 1 per halaman -->

        <p>
            Buka <em>Browser DevTools Console</em> (tekan F12) untuk melihat
            output JavaScript dari file <code>js/main.js</code>.
        </p>
        <!-- CLUE: em = penekanan, code = teks kode inline -->

        <p>
            JavaScript adalah bahasa pemrograman yang membuat halaman web
            menjadi interaktif. Di pertemuan ini, kita belum mengubah tampilan
            halaman — fokus pada menulis kode dan melihat output di Console.
        </p>
    </main>

    <footer>
        <hr>
        <!-- CLUE: hr = garis pemisah horizontal -->

        <p>
            <small>&copy; 2026 Budi Santoso — Pertemuan 1 JavaScript</small>
            <!-- CLUE: small = teks kecil, &copy; = simbol © -->
        </p>
    </footer>

    <script src="js/main.js"></script>
    <!-- CLUE: src = path ke file JS eksternal -->
    <!-- CLUE: Posisi di AKHIR body = best practice -->
    <!-- CLUE: Browser download main.js lalu jalankan isinya -->

</body>
</html>
```

---



### 9.2 Clue: `js/main.js`

```javascript
// =============================================
// File: main.js
// Pertemuan 1 — Pengenalan JavaScript
// Nama: Budi Santoso
// =============================================
// CLUE: Blok komentar di atas = header file, good practice


// --- 1. Hello World ---
console.log("Hello, JavaScript!");
// CLUE: console.log() = cetak output ke DevTools Console
// CLUE: Teks dalam tanda kutip "" = string (teks)


// --- 2. Output Angka ---
console.log(2026);
// CLUE: Angka tanpa kutip = number type
// CLUE: Tidak perlu kutip untuk angka


// --- 3. Operasi Matematika ---
console.log(10 + 5);
// CLUE: JS bisa hitung langsung di dalam console.log()
// CLUE: Output di Console: 15 (bukan "10 + 5")


// --- 4. Variabel ---
let nama = "Budi Santoso";
// CLUE: let = deklarasi variabel yang bisa diubah
// CLUE: = artinya "simpan nilai ke variabel"

const kelas = "XI RPL";
// CLUE: const = variabel konstan, nilai tidak boleh diubah
// CLUE: Default: pakai const kecuali nilai perlu berubah

console.log(nama);
// CLUE: Output nilai variabel, bukan teks "nama"
// CLUE: Console menampilkan: Budi Santoso

console.log(kelas);
// CLUE: Sama — output isi variabel kelas


// --- 5. Kombinasi Teks + Angka ---
console.log("Tahun:", 2026);
// CLUE: Bisa kirim banyak argumen, dipisah koma
// CLUE: Output: Tahun: 2026

console.log("Nama:", nama, "| Kelas:", kelas);
// CLUE: Gabungkan string dan variabel dalam satu log
// CLUE: Output: Nama: Budi Santoso | Kelas: XI RPL


// --- 6. Eksperimen Tambahan (opsional) ---
console.log("2 + 2 =", 2 + 2);
// CLUE: String + hasil operasi dalam satu baris

console.warn("Ini peringatan — bukan error!");
// CLUE: console.warn = output kuning, untuk peringatan

console.error("Ini contoh error — jangan panik!");
// CLUE: console.error = output merah, untuk error
// CLUE: Ini BUKAN error beneran — cuma demo format output
```

---



### 9.3 Clue: Eksperimen di Console (Langsung di Browser)

Buka DevTools Console, ketik satu per satu di prompt `>`:

```javascript
// CLUE: Di Console, tidak perlu console.log untuk angka/operasi
// CLUE: Console otomatis tampilkan hasil evaluasi

"Hello" + " " + "World"
// CLUE: + pada string = gabung (concatenation)
// Output: "Hello World"

typeof "teks"
// CLUE: typeof = cek tipe data
// Output: "string"

typeof 42
// Output: "number"

typeof true
// Output: "boolean"

let x = 10;
let y = 20;
console.log(x + y);
// Output: 30

clear()
// CLUE: Bersihkan semua output di Console
```

---



## 10. Checklist Penilaian



### A. Struktur Project (25 poin)


| No  | Kriteria                                          | Poin | ✓   |
| --- | ------------------------------------------------- | ---- | --- |
| 1   | Folder rapi: `index.html` + `js/main.js`          | 5    |     |
| 2   | HTML valid: doctype, charset, title               | 5    |     |
| 3   | Tag `<script src="js/main.js">` di akhir `<body>` | 5    |     |
| 4   | JavaScript di file eksternal (bukan inline)       | 5    |     |
| 5   | Header comment di `main.js` (nama, pertemuan)     | 5    |     |




### B. JavaScript & Console (45 poin)


| No  | Kriteria                                         | Poin | ✓   |
| --- | ------------------------------------------------ | ---- | --- |
| 6   | Minimal 5 perintah `console.log()` berbeda       | 15   |     |
| 7   | Ada output string, angka, dan operasi matematika | 10   |     |
| 8   | Ada penggunaan variabel (`let` atau `const`)     | 10   |     |
| 9   | Output tampil di DevTools Console (screenshot)   | 10   |     |




### C. Komentar & Dokumentasi (15 poin)


| No  | Kriteria                                       | Poin | ✓   |
| --- | ---------------------------------------------- | ---- | --- |
| 10  | Minimal 3 komentar `//` di `main.js`           | 10   |     |
| 11  | Komentar menjelaskan bagian kode (bukan noise) | 5    |     |




### D. Pemahaman Konsep (15 poin)


| No  | Kriteria                                             | Poin | ✓   |
| --- | ---------------------------------------------------- | ---- | --- |
| 12  | Bisa jelaskan peran JS vs HTML vs CSS (oral/written) | 5    |     |
| 13  | Bisa jelaskan beda inline vs external script         | 5    |     |
| 14  | Bisa buka DevTools Console mandiri                   | 5    |     |


**Total: 100 poin**


| Grade | Rentang  |
| ----- | -------- |
| A     | 85 – 100 |
| B     | 70 – 84  |
| C     | 55 – 69  |
| D     | < 55     |


---



## 11. Troubleshooting


| Masalah                                     | Penyebab                                       | Solusi                                                   |
| ------------------------------------------- | ---------------------------------------------- | -------------------------------------------------------- |
| Console kosong, tidak ada output            | DevTools dibuka **setelah** page load          | Refresh halaman (`F5`) setelah Console terbuka           |
| `Failed to load resource: 404`              | Path `src` salah                               | Pastikan file ada di `js/main.js`, cek huruf besar/kecil |
| `Uncaught ReferenceError: x is not defined` | Variabel belum dideklarasi                     | Tambahkan `let x = ...` sebelum `console.log(x)`         |
| Output muncul di halaman, bukan Console     | Pakai `document.write()` bukan `console.log()` | Ganti ke `console.log()`                                 |
| Script tidak jalan sama sekali              | Tag `<script>` typo atau path salah            | Cek `src="js/main.js"` — tanpa `/` di depan              |
| `Unexpected token` error                    | Syntax error (titik koma, kutip)               | Cek tanda kutip `"` sudah ditutup, syntax benar          |
| Inline script jalan, external tidak         | File path atau nama file salah                 | Pastikan folder `js/` sejajar dengan `index.html`        |
| Output dobel (2x)                           | Tag `<script>` terduplikasi                    | Hapus duplikat, cukup **1** tag script                   |
| Karakter aneh di output                     | Encoding bukan UTF-8                           | Pastikan `<meta charset="UTF-8">` ada di `<head>`        |
| Live Server vs double-click                 | Keduanya valid                                 | Double-click cukup untuk pertemuan 1                     |




### Cara Debug Cepat (3 Langkah)

```
1. F12 → tab Console → baca pesan error (merah)
2. Cek nomor baris error → buka main.js di baris tersebut
3. Fix error → save → refresh browser → cek Console lagi
```

---



## 12. Referensi



### Dokumentasi

- [MDN — JavaScript Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)
- [MDN — console.log()](https://developer.mozilla.org/en-US/docs/Web/API/console/log)
- [MDN —](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script) `<script>` [tag](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/script)
- [JavaScript.info — Pengenalan](https://javascript.info/intro)



### Roadmap

- Pertemuan sebelumnya: *(HTML & CSS — kelas lain)*
- **Pertemuan ini:** #1 — Pengenalan JavaScript & Setup
- Pertemuan berikutnya: #2 — Variabel & Tipe Data *(lihat* `ROADMAP.md`*)*



### Tools

- [VS Code](https://code.visualstudio.com/) — code editor
- [Live Server Extension](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) — opsional, auto-refresh browser

---

*Dokumen ini bagian dari roadmap JavaScript → TypeScript. Lihat* `ROADMAP.md` *untuk alur 40 pertemuan lengkap.*