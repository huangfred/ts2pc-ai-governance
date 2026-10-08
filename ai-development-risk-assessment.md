---
name: ai-development-risk-assessment
version: 1.0
description: A consultant-facing assessment tool for evaluating AI development mode choices. Uses a three-dimensional framework (enterprise scale × expert capability × expert authority) to locate ten common development patterns on a risk spectrum, identify contradictory combinations that signal organizational dysfunction, and produce actionable recommendations for non-technical decision-makers. Companion tool to ai-agent-enterprise-implementation.md and vibe-coding-containment.md.
---

# AI Development Risk Assessment (Consultant Tool)

## Purpose

This tool helps consultants and decision-makers answer one question:

> **Given this organization's scale, expertise, and governance structure, which AI development mode is safe to use — and which is not?**

It is a companion to `ai-agent-enterprise-implementation.md` and `vibe-coding-containment.md`. Where those documents describe the methodology, this document provides the diagnostic instrument.

---

## The Three-Dimensional Framework

Risk is not determined by which tool you use. It is determined by **who is using it, and whether they have the capability and authority to stop an unsafe deployment.**

### Dimension 1: Enterprise Scale (X-axis)

- **OPC / Individual**: The decision-maker is the operator.
- **Small Enterprise**: No technical team; relies on external tools and platforms.
- **Medium Enterprise**: Has IT staff, but no dedicated security personnel.
- **Large Enterprise**: Has dedicated security staff and compliance requirements.

### Dimension 2: Expert Capability (Y-axis)

- **Capable**: Someone on the team can see what the AI-generated code *failed to include* — missing RLS policies, exposed service-role keys, unauthenticated API routes.
- **Not Capable**: Someone reviews whether the *functionality* works, not whether it is *secure*.

### Dimension 3: Expert Authority (Switch)

- **Has Veto Power**: When this person says "this cannot go live," their decision is final.
- **No Veto Power**: Their opinion exists, but delivery-speed pressure overrides it.

**Note on Dimension 3**: For OPC/individual, veto power is not externally granted — the operator *is* the decision-maker. This dimension collapses into "capability" alone.

---

## Table 1: Ten Development Patterns — Full Assessment

| Mode | Enterprise Scale | Expert Capability | Expert Authority | Risk Level | Consultant Recommendation | Notes |
|---|---|---|---|---|---|---|
| **momo as Seller** | Any scale | Not required | Not required | Low | ✅ Recommended | Legal liability rests with the platform |
| **E-commerce Platform SaaS** | OPC / Small / Medium | Platform provides | N/A | Medium | ✅ Recommended | Review ToS |
| **No-Code Platform** | OPC / Small | Platform provides governance | N/A | Medium | ✅ Recommended | Not for core systems |
| **Low-Code Platform** | Medium / Large | Requires IT oversight | Requires veto power | Medium | ✅ Recommended | Requires institutional gate |
| **SI + Managed Hosting** | Medium / Large | SI provides | Determined by contract | Medium-High | ⚠️ Recommended with contract review | Review SI liability terms |
| **FDE + Vibe Coding (with veto)** | Medium / Large | Capable | Has veto | Medium-High | ⚠️ Recommended with institutional gate | Usable, requires security gate |
| **FDE + Vibe Coding (no veto)** | Medium / Large | Capable | No veto | High | ⚠️ Not recommended unless veto power is added | KPI conflict |
| **Vibe Coding + Managed Hosting** | OPC / Small | Not capable | No veto | High | ⚠️ Not recommended unless external security review | Requires externalized check |
| **Vibe Coding + Payments/Auth/Hosting** | OPC / Small | Not capable | No veto | Very High | ❌ Not recommended unless operator is a Type-2 Expert | Requires Type-2 Expert operating personally |
| **Build-Your-Own (self-hosted)** | OPC / Small | Not capable | No veto | Very High | ❌ Not recommended unless full-stack engineer + security capability | Requires Type-2 Expert operating personally |

---

## Table 2: Contradictory Combinations (Not Viable)

These are not tool choices. They are organizational dysfunctions.

| Contradictory Combination | Why It Is Contradictory | Consultant Diagnosis |
|---|---|---|
| **OPC + Has Veto Power** | Tautology — veto power is not externally granted | N/A; OPC has only "capability" dimension |
| **Small Enterprise + Has Veto Power** | Scale and governance capability mismatch | Organizational structure problem, not tool choice problem |
| **Medium Enterprise + Not Capable + Has Veto Power** | Transitional state, unstable | High risk and unsustainable; must either build capability or revoke authority |
| **Large Enterprise + Not Capable + No Veto Power** | Pathological state, institutional failure | Very high risk; enterprise usually unaware |

---

## Recommendation Labels — Definitions

**✅ Recommended**
Risk is controlled. Suitable for the enterprise's scale and capability. Recommend directly.

**⚠️ Recommended with conditions / Not recommended unless…**
Technically viable, but risk and enterprise capability are mismatched. If the enterprise insists, the consultant must require specific conditions be met first (security gate, external review, veto power).

**❌ Not recommended unless…**
Technically viable, but for this scale of enterprise, risk and capability are severely mismatched. Only in rare conditions (e.g., the operator is personally a Type-2 Expert) is it worth considering. The consultant should default to "no."

**Contradictory combinations**
Not a tool problem — an organizational problem. The consultant should directly identify the structural defect, not recommend an alternative tool.

---

## Consultant Workflow

### Step 1: Locate the Client

Ask three questions:

1. **Enterprise scale?** OPC / Small / Medium / Large
2. **Does anyone on your team see what the AI-generated code *failed to include*?** Capable / Not capable
3. **When this person says "cannot go live," is their decision final?** Has veto / No veto

### Step 2: Map to Risk Level

Using Table 1, locate the client's current mode and corresponding risk level.

### Step 3: Issue the Recommendation

- **✅**: Recommend directly, note caveats.
- **⚠️**: Ask "Have you met the stated condition?" If not, do not recommend. If yes, proceed with continuous oversight.
- **❌**: Ask "Is the operator personally a Type-2 Expert?" If not, say no. If yes, proceed with externalized checks as backup.
- **Contradictory**: Do not recommend a tool. Name the organizational defect.

### Step 4: Deliver the One-Line Diagnosis

> "Your risk is not in the tool you chose. It is in **[the missing gap]**. Until that gap is closed, Vibe Coding may only be used for **[the safe zone]**."

---

## Core Insight

**The same tool, in different quadrants, carries a completely different risk level.**

Vibe Coding in the green zone (capable + has veto) is medium-high risk. In the red zone (not capable + no veto), it is very high risk.

**Risk is not determined by the tool. It is determined by who is using it, and whether they have the capability and authority to stop an unsafe deployment.**

---

## Relationship to Other Documents

| Document | Role |
|---|---|
| `ai-agent-enterprise-implementation.md` | The 4-phase, 10-step methodology |
| `vibe-coding-containment.md` | The containment module (Steps 11-15) |
| `ai-development-risk-assessment.md` (this file) | The consultant-facing diagnostic instrument |
