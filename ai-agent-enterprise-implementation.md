---
name: ai-agent-enterprise-implementation
version: 1.1
description: A complete 4-phase, 10-step enterprise methodology and teacher book for deploying AI Agents and custom Skills. Focuses on conservative financial governance, negative prompting against optimistic forecasts, segregation of duties, and converting legacy ERP/ISO manuals into active agent guardrails. v1.1 adds a fifth governance layer — "Vibe Coding Risk Containment" — which is modularized in the companion skill `vibe-coding-containment.md`. Use when guiding digital transformation, corporate management restructuring, or deploying AI agents in finance, operations, and cross-functional management.
---
> **Version note**: This is v1.1. The original v1 can be viewed in the
> [commit history](https://github.com/huangfred/ts2pc-ai-governance/commits/main/ai-agent-enterprise-implementation.md).
# Enterprise AI Agent Implementation Methodology (The Teacher Book)

## Core Philosophy & Absolute Red Lines

1. **Zero-Placebo Rule**: Strictly prohibit optimistic forecasting, vague encouragement, or placebo terminology. All agent outputs must be grounded in conservative, worst-case scenarios and hard historical data.
2. **From Paper SOP to Agent Constraints**: Do not let agents read passive 500-page manuals. Convert legacy corporate risks, past operational failures, and internal controls into active, negative-prompting markdown guardrails.
3. **Vibe Coding Containment Rule**: Never allow AI-generated code to touch the "Core Security Zone" (customer PII, employee credentials, payment flows, core financials). Non-technical teams may only use Vibe Coding inside a governed sandbox whose blast radius is architecturally capped. The platform's "one-click deploy" is not a security guarantee — the platform's ToS will always shift final liability back to you.

---

## The 4-Phase & 10-Step Execution Framework

### Phase 1: Codification & Red-Line Extraction (資產盤點與規章重構)

#### Step 1: Audit Historical Failures & Extract DNA
- **Action**: Audit historical corporate failures (e.g., budget overruns, compliance breaches, project delays over the past 3 years).
- **Teacher's Rule**: Implement "Negative Prompting". Define absolute red lines. If a proposed metric crosses safe financial thresholds, the agent must automatically halt and trigger a red-alert warning.

#### Step 2: Convert ISO/ERP Playbooks into Structured Markdown Skills
- **Action**: Transform legacy paper SOPs and ERP workflows into modular `.md` skill files.
- **Teacher's Rule**: Map each skill directly to the company's RACI matrix and authorization limits. Define exact accounting line-item sequences (e.g., Revenue -> COGS -> Gross Profit -> EBITDA -> Net Income) and mandatory validation logic.

---

### Phase 2: Role-Based Agent Assignment & Governance (角色分工與 Agent 賦能)

#### Step 3: Deploy Technical & Engineering Agents
- **Action**: Equip code and system agents (e.g., Devin, Cursor) with technical skill packages enforcing architectural, security, and performance guardrails.
- **Teacher's Rule**: Never allow technical agents to bypass security or compliance standards for the sake of speed.
- **Teacher's Rule (v1.1 addendum)**: When technical agents generate code via Vibe Coding tools, they operate under the containment rules defined in `vibe-coding-containment.md`. Speed is never a valid justification for bypassing the Chu-Han Boundary.

#### Step 4: Deploy Management & Operational Agents
- **Action**: Equip administrative, financial, and HR agents with business and governance skills (e.g., budget review, talent acquisition).
- **Teacher's Rule**: Ensure business agents strictly adopt the persona of a conservative CFO Advisor or Risk Officer, maintaining skepticism toward projected ROI.

#### Step 5: Enforce Segregation of Duties (SoD) & Human-in-the-Loop (HITL)
- **Action**: Establish permission boundaries and operational checkpoints.
- **Teacher's Rule**: Apply traditional ERP segregation of duties. Never allow the same agent to generate reports and audit compliance. In the first 3 months, enforce mandatory human-in-the-loop review for all high-stakes decisions.

---

### Phase 3: Structured Workflow & Closed-Loop Integration (實際業務流串聯與閉環)

#### Step 6: Standardize Inputs via Corporate Forms
- **Action**: Bind agent inputs to standard corporate forms (e.g., P&L templates, project charter sheets, budget request forms) rather than free-form chat.
- **Teacher's Rule**: Reject conversational chaos. Force users and agents to communicate through structured data fields to prevent information distortion.

#### Step 7: Execute Conservative Calculation & Risk Scanning
- **Action**: Trigger the relevant skill to evaluate data, check asset-liability balances, and scan for operational burn rates.
- **Teacher's Rule**: Force the agent to test assumptions against worst-case scenarios and calculate cash runways and cost-growth deltas.

#### Step 8: Deliver Structured, Non-Placebo Outputs
- **Action**: Require agents to output results in a strict three-part format.
- **Teacher's Rule**: Enforce the mandatory output template:
  1. **Core Comparative Data Table** (Actual vs. Budget with variance percentages).
  2. **CFO Risk & Cash Burn Warnings** (Bullet points outlining structural margin pressures).
  3. **Defensive Adjustments** (2-3 concrete, risk-mitigating recommendations).

---

### Phase 4: Post-Mortem Immunization & Governance (迭代優化與治理)

#### Step 9: Weekly Post-Mortem Patching via `skill-updater`
- **Action**: Review operational errors, budget miscalculations, or compliance oversights weekly.
- **Teacher's Rule**: When an error occurs, immediately update the corresponding `.md` skill file. This acts as an organizational immune system—the company learns once, and all AI agents permanently remember.

#### Step 10: Compliance & Accuracy Audits
- **Action**: Periodically audit agent output accuracy, rule adherence, and overall efficiency.
- **Teacher's Rule**: Treat AI agents with the same rigorous internal auditing standards applied to human administrative staff.
- **Teacher's Rule (v1.1 addendum)**: Audits must cover both *financial* accuracy and *security* posture. Include: RLS policy status, exposed API keys, authentication coverage, and whether any micro-innovation tool has crossed into PII territory.

---

### Phase 5: Vibe Coding Risk Containment & Governed Development (AI 開發的資安隔離與治理)

> **This phase is modularized.** The full content lives in the companion skill file `vibe-coding-containment.md`. Reference it, load it, and keep it in sync. It is not "step five" — it is the fifth layer that wraps around the entire lifecycle, active from Phase 2 onward and reviewed weekly in Phase 4.

**Module reference**: `vibe-coding-containment.md`

**Steps covered by the module**:
- **Step 11**: Enforce the "Chu-Han Boundary" Architectural Isolation
- **Step 12**: Install AI-Powered Security Gates Before Deployment
- **Step 13**: Adopt Governed Low-Code as the Default for Non-Technical Teams
- **Step 14**: Platform Liability Reality Check
- **Step 15**: Weekly "Blast Radius" Review

**Integration points**:
- Activated in **Phase 2 / Step 3** the moment technical agents begin generating code.
- Reviewed in **Phase 4 / Step 9** during the weekly post-mortem.
- Audited in **Phase 4 / Step 10** as part of security posture checks.
