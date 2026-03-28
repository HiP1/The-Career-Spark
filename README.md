# The Career Spark

An AI-assisted skill for creating resumes, CVs, and cover letters through structured extraction, narrative construction, and calibrated drafting. The spark is already in the candidate's career — this skill finds it and makes it visible.

## What It Does

Most resumes undersell the candidate. This skill closes that gap honestly.

It takes a candidate's existing CV, career history, and available evidence — then extracts hidden skills, builds a strategic career narrative, and produces application materials that are both fully honest and maximally compelling. It was developed from a real multi-session resume rework project where 44 explicitly stated skills became 134 after extraction and inference, with entire skill categories completely absent from the original CV.

**The goal:** Help the candidate get interviews for roles they will actually thrive in, by producing application materials that accurately represent them at their best.

## How It Works

Six phases, each building on the previous one:

| Phase | Purpose | Key Output |
|-------|---------|------------|
| 1. Extract | Find the real skill set | Skill inventory with gaps identified |
| 2. Narrate | Build the strategic backbone | Career narrative document |
| 3. Draft | Create the resume | Resume in target format(s) |
| 4. Target | Match to specific roles | Role-resume fit analysis, ATS optimization |
| 5. Cover | Write targeted arguments | Cover letters per role |
| 6. Evaluate | Stress-test from buyer's perspective | Vulnerability report and preparation plan |

The candidate's corrections drive the process. Every correction in the original project made the output both more honest and more compelling. The skill builds correction checkpoints into every phase.

## Key Principles

- **Extraction before drafting.** Never write a resume from scratch. Extract skills, infer hidden ones, then build.
- **Narrative before format.** Without a strategic backbone, the resume is a list of jobs.
- **Accurate altitude.** Neither underselling nor overselling. The target is the framing that is both fully honest and maximally compelling.
- **Duty of care.** The resume carries the candidate's name. The AI actively scans for legal, professional, and reputational risks — including consequences the candidate has not anticipated.
- **The candidate is always right about their own experience.** Then the AI helps frame it in the language the job market uses.

## Skill Structure

```
career-spark/
├── SKILL.md                              Main workflow
└── references/
    ├── principles.md                     Master principle set
    ├── calibration-guide.md              Underselling/overselling calibration
    ├── overclaiming-guide.md             Psychology of inflation and de-escalation
    ├── narrative-archetypes.md           12 career through-line patterns
    ├── evidence-without-portfolio.md     Finding proof when no artifacts exist
    ├── cover-letter-guide.md             Targeted cover letter framework
    └── cultural-norms.md                 Resume conventions by country/region
```

The SKILL.md is the entry point. Reference files are loaded on demand based on the phase and candidate situation.

## Who It's For

- **Experienced professionals** reworking their resume for a career transition or major shift
- **Mid-career candidates** who undersell their skills and need help seeing the full picture
- **Anyone targeting specific roles** who needs tailored application materials, not a generic CV polish
- **Early-career candidates** who need help framing limited experience and building toward stronger evidence
- **Cross-border applicants** targeting markets with different cultural resume conventions

## What It Does NOT Do

This skill produces resumes, CVs, cover letters, and the strategic narrative that underpins them. It does not cover interview preparation, salary negotiation, or LinkedIn content strategy. However, its outputs — the career narrative, skill inventory, and collected interview stories — are designed as natural inputs for those activities.

## Installation

### As a Claude Skill

Download the `.skill` file from the [Releases](../../releases) page, then install it in your Claude environment.

### Manual

Clone or download this repository. Point your AI tool at the `SKILL.md` file as the entry point.

## Origin

This skill was developed from a real multi-session resume rework project (March 2026) between [Ivan "HiP" Phan](https://github.com/hip1) and Claude. Every principle was discovered through practice and refined through candidate pushback. The four-chat process that produced the original resume was documented, generalized, and extended to cover a broad range of candidates and markets.

The candidate's corrections were the single most valuable input in the original project. A process that does not build in correction loops will produce resumes that are polished but wrong. That insight is the foundation of the entire skill.

## License

MIT License. See [LICENSE](LICENSE) for details.
