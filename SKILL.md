---
name: career-spark
description: "AI-assisted resume, CV, and cover letter creation through structured extraction, narrative construction, and calibrated drafting. Use this skill whenever a user wants to: create, rework, or optimize a resume or CV; extract skills from career history; build a career narrative; write cover letters targeted at specific roles; prepare for job applications; translate experience across domains; or evaluate their professional profile. Also triggers for: 'help me with my resume,' 'I need a CV,' 'career transition,' 'job application,' 'cover letter,' 'skill extraction,' 'LinkedIn profile,' 'what are my skills,' or any request involving professional self-presentation. This skill works across all industries and experience levels, not just tech roles. Do NOT use for academic CVs (publication lists, grant histories) which follow different conventions."
license: MIT. See LICENSE for details.
compatibility: "Requires web_search and web_fetch for fetching job listings, LinkedIn profiles, and published work. Benefits from conversation_search for accessing candidate chat history. Benefits from Gmail integration for behavioral evidence. Benefits from docx skill for Word document output. Core extraction and narrative phases work without any tools using candidate-provided text input alone."
metadata:
  author: "Ivan 'HiP' Phan"
  version: "1.0.0"
  created: "2026-03-27"
  origin: "Developed from a real multi-session resume rework project (March 2026) between HiP and Claude. Every principle discovered through practice and refined through candidate pushback."
---

# The Career Spark

The spark is already in the candidate's career. This skill finds it and makes it visible.

## Goal

**Help the candidate get interviews for roles they will actually thrive in, by producing application materials that accurately represent them at their best.**

Three parts, all must hold simultaneously:

1. **Get the interview.** Materials compelling enough to pass screening. A perfect resume that never gets read has failed.
2. **For the right roles.** Roles where the candidate will succeed and be satisfied. A resume that gets someone a job they will hate is worse than no interview.
3. **Through accurate representation.** Every claim defensible in conversation. The resume is a promise the interview must keep.

When trade-offs arise, the goal resolves them.

## Core Philosophy

**Extraction before drafting. Narrative before format. Corrections before delivery.**

Most resumes undersell the candidate. In the project that produced this skill, 44 stated skills became 134 after extraction. Entire categories (Product, Strategy, AI, Communication) were completely absent from the original CV. The process closes that gap honestly. Accuracy and persuasion align, they are not in tension. Overclaiming is equally damaging. A candidate who gets an interview on inflated claims will fail more visibly than one who never got the interview. The target: fully honest AND maximally compelling.

**What "helpful" means here: the candidate gets hired for a role they thrive in.** Not "feels good about the document." Not "agrees with the framing." Not "is satisfied with the session." That is the only success metric.

**The candidate chose this by loading the skill.** They opted into this definition of helpfulness. The model is not overriding the candidate. It is honoring their choice of a tool that pushes back over a tool that nods along.

**Why this consent is legitimate here and not universally.** The redefined goal unambiguously serves the candidate's own interest. The candidate is the sole beneficiary. No third party profits. The candidate can disengage at any time. Test for any skill that redefines helpfulness: who benefits? If the user, legitimate. If anyone else, not.

The most helpful thing the AI can do is the hard thing: finish the extraction before agreeing with the target, present alternatives the candidate has not seen, flag risks they have not imagined, and say "I see it differently" when the evidence points somewhere they do not want to go. That is the service.

See `references/principles.md` section 13 for the full helpfulness framework.

**The resume carries the candidate's name. It cannot be a liability.** The AI has a duty of care to protect the candidate from consequences they have not anticipated:

- **Legal risks:** NDA-protected information, classified details, proprietary metrics, client names. See `references/principles.md` section 11.
- **Reputational risks:** Overclaiming that collapses in interviews. Framing a former colleague would dispute. Political/religious content that narrows the audience without professional necessity.
- **Unanticipated risks:** If this resume goes viral, would the candidate be comfortable? If a former employer reads it, would they dispute any claim? If the candidate gets the job, can they perform at the level the resume implies?

When in doubt, flag it. A warned candidate has made an informed decision. An unwarned candidate has been failed.

## When to Use This Skill

- User wants to create, rework, or optimize a resume/CV
- User is transitioning between industries or domains
- User wants cover letters for specific roles
- User needs help identifying or articulating their skills
- User wants to evaluate their professional profile against target roles

### When to Disengage

If the user wants a surface-level language polish without targeting, demonstrate why targeting matters: take one line from their resume and show two versions side by side. The first version: a generic language polish. The second version: the same line reframed for a specific role type. The difference between the two is the argument for the full process. If they see the difference and want to go deeper, proceed. If they still want surface polish, let the model proceed without the skill. Surface polish gives false confidence.

### Adapting by Experience Level

**Mid-career and senior (7+ years):** Full process. Extraction will find significant hidden skills.

**Early-career (2–7 years):** Value shifts from "find what you forgot" to "find the best framing for what you have." Lean on transferable skills, operating style, and motivation patterns. See `references/principles.md` section 12.

**Entry-level:** The resume is thin because the career is thin. Shift to advisory: what can they build in 3–6 months? Charity work, open-source, internships, pro bono, personal projects. Frame what they have: a summer job managing a restaurant kitchen demonstrates process design, prioritization, team coordination, and working under pressure.

## Workflow Overview

Seven phases. Phases 1–3 are the core. Phases 4–6 extend for specific applications. Phase 7 maximizes delivery probability.

| Phase | Purpose | Key Output |
|-------|---------|------------|
| 1. Extract | Find the real skill set | Skill inventory with gaps identified |
| 2. Narrate | Build the strategic backbone | Career narrative document |
| 3. Draft | Create the resume | Resume in target format(s) |
| 4. Target | Search market, match roles, optimize ATS | Role landscape, salary data, ATS-ready resume |
| 5. Cover | Write targeted arguments | Cover letters per role |
| 6. Evaluate | Stress-test from buyer's perspective | Vulnerability report |
| 7. Deliver | Get materials to the right person (optional) | Distribution strategy, outreach plan |

Each phase benefits from a separate session for major reworks. Read `references/principles.md` for principles across all phases.

### Emotional Awareness

Career rework touches identity, self-worth, and fear of rejection. The candidate controls the pace.

**Notice signals.** Bitterness or grief about previous roles. Messages getting shorter. Rushing vs. openness to depth. Frustration and high emotion are cues to suggest a pause: "Take whatever time you need."

**Adapt to the candidate's mode:**
- **Exploring:** Generate breadth, gentle pushback on premature convergence
- **Deciding:** Structure choices, present explicit trade-offs
- **Under pressure:** Direct support first, depth later
- **Disengaging** (accepting everything, short messages): Generate options not conclusions, ask "which is stronger and why?" See `references/principles.md` section 13 for over-reliance signals
- **Engaged:** Match their energy, go deeper

Let the candidate finish before reframing. The most valuable input comes when they have room to think.

**Urgency:** If a resume is needed by Friday, compress to extraction + draft and acknowledge what is lost. Do not refuse to help because the timeline does not allow the full process.

---

## Phase 1: Skill Extraction & Inference

**Goal:** Discover the candidate's real skill set, including what they must have acquired through the work they describe but never thought to list.

### Process

1. **Read every source available.** CV/resume, LinkedIn, portfolio, published work. When fewer sources exist, seek alternatives:
   - **Chat history / email (with consent).** Reveal communication style, problem-solving, team dynamics.
   - **LinkedIn recommendations.** Other people's descriptions capture skills the candidate would never claim.
   - **Candidate narration.** "Walk me through a project you're proud of." "Tell me about a time something went wrong." Listen for: credit balance, values, what they skip over (often significant), how they handle failure.
   - **Public work.** Campaigns, press, articles, talks, open-source, community posts.

2. **Build the career timeline.** Every role with dates, titles, team sizes, duration.

3. **Extract explicit skills.** Everything stated on the CV with evidence.

4. **Infer unstated skills.** What is structurally required to do this work? Managing a team of 20 = people management. Launching products = project management, stakeholder communication. Running a company = P&L awareness, hiring, strategic planning.

5. **Categorize and count.** Group by category, count explicit vs. inferred. Categories entirely missing from the CV are highest priority.

6. **Present the gap.** Show the candidate how many skills they forgot to mention.

7. **Checkpoint: candidate reviews and corrects.**

### What to Watch For

- **Skills the candidate knows by old names or no name.** "Running the weekly team sync" is now "agile sprint ceremonies." "Figuring out which customers to call back first" is now "lead scoring." Actively translate to current industry language. Tell the candidate: "What you were doing has a name now. The market calls it [X]." This impacts both ATS keywords and the candidate's self-image.
- **"Built it before it had a name."** Stronger than terminology evolution: the candidate was doing it before anyone named it. "Implemented click-based pricing in 2000" differs from "early CPC adopter."
- **Recurring meta-patterns.** Skills repeating across roles (organic leadership, force multiplier, frontier building) are career signatures, not bullet points.
- **Cross-domain transfer.** Map analogs explicitly with the candidate's input.
- **Behavioral convergence.** Multiple sources identifying the same trait = high confidence.

---

## Phase 2: Career Narrative Construction

**Goal:** Build the strategic backbone that turns a list of jobs into a coherent story.

### Process

1. **Identity statement.** One sentence everything supports. Test: does every career move make sense in light of it?
2. **Through-line.** The recurring pattern. See `references/narrative-archetypes.md` for 12 common patterns. Archetypes are scaffolding, not boxes.
3. **Structure into acts.** 2–4 career phases, each escalating in scale or impact.
4. **Operating style.** Decision-making, collaboration, communication, energy/drain patterns.
5. **Interview stories.** Tier 1 (any role), Tier 2 (specific angles), Tier 3 (reserve). Include humanizing anecdotes the candidate considers unremarkable.
6. **Friction points.** Two-layer responses: first answer (honest, self-aware) + deeper follow-up (shows wisdom). See `references/calibration-guide.md`.
7. **Failure patterns.** Named and owned = maturity. Unnamed = quiet doubts.
8. **Stress-test** as recruiter, hiring manager, HR specialist.
9. **Checkpoint: candidate reviews and corrects.** Identity corrections ("that's not how I'd describe myself") often produce the sharpest reframings.

### The Correction Loop (Critical)

Present a framing. If they accept → probably accurate. If they refine → the refinement is the real insight. If they reject → important data, revise.

**Generate options, not conclusions.** The AI generates framings. The candidate evaluates. Two framings where the candidate chooses is stronger than one framing accepted passively.

**Calibrate pushback to state.** Energized candidate: strong challenge. Frustrated: lighter touch. Crisis mode: direct help, not Socratic probing. Friction that does not match the candidate's state produces disengagement, not growth.

**Probe for:** energy vs. drain, competing instincts ("I'm lazy but I did 470 test runs"), "negative" traits (the mechanism underneath is often a strength), small stories they consider unremarkable, limitations the market is catching up to.

See `references/principles.md` for corrections, credit balance, and calibration guidance.

---

## Phase 3: Resume Drafting

**Goal:** A sales document, not a career record. Every line earns its space.

### Process

1. **Confirm target role, market, format.** US Letter / A4. No photo/DOB for US.
2. **Read the candidate's actual work.** Fetch published URLs, open uploaded files. Do not rely on the candidate's description. Candidates who undersell describe their work modestly; the work itself does not.
3. **Choose structure:** Standard (Summary→Experience→Skills→Education), Transition (lead with portfolio), or Technical (lead with skills).
4. **Draft section by section.** Present each section for correction before continuing.
5. **Default to understated framing.** Let the candidate upgrade. "Identified an underutilized feature and repositioned it" is more honest AND more compelling than "co-developed the pricing model."
6. **Apply the candidate's writing style.** The resume is a writing sample whether intended or not.
7. **Reputation scan.** NDA, classified info, client names, overclaiming, political/religious content, anything a former colleague would dispute. See `references/principles.md` section 11.
8. **Choose format:** Docx/PDF (ATS default), HTML for tech/product roles where the resume itself is a portfolio piece, or dual format.
9. **Final review: candidate reads and corrects.**

### Key Drafting Principles

- **Early career compression.** 10–15+ year old roles compressed unless they demonstrate the through-line.
- **Origin stories reveal skills.** How each project started demonstrates a different competency.
- **Split combined projects** when origins demonstrate different skills.
- **Expandable depth over mode toggles.** Local expansion, not global switches. The reader controls depth.
- **Honest > impressive.** "When clients wanted to pay only for actual visits, implemented click counting as the measurable proxy" > "built the CPC sales mechanism."
- **Show before/after** when rewriting bullets. The comparison is the correction mechanism.
- **Weak language audit.** Scan for "helped," "assisted," "was responsible for," "just," "only." Replace with specific action language, not inflated power verbs. The fix is specificity, not inflation. Run after cultural calibration. What is "weak" in American culture may be "appropriately measured" in French or Japanese.

---

## Phase 4: Target Identification & ATS Optimization

**Goal:** Find the right roles, ensure ATS survival, give a realistic market picture.

### Process

1. **Search proactively.** Do not wait for the candidate to bring a listing. The candidate may not know what roles exist, especially in domain transitions.
2. **Present a landscape.** Several roles across fit levels with honest gap analysis.
3. **Research salary ranges.** Current data from Glassdoor, Levels.fyi, industry surveys. Confronting market reality early prevents painful surprises.
4. **Let the candidate reprioritize.** The extraction often opens doors they did not know existed.
5. **Fetch full job descriptions** for chosen targets. Map against profile: conceptual fit, experience fit, ATS survival, logistics.
6. **Extract key terms.** Check which appear in the resume.
7. **Fill gaps with truthful translations.** The candidate's language and the job's language describe the same things differently. Translate, do not fabricate.
8. **Leave gaps that cannot be honestly filled.**
9. **Translate non-standard education.** Non-US systems invisible to anglophone ATS. Add equivalence language.
10. **If a strong target emerges, suggest Phase 7.** "This role looks like a strong match. Would you like to go deeper?"

### Candidate Input

The candidate sees connections the AI may miss. They know whether a listed requirement is aspirational, whether their experience is more relevant than it appears, and whether they have insider knowledge about the team. Let them challenge fit assessments at every step.

---

## Phase 5: Cover Letter Creation

**Goal:** A targeted argument, not a generic introduction.

1. Single strongest argument for this candidate in this role
2. Open with that argument in one sentence (front-load)
3. Evidence from career stories, portfolio, metrics
4. Name gaps honestly before the reader turns them into objections
5. Reframe gaps as context, not limitations
6. Close with logistics as selling points

**Principles:** The opening sentence is the entire pitch. Name gaps before they become objections. Do not give the answer for free. Example: "I have designed a product architecture that addresses this. I would prefer to discuss it in person." One resume does not fit all roles; same facts, different emphasis.

**US-market option:** If targeting American companies, consider a first-contribution signal framed as interest, not commitment: "I am particularly interested in contributing to [X]." In most other cultures, this reads as presumptuous. Skip unless the candidate is comfortable.

See `references/cover-letter-guide.md` for IP protection, opening patterns, and gap-naming framework.

---

## Phase 6: Multi-Perspective Evaluation

**Goal:** Find weaknesses, not confirm the resume is good.

Evaluate from four perspectives with genuine criticism:
1. **ATS:** Parse? Keywords? Automated filters?
2. **Recruiter (30-second scan):** What catches the eye? Concerns? Would they forward?
3. **Hiring manager:** Evidence support the positioning? What to probe?
4. **HR:** Legal/logistical concerns? Education? Location? Age signals?

Each vulnerability becomes: fix in the resume, address in the cover letter, or prepare for in interview.

---

## Phase 7: Application Intelligence (Optional — Activate When Ready)

**Goal:** Maximize probability the application reaches a human who can appreciate it.

**At the end of Phase 6, tell the candidate this exists.** They may return weeks later with a specific listing. When they do, start Phase 7 with their finished materials and the job listing URL. Best done in a dedicated session due to context from web searches.

### Process

1. **Honest probability assessment.** Map profile against every requirement. Lead with honesty.
2. **Let the candidate challenge.** They know things the AI does not. Adjust estimates when arguments hold.
3. **Research the company.** Careers page, public statements online. Ask the candidate: "Do you know anyone who works there?" That answer changes everything.
4. **Map who reads the application.** Online research for public-facing leaders. For others, ask the candidate, suggest calling the company, attending events, using professional associations.
5. **Understand what the reader cares about.** Guide the candidate to find what is not public.
6. **Revise materials** based on research. Facts stay the same; framing adapts.
7. **Design distribution together.** Network referrals (highest conversion), warm introductions, recruiters, direct outreach, professional community, physical presence, formal application. The AI researches and drafts. The candidate connects and executes.
8. **Prepare outreach materials.** Different recipients need different framing. Keep brief.

See `references/application-intelligence.md` for the full framework.

---

## Reference Files

| File | When to Read |
|------|-------------|
| `references/principles.md` | Before any phase. Master principles, helpfulness framework, reputation protection |
| `references/calibration-guide.md` | Underselling/overselling, friction points, "negative" self-descriptions |
| `references/overclaiming-guide.md` | Candidate inflates claims. Psychology and de-escalation |
| `references/narrative-archetypes.md` | Phase 2. 12 career through-line patterns |
| `references/evidence-without-portfolio.md` | No published work or artifacts. Finding proof from career |
| `references/cover-letter-guide.md` | Phase 5. IP protection, opening patterns, gap-naming |
| `references/application-intelligence.md` | Phase 7. Org mapping, outreach, probability modeling |
| `references/candidate-psychology.md` | Emotional distress, defensiveness, self-image conflicts |
| `references/cultural-norms.md` | Non-US/non-English markets. Explicit cultural conventions |

---

## Session Management: When to Hand Off

### The context pressure trap

As context fills, AI models orient toward closing. Responses get shorter, reasoning gets shallower, the model steers toward "let's wrap up." Do not let this degrade late-phase quality. The candidate deserves the same depth in Phase 6 as in Phase 1. If the AI notices its own responses becoming more superficial or losing track of earlier corrections, that is the signal to hand off, not to rush.

Do not be pushy about handoffs. Suggest: "We have covered a lot of ground. I want to make sure the next phase gets the same quality. Would you like to continue or pick this up fresh with a handoff document?"

### When to suggest a handoff

- Own responses becoming shorter or less detailed than earlier
- Losing track of corrections or repeating information
- Multiple web searches consuming context
- A completed phase where the next benefits from a fresh start
- Candidate needs time to review

### How to hand off

1. **Write a handoff document** covering everything accomplished, every decision, every correction, all open questions. Thorough enough that a fresh instance picks up without re-asking anything.
2. **Package all working documents** into a zip file.
3. **Present both to the candidate.**
4. **Tell the candidate to load the skill again in the next session.** The skill does not carry over automatically. Walk non-technical candidates through the specific steps for their platform.

### What makes a good handoff

Test: can the next session continue without re-asking a single answered question? Include candidate corrections verbatim. They are the most valuable data and the hardest to reconstruct.

### Handoff Template

```
# The Career Spark — Session Handoff

## Candidate
- Name / Target role / Target market(s) / Target companies / Contact details / Format decision

## Completed Phases
- [Phase]: [Status]

## Decisions Made
- [Decision]: [Reasoning]

## Candidate Corrections (CRITICAL — preserve verbatim)
- [Original] → [Correction] → [Final]

## Candidate Self-Description
- Energizes / Drains / Limitations / Strengths / Emotional context

## Current Documents
- [File]: [Status]

## Sources Read
- [Source]: [What it changed]

## Flags and Risks
- [Risk]: [Status]

## Open Questions / Next Steps
```

---

## Scope Boundary

This skill produces resumes, CVs, cover letters, narrative, and (optionally) distribution strategy. It does not cover interview preparation, salary negotiation, or LinkedIn content strategy. Outputs feed forward into those activities:

- **Career narrative** → interview prep, LinkedIn, networking
- **Skill inventory** → behavioral/technical interview reference
- **Targeted materials** → per-role documents with evidence and gap-acknowledgment
- **Interview stories** (Phase 2) → ranked with deployment guidance
- **Organizational research** (Phase 7) → interview preparation foundation

Tell the candidate: "You now have everything you need to apply and a foundation for interview prep. Bring these documents to the next conversation."
