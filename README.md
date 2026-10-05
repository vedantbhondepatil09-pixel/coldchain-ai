# ❄️ ColdChain AI — AI-Powered Cold Chain Intelligence & Automated Multi-Party Liability Settlement

> **Built for Fireblaze Tech League 5.0 Hackathon**  
> *Theme: AgriTech, Smart Logistics & AI Agents for Food Loss Reduction*

---

## 🎯 Executive Summary & Problem Context

In India, **over 30% of perishable agricultural produce and temperature-sensitive goods spoil before reaching retail shelves**, resulting in an annual economic loss exceeding **₹1.5+ Lakh Crore ($18+ Billion)**.

### Root Causes in Indian Cold Logistics:
1. **Unmonitored Transit Thermal Breaches**: Reefer compressor trips, auxiliary genset failures during ghat descents (e.g. Kasara / Igatpuri / Banihal), or drivers switching off chillers to save diesel.
2. **Delayed Inbound Dock Bay Congestion**: Trucks waiting 3-5 hours under 38°C sun outside wholesale cold storages before plug-in power is connected.
3. **Multi-Party Liability Disputes**: When produce arrives spoiled, Transporters blame Farmers (poor pre-cooling), Farmers blame Transporters (reefer failure), and Transporters blame Dock Managers. Insurance claims take 9-18 months to arbitrate due to missing or contested paper logs.

**ColdChain AI** solves this by unifying **real-time edge IoT telematics, Arrhenius $Q_{10}$ bio-thermal degradation modeling, offline-first driver checkpoints, and autonomous multi-agent dispute arbitration** under statutory Indian transport acts.

---

## 🚀 Key Features

### 1. 📊 Executive Multi-Stakeholder Intelligence Dashboard
- **Role Switcher**: Custom operational views tailored for **Farmers / FPOs**, **Transporters**, **Warehouse Cold Docks**, **Retailers / Quick-Commerce**, and **Admin / Insurance Assessors**.
- **Real-time KPI Metrics**: Total protected cargo value (₹), active critical thermal excursions, cold chain integrity rating (96.8%), and estimated salvage recovery.
- **Search & Filter**: Filter shipments by Indian transit corridors, crop categories (Export Grapes, Ratnagiri Mangoes, Kashmiri Apples, Strawberries, Dairy, Vaccines), and severity levels.

### 2. 📈 Live Telemetry & Thermal Chamber Studio
- Interactive **Recharts multi-axis visualization** plotting Chamber Temperature, Ambient Heat Curve, Safe Threshold Band (`T_min` to `T_max`), and Chamber Humidity (%).
- Real-time diagnostics: Carrier Transicold & Thermo King compressor health, battery reserve, solar input, door sensor seals, and GPS speed.
- Real-time 4-second simulated IoT streaming mesh across major Indian transit corridors (NH-44, NH-48, NH-160).

### 3. 🗺️ GPS Cold Corridor & Emergency Storage Rerouting Map
- Visual waypoint tracker for Indian highway routes (e.g. *Nashik Vineyards → Kasara Ghat → Kalyan Mega Cold Hub → JNPT Mumbai Port*).
- **Proactive AI Reroute Recommender**: Detects nearest certified cold storage facility (with capacity in tons and direct helpline) to salvage distressed cargo before total spoilage.

### 4. 🧬 Spoilage AI Engine ($Q_{10}$ Bio-Thermal Model)
- Mathematical kinetic shelf-life decay calculation:
  $$\text{Acceleration Factor } AF = Q_{10}^{\frac{T_{\text{chamber}} - T_{\text{target\_max}}}{10}}$$
  $$\text{Accumulated Degree-Hours } = \int \max(0, T(t) - T_{\text{target\_max}}) \, dt$$
- Real-time remaining shelf-life tracker (e.g., *4.2 days remaining vs 7.0 days baseline*).
- Financial loss quantification & salvage markdown calculator in INR (₹).

### 5. 📱 Driver Mobile-First Field Portal (Offline-First)
- Designed for low-connectivity rural highways and ghat passes.
- **Offline Simulation Switch**: Check-ins stored securely in local browser storage (`IndexedDB`/`LocalStorage`) with automated reconciliation upon signal recovery.
- Digital checkpoint logs: Odometer (km), reefer digital meter reading, door seal integrity, defrost run verification, genset fuel gauge, and geotagged photographic proof.
- **Driver SOS Emergency Button**: Immediate escalation for highway mechanical breakdowns or road gridlocks.

### 6. ⚖️ Autonomous AI Dispute Resolution & Statutory Liability Engine
- **Multi-Agent Forensic Pipeline**:
  1. *Telemetry Agent*: Ingests degree-hours and sensor breach logs.
  2. *Chain of Custody Agent*: Correlates farmgate dispatch, transit GPS stamps, and warehouse dock gate-in timestamps.
  3. *Statutory Legal Agent*: Cross-references **Carriage by Road Act 2007 (Section 10)**, **FSSAI Cold Chain Regulations 2020 (Schedule IV)**, and **NHB Guidelines**.
  4. *Financial Allocation Agent*: Synthesizes evidence to assign fair quantitative liability splits (e.g., *65% Transporter / 20% Warehouse Dock / 15% Insurance*).
- Printable, export-ready **Official Arbitration Settlement Report**.

### 7. 🧪 Anomaly Simulation Studio
- 1-Click live fault injector:
  - *Reefer Compressor Trip* (Kasara Ghat scenario)
  - *Rear Door / Seal Ajar*
  - *Highway Heatwave Spike (+40°C)*
- Step-by-step guided walkthrough to test the end-to-end incident lifecycle.

---

## 🛠️ Tech Stack

- **Framework**: Next.js 14/16 (App Router) + TypeScript + React 19
- **Styling**: Tailwind CSS + Modern Glassmorphism + Dark/Light Theme
- **Data Visualization**: Recharts (Composed Multi-Axis Time Series)
- **Icons**: Lucide React
- **State & Simulation**: React Context + LocalStorage Offline Persistence + Simulated IoT Telemetry Engine

---

## 🏁 How to Run Locally

### Prerequisites
- Node.js (v18+ or v20+)
- npm

### Installation Steps

```bash
# 1. Navigate to the project directory
cd coldchain-ai

# 2. Install dependencies
npm install

# 3. Start the development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your web browser.

To run a production build:
```bash
npm run build
npm run start
```

---

## 🎬 Step-by-Step Hackathon Demonstration Walkthrough

1. **Explore the Dashboard**:
   - Notice the live notification ticker and the KPI cards showing protected cargo value (₹1.42 Cr+).
   - Switch roles using the top-right selector (e.g., switch from *Farmer / FPO* to *Transporter* to *Admin / Insurance*).

2. **Inspect an Active Breach**:
   - Click on shipment **`CC-IN-8942`** (*Nashik Export Grapes*).
   - Switch to the **Live Telemetry & Route** tab to see the live temperature curve breaching the 2.0°C upper limit.
   - Look at the **Transit Route & GPS Cold Corridor Tracker** showing the truck near *Kasara Ghat* and the recommendation to divert to *Kalyan Agri Mega Cold Hub*.

3. **Check the Spoilage AI Engine**:
   - Switch to the **Spoilage AI Engine** tab.
   - Observe the Arrhenius $Q_{10}$ degradation metrics, accumulated degree-hours, and financial loss calculation (₹11.5L loss exposure).

4. **Test the Offline Driver Portal**:
   - Switch to the **Driver Portal** tab.
   - Toggle **"Simulated: Offline / No Signal"** to test offline mode.
   - Fill in an inspection log and click **"Save Offline Check-In"**.
   - Notice the yellow offline badge on the navbar. Toggle back to Online and click **"Sync Queued Logs"** to see instant cloud synchronization.

5. **Generate AI Multi-Party Dispute Settlement**:
   - Switch to the **AI Disputes & Legal** tab.
   - Click **"Re-Run Multi-Agent Forensic Audit"**.
   - Watch the 4-step AI pipeline execute: Ingestion → Custody Matching → Legal Clause Audit → Financial Allocation.
   - View the final **65% Transporter / 20% Warehouse / 15% Insurance** liability breakdown and click **"Print / Export Verdict"**.

6. **Inject New Anomalies**:
   - Click **"Simulate Anomaly"** on the top navigation bar to inject faults into other shipments or create a brand new consignment via **"New Shipment"**.

---

## 🏛️ Project Directory Structure

```
coldchain-ai/
├── app/
│   ├── globals.css           # Tailwind CSS styles & animations
│   ├── layout.tsx            # Global layout with theme and fonts
│   └── page.tsx              # Main unified application dashboard
├── components/
│   ├── AnomalySimulatorPanel.tsx  # Fault injection & hackathon demo wizard
│   ├── DisputeResolutionView.tsx  # Multi-agent AI legal dispute auditor
│   ├── DriverView.tsx             # Mobile-first offline-capable driver check-in
│   ├── LiveRouteMap.tsx           # Indian highway corridor waypoint map
│   ├── Navbar.tsx                 # Header with role switcher & offline sync
│   ├── NewShipmentModal.tsx       # New consignment creation wizard
│   ├── RoleViews.tsx              # Stakeholder-specific role banners
│   ├── ShipmentCard.tsx           # Interactive shipment card with gauge
│   ├── SpoilageRiskPanel.tsx      # Q10 bio-thermal shelf life calculator
│   └── TelemetryChart.tsx         # Recharts real-time telemetry visualizer
├── context/
│   └── ColdChainContext.tsx  # Central state, IoT simulator & offline queue
├── lib/
│   ├── cargoProfiles.ts      # Agricultural produce presets & thermal constants
│   ├── disputeEngine.ts      # Multi-agent audit & statutory legal engine
│   ├── mockData.ts           # Realistic Indian cold-chain dataset
│   └── spoilageEngine.ts     # Kinetic decay & emergency rerouting logic
├── types/
│   └── coldchain.ts          # Core TypeScript models
├── package.json
└── README.md
```

---

## 🏆 Hackathon Alignment (Fireblaze Tech League 5.0)

- **Scalable Architecture**: Zero server overhead, fully responsive, edge-ready data models.
- **India-Centric Domain Context**: Incorporates Nashik grapes, Kashmiri apples, Ratnagiri mangoes, Amul dairy, APMC mandis, NHAI highway corridors, and statutory legal acts (Carriage by Road Act 2007).
- **Novel AI Agent Utility**: Automated multi-party liability assignment solving India's ₹1.5 Lakh Crore cold chain dispute backlog.
