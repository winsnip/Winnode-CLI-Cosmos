
# Winnode CLI untuk Cosmos Blockchain

**Winnode CLI** adalah alat command-line untuk berinteraksi dengan blockchain Cosmos. Mendukung operasi wallet, transfer, staking, validator, serta fitur otomatisasi.

---

## 📦 Instalasi

### 🪟 Windows
1. Unduh file `winnode-cli-win.exe`, `config.json` dan `mnemonic.txt`
2. Jalankan dengan double-click atau ketik perintah:
   ```bash
   winnode-cli-win.exe
   ```

### 🐧 Linux
1. Unduh file `winnode-cli-linux`, `config.json` dan `mnemonic.txt`
2. Berikan izin eksekusi:
   ```bash
   chmod +x winnode-cli-linux
   ```
3. Jalankan dengan:
   ```bash
   ./winnode-cli-linux
   ```

###  Apple silicon/arm64
1. Unduh file `winnode-cli-mac-arm64`, `config.json` dan `mnemonic.txt`
2. Berikan izin eksekusi:
   ```
   chmod +x winnode-cli-mac-arm64
   ```
  
   ```
   codesign --sign - winnode-cli-mac-arm64
   ```

3. Jalankan dengan:
   ```
   ./winnode-cli-mac-arm64
   ```

###  Apple intel/x86
1. Unduh file `winnode-cli-mac-x64`, `config.json` dan `mnemonic.txt`
2. Berikan izin eksekusi:
   ```
   chmod +x winnode-cli-mac-x64
   ```
  
   ```
   codesign --sign - winnode-cli-mac-x64
   ```

3. Jalankan dengan:
   ```
   ./winnode-cli-mac-x64
   ```

---

## ⚙️ Build dari Source

### 🔧 Prasyarat
- Node.js v14+
- npm v6+

### 🔨 Build - Windows
```bash
# Clone repository
git clone <repository-url>
cd winnode-cli

# Install dependencies
npm install

# Build project
npm run build

# Create executable
npm run pkg
```

### 🔨 Build - Linux
```bash
# Clone repository
git clone <repository-url>
cd winnode-cli

# Install dependencies
npm install

# Build project
npm run build

# Create executable
npm run pkg-linux
```

---

## ⚙️ Konfigurasi

File konfigurasi: `config.json` (terletak di direktori yang sama dengan executable)

```json
{
  "default_chain": "Kiichain",
  "chains": {
    "Lumera": {
      "chain_id": "lumera-testnet-1",
      "chain_prefix": "lumera",
      "rpc_endpoint": "https://lumera-testnet-rpc.polkachu.com",
      "rest_endpoint": "https://lumera-testnet-api.polkachu.com",
      "gas_price": "0.025ulume",
      "coin_denom": "ulume",
      "coin_minimal_denom": "ulume",
      "coin_decimals": "6",
      "coin_symbol": "LUME"
    },
    "Kiichain": {
      "chain_id": "oro_1336-1",
      "chain_prefix": "kii",
      "rpc_endpoint": "https://rpc.dos.sentry.testnet.v3.kiivalidator.com",
      "rest_endpoint": "https://lcd.dos.sentry.testnet.v3.kiivalidator.com",
      "gas_price": "200000000000akii",
      "coin_denom": "akii",
      "coin_minimal_denom": "akii",
      "coin_decimals": "18",
      "coin_symbol": "KII"
    }
  }
}
```

---

## 🔍 Perbedaan Windows vs Linux

| Aspek              | Windows                  | Linux/Apple             |
|--------------------|--------------------------|-------------------------|
| Nama Executable    | `winnode-cli.exe`        | `winnode-cli`           |
| Perintah Build     | `npm run pkg`            | `npm run pkg-linux`     |
| Izin File          | Tidak diperlukan         | `chmod +x winnode-cli`  |
| Path Separator     | Backslash (`\`)         | Forward slash (`/`)      |

---

## ✅ Fitur Tersedia

### 💼 Wallet
- Buat wallet baru
- Lihat saldo wallet
- Daftar wallet yang tersedia

### 💸 Transfer
- Transfer token ke alamat lain
- Transfer semua token ke alamat lain

### 🔐 Staking
- Delegate token ke validator
- Undelegate token dari validator
- Redelegate antar validator
- Withdraw staking rewards

### 🧑‍⚖️ Validator
- Lihat validator aktif
- Lihat delegasi saat ini
- Lihat semua validator (termasuk jailed)
- Lihat info validator tertentu
- Unjail validator

### 🔗 Chain
- Lihat daftar chain yang tersedia
- Ganti chain aktif

### ⚙️ Auto Claim & Stake
- Auto claim rewards dan stake ke validator yang sama
- Auto claim dan stake ke validator tertentu

### 📅 Auto Stake
- Auto stake dengan interval waktu ke validator tertentu

---

## 🔐 Keamanan

- Mnemonic wallet disimpan dalam `mnemonic.txt` di direktori yang sama dengan executable.
- ⚠️ **PENTING**: Jangan bagikan `mnemonic.txt` kepada siapapun!
- Backup file tersebut di tempat aman.

---

## ⚠️ Catatan
CLI ini adalah alat bantu untuk interaksi dengan jaringan Cosmos. Pastikan memahami risiko dan tanggung jawab setiap operasi yang Anda lakukan.
# CLI-WINNODE
