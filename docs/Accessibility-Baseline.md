# Accessibility Baseline

*A shared standard for every tool in the suite. Skills reference this file rather than restating it. Companion to `docs/Data-Protection-and-AI.md`.*

**Owner:** Chipo · **Status:** Baseline v1 · **Last updated:** 30 June 2026
**Repo home:** commit as `docs/Accessibility-Baseline.md`

---

## What this is, in one line

Every tool in this suite is built so that disabled people, low-literacy users, and people on the most basic phones can actually use what it produces — to the extent the channel and the NGO's own delivery context allow. This file says exactly what that means, what each skill must do, and — honestly — what it cannot promise.

## Why this matters in the African context

Most "AI for good" tools quietly exclude the people an NGO most wants to reach. A blind staff member can't use a PDF that's really a photo of text. A person who reads at a basic level bounces off dense, jargon-heavy output. Someone on a feature phone can't open a rich web app. And disability inclusion is now a stated priority for many of the funders still active after the 2025 cuts — so getting this right is both an ethical duty and a funding advantage.

The honest framing the suite commits to: **accessibility is not automatic.** Claude handles plain language and many languages well, which helps — but screen-reader-friendly documents, voice options, and low-literacy design are things we *build in*, not things that happen for free. This file is the checklist that makes the commitment real.

## The baseline — what every skill must deliver

These apply to all skills, scoped to what each can actually control.

**1. Plain language by default.** Outputs are written to be understood at a basic reading level unless the user asks for technical depth. Short sentences, common words, no unexplained jargon, one idea at a time. Offer a "simpler version" on request.

**2. Screen-reader-friendly formats.** Any document a skill produces (Word, Markdown, PDF) must use:
- a proper heading structure (real H1/H2/H3, not bold text pretending to be headings), so a screen reader can navigate;
- alt text on every image, chart, or diagram;
- **no text trapped inside an image** — text must be selectable, readable text;
- meaningful link text ("download the budget template", not "click here");
- tables with real header rows, not layout tricks.

**3. Text and voice, where the channel allows.** Where a skill is delivered over a channel that supports it, offer both text and voice input/output (speech-to-text in, text-to-speech out) — only on channels where this has actually been built. Never promise voice on a channel where it isn't wired up.

**4. Low-literacy and feature-phone friendly.** Messages short enough for SMS, simple keyword or menu navigation, no assumption of a smartphone, rich app, or stable connection. Mindful of what a message costs the user.

## Per-skill application

The baseline lands differently depending on what a skill does.

**Document-producing skills** — `grant-proposal-drafter`, `logframe-designer`, `policy-document-drafter`. The deliverable is a `.docx` or `.md` file. The whole of baseline points 1 and 2 applies here and is fully achievable: structured headings, alt text, no text-in-images, plain language. This is the cheap win — it's just disciplined output formatting.

**Beneficiary-facing skills** — `beneficiary-assistant`. This is where the accessibility stakes are highest *and* hardest, because the end user may be disabled, low-literacy, on a feature phone, and in distress at once. All four baseline points apply, with particular weight on plain language, voice/text choice, and low-literacy menu design. This skill already carries the safety and plain-language guardrails in its own `references/whatsapp-sms-constraints.md`; this baseline reinforces and extends them.

**Internal/operational skills** — the rest. Baseline points 1 and 2 apply to anything they output for a human to read.

## The build checklist (per skill)

A skill meets the baseline when all of these are done and one test pass is recorded:

- [ ] Plain-language instruction added to the skill's prompt.
- [ ] Output-format standard applied (headings, alt text, no text-in-images, real tables/links).
- [ ] Voice/text options offered **only** where the channel supports them and they're built.
- [ ] Low-literacy / feature-phone constraints respected (for messaging skills).
- [ ] One assistive-technology test pass recorded (see below) before the skill claims the baseline.

## How we test it (the one pass that makes the claim true)

Before a skill is described as meeting this baseline, run one practical check and note the date and result in the skill folder:

1. Generate a representative output.
2. Open it with a free screen reader (e.g. NVDA on Windows, VoiceOver on Mac/iOS, TalkBack on Android) and confirm headings, alt text, and reading order work.
3. Read it back asking "would someone at a basic reading level follow this?"
4. For messaging skills, confirm it works as plain text on a feature phone / SMS, not just in a rich app.

Without this pass, the baseline is a promise, not a fact. With it, you can point a funder at evidence.

## Honest scope and limits

State these plainly; over-claiming is worse than a modest, true claim.

- **Not automatic.** Everything above is built in deliberately, skill by skill — it is not a property of the AI.
- **Depends on the NGO's delivery context.** Whether an end user has a screen reader configured, an assistive device, or any connection at all is the NGO's environment, not something the tool controls. Full accessibility is addressed per engagement.
- **Channel limits are real.** SMS and WhatsApp have hard constraints; we mitigate, we don't pretend they're solved.
- **Voice is conditional.** Promised only where actually implemented.

The defensible claim, therefore, is: *"Modules are built to an accessibility baseline — plain-language outputs, screen-reader-friendly formats, and text/voice options where the channel allows — and tested with assistive technology. Full accessibility depends on each NGO's delivery context and is handled per engagement."*

## How to use this file in a skill

Add one line to each skill's guardrails or supporting-files section:

> **Accessibility.** This skill follows the suite accessibility baseline — see `docs/Accessibility-Baseline.md`. In short: plain language, screen-reader-friendly output (real headings, alt text, no text trapped in images), and voice/text options where the channel supports them.

That keeps the standard defined once and inherited everywhere, rather than copied (and drifting) across 19 tools.
