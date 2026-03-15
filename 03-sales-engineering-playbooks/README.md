# Sales Engineering Playbooks

Discovery frameworks, qualification criteria, and technical
validation guides for enterprise Voice AI, CPaaS, and CCaaS deals.

Written from experience closing $100K–$500K deals across
financial services, healthcare, insurance, and large enterprise
contact centers.

---

## Discovery Framework

The goal of technical discovery is not to demonstrate product
knowledge. It is to surface the constraints that will determine
whether a deal is winnable and implementable.

### Tier 1 — Infrastructure Questions

Ask these in the first technical call. The answers determine
which architecture pattern applies.

| Question | What You Are Actually Qualifying |
|---|---|
| Are you currently on a legacy on-prem platform? | Migration complexity and timeline risk |
| Who manages your SIP trunking today? | Integration ownership and porting timeline |
| Do you have an internal engineering team? | Self-serve vs managed deployment model |
| What CRM are you using? | Integration complexity and existing connectors |
| Are calls recorded today? Where is that data stored? | Compliance and data residency requirements |

### Tier 2 — Compliance Questions

Non-negotiable in financial services, healthcare, and insurance.
Surface these before building a technical proposal.

| Question | Risk Being Qualified |
|---|---|
| Do you require a BAA with AI vendors? | HIPAA — eliminates vendors without BAA |
| Is payment data captured on calls? | PCI DSS — may require DTMF masking |
| Do you have data residency requirements? | Eliminates non-regional vendors |
| What is your security review process? | Deal timeline risk — SOC 2 reviews add 4–8 weeks |
| Who owns vendor approval in procurement? | Identifies true decision-making authority |

### Tier 3 — Commercial Questions

| Question | What You Are Qualifying |
|---|---|
| What is the current annual spend on your contact center platform? | Anchors budget conversation |
| Are you in an active contract with your current vendor? | Identifies timing constraints |
| What does a successful pilot look like to you? | Defines evaluation criteria before demo |
| Who else is involved in this decision? | Identifies full buying committee |

---

## Technical Objection Handling

### Objection: "We're concerned about latency."

**What they mean:** A previous AI vendor demo felt unnatural
or robotic. They associate AI voice with awkward pauses.

**How to respond:**
1. Acknowledge it as a legitimate concern — do not dismiss it
2. Ask them to describe what they experienced specifically
3. Explain the latency budget framework — where delays actually come from
4. Offer a live demo on real infrastructure, not a recorded video

**What not to do:** Quote latency numbers without context.
Saying "our STT is 200ms" means nothing to a buyer who
experienced 2,000ms end-to-end in a competitor demo.

---

### Objection: "Integration complexity is a concern."

**What they mean:** They have a legacy CRM, a custom IVR,
or an internal engineering team that is already over-committed.

**How to respond:**
1. Map their current stack before proposing anything
2. Identify which integrations are pre-built vs custom
3. Separate phase 1 scope from full integration — start smaller
4. Introduce a professional services or implementation partner

**The real risk:** Integration complexity objections that go
unresolved become the reason deals stall in legal or procurement.
Surface the full integration map in discovery, not in the SOW.

---

### Objection: "We have compliance requirements."

**What they mean:** Their legal or security team will kill
the deal if vendor documentation is incomplete.

**How to respond:**
1. Ask which frameworks apply — HIPAA, PCI, SOC 2, GDPR
2. Get vendor security documentation before the security review
3. Introduce your solutions engineer or security team early
4. Set timeline expectations — compliance reviews add weeks

**Industries where this surfaces most:**
Financial services, healthcare, and insurance.
In these verticals, assume compliance review is required
and build it into the deal timeline from day one.

---

## Deal Qualification Checklist

Use this before committing to a full technical proposal.

### Green Flags
- [ ] Active budget allocated for this fiscal year
- [ ] Executive sponsor identified and engaged
- [ ] Internal engineering resources confirmed for integration
- [ ] Current platform contract expiring within 12 months
- [ ] Compliance requirements documented and understood

### Yellow Flags — Qualify Further
- [ ] Budget is "in discussion" or requires new approval
- [ ] No internal engineering resources — implementation unclear
- [ ] Current platform contract has 18+ months remaining
- [ ] Multiple vendors still in active evaluation

### Red Flags — Reassess Priority
- [ ] No defined timeline or business driver
- [ ] Security review process unknown or undefined
- [ ] Champion has no budget authority
- [ ] Evaluation driven by IT only — no business stakeholder

---

## Platform Comparison Cheat Sheet

### CPaaS: Telnyx vs Twilio

| Dimension | Telnyx | Twilio |
|---|---|---|
| Pricing | Lower — private network routing | Higher — premium for brand |
| Developer Experience | Strong | Industry standard |
| Enterprise Support | Improving | Established |
| Voice AI Native Features | Strong | Strong (via Flex) |
| Best For | Cost-sensitive, technical buyers | Brand-familiar, developer-led |

### CCaaS: Genesys vs Five9 vs NICE CXone

| Dimension | Genesys Cloud | Five9 | NICE CXone |
|---|---|---|---|
| Enterprise Scale | Very High | High | Very High |
| AI Native Features | Strong (Genesys AI) | Strong | Strong (Enlighten AI) |
| Migration Complexity | High | Medium | High |
| Typical Deal Size | $500K+ | $100K–$500K | $500K+ |
| Best For | Large enterprise, complex routing | Mid-market, faster deployment | Large enterprise, WFM-heavy |
