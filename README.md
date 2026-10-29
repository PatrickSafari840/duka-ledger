# Duka Ledger

**Sales & stock tracker for small shops. Works offline, in French or English, with prices in Congolese francs or US dollars.**

🔗 **Live demo:** https://patricksafari840.github.io/duka-ledger/

Many small shops ("duka" in Swahili) in Goma still track sales in a notebook. Duka Ledger turns a phone into a simple point of sale: tap the products a customer buys, choose how they paid, and the stock and the day's figures update instantly.

## Features

- **Fast sale screen**: tap products to build a sale, adjust quantities, pick *Cash*, *Mobile Money* or *On credit*.
- **Live stock**: stock goes down with every sale; low-stock and out-of-stock alerts per product.
- **Dashboard**: today's revenue, profit and margin, average sale, 7-day trend, a 14-day revenue chart, best sellers and payment mix.
- **Two currencies**: prices are stored in CDF; switch the whole app to USD with your own exchange rate.
- **History & export**: every sale with time and payment method, void a sale (stock is restored), export to CSV for Excel or Google Sheets.
- **Offline-first PWA**: installable on Android/desktop, keeps working without internet (service worker + `localStorage`). No account, no server: data never leaves the device.
- **Bilingual**: English / Français, remembers your choice.

On first visit the app loads 30 days of realistic demo data so you can explore; erase it from the *Stock* tab.

## Tech

Plain HTML, CSS and JavaScript (no framework, no build step), SVG chart drawn by hand, Web App Manifest and a cache-first service worker. Light/dark mode follows the system.

| File | Purpose |
|---|---|
| `index.html` | The whole app: UI, state, rendering, i18n |
| `sw.js` | Service worker that caches the app shell for offline use |
| `manifest.webmanifest`, `icon.svg` | Makes the app installable |

## Run locally

```bash
git clone https://github.com/PatrickSafari840/duka-ledger.git
cd duka-ledger
python -m http.server 8000   # then open http://localhost:8000
```

## Ideas for next steps

- Sync between devices (e.g. a small Node.js + SQLite API)
- Customer credit book with reminders by WhatsApp
- Receipt printing / sharing as image

---

Built by **Patrick Safari**, full stack developer & IT specialist in Goma, DR Congo · [Portfolio](https://patricksafari840.github.io/patrick_safari_portfolio/) · [LinkedIn](https://www.linkedin.com/in/patrick-safari-166077255/)

Licensed under the MIT License.
