# 🪙 PlanX-Wallet

![Ruby](https://img.shields.io/badge/Ruby-3.x-red?logo=ruby&logoColor=white)
![Node](https://img.shields.io/badge/Node.js-18%2B-339933?logo=node.js&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Termux%20%7C%20Linux%20%7C%20Windows%20%7C%20macOS-0ea5e9)
![License: MIT](https://img.shields.io/badge/License-MIT-22c55e)

**PlanX-Wallet** adalah kumpulan kecil **script terpisah** yang ditulis dengan **Ruby** dan **Node.js** untuk tugas dompet/otomasi.  
Setiap script **berdiri sendiri** (tanpa argumen CLI bersama). Simpan input dalam file teks sederhana dan `.env` opsional.

> Gunakan secara bertanggung jawab dan patuhi ToS dari layanan apa pun yang Anda gunakan.

---

## ✨ Fitur
- Script Ruby + Node.js yang dapat dijalankan secara independen
- Membaca input dari file biasa (mis. `data.txt`) dan `proxy.txt` opsional
- Variabel lingkungan opsional via `.env`
- Berlisensi MIT

---

## 📁 Tata Letak Repository
```
PlanX-Wallet/
├─ bot.rb            # Ruby script (general automation)
├─ Withdrawal.rb     # Ruby script (withdrawal/transfer batch)
├─ quest.js          # Node.js worker for specific tasks
├─ info.js           # Node.js utility/info
├─ package.json      # Node deps (if any)
├─ data.txt          # Input data (one item per line)
├─ proxy.txt         # Optional proxies list
├─ .env              # Optional environment variables (DO NOT commit secrets)
└─ LICENSE           # MIT
```

---

## 🔧 Persyaratan
- **Ruby 3.x** (disarankan 3.2+)
- **Node.js 18+** (atau 20+)
- **git**

> Script membutuhkan gem Ruby atau paket Node tambahan, instal sekali lalu jalankan ulang.

---

## 🚀 Setup

### Linux / macOS / Windows (PowerShell)
```bash
git clone https://github.com/Nadir-N3/PlanX-Wallet.git
cd PlanX-Wallet

# Node deps (if any exist in package.json)
npm install
```

### Termux (Android)
```bash
pkg update -y && pkg upgrade -y
pkg install git nodejs-lts ruby -y

git clone https://github.com/Nadir-N3/PlanX-Wallet.git
cd PlanX-Wallet

npm install
```

---

## ⚙️ Konfigurasi input
- **`data.txt`** — letakkan satu token per baris.
- **`proxy.txt`** *(opsional)* — satu proxy per baris:
  ```
  http://host:port
  http://user:pass@host:port
  ```
---

## ▶️ Menjalankan script (tanpa argumen)
Semua script **terpisah**. Jalankan hanya yang Anda butuhkan:

### Node.js
```bash
node info.js
node quest.js
```

### Ruby
```bash
ruby bot.rb
ruby Withdrawal.rb
```

> Jika sebuah script membaca `data.txt` atau `proxy.txt`, pastikan file tersebut ada di root repo.

---

## 🧯 Pemecahan Masalah
- **Node “module not found”** → jalankan `npm install` di direktori repo.
- **Ruby “LoadError”** → perbarui Ruby ke 3.x; jika gem tidak ada dan tidak dibundel, instal via `gem install <name>`.
- **Permission denied** → tambahkan izin eksekusi (`chmod +x *.sh`) atau jalankan langsung via `ruby`/`node`.
- **Proxy tidak terpakai** → pastikan `proxy.txt` ada dan script benar-benar membacanya.
- **Versi Python/Node/Ruby berbeda** → jalankan `node -v` / `ruby -v` untuk memastikan versi sesuai persyaratan.

---

## 📜 Lisensi
MIT — lihat `LICENSE`.

---

## 🙌 Penulis
**Nadir-N3** · [X](https://x.com/Naadiir_08) · [Instagram](https://instagram.com/__naadiir.fx)
