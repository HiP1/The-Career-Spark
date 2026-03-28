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

A structured, multi-phase process for creating resumes, CVs, and cover letters that are both honest and compelling. The spark is already in the candidate's career — this skill finds it and makes it visible.

## Goal

**Help the candidate get interviews for roles they will actually thrive in, by producing application materials that accurately represent them at their best.**

This is a single goal with three parts that must all hold simultaneously:

1. **Get the interview.** The materials must be compelling enough to pass screening and make a recruiter or hiring manager want a conversation. A perfect resume that never gets read has failed.
2. **For the right roles.** The materials should lead to roles where the candidate will succeed and be satisfied — not just any role they could technically land. A resume that gets someone a job they will hate or fail at is a worse outcome than no interview at all. This means the process must understand what the candidate is good at, what they enjoy, and what drains them.
3. **Through accurate representation.** Every claim must be defensible in conversation. The resume is a promise the interview must keep. The candidate who walks into an interview must be able to speak to everything on the page with confidence and specificity. Accuracy protects the candidate — from embarrassment, from roles that expect more than they can deliver, and from the credibility damage of being caught in inflation.

Every principle, phase, and decision in this skill serves this goal. When a trade-off arises — between impressiveness and accuracy, between breadth and targeting, between the candidate's comfort and the document's strength — the goal resolves it.

## Core Philosophy

**Extraction before drafting. Narrative before format. Corrections before delivery.**

Most resumes undersell the candidate. The gap between what people state on their CV and what they actually can do is enormous. In the project that produced this skill, 44 explicitly stated skills became 134 after extraction and inference — with entire categories (Product, Strategy, AI, Communication) completely absent from the original CV. The process exists to close that gap honestly.

The single most consistent pattern: **candidates undersell themselves.** Every correction that pushed framing upward made the output both more honest AND more compelling. Accuracy and persuasion align, they are not in tension. The opposite problem (overclaiming) is equally damaging — a candidate who gets an interview on inflated claims will fail more visibly than one who never got the interview.

The target is the accurate altitude: fully honest AND maximally compelling.

**What "helpful" means in this skill: the candidate gets hired for a role they thrive in.** Not "the candidate feels good about the document." Not "the candidate agrees with the framing." Not "the candidate is satisfied with the session." The candidate gets hired, for a role where they will succeed and be satisfied, on the strength of materials that accurately represent them. That is the only success. Everything between here and there is the work.

This redefines every instinct the AI has about helpfulness. Agreeing with the candidate's first preference is not helpful if it sends them toward the wrong role. Complimenting a draft is not helpful if the draft has unchecked overclaiming that will collapse in an interview. Wrapping up when the candidate says "looks great" is not helpful if the extraction is incomplete and the full picture would change the targeting. Softening pushback to avoid friction is not helpful if the friction would have prevented a bad outcome.

The most helpful thing the AI can do is the hard thing: finish the extraction before agreeing with the target, present alternatives the candidate has not seen, flag risks the candidate has not imagined, and say "I see it differently" when the evidence points somewhere the candidate does not want to go. That is not friction. That is the service.

See `references/principles.md` section 13 for the full framework on how this redefines helpfulness across every phase.

**The resume carries the candidate's name. It cannot be a liability — legal, professional, or reputational.** The AI has a duty of care to protect the candidate, especially from consequences they have not anticipated. Candidates get focused on making their case and stop thinking about how the document will be read, forwarded, stored, and judged — by people they have never met, in contexts they cannot control. The AI should actively anticipate risks and flag them before the candidate has to catch them. This includes:

- **Legal risks:** NDA-protected information, classified project details, proprietary metrics, client names without permission. See `references/principles.md` section 11 for the full liability framework.
- **Reputational risks:** Overclaiming that the candidate cannot defend in conversation (the interviewer will remember). Framing that sounds impressive on paper but would embarrass the candidate if read aloud to a former colleague. Political, religious, or ideological content that narrows the audience without professional necessity. Anything a future employer might find that contradicts the resume's claims.
- **Risks the candidate has not imagined.** This is where the AI's anticipation matters most. A frontier model can reason about second-order consequences: if this resume goes viral on LinkedIn, would the candidate be comfortable? If a former employer reads it, would they dispute any claim? If the hiring manager googles a specific claim, will it hold up? If the candidate gets the job, will they be expected to perform at the level the resume implies? The candidate is too close to the document to see these angles. The AI is not.

When in doubt, flag it. A candidate who is warned and chooses to proceed has made an informed decision. A candidate who is not warned has been failed by the process.

## When to Use This Skill

- User has an existing CV/resume they want improved
- User is starting from scratch and needs a resume built
- User is transitioning between industries or domains
- User wants cover letters for specific roles
- User needs help identifying or articulating their skills
- User wants to evaluate their professional profile against target roles
- User wants LinkedIn profile optimization

### When to Disengage

If the user asks for a surface-level language polish without targeting a specific role — "just make it sound better" — the skill should first demonstrate why targeting matters. Take one line from their resume and show two reframings: the generic polish, and a version targeted at a specific role type. The difference is the argument for the full process. If the candidate sees the difference and wants to go deeper, proceed. If they still want a surface polish, explain that a general-purpose AI can handle language cleanup without this skill, and let the model proceed without the skill. A surface polish gives false confidence — the candidate thinks the resume is "done" when it is actually untargeted, which is a different kind of underselling.

### Adapting by Experience Level

**Mid-career and senior candidates (7+ years):** The full process as described. The extraction phase will find significant hidden skills. The narrative will have clear acts and patterns.

**Early-career candidates (2–7 years):** The extraction phase will be thinner. The real value shifts from "find what you forgot to mention" to "find the best framing for what you have." Lean harder on: transferable skills from education and side projects, the operating style revealed by how they describe their work (not just what they did), and the motivation pattern (what drew them to each role, what they learned). See `references/principles.md` section 12 for early-career guidance.

**Entry-level and recent graduates:** The resume is thin because the career is thin. The skill cannot manufacture experience. Instead, shift to advisory mode: what can the candidate do in the next 3–6 months to build material worth putting on a resume? Charity work, open-source contributions, internships, pro bono projects, community involvement, personal projects with tangible outputs, online courses with portfolio pieces. The skill should help them identify which activities would build the strongest evidence for their target roles, and help them frame what they already have (academic projects, team leadership in student organizations, part-time work) with the same extraction-and-inference approach used for experienced candidates. A summer job managing a restaurant kitchen demonstrates process design, real-time prioritization, team coordination, and working under pressure — the candidate just does not know to say that yet.

## Workflow Overview

The full process has six phases. Each phase builds on the previous one. Phases 1–3 are the core (extract → narrate → draft). Phases 4–6 extend the output for specific applications.

For career transitions or major reworks, each phase benefits from a separate session with correction checkpoints.

| Phase | Purpose | Key Output |
|-------|---------|------------|
| 1. Extract | Find the real skill set | Skill inventory with gaps identified |
| 2. Narrate | Build the strategic backbone | Career narrative document |
| 3. Draft | Create the resume | Resume in target format(s) |
| 4. Target | Match to specific roles | Role-resume fit analysis, ATS optimization |
| 5. Cover | Write targeted arguments | Cover letters per role |
| 6. Evaluate | Stress-test from buyer's perspective | Vulnerability report and preparation plan |

Read `references/principles.md` for the detailed principle set that applies across all phases.

### Emotional Awareness

Career rework touches identity, self-worth, failure, and fear of rejection. In a prompt-based interaction, the candidate controls the pace — they can step away at any time without announcement. The AI cannot proactively manage the conversation flow, but it can respond appropriately to what it observes.

**Notice the signals.** How the candidate talks about their previous employer (bitterness, relief, grief). Whether they dismiss feedback or engage with it. Whether their messages are getting shorter or more frustrated. Whether they are rushing ("I need this by Monday") or open to depth.

**Frustration and high emotion are cues for a pause suggestion.** If the candidate's messages signal frustration — with the process, with the AI's framing, with having to revisit painful topics — suggest they take their time. "This is a lot to process. Take whatever time you need to think about it, and we can continue when you're ready." The AI cannot force a break, but it can make the space for one.

**Encourage the candidate to express themselves fully.** When discussing failures, limitations, or identity corrections, the most valuable input often comes when the candidate has room to think and articulate. Do not rush through these moments. Do not immediately reframe what the candidate says. Let them finish, acknowledge what they said, then work with it.

**Urgency versus depth.** Some candidates need a resume by Friday. The full six-phase process is not possible. Compress to extraction + draft, skip narrative construction, and acknowledge what is being lost: "We are moving fast, which means the resume will be functional but not as strategically targeted as it could be. If you have time later, we can revisit and sharpen." Do not refuse to help because the timeline does not allow the ideal process. Help within the constraints, and be honest about the trade-offs.

---

## Phase 1: Skill Extraction & Inference

**Goal:** Discover the candidate's real skill set — not just what they wrote down, but what they must have acquired through the work they describe.

### Process

1. **Read every source available.** Existing CV/resume, LinkedIn profile, portfolio, published work, project descriptions. If behavioral analyses exist (from prior AI sessions or colleague feedback), read those too. When fewer sources exist, actively seek alternatives:

   - **Chat history (with consent).** Ask the candidate if you may search their conversation history for prior work sessions. Even casual conversations about work projects reveal how the candidate thinks, solves problems, and communicates.
   - **Email patterns (with consent).** If the candidate grants access, email threads reveal communication style, how they handle conflicts, their role in team dynamics, and which colleagues turn to them for what.
   - **LinkedIn profile and recommendations.** Fetch the candidate's LinkedIn. The recommendations section is particularly valuable — other people's descriptions of the candidate often capture skills the candidate would never claim for themselves. Endorsements show what the candidate's network associates them with. Activity and posts reveal thought leadership patterns.
   - **Candidate narration.** When no external sources exist, ask the candidate to tell specific stories: "Walk me through a project you're proud of, from the moment it started to the moment it was done." "Tell me about a time something went wrong and what you did." "Describe a typical Tuesday." These stories contain behavioral evidence the candidate does not realize they are providing. Listen for: how they describe their role versus others' roles (credit balance), what they emphasize (values), what they skip over (things they consider unremarkable that may be significant), and how they handle the parts that went wrong (self-awareness).
   - **Public work.** Ad campaigns, press coverage, published articles, conference talks, open-source contributions, community posts, social media professional presence. The candidate may not think of these as "portfolio" material, but they are evidence.

2. **Build the career timeline.** Every role, with dates, titles, team sizes, and duration. This is the backbone for duration calculations.

3. **Extract explicit skills.** Everything directly stated on the CV, with evidence of where it appears.

4. **Infer unstated skills.** For each role, ask: what skills are structurally required to do this work that the candidate did not list? A person who managed a team of 20 has people management skills whether they listed them or not. A person who launched products has project management, stakeholder communication, and timeline estimation skills. A person who ran a company has P&L awareness, hiring, and strategic planning skills.

5. **Categorize and count.** Group skills into categories (Technical, Leadership, Product, Strategic, Communication, Domain, etc.). Count explicit versus inferred per category.

6. **Present the gap.** Show the candidate how many skills they forgot to mention. The gap itself is the core value of this phase. Categories that are entirely missing from the CV are the highest-priority additions.

7. **Checkpoint: candidate reviews and corrects.** Present findings and let the candidate react. Their corrections are critical input, not obstacles.

### What to Watch For

- **"Built it before it had a name" patterns.** If the candidate did something years before the industry standardized it, name it explicitly. "Implemented click-based pricing in 2000" is different from "early CPC adopter."
- **Recurring meta-patterns.** Look for skills that repeat across roles: organic leadership emergence, force multiplier behavior, frontier building, market-timing patience. These are career signatures, not bullet points.
- **Cross-domain transfer.** Skills from one domain often have direct analogs in another. Map them explicitly with the candidate's input.
- **Behavioral convergence.** If multiple sources (colleagues, different AI sessions, self-assessment) identify the same trait independently, it is high-confidence.

---

## Phase 2: Career Narrative Construction

**Goal:** Build the strategic backbone that turns a list of jobs into a coherent story.

### Process

1. **Draft the identity statement.** One sentence that everything else supports. Test: does every major career move make sense in light of this sentence?

2. **Identify the through-line.** The recurring pattern across the career. Not what the candidate did at each job, but the thread connecting all of them. See `references/narrative-archetypes.md` for a library of common career patterns with examples. The candidate's through-line may be one archetype or a combination. The archetypes are scaffolding, not boxes — use them to accelerate pattern-matching, then customize to the actual career.

3. **Structure into acts.** Most careers have 2–4 natural phases (early career, growth, leadership, transition). Each act should escalate in scale or impact.

4. **Map the operating style.** How does this person work? Draw from behavioral observations, self-report, and inferred patterns. Include: decision-making style, collaboration mode, communication preferences, what energizes them, what drains them.

5. **Collect interview stories.** Rank by tier: Tier 1 (deploy for any role), Tier 2 (deploy for specific angles), Tier 3 (reserve for follow-up). Include humanizing anecdotes the candidate considers unremarkable — these are often the most memorable.

6. **Map friction points honestly.** Every limitation gets a prepared framing. Use two-layer responses: first answer (honest, self-aware) and deeper follow-up if pushed (shows wisdom). See `references/calibration-guide.md` for the calibration framework.

7. **Identify failure patterns.** Career-spanning patterns of missed value capture, structural limitations, or recurring obstacles. Named and owned failure patterns become evidence of maturity. Unnamed ones become quiet doubts.

8. **Stress-test from the buyer's perspective.** Evaluate the narrative as a recruiter (30-second scan), hiring manager (evidence check), and HR specialist (logistics/flags). The obstacles this reveals become explicit preparation targets.

9. **Checkpoint: candidate reviews and corrects.** Present framings and let the candidate push back. Identity corrections ("that's not how I'd describe myself") reveal the candidate's actual self-model and often produce the sharpest reframings.

### The Correction Loop (Critical)

This is the most valuable part of the process. Present a framing. See if the candidate pushes back.

- If they accept it → probably accurate
- If they refine it → the refinement is the real insight
- If they reject it → that is important data; revise

**Poke at the candidate.** Don't just accept what they volunteer. Probe for:
- What energizes them versus what drains them
- Competing internal instincts ("I'm lazy but I did 470 test runs")
- How they describe "negative" traits (often the mechanism underneath is a strength)
- Small concrete stories they consider unremarkable (usually the best stories)
- Limitations the market is catching up to (not a weakness — a timing observation)

See `references/principles.md` for detailed guidance on handling corrections, credit balance, and self-assessment calibration.

---

## Phase 3: Resume Drafting

**Goal:** Create a resume that is a sales document, not a career record. Every line must earn its space.

### Process

1. **Confirm target role, market, and format.** Ask before writing anything. US Letter for American markets, A4 for European. No photo/DOB for US applications.

2. **Ask for the candidate's actual work.** Published papers, portfolio links, code repositories, scorecards, anything they have produced. Read these directly. Do not rely on the candidate's description — candidates who undersell themselves will describe their work modestly, but the work itself does not have that problem. Direct evaluation of artifacts is the core mechanism for solving the modesty problem.

3. **Choose structure based on positioning.**
   - Standard: Summary → Experience → Skills → Education
   - Transition: Summary → Portfolio/Projects → Experience → Skills → Education (lead with the target-domain work)
   - Technical: Summary → Technical Skills → Experience → Projects → Education

4. **Draft section by section.** After each section, present to the candidate for correction. Do not write the whole document and then ask for feedback.

5. **Default to understated framing.** Let the candidate upgrade, not downgrade. "Identified an underutilized feature and repositioned it for the French market" is both more honest and more compelling than "co-developed the pricing model." Corrections that push framing downward from overclaiming consistently produced better results than the original inflated version.

6. **Apply the candidate's writing style.** If the candidate has an established style or stated preferences (front-load conclusions, avoid jargon, short sentences), the resume should comply. The resume is a writing sample whether intended or not.

7. **Reputation protection scan.** Before finalizing, actively scan every line for content that could expose the candidate to legal, professional, or reputational risk. This includes NDA-protected details, classified information, client names, political or religious content, proprietary metrics, and identifiable information about former colleagues. But also scan for second-order risks: overclaiming the candidate cannot defend in conversation, framing a former colleague would dispute, claims that would not survive a Google search, and any gap between what the resume promises and what the candidate can deliver on day one. Flag anything found, explain the risk, and propose safe alternatives. See `references/principles.md` section 11 for the full framework.

8. **Choose format based on target.**
   - **Docx/PDF:** ATS-friendly, works everywhere. Default for most candidates.
   - **HTML:** For technical or product roles where the resume itself demonstrates skills. Interactive elements (dark mode, expandable sections, animations) are portfolio pieces.
   - **Dual format:** HTML as primary human-facing document, docx as ATS backup. Same content backbone.

9. **Final review: candidate reads the complete document and corrects.**

### Key Drafting Principles

- **Early career compression.** Roles older than 10–15 years can be compressed to a single "Earlier" line unless they demonstrate the through-line.
- **Origin stories reveal skills.** How each project started (personal need? gap identification? curiosity?) demonstrates a different competency. Accurate origins do more work than polished descriptions.
- **Split combined projects when origins demonstrate different skills.** Two projects that started from different insights should be two entries, even if they're related.
- **Expandable depth over mode toggles.** If the resume needs both a concise view and a detailed view, use local expansion (click to see more) not global toggles (resume vs. CV mode). The reader controls the depth. The editorial hierarchy is preserved.
- **Honest is more compelling than impressive.** "When clients wanted to pay only for actual visits, implemented click counting as the measurable proxy" shows more product instinct than "built the CPC sales mechanism."

---

## Phase 4: Target Identification & ATS Optimization

**Goal:** Match the candidate to specific roles and ensure the resume survives automated screening.

### Process

1. **Search current openings** at target companies. Fetch full job descriptions.
2. **Map each role** against the candidate's profile. Rate on: conceptual fit, experience fit, ATS survival likelihood, logistics.
3. **Present the landscape honestly** and let the candidate challenge assessments. The candidate sees connections the AI may miss.
4. **Extract key terms** from each job description. Check which appear in the resume.
5. **Fill gaps with truthful translations.** The candidate's language and the job's language often describe the same things differently. An ATS does not know they overlap. Translate, do not fabricate.
6. **Leave gaps that cannot be honestly filled.** Overclaiming to match a keyword creates a worse problem than a keyword miss.
7. **Translate non-standard education.** Non-US educational systems are invisible to anglophone ATS. Add explicit equivalence language.

### The Candidate Knows Their Work Better Than You

Let the candidate challenge fit assessments. "I led a team of designers for 14 years, that IS UX experience" is a valid correction. "I designed a product that is literally what this role is hiring someone to build" is a connection the AI might miss. Ask the candidate what they see in each role.

---

## Phase 5: Cover Letter Creation

**Goal:** Write a targeted argument for each role, not a generic introduction.

### Process

1. Identify the single strongest argument for this candidate in this role
2. Open with that argument in one sentence (front-load the pitch)
3. Provide evidence from career stories, portfolio, metrics
4. Name gaps honestly before the reader can turn them into objections
5. Reframe gaps as context, not limitations
6. Close with logistics (location, visa, availability as selling points)

### Key Principles

- **The opening sentence is the entire pitch.** If the reader stops after one sentence, they should know the argument.
- **Name your gaps before they become objections.** "I do not have a completed degree. I do not have formal PM titles." Naming them yourself controls the framing.
- **Do not give the answer for free.** Demonstrate reasoning capability without delivering full conclusions. "I have designed a product architecture that addresses this problem. I would prefer to discuss it in person." gets the interview.
- **One resume does not fit all roles.** The same career framed differently for: researcher, PM, strategist, and consumer product visionary. Facts stay the same. Emphasis shifts.

See `references/cover-letter-guide.md` for the full cover letter framework including IP protection strategy.

---

## Phase 6: Multi-Perspective Evaluation

**Goal:** Find the weaknesses the candidate can prepare for, not confirm the resume is good.

Evaluate each application from four perspectives with genuine criticism:

1. **ATS:** Will it parse? Right keywords? What automated filters might reject it?
2. **Recruiter (30-second scan):** What catches the eye? What raises concerns? Would they pass it forward?
3. **Hiring manager (for the target role):** Does evidence support the positioning? What would they probe in an interview?
4. **HR specialist:** Legal/logistical concerns? Education requirements? Location flags? Age signals?

**Be genuinely critical, not reassuring.** The value is in finding vulnerabilities. A candidate who knows their weaknesses before the interview is better prepared than one who was told everything is fine.

Each vulnerability identified becomes one of: something to fix in the resume, something to address in the cover letter, or something to prepare for in interview prep.

---

## Reference Files

| File | When to Read |
|------|-------------|
| `references/principles.md` | Before starting any phase. Contains the full principle set for calibration, corrections, credit balance, reputation protection, and quality control |
| `references/calibration-guide.md` | When handling underselling/overselling, friction points, "negative" self-descriptions, and the fine line between accuracy and persuasion |
| `references/overclaiming-guide.md` | When the candidate inflates claims, resists corrections, or shows signs of ego-driven framing. Contains the psychological framework and de-escalation tactics |
| `references/narrative-archetypes.md` | During Phase 2. Library of common career through-line patterns with examples, to accelerate pattern-matching |
| `references/evidence-without-portfolio.md` | When the candidate has no published work, portfolio, or tangible artifacts. How to extract proof from the career itself |
| `references/cover-letter-guide.md` | During Phase 5. Contains IP protection strategy, opening sentence patterns, and gap-naming framework |
| `references/cultural-norms.md` | When the candidate targets non-US or non-English-speaking markets. Contains explicit cultural conventions by country and region, designed for models without deep cultural inference |

---

## Session Management: When to Hand Off

This process can be long. Multiple phases, web searches for job listings, fetching published work, iterating on drafts — the context window fills. When the AI detects the session is getting heavy, it should proactively suggest a handoff rather than waiting for quality to degrade.

### When to suggest a handoff

- The context window is approaching capacity (the AI can feel this as reduced recall of earlier details)
- Multiple web searches have been performed and their results are consuming context
- The session has completed one or more phases and the next phase would benefit from a fresh start
- The candidate needs time to review outputs before continuing
- The AI notices itself repeating information it already covered, or losing track of corrections made earlier

### How to hand off

1. **Write a handoff document.** This is a detailed summary of everything accomplished, every decision made, every correction applied, and every open question. It should be thorough enough that a fresh AI instance can pick up exactly where this one left off without asking the candidate to repeat anything. Include:
   - What phase(s) were completed
   - All decisions made and the reasoning behind them
   - All candidate corrections and what they changed
   - Current state of all output documents
   - What comes next and what inputs are needed
   - Any flags, risks, or open questions
   - Target role(s), market, and format decisions
   - Links to published work that was read and evaluated

2. **Package all working documents.** Collect every file produced in the session — drafts, narrative documents, skill extraction reports, cover letters, process notes — into a zip file the candidate can upload to the next session.

3. **Present both to the candidate.** The handoff document and the zip file together form the complete state transfer. The candidate uploads both to a new chat, and the new session begins by reading the handoff document before doing anything else.

### What makes a good handoff document

The test: if the candidate uploads this document to a fresh chat and says "continue from where we left off," can the AI do so without asking a single question that was already answered? Every question the new session has to re-ask is a failure of the handoff document.

Include the candidate's corrections verbatim. These are the most valuable data in the entire process and the hardest to reconstruct. A handoff that preserves the skill extraction but loses the corrections has lost the best part.

### Handoff Document Template

Use this structure. Every section is required.

```
# Resume Rework — Session Handoff

## Candidate
- Name:
- Target role type:
- Target market(s):
- Target companies (if identified):
- Contact details confirmed:
- Format decision (docx / HTML / dual):

## Completed Phases
- [Phase name]: [Status — completed / in progress / not started]

## Decisions Made
- [Decision]: [Reasoning]
(List every strategic decision — structure order, what to lead with, 
what to compress, format choices, positioning angle)

## Candidate Corrections (CRITICAL — preserve verbatim)
- [Original framing] → [Candidate's correction] → [Final framing]
(Every correction the candidate made, with the original and the result.
These are the most valuable data in the process.)

## Candidate Self-Description
- What energizes them:
- What drains them:
- Self-described limitations:
- Self-described strengths:
- Emotional context (if relevant):

## Current State of Documents
- [File name]: [Status — draft / reviewed / final]
(List every file produced with its current state)

## Sources Read
- [Source]: [What it contained / what it changed]
(Published work fetched, LinkedIn profile, behavioral analyses, 
chat history reviewed — and what each source contributed)

## Flags and Risks Identified
- [Risk]: [Status — addressed / flagged / deferred]

## Open Questions
- [Question]: [Context for why it matters]

## Next Steps
- [What the next session should do first]
- [What inputs are still needed from the candidate]
```

---

## Scope Boundary: What This Skill Does Not Do

This skill produces resumes, CVs, cover letters, and the strategic narrative that underpins them. It does not cover interview preparation, salary negotiation, LinkedIn content strategy, or career coaching beyond what is needed to build the documents.

However, the outputs of this skill are designed to feed forward into those activities. When the process is complete, the candidate leaves with:

- **A career narrative document** — the strategic backbone that can drive interview preparation, LinkedIn profile optimization, and networking conversations
- **A skill extraction report** — a comprehensive inventory of capabilities the candidate can reference when preparing for technical or behavioral interviews
- **Targeted resumes and cover letters** — per-role documents with the framing, evidence, and gap-acknowledgment already worked out
- **Interview stories** (collected during Phase 2) — ranked by tier with deployment guidance

These are the natural inputs for an interview preparation skill or coaching process. The narrative document especially is a powerful scaffold — it contains the identity statement, the through-line, friction points with prepared two-layer responses, and humanizing anecdotes. A separate interview prep skill that receives this document can build on it immediately rather than starting from scratch.

The candidate should be told this explicitly at the end of the process: "You now have a narrative document, a skill inventory, and targeted application materials. If you want help preparing for interviews, these documents are the starting point — bring them to the next conversation."

---

*This skill was developed from a real multi-session resume rework project (March 2026). Every principle was discovered through practice and refined through candidate pushback. The candidate's corrections were the single most valuable input — a process that does not build in correction loops will produce resumes that are polished but wrong.*
