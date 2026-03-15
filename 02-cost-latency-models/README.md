# Cost and Latency Models

Frameworks for modeling the real cost and latency profile of
enterprise Voice AI deployments. Built from experience with
$100K–$500K deals across financial services, healthcare,
and large enterprise contact centers.

---

## Latency Budget Framework

End-to-end conversational latency is the most common technical
objection in Voice AI deals. Buyers feel latency before they
measure it. A response that feels natural is under 1,200ms
total. Anything over 1,500ms generates complaints.

### Latency Budget Breakdown

| Component | Best Case | Typical | Degraded |
|---|---|---|---|
| Network / SIP | 20ms | 40ms | 80ms+ |
| STT (first word) | 200ms | 350ms | 600ms+ |
| LLM (first token) | 300ms | 600ms | 1,200ms+ |
| TTS (first audio) | 100ms | 200ms | 400ms+ |
| Playback buffer | 50ms | 100ms | 200ms+ |
| **Total** | **670ms** | **1,290ms** | **2,480ms+** |

**The real problem:** Latency compounds. A degraded STT
combined with a slow LLM response will break the
conversational experience entirely — even if TTS is fast.

### What Drives Latency Spikes

- STT: High concurrency, long audio segments, accented speech
- LLM: Prompt length, model size, cold starts, rate limits
- TTS: First-chunk generation time, audio format conversion
- Network: Geographic distance between services, SIP re-routing

---

## Cost Model: Voice AI at Scale

### Per-Minute Cost Breakdown

Modeled at 100,000 minutes/month — a realistic mid-market
enterprise contact center volume.

| Component | Vendor Example | Cost per Minute |
|---|---|---|
| SIP Trunking | Telnyx | $0.004 |
| STT | Deepgram (streaming) | $0.0125 |
| LLM | GPT-4o (avg 500 tokens) | $0.015 |
| TTS | ElevenLabs (turbo) | $0.008 |
| Infrastructure | Hosting / orchestration | $0.005 |
| **Total** | | **~$0.044 / min** |

**At 100,000 minutes/month:** ~$4,400/month in AI infrastructure
costs before platform fees, support, or CCaaS licensing.

### Cost Comparison: AI Agent vs Human Agent

| Model | Cost per Hour | Notes |
|---|---|---|
| Human agent (fully loaded) | $25–$45 | Salary, benefits, overhead |
| AI voice agent | $2.50–$4.00 | Infrastructure + platform |
| Blended (AI + escalation) | $8–$15 | 60% AI containment assumed |

**The buyer conversation:** AI voice agents are not free.
The ROI case is built on containment rate, handle time
reduction, and after-hours coverage — not pure cost
elimination.

---

## Vendor Cost Comparison

### STT Vendors

| Vendor | Streaming Price | Accuracy (English) | Latency |
|---|---|---|---|
| Deepgram Nova-2 | $0.0125/min | High | Low |
| Assembly AI | $0.015/min | High | Medium |
| Google STT | $0.016/min | High | Medium |
| AWS Transcribe | $0.024/min | Medium | Medium |

### TTS Vendors

| Vendor | Price | Voice Quality | Latency |
|---|---|---|---|
| ElevenLabs Turbo | $0.008/min | Very High | Low |
| Google Wavenet | $0.006/min | High | Low |
| AWS Polly Neural | $0.004/min | Medium | Very Low |
| OpenAI TTS | $0.015/min | High | Medium |

---

## Common Cost Modeling Mistakes

**Mistake 1 — Modeling at low volume**
Vendors offer volume discounts that change the math significantly
above 500K minutes/month. Always model at realistic peak volume.

**Mistake 2 — Ignoring failed containment**
Every call the AI cannot handle escalates to a human agent.
A 70% containment rate means 30% of calls still require full
human handle time. Model the blended cost, not the AI-only cost.

**Mistake 3 — Excluding orchestration infrastructure**
The middleware that connects STT, LLM, TTS, and telephony
has real infrastructure cost. Budget 10–15% of AI costs
for orchestration and reliability overhead.

**Mistake 4 — Using list pricing**
Enterprise contracts for Telnyx, Twilio, Genesys, and Five9
are negotiated. List pricing overstates cost by 20–40%
at meaningful volume. Always qualify budget against
negotiated rates.
