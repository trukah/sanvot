# Desain Gauge Chart Sentimen:

Tampilan semi-lingkaran dengan jarum yang bergerak dari kiri (bearish) ke kanan (bullish)
Gradasi warna dari merah (bearish) di kiri, abu-abu (netral) di tengah, hingga hijau (bullish) di kanan
Jarum penunjuk yang bergerak halus sesuai dengan nilai sentimen
Label untuk menunjukkan kategori sentimen (Bearish, Netral, Bullish)

## Tampilan Nilai Sentimen:

Kotak di bawah gauge menampilkan nilai sentimen dengan format "[Kategori]: [Nilai]%"
Warna teks sesuai dengan kategori sentimen (merah untuk bearish, abu-abu untuk konsolidasi, hijau untuk bullish)

## Sistem Perhitungan Sentimen:

``` Menggunakan skala 0-100%, di mana:
0-25%: Strong Bearish
25-40%: Bearish
40-60%: Konsolidasi/Netral
60-75%: Bullish
75-100%: Strong Bullish
* Nilai dihitung berdasarkan posisi CFS relatif terhadap HS dan LS

