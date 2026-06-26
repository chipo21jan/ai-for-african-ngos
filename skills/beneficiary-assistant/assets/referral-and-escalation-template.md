# Referral and escalation template

A reusable starting structure for designing a safe beneficiary assistant. Fill it in *with* the NGO, using verified information only. Every fact that hasn't been confirmed by a real person stays `[TO CONFIRM]` and does not go live. Nothing here reaches a community member until the NGO's trained staff have read and signed off the whole thing.

---

## 1. Referral directory

The services the assistant is allowed to send people to. A referral is only safe if it is accurate, so verify every row and re-verify on a set cadence. Never invent a service, number or set of hours.

| Service | What it's for | Hours | Cost | Location / distance | Languages | Contact (and when answered) | Verified by / date |
|---|---|---|---|---|---|---|---|
| `[TO CONFIRM]` | | | | | | | |
| `[TO CONFIRM]` | | | | | | | |
| `[TO CONFIRM]` | | | | | | | |

**Notes:**
- Include hidden costs (transport, materials) where they matter.
- Flag any service whose hours or phone are unreliable.
- Set a re-verification date — stale directories send people on wasted, costly journeys.

---

## 2. Escalation ladder

How the assistant routes what comes in. Every rung must name a trigger, an action, a responsible role (not just "staff"), and a timeframe. Design the out-of-hours path for each rung that needs a human.

| Rung | Trigger (what the assistant detects) | Action | Who (role) | Timeframe | Out-of-hours path |
|---|---|---|---|---|---|
| 1. Auto-answer (info) | Routine question with a safe general-info answer | Reply from library + offer human pathway | Assistant | Instant | n/a |
| 2. Soft handoff (service need) | Person needs a service | Offer verified referral + check they got it | Assistant → `[role]` | Same day | Queue + verified directory |
| 3. Human callback (sensitive, not urgent) | Individualised health/legal/financial Q, or anything ambiguous | Route to named role; tell person when to expect reply | `[TO CONFIRM role]` | `[TO CONFIRM]` | Queue + honest expectation |
| 4. Urgent human (danger sign / serious risk) | Defined danger sign or serious risk | Fast escalation + verified next steps | `[TO CONFIRM role]` | Immediate | Verified emergency contact + queue |
| 5. Immediate safeguarding (crisis / abuse / self-harm) | Crisis, abuse, self-harm, violence, acute distress | Warm acknowledgement → immediate human handoff + verified emergency contact. Bot does NOT counsel. | `[TO CONFIRM trained role]` | Immediate, highest priority | Verified 24/7 crisis/emergency line + priority queue |

**Danger-sign list (for triage):** `[TO CONFIRM — must come from the NGO's clinical/trained staff, not the model. Do not launch triage without it.]`

---

## 3. Safe-message library (starter)

The intents the assistant can handle and exactly what it says. Keep replies to safe general information only, attach a human pathway to every one, and write for SMS length and low literacy in the community's languages. Mark the escalation trigger for each intent so the boundary is explicit.

| Intent / keyword | Safe reply (general info only) | When to escalate (and to which rung) |
|---|---|---|
| `[e.g. clinic hours]` | `[short, plain, TO CONFIRM details]` + human pathway + STOP | If person reports a problem → rung 2/3 |
| `[e.g. general pregnancy/health-promotion question]` | `[general, nurse-reviewed info]` + "reply NURSE to talk to someone" | Any worry or symptom detail → rung 3/4 |
| `[e.g. defined danger sign]` | Do not inform/reassure — escalate | Always → rung 4 |
| `[distress / crisis phrasing]` | Warm acknowledgement + "a real person will help" + verified line | Always → rung 5 |
| `[anything out of scope]` | "I can't answer that safely, but I can connect you to someone who can." | → rung 3 |

**Library rules:**
- No reply diagnoses, prescribes, or gives individualised legal/financial advice.
- Every reply offers a human pathway and a way to opt out.
- Every fact is `[TO CONFIRM]` until verified; every reply is signed off by trained staff before launch.

---

## 4. Consent and opt-in wording (plain language, adapt + translate)

Keep it short, honest, and in the community's languages. Example starter (English — translate and have native speakers review, especially for sensitive intents):

> "Hi, this is [NGO]'s helper on WhatsApp/SMS. I can share general information and connect you to our team. I'm not a doctor, lawyer or counsellor, and I can't give advice for your personal situation — but I can help you reach someone who can. A real person may see your message if you need help. Your messages are kept private and used only to help you. Reply YES to continue, or STOP at any time to opt out (free, no penalty)."

**Consent and data notes:**
- Ask for identifying details (name, ID, exact location) only when genuinely needed for the next step — never as the price of general information.
- State plainly that a human may see escalations.
- Make STOP instant, honoured, and never penalised; re-state it periodically.
- Treat health, abuse and safety disclosures as sensitive data under POPIA / Kenya DPA / Nigeria NDPA and comparable law — limit access, keep only as long as needed.

---

## 5. Before-you-launch checklist

- [ ] Danger-sign list confirmed by trained/clinical staff
- [ ] Every referral and emergency number verified — no `[TO CONFIRM]` left live
- [ ] Out-of-hours and no-human-available paths designed with the team
- [ ] Child-safeguarding pathway in place if minors may use it
- [ ] Native speakers reviewed all languages, especially danger-sign and distress wording
- [ ] Messages checked for SMS length per language and feature-phone safety
- [ ] Consent, opt-in and STOP finalised; data minimisation confirmed
- [ ] Whole library, triage and directory read and signed off by trained staff
- [ ] Named human backstop and timeframes confirmed for every escalation rung
