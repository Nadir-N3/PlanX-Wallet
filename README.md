# 🪙 PlanX‑Wallet

![Ruby](https://img.shields.io/badge/Ruby-3.x-red?logo=ruby&logoColor=white)
![Node](https://img.shields.io/badge/Node.js-18%2B-339933?logo=node.js&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Termux%20%7C%20Linux%20%7C%20Windows%20%7C%20macOS-0ea5e9)
![License: MIT](https://img.shields.io/badge/License-MIT-22c55e)

**PlanX‑Wallet** is a small toolkit of **separate scripts** written in **Ruby** and **Node.js** for wallet/automation tasks.  
Each script is **stand‑alone** (no shared CLI arguments). Keep inputs in simple text files and optional `.env`.

> Use responsibly and follow the ToS of any service you interact with.

---

## ✨ Features
- Ruby + Node.js scripts that you can run independently
- Read inputs from plain files (e.g., `data.txt`) and optional `proxy.txt`
- Optional environment variables via `.env`
- MIT licensed

---

## 📁 Repository Layout
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

## 🔧 Requirements
- **Ruby 3.x** (3.2+ recommended)
- **Node.js 18+** (or 20+)
- **git**

> If your scripts need extra Ruby gems or Node packages, install them once and re-run.

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

## ⚙️ Configure inputs
- **`data.txt`** — put one entry per line (address / account / parameter your scripts expect).
- **`proxy.txt`** *(optional)* — one proxy per line:
  ```
  http://host:port
  http://user:pass@host:port
  ```
- **`.env`** *(optional)* — keep API keys or endpoints here. Example:
  ```env
  API_KEY=xxxxxxxx
  RPC_URL=https://...
  ```
  > Keep `.env` out of version control.

---

## ▶️ Run the scripts (no arguments)
All scripts are **separate**. Run only the one you need:

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

> If a script reads `data.txt` or `proxy.txt`, just make sure the files exist in the repo root.

---

## 🧯 Troubleshooting
- **Node “module not found”** → run `npm install` in the repo directory.
- **Ruby “LoadError”** → update Ruby to 3.x; if a gem is missing and not bundled, install it via `gem install <name>`.
- **Permission denied** → add execute perms (`chmod +x *.sh`) or run via `ruby`/`node` explicitly.
- **Proxy not applied** → ensure `proxy.txt` is present and the script actually reads it.
- **Different Python/Node/Ruby versions** → run `node -v` / `ruby -v` to verify versions match the requirements.

---

## 📜 License
MIT — see `LICENSE`.

---

## 🙌 Author
**Nadir‑N3** · [X](https://x.com/Naadiir_08) · [Instagram](https://instagram.com/__naadiir.fx)
