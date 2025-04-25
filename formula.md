# Logika Matematika & Output

## 1. Definisi Input
- **VF**: Volatility Factor (desimal 0.01)
- **CF**: Close Factor (desimal 0.01)
- **CR**: Core (desimal 0.01)
- **SF**: Smooth Factor, dipilih dari sesi trading:
  - ER → `SF = 8`
  - AM → `SF = 13`
  - AS → `SF = 21`
  

## 2. Perhitungan Dasar
- **High Session (HS)**
  `HS = VF + SF`
- **Low Session (LS)**
  `LS = VF - SF`
- **Range**
  `Range = HS - LS`
- **Pivot Point (PP)**
  `PP = (HS + LS + CF) / 3`

## 3. Sinyal
- **Bullish**: `CF > HS` dan `CF > LS`
- **Bearish**: `CF < LS` dan `CF < HS`
- **Konsolidasi**: `LS ≤ CF ≤ HS`

## 4. Trigger 
`P_internal = ((PP - CF) / Range) × 100`
`jika hasil diatas 100%(positif) maka (cr - hasil) = TU/trigger up`
`jika hasil dibawah 100%(negatif) maka (cr - hasil) = TD/trigger down`
`jika hasil diantara 0% s.d 100%(netral) maka {cf + (cr - vf)} + {cf - (cr-vf)} / 2 = TN/trigger netral`

## 5. Level Distribusi & Akumulasi
Untuk setiap `m` dalam {0.5, 1.618, 2.618, 4.236}:
- **Level Distribusi** (`dist_m`):
  `dist_m = PP + (Range × m)`
- **Level Akumulasi** (`acc_m`):
  `acc_m = PP - (Range × m)`

## 6. Persentase Sentimen Bar
- `d = dist_4.236 = [(2 × VF + CF) / 3] + (2 × SF × 4.236)`
- `a = acc_4.236 = [(2 × VF + CF) / 3] - (2 × SF × 4.236)`
- `P_bar = ((CF - a) / (d - a)) × 100`
- `bullishPct = clamp(P_bar, 0, 100)`
- `bearishPct = 100 - bullishPct`

---

*Semua rumus di atas hanya menggunakan VF, CF, dan SF sesuai logika sanva.*

