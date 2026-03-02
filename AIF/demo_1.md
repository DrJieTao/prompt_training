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

## 4. Talking Points

### The "Why" (During Intro – 2 Minutes)

| Point | Script |
|-------|--------|
| **The Problem** | "You just got a pitch deck for an AI cold-chain logistics startup. The founder says the market is $340B. Is that real? How do you verify it before Monday's IC meeting without spending your entire weekend?" |
| **The Old Way** | "Traditionally, you'd spend 3-4 hours Googling, reading Gartner reports, and manually building slides. By Sunday night, you're exhausted and still not sure if you missed something." |
| **The New Way** | "Today, I'll show you a pipeline that takes you from 'I need to understand this market' to 'Here's my IC-ready brief' in under 15 minutes of active work." |

---

### The "How" (During Live Demo – 10 Minutes)

| Phase | Talking Point |
|-------|---------------|
| **Showing Pre-Loaded Research** | "I ran this Gemini query last night. Notice I asked for *source citations* and *recent data*. This is your first layer of quality control—garbage in, garbage out." |
| **Introducing RTCF + Constraints** | "Here's where most people stop. They'd paste this into ChatGPT and say 'summarize this.' That's the 'lazy prompt.' Watch what happens when we add structure." |
| **Walking Through Constraints** | "The Constraints section is your 'guardrail.' See this line: 'Flag any contradictory data points'? I embedded a contradiction in the research. Let's see if the AI catches it." |
| **The Audit Moment** | "Look at Slide 5. Did the AI flag the $18B vs. $340B discrepancy? If yes—the Constraints worked. If no—we just learned why human oversight matters." |
| **Pushing to Gamma** | "Now watch. This Markdown outline drops directly into Gamma. One click, and we have a deck that would have taken 2 hours to format manually." |

---

### The "So What?" (ROI Focus – 30 Seconds)

| Point | Script |
|-------|--------|
| **Time Reclaimed** | "This pipeline turns a 4-hour weekend task into 15 minutes of active work. That's 3+ hours back for founder calls, LP meetings, or—let's be honest—your family." |
| **Quality Elevated** | "More importantly, the Constraints force rigor. You're not just faster—you're catching inconsistencies that might have slipped through a manual process." |
| **Repeatable Process** | "This isn't a one-time trick. Save this prompt. Use it for every new market you need to diligence. It becomes your repeatable edge." |

---

## 5. The "Trusted Advisor" Pitfall Warnings

Deliver these during the demo at the indicated moments:

### Warning 1: The "Confidence Illusion" (During Phase A Review)

> ⚠️ "Gemini will return results with authority. But authority ≠ accuracy. See this market size figure? It looks precise. Your job is to cross-reference. If a number seems too clean, it probably is."

### Warning 2: The "Constraint Bypass" (During Phase B)

> ⚠️ "Without the DON'T rules, the AI will happily invent competitor names to fill a slide. The Constraints section is your 'guardrail.' Want proof? Remove the constraints and watch what happens—I've done it. It's not pretty."

### Warning 3: The "Aesthetic Trap" (During Phase C)

> ⚠️ "Gamma makes everything look beautiful. That's the danger. A weak thesis in a polished deck is still a weak thesis. Your job is to audit the logic, not admire the design."

---

## 6. Technical Constraints & Setup

### Pre-Session Checklist

| Task | Purpose | Status |
|------|---------|--------|
| ☐ Run Gemini Deep Research query | Generate raw material | |
| ☐ Save output to Google Doc with shareable link | Accessible on any computer | |
| ☐ Embed the **deliberate contradiction** ($18B vs. $340B) | Set up "Trust but Verify" moment | |
| ☐ Copy RTCF + Constraints prompt into a separate Google Doc | Ready for copy/paste | |
| ☐ Pre-login to Gamma in browser | Avoid login delays during demo | |
| ☐ Test full pipeline end-to-end | Ensure no surprises | |
| ☐ Prepare backup screenshots of each phase | Fallback if tools are slow | |

### In-Session Gates

| Gate | Checkpoint | Target Time |
|------|------------|-------------|
| **Gate 1** | Research displayed on screen | 0:01 |
| **Gate 2** | RTCF prompt explained and pasted | 0:05 |
| **Gate 3** | Markdown outline generated | 0:08 |
| **Gate 4** | Gamma deck visible | 0:10 |
| **Gate 5** | Audit complete (contradiction flagged?) | 0:12 |

---

## 7. Persona Hooks

| Persona | Hook During Demo |
|---------|------------------|
| **Due Diligence Deep-Diver** | "This is how you handle massive amounts of information without losing the signal in the noise. The Constraints section is your quality filter." |
| **Skeptical Partner** | "Notice I said 'surface the evidence'—not 'make a recommendation.' The AI is the analyst; you're still the decision-maker." |
| **Portfolio Supporter** | "This exact pipeline? You can teach it to your portfolio companies for competitive analysis. That's value-add beyond capital." |

---

## 8. Success Signals

| Signal | Indicator |
|--------|-----------|
| ✅ **Comprehension** | Participants can articulate the difference between a "lazy prompt" and an RTCF + Constraints prompt |
| ✅ **Execution** | At least 80% of participants have a visible Gamma deck by the 12-minute mark |
| ✅ **Critical Thinking** | At least one participant asks about the contradiction or flags a concern about data accuracy |
| ✅ **Adoption Intent** | Participants photograph the screen or ask for the prompt template |

---

## 9. Handoff to Demo 2

> "You've just seen how to go from raw research to a polished deck. But what about the *other* direction? What if you have messy IC notes and need to turn them into a visual for a partner meeting? That's where **Napkin** comes in. Let's switch gears."

---

*Prepared for: VC Efficiency Accelerator Workshop*  
*Facilitator: Jie Tao | AI & Tech Institute*
