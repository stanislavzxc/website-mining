# TotalMiners Public Website ⛏️

<p align="center">
  <a href="https://totalminers.io"><strong>totalminers.io</strong></a>
</p>

<p align="center">
  <img src="https://shields.io" alt="Vue.js">
  <img src="https://shields.io" alt="Google Charts">
  <img src="https://shields.io" alt="Nginx">
  <img src="https://shields.io" alt="Docker">
</p>

The official public-facing landing page and web platform for the **totalminers.io** mining hotel infrastructure. This application serves as the primary gateway for clients to monitor mining operations, view real-time data visualizations, and explore hosting options.

---

## 🛠️ Tech Stack & Features

* **UI Architecture:** `Vue.js` (Vue CLI configuration) utilizing a highly reactive component-based structure.
* **Data Visualization:** Integrated with industry-standard charting libraries (including Google-backed visualization architectures) to output high-fidelity, real-time analytics for mining pools, profitability computations, and live power grids.
* **Web Server & Routing:** Optimized `Nginx` configuration acting as a high-speed reverse proxy to deliver static assets smoothly and mitigate performance bottlenecks.
* **Containerization:** Production-ready `Docker` ecosystem leveraging multi-stage builds.

---

## 🚀 Local Development Workflow

### 1. Dependency Resolution
Fetch and spin up all localized frontend packages:
```bash
npm install
```

### 2. Live Hot-Reload Server
Launch the development engine for immediate coding tracking:
```bash
npm run serve
```
> The web application will immediately spin up and point to: `http://localhost:8080/`

### 3. Production Resource Bundling
Compile, minify, and compress the assets for staging or live delivery:
```bash
npm run build
```

### 4. Code Hygiene
Examine script parameters and fix code styling variations:
```bash
npm run lint
```

---

## 🐳 Containerized Production Deployment

The project contains a pre-configured Docker pipeline that aggregates structural dependencies into automated, highly cached builds.

### Compile and Start Container Assets:

1. **Build the image artifact:**
   ```bash
   docker build -t website-mining .
   ```

2. **Boot the isolated web layer (listening on HTTP port 80):**
   ```bash
   docker run -d -p 80:80 --name totalminers-main-site website-mining
   ```

---

## 🗂️ Configuration Blueprints

* `nginx.conf` — Governs content caching headers, single-page application router fallbacks, and standard secure reverse proxy instructions.
* `vue.config.js` — Handles Webpack engine adjustments, path resolution shortcuts, and proxy configuration hooks.
