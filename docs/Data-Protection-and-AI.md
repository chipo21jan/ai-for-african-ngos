# Data Protection & AI — A Practical Note for African NGOs

*A plain-language reference for using AI tools responsibly with non-profit data. Part of the AI-for-African-NGOs suite.*

> **Not legal advice.** This explains how the relevant rules generally work so you can ask the right questions. For anything you'll rely on commercially, consult a data-protection lawyer or Data Protection Officer (DPO) in the country where you operate. Laws change, and the details vary by jurisdiction.

## 1. Why this matters
NGOs hold some of the most sensitive data there is — about beneficiaries who are often vulnerable. Using AI well means protecting that data by law *and* by ethics. Funders increasingly ask about it too. The good news: a few clear principles cover most of it.

## 2. The African data-protection landscape — it's broad
There is no single "African" data law. The rule that governs you is the **national law of the country where your organisation and your beneficiaries are.** That landscape is now extensive:

- Around **33–36 African countries have their own data-protection laws** (UNCTAD counted 33 with legislation as of 2022; more have passed since).¹
- The **African Union's Malabo Convention** (on Cyber Security and Personal Data Protection) **entered into force in June 2023**, giving the continent a shared framework — though only about **16 of 55 AU states** have ratified it so far.²
- Named examples (illustrative, not exhaustive): **South Africa** (POPIA), **Kenya** (Data Protection Act 2019), **Nigeria** (NDPA 2023), **Ghana** (Data Protection Act 2012), **Senegal** (one of the earliest, 2008), **Mauritius** (closely GDPR-aligned), plus Uganda, Rwanda, Zimbabwe, Zambia, Tanzania, Egypt, Morocco, Botswana, Angola and many more.

**Takeaway:** don't assume a fixed shortlist. Identify the specific national law(s) that apply to each NGO you work with, and design to those.

## 3. Who is responsible? Controller vs processor
This is the structure that determines accountability when you use an AI service like Claude:

- **You (or the NGO) are the "data controller"** — you decide what personal data to use and why. The legal responsibility for that data sits with you.
- **The AI vendor (Anthropic) is a "data processor"** — it processes data on your instructions. Under Anthropic's **Data Processing Addendum (DPA)**, which is built into its commercial terms and includes **Standard Contractual Clauses (SCCs)**, Anthropic acts as processor on behalf of customers.³
- Under Anthropic's **commercial terms (API, Claude for Work/Team/Enterprise), customer content is not used to train models.**⁴ (Consumer/free tiers can differ — use a commercial/API tier for any real organisational data.)

**Takeaway:** because you are the controller, the duty to have a lawful basis and to send only appropriate data is *yours*, not the vendor's.

## 4. Do GDPR, EU or US laws apply? (Anthropic is US-based)
The vendor's home country is **not** what decides which law applies. Two things decide it: **whose personal data it is, and where those people are** — plus where you operate.

- **GDPR (EU/EEA)** reaches outside Europe. It can apply if you process the personal data of **people in the EU/EEA** or offer services to them. For African beneficiaries living in Africa it usually does **not** apply — *but* it can enter through **EU donors, EU-funded programmes, or EU-based staff**, and EU funders often impose GDPR-style terms by contract.
- **US law:** there is no single US federal privacy law (it's sector- and state-specific, e.g. California's CCPA/CPRA). Anthropic being US-based governs **Anthropic's own operations**; it does **not** mean US privacy law governs *your* relationship with your beneficiaries.
- **Your obligations** to beneficiaries flow from the **national law that applies to you and them** — i.e. the relevant African law from section 2.

**Takeaway:** map the people, not the vendor. Watch for EU exposure via funders and staff.

## 5. The real hotspot: cross-border transfers
Sending an African beneficiary's personal data to a US-based service is an **international data transfer**, and most African laws regulate that specifically — for example **POPIA section 72** (South Africa), and transfer provisions in **Nigeria's NDPA** and **Kenya's DPA**. GDPR has its own transfer regime (adequacy decisions / SCCs). These rules typically require safeguards (like the SCCs in Anthropic's DPA) and sometimes consent or a specific legal basis.

**Takeaway:** if real personal data will cross a border to the AI service, check the transfer rules in the applicable law and make sure a mechanism (e.g. the signed DPA/SCCs) is in place.

## 6. The golden rule: data minimisation
The single most effective protection — and the one built into every tool in this suite — is simple: **don't send identifying personal data to the model in the first place.**

- Anonymise or generalise beneficiary details by default (no names, faces, exact locations, ID numbers).
- Work with aggregates and `[TO CONFIRM]` placeholders rather than real PII.
- Keep a human in the loop to review anything before it's used or shared.

If no identifiable personal data leaves the NGO, most cross-border-transfer and accountability problems **simply don't arise.** Minimisation isn't only ethics — it's the cheapest, strongest compliance move available.

## 7. Practical checklist (for each NGO engagement)
- [ ] Which **country's law** applies (NGO location + beneficiaries)?
- [ ] Is there a **lawful basis** (e.g. consent, legitimate interest) for the data used?
- [ ] Have we **minimised** — stripped or generalised personal data before it touches the AI?
- [ ] If real PII is unavoidable, is a **DPA/SCC** in place with the vendor, and are **cross-border transfer** rules met?
- [ ] Are we on a **commercial/API tier** (no training on content), not a consumer tier?
- [ ] Any **EU exposure** (EU funders, staff, or data subjects) that pulls in GDPR?
- [ ] **Consent & dignity:** for any beneficiary story or image, is there clear consent?
- [ ] **Retention:** is data kept only as long as needed, then deleted?

---

## Sources
1. African data-protection law counts and trend — [UNCTAD / Privacy in Africa update, 2025 (TechHive Advisory)](https://www.techhiveadvisory.africa/insights/bimonthly-update-on-privacy-in-africa-september-october-2025).
2. Malabo Convention — entry into force (June 2023) and ratification status — [Malabo Convention (overview)](https://en.wikipedia.org/wiki/Malabo_Convention).
3. Anthropic Data Processing Addendum, controller/processor roles, SCCs — [Anthropic Privacy Center: DPA](https://privacy.claude.com/en/articles/7996862-how-do-i-view-and-sign-your-data-processing-addendum-dpa).
4. Anthropic commercial terms — customer content not used for model training — [Anthropic enterprise data-protection analysis (Lexology)](https://www.lexology.com/library/detail.aspx?g=7e30c9bf-71fa-4a17-aa91-9dfb7cb44b13).

*This note is general information, not legal advice. Verify against the current law in the relevant jurisdiction and Anthropic's current terms before relying on it.*
