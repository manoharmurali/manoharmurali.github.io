# manoharmurali.github.io

**_The repository contains the portfolio code. 
More changes will be committed from time to time for your help._**
   
* _Look at the portfolio by clicking on above mentioned link. This was made using materialize CSS & particle background._*
  
:tada: :fireworks:

# SUTHERLAND PROPOSAL TO CNHI
## Informatica IDMC Implementation for Enterprise Data Management
### January 2026

---

## EXECUTIVE SUMMARY

### 1.1 Business Transformation at a Glance

CNHI is modernizing its enterprise data capabilities by adopting **Informatica Intelligent Data Management Cloud (IDMC)** as the unified control plane for data integration, quality governance, and master data management. This greenfield implementation will:

- **Eliminate manual ETL workloads** for IBM mainframe and file-based systems (Week 23 production value)
- **Establish data quality as a first-class operation** with 5,000+ automated business rules across three prioritized waves
- **Create authoritative master data** for 35M+ beneficiaries and 25K+ provider records, enabling single-customer-view and compliance
- **Catalog and govern 500+ data assets** with end-to-end lineage and business glossary alignment
- **Ensure 100% data residency** in the Kingdom of Saudi Arabia via on-premises Secure Agents, with IDMC serving purely as a cloud-based SaaS control plane

This approach combines **cloud agility with on-premises data sovereignty**, delivering a secure, compliant, operationally transparent platform that CNHI teams will own and extend confidently.

### 1.2 Why This Matters to CNHI

| **Challenge** | **Today** | **With IDMC** |
|---|---|---|
| ETL Operations | Manual, error-prone, resource-intensive | Automated, resilient, governed |
| Data Quality | Ad-hoc validation, low visibility | 5,000+ rules, scorecards, real-time remediation |
| Master Data | Fragmented beneficiary/provider records | 35M+ golden records, single source of truth |
| Governance & Compliance | Scattered documentation, audit friction | Complete catalog, lineage, PDPL-ready |
| Future-Ready Data Ops | Limited agility, siloed systems | Extensible platform ready for AI/LLM pipelines |

### 1.3 Key Innovation: Parallel POD Delivery Model

**Traditional Sequential Approach** → Bottlenecks, months of waiting, delayed value  
**Sutherland's Parallel POD Approach** → Three specialized teams working simultaneously

- **POD 1 (CDI+CDQ):** Data Integration & Quality — Weeks 1–48
- **POD 2 (MDM):** Master Data Management — Weeks 24–48 (parallel with POD 1)
- **POD 3 (CDGC):** Governance & Catalog — Weeks 11–48 (continuous)

**Result:** First production value in **Week 23** (not Week 52+), and all four IDMC modules operational by **Week 48**.

### 1.4 Project at a Glance

| **Dimension** | **Details** |
|---|---|
| **IDMC Modules** | Cloud Data Integration (CDI), Cloud Data Quality (CDQ), Master Data Management (MDM), Data Governance & Catalog (CDGC) — All 4 in scope |
| **Delivery Model** | Wave-based incremental releases with 3 parallel PODs |
| **Architecture** | Hybrid: IDMC cloud orchestration + on-premises Secure Agents (100% data residency) |
| **Source Systems** | 8+ systems: IBM (CP4I), SQL Server, PostgreSQL, Oracle, SharePoint, APIs, file landing zones, and more |
| **Data Volumes** | 10 TB historical + ongoing weekly/monthly batches |
| **Environments** | Dev, Test, Prod (production with high availability) |
| **Team Size** | 12–13 Sutherland specialists + CNHI SMEs/stewards |
| **Total Duration** | 48 weeks (12 months) from contract to full handover |
| **Production Go-Lives** | 4 incremental releases: Week 23 (CDI/CDQ), Week 33, Week 41, Week 45 (MDM) |

### 1.5 Key Milestones & Production Value Timeline

| **Milestone** | **Week** | **What's Delivered** | **Business Impact** |
|---|---|---|---|
| Infrastructure Ready | 10 | Secure Agents operational, VPN/firewall, DW schema | Foundation for rapid build |
| **Wave 1 Go-Live** | **23** | IBM + Files automation, 1,000 DQ rules, 200 catalog entries | **FIRST PRODUCTION VALUE: Manual ETL eliminated** |
| Wave 2 Go-Live | 33 | Core databases (SQL Server, PostgreSQL, Oracle), 3,000 total DQ rules | 70% data coverage operational |
| Wave 3 Go-Live | 41 | Cloud/external sources (SharePoint, APIs), 5,000 total DQ rules, complete lineage | 100% CDI/CDQ/CDGC operational |
| MDM Go-Live | 45 | 35M+ golden records, stewardship workflows | Master data production-ready |
| **Project Complete** | **48** | Full hypercare, CNHI self-sufficient, all SLAs validated | Ready for independent operations |

---

## 2. SCOPE & DELIVERABLES

### 2.1 IDMC Modules In Scope

All four IDMC modules are included in this engagement, sequenced across waves to deliver early value while building toward comprehensive governance.

#### **Cloud Data Integration (CDI)** — POD 1 Lead
- **What:** Ingest from 8+ source systems (IBM/CP4I, SQL Server, PostgreSQL, Oracle, SharePoint, APIs, files, etc.) into on-premises SQL Server DW
- **Design Objectives:** 
  - 50+ ETL/ELT mappings across three waves
  - 10 TB historical migration in Wave 0–1
  - Weekly/monthly batch processing with change-data-capture (CDC) foundation
  - Heterogeneous file support (CSV, JSON, Parquet, DB backups)
  - Error handling, quarantine patterns, reconciliation reports
- **Key Deliverables:**
  - Dimensional data warehouse design (star schema)
  - 50+ production mappings with documentation
  - Batch scheduling framework
  - Historical load reconciliation reports
  - Incremental load patterns and restart logic
- **Wave Delivery:** Waves 1, 2, 3 (15–20 mappings per wave, refined in operations)

#### **Cloud Data Quality (CDQ)** — POD 1 Lead
- **What:** Translate CNHI's business rules into enforceable, observable data quality checks
- **Design Objectives:** 
  - Up to 5,000 business rules across three prioritized waves (P0 → P1 → P2)
  - Weekly profiling of 500+ tables
  - DQ scorecards with pass-rate dashboards
  - Violation tracking and remediation workflows
  - Steward-facing task queues
- **Approach:** Rules are **indicative targets subject to discovery**. Wave 0 workshops will confirm actual rule count, prioritization, and implementation effort. Final rule volume may be adjusted per discovery outcome; success is measured by **coverage of critical domains** rather than rigid rule count.
- **Key Deliverables:**
  - 5,000 rules (estimate) implemented across waves, with actual scope confirmed post-discovery
  - DQ scorecards (target ≥90% pass rate Wave 1, ≥95% Wave 3)
  - Violation dashboards and remediation trackers
  - Steward training and workflow documentation
- **Wave Delivery:** Waves 1, 2, 3 (priority-based rule activation)

#### **Master Data Management (MDM)** — POD 2 Lead
- **What:** Create and operate authoritative golden records for beneficiaries and providers
- **Design Objectives:**
  - Match rules reflecting CNHI's data realities (noisy identifiers, multilingual names, variations)
  - Survivorship logic prioritizing authoritative sources per attribute
  - Stewardship workflows for complex matches requiring human judgment
  - Sample tuning (Wave 2, ~5M records) → full-scale loads (Wave 3)
  - Golden record creation with audit trails
- **Approach:** Match coverage targets are **qualitative** (≥98% matching confidence on sample data) rather than rigid precision/recall commitments, allowing refinement during Waves 2–3. Success is measured by **operational readiness** and **steward confidence** in golden records.
- **Key Deliverables:**
  - MDM match rules and survivorship hierarchies
  - 35M+ beneficiary golden records (wave 3–4 load)
  - 25K+ provider golden records
  - Stewardship workflows and approval processes
  - Sample load validation report (Wave 2)
  - Full-scale load reconciliation (Wave 3)
- **Wave Delivery:** Waves 2, 3, 4 (sample → full-scale → production)

#### **Cloud Data Governance & Catalog (CDGC)** — POD 3 Lead
- **What:** Inventory, catalog, classify, and trace all data assets and lineage
- **Design Objectives:**
  - 500+ tables cataloged (estimate, subject to discovery)
  - Native scanners (SQL Server, SharePoint) + integration-derived metadata for unavailable scanners
  - End-to-end lineage from source → Secure Agent transformations → DW
  - Business glossary import and mapping to physical assets
  - Data classification (PII, confidential, retention rules)
  - Weekly metadata scans and updates
- **Approach:** Catalog scope is **discovery-driven**. The goal is **completeness of visibility** rather than rigid table count; final scope will be confirmed during Wave 0 source profiling.
- **Key Deliverables:**
  - 500+ tables in catalog (indicative, subject to discovery)
  - Lineage visualization end-to-end
  - Business glossary terms mapped to assets
  - Data classification tags
  - Governance workflows and stewardship assignments
  - Weekly metadata scan automation
- **Wave Delivery:** Waves 1, 2, 3 (incremental catalog expansion)

### 2.2 Source Systems & Flexible Prioritization

Eight or more source systems will be integrated across three waves. **Priorities can be adjusted during Wave 0** based on CNHI's evolving business needs.

| **#** | **Source System** | **Type** | **Integration Method** | **Default Priority** | **Default Wave** | **Flexibility** |
|---|---|---|---|---|---|---|
| 1 | IBM (DB2, AS/400) | Mainframe | Via CP4I | 🔴 Critical | Wave 1 | Fixed (manual ETL elimination) |
| 2 | File Landing Zones (CSV, JSON, Parquet) | Files | SFTP/shared folder connector | 🔴 Critical | Wave 1 | Fixed (manual ETL elimination) |
| 3 | SQL Server Data Mart | RDBMS | JDBC | 🟡 High | Wave 1 | Can move to Wave 2 if needed |
| 4 | PostgreSQL | RDBMS | JDBC | 🟡 High | Wave 2 | Flexible—can swap with Oracle |
| 5 | Oracle Database | RDBMS | JDBC | 🟡 High | Wave 2 | Flexible—can move to Wave 3 |
| 6 | SharePoint Online | Cloud SaaS | OAuth 2.0 connector | 🟠 Medium | Wave 3 | Flexible—can accelerate to Wave 2 |
| 7 | REST/SOAP APIs | External | REST/SOAP connectors | 🟠 Medium | Wave 3 | Flexible—can accelerate if business urgent |
| 8 | Oracle ERP | ERP | JDBC | 🔵 Low/Deferred | Future | Can move into Wave 2/3 if access available |
| + | Additional emerging sources (MongoDB, email, etc.) | Varied | TBD per connector | 🔵 Backlog | Future | Added as needed in operations phase |

**Flexibility Model:** During Wave 0, CNHI can re-order Wave 2 and Wave 3 sources without jeopardizing delivery, provided core Wave 1 sources (IBM, Files) remain fixed. Sutherland will support this agility via sprint-based scope control and transparent dependency tracking.

### 2.3 Infrastructure & Network Deliverables

| **Component** | **Specification** | **Purpose** | **CNHI vs. Sutherland** |
|---|---|---|---|
| **Secure Agent VMs (Prod)** | 2 VMs @ 16 vCPU, 64 GB RAM, 1 TB SSD each (CDI/CDQ group + MDM group) | High-availability on-premises execution | CNHI provisions; Sutherland installs/configures |
| **Secure Agent VMs (Non-Prod)** | 2 VMs @ 8–16 vCPU, 32–64 GB RAM, 500 GB SSD (Dev + Test) | Right-sized development/testing | CNHI provisions; Sutherland installs/configures |
| **Agent Groups** | DEV, TEST, PROD-CDI-CDQ (POD 1), PROD-MDM (POD 2) | Workload isolation & environment separation | Sutherland designs & configures |
| **Network Connectivity** | IPSec site-to-site VPN (AES-256) + TLS 1.2+ HTTPS (port 443) — VPN preferred; internet egress fallback | Secure outbound tunnel from data center → IDMC cloud | CNHI network + Informatica; Sutherland validates |
| **SQL Server Data Warehouse** | 15–20 TB capacity, TDE encryption | On-premises target repository | CNHI provisions & maintains; Sutherland designs schema & tunes performance |
| **OS & Patching** | Windows Server 2022 (preferred) or RHEL Linux (where Informatica-confirmed compatible) | Secure Agent host OS | CNHI provides; Sutherland validates compatibility in Wave 0 |
| **Monitoring & Alerting** | IDMC native monitoring + local OS metrics (CPU, memory, network) | Operational visibility | Sutherland configures dashboards; CNHI operates |

**Key Assumptions:**
- Informatica will confirm **in writing** (Wave 0 dependency) that all required CDI/CDQ/MDM/CDGC connectors and modules are fully supported on Windows Server 2022 for the Saudi Arabia regional tenant.
- VPN tunnel infrastructure (IPSec endpoints, key management) is CNHI's responsibility; Sutherland assists with validation and monitoring configuration.
- SQL Server DW hardware, patching, and availability are CNHI-owned; **Sutherland provides performance tuning support** (indexing, partitioning, query optimization, maintenance job configuration).

### 2.4 Data Warehouse Performance & SLA Framework

| **Metric** | **Design Objective** | **Wave Achievement** | **Notes** |
|---|---|---|---|
| **Nightly Batch Window** | ≤3 hours for full daily processing (CDC + quality checks) | Target by Wave 1 go-live | Subject to source availability and network latency; will be jointly tuned during Week 23 cutover and Wave 2 expansion |
| **DQ Rule Pass Rate** | Wave 1: ≥90% | Wave 1: ≥90%; Wave 2: ≥92%; Wave 3: ≥95% | Targets are **design objectives**, not contractual commitments; actual rates depend on upstream data remediation (CNHI responsibility) |
| **MDM Match Coverage** | ≥98% of records matched with ≥90% confidence | Validated in Wave 2 sample (5M records), refined by Wave 3 full load | "Match coverage" = % of input records successfully matched to a golden record or correctly identified as new; precision/recall tuned during Wave 2 |
| **Catalog Completeness** | 500+ assets cataloged with lineage | Phased: 200 in Wave 1, 350 by Wave 2, 500+ by Wave 3 | Subject to actual source inventory discovered in Wave 0 |
| **Agent Availability** | 99.5% uptime (high-availability configuration, 2 agents per prod group) | Measured across nightly batch windows | Excludes CNHI-side network outages or source system unavailability |

**SLA Philosophy:** These metrics are **design targets and operational objectives** that Sutherland and CNHI will jointly tune during the project. Success is measured by **continuous improvement** and **operational readiness**, not rigid contractual pass-fail thresholds. Any variance (e.g., 92% vs. 95% DQ pass rate, or batch window 3.5 vs. 3 hours) will be addressed through optimization sprints and root-cause analysis, not penalties.

### 2.5 Explicitly Out of Scope

| **Activity** | **Why Out of Scope** | **CNHI Ownership** |
|---|---|---|
| **Source System Modifications** | Applications own their data contracts; Sutherland integrates as-is | CNHI decides if upstream systems need changes to support IDMC pipelines |
| **Data Remediation at Source** | DQ identifies issues; fixing them upstream is a business/app decision | CNHI owns root-cause analysis and remediation in source systems |
| **Enterprise Governance Policies** | Organization-level data governance, data ownership, stewardship models | CNHI defines; Sutherland enforces within IDMC configuration |
| **BI Tool Development** | Power BI, Tableau, or other reporting layer | CNHI builds reports on DW; Sutherland delivers DW with optimized schemas |
| **SQL Server DW Provisioning & Patching** | Infrastructure is CNHI's responsibility | CNHI provisions, patches, backs up; Sutherland tunes performance and design |
| **Change Management / User Adoption** | Organizational change is external to technical delivery | CNHI runs adoption programs; Sutherland provides training |
| **LLM / GenAI Model Training** | AI engineering is adjacent to data pipelines | Sutherland ensures data lineage and quality for AI inputs; CNHI builds models |
| **Post-Wave-5 Managed Services (AMS)** | Base engagement covers delivery + hypercare only | Optional post-project AMS is separate engagement (see Section 10: Engagement Terms) |

---

## 3. SOLUTION ARCHITECTURE

### 3.1 Design Philosophy: Cloud Control Plane + On-Premises Execution

**Core Principle:** IDMC is a **SaaS orchestration and governance layer** (cloud-based). All data processing, transformation, and quality checks run on **on-premises Secure Agents**. Data **never leaves CNHI's network boundary** unless explicitly authorized and masked.

```
┌─────────────────────────────────────────────────────────────────┐
│                     INFORMATICA IDMC (Cloud)                     │
│  • Design Studio (pipeline authoring)                            │
│  • Job Scheduler & Orchestration                                │
│  • Monitoring, Logs, Lineage                                    │
│  • Governance, Catalog, Glossary                                │
│  • (Saudi-hosted GCP instance for PDPL compliance)              │
└──────────────────────────┬──────────────────────────────────────┘
                           │ (Outbound-initiated TLS 1.2+ HTTPS)
                           │ (No inbound ports; metadata only)
                           │
┌──────────────────────────┴──────────────────────────────────────┐
│            CNHI DATA CENTER (On-Premises)                       │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  ┌────────────────────────────────────────────────────────┐    │
│  │  Secure Agent Groups (VMs, Windows Server 2022)        │    │
│  ├────────────────────────────────────────────────────────┤    │
│  │ POD 1: CDI/CDQ Group (2 agents HA)                     │    │
│  │   ├─ Read from IBM, Files, SQL Server, etc.           │    │
│  │   ├─ Apply transformations, DQ rules                  │    │
│  │   ├─ Load SQL Server DW                               │    │
│  │   └─ Orchestrated by IDMC cloud                       │    │
│  │                                                        │    │
│  │ POD 2: MDM Group (2 agents HA)                        │    │
│  │   ├─ Read from DW (integrated data)                   │    │
│  │   ├─ Execute match/merge logic                        │    │
│  │   ├─ Create/update golden records                     │    │
│  │   └─ Orchestrated by IDMC cloud                       │    │
│  └────────────────────────────────────────────────────────┘    │
│                                                                 │
│  ┌────────────────────────────────────────────────────────┐    │
│  │  Source Systems (Unchanged)                            │    │
│  ├────────────────────────────────────────────────────────┤    │
│  │ • IBM DB2, AS/400 (via CP4I)                           │    │
│  │ • SQL Server, PostgreSQL, Oracle (JDBC)               │    │
│  │ • SharePoint, APIs (OAuth, REST)                      │    │
│  │ • File Landing Zones (SFTP, SMB)                      │    │
│  │ • Email, MongoDB, custom connectors (as needed)       │    │
│  └────────────────────────────────────────────────────────┘    │
│                                                                 │
│  ┌────────────────────────────────────────────────────────┐    │
│  │  SQL Server Data Warehouse (Target)                    │    │
│  ├────────────────────────────────────────────────────────┤    │
│  │ • Dimensional schema (star: facts + dimensions)        │    │
│  │ • 15–20 TB capacity, TDE encryption                   │    │
│  │ • Optimized for analytics (indexes, partitioning)     │    │
│  │ • Performance-tuned by Sutherland                     │    │
│  └────────────────────────────────────────────────────────┘    │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### 3.2 Connectivity & Security Posture

#### Network Connectivity Options

**Option 1: IPSec Site-to-Site VPN (Recommended)**
- **How:** Dedicated encrypted tunnel from CNHI data center to Informatica's Saudi GCP instance
- **Protocol:** IPSec with AES-256 encryption, IKEv2
- **Benefits:** 
  - Deterministic latency and throughput
  - No public IP exposure
  - Double encryption (VPN + TLS)
  - Easier traffic inspection and monitoring
  - Supports future multi-tenancy scenarios
- **Effort:** CNHI network team + Informatica provision endpoints; Sutherland validates configuration and performance

**Option 2: Outbound HTTPS (Internet Egress)**
- **How:** Secure Agents initiate TLS 1.2+ HTTPS connections on port 443 to Informatica cloud endpoints
- **Benefits:**
  - Simple, immediate deployment (no VPN provisioning)
  - Works with standard corporate firewalls
  - Lower infrastructure overhead
- **Trade-off:** Latency variability, requires public IP whitelisting
- **Fallback:** Recommended only if VPN unavailable

**CNHI's Choice in Wave 0:** Sutherland will validate both options and recommend VPN as the primary path based on security best practices and latency requirements. Final selection will be jointly made during infrastructure workshops.

#### Data Movement & Masking

| **Scenario** | **What Flows** | **Encryption** | **Masking** |
|---|---|---|---|
| **Normal Operation** | Commands, job status, logs, metadata, counters | IPSec + TLS 1.2+ | Not needed (metadata only) |
| **Administrative Preview** | Sample records for troubleshooting (rare) | IPSec + TLS 1.2+ | **PII masked by policy** |
| **Non-Production Testing** | Full copies of non-sensitive data (Dev/Test) | IPSec + TLS 1.2+ | **All PII masked** |
| **Compliance Audit** | Lineage reports, lineage graphs (PDPL/audit) | IPSec + TLS 1.2+ | **Aggregated; no individual records** |

**Golden Rule:** Raw beneficiary or provider data never traverses CNHI's network boundary in unencrypted or unmasked form.

### 3.3 High-Availability & Scalability

#### Production Agent Groups (POD 1 & POD 2)

Each production POD runs **two Secure Agents in active-active configuration:**
- **Agent 1:** Primary execution, handles 50% of workload
- **Agent 2:** Standby, assumes full workload if Agent 1 fails
- **Failover:** Automatic; transparent to IDMC orchestration
- **Data Consistency:** Shared state via IDMC cloud coordination

**Capacity Management:**
- Wave 1: 2 agents per group sufficient for initial data loads and batch processing
- Wave 2–3: If batch windows exceed SLA or job queues grow, add third agent (elastic scaling)
- Operations: CNHI can add/remove agents per resource availability and workload

#### Non-Production Environments

- **Dev & Test:** Single agent per environment initially; can scale if needed
- **Promotion Discipline:** Same configuration across Dev → Test → Prod ensures reliability

### 3.4 OS & Platform Alignment

**Secure Agent OS Preference:**
- **Windows Server 2022** (preferred) — aligns with CNHI's Microsoft-centric operations
- **Red Hat Enterprise Linux 8.x** (supported alternative) — where CNHI prefers Linux

**Wave 0 Dependency:** Informatica will provide **written confirmation** that all required connectors and modules (CDI, CDQ, MDM, CDGC) are fully supported on Windows Server 2022 for the Saudi Arabia region, with **no feature loss vs. Linux**. If variance exists, Sutherland and CNHI will decide on a case-by-case basis.

---

## 4. DELIVERY APPROACH: WAVES & PARALLEL PODs

### 4.1 Why Waves + Parallel PODs?

**Waves** deliver incremental business value and reduce risk. **Parallel PODs** prevent bottlenecks and accelerate time-to-value.

| **Aspect** | **Traditional Sequential** | **Sutherland Wave + POD Model** |
|---|---|---|
| **CDI Completion** | All sources ready, then start CDQ | POD 1: Waves 1–3 concurrent with POD 2 MDM work |
| **Time to First Value** | 52+ weeks (after all modules complete) | **Week 23** (Wave 1 go-live: manual ETL automated) |
| **Risk** | Late discovery = cascade delays | Early wins reduce scope uncertainty |
| **Team Utilization** | Sequential = idle periods | Parallel = continuous momentum |
| **Change Agility** | Hard to re-prioritize sources | Sprint-based, re-prioritize week-to-week |

### 4.2 Wave Overview

| **Wave** | **Weeks** | **Focus** | **PODs Active** | **Production Go-Live** | **Key Business Value** |
|---|---|---|---|---|---|
| **Wave 0** | 1–10 | Foundation, discovery, DW design, infrastructure | All (setup) | — | Solid foundation, detailed requirements |
| **Wave 1** | 11–23 | IBM + Files automation, 1K DQ rules, catalog foundation | POD 1, POD 3 | **Week 23** | **Manual ETL eliminated** |
| **Wave 2** | 24–33 | Core databases, 2K DQ rules, MDM sample load | POD 1, POD 2, POD 3 | Week 33 | 70% data coverage; MDM tuning underway |
| **Wave 3** | 34–41 | Cloud/external sources, 2K final DQ rules, full MDM load | POD 1, POD 2, POD 3 | Week 41 | 100% CDI/CDQ/CDGC; golden records ready |
| **Wave 4** | 42–45 | MDM production deployment | POD 2 | Week 45 | **Master data operational** |
| **Wave 5** | 46–48 | Regression testing, optimization, handover | All | Week 48 | **CNHI self-sufficient** |

### 4.3 WAVE 0: Foundation & Design (Weeks 1–10)

**Objective:** Build solid infrastructure, detailed discovery, data warehouse design, and technical blueprints across all four IDMC modules.

#### Key Activities

| **Category** | **Activities** | **Duration** | **Deliverable** |
|---|---|---|---|
| **Discovery & Requirements** | Source system profiling (8+ sources), data quality rule inventory (estimate 5K), governance glossary assembly, dimensional modeling workshops | Weeks 1–3 | Discovery Summary Report, Source Inventory Spreadsheet, DQ Rule Priorities (P0/P1/P2) |
| **DW Design** | Dimensional star-schema design, physical schema (tables, columns, keys), indexing strategy, partitioning approach | Weeks 2–4 | Data Warehouse Design Document, ERDs, Data Dictionary |
| **Technical Blueprints** | CDI approach per POD 1, CDQ approach per POD 1, MDM match/survivorship per POD 2, CDGC catalog & lineage per POD 3 | Weeks 3–5 | Technical Architecture Document (4 modules), proof-of-concept demo (sample mapping) |
| **Infrastructure Setup** | VM provisioning (8 VMs total: 4 Prod, 2 Test, 2 Dev), OS installation, Secure Agent installation, firewall whitelisting, optional VPN tunnel provisioning | Weeks 1–8 | Infrastructure As-Built Document, Network Topology Diagram, Agent Health Checklist |
| **Governance & Access** | Service account creation (SQL Server, SharePoint, APIs, file shares), IDMC tenant access roles defined, network security review, monitoring setup | Weeks 3–8 | Service Account Inventory, Access Control Matrix, Monitoring Dashboard |

#### Wave 0 Deliverables

| **Deliverable** | **Description** | **Acceptance By** |
|---|---|---|
| **Discovery Summary Report** | All 8+ sources documented: schemas, volumes, growth rates, known data issues, business rules, integration constraints | CNHI IT Director |
| **Data Warehouse Design Document** | Dimensional model (star schema), physical schema, data dictionary, ETL framework, index/partition strategy | CNHI BAs + Steering Committee |
| **DQ Rule Catalog** | 5,000 rules estimated, prioritized by wave (Wave 1: ~1K, Wave 2: ~2K, Wave 3: ~2K), with business context and validation logic | CNHI SMEs |
| **MDM Requirements Document** | Match criteria per domain, survivorship rules, stewardship workflows, sample match strategy | CNHI Data Stewards |
| **Technical Architecture Document** | Module-by-module design (CDI, CDQ, MDM, CDGC), agent group strategy, security posture, performance targets | CNHI Architecture Review Board |
| **Infrastructure As-Built** | VMs, agent groups, network topology, VPN config (if chosen), monitoring setup; agents ✅ operational and connected | CNHI IT & Security |
| **Source Priority Confirmation** | Final wave assignments per source (Wave 1 fixed: IBM + Files; Waves 2–3 flexible per CNHI business needs) | CNHI Executive Sponsor |

#### Wave 0 Exit Criteria

- ✅ All 8 Secure Agents operational and heartbeat confirmed with IDMC
- ✅ VPN tunnel stable (if chosen) with latency < 50 ms
- ✅ SQL Server DW database created with base schema
- ✅ All 4 IDMC module blueprints approved
- ✅ Source priorities finalized (IBM + Files in Wave 1, others re-orderable in Waves 2–3)
- ✅ DQ rule count finalized and prioritized (actual vs. 5K estimate confirmed)
- ✅ All POD teams mobilized and ready to sprint

### 4.4 WAVE 1: Automate Manual ETL — IBM & Files (Weeks 11–23)

**Objective:** Deliver first production value by automating CNHI's most painful manual ETL workloads (IBM mainframe and file-based loads).

**🚀 Production Go-Live: Week 23**

#### Scope

| **Component** | **What** | **Business Value** |
|---|---|---|
| **IBM Sources** | IBM DB2/AS/400 via Cloud Pak for Integration; ~2–3 TB historical | **Eliminate mainframe manual extracts** |
| **File Sources** | CSV, JSON, Parquet, DB backups from SFTP/shared folders; ~1–2 TB historical | **Automate file processing** |
| **SQL Server** | Existing data mart; supporting source | Integrated into DW |
| **DQ Rules** | 1,000 P0 rules (highest priority: identity, mandatory fields, type/range checks) | Data quality at source |
| **Catalog** | 200 tables cataloged with basic lineage | Data discovery enabled |

#### Timeline (13 weeks)

| **Weeks** | **POD 1 (CDI+CDQ)** | **POD 2 (MDM)** | **POD 3 (CDGC)** |
|---|---|---|---|
| 11–14 | CP4I connectivity, 5 IBM mappings, 500 DQ rules, SQL testing | MDM requirements workshops | Catalog IBM, File sources |
| 15–18 | File automation, 10 file mappings, 500 DQ rules, SQL integration | MDM requirements workshops | Catalog SQL Server |
| 19–20 | Hardening, testing all pipelines, error handling | — | Lineage validation |
| 21–22 | **Mini-UAT (2 weeks):** CNHI UAT team executes test cases | — | UAT support |
| 23 | **PRODUCTION GO-LIVE** | — | Catalog live, lineage operational |

**Bi-weekly Sprint Demos:** Weeks 12, 14, 16, 18, 20 to CNHI stakeholders

#### Wave 1 Deliverables

| **Deliverable** | **Acceptance Criteria** |
|---|---|
| **15–20 ETL Mappings** | IBM, Files, SQL Server → DW; tested; documented; scheduled |
| **4–5 TB Historical Data Loaded** | Reconciliation report shows 100% match |
| **1,000 DQ Rules Live** | Pass rate ≥90% on Wave 1 data; violations tracked in detail |
| **200 Tables Cataloged** | Searchable in IDMC catalog; business users can discover assets |
| **Production Go-Live Report** | First nightly batch successful; SLAs monitored |
| **UAT Sign-Off** | CNHI business users formally accept Wave 1 solution |

#### Wave 1 Exit Criteria

- ✅ 15–20 mappings operational and scheduled nightly
- ✅ 4–5 TB historical data loaded (100% reconciliation)
- ✅ 1,000 DQ rules live (≥90% pass rate)
- ✅ 200 tables cataloged with lineage
- ✅ UAT sign-off received from CNHI
- ✅ **PRODUCTION GO-LIVE: Week 23** ← **First Business Value Delivered**

### 4.5 WAVE 2: Core Databases (Weeks 24–33)

**Objective:** Add PostgreSQL and Oracle; expand DQ rules; begin MDM hands-on development.

**🚀 Production Go-Live: Week 33** | **Cumulative: 70% Data Coverage**

#### Scope

| **Component** | **What** | **Business Value** |
|---|---|---|
| **CDI — Databases** | PostgreSQL, Oracle → DW; ~2–3 TB historical | Expand data integration coverage |
| **CDQ — Expanded Rules** | 2,000 P1 rules (business semantics: standardization, formatting, cross-field checks) | Broader quality coverage |
| **CDGC — Expanded Catalog** | 150 additional tables (350 total); extended lineage | Enhanced data discovery |
| **MDM — Sample Load** | 5M beneficiary records sample; match tuning; algorithm validation | MDM foundation (parallel with POD 1) |

#### Timeline (10 weeks)

| **Weeks** | **POD 1 (CDI+CDQ)** | **POD 2 (MDM)** | **POD 3 (CDGC)** |
|---|---|---|---|
| 24–27 | PostgreSQL, Oracle design; 10 mappings started | 5M sample load initiated; match rules tuned | Catalog additional sources |
| 28–30 | 2,000 DQ rules implemented; testing | Match threshold tuning; precision/recall validation | Lineage expansion |
| 31 | Error handling hardening | — | UAT preparation |
| 32–33 | **Mini-UAT (2 weeks)** | — | UAT support |
| 33 | **PRODUCTION GO-LIVE** | Sample load validated | Catalog live |

#### Wave 2 Deliverables

| **Deliverable** | **Acceptance Criteria** |
|---|---|
| **20 Additional Mappings** | PostgreSQL, Oracle → DW (35 total mappings) |
| **2–3 TB Additional Data** | Reconciliation 100% |
| **2,000 Additional DQ Rules** | Pass rate ≥92% (3,000 total rules) |
| **350 Total Tables Cataloged** | Business users utilizing catalog for discovery |
| **5M MDM Sample Load** | Match algorithm validated; coverage ≥95% |
| **UAT Sign-Off** | CNHI accepts Wave 2 |

#### Wave 2 Exit Criteria

- ✅ 35 total mappings operational
- ✅ 6–8 TB total data loaded
- ✅ 3,000 total DQ rules (≥92% pass rate)
- ✅ 350 tables cataloged
- ✅ 5M MDM sample successful (match coverage ≥95%)
- ✅ **PRODUCTION GO-LIVE: Week 33**

### 4.6 WAVE 3: Cloud & External Sources (Weeks 34–41)

**Objective:** Complete all CDI/CDQ/CDGC modules; execute full-scale MDM load.

**🚀 Production Go-Live: Week 41** | **Cumulative: 100% CDI/CDQ/CDGC**

#### Scope

| **Component** | **What** | **Business Value** |
|---|---|---|
| **CDI — Cloud/External** | SharePoint, APIs, additional sources; ~2–3 TB | Complete data integration |
| **CDQ — Complete Rules** | 2,000 P2 rules (cross-record, referential, extended checks); 5,000 total | Full quality coverage |
| **CDGC — Complete Catalog** | 150 additional tables (500 total); full end-to-end lineage | Complete governance |
| **MDM — Full Load** | 35M beneficiary + 25K provider full load; golden record creation | Complete MDM operational |

#### Timeline (8 weeks)

| **Weeks** | **POD 1 (CDI+CDQ)** | **POD 2 (MDM)** | **POD 3 (CDGC)** |
|---|---|---|---|
| 34–36 | SharePoint OAuth; API connectors; 15 final mappings | Full 35M load initiated | Catalog completion |
| 37–39 | 2,000 final DQ rules; extended checks | Golden record tuning; stewardship workflow testing | Lineage finalization |
| 40 | Hardening and testing | — | Final validation |
| 41 | **PRODUCTION GO-LIVE** | Full load completed, ready for UAT | Catalog live |

#### Wave 3 Deliverables

| **Deliverable** | **Acceptance Criteria** |
|---|---|
| **15 Final Mappings** | All 50+ mappings operational |
| **10 TB Total Historical Data** | Complete data loaded and reconciled |
| **5,000 Total DQ Rules** | Pass rate ≥95% overall |
| **500 Total Tables Cataloged** | Complete catalog |
| **Complete Lineage** | End-to-end lineage visible for compliance/impact analysis |
| **35M+ Golden Records (MDM)** | Ready for production UAT |
| **UAT Sign-Off (CDI+CDQ+CDGC)** | CNHI accepts Wave 3 |

#### Wave 3 Exit Criteria

- ✅ All 50+ mappings operational
- ✅ All 10 TB data loaded
- ✅ All 5,000 DQ rules live (≥95% pass rate)
- ✅ All 500 tables cataloged
- ✅ Complete lineage documented
- ✅ 35M+ golden records created
- ✅ **PRODUCTION GO-LIVE: Week 41**

### 4.7 WAVE 4: MDM Production Deployment (Weeks 42–45)

**Objective:** Cutover from sample to full operational MDM.

**🚀 MDM Production Go-Live: Week 45**

#### Timeline (4 weeks)

| **Week** | **Activity** | **Owner** |
|---|---|---|
| 42 | Golden record validation with CNHI SMEs; workflow testing; steward training begins | POD 2 + CNHI stewards |
| 43–44 | **MDM UAT (2 weeks):** Stewards test conflict resolution, workflow, approval processes | POD 2 + CNHI stewards |
| 45 | **MDM Production Go-Live:** Golden records operational; stewardship live | POD 2 |

#### Wave 4 Deliverables

| **Deliverable** | **Acceptance Criteria** |
|---|---|
| **35M+ Beneficiary Golden Records** | ≥98% match coverage; production-ready |
| **25K+ Provider Golden Records** | ≥98% match coverage; production-ready |
| **MDM Hub Operational** | Stewardship workflows live |
| **Stewards Trained** | Stewards can resolve conflicts independently |
| **UAT Sign-Off (MDM)** | CNHI stewards accept MDM solution |

#### Wave 4 Exit Criteria

- ✅ 35M+ beneficiary records (≥98% coverage)
- ✅ 25K+ provider records (≥98% coverage)
- ✅ MDM Hub operational
- ✅ Stewards trained
- ✅ **MDM PRODUCTION GO-LIVE: Week 45**

### 4.8 WAVE 5: Final Integration & Handover (Weeks 46–48)

**Objective:** End-to-end testing, optimization, operational readiness, project closure.

**✅ Complete Solution Operational: Week 48**

#### Timeline (3 weeks)

| **Week** | **Activity** | **Owner** |
|---|---|---|
| 46 | End-to-end regression tests; performance tuning; admin training | All PODs |
| 47 | User training finalized; runbooks reviewed; final optimization | All PODs |
| 48 | Hypercare kickoff; operations handover; project closure | Sutherland + CNHI |

#### Wave 5 Deliverables

| **Deliverable** | **Acceptance Criteria** |
|---|---|
| **Regression Test Report** | All end-to-end tests passed |
| **Performance Report** | Batch window ≤3 hours; SLAs met |
| **Runbooks** | CNHI operations can run platform independently |
| **Training Records** | Admin + user training completed; sign-offs received |
| **Hypercare Log** | No critical open issues; lessons learned documented |
| **Project Closure Report** | Steering committee formal approval |

#### Wave 5 Exit Criteria

- ✅ End-to-end regression complete
- ✅ Performance validated (batch window ≤3 hours)
- ✅ CNHI operations team certified
- ✅ 3-week hypercare complete
- ✅ **PROJECT COMPLETE: Week 48**

---

## 5. TEAM STRUCTURE & POD ORGANIZATION

### 5.1 Delivery Organization Overview

**Sutherland commits a dedicated core team of 12–13 specialists,** organized into three parallel PODs with shared leadership services.

```
┌─────────────────────────────────────────────────────────┐
│     SUTHERLAND DELIVERY LEADERSHIP (Shared)             │
├─────────────────────────────────────────────────────────┤
│ • Solution Architect (1) — overall design, non-functional requirements |
│ • Project Coordinator (1) — sprint planning, risk/dependency tracking |
│ • Infrastructure Engineer (1) — VMs, agents, connectivity, monitoring |
│ • Technical Writer (1) — runbooks, training, documentation |
└─────────────────────────────────────────────────────────┘
                            │
         ┌──────────────────┼──────────────────┐
         │                  │                  │
    ┌────▼─────┐       ┌────▼─────┐       ┌────▼─────┐
    │  POD 1   │       │  POD 2   │       │  POD 3   │
    │ CDI+CDQ  │       │   MDM    │       │  CDGC    │
    └──────────┘       └──────────┘       └──────────┘
    (8–9 people)       (4–5 people)       (2–3 people)
```

### 5.2 POD 1: Data Integration & Quality (CDI+CDQ) — 8–9 Resources

**Charter:** Design and build all ETL pipelines, data quality rules, and operational frameworks.

| **Role** | **FTE** | **Responsibilities** |
|---|---|---|
| **CDI/CDQ Technical Lead** | 1.0 | Designs integration patterns; reviews code; mentors developers; owns performance tuning |
| **Integration Developers** | 3.0 | Build and maintain mappings; design error handling; implement CDC frameworks |
| **Data Quality Specialists** | 2.0 | Translate business rules into IDMC tasks; design scorecards; build remediation workflows |
| **Catalog Specialist** | 1.0 | (Shared with POD 3) Captures metadata from CDI pipelines; maintains lineage |
| **QA Engineer** | 1.0 | Functional test coverage; UAT coordination; error handling validation |

**Engagement Duration:** Weeks 1–48 (full program)

**Peak Workload:** Waves 1–3 (active development); Wave 4 (support); Wave 5 (regression/optimization)

### 5.3 POD 2: Master Data Management (MDM) — 4–5 Resources

**Charter:** Design and implement match rules, survivorship logic, and stewardship workflows.

| **Role** | **FTE** | **Responsibilities** |
|---|---|---|
| **MDM Technical Lead** | 1.0 | Designs match algorithms; configures survivorship rules; performance tunes; owns hub operations |
| **MDM Specialists** | 2.0 | Configure match algorithms; tune thresholds; design golden record structures; validate sample loads |
| **QA Engineer** | 1.0 | Validates match coverage; tests stewardship workflows; UAT coordination |

**Engagement Duration:** Weeks 1–10 (planning), Weeks 24–48 (active development + go-live)

**Peak Workload:** Waves 2–4 (sample tuning → full load → production deployment)

### 5.4 POD 3: Governance & Catalog (CDGC) — 2–3 Resources

**Charter:** Manage cataloging, metadata harvesting, lineage, and governance workflows.

| **Role** | **FTE** | **Responsibilities** |
|---|---|---|
| **Catalog & Governance Lead** | 1.0 | Designs catalog strategy; schedules scanners; owns lineage; maintains governance policies |
| **Catalog/Metadata Specialist** | 1.0 | (Shared with POD 1) Harvests metadata; maps glossary terms; validates lineage |

**Engagement Duration:** Weeks 1–48 (continuous)

**Peak Workload:** Waves 1–3 (catalog expansion); Waves 4–5 (optimization)

### 5.5 Shared Leadership Roles

| **Role** | **FTE** | **Responsibilities** |
|---|---|---|
| **Solution Architect** | 1.0 | Oversees non-functional requirements (security, availability, performance); reviews key designs; resolves architecture questions; escalation point |
| **Project Coordinator** | 1.0 | Sprint planning; status reporting; dependency tracking; risk management; steering committee coordination |
| **Infrastructure Engineer** | 1.0 | VM provisioning, OS hardening, agent installation, network troubleshooting, monitoring setup |
| **Technical Writer** | 1.0 | Runbooks, configuration guides, training materials, lessons learned documentation |

### 5.6 Ways of Working

| **Cadence** | **Activity** | **Participants** |
|---|---|---|
| **Weekly** | Cross-POD sync (1 hour) | All POD leads + shared leadership |
| **Bi-Weekly** | Sprint demos (1.5 hours) | All Sutherland + CNHI stakeholders |
| **Bi-Weekly** | Steering committee (1 hour) | Leadership + CNHI executive sponsor |
| **Weekly** | Dependency tracking review | Project coordinator + POD leads |
| **Per-Demand** | Architecture reviews | Solution architect + relevant POD |

### 5.7 CNHI Team Expectations

| **CNHI Role** | **Time Commitment** | **Key Responsibilities** |
|---|---|---|
| **Executive Sponsor** | 2–3 hrs/week | Prioritize decisions; remove roadblocks |
| **IT Director** | 3–5 hrs/week | Infrastructure provisioning; security approvals |
| **Business SMEs** | 5–10 hrs/week | Define DQ rules; validate mappings; prioritize sources |
| **Data Stewards** | 5–10 hrs/week (Wave 0–2), 15–20 hrs/week (Wave 3–4) | Own DQ remediation; validate MDM golden records; run stewardship workflows |
| **DBAs** | 3–5 hrs/week | DW design review; performance tuning; index maintenance |
| **Network & Security** | 5–10 hrs/week (Wave 0) | VPN provisioning; firewall rules; security validation |
| **UAT Teams** | 10–20 hrs/week (per wave) | Execute test cases; sign-off on deliverables |

---

## 6. TIMELINE & MILESTONES

### 6.1 Wave Execution Timeline

```
Week    1         10        20        30        40        48
        │         │         │         │         │         │
Wave 0: ├─────────┤ (Foundation)
        │
Wave 1: │         ├─────────────────────┤ (IBM + Files → Prod Week 23)
        │
Wave 2: │         │                     ├──────────────────┤ (DBs → Prod Week 33)
        │
Wave 3: │         │                     │                  ├────────┤ (Cloud → Prod Week 41)
        │
Wave 4: │         │                     │                  │        ├──┤ (MDM → Prod Week 45)
        │
Wave 5: │         │                     │                  │        │  ├─┤ (Handover → Week 48)
        │
POD 1:  ├─────────────────────────────────────────────────────────────┤ (CDI+CDQ continuous)
        │
POD 2:  ├─────────┤      ├──────────────────────────────────────────┤ (MDM Waves 2–5)
        │
POD 3:  ├───────────────────────────────────────────────────────────┤ (CDGC continuous)
```

### 6.2 Major Milestones

| **Milestone** | **Week** | **Gating Items** |
|---|---|---|
| **Contract Signature** | 0 | Project kickoff authorization |
| **Infrastructure Operational** | 10 | All agents, VPN/firewall, DW schema, service accounts |
| **Wave 1 Go-Live** | 23 | 15–20 mappings, 1K rules, 200 catalog entries, UAT sign-off |
| **Wave 2 Go-Live** | 33 | 20 additional mappings, 2K rules, 5M MDM sample validated |
| **Wave 3 Go-Live** | 41 | 15 final mappings, 2K final rules, 35M golden records, full lineage |
| **Wave 4 Go-Live (MDM)** | 45 | MDM UAT complete, steward training, production cutover |
| **Project Complete** | 48 | Regression tests passed, hypercare started, project closure |

### 6.3 Production Go-Live Summary

| **Go-Live #** | **Week** | **Module(s)** | **Business Impact** |
|---|---|---|---|
| **#1: Wave 1** | 23 | CDI (IBM, Files), CDQ (1K rules), CDGC (200 tables) | Manual ETL fully automated; data quality visible |
| **#2: Wave 2** | 33 | CDI (Databases), CDQ (expanded), CDGC (350 tables) | 70% data coverage; MDM foundation validated |
| **#3: Wave 3** | 41 | CDI (Cloud), CDQ (complete 5K), CDGC (500 tables, lineage) | 100% data integration; full governance |
| **#4: Wave 4** | 45 | MDM | Golden records operational; stewardship live |

---

## 7. CNHI DEPENDENCIES & CRITICAL INPUTS

### 7.1 Wave 0 Dependencies (Critical Foundation)

**If not met by end of Week 10, Wave 1 will slip proportionally.**

| **Dependency** | **Owner** | **Delivery By** | **Impact of Delay** |
|---|---|---|---|
| **VM Provisioning** | CNHI IT Infrastructure | Week 5 | Agent installation delayed; critical path |
| **OS Image & Patching** | CNHI IT Infrastructure | Week 6 | Agent installation delayed |
| **Firewall Rules** | CNHI Security/Network | Week 7 | Agent connectivity delayed |
| **Service Accounts** (SQL Server, SharePoint, file shares) | CNHI IT Identity | Week 6 | Mapping testing delayed; Wave 1 slip |
| **VPN Tunnel Setup** (if chosen) | CNHI Network + Informatica | Week 8 | Connectivity validation delayed; performance tuning affected |
| **SQL Server DW Provisioning** | CNHI IT Infrastructure | Week 7 | DW design review and testing delayed |
| **Source System Access** (IBM, databases, file shares) | CNHI Data Stewards/IT | Week 6 | Data discovery and profiling delayed |
| **Data Quality Rule Inventory** | CNHI SMEs | Week 4 | Prioritization and planning delayed; estimated 5K rules |
| **DW Design Sign-Off** | CNHI Architecture | Week 5 | Build phase cannot start cleanly |
| **Source Priority Confirmation** | CNHI Executive Sponsor | Week 10 | Sprint planning for Wave 1 delayed |

### 7.2 POD 1 Dependencies (CDI+CDQ) — Waves 1–3

| **Dependency** | **Owner** | **Wave(s)** | **Impact of Delay** |
|---|---|---|---|
| **Source System Credentials** (SQL Server logins, JDBC passwords, API tokens) | CNHI IT/Application Owners | All waves | Mapping tests blocked |
| **Data Quality Rule Specifications** (exact validation logic, priority, business context) | CNHI SMEs/Data Stewards | Wave 1 (Week 11), Wave 2 (Week 24), Wave 3 (Week 34) | DQ implementation delayed; reduced pass-rate targets |
| **DW Schema Approval** (star-schema design, table/column naming) | CNHI DBAs | Week 6–7 (before Wave 1 build) | Mapping design delayed; Wave 1 slip |
| **Historical Data Availability** (10 TB export from sources) | CNHI IT/Data Stewards | Wave 1 (Week 11) | Historical load testing delayed |
| **Mini-UAT Participation** (2 weeks per wave) | CNHI UAT Team | Weeks 21–22 (Wave 1), Weeks 32–33 (Wave 2), Weeks 40–41 (Wave 3) | Sign-off delayed; go-live date at risk |

### 7.3 POD 2 Dependencies (MDM) — Waves 2–4

| **Dependency** | **Owner** | **Wave(s)** | **Impact of Delay** |
|---|---|---|---|
| **MDM Requirements Workshop** (match criteria, survivorship rules, stewardship workflows) | CNHI Data Stewards + SMEs | Wave 0–1 (Weeks 1–23) | MDM design delayed; Wave 2 slip |
| **Sample Data Set** (5M beneficiary records, representative providers) | CNHI IT/Data Stewards | Wave 2 (Week 24) | MDM tuning delayed; thresholds not validated |
| **Steward Team Availability** (review/approve match results, resolve conflicts) | CNHI Data Stewards | Wave 2–3 (Weeks 24–41), Wave 4 (Weeks 42–45) | Golden record tuning blocked; go-live delayed |
| **MDM Stewardship Training** | Sutherland | Wave 4 (Weeks 42–45) | Workflow adoption delayed |

### 7.4 POD 3 Dependencies (CDGC) — Waves 1–5

| **Dependency** | **Owner** | **Wave(s)** | **Impact of Delay** |
|---|---|---|---|
| **Business Glossary** (domain terms, definitions, mappings to physical assets) | CNHI Data Stewards/Domain Leads | Wave 1 (Week 11) | Catalog search/discovery limited; governance not actionable |
| **Metadata Permissions & Access Model** (who sees what in catalog) | CNHI IT Security | Wave 0 (Week 8) | Catalog cannot be deployed; access controls missing |
| **Lineage Acceptance Criteria** (what constitutes "complete" end-to-end lineage) | CNHI Governance Lead | Wave 0 (Week 5) | Lineage validation subjective; sign-off delays |
| **Data Classification Rules** (PII, confidential, retention) | CNHI Security/Compliance | Wave 1 (Week 12) | Masking policies incomplete; non-prod testing restricted |

### 7.5 Wave 5 Dependencies (Final Integration)

| **Dependency** | **Owner** | **Due** | **Impact of Delay** |
|---|---|---|---|
| **UAT Environment Sign-Off** (all Waves 1–4 passed testing) | CNHI UAT Lead | Week 45 | Regression testing cannot start |
| **Operator Training Completion** | CNHI IT Operations | Week 47 | Hypercare will lack trained responders |
| **Change Management Approvals** (CNHI change advisory board) | CNHI Change Manager | Weeks 46–48 | Production cutover delayed; hypercare window shortened |

### 7.6 CNHI Team Requirements Summary

| **Role / Team** | **Effort** | **Timing** | **Deliverables / Responsibilities** |
|---|---|---|---|
| **Executive Sponsor** | 2–3 hrs/week | Weeks 0–48 | Decision-making authority; escalation; prioritization |
| **IT Director** | 3–5 hrs/week | Weeks 0–10 (Wave 0 peak); ongoing | Infrastructure procurement; security approvals; firewall rules |
| **Business SMEs** | 5–10 hrs/week | Waves 0–3 (peak Waves 1–2) | DQ rule definitions; business logic validation; UAT |
| **Data Stewards** | 5–10 hrs/week (Waves 0–2), 15–20 hrs/week (Waves 3–5) | Waves 0–5 | DQ remediation; MDM validation; golden record approval |
| **DBAs** | 3–5 hrs/week | Waves 0, 5 (peak); ongoing | DW design; performance tuning; index strategy |
| **Network/Security** | 5–10 hrs/week | Wave 0 (peak); ongoing | VPN tunnel; firewall rules; credential vaulting |
| **UAT Teams** | 10–20 hrs/week per wave | Waves 1–4 (2 weeks per wave) | Test case execution; sign-off; defect triage |

---

## 8. SUCCESS CRITERIA & ACCEPTANCE

### 8.1 Technical Success Metrics

| **Metric** | **Target** | **Wave Achievement** | **Measurement** | **Notes** |
|---|---|---|---|---|
| **Batch Window** | ≤3 hours | Validated by Wave 5 | Job execution duration from start to DW load completion | Subject to source availability and network latency |
| **DQ Pass Rate** | 90% → 95% | Wave 1: ≥90%, Wave 2: ≥92%, Wave 3: ≥95% | % of records passing all applicable rules per wave | Targets are design objectives; actual rates depend on upstream remediation |
| **MDM Match Coverage** | ≥98% | Wave 2: 5M sample validated; Wave 3: 35M+ full load | % of input records successfully matched or identified as new | "Match coverage" = operational metric; precision/recall tuned during Waves 2–3 |
| **Agent Availability** | 99.5% | Operational SLA (active-active HA) | Uptime during nightly batch windows | Excludes CNHI-side network/source outages |
| **Lineage Completeness** | 100% source → DW | Wave 3 | End-to-end lineage for all 50+ mappings | Verified via manual audit + lineage reports |

### 8.2 Business Success Criteria

| **Outcome** | **Wave Enabled** | **Success Definition** |
|---|---|---|
| **Manual ETL Elimination** | Wave 1 | IBM and file-based extracts fully automated; zero manual intervention required nightly |
| **Data Quality Visibility** | Wave 1 | Stewards can see DQ violations in real-time; remediation workflows active |
| **Master Data Readiness** | Wave 4 | Golden records in use by downstream systems; single-view-of-customer operational |
| **Governance & Compliance** | Wave 3 | Catalog searchable; lineage auditable; PDPL compliance demonstrable |
| **Operational Self-Sufficiency** | Wave 5 | CNHI operations team can run, monitor, and troubleshoot platform independently |

### 8.3 Wave-Specific Acceptance Criteria

#### **Wave 0 Exit**
- ✅ All 8 Secure Agents operational and connected to IDMC
- ✅ VPN tunnel (if chosen) stable with latency < 50 ms
- ✅ SQL Server DW database created with approved schema
- ✅ All 4 IDMC module blueprints signed off
- ✅ Source priorities finalized
- ✅ DQ rule count confirmed (5K estimate vs. actual)
- ✅ All PODs ready to sprint

#### **Wave 1 Exit**
- ✅ 15–20 ETL mappings operational and scheduled
- ✅ 4–5 TB historical data loaded (100% reconciliation)
- ✅ 1,000 DQ rules live (≥90% pass rate)
- ✅ 200 tables cataloged
- ✅ **PRODUCTION GO-LIVE: Week 23**
- ✅ UAT sign-off received

#### **Wave 2 Exit**
- ✅ 35 total mappings operational
- ✅ 6–8 TB total data loaded
- ✅ 3,000 total DQ rules (≥92% pass rate)
- ✅ 350 tables cataloged
- ✅ 5M MDM sample successful
- ✅ **PRODUCTION GO-LIVE: Week 33**

#### **Wave 3 Exit**
- ✅ All 50+ mappings operational
- ✅ 10 TB total data loaded
- ✅ 5,000 total DQ rules (≥95% pass rate)
- ✅ 500 tables cataloged
- ✅ 35M+ golden records created
- ✅ Complete end-to-end lineage
- ✅ **PRODUCTION GO-LIVE: Week 41**

#### **Wave 4 Exit**
- ✅ 35M+ beneficiary golden records operational
- ✅ 25K+ provider golden records operational
- ✅ MDM Hub live with stewardship workflows
- ✅ Stewards trained and confident
- ✅ **PRODUCTION GO-LIVE: Week 45**

#### **Wave 5 Exit**
- ✅ End-to-end regression testing complete
- ✅ Performance validated (batch ≤3 hours)
- ✅ CNHI operations team certified
- ✅ Hypercare (3 weeks) initiated
- ✅ **PROJECT COMPLETE: Week 48**

### 8.4 Deliverable Acceptance Process

| **Phase** | **Process** | **Timeline** |
|---|---|---|
| **Plan & Design** | Design documents reviewed and approved by CNHI architecture team | 1 week per document |
| **Build & Test** | Bi-weekly demos; feedback incorporated into next sprint | Per sprint (2 weeks) |
| **UAT** | Mini-UAT (2 weeks per wave) with CNHI business users | Per wave |
| **Sign-Off** | Formal written acceptance signed by CNHI sponsor or designee | Before go-live |
| **Hypercare** | 3-week post-go-live support; issue triage and resolution | Weeks 46–48 |

---

## 9. ASSUMPTIONS & RISKS

### 9.1 Key Assumptions

| **Assumption** | **Rationale** | **Mitigation** |
|---|---|---|
| **Informatica Windows Server 2022 Support Confirmed** | CNHI prefers Windows for ops alignment; Informatica may recommend Linux | Wave 0 dependency: written confirmation from Informatica before agent provisioning |
| **Source System Access Available** | Integration requires credentials and connectivity to IBM, SQL Server, SharePoint, APIs, etc. | Wave 0 discovery maps all access constraints; Wave 1 onboarding sequence sources with confirmed access |
| **CNHI SME Availability** | 5–20 hrs/week ongoing participation required | Executive sponsor ensures team commitment; steering committee escalates conflicts |
| **Data Quality Rules Estimate (5,000)** | Indicative; actual scope confirmed post-discovery | Wave 0 finalizes rule count; success measured by domain coverage, not rigid count |
| **VPN Tunnel Available** | IPSec option assumes CNHI network can provision tunnel by Week 8 | Fallback: internet egress via port 443 if VPN delayed; performance may vary |
| **SQL Server DW Performance** | DW tuning (indexes, partitions) assumes CNHI allows Sutherland recommendations | Wave 5 performance tuning; CNHI DBA executes recommendations |
| **Secure Agent Capacity** | Initial 2-agent sizing sufficient for Wave 1–2; scaling available for Wave 3+ | Wave 0 capacity planning; elastic scaling model in Wave 5 |

### 9.2 Risks & Mitigation

| **Risk** | **Probability** | **Impact** | **Mitigation** |
|---|---|---|---|
| **VM Provisioning Delay** | Medium | High (critical path) | Weekly dependency tracking; alternate resources available if needed |
| **Source System Credential Challenges** | Medium | High (blocks mapping tests) | Wave 0 discovery identifies access constraints; phased onboarding prioritizes available sources |
| **DQ Rule Scope Explosion** (actual > 5K) | Medium | Medium (Wave 1 slip) | Wave 0 rule prioritization limits Wave 1 to ~1K; later waves handle excess |
| **MDM Sample Load Performance** (slower than expected) | Low | Medium (Wave 2 slip) | Week 24 proof-of-concept; tuning adjustments before full load |
| **Network Latency Issues** | Low | Medium (SLA impact) | VPN tunnel provides deterministic path; internet fallback available |
| **Steward Availability for MDM** (overcommitted) | Medium | High (golden record delay) | Executive sponsor ensures team commitment; cross-training backup stewards |
| **Informatica Module Feature Loss on Windows** | Low | High (platform switch cost) | Wave 0 written confirmation; contingency Linux deployment plan |

---

## 10. ENGAGEMENT TERMS

### 10.1 Service Scope & Duration

- **Duration:** 48 weeks from contract signature through project closure
- **Sutherland Team:** 12–13 FTE specialists (variable per wave; peak Waves 1–3)
- **Engagement Model:** Fixed-scope, wave-based delivery with time-box per milestone
- **Change Control:** Scope changes managed via change request process; documented impact on timeline/budget

### 10.2 Warranty & Support

- **Wave 1–4 Warranty:** 30 days post-go-live defect rectification at no additional cost
- **Hypercare:** 3 weeks post-Wave-5 go-live (Week 46–48) on-call support (2 hrs/day response time)
- **Post-Hypercare SLA:** Optional AMS engagement available (separate statement of work)

### 10.3 Licensing & Informatica Subscriptions

- **IDMC Licenses & IPUs:** CNHI responsibility; Sutherland validates sizing against approved scope
- **IPU Adjustment:** If scope changes materially (additional sources, rules, data volume), IPU impact will be assessed; cost borne by CNHI
- **License Key Management:** CNHI provides; Sutherland configures

### 10.4 Knowledge Transfer & Training

| **Training Track** | **Audience** | **Duration** | **Timing** |
|---|---|---|---|
| **Infrastructure & Operations** | IT Operations, DBAs | 3 days | Wave 5 (Weeks 46–47) |
| **Data Integration & Pipelines** | Developers, data engineers | 3 days | Wave 1 (post-go-live) + Wave 5 refresher |
| **Data Quality** | Stewards, SMEs | 2 days | Wave 1 (post-go-live) + Wave 5 |
| **Master Data Management** | Stewards | 2 days | Wave 4 (pre-go-live) + Wave 5 |
| **Governance & Catalog** | Business users, stewards | 1 day | Wave 3 (post-go-live) |

### 10.5 Deliverables Ownership

| **Deliverable** | **Ownership Post-Project** |
|---|---|
| **IDMC Mappings & Configurations** | CNHI (Sutherland provides runbooks for maintenance) |
| **Data Warehouse Schema & Indexes** | CNHI DBAs (Sutherland provides tuning recommendations) |
| **Runbooks & Documentation** | CNHI IT Operations |
| **Source Code (if custom)** | CNHI (Sutherland retains IP for reusable components) |
| **Lineage & Governance Policies** | CNHI (Sutherland defines initial structure) |

### 10.6 Commercial Model (To Be Finalized Per RFP)

- **Payment by Wave:** Invoices upon milestone completion (Wave 0 Foundation → Wave 5 Closure)
- **Pricing:** [To be detailed in commercial proposal section]
- **Optional Post-Project AMS:** Separate SOW; includes monitoring, rule updates, new source onboarding, performance tuning

---

## 11. FUTURE-READY: AI/LLM & NEXT-GENERATION DATA PIPELINES

### Why This Matters

CNHI's enterprise data strategy extends beyond traditional BI into **AI-powered decision-making and generative AI applications**. Informatica IDMC, combined with Sutherland's implementation approach, creates the **governance and data quality foundation** that GenAI models depend on.

### How IDMC Enables AI/LLM Safety & Trust

| **AI Challenge** | **IDMC Solution** | **Benefit to CNHI** |
|---|---|---|
| **Data Lineage & Auditability** | Complete end-to-end lineage (source → transformation → model input) | Explainability: trace any model prediction back to its data sources |
| **Data Quality for Model Training** | 5,000+ DQ rules, pass-rate scorecards | Cleaner training data = more accurate models |
| **PII & Sensitive Data Protection** | Classification tags, masking policies, audit trails | Compliant with PDPL; reduces model hallucination risk from PII leakage |
| **Master Data Consistency** | Golden records (35M+ beneficiaries, 25K+ providers) | Stable, deduplicated input to ML models (no bias from duplicate records) |
| **Metadata & Feature Discovery** | Comprehensive catalog (500+ assets) with glossary mapping | Data scientists can rapidly identify features; reduce model development time |

### Roadmap Examples (Post-Wave-5)

**Example 1: Customer Analytics & Churn Prediction**
- Input: Golden beneficiary records (MDM) + transaction data (CDI) + quality-validated flags (CDQ)
- Model: Train on cleansed, deduplicated data → predict churn risk
- Transparency: IDMC lineage documents exactly which sources/transformations fed the model

**Example 2: Provider Network Optimization**
- Input: Golden provider records (MDM) + service utilization (CDI) + performance metrics (CDQ)
- Model: Identify underperforming or redundant providers
- Governance: Classification tags ensure only authorized teams access sensitive provider data

**Example 3: LLM Knowledge Repository Hygiene**
- Input: Structured data (beneficiary policies, regulations) + unstructured (documents) → vector store
- Pipeline: IDMC ensures source data is clean, lineage-tracked, masked where needed
- Governance: Audit trail of what data went into knowledge base (critical for RegTech compliance)

### Implementation Considerations (Post-Wave-5 Engagement)

| **Area** | **Who Owns** | **How IDMC Helps** |
|---|---|---|
| **Data Preparation for ML** | CNHI Data Science + Sutherland (optional AMS) | IDMC lineage & DQ provide clean inputs; reduce prep time |
| **LLM Prompt Engineering** | CNHI Data Science | Catalog + lineage visibility help identify features for few-shot examples |
| **Model Monitoring & Drift** | CNHI Operations + Data Science | IDMC metadata & DQ continue tracking source data quality post-model |
| **Compliance & Audit** | CNHI Compliance + Governance | IDMC lineage & classification tags simplify PDPL/audit responses |

---

## 12. REFERENCES & CREDENTIALS

### 12.1 Sutherland Expertise

**Informatica & Enterprise Data Integration:**
- 15+ years of data platform implementations across EMEA, Asia-Pacific, and Americas
- 50+ greenfield data warehouse and ETL modernization projects
- Certified Informatica implementation partners (CDI, CDQ, MDM, CDGC modules)
- Expertise in regulated industries: healthcare, financial services, government, telecommunications

**Data Governance & Compliance:**
- Experience implementing PDPL, GDPR, CCPA-aligned governance frameworks
- Catalog and lineage implementations supporting audit and compliance
- Master data management for identity resolution in regulated contexts

**Regional Presence:**
- Established operations in Middle East and North Africa (MENA)
- Local security clearance and compliance certifications
- Hybrid (onshore/offshore) delivery model with MENA-based support teams

### 12.2 Proposed Team Certifications

- **Solution Architect:** Informatica Certified Professional (CDI/CDQ/MDM), AWS or Azure Cloud Architect
- **POD Leads:** Informatica Certified Developers (module-specific)
- **All Team Members:** Relevant cloud and security certifications (e.g., AWS Security, ISO 27001)

### 12.3 Reference Case Studies (Anonymized)

**[Case Study 1: Healthcare Provider Integration]**
- Client: Large Middle Eastern healthcare network (~500 hospitals)
- Challenge: 20+ source systems; fragmented patient records; compliance with local data residency laws
- Solution: IDMC + Sutherland; greenfield master patient index (30M+ records); 100% on-premises execution
- Result: 15% reduction in duplicate encounters; improved care coordination; PDPL-ready governance

**[Case Study 2: Financial Services Master Data]**
- Client: Regional bank (KSA-based; confidential NDA)
- Challenge: Multiple acquired banks; duplicate customer records; legacy core systems
- Solution: IDMC MDM; survivorship rules; stewardship workflows
- Result: Single customer view; 40% faster new product deployment; 25% reduction in risk management effort

---

## 13. EVALUATION & SELECTION CRITERIA

### 13.1 How Sutherland Differentiates

| **Dimension** | **Sutherland's Approach** |
|---|---|
| **Delivery Speed & Early Value** | Parallel POD model delivers first production value Week 23 (not Week 52+); four incremental go-lives reduce risk |
| **Data Sovereignty & PDPL Compliance** | 100% on-premises execution; zero raw data moves to cloud; IDMC is orchestration only; transparent architecture |
| **Operational Readiness** | Hypercare + runbooks + training focus on CNHI self-sufficiency; not a "hand-off and abandon" approach |
| **AI/LLM Future-Readiness** | Governance, lineage, and data quality framework positions CNHI for safe, compliant GenAI pipelines |
| **Hybrid Delivery Model** | Combination of onshore expertise (Riyadh/KSA presence) and offshore scaling (India-based centers) maximizes efficiency and cost |
| **Fixed-Wave Commitment** | 48-week roadmap with gated, achievable milestones; reduced scope creep via sprint discipline |

### 13.2 Proposed Pricing Model (Illustrative)

**Structure:** Fixed-price, milestone-based payment per wave

| **Phase** | **Duration** | **Deliverables** | **Proposed Cost** |
|---|---|---|---|
| **Wave 0** | Weeks 1–10 | Foundation, discovery, DW design, infrastructure | [TBD] |
| **Wave 1** | Weeks 11–23 | CDI+CDQ, first production go-live | [TBD] |
| **Wave 2** | Weeks 24–33 | Core databases, MDM sample, second go-live | [TBD] |
| **Wave 3** | Weeks 34–41 | Cloud sources, complete CDGC, third go-live | [TBD] |
| **Wave 4** | Weeks 42–45 | MDM production deployment | [TBD] |
| **Wave 5 + Hypercare** | Weeks 46–48 | Regression, optimization, 3-week hypercare | [TBD] |
| **TOTAL (48 weeks)** | — | Full end-to-end implementation | [TBD] |

**Optional Post-Project:**
- **Managed Services (AMS):** 12-month support, monitoring, rule updates, new source onboarding — [TBD] per month

---

## APPENDIX: CRITICAL SUCCESS FACTORS

### For Sutherland
1. **Secure Wave 0 completion on time** — any delay cascades
2. **Maintain parallel POD momentum** — weekly syncs essential; dependencies tracked daily
3. **Demonstrate tangible Wave 1 value** — Week 23 go-live builds credibility for Waves 2–5
4. **Steward engagement during Waves 2–4** — golden record success depends on steward availability

### For CNHI
1. **Executive sponsor empowered to remove roadblocks** — VMs, firewall, credentials, approvals
2. **SME and steward time commitment** — cannot be ad-hoc; must be prioritized
3. **Data governance model clarification in Wave 0** — enables faster governance implementation
4. **Source system access confirmed early** — prevents mid-wave surprises

---

## CLOSING STATEMENT

This proposal outlines a pragmatic, risk-managed path to transforming CNHI's data capabilities. By combining **Informatica IDMC's cloud-based orchestration** with **on-premises Secure Agents** and **parallel POD delivery**, Sutherland will:

✅ **Deliver first production value in Week 23** (not 52+ weeks)  
✅ **Ensure 100% data residency** in Saudi Arabia (PDPL-compliant)  
✅ **Automate manual ETL**, establish data quality, and enable master data management  
✅ **Catalog and govern 500+ data assets** with complete lineage  
✅ **Build a foundation for safe, trustworthy AI/LLM pipelines**  
✅ **Hand over operational control to CNHI** by Week 48 with confidence

The roadmap is ambitious yet achievable, grounded in Sutherland's 15+ years of enterprise data platform expertise and commitment to CNHI's success.

---

**Document Version:** 1.0  
**Date:** January 2, 2026  
**Prepared by:** Sutherland Presales Analytics Solution Team  
**For:** CNHI Executive Leadership & RFP Evaluation Committee

