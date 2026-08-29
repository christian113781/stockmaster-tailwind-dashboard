# StockMaster Inventory Pro

> A clean, fully responsive **inventory management dashboard** built with HTML, Tailwind CSS, and Alpine.js — no build tools, no backend required.

🔗 **Live Demo:** [stockmaster-tailwind-dashboard.vercel.app](https://stockmaster-tailwind-dashboard.vercel.app/)

---

## Screenshot

![Inventory Dashboard](https://stockmaster-tailwind-dashboard.vercel.app/assets/preview.png)

---

## Features

- **Inventory Dashboard** — KPI stat cards, stock movement bar chart, category donut chart, revenue trend line chart
- **Products** — full product table with search, filters, and a multi-step Add Product modal
- **Purchase Orders** — order listing with status badges and approval workflow UI
- **Stock Movements** — transfer log with in/out/transfer types and warehouse tags
- **Suppliers** — supplier directory with performance ratings
- **Warehouses** — utilisation bars per warehouse location
- **Profile** — user profile page with activity feed
- **Auth pages** — Login and Register pages
- **404 page** — custom error page
- **Dark mode** — persisted via `localStorage`, respects `prefers-color-scheme`
- **Collapsible sidebar** — icon-only collapsed mode on desktop, off-canvas on mobile
- **Accessible** — skip links, `aria-*` attributes, focus traps in modals, keyboard navigation throughout

---

## Tech Stack

| Layer | Technology |
|---|---|
| Markup | HTML5 (multi-page, no framework) |
| Styling | [Tailwind CSS](https://tailwindcss.com/) via CDN + custom `style.css` |
| Interactivity | [Alpine.js v3](https://alpinejs.dev/) via CDN |
| Typography | [Poppins](https://fonts.google.com/specimen/Poppins) (Google Fonts) |
| Deployment | [Vercel](https://vercel.com/) |

No npm, no bundler, no backend. Drop the files in any static host and it works.

---

## Project Structure

```
stockmaster/
├── index.html              # Dashboard (main page)
├── products.html           # Product catalog
├── purchase-orders.html    # Purchase orders
├── stock-movements.html    # Stock movement log
├── suppliers.html          # Supplier directory
├── warehouses.html         # Warehouse management
├── profile.html            # User profile
├── login.html              # Login page
├── register.html           # Register page
├── 404.html                # 404 error page
└── assets/
    ├── css/
    │   └── style.css       # Custom styles (sidebar, charts, modal, dark mode)
    └── js/
        └── main.js         # Shared Alpine.js logic (sidebar, notifications, modal plumbing, chart data)
```

---

## Getting Started

No installation needed. Just clone and open.

```bash
git clone https://github.com/your-username/stockmaster.git
cd stockmaster
open index.html
```

Or serve locally with any static server:

```bash
# Python
python -m http.server 3000

# Node (npx)
npx serve .
```

Then visit `http://localhost:3000`.

---

## Pages

| Page | URL | Description |
|---|---|---|
| Dashboard | `/index.html` | KPI cards, charts, recent movements, alerts |
| Products | `/products.html` | Product table, Add Product modal |
| Purchase Orders | `/purchase-orders.html` | PO list with status tracking |
| Stock Movements | `/stock-movements.html` | In/out/transfer log |
| Suppliers | `/suppliers.html` | Supplier directory |
| Warehouses | `/warehouses.html` | Warehouse utilisation |
| Profile | `/profile.html` | User account page |
| Login | `/login.html` | Sign-in form |
| Register | `/register.html` | Sign-up form |
| 404 | `/404.html` | Not found page |

---

## Dashboard Widgets

- **Stat cards** — Total SKUs, Stock Value, Low Stock Alerts, Out of Stock
- **Stock Movement chart** — grouped bar chart (Stock In vs Out), last 7 days
- **By Category** — horizontal progress bars + SVG donut chart
- **Revenue Trend** — SVG line chart with target line, last 6 months
- **Top Products** — ranked by revenue with proportional bars
- **Supplier Performance** — on-time delivery rate per supplier
- **Purchase Order Status** — SVG donut breakdown (Completed / In Transit / Pending / Cancelled)
- **Stock Ageing** — stacked bar showing days since last movement
- **Recent Movements** — scrollable table with status badges
- **Low Stock Alerts** — quick reorder list
- **Warehouse Utilisation** — progress bars per location

---

## Customisation

All data is defined as plain JavaScript arrays in `main.js` and `index.html`. To connect a real backend, replace the static arrays with `fetch()` calls in the Alpine component's `init()` hook.

**Colors** are set in the Tailwind config block inside each HTML file:

```js
tailwind.config = {
  theme: {
    extend: {
      colors: {
        brand: {
          50: '#f0f4ff', 400: '#818cf8',
          500: '#6366f1', 600: '#4f46e5', 700: '#4338ca',
        }
      }
    }
  }
}
```

Swap the hex values to rebrand the entire UI instantly.

---

## Browser Support

Works in all modern browsers (Chrome, Firefox, Safari, Edge). Requires JavaScript enabled.

---

## License

MIT — free to use, modify, and distribute.

---

## Author

Built with ❤️ using Tailwind CSS + Alpine.js.
