# Roadmap Pembelajaran: JavaScript → TypeScript

## Informasi Kurikulum


| Field               | Detail                                            |
| ------------------- | ------------------------------------------------- |
| **Program**         | Rekayasa Perangkat Lunak (RPL)                    |
| **Target Kelas**    | XI – XII RPL                                      |
| **Durasi**          | 1 Tahun Ajaran (~40 minggu efektif)               |
| **Total Pertemuan** | 40 pertemuan (1× / minggu, ±90 menit)             |
| **Prasyarat**       | HTML5 & CSS3 *(diajarkan di kelas/mapel lain)*    |
| **Fokus**           | Fondasi JavaScript & TypeScript sebelum React/Vue |
| **Versi Dokumen**   | 1.0                                               |
| **Tanggal**         | Agustus 2026                                      |


---

## Daftar Isi

1. [Tujuan Pembelajaran](#1-tujuan-pembelajaran)
2. [Prasyarat & Asumsi](#2-prasyarat--asumsi)
3. [Alur Kurikulum](#3-alur-kurikulum)
4. [Fase 1 — JavaScript Core (Pertemuan 1–16)](#fase-1--javascript-core-pertemuan-116)
5. [Fase 2 — Async & API (Pertemuan 17–28)](#fase-2--async--api-pertemuan-1728)
6. [Fase 3 — TypeScript (Pertemuan 29–36)](#fase-3--typescript-pertemuan-2936)
7. [Fase 4 — Bridge ke Framework (Pertemuan 37–40)](#fase-4--bridge-ke-framework-pertemuan-3740)
8. [Project Portfolio](#project-portfolio)
9. [Checklist Siap React/Vue](#checklist-siap-reactvue)
10. [Rubrik Penilaian](#rubrik-penilaian)
11. [Referensi](#referensi)

---



## 1. Tujuan Pembelajaran

Setelah menyelesaikan roadmap ini, siswa diharapkan mampu:


| No  | Kompetensi                                                                   |
| --- | ---------------------------------------------------------------------------- |
| 1   | Menulis JavaScript modern (ES6+) dengan benar dan terstruktur                |
| 2   | Memanipulasi DOM dan menangani event tanpa framework                         |
| 3   | Mengelola data asynchronous dengan Promise dan async/await                   |
| 4   | Membangun aplikasi CRUD sederhana dengan Fetch API                           |
| 5   | Menerapkan TypeScript untuk type safety pada project JavaScript              |
| 6   | Memahami konsep component, state, dan props secara vanilla sebelum React/Vue |
| 7   | Debug error JavaScript/TypeScript secara mandiri                             |


---



## 2. Prasyarat & Asumsi



### Prasyarat (diasumsikan sudah dikuasai)

- Struktur HTML5 semantik (`header`, `nav`, `main`, `section`, dll.)
- CSS dasar (selector, box model, flexbox, responsive dasar)
- Familiar dengan browser DevTools (Elements tab)



### Asumsi pembelajaran

- 1 pertemuan = ±90 menit (2 JP)
- Siswa mengerjakan latihan mandiri di luar jam pelajaran (±1–2 jam/minggu)
- Setiap fase diakhiri dengan project integrasi
- React/Vue **tidak** diajarkan dalam roadmap ini — hanya persiapan fondasi



### Tools yang dibutuhkan

- Browser modern (Chrome / Edge / Firefox)
- VS Code + ekstensi: ESLint, Prettier, **Error Lens**
- Node.js (mulai Fase 3 — TypeScript)
- Git dasar (opsional, disarankan mulai Fase 2)

---



## 3. Alur Kurikulum

```
Prasyarat          Roadmap ini                    Setelah roadmap
─────────          ───────────                    ───────────────
HTML + CSS    →    JS Core (16)              →    React ATAU Vue
(dikelas lain)     Async & API (12)               (pilih salah satu)
                   TypeScript (8)
                   Bridge (4)
                   ─────────────
                   40 pertemuan
```


| Fase                    | Pertemuan | Durasi    | Bobot |
| ----------------------- | --------- | --------- | ----- |
| 1 — JavaScript Core     | #1–16     | 16 minggu | 40%   |
| 2 — Async & API         | #17–28    | 12 minggu | 30%   |
| 3 — TypeScript          | #29–36    | 8 minggu  | 20%   |
| 4 — Bridge ke Framework | #37–40    | 4 minggu  | 10%   |


---



## Fase 1 — JavaScript Core (Pertemuan 1–16)

**Tujuan fase:** Memahami cara kerja JavaScript — syntax, logic, data, dan DOM.

---



### Pertemuan 1 — Pengenalan JavaScript & Setup


| Aspek           | Detail                                                             |
| --------------- | ------------------------------------------------------------------ |
| **Topik**       | Apa itu JS, role di web, `<script>`, console.log, DevTools Console |
| **Latihan**     | Hello World, eksperimen di Console, inline vs external script      |
| **Deliverable** | File `index.html` + `main.js` dengan 5+ perintah console           |


**Poin kunci:** JavaScript berjalan di browser; Console adalah teman debugging.

---



### Pertemuan 2 — Variabel & Tipe Data


| Aspek           | Detail                                                                                 |
| --------------- | -------------------------------------------------------------------------------------- |
| **Topik**       | `let`, `const`, `var` (beda & best practice), string, number, boolean, null, undefined |
| **Latihan**     | Kalkulator sederhana di console, template literal                                      |
| **Deliverable** | Latihan: deklarasi variabel + operasi aritmatika                                       |


**Poin kunci:** Pakai `const` default, `let` jika nilai berubah; hindari `var`.

---



### Pertemuan 3 — Operator & Kondisi


| Aspek           | Detail                                                                                |
| --------------- | ------------------------------------------------------------------------------------- |
| **Topik**       | Operator aritmatika, perbandingan (`===`), logical (`&&`, `||`, `!`), if/else, switch |
| **Latihan**     | Program penentu grade (A/B/C/D), fizzbuzz dasar                                       |
| **Deliverable** | 3 program kondisi terpisah                                                            |


**Poin kunci:** Selalu pakai `===` bukan `==`.

---



### Pertemuan 4 — Looping


| Aspek           | Detail                                                        |
| --------------- | ------------------------------------------------------------- |
| **Topik**       | `for`, `while`, `do...while`, `for...of`, `break`, `continue` |
| **Latihan**     | Tabel perkalian, loop array sederhana                         |
| **Deliverable** | FizzBuzz lengkap (1–100)                                      |


**Poin kunci:** `for...of` untuk iterasi array; pahami kapan loop berhenti.

---



### Pertemuan 5 — Fungsi (Bagian 1)


| Aspek           | Detail                                                     |
| --------------- | ---------------------------------------------------------- |
| **Topik**       | Function declaration, parameter, return value, scope dasar |
| **Latihan**     | Fungsi konversi suhu, hitung luas bangun datar             |
| **Deliverable** | Minimal 5 fungsi reusable                                  |


**Poin kunci:** Fungsi = blok kode reusable; return mengembalikan nilai.

---



### Pertemuan 6 — Fungsi (Bagian 2)


| Aspek           | Detail                                                        |
| --------------- | ------------------------------------------------------------- |
| **Topik**       | Arrow function, default parameter, rest parameter (`...args`) |
| **Latihan**     | Refactor fungsi pertemuan 5 ke arrow function                 |
| **Deliverable** | Cheat sheet perbedaan declaration vs arrow                    |


**Poin kunci:** Arrow function tidak punya `this` sendiri — catat untuk nanti.

---



### Pertemuan 7 — Array Dasar


| Aspek           | Detail                                             |
| --------------- | -------------------------------------------------- |
| **Topik**       | Create, access, push/pop, length, iterasi manual   |
| **Latihan**     | Manipulasi daftar nilai siswa, cari min/max manual |
| **Deliverable** | Program kelola array tanpa method built-in         |


---



### Pertemuan 8 — Array Methods


| Aspek           | Detail                                                                      |
| --------------- | --------------------------------------------------------------------------- |
| **Topik**       | `map`, `filter`, `reduce`, `find`, `findIndex`, `some`, `every`, `includes` |
| **Latihan**     | Transform data produk: filter harga, map diskon, reduce total               |
| **Deliverable** | Worksheet 10 soal array methods                                             |


**Poin kunci:** ⭐ **Paling kritis untuk React/Vue** — kuasai `map` dan `filter`.

---



### Pertemuan 9 — Object & Destructuring


| Aspek           | Detail                                                                 |
| --------------- | ---------------------------------------------------------------------- |
| **Topik**       | Object literal, property access, method, destructuring, spread (`...`) |
| **Latihan**     | Model data siswa, merge object, destructuring parameter fungsi         |
| **Deliverable** | Array of objects + manipulasi dengan spread                            |


---



### Pertemuan 10 — Scope, Closure & `this`


| Aspek           | Detail                                                           |
| --------------- | ---------------------------------------------------------------- |
| **Topik**       | Global vs local scope, block scope, closure konsep, `this` dasar |
| **Latihan**     | Debug scope bug, counter dengan closure                          |
| **Deliverable** | Penjelasan tertulis 3 bug scope + perbaikannya                   |


**Poin kunci:** Sumber bug #1 di JavaScript — luangkan waktu di sini.

---



### Pertemuan 11 — DOM: Seleksi & Manipulasi


| Aspek           | Detail                                                                                 |
| --------------- | -------------------------------------------------------------------------------------- |
| **Topik**       | `querySelector`, `getElementById`, `textContent`, `innerHTML`, `classList`, attributes |
| **Latihan**     | Ubah teks, ganti warna, toggle class via JS                                            |
| **Deliverable** | Halaman profil interaktif (tanpa framework)                                            |


---



### Pertemuan 12 — DOM: Create & Remove Elements


| Aspek           | Detail                                                            |
| --------------- | ----------------------------------------------------------------- |
| **Topik**       | `createElement`, `appendChild`, `removeChild`, `DocumentFragment` |
| **Latihan**     | Render list dinamis dari array ke DOM                             |
| **Deliverable** | Dynamic list renderer (input → tampil di halaman)                 |


**Poin kunci:** `.map()` + DOM = preview cara React render list.

---



### Pertemuan 13 — Event Handling


| Aspek           | Detail                                                                                        |
| --------------- | --------------------------------------------------------------------------------------------- |
| **Topik**       | `addEventListener`, event object, `preventDefault`, event delegation, keyboard & mouse events |
| **Latihan**     | Form validation real-time, klik counter, keyboard shortcut                                    |
| **Deliverable** | Form dengan validasi JS (no submit jika invalid)                                              |


---



### Pertemuan 14 — ES Modules


| Aspek           | Detail                                                              |
| --------------- | ------------------------------------------------------------------- |
| **Topik**       | `import`/`export`, named vs default export, struktur folder project |
| **Latihan**     | Pisah logic ke `utils.js`, `data.js`, `main.js`                     |
| **Deliverable** | Project multi-file dengan modules                                   |


---



### Pertemuan 15 — Project: Todo App (Bagian 1)


| Aspek           | Detail                                                |
| --------------- | ----------------------------------------------------- |
| **Topik**       | Add todo, render list, toggle complete, struktur data |
| **Latihan**     | Implementasi CRUD Create + Read                       |
| **Deliverable** | Todo app v1 (tanpa persist)                           |


---



### Pertemuan 16 — Project: Todo App (Bagian 2) + Evaluasi Fase 1


| Aspek           | Detail                                                      |
| --------------- | ----------------------------------------------------------- |
| **Topik**       | Delete, filter (all/active/done), localStorage, code review |
| **Latihan**     | Selesaikan Todo app + simpan ke localStorage                |
| **Deliverable** | **Todo App v2** (lengkap) + evaluasi fase 1                 |


**Checkpoint Fase 1:** Siswa lulus jika Todo app berfungsi penuh tanpa tutorial.

---



## Fase 2 — Async & API (Pertemuan 17–28)

**Tujuan fase:** Bekerja dengan data dari luar — asynchronous JavaScript dan REST API.

---



### Pertemuan 17 — Callback & Konsep Async


| Aspek           | Detail                                                        |
| --------------- | ------------------------------------------------------------- |
| **Topik**       | Sync vs async, callback, callback hell, mengapa async penting |
| **Latihan**     | Simulasi delay dengan `setTimeout`, callback chain            |
| **Deliverable** | Diagram sync vs async + contoh callback                       |


---



### Pertemuan 18 — Promise


| Aspek           | Detail                                                         |
| --------------- | -------------------------------------------------------------- |
| **Topik**       | Membuat Promise, `.then()`, `.catch()`, `.finally()`, chaining |
| **Latihan**     | Fetch simulasi data, handle success & error                    |
| **Deliverable** | 3 Promise exercise (resolve, reject, chain)                    |


---



### Pertemuan 19 — Async/Await


| Aspek           | Detail                                                                    |
| --------------- | ------------------------------------------------------------------------- |
| **Topik**       | `async function`, `await`, try/catch dengan async, parallel vs sequential |
| **Latihan**     | Refactor Promise ke async/await                                           |
| **Deliverable** | Cheat sheet: Promise vs async/await                                       |


**Poin kunci:** Format modern yang dipakai hampir di semua codebase React/Vue.

---



### Pertemuan 20 — Fetch API Dasar


| Aspek           | Detail                                                               |
| --------------- | -------------------------------------------------------------------- |
| **Topik**       | `fetch()`, HTTP methods (GET), response.json(), status code, headers |
| **Latihan**     | Fetch data dari JSONPlaceholder / REST Countries                     |
| **Deliverable** | Halaman tampilkan list posts/users dari API                          |


---



### Pertemuan 21 — Fetch: POST, PUT, DELETE


| Aspek           | Detail                                             |
| --------------- | -------------------------------------------------- |
| **Topik**       | Request body, headers `Content-Type`, CRUD via API |
| **Latihan**     | Create & delete post via JSONPlaceholder           |
| **Deliverable** | CRUD demo dengan API publik                        |


---



### Pertemuan 22 — Error Handling & Loading State


| Aspek           | Detail                                                                   |
| --------------- | ------------------------------------------------------------------------ |
| **Topik**       | Network error, HTTP error, loading indicator, empty state, retry pattern |
| **Latihan**     | UI loading spinner, pesan error user-friendly                            |
| **Deliverable** | Fetch wrapper function dengan error handling                             |


**Poin kunci:** React/Vue semua punya loading & error state — pahami di vanilla dulu.

---



### Pertemuan 23 — JSON & Manipulasi Data API


| Aspek           | Detail                                                                  |
| --------------- | ----------------------------------------------------------------------- |
| **Topik**       | Parse/stringify, nested data, transform API response, pagination konsep |
| **Latihan**     | Transform response API ke format yang UI butuhkan                       |
| **Deliverable** | Data transformer utility + unit test manual                             |


---



### Pertemuan 24 — Event Loop (Konsep)


| Aspek           | Detail                                                          |
| --------------- | --------------------------------------------------------------- |
| **Topik**       | Call stack, task queue, microtask, mengapa async tidak blocking |
| **Latihan**     | Latihan urutan output (`setTimeout` vs Promise)                 |
| **Deliverable** | Diagram event loop + penjelasan 3 skenario                      |


---



### Pertemuan 25 — Project: Weather App


| Aspek           | Detail                                                            |
| --------------- | ----------------------------------------------------------------- |
| **Topik**       | Fetch API cuaca (OpenWeather / wttr.in), tampilkan kondisi & suhu |
| **Latihan**     | Search by city, loading & error state                             |
| **Deliverable** | **Weather App v1**                                                |


---



### Pertemuan 26 — Project: Movie/Book Catalog


| Aspek           | Detail                                                |
| --------------- | ----------------------------------------------------- |
| **Topik**       | Fetch TMDB / Open Library, list + detail view, search |
| **Latihan**     | Render grid cards, klik untuk detail                  |
| **Deliverable** | **Catalog App** dengan search                         |


---



### Pertemuan 27 — Project: Notes CRUD App


| Aspek           | Detail                                                 |
| --------------- | ------------------------------------------------------ |
| **Topik**       | Full CRUD dengan API, form handling, konfirmasi delete |
| **Latihan**     | Create, edit, delete notes via JSONPlaceholder         |
| **Deliverable** | **Notes CRUD App**                                     |


---



### Pertemuan 28 — Evaluasi Fase 2


| Aspek           | Detail                                               |
| --------------- | ---------------------------------------------------- |
| **Topik**       | Code review project, Q&A async, persiapan TypeScript |
| **Latihan**     | Presentasi project + live coding fetch               |
| **Deliverable** | Revisi 1 project + evaluasi fase 2                   |


**Checkpoint Fase 2:** Siswa lulus jika bisa fetch, tampilkan, dan handle error tanpa tutorial.

---



## Fase 3 — TypeScript (Pertemuan 29–36)

**Tujuan fase:** Menambah type safety dan persiapan codebase modern (React/Vue + TS).

---



### Pertemuan 29 — Pengenalan TypeScript & Setup


| Aspek           | Detail                                                             |
| --------------- | ------------------------------------------------------------------ |
| **Topik**       | Apa itu TS, compile ke JS, install Node.js, `tsc`, `tsconfig.json` |
| **Latihan**     | Setup project TS, compile hello world                              |
| **Deliverable** | Project TS pertama berjalan di browser                             |


---



### Pertemuan 30 — Types Dasar


| Aspek           | Detail                                                                       |
| --------------- | ---------------------------------------------------------------------------- |
| **Topik**       | Type annotations, inference, `string`, `number`, `boolean`, `any`, `unknown` |
| **Latihan**     | Annotasi variabel & parameter fungsi Todo app                                |
| **Deliverable** | Latihan 15 soal type annotation                                              |


**Poin kunci:** Hindari `any` — gunakan `unknown` jika type belum pasti.

---



### Pertemuan 31 — Array, Tuple & Union Types


| Aspek           | Detail                                                        |
| --------------- | ------------------------------------------------------------- |
| **Topik**       | Typed arrays, tuple, union (`string | number`), literal types |
| **Latihan**     | Type data produk, status enum literal                         |
| **Deliverable** | Typed data models untuk Notes app                             |


---



### Pertemuan 32 — Interface & Type Alias


| Aspek           | Detail                                                            |
| --------------- | ----------------------------------------------------------------- |
| **Topik**       | `interface`, `type`, optional property (`?`), readonly, extending |
| **Latihan**     | Interface `User`, `Todo`, `Note`, `ApiResponse<T>`                |
| **Deliverable** | File `types.ts` untuk project                                     |


**Poin kunci:** Interface = blueprint data — persis seperti props di React/Vue.

---



### Pertemuan 33 — Function Types & Generics Dasar


| Aspek           | Detail                                                     |
| --------------- | ---------------------------------------------------------- |
| **Topik**       | Typed functions, callback types, generic `<T>`, `Array<T>` |
| **Latihan**     | Generic function `fetchData<T>()`, typed event handlers    |
| **Deliverable** | Typed fetch wrapper dari Fase 2                            |


---



### Pertemuan 34 — Type Narrowing & Strict Mode


| Aspek           | Detail                                                        |
| --------------- | ------------------------------------------------------------- |
| **Topik**       | typeof guard, instanceof, discriminated union, `strict: true` |
| **Latihan**     | Fix 10 error TypeScript compiler                              |
| **Deliverable** | Project dengan `strict: true` tanpa error                     |


---



### Pertemuan 35 — Migrate Project ke TypeScript


| Aspek           | Detail                                                        |
| --------------- | ------------------------------------------------------------- |
| **Topik**       | Rename `.js` → `.ts`, tambah types bertahap, handle DOM types |
| **Latihan**     | Migrate Todo app atau Notes app ke TS                         |
| **Deliverable** | **Project TS v1** (migrated)                                  |


---



### Pertemuan 36 — Evaluasi Fase 3


| Aspek           | Detail                                                     |
| --------------- | ---------------------------------------------------------- |
| **Topik**       | Code review types, Q&A, best practices TS di project nyata |
| **Latihan**     | Presentasi perbedaan JS vs TS project yang sama            |
| **Deliverable** | Revisi project TS + evaluasi fase 3                        |


**Checkpoint Fase 3:** Siswa lulus jika project TS compile tanpa error dan bisa jelaskan setiap interface.

---



## Fase 4 — Bridge ke Framework (Pertemuan 37–40)

**Tujuan fase:** Memahami konsep yang dipakai React/Vue — tanpa framework dulu.

---



### Pertemuan 37 — Component Thinking (Vanilla)


| Aspek           | Detail                                                                            |
| --------------- | --------------------------------------------------------------------------------- |
| **Topik**       | Fungsi sebagai component, template string, props sebagai parameter, composability |
| **Latihan**     | Buat `Card(data)`, `Button(label, onClick)`, `ListItem(item)`                     |
| **Deliverable** | Mini component library vanilla (3–5 components)                                   |


```
// Preview pola React/Vue — masih vanilla JS
function Card({ title, body }) {
  return `<article class="card"><h3>${title}</h3><p>${body}</p></article>`;
}
```

---



### Pertemuan 38 — State & Re-render Pattern


| Aspek           | Detail                                                                |
| --------------- | --------------------------------------------------------------------- |
| **Topik**       | State object, render function, update state → re-render, immutability |
| **Latihan**     | Counter, toggle, list dengan state management manual                  |
| **Deliverable** | Todo app v3 dengan render pattern (mirip React state)                 |


**Poin kunci:** React `useState` = state + re-render. Vue `ref` = reactive state. Pahami polanya di sini.

---



### Pertemuan 39 — Side Effects & Lifecycle Konsep


| Aspek           | Detail                                                                    |
| --------------- | ------------------------------------------------------------------------- |
| **Topik**       | Side effect (fetch on load), cleanup (remove listener), lifecycle analogi |
| **Latihan**     | App fetch data on init, unsubscribe on destroy                            |
| **Deliverable** | App dengan init effect + cleanup                                          |


**Poin kunci:** React `useEffect` / Vue `onMounted` + `onUnmounted` — konsepnya sama.

---



### Pertemuan 40 — Evaluasi Akhir & Persiapan React/Vue


| Aspek           | Detail                                                                      |
| --------------- | --------------------------------------------------------------------------- |
| **Topik**       | Ujian praktik, presentasi portfolio, preview React vs Vue, roadmap lanjutan |
| **Latihan**     | Live coding + presentasi 1 project terbaik                                  |
| **Deliverable** | **Portfolio 4 project** + checklist siap framework                          |


**Checkpoint Akhir:** Lihat [Checklist Siap React/Vue](#checklist-siap-reactvue).

---



## Project Portfolio

Siswa wajib memiliki minimal **4 project** saat roadmap selesai:


| No  | Project            | Fase   | Fitur minimum                            |
| --- | ------------------ | ------ | ---------------------------------------- |
| 1   | **Todo App**       | Fase 1 | CRUD, filter, localStorage               |
| 2   | **Weather App**    | Fase 2 | Fetch API, search, loading/error state   |
| 3   | **Notes CRUD App** | Fase 2 | Full CRUD via REST API                   |
| 4   | **Typed App (TS)** | Fase 3 | Migrate salah satu project ke TypeScript |


Project bonus (opsional):

- Movie/Book Catalog dengan search & detail view
- Kalkulator scientific dengan history
- Quiz app dengan score & timer

---



## Checklist Siap React/Vue

Siswa **dinyatakan siap** memasuki React atau Vue jika memenuhi **semua** item:

### JavaScript

- [ ] Menjelaskan perbedaan `let`, `const`, dan scope
- [ ] Menggunakan `map`, `filter`, dan `reduce` tanpa referensi
- [ ] Membuat dan memanggil fungsi (declaration & arrow)
- [ ] Memanipulasi DOM dan menangani event
- [ ] Membedakan sync vs async dengan contoh
- [ ] Fetch data dengan async/await + handle error
- [ ] Membangun CRUD app tanpa framework



### TypeScript

- [ ] Menulis interface untuk model data
- [ ] Mengannotasi parameter fungsi dan return type
- [ ] Membaca dan memperbaiki error TypeScript compiler
- [ ] Project TS compile dengan `strict: true`



### Konsep Framework

- [ ] Menjelaskan apa itu "component" dengan contoh vanilla
- [ ] Menjelaskan "state" dan kenapa butuh re-render
- [ ] Menjelaskan "props" sebagai parameter component
- [ ] Paham bahwa React/Vue **dibangun di atas JavaScript**, bukan menggantikannya

---



## Rubrik Penilaian



### Bobot per komponen (100%)


| Komponen                | Bobot | Keterangan                     |
| ----------------------- | ----- | ------------------------------ |
| Kehadiran & partisipasi | 10%   | Aktif di kelas, tanya jawab    |
| Latihan mingguan        | 20%   | Deliverable per pertemuan      |
| Project fase            | 40%   | 4 project portfolio (10% each) |
| Evaluasi fase (4×)      | 20%   | Checkpoint tiap akhir fase     |
| Ujian akhir (P40)       | 10%   | Live coding + presentasi       |




### Kriteria project (skor 1–4)


| Skor | Kriteria                                                     |
| ---- | ------------------------------------------------------------ |
| 4    | Berfungsi lengkap, kode rapi, ada error handling, deployable |
| 3    | Berfungsi mayoritas, kode cukup terstruktur                  |
| 2    | Berfungsi sebagian, butuh bantuan debugging                  |
| 1    | Tidak berfungsi / copy-paste tanpa paham                     |


---



## Referensi



### Dokumentasi resmi

- [MDN JavaScript Guide](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide)
- [MDN Fetch API](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API)
- [TypeScript Handbook](https://www.typescriptlang.org/docs/handbook/intro.html)
- [JavaScript.info](https://javascript.info/) — tutorial terstruktur gratis



### API publik untuk latihan

- [JSONPlaceholder](https://jsonplaceholder.typicode.com/) — fake REST API
- [REST Countries](https://restcountries.com/) — data negara
- [OpenWeatherMap](https://openweathermap.org/api) — data cuaca (butuh API key gratis)
- [TMDB API](https://developer.themoviedb.org/docs) — data film (butuh API key gratis)



### Roadmap lanjutan (setelah dokumen ini)

1. **React** + TypeScript — atau —
2. **Vue 3** + TypeScript
3. State management (Pinia / Zustand)
4. Backend dasar (Node.js + Express) — opsional

---



## Lampiran: Skala ke 80 Pertemuan (2× / Minggu)

Jika kelas bertemu **2× per minggu**, gandakan latihan per topik:


| Fase        | Pertemuan | Pembagian                                         |
| ----------- | --------- | ------------------------------------------------- |
| JS Core     | #1–32     | Pertemuan ganjil = teori, genap = praktik/project |
| Async & API | #33–56    | +2 project API tambahan                           |
| TypeScript  | #57–72    | +generics lanjut, utility types dasar             |
| Bridge      | #73–80    | +mini project component system lengkap            |


Topik dan urutan tetap sama — yang bertambah adalah **jam praktik dan review code**.

---

*Dokumen ini melengkapi* `TECHNICAL_DOCUMENT.md` *(project HTML). HTML & CSS diasumsikan sudah dikuasai dari mapel/kelas lain.*