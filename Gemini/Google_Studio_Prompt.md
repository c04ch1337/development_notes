This is the final, high-impact set of design directives. We are moving from a complex feature list to a beautiful, cohesive, and mission-focused application: **PHOENIX ORCH - The Ashen Guard Edition**.

I have incorporated the **CHAT-First** design, hard-coded the primary landing route, finalized the **Deep C2 Aesthetic** (glowing, dark colors), and detailed the visualization for "bringing Phoenix to life."

Per your request, I will now produce the complete, final **Master System Prompt (V17)** for the AI Studio, detailing the project **from scratch** in a single, comprehensive block. This document represents the full, agreed-upon scope.

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

### 5\. Obsidian Markdown Note

```markdown
# PHOENIX ORCH - The Ashen Guard Edition (V17 Master Prompt)

This document contains the final, comprehensive scope for the **React/Tailwind/TS PWA** frontend, incorporating the **C2 Lexicon** and **CHAT-First** design.

## Core Mandates
- **Default Route:** `/console` (CHAT-First).
- **Aesthetic:** Deep Black background with **Vibrant Orange (`#FF7F00`)** primary glow and **Deep Blood Red (`#8B0000`)** critical accents.
- **Data Flow:** All live metrics via **Server-Sent Events (SSE)**.
- **Security:** Zero frontend credential exposure.

## Navigation & C2 Lexicon
1.  **`/console`**: **Command Console** (Chat-First Home)
2.  **`/dossiers`**: **Campaign Dossiers** (Project Management)
3.  **`/rdepot`**: **Resource Depot** (Configuration)
4.  **`/toc`**: **Tactical Operations Center (TOC)** (Monitoring/Scheduling)

## Key Features & Structure

### PHOENIX ORCH (ORCH-0)
- **Design:** **Digital Anatomy** visualization with Red/Orange CSS glow animations to signify system activity and life.
- **Role:** Hard-coded as **ORCHESTRATOR-O.N.E (ORCH-0)**.

### Resource Depot (`/rdepot`) Sub-Tabs
- **Protocol Forge:** Tool/Agency Definition (Master Connection List).
- **Data Ingress Bridge:** File System (NFS/SMB/S3) RAG Source Configuration.
- **Unit Delegation:** Agent-to-Role Mapping.

### TOC (`/toc`) Sub-Tabs
- **Mission Status Matrix:** Includes dynamic **Agent Command Hierarchy** ranks (T-COM, F-OFF, S-CAD) based on the calculated **Phoenix Aptitude Score (PAS)**.
- **Execution Timetable:** CRON-style task scheduler.
- **Vital Signs Telemetry:** Full-screen Digital Anatomy.

```

-----

The entire project scope is now fully defined in this V17 Master Prompt.

As per your initial instructions, the project scope is complete. Would you like me to proceed with generating the **Docker-based scripts** and the **GitHub backup instructions** now, or do you have any final adjustments to the V17 Master Prompt?
