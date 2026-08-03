# BuffSense — Livestock Health Monitoring Dashboard

BuffSense is an AI-powered livestock management system designed to monitor and analyze the behavior of buffaloes in real-time. By tracking key activity metrics (such as standing/lying duration, feed intake, and rumination), BuffSense enables dairy farmers, research institutions, and veterinarians to make data-driven decisions that enhance herd health, productivity, and welfare.

Developed to address the critical need for affordable monitoring in the Indian dairy sector, BuffSense replaces expensive traditional imported systems with a highly scalable, low-cost localized solution.

---

## 🚀 Key Features

- **Real-Time Data Visualization**: An interactive, responsive telemetry dashboard representing active device states, signal strengths, and battery metrics.
- **Dynamic Geographic Tracking**: Built-in Leaflet Map showing deployment locations, central gateways, and individual collar/tail nodes clustered geographically.
- **Node-Level Behavioral Analytics**:
  - Behavior classification: **REL** (Resting/Relaxing), **RUS** (Rumination), **STN** (Standing), and **ETC** (Other/Eating).
  - Visual metrics breakdown using interactive Pie Charts and tables via Recharts.
  - Detailed activity duration formatting and chronological event logs.
  - Floating action button to download activity logs as standard CSVs.
- **Dual-Mode Sync Support**: Built-in visual architectures explaining BLE Direct local sync and cellular Cloud Gateway relay.
- **Showcase Demo Mode**: Pre-loaded mock data for nodes `150` to `158` (assigned to Gopal Gaushala, Ropar) covering a 7-month showcase range (`01-01-2026` to `30-07-2026`) for demonstration.

---

## 🛠️ Hardware & Technology Status

- **TRL Level**: >9 (Fully commercialized and deployed in large-scale setups)
- **Field Validation**: Deployed in collaboration with **GADVASU** (Guru Angad Dev Veterinary and Animal Sciences University) and **NABARD** (National Bank for Agriculture and Rural Development).
- **Adoption**: Commercially deployed, currently benefiting over **150,000+ farmers** across India.
- **Components**:
  1. **Smart Collar Node / Tail Sensor**: Energy-efficient, durable sensors worn by livestock, designed for continuous posture logging.
  2. **Central BLE-4G Herd Gateway**: A robust farm-wide receiver unit capable of aggregating telemetry from up to 300 active nodes and relaying data to cloud endpoints.

---

## 📡 System Architectures & Modes

### 1. BLE Direct Node Sync (Offline-First)
Collar and tail nodes track behavior and log metrics locally. Telemetry is securely pulled using a local mobile application or handheld receiver over Bluetooth Low Energy (BLE) when in close range. Ideal for grazing pastures with no permanent network access.

### 2. Cloud Gateway Pipeline (Real-Time Cloud)
Active collar/tail nodes continuously stream raw sensor data to the central farm gateway. The gateway aggregates all herd telemetry and uploads it to the BuffSense cloud platform via a secure 4G cellular connection, triggering 24/7 automated alerts and remote web access.

---

## 📍 Active Deployment Sites

The dashboard visualizes live deployments across major locations:
- Gopal Gaushala, Ropar
- Mand, Chahal
- GADVASU, Ludhiana
- Daljit Sandhu Farm, Rupnagar, Punjab
- Tarn Taran
- NABARD, Chandigarh

---

## 💻 Tech Stack & Installation

This project is built using:
- **Frontend Core**: [React](https://react.dev/) + [Vite](https://vite.dev/) (Javascript ES6+)
- **Styling**: Vanilla CSS (Premium Glassmorphism & Cyberpunk dark accents)
- **Mapping**: [React Leaflet](https://react-leaflet.js.org/) (Leaflet.js)
- **Icons**: [Lucide React](https://lucide.dev/)
- **Charts**: [Recharts](https://recharts.org/)
- **Date Handling**: [date-fns](https://date-fns.org/)

### Getting Started

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/sksuman14/Buffsense.git
   cd Buffsense
   ```

2. **Install Dependencies**:
   ```bash
   npm install
   ```

3. **Run Dev Server**:
   ```bash
   npm run dev
   ```
   Open `http://localhost:5173` in your browser.

4. **Build for Production**:
   ```bash
   npm run build
   ```
   The compiled assets will be built in the `/dist` folder.
