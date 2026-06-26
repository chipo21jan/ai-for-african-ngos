# WhatsApp and SMS constraints — designing for the real channel

The safety logic in `safe-messaging-and-referral.md` decides *what* the assistant says. This reference covers *how* it has to say it, given the channels and devices the community actually uses. The mistake to avoid is designing for a smartphone with data and good signal, then discovering the people who most need the assistant are on a feature phone, paying per text, reading at a basic level, in a language the draft didn't cover. Design for the hardest case and the easy cases take care of themselves.

## SMS: short, plain, and costed

SMS is often the channel that reaches *everyone* — feature phones included — so treat it as the baseline, not an afterthought.

- **160 characters per segment.** A standard SMS is 160 GSM characters. Go over and it splits into concatenated segments, each typically billed separately. Accented characters and many non-Latin scripts (Arabic, Amharic/Ge'ez, etc.) drop the limit to ~70 characters per segment, which matters a lot for multilingual work. Design replies to fit cleanly, and know the segment count of every message in the library.
- **Cost falls on someone.** Whether the user or the NGO pays, long or chatty flows cost money. Keep exchanges tight. Don't send three messages where one will do; don't make people text back and forth needlessly.
- **No formatting, no links assumed.** Plain text only — no bold, no buttons, and don't assume a person can or will open a link (data, smartphone, trust). If a link is essential, also give a non-link path (a number to call, a place to go).
- **Keyword navigation.** SMS menus work by keywords: "Reply 1 for clinic hours, 2 to talk to a nurse, STOP to opt out." Keep keywords short, obvious, and forgiving of typos, spacing and case.

## WhatsApp: richer, but with its own rules

Where smartphones and data exist, WhatsApp is often preferred — but it has constraints that shape the design.

- **Session vs template messages.** On the WhatsApp Business Platform, businesses can reply freely only within a customer-service window (currently 24 hours) after the user's last message. Outside that window, only pre-approved **template messages** can be sent. This directly shapes how the assistant follows up, re-engages or sends reminders — design within it rather than around it.
- **Templates need approval and are limited.** Proactive/notification messages must be pre-registered and approved, and categories (utility, etc.) carry rules. Don't design a flow that depends on free-form outreach outside the window.
- **Use rich features sparingly and with fallback.** Quick-reply buttons, list menus and voice notes can help low-literacy users, but they assume an app version and data. Always have a plain-text equivalent so nobody is locked out.
- **Opt-in is required.** WhatsApp requires that people opt in before being messaged. Build clear opt-in and respect it.

## Low bandwidth and feature-phone realities

- **Assume intermittent connectivity.** Messages may arrive late, out of order, or in a burst when a phone reconnects. The assistant must handle queued and delayed messages gracefully — never assume a real-time back-and-forth, and never time out a person harshly for replying an hour later.
- **Assume shared and basic devices.** Phones are shared within families; a person may not be the only one reading. Keep replies discreet (see do-no-harm). Don't rely on features a basic phone lacks.
- **Minimise data and message count.** Every extra message is data and possibly money. Lead with the answer; don't make people wade through pleasantries.

## Plain language at low literacy

- **Short sentences, common words, one idea per message.** Write the way a kind, clear health worker speaks — not the way a policy document reads. Avoid jargon, acronyms and abstract phrasing.
- **Concrete and actionable.** "Go to Clinic X on Mondays, mornings, it's free" beats "Maternal services are available at designated facilities." Tell people what to do, where, when, and what it costs.
- **Test for reading level.** Aim for the lowest literacy in the community. If a message needs a second read to parse, simplify it.
- **Offer voice where you can.** For low-literacy users, voice notes (on WhatsApp) or a "call to hear this" option can be the difference between included and excluded.

## Multilingual handling

- **Detect or ask for language early, then stay in it.** Don't make people read English to get to their language. Offer a simple language choice up front and keep the whole flow consistent in their choice.
- **Translate meaning, not just words.** Health, legal and safety terms carry cultural weight; a literal translation can mislead or offend. Use translations the NGO and community trust, and have native speakers review — especially for sensitive intents and for danger-sign wording, where a mistranslation is a safety risk.
- **Mind script and length.** Non-Latin scripts shrink SMS segment limits; some languages run longer than English. Re-check message length per language, don't assume the English count holds.

## Menu and keyword navigation

- **Keep menus shallow and short.** A handful of options, not a deep tree. People on SMS can't see a whole menu at once and won't scroll endlessly.
- **Always offer "talk to a person" and "STOP".** A human-pathway option and a clear opt-out should be reachable from anywhere in the flow, every time.
- **Be forgiving.** Accept variations, typos and natural-language replies where possible; never trap someone because they typed "1." instead of "1" or answered in a sentence.

## Opt-in, opt-out and response-time expectations

- **Opt-in clearly, opt-out easily.** Get consent before messaging; make STOP/opt-out obvious, instant, honoured, and never penalised. Re-state the opt-out periodically.
- **Set honest expectations.** Tell people when to expect a human reply, and be truthful — "a nurse will reply during the day (Mon–Fri)" not "immediately" if that's false. For anything urgent, always pair the wait with a verified emergency contact (see the safeguarding reference).
- **Acknowledge receipt.** A short "Got your message, a person will reply by [time]" stops people feeling abandoned while they wait — without falsely implying the bot has handled it.

## Accessibility

- **Voice notes and call-back options** for those who can't or prefer not to read.
- **Simple, consistent menus** that don't change shape between sessions.
- **Discreet wording** for users who may be overheard or whose phone is shared.
- **Patience with slow or partial replies**, so older users, low-literacy users and people in distress are not cut off for being slow.

The throughline: an assistant that only works on a smartphone, on data, in English, with good signal, in real time, has already excluded the people who most need it. Build for SMS, feature phones, low literacy and the local language first, and let the richer experiences be a bonus on top.
