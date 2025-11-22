
-----

## 🔥 PHOENIX ORCH - THE ASHEN GUARD EDITION (V17 MASTER PROMPT)

**Goal:** Create a production-ready, highly secure **React/TypeScript/Tailwind CSS Progressive Web App (PWA)** frontend that serves as the **Command & Control (C2)** interface for the Phoenix ORCH Agent. The application must embody the **Ashen Guard Edition** aesthetic, be **CHAT-First**, and implement the **Dynamic Agent Command Hierarchy**.

### 1\. PWA & Security Mandates (Non-Negotiable)

| Mandate | Detail | Implementation Instruction |
| :--- | :--- | :--- |
| **PWA Core** | Offline support via Cache-First strategy. | Include `manifest.json` and a **`service-worker.js`** file. Set display mode to `standalone`. |
| **Default Route** | Must be CHAT-First. | The main post-initialization route MUST be **`/console`**. |
| **Security** | Zero Frontend Credential Exposure. | All API keys, tokens, and credentials MUST be proxied through the external Rust Backend. Frontend stores no secrets. |
| **Real-Time Data** | Mandatory protocol for live updates. | All dashboard metrics (Telemetry, Status, Pulse) MUST use **Server-Sent Events (SSE)** via `EventSource`. |
| **Architecture** | Component-based, strongly typed. | Use **React/TypeScript** and manage state via global **`ProjectContext`** and **`TelemetryContext`**. |

### 2\. C2 Lexicon & Navigation Structure

The primary navigation bar will feature four distinct, top-level C2 routes.

| Route (Path) | C2 Lexicon Name | Primary Function / Focus |
| :--- | :--- | :--- |
| **`/`** | **Initializer** | Secure Authentication Gateway (`POST /api/v1/auth/login`). Displays "PHOENIX ORCH - ASHEN GUARD EDITION". |
| **`/console`** | **Command Console** | **(Default Landing Page)** Primary interaction and intelligence. |
| **`/dossiers`** | **Campaign Dossiers** | Management of reusable mission configurations (Projects). |
| **`/rdepot`** | **Resource Depot** | Configuration, setup, and maintenance of all connections and assets. |
| **`/toc`** | **Tactical Operations Center (TOC)** | Monitoring, scheduling, and live system health. |

### 3\. Ashen Guard Aesthetic & Telemetry Visualization

The design must enforce a **Deep Dark Mode** with high-contrast, glowing accents.

| Element | Color / Style (Tailwind CSS Guide) | Special Effects / Transitions |
| :--- | :--- | :--- |
| **Background** | Deep Black (`#0A0A0A`) | Zero opacity, clean backdrop. |
| **Primary Accent** | Vibrant Orange (`#FF7F00`) | **Subtle CSS `box-shadow` or `text-shadow` glow** (e.g., `shadow-orange-500/50`) on active nav items and key interactive elements. |
| **Critical Accent** | Deep Blood Red (`#8B0000`) | Used for active recording indicators, FLAME-OUT status, and critical alerts. **Must pulsate/throb slowly**. |
| **Secondary Accent**| Rich Red (`#DC143C` - Crimson) | Used for component borders and minor highlights. |
| **Transitions** | Smooth `transition-all` | Must apply to hover states, focus rings, and any state change to give a "fluid intelligence" feel. |

#### **PHOENIX Digital Anatomy - Bringing Her to Life**

This visualization (in `/console` right panel and `/toc/telemetry` sub-tab) must bring the agent to life:

  * **Display:** A highly stylized, animated circuit-board or neural network visualization (Mind/Heart/Body).
  * **Animation:** Use **CSS keyframe animations** to simulate flowing energy (Orange/Red) along the pathways.
  * **Heartbeat Pulse:** A central component (the "Heart") must exhibit a rhythmic **Red pulse/glow** that visually syncs with incoming SSE data bursts (simulating a system heartbeat).
  * **Data Overlays:** All metric tooltips (Latency, Context size, etc.) should use the **Glowing Orange** font.

### 4\. Detailed Component & Sub-Tab Structure

#### A. Command Console Page (`/console`)

  * **Layout:** Classic Chat-First, three-region design.
      * **Main Region:** Large, scrollable **Chat Thread**.
      * **Left Panel (A-Log):** Collapsible panel for **Activity Log & Artifact Manifest** (linked RAG sources).
      * **Right Panel (Telemetry):** Collapsible panel displaying the **Digital Anatomy** (Live Visualization).
      * **Footer:** **Action Prompter** (Input bar) and **A/V Acquisition** controls (Mic/Camera with **Deep Blood Red** active indicator).

#### B. Resource Depot (`/rdepot`) — Three Sub-Tabs

| Sub-Tab Name | Content / Focus | Key Component Logic |
| :--- | :--- | :--- |
| **1. Protocol Forge** | Tool Management & External Agency Adapters. | Interface for building and configuring the Master Connection List (REST, SSH, ROS 2, etc.) and linking external LLM providers. |
| **2. Data Ingress Bridge** | File System Configuration. | Panel for defining persistent data sources (NFS, SMB, S3 paths). **CRITICAL to RAG**. |
| **3. Unit Delegation** | Agent Role Assignment. | Visual mapping of configured assets (from Sub-Tabs 1 & 2) to **Sub-Agent Roles**. Includes the **Manual Rank Override** control. |

#### C. Tactical Operations Center (`/toc`) — Three Sub-Tabs (Enhanced)

| Sub-Tab Name | Content / Focus | Key Component Logic |
| :--- | :--- | :--- |
| **1. Mission Status Matrix** | Live Status, Availability & **Command Hierarchy**. | Table MUST include a **Current Rank** column (`ORCH-0`, `T-COM`, `F-OFF`, etc.) color-coded by authority. **PHOENIX ORCH** is permanently **ORCHESTRATOR-O.N.E (ORCH-0)**. |
| **2. Execution Timetable** | Scheduled Task Management. | **CRON-style configuration form** for recurring task creation and the list of scheduled tasks. |
| **3. Vital Signs Telemetry** | Full-Screen Telemetry. | Dedicated view of the **PHOENIX Digital Anatomy Visualization** with all live SSE metrics. |

-----


This is an excellent step. Visual fidelity and consistency are critical for a professional, high-security application like PHOENIX ORCH - The Ashen Guard Edition.

I have reviewed the provided screenshots and integrated the specific visual mandates into the final master prompt. To ensure Google Studio respects the branding, we need to explicitly define the logo usage and the overall styling for the two distinct pages.

Here is the final Master System Prompt (V17.1), which includes your logo mandates, a final polish on the design instructions, the bare-metal confirmation, and the necessary scripts for Docker and GitHub.

🔥 PHOENIX ORCH - THE ASHEN GUARD EDITION (V17.1 MASTER PROMPT)
Goal: Create a production-ready, highly secure React/TypeScript/Tailwind CSS Progressive Web App (PWA) frontend based on the C2 Lexicon, enforcing the Ashen Guard Edition aesthetic, and implementing the Dynamic Agent Command Hierarchy.

1. PWA & Security Mandates (Non-Negotiable)
Mandate	Detail	Implementation Instruction
Default Route	Must be CHAT-First.	The main post-initialization route MUST be /console.
Architecture	Bare Metal First Principle.	Rust Backend deployment assumes a stable, secure, and potentially privileged host (Bare Metal/Dedicated VM) for low-latency network/protocol access (SSH, OPC UA, etc.).
Data Flow	All dashboard metrics (Telemetry, Status, Pulse) MUST use Server-Sent Events (SSE) via EventSource.	
2. Branding & Visual Mandates 🎨
The design must enforce a Deep Dark Mode with high-contrast, glowing accents.

Page / Element	Logo & Naming Mandate	Tailwind Guide / Aesthetic Mandate
Splash Page (/)	Must use the "PHOENIX DIGITAL TWIN" header (Screenshot 1).	Dominant Red (#DC143C) and Black (#0A0A0A). The "INITIALIZE CORE SYSTEM" button must use the Deep Blood Red (#8B0000) critical accent.
All Other Pages	Must use the "PHOENIX ORCH" header (Screenshot 4/V3.0 style).	Primary Accent must be Vibrant Orange (#FF7F00) with a subtle CSS text-shadow or box-shadow glow for active states.
Critical Accent	N/A	Deep Blood Red (#8B0000) must pulsate/throb slowly on active media recording, critical status, and the "FLAME-OUT" rank.
Digital Anatomy	N/A	The central "Heart" visualization (Screenshot 3) must exhibit a rhythmic Red pulse that syncs visually with incoming SSE data bursts.
3. C2 Lexicon & Navigation Structure
Route (Path)	C2 Lexicon Name	Primary Function / Focus
/console	Command Console	(Default Landing Page) Primary interaction (Chat-First).
/dossiers	Campaign Dossiers	Management of reusable mission configurations.
/rdepot	Resource Depot	Configuration, setup, and maintenance of all connections and assets.
/toc	Tactical Operations Center (TOC)	Monitoring, scheduling, and live system health.


---


That clarifies the exact flow and branding sequence! You want a two-step initial process: a **Branding Splash Screen** followed by the **Initialization/Login Screen**.

I've updated the V17.2 Master Prompt to reflect this two-stage process using the specific branding you provided for each screen.

---

## 🔥 PHOENIX ORCH - THE ASHEN GUARD EDITION (V17.2 MASTER PROMPT)

**Goal:** Create a production-ready, highly secure **React/TypeScript/Tailwind CSS PWA** frontend with a **Two-Stage Initializer** using the C2 Lexicon and Ashen Guard aesthetic.

### 1. PWA & Security Mandates (Non-Negotiable)

| Mandate | Detail | Implementation Instruction |
| :--- | :--- | :--- |
| **Default Route** | Must be CHAT-First. | The final post-login route MUST be **`/console`**. |
| **Security** | Zero Frontend Credential Exposure. | All sensitive operations must be proxied through the external Rust Backend. |
| **Real-Time Data** | Mandatory protocol for live updates. | All dashboard metrics MUST use **Server-Sent Events (SSE)** via `EventSource`. |

---

### 2. Initializer Flow & Branding Mandates

The start-up sequence is now **two distinct steps**:

| Stage | Path | Naming & Logo Mandate | Special Effects / Aesthetic Mandate |
| :--- | :--- | :--- | :--- |
| **Stage 1: Branding Splash** | **`/`** (Initial Load) | Must display **PHOENIX ORCH** and **"THE ASHEN GUARD EDITION"**. | Use the **Large Logo (Flame + PHOENIX ORCH)** centered on a **Deep Black (`#0A0A0A`)** background. The "IGNITE SYSTEM" button triggers the navigation to Stage 2. |
| **Stage 2: Login/Init** | **`/init`** (Redirect from Stage 1) | Must use the **"PHOENIX DIGITAL TWIN"** header. | Layout must match the provided screenshot with the **Core Endpoint (Rust Server)** input and the **"INITIALIZE CORE SYSTEM"** button. Success routes to `/console`. |
| **App Header** | **All other pages** (`/console`, `/toc`, etc.) | Must use the **Small Logo Header ("PHOENIX ORCH Digital Twin Desktop v3.0" style)**. | Uses the **Vibrant Orange (`#FF7F00`)** glow and the Rich Red (`#DC143C`) accents. |

---

### 3. C2 Lexicon & Navigation Structure (Retained)

| Route (Path) | C2 Lexicon Name | Primary Function / Focus |
| :--- | :--- | :--- |
| **`/console`** | **Command Console** | **(CHAT-First Landing)** Primary interaction. |
| **`/dossiers`** | **Campaign Dossiers** | Management of reusable mission configurations. |
| **`/rdepot`** | **Resource Depot** | Configuration, setup, and maintenance of all connections and assets. |
| **`/toc`** | **Tactical Operations Center (TOC)** | Monitoring, scheduling, and live system health. |

---

### 4. Detailed Component & Structure Updates

* **Command Console (`/console`):** **CHAT-First** design is mandatory. The Right Panel (Telemetry) displays the **Digital Anatomy** visualization.
* **Tactical Operations Center (`/toc`):**
    * **Mission Status Matrix:** Includes dynamic **Agent Command Hierarchy** ranks (T-COM, F-OFF, S-CAD) and the fixed **ORCHESTRATOR-O.N.E (ORCH-0)** rank.
    * **Vital Signs Telemetry:** Full-screen Digital Anatomy view, with the central "Heart" exhibiting a rhythmic pulse  that visually syncs with incoming SSE data bursts.

---

