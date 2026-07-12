# TotalMiners Public Website ⛏️

<p align="center">
  <a href="https://totalminers.io"><strong>totalminers.io</strong></a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Vue.js-4FC08D?style=for-the-badge&logo=vue.js&logoColor=white" alt="Vue.js">
  <img src="https://img.shields.io/badge/Chart.js-FF6384?style=for-the-badge&logo=chart.js&logoColor=white" alt="Chart.js">
  <img src="https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white" alt="Nginx">
  <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker">
  <img src="https://img.shields.io/badge/i18n-26A69A?style=for-the-badge&logo=google-translate&logoColor=white" alt="i18n">
</p>




The official public-facing web platform and user dashboard for the **totalminers.io** mining hotel infrastructure. This frontend application serves as the primary hub for clients to calculate mining profitability, manage hardware units, and monitor live performance data.

---
<p align="center">
  <img src="./docs/sh.png" alt="Meract Platform Preview" width="100%">
</p>


## 🛠️ Tech Stack & Key Features

* **UI Architecture:** Built on `Vue.js` (Vue CLI) with a responsive, component-driven dashboard system.
* **Advanced Visualizations (Chart.js):** Powered by `Chart.js` to render high-fidelity, interactive historical tracking models, including:
  * Live Bitcoin (BTC) market price trends.
  * Personal mining statistics, hashrate fluctuations, and performance metrics.
* **Hardware Power Calculator:** An interactive hardware computation module allowing users to input specific parameters and instantly calculate power requirements, costs, and potential mining yields.
* **Microservices & REST API Integration:** Heavily integrated into a distributed ecosystem. The client-side application orchestrates communication across multiple backend microservices via REST API to perform direct, real-time miner hardware manipulation.
* **Web Server & Reverse Proxy:** Structured with a production-optimized `Nginx` server configuration to ensure secure static routing and seamless Single Page Application (SPA) routing fallbacks.
* **Containerization:** Bundled within a standalone, multi-stage `Docker` configuration for optimized deployment pipelines.
* * **Many-languages, uses i18n:** Using data-objects for translate text.

---
<p align="center">
  <img src="./docs/sh1.png" alt="Meract Platform Preview" width="100%">
</p>
<p align="center">
  <img src="./docs/sh2.png" alt="Meract Platform Preview" width="100%">
</p>

## 🚀 Local Development Workflow

### 1. Dependency Resolution
Fetch and install all localized frontend packages:
```bash
npm install
```

### 2. Live Hot-Reload Server
Launch the local development engine:
```bash
npm run serve
```
> The web application will immediately spin up and point to: `http://localhost:8080/`

### 3. Production Resource Bundling
Compile, minify, and compress assets for deployment:
```bash
npm run build
```

### 4. Code Hygiene & Linting
Examine script parameters and automatically fix syntax anomalies:
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
* `vue.config.js` — Handles Webpack engine adjustments, path resolution shortcuts, and API proxy configuration hooks for local development.

## 🗂️ Project Directory Layout

```text
./
├── nginx.conf          # Caching & SPA reverse-proxy routing blueprint
├── vue.config.js       # Webpack aliases & local API proxy settings
├── public/             # Static root index, favicon, and core assets
└── src/
    ├── main.js         # Vue application bootstrapping entrypoint
    ├── App.vue         # Root component view
    ├── i18n/           # Global translation files and translation hook
    ├── router/         # Application view routing configuration
    └── components/     # Application modular feature blocks
        ├── BlockCalculator.vue  # Hardware computations engine
        ├── ChartLine.vue        # Chart.js line graphing wrapper
        ├── MyMiners.vue         # RestAPI direct hardware management 
        ├── MyStat.vue           # Personalized client stats grid
        ├── AppDashboard.vue     # Aggregated main core container
        └── AppTickets.vue       # Customer billing and text support
        else...
```

---
