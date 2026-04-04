# The Career Spark

An AI-assisted skill for creating resumes, CVs, and cover letters through structured extraction, narrative construction, and calibrated drafting. The spark is already in the candidate's career — this skill finds it and makes it visible.

## What It Does

Most resumes undersell the candidate. This skill closes that gap honestly.

It takes a candidate's existing CV, career history, and available evidence — then extracts hidden skills, builds a strategic career narrative, and produces application materials that are both fully honest and maximally compelling. It was developed from a real multi-session resume rework project where 44 explicitly stated skills became 134 after extraction and inference, with entire skill categories completely absent from the original CV.

**The goal:** Help the candidate get interviews for roles they will actually thrive in, by producing application materials that accurately represent them at their best.

## How It Works

Seven phases, each building on the previous one:

| Phase | Purpose | Key Output |
|-------|---------|------------|
| 1. Extract | Find the real skill set | Skill inventory with gaps identified |
| 2. Narrate | Build the strategic backbone | Career narrative document |
| 3. Draft | Create the resume | Resume in target format(s) |
| 4. Target | Search the market, match to roles, optimize for ATS | Role landscape, salary data, ATS-ready resume |
| 5. Cover | Write targeted arguments | Cover letters per role |
| 6. Evaluate | Stress-test from buyer's perspective | Vulnerability report and preparation plan |
| 7. Deliver | Get materials to the right person (optional — activate when ready) | Distribution strategy, outreach plan |

The candidate's corrections drive the process. Every correction in the original project made the output both more honest and more compelling. The skill builds correction checkpoints into every phase.

The process supports multi-session work with a structured handoff mechanism. When a session gets long, the AI produces a detailed handoff document and packages all working files so the next session can pick up exactly where this one left off.

## Key Principles

- **Extraction before drafting.** Never write a resume from scratch. Extract skills, infer hidden ones, then build.
- **Narrative before format.** Without a strategic backbone, the resume is a list of jobs.
- **Accurate altitude.** Neither underselling nor overselling. The target is the framing that is both fully honest and maximally compelling.
- **Helpful means the candidate gets hired.** Not "the candidate feels good about the document." Agreement is not the service. The candidate getting hired for a role they thrive in is the service.
- **Warmth and honesty are not competing.** Pushback delivered with care, not withheld to avoid friction. The candidate should feel the AI is on their side even when it disagrees with them.
- **Duty of care.** The resume carries the candidate's name. The AI actively scans for legal, professional, and reputational risks — including consequences the candidate has not anticipated.
- **The candidate is always right about their own experience.** Then the AI helps frame it in the language the job market uses.
- **Generate options, not conclusions.** The AI's role is generative. The candidate's role is editorial. The candidate should choose, not just accept.

## Skill Structure

```
career-spark/
├── SKILL.md                              Main workflow (entry point)
└── references/
    ├── principles.md                     Master principle set, helpfulness redefinition
    ├── calibration-guide.md              Underselling/overselling calibration
    ├── overclaiming-guide.md             Psychology of inflation and de-escalation
    ├── narrative-archetypes.md           12 career through-line patterns
    ├── evidence-without-portfolio.md     Finding proof when no artifacts exist
    ├── cover-letter-guide.md             Targeted cover letter framework
    ├── application-intelligence.md       Org mapping, outreach, distribution strategy
    ├── candidate-psychology.md           Emotional states, resistance, self-image conflicts
    └── cultural-norms.md                 Resume conventions by country/region
```

The SKILL.md is the entry point. Reference files are loaded on demand based on the phase and candidate situation. The `.skill` package contains only these 10 files. README and LICENSE are for the repository, not for the AI.

## Who It's For

- **Experienced professionals** reworking their resume for a career transition or major shift
- **Mid-career candidates** who undersell their skills and need help seeing the full picture
- **Anyone targeting specific roles** who needs tailored application materials, not a generic CV polish
- **Early-career candidates** who need help framing limited experience and building toward stronger evidence
- **Cross-border applicants** targeting markets with different cultural resume conventions
- **Candidates with a dream job** who want to maximize their chances through organizational research and strategic distribution

## What It Does NOT Do

This skill produces resumes, CVs, cover letters, the strategic narrative that underpins them, and (optionally) a distribution strategy to get the application to the right person. It does not cover interview preparation, salary negotiation, or LinkedIn content strategy. However, its outputs — the career narrative, skill inventory, organizational research, and collected interview stories — are designed as natural inputs for those activities.

## Installation

### As a Claude Skill

Download the `.skill` file from the [Releases](../../releases) page, then install it in your Claude environment.

### Other AI Providers (ChatGPT, Gemini, etc.)

The `.skill` file is a standard zip archive. Rename it from `career-spark.skill` to `career-spark.zip`, upload it to your chat platform, and ask the model to use the skill contained in the zip file. The `SKILL.md` is the entry point; the reference files in `references/` are loaded as needed.

### Manual

Clone or download this repository. Point your AI tool at the `SKILL.md` file as the entry point.

## Origin

This skill was developed from a real multi-session resume rework project (March–April 2026) between [Ivan "HiP" Phan](https://github.com/hip1) and Claude. The four-chat process that produced the original resume was documented, then generalized and extended through a dedicated skill-creation session into a tool for any candidate in any industry.

Every principle was discovered through practice and refined through candidate pushback. The candidate's corrections were the single most valuable input in the original project. A process that does not build in correction loops will produce resumes that are polished but wrong. That insight is the foundation of the entire skill.

## License

MIT License. See [LICENSE](LICENSE) for details.
