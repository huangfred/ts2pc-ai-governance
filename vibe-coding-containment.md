---
name: vibe-coding-containment
version: 1.0
description: A standalone containment module for governing AI-generated code (Vibe Coding) in non-technical teams. Enforces architectural isolation between the Core Security Zone and the Micro-Innovation Zone, mandates AI-powered security gates before deployment, recommends governed low-code platforms over free-form prompting tools, and provides a legal reality check on platform liability. Use when non-technical teams adopt tools like Lovable, Turbofy, Bolt, or Cursor, or when an organization must cap the blast radius of AI-generated software.
---

# Vibe Coding Containment Module

## Purpose

This module governs the risks introduced when non-technical teams use AI agents to generate and deploy software. It is a **persistent defensive layer**, not a one-time step. It must be active from the moment technical agents are deployed and must keep running through every weekly iteration.

## Core Principle

> **The platform's "one-click deploy" is not a security guarantee. The platform's ToS will always shift final liability back to you. Design as if the platform bears zero liability.**

---

## Step 11: Enforce the "Chu-Han Boundary" Architectural Isolation

- **Action**: Physically separate the enterprise system into two zones before any AI code generation begins.
- **Teacher's Rule**:
  - **Core Security Zone (Outsource to Mature SaaS)**: Customer PII, employee credentials, payment processing, and core financials MUST use battle-tested SaaS (e.g., Salesforce/HubSpot for CRM, Clerk for auth, Stripe for payments). Vibe Coding is strictly forbidden here.
  - **Micro-Innovation Zone (Vibe Coding Sandbox)**: Unique business logic (e.g., a niche check-in workflow, an internal dashboard) may be AI-generated, but ONLY behind the API umbrella of the Core Zone. The AI handles logic, never identity or payment data.
  - **Kill Switch**: The moment a "micro-innovation" tool begins accumulating real user PII, it MUST be migrated to the Core Zone. "18 test records" and "18,000 real user records" look identical in a UI — a human reviewer must inspect the data layer, not the interface.

---

## Step 12: Install AI-Powered Security Gates Before Deployment

- **Action**: Mandate automated security scanning (e.g., Snyk, Checkmarx, Semgrep) in the CI/CD pipeline before any AI-generated code reaches production.
- **Teacher's Rule**:
  - Traditional SAST tools scan for "code that is written wrong." Vibe Coding disasters are usually "code that was never written" — e.g., a missing Supabase RLS policy. The scanner must explicitly check for **absence of security controls**, not just presence of CVEs.
  - Configure a **hard deployment block**: if the scan detects a disabled RLS policy, an exposed service-role key, or an unauthenticated API route, deployment is physically prevented. "Warning" is not enough; the deploy button must fail.

---

## Step 13: Adopt Governed Low-Code as the Default for Non-Technical Teams

- **Action**: When a team lacks engineering resources, route them to governed low-code platforms (e.g., Retool, FlutterFlow, Power Apps) instead of free-form prompting tools (Lovable, Turbofy, Bolt).
- **Teacher's Rule**:
  - Governed low-code platforms enforce **default-deny** at the resource layer: unconfigured permissions mean "no access," not "full access." This is the closest thing to a real safety net.
  - Document the residual risk: even governed platforms have escape hatches (e.g., direct DB credential connections bypass Access Policies). Audit these escape hatches quarterly.

---

## Step 14: Platform Liability Reality Check

- **Action**: Before adopting any AI dev platform, have legal counsel review the ToS for: liability caps, jurisdiction clauses, and "as-is" disclaimers.
- **Teacher's Rule**:
  - Assume the platform's liability cap (e.g., €25,000 per incident) is the *maximum* you will ever recover. For a commercial app handling real user data, this is effectively zero.
  - Cross-border litigation is economically irrational for most SMEs. The contract clause may be legally unenforceable under EU consumer protection law, but the cost of *proving* that exceeds the recovery. Design as if the platform bears zero liability.

---

## Step 15: Weekly "Blast Radius" Review

- **Action**: In the weekly post-mortem, add a dedicated review of what data the AI-generated tools can currently reach.
- **Teacher's Rule**: Ask one question every week: "If this tool were compromised tomorrow, what is the worst thing an attacker could reach?" If the answer includes PII, payment data, or core financials, the tool has escaped its sandbox and must be migrated or shut down immediately.

---

## Failure Modes This Module Prevents

| Failure Mode | How This Module Prevents It |
|---|---|
| A "micro-innovation" tool silently accumulates real PII | Step 11 Kill Switch: human reviewer inspects the data layer, not the UI |
| AI-generated code deploys with no RLS policy | Step 12 hard deployment block: scanner checks for *absence* of controls |
| Non-technical team uses free-form prompting tools by default | Step 13: route them to governed low-code with default-deny |
| Organization assumes the platform bears liability | Step 14: design as if liability cap is zero |
| No one notices a tool has escaped its sandbox | Step 15: weekly blast radius review |
