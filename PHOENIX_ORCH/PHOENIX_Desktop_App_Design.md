## 🏗️ PHOENIX ORCH SPA ARCHITECTURE - COMPREHENSIVE NAVIGATION STRUCTURE

### **🎯 MAIN NAVIGATION BAR (Top Level)**

```typescript
enum MainNavRoute {
  CONSOLE = "/console",           // Command Console (Default)
  DOSSIERS = "/dossiers",         // Campaign Management
  RDEPOT = "/rdepot",             // Resource Depot
  TOC = "/toc",                   // Tactical Operations Center
  ORCHESTRATOR = "/orchestrator", // Master Control
  TELEMETRY = "/telemetry",       // Health Dashboard
}
```

### **🖥️ COMMAND CONSOLE (`/console`) - CHAT-FIRST INTERFACE**

#### **Main Console Layout:**
```
┌─────────────────┬───────────────────────────┬─────────────────┐
│   LEFT PANEL    │       MAIN CHAT AREA      │   RIGHT PANEL   │
│   (Collapsible) │                           │  (Collapsible)  │
├─────────────────┼───────────────────────────┼─────────────────┤
│ • A-Log         │ • Chat Thread             │ • Digital       │
│ • Artifacts     │ • Multi-Agent             │   Anatomy       │
│ • RAG Sources   │   Conversations           │ • Live Metrics  │
│ • Quick Tasks   │ • File Previews           │ • Agent Status  │
└─────────────────┴───────────────────────────┴─────────────────┘
                     ▼
┌─────────────────────────────────────────────────────────────────┐
│                         FOOTER CONTROLS                         │
│  [Action Prompter] [🎤] [📹] [🔴 REC] [ALWAYS ON] [Emergency]  │
└─────────────────────────────────────────────────────────────────┘
```

#### **Console Sub-Tabs/Blades:**
1. **Chat Thread** - Primary conversation interface
2. **Multi-Agent Comms** - Agent-to-agent communication monitor
3. **Quick Actions** - One-click task buttons
4. **File/Context Manager** - Attached documents and data

### **📁 CAMPAIGN DOSSIERS (`/dossiers`) - MISSION MANAGEMENT**

#### **Main Tabs:**
```typescript
enum DossiersTabs {
  ACTIVE_CAMPAIGNS = "active",
  CAMPAIGN_TEMPLATES = "templates", 
  MISSION_ARCHIVES = "archives",
  RAG_KNOWLEDGE_BASES = "knowledge",
  AGENT_TEMPLATES = "agent-templates",
}
```

#### **Blade Components:**
1. **Campaign Creator Wizard**
   - Objective Definition
   - Agent Team Assembly
   - Resource Allocation
   - Success Criteria

2. **Live Campaign Dashboard**
   - Progress Tracking
   - Agent Performance
   - Resource Consumption
   - Timeline Visualization

3. **RAG Training Interface**
   - Knowledge Base Management
   - Training Progress
   - Source Validation
   - Integration Testing

### **🛠️ RESOURCE DEPOT (`/rdepot`) - AGENT & TOOL FABRICATION**

#### **Main Tabs:**
```typescript
enum ResourceDepotTabs {
  PROTOCOL_FORGE = "forge",           // Tool Creation
  DATA_INGRESS_BRIDGE = "ingress",    // Data Sources
  UNIT_DELEGATION = "delegation",     // Agent Management
  FRAMEWORK_INTEGRATION = "frameworks", // External Systems
  PROVIDER_ECONOMICS = "economics",   // Cost Optimization
  KNOWLEDGE_ACQUISITION = "knowledge", // Learning Sources
}
```

#### **Blade Components:**

**A. Protocol Forge Blades:**
1. **Connector Library** - Pre-built protocol adapters
2. **Tool Designer** - Custom tool creation interface
3. **API Composer** - REST/gRPC/WebSocket builder
4. **Protocol Testing** - Connection validation suite

**B. Unit Delegation Blades:**
1. **Agent Gallery** - Browse existing agents
2. **Agent Creator** - Multi-source agent creation
3. **Role Assigner** - Hierarchy position assignment
4. **Capability Manager** - Skill and tool assignment

**C. Framework Integration Blades:**
1. **Framework Discovery** - Auto-detect external systems
2. **Adapter Configurator** - Connection setup
3. **Command Mapping** - Control translation
4. **Security Bridge** - Authentication and permissions

### **🎮 TACTICAL OPERATIONS CENTER (`/toc`) - MONITORING & CONTROL**

#### **Main Tabs:**
```typescript
enum TacticalOpsTabs {
  MISSION_STATUS = "status",         // Live Agent Matrix
  EXECUTION_TIMETABLE = "schedule",  // Task Scheduler
  VITAL_SIGNS = "vitals",           // Health Telemetry
  COMMUNICATIONS_AUDIT = "comms",   // Message Monitoring
  RESOURCE_MONITOR = "resources",   // System Resources
}
```

#### **Blade Components:**

**A. Mission Status Blades:**
1. **Agent Matrix** - Grid view of all agents
2. **Hierarchy Map** - Visual command structure
3. **Performance Metrics** - Individual agent stats
4. **Alert Center** - Notifications and warnings

**B. Vital Signs Blades:**
1. **Digital Anatomy** - Full-screen health visualization
2. **Body Metrics** - Infrastructure health
3. **Mind Metrics** - Cognitive performance
4. **Heart Metrics** - Emotional intelligence
5. **Spirit Metrics** - Existential health

### **👑 ORCHESTRATOR MASTER CONTROL (`/orchestrator`) - GOD MODE**

#### **Main Tabs:**
```typescript
enum OrchestratorTabs {
  COMMAND_HIERARCHY = "hierarchy",
  AUTONOMOUS_CONTROL = "autonomous",
  EMERGENCY_PROTOCOLS = "emergency",
  SYSTEM_CONFIGURATION = "config",
  EVOLUTION_TRACKER = "evolution",
}
```

#### **Blade Components:**

**A. Command Hierarchy Blades:**
1. **Rank Management** - Authority level configuration
2. **Permission Matrix** - Access control by role
3. **Override Controls** - Human intervention settings
4. **Chain of Command** - Reporting structure editor

**B. Autonomous Control Blades:**
1. **Self-Orchestration Settings** - Autonomous agent creation rules
2. **Resource Boundaries** - Deployment constraints
3. **Learning Parameters** - AI behavior tuning
4. **Ethical Guardrails** - Moral boundaries

**C. Emergency Protocols Blades:**
1. **Kill Switch Panel** - Individual agent termination
2. **System Isolation** - Emergency containment
3. **Backup Controls** - Data preservation
4. **Recovery Procedures** - Restart and repair

### **🏥 HEALTH TELEMETRY (`/telemetry`) - MEDICAL DASHBOARD**

#### **Main Tabs:**
```typescript
enum TelemetryTabs {
  DIGITAL_ANATOMY = "anatomy",
  REAL_TIME_METRICS = "realtime",
  HEALTH_HISTORY = "history",
  DIAGNOSTIC_TOOLS = "diagnostics",
  WELLNESS_PLAN = "wellness",
}
```

#### **Blade Components:**

**A. Digital Anatomy Blades:**
1. **3D Body Visualization** - Interactive system model
2. **Organ System Views** - Focus on specific subsystems
3. **Vital Sign Monitors** - Real-time metric displays
4. **Alert Overlay** - Problem area highlighting

**B. Diagnostic Tools Blades:**
1. **System Scanner** - Comprehensive health check
2. **Performance Analyzer** - Bottleneck identification
3. **Security Auditor** - Vulnerability assessment
4. **Repair Assistant** - Automated fix suggestions

### **🚀 QUICK ACCESS BLADES (Slide-out Panels)**

#### **Global Quick Panels:**
1. **Agent Quick View** - Mini status for selected agent
2. **Task Creator** - Rapid task assignment
3. **Communication Panel** - Direct message to agents
4. **Emergency Controls** - Always-available kill switches
5. **Search & Command** - Universal command interface

### **📊 DASHBOARD WIDGET SYSTEM**

#### **Customizable Dashboard Elements:**
1. **Agent Army Overview** - Force composition at a glance
2. **System Health Gauge** - Overall vitality score
3. **Active Campaigns** - Mission progress summary
4. **Resource Consumption** - CPU/Memory/Network usage
5. **Emotional State** - Current mood and stability
6. **Ethical Compass** - Recent moral decisions
7. **Learning Progress** - Knowledge acquisition rate
8. **Network Activity** - Communication traffic

### **🎯 NAVIGATION FLOW RECOMMENDATIONS**

#### **Primary User Journeys:**

**1. Daily Operations Flow:**
```
Console (Chat) → Check Telemetry → Review Active Campaigns → Monitor Agents
```

**2. Mission Planning Flow:**
```
Dossiers (Create Campaign) → Resource Depot (Assemble Team) → TOC (Monitor)
```

**3. Emergency Response Flow:**
```
Telemetry (Identify Issue) → Orchestrator (Intervene) → TOC (Verify Resolution)
```

**4. System Maintenance Flow:**
```
Telemetry (Health Check) → Resource Depot (Updates) → Orchestrator (Tuning)
```

### **🔧 TECHNICAL IMPLEMENTATION STRUCTURE**

```typescript
// Recommended Component Hierarchy:
<PhoenixApp>
  <GlobalNavBar />
  <MainLayout>
    <SidebarQuickAccess />     // Collapsible left panel
    <MainContentArea>
      <Route path="/console" component={CommandConsole} />
      <Route path="/dossiers" component={CampaignDossiers} />
      <Route path="/rdepot" component={ResourceDepot} />
      <Route path="/toc" component={TacticalOpsCenter} />
      <Route path="/orchestrator" component={OrchestratorControl} />
      <Route path="/telemetry" component={HealthTelemetry} />
    </MainContentArea>
    <SlideOutPanels />         // Contextual right panels
  </MainLayout>
  <GlobalFooter />
  <EmergencyOverlay />         // Always available emergency controls
</PhoenixApp>
```

This structure provides comprehensive coverage of all Phoenix ORCH capabilities while maintaining the CHAT-first philosophy and ensuring critical controls are always accessible. The blade/tab system allows deep diving into specific functionalities without losing context or navigation flow.
