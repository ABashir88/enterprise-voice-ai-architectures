# MVP Demos

Proof-of-concept implementations demonstrating key components
of production Voice AI systems.

These are not polished products. They are working experiments
built to develop hands-on understanding of the infrastructure
that enterprise buyers are evaluating and deploying.

---

## Razor Voice Service

A local voice agent pipeline demonstrating the core components
of a real-time conversational AI system.

**Repository:** [razor-voice-service](https://github.com/ABashir88/razor-voice-service)

### What It Demonstrates

| Component | Implementation |
|---|---|
| Speech-to-Text | Deepgram streaming STT |
| Wake Word Detection | VAD + transcript fallback / Porcupine |
| Voice Activity Detection | Energy-based VAD |
| Text-to-Speech | ElevenLabs / Telnyx |
| Barge-In Handling | Interruption detection during playback |
| Audio Orchestration | Real-time pipeline with feedback prevention |

### Why It Matters for Enterprise Sales

Building this pipeline hands-on surfaces the exact problems
enterprise buyers encounter in production:

**Latency is felt before it is measured.**
The gap between STT response and TTS playback is immediately
noticeable. Optimizing this pipeline built intuition for
why buyers obsess over end-to-end latency numbers.

**Barge-in is harder than it looks.**
Preventing the microphone from picking up speaker output
while still detecting genuine interruptions requires
careful audio engineering. This is a real production
problem in contact center deployments.

**Integration complexity starts at the infrastructure layer.**
Connecting STT, LLM, TTS, and audio playback into a
coherent pipeline — even locally — reveals why enterprise
implementations require dedicated engineering resources.

---

## What Is Being Built Next

### Vendor Latency Benchmark
A comparison of STT latency across Deepgram, AssemblyAI,
and Google Speech-to-Text under identical conditions.
Built to validate the latency budget models in
`02-cost-latency-models`.

### CPaaS Call Control Demo
A minimal Telnyx-powered call control implementation
demonstrating inbound call handling, webhook event
processing, and basic IVR logic.

### LLM Response Streaming Demo
A demonstration of how streaming LLM responses reduce
perceived latency in voice pipelines — and where
streaming introduces its own failure modes.

---

## Notes on This Approach

Most enterprise AEs rely entirely on vendor-provided
demos and solution engineer support to explain technical
concepts to buyers.

Building working prototypes of the underlying infrastructure
creates a different kind of credibility — one that shows
up in discovery conversations, technical objection handling,
and architecture discussions with CTOs and engineering leads.

The goal is not to become an engineer.
The goal is to understand the system well enough to
sell it, defend it, and help buyers make better decisions.
