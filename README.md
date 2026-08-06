# Wager Predict Bot Scripts 🚀

This collection of Python scripts automates tasks on the **Wager Predict** protocol — an on-chain prediction market platform on BSC Testnet. The scripts handle market trading (auto/manual buy & sell), market creation, and faucet claiming (USDC/testnet tokens) across multiple wallets.

🔗 Register: [Wager Predict](https://wagerpredict.com/r/thog)

## ✨ Features Overview

### General Features

- **Multi-Account Support**: Reads private keys from `pvkey.txt` to perform actions across multiple accounts.
- **Colorful CLI**: Uses `colorama` for visually appealing output with box-drawing borders and colored icons.
- **Asynchronous Execution**: Built with `asyncio` for efficient concurrent task processing using semaphore-based threading.
- **Error Handling**: Comprehensive error catching for blockchain transactions and RPC issues.
- **Bilingual Support**: Supports both English and Vietnamese output.
- **Proxy Support**: Supports HTTP, HTTPS, SOCKS4, and SOCKS5 proxies via `proxies.txt`.
- **POA Middleware**: Injects BSC Testnet POA middleware automatically for correct RPC calls.

### Included Scripts

✨ **MARKET Trading** (`trade.py`)

- ✅ Auto mode: claims winnings, sells the larger side, or buys the cheaper side (YES/NO) at ≤ 50c
- ✅ Manual mode: buy, sell, claim per selected market with state overview
- ✅ Reads 464+ open markets via REST API, keyword filter, and odds/slippage handling
- ✅ Auto-approves USDC before buying when allowance is insufficient
- ✅ Full tx hashes with BSCScan explorer links in the output
- ✅ Multi-wallet and manual/auto mode selection

✨ **CREATE MARKET** (`create.py`)

- ✅ Creates a self-serve market on-chain via `createMarketSelfServe`
- ✅ Previews seed cost and validity bond, checks USDC balance
- ✅ Auto-approve USDC to the Registry
- ✅ Posts market metadata (question, options, category) to the API
- ✅ Returns the market ID and full explorer links

✨ **FAUCET** (`faucet.py`)

- ✅ Fills USDC for multiple wallets from the Wager Predict testnet faucet
- ✅ Supports captcha solving (CapMonster / local Captcha-Solver)
- ✅ Multi-wallet processing with proxy support and pausing between wallets

## 🛠️ Prerequisites

Before running the scripts, ensure you have the following installed:

- **Python 3.8+**
- **pip** (Python package manager)
- **Dependencies**: Install via `pip install aiohttp aiohttp-socks eth-account colorama web3`
- **pvkey.txt**: Add private keys (one per line) for wallet automation
- **proxies.txt** (optional): Add proxy addresses for network requests

## 📦 Installation

1. **Clone or download this repository:**
   ```sh
   git clone https://github.com/thog9/Wagerpredict-testnet.git
   cd Wagerpredict-testnet
   ```

2. **Install Dependencies:**
   ```sh
   pip install -r requirements.txt
   ```

3. **Prepare Input Files:**

   Create `pvkey.txt` with your private keys (one per line):
   ```
   0x1234567890abcdef...
   0xabcdef1234567890...
   ```

   Create `proxies.txt` (optional) — one proxy per line:
   ```
   http://user:pass@ip:port
   socks5://user:pass@ip:port
   ip:port:user:pass
   ```

4. **Run:**
   ```sh
   python main.py
   ```
   - Choose a language (Vietnamese / English).
   - Select the script you want to run.

**Language Selection:**
- Choose between Vietnamese (Tiếng Việt) and English.
- All scripts support bilingual output.

---

## 📁 Project Structure

```
Wagerpredict-testnet/
├── main.py                # Central menu system
├── pvkey.txt              # Private keys file
├── proxies.txt            # Proxies file (optional)
├── requirements.txt       # Python dependencies
├── README.md              # This file
└── scripts/               # Individual scripts
    ├── trade.py           # Market trading bot (auto / manual)
    ├── create.py          # Create prediction markets
    └── faucet.py          # Faucet tool for testnet tokens
```

---

## 📨 Contact

Connect with us for support or updates:

- **Telegram**: [thog099](https://t.me/thog099)
- **Channel**: [CHANNEL](https://t.me/thogairdrops)
- **Group**: [GROUP CHAT](https://t.me/thogchats)
- **X**: [Thog](https://x.com/thog099)

---

## ☕ Support Us

Love these scripts? Fuel our work with a coffee!

🔗 BUYMECAFE: [BUY ME CAFE](https://buymecafe.vercel.app/)

🔗 WEBSITE: [BUY SCRIPTS](https://thogtoolhub.com/)
