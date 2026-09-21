# integroUA Marketing Website

Production-ready static marketing website for **integroUA** — analytics-driven marketing strategy, competitor research, and execution roadmaps for businesses and agencies.

Designed for version control on **GitHub** and zero-config deployment to **Cloudflare Pages**.

---

## 📁 Directory Structure

```text
.
├── .gitignore               # System, editor, and secret exclusions
├── _headers                 # Cloudflare Pages security & caching headers
├── _redirects               # Cloudflare Pages redirect rules (custom 404)
├── README.md                # Project documentation & deployment guide
├── index.html               # Main landing page (B2B business clients)
├── agencies.html            # Agency partnership & outsourcing page
├── thanks.html              # Thank-you & booking confirmation page
├── privacy.html             # Privacy policy & compliance
├── 404.html                 # Custom 404 error page
├── css/
│   └── main.css             # Unified production stylesheet & design tokens
├── js/
│   └── main.js              # Interactivity, analytics, UTM capture & forms
└── assets/
    ├── icons/               # SVG logos, symbols, and favicon
    │   ├── logo.svg         # Primary integroUA brand logo
    │   ├── logo-symbol.svg  # 4-quad brand mark
    │   ├── logo-dark.svg    # Dark variant for light backgrounds
    │   └── favicon.svg      # Vector site icon
    ├── images/              # Media assets & social cards
    │   └── og-integroua.svg # Open Graph preview image (1200x630)
    └── integro-strategy-example.pdf  # Sample deliverable
```

---

## 🚀 Deployment to Cloudflare Pages

### Option 1: Via GitHub Integration (Recommended)
1. Push this repository to GitHub:
   ```bash
   git init
   git add .
   git commit -m "feat: initial integroUA static site release"
   git branch -M main
   git remote add origin https://github.com/<your-username>/integroua-website.git
   git push -u origin main
   ```
2. In the [Cloudflare Dashboard](https://dash.cloudflare.com/):
   - Navigate to **Workers & Pages** → **Create application** → **Pages** → **Connect to Git**.
   - Select the `integroua-website` repository.
   - Set **Build settings**:
     - **Framework preset**: `None`
     - **Build command**: *(leave blank)*
     - **Build output directory**: `/` (or root)
   - Click **Save and Deploy**.

### Option 2: Direct Upload via Wrangler CLI
```bash
npx wrangler pages deploy . --project-name=integroua
```

---

## 💻 Local Development

Run any static HTTP server from the project root:

```bash
# Python 3
python -m http.server 8000

# Node / npx
npx serve .
```

Open [http://localhost:8000](http://localhost:8000) in your browser.
