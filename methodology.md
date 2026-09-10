# BENNETTAI211 — Methodology

**Version:** 1.0 · **Date:** 2026-09-10 · **Author:** Jameson Bennett, Bennett AI Solutions Inc. · **Contact:** jb@bennettaisolutions.tech

## 1. What this document is

A plain-language explanation of how the BENNETTAI211 awareness simulator generates its agent briefings — and, just as importantly, the compliance reasoning that defines what the platform will never claim. Written for investors, clinicians, and diligence reviewers.

## 2. The problem being solved

Consumer concern about microplastics hit a tipping point: 90% of Americans are concerned about health impacts (Ipsos/Grove, May 2025) and awareness jumped 32% since 2023 (Ocean Conservancy, 2026) — yet there is no consumer product that measures personal microplastic exposure, the DTC blood tests that exist deliver "a number, few answers" (WSJ, 2026), and the science itself is contested (WHO 2022 found little evidence of harm at current levels; 2026 peer critiques challenged several headline detection studies). BENNETTAI211 fills the gap that is actually fillable today: an awareness and education platform with sourced, dated, honestly-caveated information — not a device, not a test, not a detox product.

## 3. How the simulator computes its outputs

### 3.1 The awareness score
A preset baseline (urban commuter 55, coastal family 48, desk-worker 38, custom 45) adjusted by bottled-water habit (+15 mostly bottled, −8 mostly filtered), clamped to 10–95, rendered as an "estimated exposure" range on a LOW–HIGH gauge. The score is explicitly a model-estimated awareness range from published intake studies — not a personal measurement.

### 3.2 The five agent briefings
Each agent has a public generation rule and a sourced basis: Exposure Tracker (published intake estimates), Detox Coach (evidence-graded lifestyle guidance only — no health-outcome claims), Health Correlation (WHO 2022 + associative-not-causal labeling + 2026 critiques disclosed), Research Integration (detection studies with citations and caveats), Community Engagement (conversation starters, no advice). Every briefing carries its sources and dates inline.

## 4. Compliance reasoning (the core of the design)

- **FDA General Wellness policy** (2016 guidance): low-risk consumer wellness devices/apps making only general wellness (non-disease) claims are not subject to premarket review. BENNETTAI211's positioning — awareness, education, lifestyle guidance, no disease or diagnostic claims — sits inside this lane by design.
- **FTC Health Products Compliance Guidance** (Dec 2024): health/detox claims require competent and reliable scientific evidence. "Detox" is the most enforcement-prone claim in consumer health (Teami LLC: $15.2M judgment, 2020). The platform therefore makes no detox/removal claims at all.
- **23andMe (Chapter 11, Mar 2025)** is the cautionary tale for DTC testing models: a number without actionable, validated meaning is not a durable product.
- **Consequence:** no device, no test kit, no removal product, no diagnostic or treatment claim will appear on the platform. The current build is pure browser-based awareness content.

## 5. Limitations

- **Not a measurement.** The awareness score is model-estimated from population studies; it says nothing about any individual's actual exposure.
- **Contested science.** WHO (2022) found little evidence of harm at current levels; 2026 critiques questioned headline detection studies. The platform discloses this on every briefing rather than hiding it.
- **No consumer measurement product exists** — a real wearable/test would require years of validation and its own regulatory path.
- **No health advice.** Nothing here is medical advice; users are directed to clinicians for health questions.

## 6. Validation plan

1. User study (n=50–100) measuring comprehension: do users understand the score is an estimate, not a measurement?
2. Source audit: quarterly re-verification of every cited figure; update log published.
3. Evidence-guidance audit: every Detox Coach suggestion graded against a pre-published evidence rubric.
4. Compliance review: annual FTC/FDA-facing review of all copy; zero-claim regression test in CI.

## 7. Confidentiality

Generation rules and sources are public by design. The simulator collects no data (no accounts, no tracking). Any future user data would require explicit opt-in and published privacy terms. No PII is processed in the current build.

---

*This document accompanies the public simulator (index.html) and the rules page (algorithm.html). It is background for diligence, not medical or legal advice.*
