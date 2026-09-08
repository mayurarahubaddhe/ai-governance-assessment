# AI Responsible Product Assessment

A tool that assesses an AI-powered system against defined Responsible AI, governance, and regulatory controls - identifies evidence-backed gaps, and recommends remediation.

**This is not an "is this AI ethical?" tool.** "Ethical" isn't measurable, and a tool that outputs an ethics score manufactures false confidence. This tool instead evaluates whether specific, named controls - drawn from NIST AI RMF and the EU AI Act - are actually documented and evidenced for a given system. It's explicit about what could not be verified, and it never treats missing evidence as a pass.

## What it does

1. **Intake** - a short set of questions establishes what the system does, who it affects, and what data it uses.
2. **Risk & EU AI Act classification** - a fully deterministic rules engine (no AI judgment involved) computes a risk tier and EU AI Act status, including a hard block for Article 5 prohibited practices.
3. **Evidence review** - mark each applicable governance criterion as Pass, Partial, Fail, Unable to assess, or Not applicable.
4. **Report** - a scored, evidence-based report: readiness percentages, a confidence score, findings by severity, and specific remediation recommendations. Downloadable.

## Before you try it: this version is manually assessed

**There is no auto-fill.** You can upload supporting documents (PDF, Word, text), but in this shared version they're stored for your own reference only - the tool does not read them and automatically populate answers. Depending on the system's risk tier, somewhere between ~15 and ~74 criteria will apply, and **you mark the status of each one yourself**, based on your own review of the evidence.

This is a deliberate, disclosed limitation, not a hidden one: an AI-assisted evidence-mapping step exists in the underlying design (see the guide, Section 8) where a model proposes a status per criterion for a human to accept or reject - but that step depends on a live connection this standalone file doesn't have, so it's switched off here in favor of full manual review. Expect a real assessment to take some hands-on time, not a few seconds.

## Try it

**[Open the live tool](https://yourusername.github.io/your-repo-name/)** - runs directly in your browser, no install, no account, no download.

Two demo scenarios are preloaded for quick testing - a high-risk credit engine and a low-risk internal summarizer - so you can see the full report output without doing all 74 criteria by hand first.

*(Nothing you enter or upload leaves your browser - everything runs client-side.)*

## Documentation

📄 **[Framework & User Guide (PDF)](./AI-Governance-Assessment-Guide.pdf)** - covers:
- Why "is this AI ethical?" is the wrong question, and what this tool measures instead
- The 18-domain assessment framework and how criteria are structured around evidence, not assertions
- How the risk & context engine decides which controls apply to a given system
- How the EU AI Act and NIST AI RMF are incorporated
- How scoring works, in plain terms - readiness, confidence, and verdict, without the underlying formulas
- The role of AI in the tool (proposes evidence mappings; never sets the final score)
- A full step-by-step usage guide

## Current scope

- **Evidence-based assessment only** - you supply the documentation and evidence; the tool doesn't yet assess a system from its public web presence alone (planned).
- **No persistence** - assessments live only in your browser session and are lost on refresh. Download your report before closing the tab.
- **A representative set of criteria**, not yet the full eventual library.
- **Not a legal compliance certification.** Regulatory mapping is a traceability aid, not legal advice.

## Feedback

Issues and discussion welcome via GitHub Issues - particularly on the framework structure and scoring logic.

---

*Built by Mayura Rahubaddhe.*
