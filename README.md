# Quant-AI Sanva Theory Calculator


Kiye dokumentasi kanggo kode HTML, CSS, lan JavaScript sing nggawe alat itungan Quant-AI sederhana nganggo dasar Sanva Theory. Tampilane digawe modern lan responsif ben apik dideleng nang pirang-pirang ukuran layar.

## Deskripsi Ringkes

Alat kiye gunane nggo ngitung Pivot Point (PP), nganalisis sentimen pasar (Bullish, Bearish, Konsolidasi), lan nampilna level-level Distribusi (DI) karo Akumulasi (AK) sing penting miturut teori Sanva. Input utamane yakuwe Volatility Factor (VF), Close Factor (CF), karo pilihan Sesi Trading (ER, AM, AS) sing nentokna Smooth Factor (SF).

## Fitur-Fitur Utama

* **Input Gampang:** Nglebokna nilai VF karo CF nganggo kolom input angka.
* **Pilihan Sesi:** Milih sesi trading (ER, AM, AS) nganggo tombol radio nggo nentokna SF.
* **Itungan Otomatis:** Ngitung High Session (HS), Low Session (LS), Pivot Point (PP), karo Range (R) pas tombol "Hitung" diklik.
* **Analisis Sentimen:** Nentokna sinyal sentimen pasar (Bullish, Bearish, utawa Konsolidasi) adhedhasar posisi CF relatif maring HS karo LS, terus nampilna nganggo teks karo ikon warna (Ijo, Abang, Kuning).
* **Visualisasi Sentimen:** Nampilna garis gradien (Abang-Kuning-Ijo) karo penanda (marker) sing nuduhna posisi CF relatif maring PP nang rentang HS-LS, lengkap karo persentase sentimen.
* **Tabel DI & AK:** Nampilna level-level rega penting kanggo Distribusi (target buyer, level lanjutan) karo Akumulasi (target seller, level lanjutan) nang tabel sing kepisah.
* **Kartu Informasi:** Ana bagian informasi sing teyeng dideleng/umpetna (collapsible) nggo njelasna cara nggunakna karo catetan penting.
* **Tampilan Modern & Responsif:** Desaine nganggo gradient, efek blur, karo layout sing bisa nyesuaikna karo ukuran layar (desktop utawa HP).
* **Validasi Input:** Ana pengecekan sederhana nggo mestikna VF karo CF sing dilebokna kuwe angka sing valid.

## Cara Nggunakna

1.  **Bukak File HTML:** Bukak file `index.html` (utawa jeneng liyane nek wis diganti) nang browser web.
2.  **Isi Input:**
    * Lebokna angka **Volatility Factor (VF)** nang kolom sing ana.
    * Lebokna angka **Close Factor (CF)** nang kolom sing ana.
3.  **Pilih Sesi:** Pilih salah siji sesi trading (**ER**, **AM**, utawa **AS**) nganggo ngeklik tombol radio sing pas. Pilihan kiye bakal nentokna nilai Smooth Factor (SF) sing digunakna nang itungan.
4.  **Klik "Hitung":** Klik tombol "Hitung" nggo mulai proses itungan.
5.  **Deleng Hasil:**
    * Bagian nduwur bakal nampilna **Pivot Point (PP)**, **Sesi (MS)** sing dipilih, karo **Sinyal Sentimen** (Bullish/Bearish/Konsolidasi) karo ikon warnane.
    * **Visualisasi Sentimen** bakal muncul nang ngisore, nuduhna posisi CF nang garis gradien.
    * **Tabel Distribusi** karo **Akumulasi** bakal nampilna level-level rega sing wis diitung.
    * Waca **Catetan** nang bagian ngisor nggo penginget.
6.  **Info Tambahan:** Klik bagian "Informasi Penting / Cara Penggunaan" nggo ndeleng utawa ngumpetna panduan ringkes.

## Struktur Kode

* **HTML (`index.html`):** Nggawe struktur halaman, termasuk formulir input, tombol, karo wadah nggo nampilna hasil (div karo id `result`, tabel, lsp). Uga nglebokna elemen-elemen nggo visualisasi sentimen karo kartu informasi.
* **CSS (nang tag `<style>`):** Ngatur tampilan karo gaya halaman ben katon apik. Kiye termasuk warna latar mburi, font, ukuran, padding, margin, layout (nganggo Flexbox karo Grid), efek visual (gradient, shadow, blur), karo nggawe responsif ben pas nang macem-macem layar. Uga ngatur gaya khusus nggo visualisasi sentimen (garis, marker) karo kartu informasi sing teyeng dilipat.
* **JavaScript (nang tag `<script>`):**
    * `calculate()`: Fungsi utama sing diundang pas tombol "Hitung" diklik. Njikot nilai input, validasi, nglakoni kabeh itungan Sanva Theory (HS, LS, PP, R), nentokna sentimen, terus nampilna hasile nang elemen HTML sing sesuai. Fungsi kiye uga nyimpen nilai itungan terakhir nggo digunakna nang fungsi liya.
    * `updateSentimentVisualization()`: Ngatur tampilan visualisasi sentimen. Ngitung posisi marker karo persentase adhedhasar nilai LS, HS, CF, karo PP. Terus ngupdate posisi (`left`) karo warna marker (`cf_marker`) karo teks persentase (`cf_percentage`) nang garis gradien. Fungsi kiye uga ngatur kapan visualisasi kudu ditampilna utawa diumpetna.
    * `showMessageBox()`: Fungsi nggo nampilna pesen (saiki isih nganggo `alert()`, apike diganti nganggo modal sing luwih apik).
    * Logika Kartu Informasi: Ngatur ben kartu informasi teyeng dibukak tutup pas judule diklik.
    * Event Listener `resize`: Ngrungokna nek ukuran jendela browser berubah, terus ngundang `updateSentimentVisualization()` maning nggo nyesuaikna posisi marker nganggo nilai itungan terakhir sing disimpen.

## Catetan Penting

* Itungan kiye **sifate eksperimental** lan adhedhasar interpretasi Sanva Theory.
* Hasil sing ditampilna **dudu saran keuangan utawa sinyal trading pasti**.
* **Gunakna manajemen risiko** sing bener nek arep njikot keputusan trading adhedhasar analisis kiye.
* Pestikna nilai VF, CF, karo Sesi sing dilebokna kuwe **relevan karo data pasar sing lagi dianalisis**.

---

Muga-muga dokumentasi kiye mbantu, Lur!
