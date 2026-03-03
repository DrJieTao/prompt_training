# Demo 2: Napkin – "The Intelligent Handout Maker"

## 1. Overview

| Element | Value |
|---------|-------|
| **Tools** | ChatGPT/Claude/Gemini (Interview → Generate → Persona Review → Refine) → Napkin |
| **Objective** | Demonstrate advanced meta-prompting patterns (Interview + Persona Review) to transform messy IC notes into a board-ready visual infographic |
| **VC Use Case** | Post-IC meeting follow-up visual for founders and LP updates |
| **Time Allocation** | 12 minutes |
| **Patterns Introduced** | Interview Pattern, Persona-Based Review Pattern |

---

## 2. The Workflow (5 Phases)

| Phase | Pattern | Tool | Output | Time |
|-------|---------|------|--------|------|
| **A** | Interview (3 Qs) | ChatGPT/Claude | Enriched context | 2.5 min |
| **B** | Generate | ChatGPT/Claude | First draft (plain-text bullets) | 1.5 min |
| **C** | Persona Review (2 personas) | ChatGPT/Claude | Critique + improvement suggestions | 2.5 min |
| **D** | Refine | ChatGPT/Claude | Improved draft (plain-text bullets) | 1.5 min |
| **E** | Visualize | Napkin | Board-ready infographic | 3 min |
| | Buffer | | | 1 min |
| | **Total** | | | **12 min** |

---

## 3. The Input (The "Raw Material")

*Copy and provide this to participants as the starting point.*

```
IC Notes: AlphaLogistics Strategic Pivot Discussion

- Current state: Manual dispatch system, 45 enterprise clients, $3.2M ARR
- Problem: Churn increasing (18% last quarter) due to lack of real-time visibility
- Proposed pivot: "Automation-First" layer on top of existing TMS integrations
- Competitor landscape:
  - Legacy players (SAP, Oracle): High cost, 6-month implementation, full-featured
  - Point solutions (Fourkites, Project44): Real-time tracking only, no dispatch
  - AlphaLogistics opportunity: Bridge the gap—real-time + dispatch automation 
    at mid-market price
- Key risk: Engineering bandwidth—can they ship the new module by Q3?
- Board ask: $2M bridge to extend runway while pivot is validated
- Success metric: Reduce churn to <10% within 2 quarters post-launch
```

**Deliberate Ambiguity (Trust but Verify):** The notes mention "18% churn last quarter" but don't clarify if this is monthly, quarterly, or annualized. A good interview should surface this.

---

## 4. The Prompt Suite

---

### Phase A: The Interview Pattern Prompt

**Purpose:** Instead of guessing context, the AI asks targeted questions to fill gaps before generating output.

```
ROLE:
You are a Strategic Communications Advisor helping a VC investor prepare 
a visual summary for a portfolio company board meeting.

TASK:
Before generating any output, conduct a brief interview to gather critical 
context. Ask exactly 3 questions, ONE AT A TIME. Wait for my response 
before asking the next question.

INTERVIEW FOCUS AREAS:
- Audience: Who will see this visual?
- Purpose: What decision or action should it drive?
- Data Clarity: Are there any ambiguous metrics that need clarification?

CONSTRAINTS:
- Maximum 3 questions
- Each question must address a gap that would significantly impact the 
  quality of the final visual
- Do not generate any output until all 3 questions are answered
- Keep questions concise and specific

CONTEXT:
I have rough IC notes about a portfolio company's strategic pivot. I need 
to turn these into a professional visual for stakeholders.

Here are my notes:

[PASTE IC NOTES HERE]

Begin the interview now. Ask your first question.
```

---

#### Expected Interview Flow

| Question # | Expected AI Question | Pre-Scripted Answer (for live demo) |
|------------|---------------------|-------------------------------------|
| **Q1** | "Who is the primary audience for this visual—the founder/CEO, your internal partners, or external LPs?" | "Two audiences: First, a follow-up email to the CEO. Second, a slide in our LP quarterly update." |
| **Q2** | "What is the single most important message you want this visual to convey—the competitive opportunity, the risk, or the funding ask?" | "The competitive positioning—why AlphaLogistics can win the 'middle market' that legacy and point solutions ignore." |
| **Q3** | "The notes mention '18% churn last quarter'—is this monthly churn, quarterly churn, or annualized? This significantly impacts how we present the problem." | "Good catch. It's quarterly churn—so roughly 6% monthly. That's the number we should use." |

**Teaching Moment:** After Q3, pause and say: *"Notice what just happened. The AI caught an ambiguity that could have embarrassed us in front of LPs. This is why we interview before we generate."*

---

### Phase B: Generate First Draft

**Purpose:** After the interview, generate a structured plain-text output optimized for Napkin.

```
Based on my answers to your interview questions, generate a structured 
text block optimized for conversion into a visual infographic.

FORMAT:
Output as clean, plain-text bullet points organized into logical sections:

1. THE PROBLEM
   - What gap or pain point exists in the market?
   - Keep to 2-3 bullets, ≤15 words each

2. THE COMPETITIVE LANDSCAPE
   - Key players and their limitations
   - Where the opportunity lies
   - Keep to 3-4 bullets, ≤15 words each

3. THE POSITIONING
   - How the company addresses the gap
   - Current traction and proof points
   - Keep to 2-3 bullets, ≤15 words each

4. KEY METRICS
   - Critical numbers that tell the story
   - Include any clarified/corrected data from the interview
   - Keep to 3-5 bullets, ≤10 words each

5. KEY RISK & MITIGATION
   - Primary risk identified
   - How it's being addressed
   - Keep to 2 bullets, ≤15 words each

CONSTRAINTS:
- Use only information from the original notes and interview answers
- Do not invent data points not provided
- Flag any remaining ambiguities with [UNCLEAR: ...]
- Keep language crisp and visual-ready (no paragraphs, no filler words)
```

---

#### Expected First Draft Output (Example)

```
AlphaLogistics: Capturing the Mid-Market Opportunity

THE PROBLEM
- Mid-market logistics companies need real-time visibility AND dispatch automation
- Current solutions force them to choose one or the other
- Result: 6% monthly churn due to unmet needs

THE COMPETITIVE LANDSCAPE
- Legacy Players (SAP, Oracle): Full-featured but expensive, 6-month implementation
- Point Solutions (Fourkites, Project44): Real-time tracking only, no dispatch
- The Gap: No solution serves mid-market needs at mid-market price

THE POSITIONING
- AlphaLogistics bridges the gap: Real-time visibility + dispatch automation
- Right-sized for mid-market: Faster implementation, competitive pricing
- Current traction: $3.2M ARR, 45 enterprise clients

KEY METRICS
- $3.2M ARR
- 45 enterprise clients
- 6% monthly churn (corrected)
- Target: <10% quarterly churn post-pivot
- $2M bridge ask

KEY RISK & MITIGATION
- Risk: Q3 delivery dependent on engineering bandwidth
- Mitigation: Bridge funding extends runway for focused execution
```

---

### Phase C: The Persona-Based Review Prompt

**Purpose:** Before finalizing, the AI critiques its own output through multiple stakeholder lenses to catch blind spots.

```
Now review the draft you just created by assuming TWO different personas, 
one at a time. For each persona, provide specific, actionable feedback 
based strictly on that stakeholder's priorities and concerns.

---

PERSONA 1: The Skeptical GP

Background: Senior partner who has seen hundreds of portfolio updates.

Priorities:
- Risks must be clearly stated, not buried or softened
- Metrics must be verified and sourced
- No spin, no marketing language
- Visuals should not hide bad news behind pretty design

Your task: Review the draft through this lens. Identify 2-3 specific 
weaknesses and suggest 1-2 improvements based on YOUR priorities above.

---

PERSONA 2: The Portfolio Company CEO (The Recipient)

Background: Founder receiving this visual after the board meeting.

Priorities:
- Wants to feel heard, not judged
- Needs clarity on what the board actually decided
- Wants alignment on next steps and the funding ask
- Sensitive to how problems are framed (partnership vs. report card)

Your task: Review the draft through this lens. Identify 2-3 specific 
weaknesses and suggest 1-2 improvements based on YOUR priorities above.

---

After both reviews, synthesize the feedback into a PRIORITIZED LIST of 
the top 3 improvements to make. These must be derived directly from the 
persona critiques above—do not add generic suggestions.
```

---

#### Expected Persona Review Output (Example)

```
PERSONA 1: The Skeptical GP

Critiques:
1. "The engineering bandwidth risk is mentioned but not quantified. What's 
   the probability of missing Q3? What's the fallback plan?"
2. "The $2M bridge ask is listed but not contextualized. What's the current 
   runway? When does the money run out without the bridge?"
3. "The 'mid-market opportunity' framing feels like marketing. Where's the 
   evidence that this segment is underserved?"

Suggestions:
- Add runway context: "Current runway: X months. Bridge extends to Y months."
- Include a "Key Assumptions" or "What Must Be True" section for rigor.

---

PERSONA 2: The Portfolio Company CEO

Critiques:
1. "The churn framing leads with our failure. Can we reframe as 'the problem 
   we're solving' rather than 'our problem'?"
2. "I want to see the success metric more prominently—it shows we have a 
   clear target, not just a vague pivot."
3. "The visual should feel like a partnership document, not a report card 
   on our performance."

Suggestions:
- Lead with the market opportunity, not the churn problem.
- Make the <10% churn target a prominent element to show clear success criteria.

---

SYNTHESIZED TOP 3 IMPROVEMENTS:

1. Reframe the narrative: Lead with "the market gap we're solving" rather 
   than "our churn problem" (addresses CEO concern, maintains GP rigor)
2. Add runway context to the funding ask: "Current runway: X months. Bridge 
   extends to Y months." (addresses GP concern)
3. Make the success metric (<10% churn target) more prominent to show clear, 
   measurable goals (addresses both personas)
```

---

### Phase D: Refine Based on Feedback (Context-Dependent)

**Purpose:** Incorporate the improvements identified in Phase C and regenerate the output.

```
Now incorporate the top 3 improvements identified in the persona review 
above and regenerate the structured text block.

INSTRUCTIONS:
- Reference the specific improvements synthesized from the Skeptical GP 
  and CEO personas in the previous step
- Each change must trace directly to a persona critique
- Do not add generic improvements not derived from the persona feedback
- Maintain the same plain-text bullet format optimized for Napkin

OUTPUT FORMAT:
Regenerate the full structured text block with improvements incorporated.

After the revised text block, include a brief CHANGE LOG that maps each 
revision to the persona feedback that drove it:
- Change 1: [Description] ← Driven by [Persona] concern about [Issue]
- Change 2: [Description] ← Driven by [Persona] concern about [Issue]
- Change 3: [Description] ← Driven by [Persona] concern about [Issue]
```

---

#### Expected Refined Output (Example)

```
AlphaLogistics: Capturing the Mid-Market Opportunity

THE MARKET GAP
- Mid-market logistics companies need real-time visibility AND dispatch automation
- Legacy solutions are overkill; point solutions are incomplete
- No current player serves this segment at the right price point

THE COMPETITIVE LANDSCAPE
- Legacy Players (SAP, Oracle): Full-featured, 6-month deploy, enterprise pricing
- Point Solutions (Fourkites, Project44): Tracking only, no dispatch capability
- AlphaLogistics Opportunity: Bridge the gap for underserved mid-market

THE POSITIONING
- Real-time visibility + dispatch automation in one platform
- Right-sized implementation and pricing for mid-market
- Current traction: $3.2M ARR, 45 enterprise clients

KEY METRICS
- $3.2M ARR | 45 enterprise clients
- Current churn: 6% monthly
- Success target: <10% quarterly churn within 2 quarters post-launch
- Bridge ask: $2M (extends runway from 4 months to 12 months)

KEY RISK & MITIGATION
- Risk: Q3 delivery dependent on engineering bandwidth
- Mitigation: Bridge funding provides 8 additional months for focused execution

---

CHANGE LOG:
- Change 1: Renamed "THE PROBLEM" to "THE MARKET GAP" and reframed language 
  ← Driven by CEO concern about leading with failure
- Change 2: Added runway context to bridge ask (4 months → 12 months) 
  ← Driven by GP concern about uncontextualized funding request
- Change 3: Made success target (<10% churn) a prominent, measurable element 
  ← Driven by both personas wanting clear success criteria
```

**Facilitator Note:** Before pushing to Napkin, remove the CHANGE LOG section—it's for learning purposes only.

---

### Phase E: Napkin Visualization

**Purpose:** Paste the refined plain-text output into Napkin to generate a professional infographic.

#### How Napkin Works

| Input | Output |
|-------|--------|
| Plain text (paragraphs or bullet points) | Auto-generated infographic options |
| No prompts, no styling instructions | Napkin interprets structure and suggests visual formats |

#### Step-by-Step Workflow

| Step | Action | Facilitator Note |
|------|--------|------------------|
| **1. Copy Text** | Copy the refined text block from Phase D (without the CHANGE LOG) | Clean bullets only |
| **2. Open Napkin** | Navigate to Napkin's editor (napkin.ai) | Ensure logged in |
| **3. Paste Text** | Paste directly into the text editor | No formatting needed |
| **4. Generate** | Click "Spark" or the auto-generate icon | Napkin reads the text structure |
| **5. Browse Options** | Review 3-4 suggested visual formats | Comparison, flowchart, matrix, etc. |
| **6. Select Style** | Choose the format that best tells your story | For competitive positioning: side-by-side or matrix |
| **7. Polish** | Adjust colors to professional palette (navy, white, accent) | 30 seconds max |
| **8. Export** | "Copy as Image" or download PNG/SVG | Ready for email or deck |

#### Talking Point During Phase E

> "Notice we didn't tell Napkin *how* to visualize this. We just gave it clean text—bullet points describing the market gap, the landscape, and our positioning. Napkin reads the structure and suggests visual formats. Your job is to pick the one that tells your story best."

---

## 5. The "Follow-Along" Steps

| Step | Action | Facilitator Note | Time |
|------|--------|------------------|------|
| **1. Set the Scene** | "You have messy IC notes. The old way: paste and pray. The new way: Interview → Generate → Review → Refine → Visualize." | Frame the 5-phase workflow on a slide | 30 sec |
| **2. Launch Interview** | Paste the Interview Pattern prompt + IC notes into ChatGPT/Claude | "Watch—it asks US questions instead of guessing" | 30 sec |
| **3. Answer Q1** | Respond: "Two audiences: CEO follow-up email and LP quarterly slide." | Participants observe | 30 sec |
| **4. Answer Q2** | Respond: "The competitive positioning—why AlphaLogistics wins the middle market." | Participants observe | 30 sec |
| **5. Answer Q3** | Respond: "Good catch. It's quarterly churn—so roughly 6% monthly." | **Teaching moment:** "The AI caught the ambiguity!" | 30 sec |
| **6. Generate First Draft** | Paste the Generate prompt (or AI auto-generates) | "Already better than a blind paste—but we're not done" | 1 min |
| **7. Review First Draft** | Skim the plain-text output | Point out the structure | 30 sec |
| **8. Trigger Persona Review** | Paste the Persona Review prompt | "Now the AI critiques itself through two lenses" | 30 sec |
| **9. Read GP Critique** | Highlight: "The GP wants runway context and risk quantification" | Show on screen | 45 sec |
| **10. Read CEO Critique** | Highlight: "The CEO wants reframing—partnership, not report card" | Show on screen | 45 sec |
| **11. Show Synthesis** | Read the top 3 improvements | "These are our marching orders—derived from the personas" | 30 sec |
| **12. Refine** | Paste the Refine prompt | "One more pass with targeted improvements" | 1 min |
| **13. Review Refined Output** | Show the CHANGE LOG | "Every change traces to a persona critique" | 30 sec |
| **14. Push to Napkin** | Copy text (without CHANGE LOG), paste into Napkin | Click "Spark" to generate | 1 min |
| **15. Select Style** | Browse 2-3 visual options | Let participants see choices | 1 min |
| **16. Quick Polish** | Adjust colors to navy/professional | "30 seconds of polish" | 30 sec |
| **17. Export** | "Copy as Image" for email/deck | "Board-ready in 12 minutes" | 30 sec |
| **Buffer** | Catch-up for stragglers | Troubleshoot any issues | 1 min |

---

## 6. Talking Points

### The "Why" (During Intro – 1 Minute)

| Point | Script |
|-------|--------|
| **The Problem** | "We've all left an IC meeting with notes that look like a crime scene. Usually, these sit in a folder until someone asks for a 'quick visual' at 5pm on Friday." |
| **The Old Way** | "You'd spend an hour in PowerPoint, realize you forgot a key point, redo it, then send it to the founder who says 'this doesn't capture what we discussed.'" |
| **The New Way** | "Today, I'll show you a workflow that interviews you, generates a draft, critiques itself, refines, and visualizes—all in 12 minutes." |

---

### The "How" (During Live Demo – 9 Minutes)

| Phase | Talking Point |
|-------|---------------|
| **Interview Pattern** | "Notice the AI is asking US questions. This is the Interview Pattern. Instead of guessing your context, it extracts it. Three questions, maximum signal." |
| **The Ambiguity Catch** | "Did you see that? It asked about the churn metric. '18% last quarter' is ambiguous. The AI caught it before we embarrassed ourselves in front of LPs." |
| **First Draft** | "This is already better than a blind paste. But here's the key insight: the AI doesn't know if this will land with your GP or your founder. So we ask it to check." |
| **Persona Review** | "This is the Persona Review Pattern. We're asking the AI to critique its own work through two lenses: a skeptical GP and the founder who'll receive this." |
| **The Tension** | "Notice the GP wants more risk disclosure. The CEO wants softer framing. These are real tensions you navigate every day. The AI surfaced them before the meeting." |
| **Context-Dependent Refinement** | "Look at the Refine prompt—we didn't hard-code the improvements. We pointed the AI to 'the top 3 improvements identified above.' Your personas might give different feedback; the refinement adapts." |
| **Napkin Magic** | "Now watch. This plain text drops into Napkin. It reads the structure—sections, bullets, metrics—and suggests visual formats. We didn't design anything; we just wrote clearly." |

---

### The "So What?" (ROI Focus – 1 Minute)

| Point | Script |
|-------|--------|
| **Time Reclaimed** | "This workflow turns a 2-hour Friday panic into 12 minutes of structured work. That's time back for founder calls or, let's be honest, your weekend." |
| **Quality Elevated** | "More importantly, you caught the churn ambiguity AND pre-tested the visual with two stakeholder personas. That's not just faster—it's better." |
| **Repeatable Process** | "Save these prompts. Use them for every IC follow-up, every board visual, every LP slide. It becomes your repeatable edge." |

---

## 7. The "Trusted Advisor" Pitfall Warnings

Deliver these during the demo at the indicated moments:

### Warning 1: The "Interview Fatigue" Risk (After Q3)

> ⚠️ "Three questions is the sweet spot. More than five and you've lost the efficiency gain. The Interview Pattern is about *targeted* context extraction, not a full discovery session. If you need more than five questions, your input material is too vague—fix that first."

### Warning 2: The "Echo Chamber" Risk (During Persona Review)

> ⚠️ "The personas are only as good as you define them. If both personas have the same priorities, you'll get redundant feedback. Choose personas with *tension*—like a skeptical GP who wants risk disclosure and a founder who wants partnership framing. That tension is where the insight lives."

### Warning 3: The "Refinement Loop" Risk (After Phase D)

> ⚠️ "One refinement pass is usually enough. If you keep looping—review, refine, review, refine—you'll over-engineer the output and lose the efficiency gain. Ship it, get real human feedback, iterate later. Perfectionism is the enemy of done."

### Warning 4: The "Garbage Text, Garbage Visual" Risk (Before Phase E)

> ⚠️ "Napkin is only as good as the text you feed it. If your bullets are vague or disorganized, the infographic will be too. That's why we spent time in Phases A-D structuring the content. The Interview and Persona Review weren't just about the AI—they were about giving Napkin clean input."

---

## 8. Technical Constraints & Setup

### Pre-Session Checklist

| Task | Purpose | Status |
|------|---------|--------|
| ☐ Copy IC notes into a Google Doc | Ready for participants to access | |
| ☐ Pre-write all prompts (A, B, C, D) in a separate Google Doc | Easy copy/paste on unfamiliar computer | |
| ☐ Pre-script answers to the 3 interview questions | Smooth live demo flow | |
| ☐ Pre-login to Napkin in browser | Avoid login delays | |
| ☐ Test full 5-phase workflow end-to-end | Ensure no surprises | |
| ☐ Prepare backup screenshots of each phase | Fallback if tools are slow | |
| ☐ Confirm Napkin free tier allows export | No paywall interruption | |

### In-Session Gates

| Gate | Checkpoint | Target Time |
|------|------------|-------------|
| **Gate 1** | Interview prompt pasted, Q1 received | 0:01 |
| **Gate 2** | All 3 questions answered | 0:03 |
| **Gate 3** | First draft visible | 0:05 |
| **Gate 4** | Persona Review prompt pasted | 0:06 |
| **Gate 5** | Both persona critiques visible | 0:08 |
| **Gate 6** | Refined output generated | 0:10 |
| **Gate 7** | Napkin visual generated | 0:11 |
| **Gate 8** | Export demonstrated | 0:12 |

---

## 9. Persona Hooks

| Persona | Hook During Demo |
|---------|------------------|
| **Due Diligence Deep-Diver** | "The Interview Pattern works for diligence too. Before synthesizing a market report, have the AI ask you: 'What's the investment thesis? What risks are you most concerned about?' Targeted context, better output." |
| **Skeptical Partner** | "Notice the AI didn't just accept the notes at face value. It asked about the churn metric, then the Persona Review caught the missing runway context. That's the rigor you want from your team—now it's built into the workflow." |
| **Portfolio Supporter** | "The Persona Review is your 'pre-flight check.' You're simulating stakeholder reactions before the real meeting. The founder won't be surprised; the GP won't ask 'where's the risk?' You've already stress-tested it." |

---

## 10. The Meta-Lesson

> "Demo 1 showed you how to go from research to deck using RTCF + Constraints. Demo 2 shows you two new patterns: **Interview** and **Persona Review**. You're not writing prompts anymore—you're **directing workflows**. The AI asks questions, generates, critiques itself, and refines. Your job is to be the architect, not the typist."

---

## 11. Success Signals

| Signal | Indicator |
|--------|-----------|
| ✅ **Comprehension** | Participants can articulate the difference between "paste and pray" and the Interview Pattern |
| ✅ **Pattern Recognition** | At least one participant says "I could use the Persona Review for [X]" |
| ✅ **Execution** | 80%+ of participants have a visible Napkin visual by the 12-minute mark |
| ✅ **Critical Thinking** | Someone asks about choosing the right personas or handling conflicting feedback |
| ✅ **Adoption Intent** | Participants photograph the screen or ask for the prompt templates |

---

## 12. Handoff to Demo 3 (NotebookLM Teaser)

> "You've now seen two patterns: Interview and Persona Review. But what if you need to query *existing* knowledge—dozens of pitch decks, market reports, or policy documents—without re-uploading them every time? That's where NotebookLM comes in. Quick 2-minute preview of what's possible."

---

*Prepared for: VC Efficiency Accelerator Workshop*  
*Facilitator: Jie Tao | AI & Tech Institute*
