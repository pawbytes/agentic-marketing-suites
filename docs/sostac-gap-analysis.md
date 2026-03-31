# SOSTAC Framework Gap Analysis

> **Generated:** 2026-03-13
> **Status:** Documented — awaiting implementation
> **Scope:** Gaps between the current `marketing-sostac` skill and comprehensive SOSTAC framework coverage

---

## How to Read This Document

Each phase lists missing frameworks ordered by impact. Every entry includes:
- **What it is** — one-line definition
- **Why it matters** — why the gap hurts plan quality
- **Where it goes** — which file(s) to update
- **Implementation notes** — what "done" looks like

Severity legend:
- 🔴 **High** — plan quality meaningfully degrades without this
- ⚠️ **Medium** — useful for a meaningful subset of brands/contexts
- 🟢 **Low** — nice-to-have, covers edge cases

---

## Phase 1: SITUATION — "Where are we now?"

**Current coverage:** 12 frameworks + 14 competitor analysis methods
**Gap severity:** ⚠️ Medium

### Missing Frameworks

| # | Framework | Severity | What It Is | Why It Matters |
|---|---|---|---|---|
| S1 | **VRIO Framework** | 🔴 | Assesses resources as Valuable, Rare, Inimitable, Organized | Goes deeper than SWOT on *why* a competitor's advantage is sustainable — critical for positioning decisions in Phase 3 |
| S2 | **Value Chain Analysis** (Porter) | ⚠️ | Decomposes internal activities to find cost/differentiation advantages | Identifies where in the business the actual advantage originates, not just what it is |
| S3 | **BCG Growth-Share Matrix** | ⚠️ | Portfolio analysis: Stars, Cash Cows, Question Marks, Dogs | Essential for multi-product brands deciding where to invest marketing spend |
| S4 | **GE McKinsey Nine-Cell Matrix** | 🟢 | Multi-factor portfolio assessment (industry attractiveness × competitive strength) | More nuanced than BCG — better for complex portfolios. Can skip if BCG is implemented |
| S5 | **EFE/IFE Matrices** | ⚠️ | External/Internal Factor Evaluation with weighted scoring | Turns SWOT gut-feel into scored, prioritized factors — adds quantitative rigor |
| S6 | **SPACE Matrix** | 🟢 | Strategic Position & Action Evaluation on 4 axes | Determines if brand should be aggressive, competitive, conservative, or defensive |
| S7 | **RFM Analysis** | 🔴 | Recency, Frequency, Monetary — customer value segmentation | Critical for any brand with existing customers — feeds directly into Strategy targeting |
| S8 | **Share of Search Analysis** (Les Binet) | 🔴 | Brand demand proxy using organic search volume trends | Correlates with market share, free to measure, modern brand health baseline |
| S9 | **Dark Funnel Audit** | 🔴 | Map untrackable buyer research in private channels, AI tools, communities | 60-70% of the buying journey is now invisible to analytics — ignoring it means misunderstanding how customers actually buy |
| S10 | **6Cs Model** | ⚠️ | Customers, Company, Competitors, Collaborators, Context, Content | Broader than SWOT — forces consideration of partners and content ecosystem |
| S11 | **Social Listening / Sentiment Analysis** | ⚠️ | Real-time brand and market monitoring methodology | Referenced implicitly in auto-discovery but not structured as a named framework with methodology |
| S12 | **First-Party Data Maturity Assessment** | ⚠️ | Evaluate organizational readiness for cookieless world | Goes beyond the existing privacy audit — assesses capability, not just compliance |

**Implementation notes:**
- Add S1, S7, S8, S9 to `references/frameworks.md` with full methodology (interview questions, output template, pitfall avoidance)
- Add S3, S5 to `references/frameworks.md` with methodology — mark S4, S6 as conditional ("invoke when portfolio has 3+ products" / "invoke when strategic direction is unclear")
- Add S8, S9 to `references/auto-discovery.md` with browser automation commands
- Update `SKILL.md` Phase 1 output template to include new required sections

### Missing Competitor Analysis (Operationalized)

| # | Gap | Severity | What's Missing | Implementation |
|---|---|---|---|---|
| SC1 | **SEMrush/Ahrefs keyword gap analysis** | 🔴 | Mentioned as tools but no scripted commands — should show keywords competitors rank for that brand doesn't | Add to `references/auto-discovery.md` with commands targeting Ahrefs or SEMrush free tools, or web search fallback |
| SC2 | **Backlink analysis** | ⚠️ | No procedure at all — competitor backlink profiles reveal link-building opportunities and content gaps | Add to `references/auto-discovery.md` — at minimum scrape Ahrefs free backlink checker |
| SC3 | **Share of Voice (SOV) calculation** | 🔴 | Referenced as a metric but no extraction method — SOV > SOM is a proven predictor of growth (Binet & Field) | Add operationalized SOV calculation using Google Trends + SERP visibility + social mention volume |
| SC4 | **Competitive Profile Matrix (CPM)** | ⚠️ | No weighted scoring of critical success factors across competitors | Add to `references/frameworks.md` as a structured scoring template — turns competitor landscape table into quantitative comparison |

---

## Phase 2: OBJECTIVES — "Where do we want to be?"

**Current coverage:** 8 frameworks
**Gap severity:** ⚠️ Medium

### Missing Frameworks

| # | Framework | Severity | What It Is | Why It Matters |
|---|---|---|---|---|
| O1 | **Balanced Scorecard** (for objective-setting) | ⚠️ | Financial + Customer + Internal Process + Learning & Growth objectives | Currently only used in Phase 6 Control — should also be used to *set* multi-perspective objectives |
| O2 | **CLV/LTV Targets** | 🔴 | Customer Lifetime Value improvement as a structured objective | Referenced in benchmarks but not structured as an objective-setting methodology with formulas and target ranges |
| O3 | **Product-Led Growth Metrics** | 🔴 | Time-to-Value, Activation Rate, PQLs, Expansion Revenue targets | Missing entirely — essential for SaaS/PLG companies. Without these, PLG brands get wrong KPIs |
| O4 | **Community-Led Growth Metrics** | ⚠️ | Community-attributed pipeline, member-to-customer conversion, advocacy score | Missing — growing importance for community-first brands |
| O5 | **Dark Social KPIs** | 🔴 | Self-reported attribution volume, deep direct traffic trends, branded search growth | Without these, 60%+ of marketing influence goes unmeasured and therefore unfunded |
| O6 | **Marketing Efficiency Ratio (MER)** | 🔴 | Total revenue ÷ total marketing spend as a target | Missing as a target-setting framework — the holistic efficiency metric when channel attribution breaks down |
| O7 | **Pipeline Velocity Metrics** | ⚠️ | Speed × volume × conversion × value of pipeline movement | Missing for B2B — critical for sales-assisted models |
| O8 | **Market Share Objectives** | ⚠️ | Target share of market, share of voice, share of search | Not structured as a named methodology with benchmarks and target-setting guidance |

**Implementation notes:**
- Add O2, O3, O5, O6 to `references/frameworks.md` with formula, benchmark ranges by vertical, and objective template
- Add O3 conditionally: "Apply when brand uses freemium, free trial, or self-serve signup"
- Add O5 with a note connecting back to S9 (Dark Funnel Audit) — if the audit is skipped, these KPIs are still valuable
- Update `references/best-practices.md` §3 with expanded benchmark tables for PLG and CLG
- Update `SKILL.md` Phase 2 output template to include optional sections for PLG/CLG/Dark Social objectives

---

## Phase 3: STRATEGY — "How do we get there?"

**Current coverage:** 11 frameworks
**Gap severity:** 🔴 High — biggest gap in the entire skill

### Missing Frameworks

| # | Framework | Severity | What It Is | Why It Matters |
|---|---|---|---|---|
| ST1 | **Growth Loops vs Funnels** | 🔴 | Self-reinforcing loops (viral, UGC, paid, sales, content, data) instead of linear funnels | Fundamental shift in modern growth strategy. Mentioned in best-practices but no dedicated methodology with loop identification, design, and measurement |
| ST2 | **Product-Led Growth (PLG) Strategy** | 🔴 | Product as primary GTM engine — freemium, self-serve, PQLs, expansion revenue | Missing as a strategic framework. Only appears in growth model selection table as one line |
| ST3 | **Community-Led Growth (CLG) Strategy** | ⚠️ | Community as distribution moat — 5 Ps Framework, SPACES Model, Lighthouse-Port-City model | Missing entirely from SOSTAC. The community skill exists but SOSTAC doesn't produce CLG strategy recommendations |
| ST4 | **Demand Creation vs Demand Capture** | 🔴 | Bifurcate strategy into brand-building (dark/unmeasurable) vs conversion (trackable) | Without this distinction, brands over-index on measurable channels and under-invest in brand. This is the Binet & Field long vs short framework applied |
| ST5 | **Competitive Positioning Maps / Perceptual Maps** | ⚠️ | 2D plots of brand vs competitors on key attributes with white-space identification | Referenced inside STP but not as a standalone methodology with axis selection guidance and worked example |
| ST6 | **Strategic Group Analysis** | ⚠️ | Cluster competitors by strategy similarity — find where the herd is and where white space exists | Different from perceptual maps. Reveals competitive clusters and underserved positions |
| ST7 | **Bowman's Strategic Clock** | ⚠️ | 8 competitive positioning options based on price/perceived value | More nuanced than Porter's Generic Strategies (8 positions vs 3). Better for pricing-strategy-adjacent positioning |
| ST8 | **Scenario Planning** | ⚠️ | Develop multiple future scenarios — test if strategy is robust across different outcomes | Missing — important for volatile markets, regulatory uncertainty, or AI disruption risk |
| ST9 | **Revenue Architecture** (Winning by Design) | ⚠️ | Recurring revenue models — bow-tie funnel, impact loops, NRR-centric design | Missing — essential for subscription businesses. Reframes the funnel from "acquire" to "expand" |
| ST10 | **Ecosystem / Platform Strategy** | 🟢 | Build network effects, integrations, marketplaces around core product | Missing — relevant for platform and marketplace businesses specifically |
| ST11 | **Privacy-First Strategy** | ⚠️ | Cookieless targeting, contextual advertising, consent-based personalization as strategic pillars | Covered only tactically in privacy audit — missing as a strategic-level decision framework |
| ST12 | **AI-First Go-to-Market** | ⚠️ | Leverage AI for personalization-at-scale, dynamic pricing, predictive targeting as a strategic option | Missing — increasingly relevant as AI transforms GTM |
| ST13 | **Three Horizons of Growth** (McKinsey) | 🟢 | H1: core business, H2: emerging opportunities, H3: transformational bets | Useful for resource allocation across growth horizons — especially for established brands |

**Implementation notes:**
- ST1 is the highest-priority addition: add to `references/frameworks.md` with loop types (viral, UGC, paid, sales, content, data network), loop identification method, and how to choose primary loop based on business model
- ST2 needs a full methodology: PLG readiness assessment → PLG model selection (freemium vs free trial vs reverse trial vs open core) → PLG metrics → PLG-specific channel strategy
- ST4 is critical for budget allocation: add the 60/40 brand-building vs performance split (Binet & Field), how to measure brand-building ROI indirectly, and how this connects to the 70/20/10 budget rule in Phase 4
- ST3, ST5, ST6 can be added as conditional frameworks invoked when relevant
- Update `SKILL.md` Phase 3 output template to include Growth Model, Primary Growth Loop, and Demand Creation/Capture split sections
- Consider creating a new `references/growth-strategy.md` file for ST1-ST4 since they form a cohesive modern growth strategy block

---

## Phase 4: TACTICS — "The details of strategy"

**Current coverage:** 16+ frameworks including 8 Situational Playbooks
**Gap severity:** ⚠️ Medium

### Missing Frameworks

| # | Framework | Severity | What It Is | Why It Matters |
|---|---|---|---|---|
| T1 | **ABM (Account-Based Marketing) Tactics** | 🔴 | 1:1, 1:Few, 1:Many tactical tiers for high-value B2B accounts | Missing — essential for enterprise B2B. Currently no account-level tactical planning |
| T2 | **Growth Loop Implementation** | 🔴 | Tactical execution playbook for viral, UGC, paid, sales, content loops | Strategy (ST1) defines which loop; this is *how* to build and measure it tactically |
| T3 | **Product-Led Tactics** | ⚠️ | Free trial optimization, in-product onboarding, PQL scoring, activation triggers | CRO skill handles some, but SOSTAC doesn't produce PLG tactical plans. Bridge needed |
| T4 | **Community Tactics** | ⚠️ | Platform choice, engagement rituals, champion programs, co-creation | Community skill has them but SOSTAC doesn't plan them in the tactics phase |
| T5 | **CDP Activation Tactics** | ⚠️ | Real-time segmentation, cross-channel personalization, predictive audiences | Modern personalization infrastructure — missing as a tactical choice |
| T6 | **Cookieless Attribution Tactics** | ⚠️ | Server-side tracking, probabilistic matching, conversion modeling, data clean rooms | Tactical implementation of privacy-first measurement |
| T7 | **Conversational Marketing** | ⚠️ | Chatbots, AI agents, messaging-first engagement (WhatsApp, SMS, live chat) | Growing channel — missing entirely. Relevant for lead gen, support-as-marketing, and activation |
| T8 | **Retail Media / Commerce Media** | 🟢 | Amazon Ads, retailer ad networks, shoppable content | Missing — relevant for e-commerce brands selling through marketplaces |
| T9 | **Content Marketing Matrix** | ⚠️ | Map content types by awareness↔purchase and emotional↔rational | Missing — helps visualize content portfolio balance and identify gaps |
| T10 | **RACE Framework** (tactical expansion) | 🟢 | Reach, Act, Convert, Engage — detailed tactical actions per stage | Used in objectives but not expanded into tactical execution detail |
| T11 | **Creator Economy Tactics** | ⚠️ | Long-term creator partnerships, creator-led commerce, co-creation, ambassador programs | Lightly covered via influencer skill but not surfaced in SOSTAC tactical planning |

**Implementation notes:**
- T1 is the highest-priority addition for B2B brands: add ABM tier model (1:1, 1:Few, 1:Many), account selection criteria, personalization depth per tier, and tech stack requirements
- T2 connects to ST1: add implementation detail for each loop type (viral coefficient targets, UGC submission flows, paid reinvestment ratios, sales loop metrics)
- T3, T4 need "bridge" sections that point to the specialist skills while ensuring SOSTAC *plans* the tactical allocation
- T7 should be added to the Situational Playbook Router — conversational marketing fits as a tactic under Demand Generation and Conversion-Led playbooks
- Consider adding T1 as a 9th Situational Playbook: "Enterprise ABM" triggered by "B2B + ACV > $25K + named account strategy"

---

## Phase 5: ACTION — "Who does what, when?"

**Current coverage:** 10 frameworks
**Gap severity:** 🟢 Low — best-covered phase

### Missing Frameworks

| # | Framework | Severity | What It Is | Why It Matters |
|---|---|---|---|---|
| A1 | **3Ms Framework** (PR Smith) | ⚠️ | Men (people), Money (budget), Minutes (timeline) — PR Smith's own action planning model | Ironic gap — this is from SOSTAC's creator. Simple but ensures all three resource dimensions are covered |
| A2 | **Gantt Charts** | 🟢 | Visual timeline-based project scheduling | Basic PM tool — useful for stakeholder communication and dependency visualization |
| A3 | **Campaign Briefs** (standardized template) | ⚠️ | Consistent brief format for each campaign or initiative | The agency skill has campaign strategy.md but no individual initiative brief template for handing off to specialists |
| A4 | **Workflow / Process Mapping** | 🟢 | Document approval flows, handoffs, dependencies | Important for scaling teams — missing but only relevant for larger operations |
| A5 | **RevOps Architecture** | ⚠️ | Unified revenue operations — marketing + sales + CS tech stack integration, data flows | Missing — connects marketing actions to sales and CS operations |
| A6 | **No-Code/Low-Code Execution** | 🟢 | Rapid landing page, workflow, integration deployment without engineering | Increasingly important for fast execution — mention as an execution option |

**Implementation notes:**
- A1 is a quick win: add the 3Ms as a planning checklist within the existing Phase 5 section. Three questions: "Do we have the right people?", "Is the budget allocated?", "Is the timeline realistic?"
- A3: create a campaign brief template in `references/frameworks.md` that specialists receive when spawned by the agency coordinator
- A5: add as a conditional section ("When brand has sales team, define RevOps handoffs")
- A2, A4, A6 are low priority — mention them as available tools rather than building full methodologies

---

## Phase 6: CONTROL — "How do we monitor?"

**Current coverage:** 11 frameworks
**Gap severity:** ⚠️ Medium

### Missing Frameworks

| # | Framework | Severity | What It Is | Why It Matters |
|---|---|---|---|---|
| C1 | **Self-Reported Attribution** | 🔴 | "How did you hear about us?" open-text field on high-intent forms | Simplest and most effective dark funnel measurement. Captures word-of-mouth, podcasts, communities, AI recommendations |
| C2 | **Marketing Efficiency Ratio (MER)** | 🔴 | Total revenue ÷ total marketing spend — holistic efficiency metric | When channel attribution breaks down (it already has), MER is the reliable fallback |
| C3 | **Demand Creation vs Capture Reporting** | 🔴 | Separate measurement for brand-building vs conversion activities | Without this, brand-building always loses budget to short-term measurable channels |
| C4 | **Cohort & Retention Analysis** | 🔴 | Track user cohorts over time — retention curves, engagement decay, LTV evolution | Missing — critical for subscription/SaaS. Without cohorts, averages hide deteriorating quality |
| C5 | **Predictive Analytics / AI Forecasting** | ⚠️ | ML models for CLV prediction, churn prediction, pipeline forecasting | Missing as a structured methodology — becoming standard for data-mature brands |
| C6 | **Real-Time Anomaly Detection** | ⚠️ | AI-powered alerts for performance deviations, budget pacing, quality issues | Modern monitoring standard — catches problems hours/days faster than dashboard reviews |
| C7 | **Privacy-Compliant Measurement** | ⚠️ | Conversion modeling, aggregated reporting, data clean rooms, differential privacy | Missing as an ongoing control methodology — only covered as a one-time audit |
| C8 | **Win/Loss Analysis** | ⚠️ | Post-deal interviews to understand why deals were won or lost vs competitors | Missing — feeds back into competitor analysis (Phase 1) and positioning (Phase 3). B2B-critical |
| C9 | **Evidence-Based Attribution Reporting** | ⚠️ | Confidence-level labeling (High/Medium/Low) instead of false precision | Modern alternative to pretending perfect attribution exists — more honest and more useful |

**Implementation notes:**
- C1 is the highest-impact, lowest-effort addition: add to `references/frameworks.md` with field placement guidance, question wording options, and how to analyze free-text responses
- C2, C3 connect to ST4 (Demand Creation vs Capture strategy): add as paired monitoring methodologies
- C4: add cohort analysis methodology with retention curve visualization guidance, cohort comparison method, and "good" retention benchmarks by vertical
- C8: add as a conditional section ("When brand has B2B sales, implement Win/Loss analysis") with interview template and feedback loop back to Phase 1 and Phase 3
- Consider grouping C1, C2, C3, C9 into a "Modern Attribution Stack" section in `references/frameworks.md` since they form a coherent alternative to pure multi-touch attribution

---

## Cross-Phase Gaps

These gaps span multiple phases and represent systemic blind spots:

### Gap X1: Product-Led Growth (PLG) — Missing Across All Phases

| Phase | What's Missing |
|---|---|
| Situation | PLG readiness assessment, product-market fit signals |
| Objectives | Time-to-Value, Activation Rate, PQL targets, Expansion Revenue |
| Strategy | PLG model selection (freemium vs trial vs reverse trial vs open core) |
| Tactics | In-product onboarding, PQL scoring, activation triggers, self-serve optimization |
| Action | PLG team structure, product-marketing alignment |
| Control | PLG-specific metrics dashboard, product usage analytics |

**Recommendation:** Create `references/plg-framework.md` covering all phases. Add conditional invocation: "Apply when brand uses freemium, free trial, or self-serve signup model."

### Gap X2: Dark Social / Demand Creation — Missing Across 4 Phases

| Phase | What's Missing |
|---|---|
| Situation | Dark Funnel Audit — where are buyers researching that you can't see? |
| Objectives | Dark Social KPIs, MER targets |
| Strategy | Demand Creation vs Demand Capture budget/effort split |
| Control | Self-Reported Attribution, MER monitoring, Evidence-Based Reporting |

**Recommendation:** Add a "Dark Social & Demand Creation" section to `references/best-practices.md` covering the full measurement philosophy and tactical implementation. This is arguably the single most important modernization needed.

### Gap X3: Community-Led Growth (CLG) — Missing Across 3 Phases

| Phase | What's Missing |
|---|---|
| Strategy | CLG as a strategic model (5 Ps, SPACES, Lighthouse-Port-City) |
| Tactics | Community platform choice, engagement rituals, champion programs |
| Objectives | Community-attributed pipeline, member-to-customer conversion |

**Recommendation:** Add CLG sections to existing phase references. Bridge to the existing `marketing-community` skill so SOSTAC *plans* community strategy and the specialist skill *executes* it.

### Gap X4: Growth Loops — Missing Across 2 Phases

| Phase | What's Missing |
|---|---|
| Strategy | Loop identification, primary loop selection based on business model |
| Tactics | Loop implementation playbooks (viral, UGC, paid, sales, content, data) |

**Recommendation:** Add to `references/frameworks.md` as a paired Strategy + Tactics framework. This replaces/supplements the linear funnel thinking that still dominates the current skill.

---

## Implementation Priority Matrix

Ordered by impact on plan quality:

| Priority | Items | Effort | Impact |
|---|---|---|---|
| **P0 — Do First** | ST1 (Growth Loops), ST4 (Demand Creation vs Capture), C1 (Self-Reported Attribution), C2 (MER), C4 (Cohort Analysis), S9 (Dark Funnel Audit) | Medium | 🔴 These 6 items fix the biggest philosophical gap — the skill currently assumes all marketing is measurable and funnel-shaped |
| **P1 — High Value** | ST2 (PLG Strategy), O3 (PLG Metrics), O5 (Dark Social KPIs), T1 (ABM), S7 (RFM), S8 (Share of Search), SC1 (Keyword Gap), SC3 (SOV Calculation) | Medium-High | 🔴 These cover the most common brand types (SaaS/PLG, B2B enterprise) and the most requested modern metrics |
| **P2 — Good Additions** | S1 (VRIO), S3 (BCG), ST3 (CLG), ST5 (Perceptual Maps), ST7 (Bowman's Clock), T2 (Loop Implementation), T7 (Conversational Marketing), C3 (Demand Reporting), C8 (Win/Loss) | Medium | ⚠️ Fills meaningful gaps for specific brand types and adds strategic depth |
| **P3 — Nice to Have** | S4 (GE McKinsey), S6 (SPACE), S10 (6Cs), ST8 (Scenario Planning), ST10 (Ecosystem), ST13 (Three Horizons), T8 (Retail Media), A2 (Gantt), A4 (Process Mapping), A6 (No-Code) | Low | 🟢 Conditional or edge-case frameworks — add when core gaps are filled |

---

## File-Level Change Map

Where each gap should be implemented:

| File | Items to Add |
|---|---|
| `references/frameworks.md` | S1, S3, S5, S7, S8, O2, O3, O5, O6, ST1, ST2, ST4, ST5, ST6, ST7, T1, T9, A1, C1, C2, C3, C4, C8, C9 |
| `references/auto-discovery.md` | S9 (Dark Funnel commands), SC1 (Keyword gap commands), SC2 (Backlink commands), SC3 (SOV commands) |
| `references/best-practices.md` | O3 (PLG benchmarks), O4 (CLG benchmarks), ST3 (CLG strategy), T3 (PLG tactics), T4 (Community tactics), C5 (Predictive analytics), C6 (Anomaly detection), C7 (Privacy measurement) |
| `SKILL.md` | Update Phase 1-6 output templates to include new required/optional sections |
| **New file:** `references/plg-framework.md` | Cross-phase PLG coverage (Gap X1) |
| **New file:** `references/growth-strategy.md` | Growth Loops + Demand Creation/Capture + CLG (Gaps X2, X3, X4) |

---

## Total Gap Count

| Phase | Missing Frameworks | Missing Competitor Ops |
|---|---|---|
| Situation | 12 | 4 |
| Objectives | 8 | — |
| Strategy | 13 | — |
| Tactics | 11 | — |
| Action | 6 | — |
| Control | 9 | — |
| **Total** | **59** | **4** |
