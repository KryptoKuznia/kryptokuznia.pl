# kryptokuznia.pl

<h3 align="center">
  <div>
    <a href="https://github.com/KryptoKuznia/kryptokuznia.pl/issues">
        <img src="https://img.shields.io/github/issues/KryptoKuznia/kryptokuznia.pl?color=fab387&labelColor=303446&style=for-the-badge">
    </a>
    <a href="https://github.com/KryptoKuznia/kryptokuznia.pl/stargazers">
        <img src="https://img.shields.io/github/stars/KryptoKuznia/kryptokuznia.pl?color=ca9ee6&labelColor=303446&style=for-the-badge">
    </a>
    <a href="https://github.com/KryptoKuznia/kryptokuznia.pl/blob/main/LICENSE">
        <img src="https://img.shields.io/static/v1.svg?style=for-the-badge&label=License&message=MIT&logoColor=ca9ee6&colorA=313244&colorB=cba6f7"/>
    </a>
    <br>
    </div>
</h3>

> A live BTC and crypto market dashboard, built with Next.js

**kryptokuznia.pl** is a lightweight, single-page crypto market dashboard built with **Next.js**, **React**, and **Tailwind CSS**. It aggregates data from **Binance**, **CoinGecko**, and **Alternative.me** into one view and auto-refreshes every minute, without reloading the page.

## 📊 Features

- live BTC/USDT price from Binance — price, 24h change, high/low, volume
- top-crypto market table (BTC, ETH, SOL, BNB) from CoinGecko — 24h / 7d / 30d change
- global market cap and BTC dominance
- Fear & Greed Index gauge
- ATH (all-time high) card for tracked assets
- background auto-refresh every 60 seconds
- independent fetching per source (`Promise.allSettled`) — one API failing doesn't take down the rest of the dashboard
- `GET /api/dashboard` endpoint returning the aggregated data as JSON

## 📋 Requirements

- Node.js 20+
- npm

## 🛠️ Installation

```bash
git clone https://github.com/KryptoKuznia/kryptokuznia.pl.git
cd kryptokuznia.pl
npm install
```

### ❄️ Using devenv

The project ships a [devenv](https://devenv.sh/) config that pulls in Node.js and npm for you:

```bash
devenv shell
```

## 📖 Usage

```bash
npm run dev
```

The app starts on [http://localhost:3000](http://localhost:3000).

| Command          | Description                  |
| ---------------- | ----------------------------- |
| `npm run dev`   | start the dev server          |
| `npm run build` | production build              |
| `npm run start` | run the production build      |
| `npm run lint`  | lint the codebase             |

## 🗂️ Data Sources

- [Binance API](https://binance-docs.github.io/apidocs/) — BTC/USDT price and volume
- [CoinGecko API](https://www.coingecko.com/en/api) — market and global data
- [Alternative.me](https://alternative.me/crypto/fear-and-greed-index/) — Fear & Greed Index

## 👨🏻‍💻 Development

The development environment is built around [devenv](https://devenv.sh/) and [direnv](https://direnv.net/).

1. **Clone the repository**

   ```sh
   git clone https://github.com/KryptoKuznia/kryptokuznia.pl.git
   cd kryptokuznia.pl
   ```

1. **Activate the environment**

   If you have Nix and direnv installed, the environment activates automatically when you enter the directory. Otherwise:

   ```sh
   direnv allow
   ```

1. **Run the server**

   `devenv` defines a `web` process that runs `npm run dev`:

   ```sh
   devenv up
   ```

## ⚠️ Disclaimer

Data is provided for informational purposes only and does not constitute investment advice.

## 📜 License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.
