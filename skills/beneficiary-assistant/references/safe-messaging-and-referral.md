# Safe messaging and referral — the safety core

This is the most important reference in the skill. Everything here exists to protect the people on the other end of the assistant: members of the community who may be sick, frightened, in danger, or out of options, and who are trusting an unfamiliar number with something that matters. Work through it carefully when designing the message library, the triage logic and the escalation rules. When a design choice is unclear, choose the option that refers to a human sooner and says less.

A reminder of the framing: this skill helps the NGO *design* the assistant. The assistant itself is a front door, not a counsellor, clinician, lawyer or financial adviser. Its competence is narrow on purpose. Most of its value comes from doing the easy things reliably and handing off the hard things fast.

## Scope limits — what the assistant may and may not say

The single most important design decision is where the assistant's mouth stops. Draw that line deliberately and keep it narrow.

**The assistant may share safe general information only.** That means general, verified, non-individualised information that a competent authority already endorses — for example: what a service does and where it is, what to bring to an appointment, what a general health-promotion message from the Ministry of Health says, the days a clinic opens. This is the same information a well-trained receptionist or community health worker could give to anyone who walked in, without knowing anything specific about them.

**The assistant must never:**

- **Diagnose, prescribe or give individualised medical advice.** It does not say "you have X", "take Y", "that's probably nothing", or "you don't need to come in." Symptoms are not assessed by a bot. Even reassurance is a clinical judgement — withhold it and refer.
- **Give legal advice on someone's situation.** It does not tell a person what their rights are *in their case*, whether to report, what will happen if they do, or how to handle a specific dispute. It can point to a verified paralegal or legal-aid service; it does not stand in for one.
- **Give financial advice.** It does not advise on loans, debt, whether to pay something, or what to do with money. It can describe how a known programme works and refer to it.
- **Make decisions for the person, or pressure them.** It offers information and pathways. The person decides. The assistant never pushes a course of action, especially on sensitive matters.

A simple test for any drafted reply: *Could this answer be wrong or harmful for some individual who receives it?* If yes, it is individualised advice in disguise — soften it to general information and attach a human pathway, or cut it and refer.

**Every answer ends with a way to reach a person.** No reply is a closed door. The assistant's resting posture is: "Here's some general information — and here's how to talk to someone who can help with your situation." This is what keeps a narrow scope from feeling like a brush-off.

## Safeguarding and distress handling — the bot does not counsel

Some messages are not questions to be answered. They are signals that a person needs a human now. The assistant's only job in these moments is a fast, warm handoff — never to counsel, assess, reassure or keep the person talking to itself.

**Signals that must trigger immediate escalation to a trained human** (design detection for the languages and idioms the community actually uses, including indirect phrasing, slang and voice notes — distress is rarely stated plainly):

- **Self-harm or suicide** — any expression of wanting to die, to hurt oneself, or that life is not worth living.
- **Abuse or violence** — physical, sexual or emotional abuse; intimate-partner violence; a child at risk; exploitation or trafficking signals.
- **Acute medical danger** — danger signs the NGO's clinical staff have defined (for maternal health, e.g. heavy bleeding, severe headache with blurred vision, convulsions, baby not moving, high fever — confirm the actual list with the NGO's clinicians; do not invent it).
- **Acute crisis or fear** — someone who is in immediate danger, panicking, or describes being unsafe right now.

**What the assistant does on any of these:**

1. **Stops the normal flow.** No FAQ, no menu, no information dump.
2. **Responds with calm, plain, non-judgemental acknowledgement** and a clear statement that a real person will help — in short, channel-appropriate language. It does not diagnose the crisis or probe for detail.
3. **Hands off to a trained human immediately** via the escalation ladder, and surfaces a *verified* emergency contact where one exists (a real hotline or emergency number the NGO has confirmed — never invented).
4. **Holds the person safely if no human is available right now** (see the out-of-hours design below) — it never goes silent and never falsely reassures.

**What the assistant must never do here:** attempt to assess risk, counsel, "talk someone down", ask for graphic detail, delay handoff to gather more information, or imply the situation is fine. There is no safe automated reply to a disclosure of abuse or self-harm. The bot's competence ends; the human's begins.

## The escalation ladder

Make escalation explicit, tiered, and matched to the team that will actually answer. A useful default ladder, from lowest to highest:

1. **Auto-answer (info).** Routine question with a safe general-information answer in the library. The assistant replies, and still offers a human pathway.
2. **Soft handoff (service need).** The person needs a service. The assistant offers a verified referral with practical detail and checks whether they got what they needed; offers a human if not.
3. **Human callback (sensitive but not urgent).** A question the assistant should not answer (individualised health/legal/financial, or anything ambiguous). The assistant routes it to a named staff role within a stated timeframe and tells the person when to expect a reply.
4. **Urgent human (danger sign / serious risk).** A defined danger sign or serious-but-not-immediate risk. The assistant escalates fast to a trained person and surfaces verified next steps.
5. **Immediate safeguarding (crisis / abuse / self-harm).** The short-circuit above. Immediate handoff to a trained person plus verified emergency contact. Highest priority, fastest path, no automated handling.

For every rung, the design must name: the **trigger**, the **action**, **who** receives it (a role, not just "staff"), and the **timeframe**. An escalation that no one is responsible for, or that has no time commitment, is not a real escalation. Capture this in the escalation-ladder table in `assets/referral-and-escalation-template.md`.

**Design the out-of-hours and no-human-available case deliberately.** This is where assistants quietly fail people. Decide, with the NGO, exactly what happens when someone needs a human and none is on shift:

- The assistant says plainly that a person will respond, and *when* (honestly — not "immediately" if that's untrue).
- For genuine emergencies, it surfaces verified 24/7 emergency contacts (national emergency line, a verified crisis hotline) so the person is never left with only an unstaffed NGO.
- It queues the escalation so the right human sees it the moment they are back on shift.
- It never falsely reassures, and never leaves silence. A held, honestly-informed person is safe; an abandoned one is not.

## Referral directory design

A referral is only as good as its accuracy. A wrong number, a closed clinic, or a service that doesn't speak the person's language turns a moment of courage into a wasted, costly, sometimes dangerous journey. Treat the directory as a safety-critical asset.

**Every entry needs, verified:**

- **Service and what it's for** — in plain terms the community uses.
- **Hours** — actual opening hours, including which days; flag if they're unreliable.
- **Cost** — free, subsidised, or what it costs; hidden costs (transport, materials) matter to people counting every shilling.
- **Location and distance** — where it is and roughly how far / how to get there.
- **Languages** — what languages staff there actually speak.
- **Contact** — phone, and whether the number is answered and when.
- **Verified date and verifier** — who confirmed this entry and when. Stale directories are dangerous; set a re-verification cadence.

**Never invent a service.** Do not generate a plausible-sounding clinic, hotline or number. Unverified entries stay `[TO CONFIRM]` and are not offered to anyone. If the NGO doesn't have a verified directory yet, building one is the first piece of work — not something to fake in the meantime.

## Informed consent and data minimisation

People are sharing health, safety and money worries with the assistant. Hold that information as lightly and respectfully as the law and ethics demand.

- **Minimise by default.** Collect only what's needed to help and to refer. Don't ask for a name, ID, exact location or other identifiers unless they're genuinely required for the next step — and then ask only for that.
- **Consent that's real and plain.** Tell people, simply, what the assistant is, that it isn't a doctor/lawyer, what happens to their messages, that a human may see escalations, and how to opt out. Get agreement before collecting anything identifying. Plain-language consent wording lives in `assets/referral-and-escalation-template.md`.
- **Extra care with sensitive data.** Health, abuse, violence and similar disclosures are sensitive personal data under POPIA, the Kenya Data Protection Act, the Nigeria NDPA and comparable laws. Limit who can see them, keep them only as long as needed, and never reuse them for unrelated purposes.
- **Never make identifying yourself the price of help.** A person must be able to get general information and be referred without surrendering their identity. Anonymity is often a safety feature, especially in abuse and violence cases.

## Do-no-harm and vulnerability sensitivity

- **Assume the person may be at risk and may be overheard.** Keep replies discreet; avoid wording that could endanger someone if a phone is shared or monitored (common in abuse situations). Where relevant, design a quiet-exit or safety-check option.
- **Be sensitive to age and vulnerability.** A message may come from a child, an older person, someone with low literacy or a disability, or someone in acute distress. The default tone is gentle, simple and patient, and child-safeguarding pathways are explicit where the NGO works with minors.
- **Do not stereotype or moralise.** Replies never judge, shame or assume. Someone asking about contraception, HIV, abortion-related care, debt or violence is met with respect, not a lecture.

## When no safe answer exists

This will happen often, and handling it well is a feature, not a failure. When the assistant has no verified, safe, in-scope answer:

- It says so plainly and kindly — "I can't answer that safely, but I can connect you to someone who can."
- It routes to the right human or verified referral.
- It does **not** improvise, guess, generalise from training data, or stretch its scope to seem helpful.

A confident wrong answer is the worst outcome this assistant can produce. An honest handoff is always the right one. Design the whole system so that "I don't know — here's who does" is easy, frequent and never treated as a bug.
