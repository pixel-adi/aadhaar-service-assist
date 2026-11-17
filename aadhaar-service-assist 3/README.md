# Aadhaar Service Assist — an Agent Skill

An open [Agent Skill](https://agentskills.io) that helps AI assistants guide residents through basic Aadhaar services, **quickly and from a built-in knowledge base**:

- Updating address, mobile, email, name, date of birth, gender, photo or fingerprints, and which channel to use (Aadhaar App, myAadhaar or an Aadhaar Seva Kendra)
- **"Do you have any of these?"** checklists that tell people whether their documents will be accepted, and what to do if they have none
- Booking an appointment, fees, processing times, complaints and Regional Office contacts
- Answers in **any Indian language**, plus an option to **read the answer aloud**

> **Unofficial guidance.** Not issued or endorsed by UIDAI. Official information: [uidai.gov.in](https://uidai.gov.in) · helpline **1947**.

## What's new in v2.0.0

- **Answers locally first.** The assistant answers from the knowledge base in the skill and searches the web only when something isn't covered. Responses are much faster.
- **Knowledge base:**
  - UIDAI **Citizen's Charter (Jan 2024)**, converted to Markdown with its original structure. As of Nov 2026 this is still the charter UIDAI links.
  - **Lists of Acceptable Documents** from the Aadhaar (Enrolment and Update) First Amendment Regulations, 2026.
  - **Current facts** that override the 2024 charter: fees from Oct 2025, the new Aadhaar App, free myAadhaar document update until 14 Jun 2027.
- **Checklist flow.** The assistant asks "Do you have any of these?", and people reply with numbers.
- **Translate and read aloud.** Every answer ends with an offer to translate it or read it out.
- **Interactive Aadhaar Document Checker** (`assets/aadhaar-document-checker.html`). Tap a task, tick your documents, get the answer, translate it, and hear it read aloud.

## Install

**Claude (claude.ai / desktop / mobile):** download `aadhaar-service-assist.zip` from **Releases** → Settings → Capabilities → Skills → Upload skill. If you uploaded v1, replace it.

**ChatGPT:** Skills → Create → Upload from your computer → choose the zip.

**Claude Code, Codex, Cursor, Copilot, VS Code:**
```
npx skills add <github-owner>/aadhaar-service-assist
```

## Structure

```
aadhaar-service-assist/
├── SKILL.md                                 # workflow, legal boundaries, quick-answer knowledge base
├── references/
│   ├── citizen-charter-jan-2024.md          # full UIDAI Citizen's Charter in Markdown
│   └── acceptable-documents-2026.md         # Lists I–IV of acceptable documents (2026)
└── assets/
    └── aadhaar-document-checker.html        # interactive checker (works in any browser)
```

## Privacy and law

Built to stay within the **Aadhaar Act, 2016**: it never collects Aadhaar numbers, OTPs or biometrics, and never impersonates UIDAI. It also follows the **DPDP Act, 2023 / DPDP Rules, 2025**: purpose limitation, data minimisation, nothing stored, and guardian-led handling for children. The checker page keeps nothing you tick.

## Keeping it current

When fees, the document list or app features change, update **Current facts** in `SKILL.md` and the files in `references/`, then bump `metadata.version` and `metadata.knowledge-base-date`.

## Disclaimer

Not legal advice. Anyone who deploys an assistant using this skill is responsible for their own obligations as a data fiduciary under the DPDP Act.

## License

Apache-2.0
