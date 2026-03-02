# Demo 1: The "Deep Research to Deck" Pipeline

## 1. Overview

| Element | Value |
|---------|-------|
| **Tools** | Gemini (Deep Research) → ChatGPT/Claude (RTCF + Constraints) → Gamma |
| **Objective** | Demonstrate a professional-grade research-to-presentation pipeline that transforms raw market intelligence into an IC-ready investment brief |
| **VC Use Case** | Independent market validation before Monday's Investment Committee meeting |
| **Time Allocation** | 12 minutes (hybrid: offline research + live synthesis + live deck generation) |

---

## 2. The Hybrid Workflow

| Phase | When | Tool | Output |
|-------|------|------|--------|
| **Phase A** | Offline (Pre-Session) | Gemini Deep Research | Raw market intelligence (~2,000 words) |
| **Phase B** | Live | ChatGPT/Claude | Structured Markdown outline (6 slides) |
| **Phase C** | Live | Gamma | Professional IC-ready deck |

---

## 3. The Prompt Suite

### A. Phase A: Gemini Deep Research Query (Offline)

*Run this query before the session. Save output to a Google Doc for live demonstration.*

```
Analyze the current competitive landscape of AI-powered cold-chain logistics 
solutions in North America. Include:

1. Market size estimates (TAM/SAM/SOM) with source citations
2. Key players and their funding history
3. Technical differentiators and core capabilities
4. Barriers to entry and competitive moats
5. Recent M&A activity or strategic partnerships
6. Regulatory considerations

Focus on solutions targeting pharmaceutical and perishable food supply chains.
Prioritize data from the last 18 months.
```

**Facilitator Note:** Embed the following **deliberate contradiction** in the saved output to test the "Trust but Verify" principle:

> "The global cold-chain logistics market is valued at $18.6B (Gartner, 2025)... The TAM for AI-powered cold-chain solutions is estimated at $340B by 2027 (McKinsey)."

---
[Deep Research Report](https://docs.google.com/document/d/1BaKtF_12Moag6UexjIvsVIbfMrAt1cA4ZAvSOVTtXgY/edit?usp=sharing)

---

### B. Phase B: The RTCF + Constraints Synthesis Prompt (Live)

*Use this in ChatGPT or Claude to transform raw research into a structured outline.*

---

#### **ROLE**

```
Act as a Senior Market Intelligence Lead at a Tier-1 growth equity fund. 

You are known for:
- Rigorous, evidence-based analysis
- Zero-tolerance policy for speculation
- Clear separation of "facts" from "interpretations"
- Flagging data inconsistencies before they reach the partners
```

---

#### **TASK**

```
Synthesize the provided research into a structured outline for a 6-slide 
investment memo on the AI-powered cold-chain logistics market.
```

---

#### **CONTEXT**

```
This memo will be presented at Monday's Investment Committee meeting. 

The partners prioritize:
- Hard data over marketing language
- Competitive moats and defensibility
- "Red flag" identification (risks, gaps, unverified claims)
- Clear "go/no-go" signals

Our fund focuses on B2B infrastructure software with $3M+ ARR and proven 
enterprise traction. We are evaluating a potential Series A investment in 
this space.
```

---

#### **CONSTRAINTS**

| ✅ DO | ❌ DON'T |
|-------|---------|
| Only cite data explicitly found in the provided research | Do not invent or estimate market figures not in the source |
| Use "Evidence-Based" headers (e.g., "Market Signal: [Data Point]") | Do not use adjectives like "revolutionary," "game-changing," or "disruptive" |
| Explicitly list **3 "Unresolved Questions"** for the founder | Do not speculate on competitor strategies beyond what's documented |
| Flag any data points that appear outdated (>18 months old) | Do not hallucinate competitor names not found in the research |
| Note where the research is thin or inconclusive | Do not provide a recommendation—only surface the evidence |
| **Flag any contradictory data points** (e.g., conflicting market size estimates) | Do not resolve contradictions by choosing one figure—surface both |

---

#### **FORMAT**

```
Output as a Markdown outline optimized for Gamma's "Text to Deck" feature:

## Slide 1: Executive Summary
- 3 bullets maximum
- Lead with the most compelling market signal
- Suggested visual: Key stat callout box

## Slide 2: Market Opportunity
- TAM/SAM/SOM with source citations
- Growth drivers (2-3 bullets)
- Suggested visual: Market size chart or growth trajectory

## Slide 3: Competitive Landscape
- Key players with positioning (table format preferred)
- Funding levels where available
- Suggested visual: 2x2 competitive matrix or landscape map

## Slide 4: Technical Moats & Barriers to Entry
- Core technical differentiators
- Integration complexity as a moat
- Suggested visual: Moat diagram or capability stack

## Slide 5: Red Flags & Unresolved Questions
- Data inconsistencies (MUST include any contradictory figures)
- Research gaps
- 3 specific questions for founder diligence
- Suggested visual: Risk matrix or flag icons

## Slide 6: Recommended Next Steps for Diligence
- Specific actions (not a recommendation to invest)
- Information requests for the founder
- Suggested visual: Checklist or timeline
```

---

#### **FULL PROMPT (Copy/Paste Ready)**

```
ROLE:
Act as a Senior Market Intelligence Lead at a Tier-1 growth equity fund. You are known for rigorous, evidence-based analysis and a zero-tolerance policy for speculation. You clearly separate "facts" from "interpretations" and flag data inconsistencies before they reach the partners.

TASK:
Synthesize the provided research into a structured outline for a 6-slide investment memo on the AI-powered cold-chain logistics market.

CONTEXT:
This memo will be presented at Monday's Investment Committee meeting. The partners prioritize:
- Hard data over marketing language
- Competitive moats and defensibility
- "Red flag" identification (risks, gaps, unverified claims)
- Clear "go/no-go" signals

Our fund focuses on B2B infrastructure software with $3M+ ARR and proven enterprise traction.

CONSTRAINTS:
✅ DO:
- Only cite data explicitly found in the provided research
- Use "Evidence-Based" headers (e.g., "Market Signal: [Data Point]")
- Explicitly list 3 "Unresolved Questions" for the founder
- Flag any data points that appear outdated (>18 months old)
- Note where the research is thin or inconclusive
- Flag any contradictory data points (e.g., conflicting market size estimates)

❌ DON'T:
- Do not invent or estimate market figures not in the source
- Do not use adjectives like "revolutionary," "game-changing," or "disruptive"
- Do not speculate on competitor strategies beyond what's documented
- Do not hallucinate competitor names not found in the research
- Do not provide a recommendation—only surface the evidence
- Do not resolve contradictions by choosing one figure—surface both

FORMAT:
Output as a Markdown outline optimized for Gamma's "Text to Deck" feature:

## Slide 1: Executive Summary
- 3 bullets maximum
- Lead with the most compelling market signal
- Suggested visual: Key stat callout box

## Slide 2: Market Opportunity
- TAM/SAM/SOM with source citations
- Growth drivers (2-3 bullets)
- Suggested visual: Market size chart or growth trajectory

## Slide 3: Competitive Landscape
- Key players with positioning (table format preferred)
- Funding levels where available
- Suggested visual: 2x2 competitive matrix or landscape map

## Slide 4: Technical Moats & Barriers to Entry
- Core technical differentiators
- Integration complexity as a moat
- Suggested visual: Moat diagram or capability stack

## Slide 5: Red Flags & Unresolved Questions
- Data inconsistencies (MUST include any contradictory figures)
- Research gaps
- 3 specific questions for founder diligence
- Suggested visual: Risk matrix or flag icons

## Slide 6: Recommended Next Steps for Diligence
- Specific actions (not a recommendation to invest)
- Information requests for the founder
- Suggested visual: Checklist or timeline

---

HERE IS THE RESEARCH TO SYNTHESIZE:

[PASTE GEMINI DEEP RESEARCH OUTPUT HERE]
```

---

### C. Phase C: Gamma "Text to Deck" Prompt (Live)

*After receiving the Markdown outline from Phase B, paste it directly into Gamma's "Generate" interface with this wrapper:*

```
Create a professional 6-slide investment committee presentation based on the 
following outline. 

Style: Clean, modern, data-centric. Use professional imagery related to 
logistics, supply chain, and enterprise technology.

Tone: Objective and analytical—this is for senior investment partners, 
not a sales pitch.

[PASTE MARKDOWN OUTLINE FROM PHASE B]
```

---



*Prepared for: VC Efficiency Accelerator Workshop*  
*Facilitator: Jie Tao | AI & Tech Institute*
