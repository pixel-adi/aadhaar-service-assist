# Aadhaar Service Assist — an Agent Skill

An open [Agent Skill](https://agentskills.io) that helps AI assistants guide residents through basic Aadhaar services:

- Updating address, mobile, email, name, DoB, gender or biometrics — and which channel to use (Aadhaar App, myAadhaar, or an Aadhaar Seva Kendra)
- Booking an Aadhaar Seva Kendra appointment
- What documents, device and fee to keep ready
- Whether a document the person has is valid for the update they want

It is designed to stay within the **Aadhaar Act, 2016** (no collection of Aadhaar numbers, OTPs or biometrics; no impersonation of UIDAI) and the **DPDP Act, 2023 / DPDP Rules, 2025** (purpose limitation, data minimisation, no retention, guardian-led handling for children).

> **Unofficial guidance.** This skill is not issued or endorsed by UIDAI. Official information is at [uidai.gov.in](https://uidai.gov.in) and helpline **1947**. Fees and document rules change. The skill tells the assistant to re-check official pages, and the reference section was last reviewed on 17 Nov 2026.

## Install

**Claude (claude.ai / desktop):** Download `aadhaar-service-assist.zip` → Settings → Capabilities → Skills → Upload skill.

**Claude Code:** copy the `aadhaar-service-assist/` folder into `~/.claude/skills/`, or:
```
npx skills add <github-owner>/aadhaar-service-assist --agent claude-code
```

**ChatGPT:** Skills → Create → Upload from your computer → choose `aadhaar-service-assist.zip`.

**Codex, Cursor, GitHub Copilot, VS Code and other Agent Skills–compatible tools:** place the `aadhaar-service-assist/` folder in the tool's skills directory, or use `npx skills add <github-owner>/aadhaar-service-assist`.

## Structure

```
aadhaar-service-assist/
└── SKILL.md      # instructions + legal boundaries + reference data
```

## Keeping it current

Fees, the List of Supporting Documents and app features change. When they do, update the reference sections in `SKILL.md` and bump `metadata.version` and `metadata.last-reviewed`.

## Disclaimer

This is not legal advice. Deployers of an assistant using this skill are responsible for their own obligations as data fiduciaries under the DPDP Act: privacy notice, consent, grievance redressal, breach handling and retention.

## License

Apache-2.0
