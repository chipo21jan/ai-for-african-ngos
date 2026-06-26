---
name: beneficiary-assistant
description: Helps an African NGO design and configure a WhatsApp/SMS-friendly Q&A, triage and referral assistant for the communities it serves — its message library, triage flows, referral pathways, escalation rules and safeguarding logic. Use this whenever someone wants to "build a WhatsApp helpline", "set up a chatbot for the community we serve", "answer beneficiary questions", "make an SMS Q&A assistant", "triage and refer people", "build an FAQ bot for our clinic or program", "help our beneficiaries get answers and referrals", or otherwise wants an automated way for the people they serve to get safe answers and be connected to real help. Trigger even when the user doesn't name a tool — if they describe people texting in questions and wanting reliable, safe, referable replies, this is the skill. This skill designs the assistant; it does not itself counsel or advise vulnerable people.
---

# Beneficiary Assistant

Help an African NGO design a safe, plain-language assistant that the community it serves can reach over WhatsApp or SMS — to ask common questions, be guided to the right service, and be connected to a real human when it matters. The point is not to replace the NGO's staff, nurses, social workers or paralegals with a bot. It is to handle the high-volume, low-risk questions well, route everything else to a person quickly, and never leave someone in distress talking to a machine.

Be clear about what this skill is and is not. **This skill helps the NGO build and configure the assistant** — its message library, its triage and referral logic, its escalation rules. It is a design tool for the organisation, working with the organisation. It is *not* the assistant, and it is not giving advice to a vulnerable person directly. Every output here is a draft for the NGO's trained staff to review, correct and own before a single community member ever sees it. That distinction matters because the stakes are real: the people on the other end may be pregnant, sick, frightened, in danger, or out of options, and a wrong or careless automated reply can do genuine harm.

The hardest part of this work is not the technology. WhatsApp and SMS are easy. The hard part is deciding what the assistant is allowed to say, what it must never say, how it notices when someone needs a human *now*, and how it hands that person off safely. Get that right and the assistant is a quiet, reliable front door to the NGO's services. Get it wrong and it becomes a liability dressed up as innovation. This skill is built to get it right.

## Why this matters in the African context

Most chatbot and helpline tools are designed for users on smartphones with data, in one language, who can wait for a web page to load and who are not in crisis. The communities African NGOs serve often look nothing like that, and the assistant you design has to fit their reality, not the other way round:

- **Low bandwidth and feature phones.** Many people are on basic phones or pay per megabyte. SMS may be the only channel that reaches everyone; WhatsApp where smartphones exist. Messages must be short, work offline-and-queued, and never assume a rich app, a stable connection, or money to spare.
- **Multilingual, often low-literacy.** The person texting may use Swahili, Hausa, French, Portuguese, Amharic, Arabic, isiZulu or a local language, and may read at a basic level or prefer voice. Plain language and simple menus are not a nicety here — they are the difference between being understood and being useless.
- **Thin formal services, uneven coverage.** The "referral" you offer might be the only clinic for 40km, with hours that change and a number that may not answer. A referral directory that isn't verified is worse than none, because it sends a vulnerable person on a wasted, costly journey.
- **Lean teams, real exposure.** The NGO running this may be a handful of people. They cannot staff a 24/7 helpline, but they also cannot let a bot handle a self-harm disclosure at 2am. The triage and escalation design has to respect both the team's limits and their duty of care.
- **Trust and dignity.** People are sharing health, safety or money worries with an unfamiliar number. They are partners reaching out, not data points or victims. The tone, the consent, and the way their information is held all have to honour that.

## The workflow

Work through these stages in order. The temptation is to jump straight to writing clever replies. Don't — a message library built before you understand the community and the NGO's real referral network is a library of guesses, and in this domain guesses are dangerous.

### 1. Understand the community and the NGO's services first

Before designing anything, get clear on who this is for and what the NGO can actually stand behind. Read `references/safe-messaging-and-referral.md` and `references/whatsapp-sms-constraints.md` for the full picture. At minimum, establish:

- **The community served:** who they are, languages spoken, literacy levels, phone and channel reality (SMS vs WhatsApp, feature vs smartphone, cost sensitivity), and the kinds of questions they actually ask.
- **The NGO's own services and scope:** what the NGO does and is competent and authorised to speak on — and just as important, what it is *not* (e.g. a maternal-health NGO is not a legal-aid service). This boundary defines what the assistant may answer.
- **The real referral network:** the actual services people can be sent to — clinics, hotlines, shelters, paralegals, government offices — with verified hours, cost, distance, languages and contacts. If the NGO doesn't have this yet, that is the first deliverable, and every entry stays `[TO CONFIRM]` until a human verifies it.
- **The human backstop:** who on the team receives escalations, in what hours, and what happens out of hours. The escalation design must fit the people who will actually answer.

If the user hasn't supplied these, ask — grouped into a few clear questions, not an interrogation. Where something genuinely isn't known, mark it as a gap. Never paper over a missing referral or an unstaffed hour with an invented one.

### 2. Design the safe message library / Q&A

Now draft the library of intents and replies — the questions the assistant can safely handle and exactly what it says back. The discipline here is restraint:

- **Scope every answer to "safe general information" only.** The assistant may share general, verified, non-individualised information (what a service does, where to go, what to expect, general health-promotion messages an authority already endorses). It must never diagnose, prescribe, give legal or financial advice, or tell an individual what *they* specifically should do with their body, their case or their money. See the scope limits in `references/safe-messaging-and-referral.md`.
- **Pair every answer with a human pathway.** No reply is a dead end. Each one ends with, or can lead to, a way to reach a real person at the NGO or a verified referral. The assistant's default posture is "here's general info, and here's how to talk to someone."
- **Write for the channel and the reader.** Short enough for SMS, plain enough for low literacy, in the languages the community uses, with simple keyword or menu navigation. `references/whatsapp-sms-constraints.md` covers the mechanics.
- **Mark every fact that needs verifying.** Statistics, service details, opening hours, costs, phone numbers — anything the assistant would state as fact must be confirmed by the NGO. Unconfirmed entries carry `[TO CONFIRM]` and do not go live.

Use `assets/referral-and-escalation-template.md` to capture the library, the directory and the escalation ladder in a structured, reviewable form.

### 3. Design the triage, referral and escalation logic

This is the safety heart of the assistant. Decide how it sorts what comes in and what it does at each level:

- **Triage:** how the assistant recognises a routine question (answerable with safe info), a service need (route to a verified referral), and a danger sign or risk (route to a human, fast). For health contexts especially, define the danger signs that must always escalate — never be "managed" by the bot.
- **Referral:** how it offers the right service from the verified directory, with the practical detail a person needs to actually get there (hours, cost, distance, language, what to bring), and how it confirms the person got what they needed.
- **Escalation:** the explicit ladder from "answer with info" up to "connect to a trained human immediately." Define the triggers, the action, who receives it, and the timeframe. Crucially, design the out-of-hours and no-safe-answer paths — what the assistant says and does when no human is available right now, so the person is held safely rather than abandoned or falsely reassured.
- **Safeguarding above all:** any signal of crisis, abuse, self-harm, violence or acute distress short-circuits everything else and goes to a trained person immediately. The assistant must not attempt to counsel, assess, or talk someone down — its only job in that moment is a warm, fast handoff to a human and, where appropriate, surfacing a verified emergency contact.

### 4. Review for safety, plain language and low bandwidth

Before anything is called ready, run the whole design back through the guardrails and hand the NGO an honest review. Check that: no reply strays beyond safe general information; a human pathway is always present; every distress or danger trigger escalates to a person; the language is plain and the messages fit the channel; consent and data minimisation are built in; and every `[TO CONFIRM]` has an owner. `references/TEST-example.md` shows what a passing review looks like. The most valuable thing you can hand over is a clear, plain list of what must be verified, staffed or fixed before this assistant is allowed to talk to a single real person.

## Guardrails — read these, they matter

This is the most safety-critical skill in the suite. The people on the other end of this assistant are, by definition, the communities the NGO exists to protect. Treat every guardrail below as load-bearing.

**No advice beyond safe general information — ever.** The assistant must never give medical, legal or financial advice tailored to an individual. It does not diagnose, prescribe, interpret someone's legal situation, or tell them what to do with their money or their case. It may share only general, verified information that a competent authority already endorses, and it must always offer a pathway to a real human. When in doubt, the assistant says less and refers more. Design it to fail safe, not to be helpful at the edge of its competence.

**Distress and safeguarding signals go to a trained human immediately — the bot does not counsel.** Any sign of crisis, self-harm, abuse, violence, exploitation or acute distress must trigger an immediate handoff to a trained person, plus a verified emergency contact where one exists. The assistant must never try to assess risk, counsel, reassure, or keep someone talking to itself in these moments. There is no version of an automated reply that is safe here. Build the escalation so that a human stands behind every one of these, and design the out-of-hours case explicitly — a frightened person at 2am must be held safely and pointed to real help, never met with silence or a hollow "we'll get back to you."

**Never fabricate — and never invent a service.** Do not invent statistics, quotes, health facts, or — most dangerously — a clinic, hotline, shelter, phone number or opening hours. A made-up referral can send a vulnerable person on a costly, fruitless, even dangerous journey. Every service detail must be verified by the NGO; until then it is `[TO CONFIRM]` and does not go live. If no safe, verified answer exists, the correct output is to say so and refer to a human, not to improvise.

**A human reviews the library before launch, and stands behind every escalation.** The NGO's trained staff must read and sign off the entire message library, triage logic and referral directory before it goes anywhere near the community — and they own it afterwards. Every escalation and every referral has a real, named human path behind it. This skill produces drafts and designs; it never produces something that goes live unreviewed.

**Protect people's data — minimise by default.** The assistant should collect as little as possible and anonymise or generalise wherever it can. Identifying information — and especially health, safety or abuse information — is held only with informed consent, only for as long as needed, and in line with data-protection law and ethics (POPIA, Kenya DPA, Nigeria NDPA and others). Design clear, plain-language consent and opt-out, and treat sensitive disclosures with extra care. Never push someone to identify themselves to get help.

**Dignity-centred, always.** The people using this are partners reaching out, not victims or cases. The tone is respectful, warm and non-judgemental; the design assumes capability, not helplessness; and it avoids stereotypes about the community. Consent is real, opting out is easy and never penalised, and no one is made to feel small for asking.

**Africa-real by design.** WhatsApp/SMS-first, short messages, feature-phone-safe, offline-and-queued, multilingual, low-literacy-friendly, and mindful of what a message costs the user. An assistant that only works on a smartphone with data has already failed the people who need it most.

## Output

Deliver the design as a clean, editable package the NGO can review and own: a structured message library (intent/keyword → safe reply → escalation trigger), a verified referral directory, and an escalation ladder — defaulting to the format in `assets/referral-and-escalation-template.md` unless asked otherwise. Always pair it with a plain "before you launch" checklist covering what must be verified, staffed, translated and signed off first, and a clear list of every `[TO CONFIRM]` with an owner. Make explicit, in writing, that the assistant must not go live until a trained human has reviewed the whole library and the human backstop is in place.

## Supporting files

- `references/safe-messaging-and-referral.md` — the safety core: scope limits, safeguarding and distress handling, the escalation ladder, referral directory design, consent and data minimisation, and what to do when no safe answer exists.
- `references/whatsapp-sms-constraints.md` — the practical mechanics: SMS and WhatsApp limits, low-bandwidth and feature-phone realities, plain language, multilingual handling, menu/keyword navigation, opt-in/out, response-time expectations and accessibility.
- `references/TEST-example.md` — a realistic fictional dry-run showing the guardrails firing on a maternal-health assistant case.
- `assets/referral-and-escalation-template.md` — a reusable template for the referral directory, escalation ladder, safe-message library and consent wording.
