# The Architecture of Extraterritoriality

**Why the Reach of US Law Follows the Networks the World Chose to Use**

*October 11, 2026 — Liviu Birjega*

*__Disclaimer:__ The ideas and opinions in this paper are solely the author’s and do not necessarily represent the views of any organization with which the author is affiliated.*

*__A note on method:__ For what it is worth, artificial intelligence was used in the research and writing of this paper. I mention it because it is not yet an assumption; before long, the notable thing will be a paper written without it.*

## Why I Wrote This

I am not a lawyer, and this is not a legal treatise. I am a software engineer. For the past twenty-five years or so, I have built systems for a variety of government clients inside a multinational organization, and somewhere along the way it dawned on me that decisions I had treated as purely technical (where data is stored, which vendor’s tools we use, how a payment is routed) were also decisions about whose law applies. Nobody on my side of those decisions had thought of them that way, and I include myself.

I am an American by choice. Before becoming a citizen, I worked under the legal systems of Romania and Canada, and that experience left me with one useful reflex: I no longer assume that a country’s rules stop at its border. I say this because what follows could be misread as a complaint about American power. It is not. It is an attempt to describe, as accurately as I can and with sources, how that power reaches organizations that have never set foot in the United States. Americans built most of the networks the world now runs on, and I think we, as much as anyone, should understand what that reach looks like from the outside.

In July 2025 I did the research for a short paper, never published, on why Europe remains so dependent on American information technology. My answer was that the causes were mostly European: a market fragmented across twenty-seven legal systems, scarcer risk capital, and a culture that rewards stability over disruption. This paper follows that dependence to its legal consequence. When the world runs its payments, its data and its chips on American networks, American law travels with them. That was never anyone’s plan, exactly. It is a by-product, and this paper sets out to map it.

What pushed me to write it down was a pattern I kept running into. Capable people like executives, consultants and engineers who are careful about everything else, hold one of two mistaken beliefs. The first is that hosting data in Frankfurt, or buying from a European vendor, or never signing a contract in New York, places a company outside US jurisdiction. The second is the mirror image: that every enforcement action is a Washington plot. Both are wrong, and both are expensive. The first gets you a sealed indictment or a subpoena you never saw coming; the second gets you a strategy built on grievance instead of on the four gateways through which the law actually attaches.

This paper is for the people who make those decisions: the CTO choosing a cloud region, the CFO deciding whether a US listing is worth its regulatory tail, the general counsel at a non-US firm who has read Pierucci\[1\] and wants the documented version rather than the polemic, and the executive who travels through JFK without knowing what might be waiting. By the end, you should be able to map your own exposure, gateway by gateway, instead of merely feeling uneasy about it.

## Executive Overview: Jurisdiction Follows Infrastructure

If your organization operates anywhere in the world and relies on US-origin technology, clears transactions in US dollars, or stores data on American-owned cloud platforms, you are already operating within the regulatory gravitational pull of the United States. You do not need an office in New York, a subsidiary in Delaware, or American employees on payroll for US federal law to reach your operations.

This global legal reach rests primarily on three levers:

- **Export Controls That Follow the Tech:** Under the US Export Administration Regulations (EAR), any product manufactured abroad that contains more than a modest share of controlled US-origin content (generally 25% of value, or 10% for embargoed destinations) or is produced using specified US software, technology or equipment remains under US regulatory oversight. Violating these terms risks cutting a firm off entirely from future access to American technology. [\[2\]](https://www.ecfr.gov/current/title-15/subtitle-B/chapter-VII/subchapter-C/part-734)

- **Cloud Data Access Regardless of Geography:** Under the 2018 CLOUD Act, any service provider subject to US jurisdiction must produce data within its possession, custody or control in response to a court-issued warrant, even if that data sits on physical servers in Frankfurt, Paris, or Tokyo. In practice, storing files locally in Europe does not shield them from US legal process. [\[3\]](https://www.congress.gov/bill/115th-congress/house-bill/4943)

- **The Financial and Electronic Conduit:** Routing a payment through a New York correspondent bank, or sending communications across US-based servers, supplies the jurisdictional hook for wire-fraud, money-laundering and sanctions statutes. For the Foreign Corrupt Practices Act (FCPA) the position is narrower: the “interstate commerce” hook applies to issuers of US-listed securities and to US domestic concerns, while other foreign persons are reached only for acts committed while they are in US territory (15 U.S.C. § 78dd-3), and the Second Circuit’s Hoskins decision bars using conspiracy charges to bootstrap around that limit. [\[4\]](https://www.justice.gov/criminal/criminal-fraud/fcpa-resource-guide)[\[5\]](https://law.justia.com/cases/federal/appellate-courts/ca2/16-1010/16-1010-2018-08-24.html)

**The short version:** Extraterritoriality is not an accident of globalization, and it is not a conspiracy either. It is what happens when one country’s institutions and companies build most of the financial, digital and technological plumbing that everyone else decides to use, for ordinary reasons of cost, convenience and scale. In cloud computing alone, Amazon, Microsoft and Google hold about 70% of the European market, against roughly 15% for all European providers combined. [\[6\]](https://www.srgresearch.com/articles/european-cloud-providers-local-market-share-now-holds-steady-at-15) Jurisdiction follows that infrastructure, and other powers with comparable leverage are building the same tools (Sections 5.2 and 5.3). For corporate leadership, managing that reach is no longer just a compliance chore; it is a question of sovereign risk and corporate strategy.

## 1. The “Lawfare” Debate: Legal Integrity or Economic Weapon?

Over the past two decades, US enforcement abroad has grown in scale and visibility. Outside the United States, critics have labeled the phenomenon “lawfare”: the deliberate use of legal mechanisms and judicial processes to achieve geopolitical and commercial advantage. The charge runs both ways, though. At his January 2025 confirmation hearing, Secretary of State Marco Rubio argued that the post-war global order is not just obsolete but has become a weapon used against the United States. [\[7\]](https://www.pbs.org/newshour/politics/watch-live-marco-rubio-testifies-at-senate-hearing-for-secretary-of-state-confirmation) That is the same accusation, aimed in the opposite direction. Each side sees itself as the target, which seems to me a better starting point than either story on its own.

The most famous critique emerged in 2019 with Frédéric Pierucci’s bestselling book, “*Le Piège américain”* (“The American Trap”), co-authored with journalist Matthieu Aron. Pierucci, a former senior executive at the French industrial giant Alstom, argued that Washington uses its aggressive extraterritorial legal toolkit to destabilize foreign commercial rivals, softening them up until American competitors can acquire them on advantageous terms. \[1\]

- **The Pierucci Case (Alstom):** In April 2013, Pierucci was arrested by the FBI at JFK Airport on FCPA bribery charges linked to the Tarahan power project in Indonesia. [\[8\]](https://www.justice.gov/opa/pr/former-executive-french-power-company-charged-foreign-bribery-scheme) Facing extensive pre-trial detention, he watched Alstom plead guilty in December 2014 and agree to what was then a record $772 million criminal penalty. [\[9\]](https://www.justice.gov/opa/pr/alstom-pleads-guilty-and-agrees-pay-772-million-criminal-penalty-resolve-foreign-bribery) In the same period, General Electric acquired Alstom’s core power and grid businesses, assets vital to France’s nuclear energy infrastructure, in a $13.5 billion deal that closed in November 2015. \[10\]

What does this story actually prove? Less than it seems, in one respect: the misconduct was real. Alstom admitted that it had paid tens of millions of dollars in bribes on several continents, and Daniel Kahn, who ran the DOJ’s FCPA unit at the time, has flatly denied that GE’s commercial interests played any part in the prosecution. \[11\] But for a foreign company the lesson holds regardless of intent. The procedural tools the US brought to bear were enough to change the fate of a multinational, and they would be again.

## 2. The Four Gateways: How US Law Attaches to Foreign Firms

US jurisdiction does not attach at random. It needs a hook, a “nexus” in the legal term, that links foreign activity to the United States. There are four that matter for most businesses.

### 2.1 The Financial Gateway: Dollar Clearing and Correspondent Accounts

Because the US dollar serves as the world’s reserve currency, international dollar payments almost inevitably clear through correspondent accounts at banks based in New York. Under US law, that split-second transit constitutes the use of a US “instrumentality of interstate commerce”. This single electronic touchpoint supports jurisdiction under wire-fraud statutes, money-laundering rules, and economic sanctions under the International Emergency Economic Powers Act (IEEPA). For issuers and domestic concerns it also satisfies the FCPA’s interstate-commerce element.

- **Total S.A. (2013):** The French energy giant agreed to pay $398.2 million to settle FCPA charges over approximately $60 million in payments made to intermediaries of an Iranian official between 1995 and 2004. [\[12\]](https://www.sec.gov/newsroom/press-releases/2013-94) \[13\] The US asserted jurisdiction on the basis of Total’s status as an issuer of American Depositary Receipts on the New York Stock Exchange; a single $500,000 payment in 1995 from an account at a New York bank to a Swiss account supplied the interstate-commerce element for the anti-bribery charge.

- **BNP Paribas (2014):** In a landmark sanctions enforcement case, BNP Paribas pleaded guilty and agreed to pay nearly $9 billion for processing transactions on behalf of Sudanese, Iranian, and Cuban entities. The bank conducted no core business on US soil regarding these deals; the legal nexus was almost entirely the clearing of US dollars through New York. [\[14\]](https://www.justice.gov/opa/pr/bnp-paribas-agrees-plead-guilty-and-pay-89-billion-illegally-processing-financial)

- **Halkbank (2023):** The US Supreme Court confirmed in *Türkiye Halk Bankası A.Ş. v. United States* that the Foreign Sovereign Immunities Act does not govern criminal prosecutions, so foreign state-owned institutions enjoy no automatic statutory immunity from US criminal charges. [\[15\]](https://supreme.justia.com/cases/federal/us/598/21-1450/)

### 2.2 The Digital Gateway: Cloud Storage and the CLOUD Act

Passed in March 2018, the Clarifying Lawful Overseas Use of Data (CLOUD) Act established a simple rule: if a service provider is subject to US jurisdiction, it must produce customer data within its “possession, custody, or control” in response to a judicially authorized warrant, no matter where that data is physically hosted. [\[3\]](https://www.congress.gov/bill/115th-congress/house-bill/4943)

- **Corporate Control Trumps Geography:** Housing data in Frankfurt or Paris data centers does not confer legal immunity. If the provider is an American entity (such as Microsoft, AWS, or Google), US courts can compel production of that data.

- **The Senate Admission:** In June 2025, Anton Carniaux, Director of Public and Legal Affairs at Microsoft France, admitted under oath before a French Senate inquiry that he could not guarantee that French citizens’ data would never be transferred to US authorities under American legal process. \[16\]

- **Conflict with European Privacy:** This mechanism clashes directly with Article 48 of the EU GDPR, which forbids transfers based on foreign court orders unless backed by a formal international agreement; the EDPB and EDPS concluded in 2019 that a CLOUD Act order is not by itself a lawful basis for transfer. [\[17\]](https://www.edpb.europa.eu/our-work-tools/our-documents/letters/edpb-edps-joint-response-libe-committee-impact-us-cloud-act_en) While the CLOUD Act allows bilateral executive agreements, the US has concluded them only with the UK and Australia, leaving EU companies exposed in a direct legal crossfire. The conflict is older than the CLOUD Act: in Schrems II (2020) the Court of Justice of the EU struck down the EU–US Privacy Shield because US surveillance law gave Europeans no effective remedy, and the Data Privacy Framework that replaced it in 2023 rests on the same contested ground. [\[18\]](https://curia.europa.eu/juris/liste.jsf?num=C-311/18)

### 2.3 The Technological Gateway: US-Origin Content and Export Rules

Through the Export Administration Regulations (EAR), Washington claims authority over goods manufactured anywhere in the world if they incorporate controlled US components or are produced with specified American technology or tools. [\[2\]](https://www.ecfr.gov/current/title-15/subtitle-B/chapter-VII/subchapter-C/part-734)

- **The De Minimis Rule:** Items made outside the US are subject to US export controls if they contain more than 25% controlled US-origin content by value (or just 10% for embargoed destinations).

- **The Foreign Direct Product Rule (FDPR):** Even if a product contains no physical US parts, it falls under US jurisdiction if it is the direct product of specified US software or technology or is made in a plant that is itself such a product. After Huawei was placed on the Entity List in May 2019, the Commerce Department expanded the FDPR in May and August 2020 specifically to bar foreign foundries from fabricating advanced chips for the company.

### 2.4 The Corporate Gateway: US Stock Listings and Issuer Status

When a foreign company registers shares in the US or lists American Depositary Receipts (ADRs) on the New York Stock Exchange or Nasdaq, it becomes an “issuer” under the Securities Exchange Act of 1934. This triggers the FCPA’s extensive accounting provisions: [\[19\]](https://www.law.cornell.edu/uscode/text/15/78m)

- **Universal Reach:** Issuers must maintain books, records, and internal accounting controls that accurately reflect corporate transactions globally. Unlike the bribery provisions, these accounting rules require no corrupt intent or US territorial link; they can penalize how transactions are booked anywhere in the world.

- **Siemens and Delisting:** In 2008, Siemens AG paid $800 million to US authorities, with the parent company pleading guilty to books-and-records and internal-controls violations rather than bribery. Several European multinationals, Siemens among them in 2014, later delisted from US exchanges to sever this vulnerability.

### 2.5 The Gateways in Combination: The ICC Sanctions (2025–2026)

The clearest recent demonstration of these gateways working together does not involve a company at all. It involves a court. The International Criminal Court was created by the Rome Statute, adopted in 1998 by a vote of 120 to 7 with 21 abstentions; the United States, China, Russia and India are not members. [\[20\]](https://www.icc-cpi.int/sites/default/files/Publications/Rome-Statute.pdf) Under Article 12, the court claims jurisdiction over crimes committed on the territory of a member state even when the accused is a national of a non-member, an assertion US administrations of both parties have rejected as an attempt to bind citizens of a state that never consented. Washington’s record is not one of blanket hostility, however: it allowed the Darfur referral in 2005, voted for the Libya referral in 2011 and, in 2023, began sharing evidence with the court on Russian war crimes in Ukraine.

After the court issued arrest warrants for Israeli Prime Minister Benjamin Netanyahu and former Defense Minister Yoav Gallant in November 2024, Executive Order 14203 (6 February 2025) authorized sanctions on court personnel under IEEPA. Then-Prosecutor Karim Khan was designated first, followed by judges and deputy prosecutors in June, August and December 2025 and the court’s president in August 2026. On 9 October 2026, the United States sanctioned the court itself. [\[21\]](https://www.federalregister.gov/documents/2025/02/12/2025-02612/imposing-sanctions-on-the-international-criminal-court)

The effects ran through exactly the channels described above. Khan’s bank accounts were closed and, by widely reported accounts that Microsoft disputes, he lost access to his Microsoft-hosted court email; a Canadian judge on the court has described losing all her US-provided services, including her credit cards, without warning. In response, the court is moving its office software from Microsoft to Germany’s openDesk. [\[22\]](https://www.heise.de/en/news/Criminal-Court-Microsoft-s-email-block-a-wake-up-call-for-digital-sovereignty-10387383.html) None of those affected is American, and the court sits in The Hague; the reach came entirely through the financial and digital gateways.

What makes the episode worth studying is that each side accuses the other of exactly the same thing: extraterritorial overreach. The court asserts jurisdiction over nationals of states that never joined it; the United States answers by using dollar clearing and cloud services to reach a court and staff outside its territory. Which claim is the more legitimate is a political question, and not one this paper tries to settle. The lesson for business is narrower: when US sanctions apply, the service providers a client depends on will comply, wherever that client is located.

## 3. Inside the FCPA: Why the US Rules Are So Potent

The Foreign Corrupt Practices Act (15 U.S.C. § 78dd-1 et seq.) is Washington’s most far-reaching anti-corruption statute. Its reach comes from three elastic legal concepts: [\[4\]](https://www.justice.gov/criminal/criminal-fraud/fcpa-resource-guide)

- **The Flexible “Knowing” Standard:** Prosecutors do not need to prove that senior leadership had direct, explicit knowledge of a bribe. Awareness of a “high probability” of illicit conduct or “conscious disregard” (willful blindness) satisfies the legal threshold.

- **Who Counts as a “Foreign Official”?:** The statute extends far beyond cabinet ministers. Courts define employees of state-owned or state-directed enterprises as foreign officials. In many emerging markets, a procurement manager at a state utility, a doctor at a public hospital, or an engineer at a national oil company qualifies.

- **The Facilitation Trap:** While the FCPA contains an exception for nominal “grease payments” to expedite routine administrative acts, prosecutors interpret this exemption so narrowly that relying on it is hazardous. Most global corporations have banned them altogether.

### 3.1 Political Calibration: The 2025 “Trump Pause” and Current Realities

Extraterritorial enforcement is not immune to domestic politics. On 10 February 2025, President Trump issued Executive Order 14209, pausing new FCPA investigations for 180 days to review guidelines and ensure enforcement prioritized “American economic competitiveness”. [\[23\]](https://www.federalregister.gov/documents/2025/02/14/2025-02873/pausing-foreign-corrupt-practices-act-enforcement-to-further-american-economic-and-national-security)

When enforcement resumed in June 2025 under Deputy Attorney General Todd Blanche, the DOJ unveiled refocused priorities: [\[24\]](https://www.justice.gov/dag/media/1403031/dl)

- **The Four Target Factors:** Prosecutors were directed to concentrate on (1) bribery involving cartels and transnational criminal organizations; (2) conduct that deprives American firms of fair access to foreign markets; (3) corruption threatening US national security or critical infrastructure; and (4) serious misconduct involving substantial bribe payments or sophisticated concealment.

- **The Judicial Stress-Test (Adani):** What followed the pause is a live test of the new guidelines in court, not a rubber stamp. In May 2026 the DOJ moved to dismiss its entire 2024 indictment against Gautam Adani, Sagar Adani and co-defendants. On 10 August 2026, US District Judge Nicholas Garaufis (E.D.N.Y.) dismissed with prejudice the securities- and wire-fraud counts against the three defendants who had appeared, but criticized the “highly unusual” review process, rejected the Department’s contention that the case met none of the four Blanche factors, and ordered fact-based justification before ruling on the FCPA-conspiracy and obstruction counts against five non-appearing defendants. On 3 September 2026 he denied that remaining motion without prejudice, finding the stated reasons unsupported by evidence; on 28 September the DOJ petitioned the Second Circuit for a writ of mandamus. [\[25\]](https://www.mofo.com/resources/insights/261006-international-anti-corruption-developments-september-2026)

- **The New Mandate in Action (Scoular):** Conversely, on 17 July 2026 the Nebraska agribusiness Scoular entered into a three-year deferred prosecution agreement and $10 million resolution over roughly $400,000 in bribes paid, through customs brokers, to Mexican officials at the US–Mexico border between 2013 and 2019. The DOJ emphasized that a portion of those payments, without the company’s knowledge, benefited a cartel, making this the first resolution framed explicitly around the cartel pillar. [\[26\]](https://www.justice.gov/opa/pr/agricultural-company-pay-over-10m-resolve-foreign-bribery-case)

- **Market Significance:** Academic research indicates that upon the signing of EO 14209, past FCPA targets experienced abnormal stock returns yielding roughly $39 billion in aggregate value. \[27\] Enforcement, in other words, is a dial rather than a constant, and the markets price it that way.

## 4. The Human Element: How Procedure Shapes Outcomes

For foreign executives, the greatest practical risk lies less in the statute than in procedure. The US federal system resolves the great majority of criminal cases, against Americans and foreigners alike, through plea agreements rather than trials, but several of its features weigh especially heavily on a defendant with no ties to the country:

- **Sealed Indictments and Transit Arrests:** Indictments can be filed under seal, so an executive may learn of one only on arrival, or during a layover, at a US airport. Pierucci was detained without prior notice at JFK Airport. [\[8\]](https://www.justice.gov/opa/pr/former-executive-french-power-company-charged-foreign-bribery-scheme)

- **Severe Bail Hurdles:** A foreign national has few ties to the country, so prosecutors routinely argue flight risk, and many defendants spend months, sometimes years, in high-security detention while the case proceeds.

- **The Mathematics of Settlement:** According to Stanford Law School data, FCPA investigations average 39 months, costing companies around $1.57 million per month in legal and audit fees. Facing long potential sentences, 74% of DOJ individual defendants and 92% of SEC defendants choose to settle. [\[28\]](https://fcpa.stanford.edu/statistics-analytics.html)

- **The Corporate Compromise:** Once an individual executive agrees to cooperate, prosecutors use their testimony as leverage against the employer. The parent company typically signs a Deferred Prosecution Agreement (DPA), pays multi-million-dollar fines, and agrees to an invasive, US-appointed independent compliance monitor.

## 5. Everyone Builds Gateways: Europe, China and Canada

### 5.1 Europe’s Fight for Digital and Economic Sovereignty

European leaders increasingly view US legal reach not as standard anti-corruption cooperation, but as a vulnerability to European economic independence. Much of that vulnerability is self-made: the Draghi report on European competitiveness (September 2024) traced Europe’s technology gap chiefly to a fragmented single market, thin scale-up capital and regulatory burden, rather than to anything done in Washington. [\[29\]](https://commission.europa.eu/topics/eu-competitiveness/draghi-report_en) On 3 June 2026, the European Commission proposed the Cloud and AI Development Act (CADA, COM (2026) 502) as the centerpiece of its Technological Sovereignty Package, aimed directly at reducing dependence on non-EU cloud providers. Its “autonomy” pillar creates a four-level sovereignty assurance framework that public-sector bodies apply according to their risk assessments: [\[30\]](https://digital-strategy.ec.europa.eu/en/library/proposal-cloud-and-ai-development-act-cada)

- **Level 1:** Data processed and stored on infrastructure located in the EU.

- **Level 2:** Adds verifiable protection against third-country access to data or remote suspension of service (“kill switch”), with supply-chain transparency.

- **Level 3:** Adds EU ownership and control of the provider.

- **Level 4:** The highest tier, adding personnel clearance and independent audit for the most sensitive and defense-related workloads.

The Commission estimates that roughly 20% of public contracts would fall under Level 2, fewer than 10% under Level 3, and about 1%, mainly defense-related, under Level 4, so the exclusionary effect on US hyperscalers is concentrated rather than market-wide. [\[31\]](https://www.lawfaremedia.org/article/the-eu-cloud-and-ai-development-act) CADA remains a proposal in trilogue, and industry pushback has been significant: a CCIA-led coalition of international industry associations issued a joint statement ahead of the 8 June 2026 Telecom Council, and critics argue that the highest tiers function as origin-based market restrictions rather than technical safeguards; Bitkom’s July 2026 position paper, while welcoming the Act, cautioned against over-regulation and called for a precise definition of “sovereign cloud”; and the German Chambers of Commerce (DIHK) filed their own submission in September 2026. [\[30\]](https://digital-strategy.ec.europa.eu/en/library/proposal-cloud-and-ai-development-act-cada)[\[32\]](https://ccianet.org/library/joint-statement-by-international-industry-associations-on-the-cloud-and-ai-development-act-cada-ahead-of-the-telecom-council-of-8-june-2026/)

There is a reason CADA targets infrastructure rather than law. Europe’s dependence was not imposed; it accumulated. The United States took an early lead in computing in the 1960s and 1970s through public investment and companies like IBM, Intel and Microsoft, and that lead compounded, because capital, talent and standards follow the winners. Europe has spent the decades since trying to scale companies across twenty-seven legal systems and almost as many languages, with far less risk capital and a culture more tolerant of stability than of failure. Its strongest technology firms have tended to end up on American platforms or American exchanges: Arm, Britain’s most important chip designer, chose New York over London for its 2023 listing, which is precisely the corporate gateway described in Section 2.4. The European Chips Act of 2023 (€43 billion mobilized toward a 20% share of global production by 2030) and the GAIA-X cloud initiative are attempts to rebuild capacity, not to change jurisdiction. [\[33\]](https://digital-strategy.ec.europa.eu/en/policies/european-chips-act) Until a European provider operates at the scale of the US hyperscalers, European data will mostly sit with companies that answer to US courts, whichever continent the servers are on.

Beyond cloud rules, European nations have updated their offensive and defensive playbooks:

- **Domestic Resolution (Sapin II):** France enacted the Sapin II law in December 2016 to introduce French-style DPAs (the *convention judiciaire d’intérêt public*, CJIP), enabling domestic prosecutors to penalize French firms and retain settlement funds domestically before the US DOJ steps in. The January 2020 Airbus settlement, roughly €3.6 billion split among France’s PNF, the UK SFO and the DOJ, became the blueprint for this strategy. \[34\]

- **Trade Defenses:** The EU has deployed an updated Blocking Statute (Regulation 2271/96, extended to US Iran sanctions in 2018) and the Anti-Coercion Instrument (Regulation (EU) 2023/2675, in force December 2023) to penalize third nations attempting to coerce European commerce through unilateral economic measures. [\[35\]](https://eur-lex.europa.eu/eli/reg/2023/2675/oj)

### 5.2 The Chinese Mirror: Replicating US Tools

China has not limited itself to diplomatic protest. It has built a near-symmetrical set of its own instruments:

| **US Legal Mechanism**                   | **Chinese Symmetrical Counterpart**                                                               |
|------------------------------------------|---------------------------------------------------------------------------------------------------|
| Commerce Dept Entity List (EAR)          | Unreliable Entity List (MOFCOM provisions, Sept 2020)                                             |
| Export Control Reform Act 2018           | PRC Export Control Law (in force 1 Dec 2020)                                                      |
| Secondary Sanctions (IEEPA / CAATSA)     | Anti-Foreign Sanctions Law (AFSL, June 2021)                                                      |
| EU / Foreign Blocking Statutes           | Rules on Counteracting Unjustified Extraterritorial Application of Foreign Legislation (Jan 2021) |
| Foreign Direct Product Rule & De Minimis | MOFCOM Announcement No. 61 (Dual-Use Rare Earths, Oct 2025)                                       |

A prominent example is MOFCOM Announcement No. 61 (9 October 2025), which claimed jurisdiction over foreign-made items containing as little as 0.1% Chinese-origin controlled rare earths by value, or manufactured using Chinese rare-earth refining technology. It is a direct transplant of the US de minimis and FDPR concepts. \[36\] Its extraterritorial provisions were suspended for one year under the US–China arrangement of 30 October 2025; that suspension lapses on 10 November 2026. [\[37\]](https://cms.law/en/chn/legal-updates/china-expands-reporting-regime-for-export-control-and-adds-14-eu-entities-to-control-list)

Beijing has not been idle during the pause. On 22 June 2026, MOFCOM Announcement No. 23 placed MP Materials, USA Rare Earth and eight other US entities on China’s export-control list, and Announcement No. 30 of 24 July 2026 added 14 EU entities, including Rheinmetall. [\[37\]](https://cms.law/en/chn/legal-updates/china-expands-reporting-regime-for-export-control-and-adds-14-eu-entities-to-control-list) On 24 June 2026, Announcement No. 26 established a formal reporting and reward mechanism (effective 1 July 2026) for suspected strategic-mineral export violations, expressly covering circumvention through third-country transshipment, product disassembly and relabeling, and extending liability to freight forwarders, customs brokers, e-commerce platforms and financial-service providers that knowingly assist. [\[38\]](https://www.morganlewis.com/pubs/2026/07/recent-china-export-control-actions-signal-active-enforcement-for-rare-earths-and-strategic-minerals) This confirms that extraterritorial reach is now a standard instrument of any power with sufficient leverage.

### 5.3 Allies Build Gateways Too: Canada’s Lawful Access Act

The reflex to build jurisdictional reach is not confined to rivals. Canada, a treaty ally with no quarrel against US enforcement, is legislating its own digital gateway. Bill C-22, the Lawful Access Act, passed the House of Commons on 18 June 2026 under time allocation and is now before the Senate, which took up its study when Parliament returned on 21 September. [\[39\]](https://www.parl.ca/legisinfo/en/bill/45-1/c-22) Part 2 of the bill, the Supporting Authorized Access to Information Act, would impose capability-building and compliance duties on “electronic service providers” serving Canadians, foreign providers included, without the federal-jurisdiction gate that limits Canada’s already-enacted Critical Cyber Systems Protection Act (Bill C-8, whose Part 2 remains dormant pending designation orders). [\[40\]](https://www.justice.gc.ca/eng/csj-sjc/pl/charter-charte/c22_2.html)

The reaction from Washington is worth noting, because it reverses the usual roles. A letter from House Judiciary Republicans warned that Bill C-22 could allow Canadian officials to compel American companies to build backdoors into their encrypted systems, creating vulnerabilities that cannot be geographically limited (which is exactly the objection Europeans raise against the CLOUD Act) and urged Ottawa to negotiate a CLOUD Act agreement instead. [\[41\]](https://judiciary.house.gov/media/in-the-news/house-gop-warns-canada-its-new-cybersecurity-bill-could-pose-privacy-risks) Those negotiations have been ongoing since March 2022 without result; Canada would become the third partner after the UK and Australia. [\[42\]](https://www.justice.gov/opa/pr/united-states-and-canada-welcome-negotiations-cloud-act-agreement) Commentators disagree about the direction of the relationship: the Citizen Lab argues that C-22 moves Canada toward a CLOUD Act agreement that could let US agencies conduct surveillance in Canada, while a Lawfare analysis argues the bill’s Part 2 powers put the agreement Canada needs out of reach. [\[43\]](https://citizenlab.ca/research/analysis-of-proposed-surveillance-law-expansion-under-bill-c-22/)

Either way, the episode makes the structural point. Any state with sufficient leverage over the providers its citizens depend on will eventually legislate access to them; the United States is simply the state with the most leverage, and the one whose providers everyone else uses.

## 6. The Counter-Perspective: A Coordinated System, not a Pure Conspiracy

The “lawfare” thesis is intuitive, and it is not entirely wrong. But reducing every enforcement action to an American commercial plot runs into some stubborn facts:

- **The Bribery Was Real:** Defendants like Alstom, Total, and Siemens acknowledged extensive, institutional bribery schemes involving hundreds of millions of dollars in illicit payoffs. Prosecuting real corruption is not economic sabotage.

- **US Firms Bear the Brunt:** Stanford Clearinghouse records show that American corporations make up roughly 59% of all FCPA defendants. [\[28\]](https://fcpa.stanford.edu/statistics-analytics.html) Goldman Sachs’s record $2.9 billion 1MDB penalty in 2020 remains the largest FCPA settlement in history. [\[44\]](https://www.justice.gov/opa/pr/goldman-sachs-charged-foreign-bribery-case-and-agrees-pay-over-29-billion)

- **Judicial Guardrails Exist:** In *Hoskins* (2018), the Second Circuit held that foreign nationals outside the statute’s enumerated categories cannot be prosecuted for FCPA conspiracy if they could not be charged as principals; the court affirmed the executive’s acquittal in 2022. [\[5\]](https://law.justia.com/cases/federal/appellate-courts/ca2/16-1010/16-1010-2018-08-24.html) And in *Adani* (2026), a district court refused to rubber-stamp an executive-branch decision to abandon FCPA charges, demanding fact-based reasons under Rule 48(a). [\[25\]](https://www.mofo.com/resources/insights/261006-international-anti-corruption-developments-september-2026) In *Learning Resources v. Trump* (February 2026), the Supreme Court held 6–3 that IEEPA does not authorize tariffs, while leaving the statute’s sanctions and asset-blocking powers untouched. [\[45\]](https://www.faegredrinker.com/en/insights/publications/2026/2/supreme-court-decides-learning-resources-inc-v-trump-and-trump-v-vos-selections-inc)

- **From Unilateralism to Global Multilateralism:** The landmark resolutions of recent years, Airbus, Glencore and Odebrecht among them, were not unilateral American shakedowns. They were joint actions coordinated between the US, the UK Serious Fraud Office, and French or Brazilian authorities, with penalty revenues shared across borders. [\[44\]](https://www.justice.gov/opa/pr/goldman-sachs-charged-foreign-bribery-case-and-agrees-pay-over-29-billion)

**Core Conclusion:** The danger for international business is not a secret Washington conspiracy. It is a structural reality: the sheer density of American financial, technological, and digital networks gives the US unmatched jurisdictional reach, which can be dialed up or down depending on the political priorities of the executive branch, subject to limits that the courts are now actively testing.

## 7. Mapping Your Own Exposure

None of the foregoing is legal advice, and the right response differs for every organization. But the four gateways, plus the procedural pressures that follow them, suggest a short set of questions that any board, general counsel or chief technology officer should be able to answer without hesitation. If an answer is “we don’t know”, that is the exposure.

| **Gateway**             | **Where the Law Attaches**                                                                  | **Questions You Should Be Able to Answer**                                                                                                                                                                                            |
|-------------------------|---------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Financial Clearing      | Any dollar payment clearing through New York correspondent banks.                           | Which of our payment flows touch US dollars, and to whom? Are the counterparties screened against OFAC lists? For politically sensitive supply chains, could we settle in another currency, and what would that cost?                 |
| Cloud & Data            | Data held by a provider subject to US jurisdiction, wherever the servers sit.               | Who holds the encryption keys to our data? Could our provider decrypt and produce it in response to a US order without telling us? What do our contracts say about notice and the right to challenge?                                 |
| Technology & Components | Products with more than 10–25% controlled US content or made with US software or equipment. | Do we know the US-origin share of each product, down to the component? Have we screened the same bill of materials against China’s export-control and Unreliable Entity lists? Who would lose access first if a license were revoked? |
| Corporate Listings      | US ADRs, SEC registration, or US subsidiaries.                                              | What does the US listing earn us in capital cost, and what does it cost us in FCPA accounting exposure? Are US operations ring-fenced? If a resolution were needed, could it be reached at home under a domestic DPA regime?          |
| Executive Travel        | Transit through US airports by senior leadership.                                           | Has counsel assessed whether any live investigation touches our executives? Do executives have independent counsel separate from the company’s? Who decides whether a trip goes ahead?                                                |

The questions are deliberately plain. If this paper has one point, it is that US law is not uniquely sinister; it is uniquely well-connected, and the connections can be known. An organization that can answer the questions above has mapped its gateways; one that cannot is relying on geography to protect it, and geography has not done that job for some time.

## 8. Endnotes

\[1\] Frédéric Pierucci with Matthieu Aron, Le Piège américain (JC Lattès, 2019); The American Trap (Hodder & Stoughton, 2019).

[\[2\]](https://www.ecfr.gov/current/title-15/subtitle-B/chapter-VII/subchapter-C/part-734) 15 C.F.R. § 734.4 (de minimis); 15 C.F.R. § 734.9 (foreign direct product rules); BIS, Addition of Huawei to the Entity List, 84 Fed. Reg. 22961 (21 May 2019); BIS FDPR expansions, 85 Fed. Reg. 29849 (19 May 2020) and 85 Fed. Reg. 51596 (20 August 2020).

[\[3\]](https://www.congress.gov/bill/115th-congress/house-bill/4943) Clarifying Lawful Overseas Use of Data Act, Pub. L. 115-141, div. V (23 March 2018); 18 U.S.C. §§ 2703, 2713; Microsoft Corp. v. United States, No. 17-2 (U.S. 17 April 2018) (vacated as moot).

[\[4\]](https://www.justice.gov/criminal/criminal-fraud/fcpa-resource-guide) 15 U.S.C. §§ 78dd-1(f)(1)–(2), 78dd-3; DOJ/SEC Resource Guide (2020), ch. 2.

[\[5\]](https://law.justia.com/cases/federal/appellate-courts/ca2/16-1010/16-1010-2018-08-24.html) United States v. Hoskins, 902 F.3d 69 (2d Cir. 2018); 44 F.4th 140 (2d Cir. 2022).

[\[6\]](https://www.srgresearch.com/articles/european-cloud-providers-local-market-share-now-holds-steady-at-15) Synergy Research Group, “European Cloud Providers’ Local Market Share Now Holds Steady at 15%” (July 2025).

[\[7\]](https://www.pbs.org/newshour/politics/watch-live-marco-rubio-testifies-at-senate-hearing-for-secretary-of-state-confirmation) US Senate Committee on Foreign Relations, Nomination Hearing of Marco Rubio to be Secretary of State, opening statement (15 January 2025).

[\[8\]](https://www.justice.gov/opa/pr/former-executive-french-power-company-charged-foreign-bribery-scheme) US Department of Justice, “Former Senior Executive of French Power Company Charged in Connection with Foreign Bribery Scheme” (16 April 2013); Bloomberg, “Alstom Executives Charged in U.S. With FCPA Crimes” (16 April 2013).

[\[9\]](https://www.justice.gov/opa/pr/alstom-pleads-guilty-and-agrees-pay-772-million-criminal-penalty-resolve-foreign-bribery) US Department of Justice, “Alstom Pleads Guilty and Agrees to Pay $772 Million Criminal Penalty” (22 December 2014); “Alstom Sentenced to Pay $772 Million Criminal Fine to Resolve Foreign Bribery Charges” (13 November 2015).

\[10\] General Electric Co., Form 10-Q for Q3 2014; transaction closed 2 November 2015.

\[11\] Lexology, commentary on The American Trap (31 July 2019); CGTN interviews with Pierucci (May 2019 and 29 September 2021).

[\[12\]](https://www.sec.gov/newsroom/press-releases/2013-94) SEC Press Release 2013-94, “SEC Charges Total S.A. for Illegal Payments to Iranian Official” (29 May 2013); SEC Order, Exchange Act Release No. 34-69654 (29 May 2013).

\[13\] Total S.A., Form 6-K exhibit 99.1 (29 May 2013): total $398.2M; DOJ $245.2M; SEC $153M.

[\[14\]](https://www.justice.gov/opa/pr/bnp-paribas-agrees-plead-guilty-and-pay-89-billion-illegally-processing-financial) US Department of Justice, “BNP Paribas Agrees to Plead Guilty and to Pay $8.9 Billion for Illegally Processing Financial Transactions for Countries Subject to U.S. Economic Sanctions” (30 June 2014).

[\[15\]](https://supreme.justia.com/cases/federal/us/598/21-1450/) Türkiye Halk Bankası A.Ş. v. United States, 598 U.S. 264 (2023).

\[16\] French Senate, commission d’enquête hearing of Microsoft France (10 June 2025); ActuIA, “Sensitive Data and Cloud Act: Microsoft France Admits It Cannot Oppose an American Injunction” (25 July 2025).

[\[17\]](https://www.edpb.europa.eu/our-work-tools/our-documents/letters/edpb-edps-joint-response-libe-committee-impact-us-cloud-act_en) EDPB–EDPS, Initial legal assessment of the impact of the US CLOUD Act on the European legal framework for personal data protection (10 July 2019).

[\[18\]](https://curia.europa.eu/juris/liste.jsf?num=C-311/18) Court of Justice of the EU, Case C-311/18, Data Protection Commissioner v Facebook Ireland Ltd and Maximillian Schrems (16 July 2020); Commission Implementing Decision (EU) 2023/1795 on the EU–US Data Privacy Framework (10 July 2023).

[\[19\]](https://www.law.cornell.edu/uscode/text/15/78m) 15 U.S.C. § 78m(b)(2); DOJ and SEC, A Resource Guide to the U.S. Foreign Corrupt Practices Act (2d ed. 2020), ch. 3; DOJ and SEC Siemens resolutions (15 December 2008).

[\[20\]](https://www.icc-cpi.int/sites/default/files/Publications/Rome-Statute.pdf) Rome Statute of the International Criminal Court, UN Doc. A/CONF.183/9 (17 July 1998), art. 12; UN Security Council Resolutions 1593 (2005) and 1970 (2011).

[\[21\]](https://www.federalregister.gov/documents/2025/02/12/2025-02612/imposing-sanctions-on-the-international-criminal-court) Executive Order 14203, “Imposing Sanctions on the International Criminal Court” (6 February 2025); NL Times, “U.S. sanctions ICC chairman, prosecutor in latest attack on court in The Hague” (19 August 2026) and “U.S. threatens to cripple ICC as Trump administration imposes new sanctions” (9 October 2026).

[\[22\]](https://www.heise.de/en/news/Criminal-Court-Microsoft-s-email-block-a-wake-up-call-for-digital-sovereignty-10387383.html) Associated Press, “Cut off by their banks and even iced out by Alexa, sanctioned ICC staffers remain resolute” (2025); heise online, “Criminal Court: Microsoft’s email block a wake-up call for digital sovereignty” (May 2025); Politico Europe, “International Criminal Court to drop Microsoft over sanction fears” (October 2025); NL Times (9 October 2026).

[\[23\]](https://www.federalregister.gov/documents/2025/02/14/2025-02873/pausing-foreign-corrupt-practices-act-enforcement-to-further-american-economic-and-national-security) Executive Order 14209, “Pausing Foreign Corrupt Practices Act Enforcement to Further American Economic and National Security,” 90 Fed. Reg. 9587 (10 February 2025).

[\[24\]](https://www.justice.gov/dag/media/1403031/dl) US Department of Justice, Guidelines for Investigations and Enforcement of the Foreign Corrupt Practices Act (9 June 2025) (the “Blanche Memorandum”).

[\[25\]](https://www.mofo.com/resources/insights/261006-international-anti-corruption-developments-september-2026) United States v. Adani et al., No. 24-cr-433 (E.D.N.Y.), Memorandum & Order (10 August 2026) and Memorandum & Order (3 September 2026); DOJ petition for writ of mandamus (2d Cir., 28 September 2026); Morrison & Foerster, Top 10 International Anti-Corruption Developments for August 2026 (9 September 2026) and for September 2026 (6 October 2026).

[\[26\]](https://www.justice.gov/opa/pr/agricultural-company-pay-over-10m-resolve-foreign-bribery-case) US Department of Justice, press release and deferred prosecution agreement, United States v. The Scoular Company (W.D. Tex., 17 July 2026); Davis Polk, “DOJ’s most recent FCPA case sheds light on enforcement trends” (23 July 2026); Morgan Lewis, “Recent FCPA Resolution Points to DOJ’s Focus on Cartels, Adherence to Blanche Memo” (22 July 2026).

\[27\] Crippa, Malesky and Picci, “Making Bribery Profitable Again?”, International Organization 79 (2025).

[\[28\]](https://fcpa.stanford.edu/statistics-analytics.html) Stanford Law School Foreign Corrupt Practices Act Clearinghouse, “Statistics & Analytics” (data through 30 July 2025).

[\[29\]](https://commission.europa.eu/topics/eu-competitiveness/draghi-report_en) Mario Draghi, The Future of European Competitiveness, report to the European Commission (9 September 2024).

[\[30\]](https://digital-strategy.ec.europa.eu/en/library/proposal-cloud-and-ai-development-act-cada) European Commission, Proposal for a Regulation on a Cloud and AI Development Act, COM (2026) 502 (3 June 2026), Annex II; Bloomsbury Intelligence and Security Institute, “EU Cloud and AI Development Act: Sovereignty, AI and US Tech Dependence” (8 July 2026).

[\[31\]](https://www.lawfaremedia.org/article/the-eu-cloud-and-ai-development-act) Lawfare, “The EU Cloud and AI Development Act” (June 2026), reporting Commission estimates of the share of contracts at each assurance level; Cloud Security Alliance, “EU Tech Sovereignty: Cloud Concentration Risk and the Compliance Cascade” (June 2026).

[\[32\]](https://ccianet.org/library/joint-statement-by-international-industry-associations-on-the-cloud-and-ai-development-act-cada-ahead-of-the-telecom-council-of-8-june-2026/) CCIA et al., Joint statement by international industry associations on the Cloud and AI Development Act ahead of the Telecom Council of 8 June 2026 (9 June 2026); Bitkom, Position Paper: Cloud & AI Development Act (July 2026); DIHK, Stellungnahme zum Cloud and AI Development Act (17 September 2026).

[\[33\]](https://digital-strategy.ec.europa.eu/en/policies/european-chips-act) Regulation (EU) 2023/1781 (European Chips Act), entered into force 21 September 2023; European Commission, “European Chips Act” policy page; GAIA-X European Association for Data and Cloud AISBL.

\[34\] Law No. 2016-1691 of 9 December 2016 (Sapin II); Airbus SE, CJIP with the Parquet National Financier, DPA with the UK SFO and DPA with the DOJ (31 January 2020).

[\[35\]](https://eur-lex.europa.eu/eli/reg/2023/2675/oj) Council Regulation (EC) No 2271/96, as amended by Commission Delegated Regulation (EU) 2018/1100 (7 August 2018); Regulation (EU) 2023/2675 (Anti-Coercion Instrument, in force 27 December 2023).

\[36\] Mayer Brown, “PRC Announces New Export Controls on Rare Earth and Battery Materials and Technology” (13 October 2025); White & Case and Freshfields client alerts (October 2025).

[\[37\]](https://cms.law/en/chn/legal-updates/china-expands-reporting-regime-for-export-control-and-adds-14-eu-entities-to-control-list) China Briefing (10 November 2025) on the one-year suspension to 10 November 2026; MOFCOM Announcement No. 23 of 2026 (22 June 2026) and Announcement No. 30 of 2026 (24 July 2026); CMS, “China expands reporting regime for export control and adds 14 EU entities to control list” (August 2026).

[\[38\]](https://www.morganlewis.com/pubs/2026/07/recent-china-export-control-actions-signal-active-enforcement-for-rare-earths-and-strategic-minerals) MOFCOM Announcement No. 26 of 2026 on Further Improving the Reporting and Handling Mechanism for Violations of Export Controls on Strategic-Mineral Dual-Use Items (24 June 2026, effective 1 July 2026); Morgan Lewis, “Recent China Export Control Actions Signal Active Enforcement for Rare Earths and Strategic Minerals” (July 2026).

[\[39\]](https://www.parl.ca/legisinfo/en/bill/45-1/c-22) Parliament of Canada, LEGISinfo, Bill C-22, 45th Parliament, 1st Session, An Act respecting lawful access (Lawful Access Act, 2026): passed by the House of Commons 18 June 2026; first reading in the Senate 18 June 2026; Dentons, “Bill C-22: Strengthening Canada’s lawful access regime” (June 2026).

[\[40\]](https://www.justice.gc.ca/eng/csj-sjc/pl/charter-charte/c22_2.html) Bill C-22, Part 2 (Supporting Authorized Access to Information Act), as passed by the House of Commons; Critical Cyber Systems Protection Act (enacted by Bill C-8), Part 2 (not in force as of 1 October 2026).

[\[41\]](https://judiciary.house.gov/media/in-the-news/house-gop-warns-canada-its-new-cybersecurity-bill-could-pose-privacy-risks) Letter from members of the US House Judiciary Committee to the Minister of Public Safety of Canada regarding Bill C-22 (May 2026).

[\[42\]](https://www.justice.gov/opa/pr/united-states-and-canada-welcome-negotiations-cloud-act-agreement) US Department of Justice, “United States and Canada Welcome Negotiations of a CLOUD Act Agreement” (22 March 2022); CBC News, “Lawful access bill pile-on continues as U.S. lobby group warns Liberals of trade implications” (May 2026).

[\[43\]](https://citizenlab.ca/research/analysis-of-proposed-surveillance-law-expansion-under-bill-c-22/) Citizen Lab, “(Un)forced Errors: Analysis of Proposed Surveillance Law Expansion under Bill C-22, An Act respecting lawful access” (June 2026); Kate Robertson, “Trump Wants to Tap Your Phone. Ottawa Might Let Him”, The Walrus (May 2026); Lawfare, “Chasing Surveillance Powers, Canada Risks the CLOUD Act Deal It Needs” (August 2026).

[\[44\]](https://www.justice.gov/opa/pr/goldman-sachs-charged-foreign-bribery-case-and-agrees-pay-over-29-billion) US Department of Justice, Goldman Sachs 1MDB resolution (22 October 2020); coordinated resolutions in Airbus (January 2020), Odebrecht/Braskem (December 2016) and Glencore (May 2022).

[\[45\]](https://www.faegredrinker.com/en/insights/publications/2026/2/supreme-court-decides-learning-resources-inc-v-trump-and-trump-v-vos-selections-inc) Learning Resources, Inc. v. Trump, No. 24-1287, consolidated with Trump v. V.O.S. Selections, Inc., No. 25-250 (U.S. 20 February 2026).
