# 01 - Introduction

## Why This Book
Artificial intelligence has moved from experimentation to execution. Technology leaders are expected to deliver outcomes quickly while managing risk, cost, and organizational change. In my experience with actually getting value and understanding how to generate value has been one of the biggest challenges. Whether your work in an organization that go with the "AI team" or are full scale into making product support AI driven, rewriting the process landscape or are just curious this book is for you.  

## The Leadership Shift
AI is not only a technical capability. It changes how teams work, how products are built, and how decisions are made. This requires leaders to redesign systems, incentives, and operating habits.

## What You Will Learn
- How to define an AI strategy tied to business goals
- How to build AI capabilities inside engineering organizations
- How to govern AI responsibly and pragmatically
- How to secure AI systems in real-world environments

## How to Use This Book
Read each chapter in order for a full transformation narrative. Use the checklists at the end of each chapter to drive planning sessions with your leadership team.

---

# AI Engineering - a bit of background on why I created this book

## Executive summary

The market has moved past the "should we adopt AI coding tools" question. 85% of developers already use AI coding tools regularly, and Gartner expects 40% of enterprise applications to contain task-specific AI agents by the end of 2026 - up from under 5% in 2025. The open question for leadership is no longer adoption, it's control: Gartner also expects over 40% of agentic AI projects to be cancelled by 2027 due to cost overruns, unclear ROI, and weak risk controls. The organizations pulling ahead are not the ones with the most agents - they're the ones that engineered governance into the system from day one. One striking data point should anchor the leadership narrative: organizations that build control into their AI systems deploy 16x more agents than those relying on manual governance, spend 4x less of their AI budget doing it, and post 18% higher operating margins. That is the business case, in one sentence: governance is not a brake on scale, it is the precondition for it.

## 1. What already exists - state of the art (2025-2026)

**Tool adoption is mainstream, but fragmented by design.** The AI coding assistant market reached $12.8B in 2026 (27% CAGR to 2032). Three tools dominate for different reasons: GitHub Copilot leads on raw enterprise distribution (4.7M paid seats, deep Microsoft/IDE integration), Cursor leads on revenue ($2B ARR, 1M+ paying users), and Claude Code leads on developer satisfaction (46% "most loved" in JetBrains' April 2026 survey, vs. 19% Cursor and 9% Copilot). 70% of engineers now use 2-4 tools simultaneously. The emerging enterprise pattern is deliberate, not accidental: Copilot as the broad autocomplete baseline for every engineer, Claude Code adopted bottom-up by senior engineers for high-leverage agentic work. Leadership implication: a single-vendor mandate is increasingly out of step with how engineers actually work - the winning pattern is a curated, governed multi-tool portfolio, not a monopoly license.

**Adoption has outrun governance.** 72% of large enterprises report agentic AI in production, but only 21% have a mature AI-agent governance model, and 84% haven't redesigned roles around AI at all. Only 8% of organizations globally have a comprehensive AI governance framework despite 88% actively using AI. At board level the gap is just as stark: only ~39% of Fortune 100 boards have explicit AI oversight mechanisms, and 66% of boards report limited-to-no working knowledge of AI. This is the central tension the book should name explicitly: velocity of deployment has decoupled from maturity of control, and that gap is where the cancelled projects, the security incidents, and the trust erosion come from.

**Code quality has become a boardroom issue, not just an engineering one.** 45% of AI-generated code samples introduce OWASP Top 10 vulnerabilities, a rate that hasn't improved across testing cycles from 2025 into 2026. 70% of engineering leaders say application quality has already degraded because code generation outpaced testing capacity. Only 29% of developers trust the code their own AI tools produce, despite 92% using them daily. This is not a reason to slow adoption - DORA's 2025 research is explicit that AI acts as a multiplier of existing engineering conditions, amplifying strength in disciplined organizations and amplifying dysfunction in fragmented ones. The lesson for leadership: AI does not fix a weak engineering culture, it exposes it faster and at greater scale.

**Regulation has a hard deadline.** The EU AI Act's high-risk provisions (credit scoring, employment, insurance underwriting, and similar regulated domains) take full effect 2 August 2026, with fines up to 7% of global annual turnover. This converts "AI governance" from a best-practice conversation into a compliance deadline with a fixed date, which is a useful forcing function for board attention.

## 2. What it means for how software gets built (through 2030)

Several forecasters converge on the same shape of change, even where the exact numbers differ:

- **The unit of work shifts from "write code" to "specify, orchestrate, and validate."** By 2030, a standard CRUD application with auth, database, and API layer is expected to be a prompt, not a project. Engineers increasingly assign work to specialized agents (architecture, testing, security, deployment) rather than writing every line themselves.
- **Three technical shifts converge**: agents that see and hear (multimodal), agents that remember across sessions (persistent memory), and agents that work in teams (multi-agent orchestration). By 2028, roughly a third of agentic AI implementations are expected to combine multiple specialized agents to handle complex tasks - this is the direction Henrik's Domain 6 (AI Runtime & Operations) is already built for.
- **The engineering role bifurcates rather than disappears.** Staff+ engineers who own systems, architecture, and outcomes become more valuable, not less. Entry-level, execution-heavy roles face the sharpest contraction because an agent has no marginal cost and infinite patience for routine multi-step work. The scarce skill becomes workflow integration, governance judgment, and cross-agent communication - not typing speed.
- **"AI SRE" is becoming a distinct discipline.** Multi-agent incident response (a coordinator agent delegating to metrics/traces/logs sub-agents) is moving from prototype to production, with SLOs now explicitly covering model latency P99, token throughput, and hallucination rate as first-class operational metrics - not just uptime.

## 3. What it means for the tools engineers will use

The tools layer is consolidating around three archetypes rather than one winner, and leadership should plan procurement and platform strategy around that reality rather than betting on a single vendor:

1. **Broad-baseline assistants** (Copilot-class): distributed to every engineer, IDE-integrated, low friction, procurement-friendly at enterprise scale.
2. **High-leverage agentic tools** (Claude Code-class): adopted bottom-up by senior/staff engineers for multi-step, high-autonomy work; typically the tool with the highest satisfaction and the highest risk surface.
3. **Runtime & orchestration platforms**: the emerging category (agent registries, MCP/tool connectors, observability, policy-as-code enforcement) that most enterprises have not yet standardized - this is precisely the gap Henrik's Domain 5/6 split is designed to close, and it maps to what the market is now calling "AI platform engineering": a shared control plane for model access, agent orchestration, cost governance, and compliance, distinct from the runtime layer that executes agents.

The category mismatch to watch for, and worth a callout in the book: organizations frequently pay for governance tooling when they actually need execution infrastructure, or build runtime scaffolding when they actually needed a finished, governed platform. Getting this sequencing wrong is a recurring cause of stalled AI engineering initiatives.

## 4. What it means for leadership - how the C-suite and core stakeholders support the journey

| Stakeholder | 2026 reality | What "supporting the journey" concretely looks like |
|---|---|---|
| **CEO / Board** | Only 39% of Fortune 100 boards have explicit AI oversight; 66% report limited AI knowledge. EU AI Act enforcement begins Aug 2026. | Establish a board-level AI oversight mechanism (committee or named director) before a regulatory deadline forces it. Treat this as a fixed-date compliance item, not a discretionary initiative. |
| **CIO** | Role is being redefined from "runs technology" to "drives business value with AI"; now judged on outcomes, not uptime. | Own the shift from AI experimentation (2025 posture) to AI ROI (2026 posture). Act as integrator across CDO/CAIO/CISO/CTO - governance requires those functions to agree on shared standards, and the CIO is the natural convener. |
| **CTO / VP Engineering** | Organizations with senior AI leadership are 2x as likely to scale AI successfully (McKinsey). Governed orgs deploy 16x more agents at 4x lower cost. | Fund the runtime/observability layer (Domain 6) as seriously as the platform layer (Domain 5) - this is where the 2026 literature shows the gap actually is. Sponsor phase-gated automation (tool permissions narrow as risk increases) rather than all-or-nothing autonomy. |
| **Chief AI Officer / Head of AI Governance** | 60% of Fortune 100 companies expected to appoint a dedicated head of AI governance in 2026 (Forrester); only 21% currently have a mature governance model. | Stand up policy-as-code enforcement tied to a named owner, not a static policy document. Make governance a real-time runtime function, not an annual audit. |
| **CFO** | 40%+ of agentic AI projects forecast to be cancelled by 2027 over unclear ROI. | Demand the same rigor applied to AI investment as any other capital allocation: named business outcome, baseline metric, and a kill criterion - before scale-up, not after. |
| **CHRO / People leaders** | Skills demand is shifting from code-writing to systems thinking and AI orchestration; 85% of leaders say adaptability is critical, only 7% believe they're actually leading on it. | Redesign career ladders around orchestration and judgment, not typing throughput. Treat reskilling as a scheduled capability investment (Henrik's Domain 3), not a reactive layoff-adjacent scramble. |
| **Engineering managers** | 70% of leaders report quality has already degraded because code generation outpaced test capacity. | Track AI-attributed regression rate and review-confidence score as first-class engineering metrics (Domain 7 Outcomes), the same way security incidents are tracked. |

## 5. Key data points (for citation in the book)

| Statistic | Source |
|---|---|
| 85% of developers use AI coding tools regularly; 92% daily | Multiple 2026 developer surveys |
| Gartner: 40% of enterprise apps will include task-specific AI agents by end of 2026 (from <5% in 2025) | Gartner, Software Engineering 2030 |
| Gartner: 40%+ of agentic AI projects cancelled by 2027 (cost, ROI, risk controls) | Gartner |
| Governed orgs deploy 16x more agents, spend 4x less AI budget, post 18% higher operating margins | IBM 2026 Tech Leader Study |
| 72% of enterprises in agentic AI production; only 21% have mature governance | Agentic AI Institute, Deloitte |
| Only 8% of organizations have a comprehensive AI governance framework vs. 88% using AI | Kiteworks / industry governance surveys, 2026 |
| Only ~39% of Fortune 100 boards have explicit AI oversight; 66% of boards report limited AI knowledge | Board governance disclosures, 2026 |
| EU AI Act high-risk provisions fully enforced 2 Aug 2026; fines up to 7% global turnover | EU AI Act |
| 45% of AI-generated code introduces OWASP Top 10 vulnerabilities (Veracode, unimproved 2025->2026) | Veracode |
| 70% of engineering leaders report quality degradation from AI-accelerated development | SmartBear survey, 273 leaders |
| Only 29% of developers trust AI-generated code despite 92% daily usage | 2026 developer trust surveys |
| AI coding assistant market: $12.8B (2026) -> $30.1B (2032), 27% CAGR | Market research, 2026 |
| McKinsey: orgs with senior AI leadership 2x as likely to scale AI successfully; only 1% call their AI strategy "mature" | McKinsey State of AI / Global Tech Agenda 2026 |
| DORA: AI acts as a multiplier of existing engineering conditions, not a fix for weak ones | Google Cloud DORA, State of AI-Assisted Software Development 2025 |

## 6. One-line framing for the book

*"In 2026, the constraint on AI engineering is no longer whether the technology works - it's whether the organization can govern it fast enough to keep deploying it safely. Leadership's job is to build that governance capacity ahead of the deployment curve, not behind it."*

---

### Sources
- [Software Engineering 2030: The Impact of AI - Gartner](https://www.gartner.com/en/software-engineering/insights/software-engineering-2030-impact-of-ai)
- [The Future of Software Engineering with AI: Six Predictions - Pragmatic Engineer](https://newsletter.pragmaticengineer.com/p/the-future-of-software-engineering-with-ai)
- [2026 Tech Leader Study: Building the IT foundation for agentic AI at scale - IBM](https://www.ibm.com/thought-leadership/institute-business-value/en-us/report/2026-cxo)
- [How agentic AI will reshape engineering workflows in 2026 - CIO.com](https://www.cio.com/article/4134741/how-agentic-ai-will-reshape-engineering-workflows-in-2026.html)
- [What is redefining the CIO role in 2026?](https://www.digitransformationsummit.com/blogs/what-is-redefining-the-cio-role-in-2026/)
- [AI Governance in 2026: Why Boards That Wait Will Inherit an Ungovernable Mess - Kiteworks](https://www.kiteworks.com/cybersecurity-risk-management/ai-governance-boards-2026-mess/)
- [2026 is the year of enterprise AI governance - Speakeasy](https://www.speakeasy.com/blog/2026-year-of-ai-governance)
- [McKinsey Global Tech Agenda 2026](https://www.mckinsey.com/capabilities/mckinsey-technology/our-insights/mckinsey-global-tech-agenda-2026)
- [Redesigning technology workforce for the agentic AI era - McKinsey](https://www.mckinsey.com/capabilities/mckinsey-technology/our-insights/designing-an-end-to-end-technology-workforce-for-the-ai-first-era)
- [No more pyramids: Rethinking your workforce for the agentic AI era - PwC](https://www.pwc.com/us/en/tech-effect/ai-analytics/agentic-ai-workforce-redesign.html)
- [AI Coding Assistant Market Share 2026: Cursor vs Copilot](https://www.ideaplan.io/blog/ai-coding-assistant-market-share-2026)
- [Which AI Coding Tools Do Developers Actually Use at Work? - JetBrains](https://blog.jetbrains.com/research/2026/04/which-ai-coding-tools-do-developers-actually-use-at-work/)
- [AI Code Quality in 2026: Guardrails for AI-Generated Code](https://tfir.io/ai-code-quality-2026-guardrails/)
- [Agentic AI Enterprise Adoption 2026: Governance Gap](https://agenticaiinstitute.org/agentic-ai-enterprise-adoption-2026-governance-gap/)
- [DORA State of AI-Assisted Software Development 2025](https://dora.dev/dora-report-2025/)
- [AI Platform Engineering: A Complete Guide for 2026 - TrueFoundry](https://www.truefoundry.com/blog/what-is-ai-platform-engineering)
