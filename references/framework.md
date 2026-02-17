# Reality's Moat Framework

## Core Thesis

When building software is free, the only defensible advantage is **scar tissue**: operational knowledge earned in a shifting system where the current state isn't self-explanatory.

Every software product is a ratio: **scar tissue to specifiable code**. When code goes to zero, only scar tissue remains.

---

## Disqualification Table

Before scoring, eliminate claimed advantages that dissolve when code is free.

| Claimed Advantage | Dissolves Because |
|---|---|
| **Scale in commodity features** | Replicated in hours by describing what you need |
| **Proprietary dataset (observational)** | AI trains on equivalents; anyone studies to same answer |
| **Integration complexity** | Rebuilt by describing what you need |
| **Network effects (settled product)** | Switching is free → crowd moves |
| **Code/features** | Anyone can build it |

**Test each claimed advantage:** "If a well-funded team described this to an AI and built it in a weekend, would the advantage survive?" If no → dissolved.

---

## Seven Dimensions

Score each dimension. Use the examples as anchors.

### D1: Scar Tissue Ratio

**Question:** What percentage of the company's value is operational knowledge vs specifiable code?

| Score | Anchor | Example |
|---|---|---|
| **WEAK** (10-30% knowledge) | Product is mostly code/features. Could be rebuilt in a weekend. | Generic SaaS, commodity ML |
| **MODERATE** (40-60%) | Mix of code and domain knowledge. Some operational insight. | Standard vertical SaaS |
| **STRONG** (70-90% knowledge) | Code is the container. Knowledge is the product. | Medical transcription: "The transcription is the container. The scar tissue is the product." |

**Research questions:**
- What does the company actually sell vs what customers think they're buying?
- Strip away the software — what operational knowledge would remain?
- Could a competitor rebuild the product but still fail at the job?

---

### D2: Knowledge Type

**Question:** Does the company's knowledge converge (anyone reaches same answer) or diverge (history-dependent, non-reproducible)?

| Score | Anchor | Example |
|---|---|---|
| **CONVERGING** | Same experiments → same results. Any sufficiently large dataset reaches parity. | Radiology: "A competitor with a different million scans reaches the same diagnostic accuracy" |
| **COUNTDOWN** | Operational but settled. Converges given enough time/funding. IP may extend. | Drug screening: "Given enough time and funding, they converge on the same answers" |
| **DIVERGING** | History-dependent. Same event teaches different companies different things. | Insurance claims: "A newcomer reading today's requirements misinterprets them, because they lack the context" |

**The litmus test:** "Can a well-funded newcomer reach parity by studying the current state of the system? If yes → converging (countdown). If no → diverging (compounds)."

**Research questions:**
- Could a competitor study the company's outputs and reach the same capability?
- Does each year's knowledge make the next year's lessons richer?
- Do two companies experiencing the same market event learn different things?

---

### D3: System Dynamics

**Question:** Is the system the company operates in shifting or settled?

| Score | Anchor | Example |
|---|---|---|
| **SETTLED** | Same inputs → same outputs. Underlying rules don't change. | Biology: "The same molecule hits the same receptor every time" |
| **PERIODIC** | Rules change but predictably. Adaptation doesn't reshape the surface. | Annual compliance updates with clear specs |
| **SHIFTING** | Rules change AND each adaptation reshapes the surface the next change hits. | Payer reimbursement: "each adaptation reshapes the surface the next change hits" |
| | | Cybersecurity: attackers adapt within hours, each defense reshapes the attack surface |

**Key distinction:** A shifting system isn't just "things change." It's that **the company's own adaptations create new failure surfaces** when the next change hits. The system and the company co-evolve.

**Research questions:**
- How often do the rules/standards/adversaries in this market change?
- When they change, does the company's previous adaptation create NEW failure modes?
- Is the current state self-explanatory, or does it only make sense with historical context?

---

### D4: Operational Depth

**Question:** Does the company operate in the system (act and see consequences) or merely observe it (collect data, watch outcomes)?

| Score | Anchor | Example |
|---|---|---|
| **OBSERVATIONAL** | Collects data by watching. Knowledge is in the data, not the process. | Radiology: "images don't change between readings" |
| **OPERATIONAL (settled)** | Acts in system, sees consequences. But system is settled so knowledge converges. | Drug discovery: "you have to run the assay" but biology holds still |
| **OPERATIONAL (shifting)** | Acts in shifting system. Each action generates non-reproducible knowledge. | Claims processing: "each denied claim taught them something specific" |

**The test:** "AI can study anything, but it can't operate for you." Is this company's knowledge the kind AI could learn from data, or must you submit the claim / process the transaction / deploy the code to learn it?

**Research questions:**
- How does the company learn? By watching data or by acting and seeing consequences?
- Could a competitor with access to all the company's data replicate the company's judgment?
- Does each customer interaction generate knowledge that only exists because the interaction happened?

---

### D5: Compounding (Width × Depth)

**Question:** Does the scar tissue compound along both dimensions?

**Width** = more customers/endpoints surface more failure modes from a single system change.
**Depth** = each new change interacts with every previous one, creating interpretive advantage.

| Score | Anchor | Example |
|---|---|---|
| **LINEAR** | More customers = more data, but each datapoint stands alone. | ML training: "You don't need to know what last year's training run looked like" |
| **WIDTH** | Customer combinations surface non-obvious failure modes. | Hospital software: 700 hospitals → ~250,000 pairwise interactions. 50 hospitals → ~1,200. The gap is 200:1, not 14:1. |
| **WIDTH × DEPTH** | Combinations AND history-dependent interpretation. Gap widens superlinearly. | Payments: "newcomer saw a parameter update. Stripe saw a cascade" |

**Research questions:**
- How many customers/endpoints operate in the same shifting system?
- Does one customer's surprise illuminate another's?
- Does the company's history let it interpret new changes differently than a newcomer would?

---

### D6: Verification Moat

**Question:** What is the verification cost × cost of being wrong?

| Score | Anchor | Example |
|---|---|---|
| **LOW × LOW** | Easy to test, cheap to fail. Build-your-own is viable. | Internal tooling, content management |
| **HIGH × LOW** | Expensive to verify but failures are manageable. | Analytics platforms, recommendation engines |
| **HIGH × HIGH** | Expensive to verify AND catastrophic to fail. Maximum scar tissue value. | Payments: "The verification — actually processing transactions across jurisdictions until you've found every failure mode — is not free" |

**Research questions:**
- What would it cost a customer to build their own and verify it works in production?
- What happens when the build-your-own version fails? (Embarrassment vs frozen funds vs denied claims vs security breach)
- How long would production verification take to surface the edge cases this company already knows?

---

### D7: System Replacement Risk (The Chegg Test)

**Question:** Could the entire system be replaced, making the scar tissue worthless?

| Score | Anchor | Example |
|---|---|---|
| **HIGH RISK** | AI or technology could replace the entire system, not just compete within it. | Chegg: "AI didn't just compete with Chegg — it replaced the system" |
| **MODERATE RISK** | Adjacent technology could partially displace the system. | Document management → AI-native workflows |
| **LOW RISK** | System is rooted in physical/regulatory/adversarial reality that can't be replaced. | Payments (banks/regulations), clinical documentation (payers), cybersecurity (human adversaries) |

**The hardest judgment:** "It's whether the world is still shifting within the same system, or replacing it with a different one."

**Research questions:**
- Could AI eliminate the need for the system entirely, not just automate within it?
- Is the system rooted in physical reality, human institutions, or adversarial dynamics?
- If the system were replaced, would any of this company's operational knowledge transfer?

---

## AI Multiplier

"AI is a multiplier on scar tissue: if you have it, AI makes it more valuable. If you don't, AI helps you build the code, but the code was never the product."

After scoring all 7 dimensions, assess: **Does AI deepen this company's moat or dissolve it?**

- **Deepens:** Company has scar tissue + AI compresses reaction time to new surprises → widens gap
- **Neutral:** AI helps both the company and competitors equally
- **Dissolves:** Company's advantage was code/data that AI commoditizes

---

## Archetype Map

| Archetype | D1 Ratio | D2 Knowledge | D3 System | D4 Operational | D5 Compound | D6 Verification | D7 Replacement |
|---|---|---|---|---|---|---|---|
| **Stripe** | STRONG | DIVERGING | SHIFTING | OPERATIONAL (shifting) | WIDTH × DEPTH | HIGH × HIGH | LOW RISK |
| **Chegg** | MODERATE | CONVERGING | SETTLED→REPLACED | OPERATIONAL (settled) | LINEAR | LOW × LOW | HIGH RISK |
| **Epic** | STRONG | DIVERGING | SHIFTING | OPERATIONAL (shifting) | WIDTH × DEPTH | HIGH × HIGH | LOW RISK |
| **Radiology Co** | WEAK | CONVERGING | SETTLED | OBSERVATIONAL | LINEAR | HIGH × LOW | MODERATE RISK |
| **Claims Co** | STRONG | DIVERGING | SHIFTING | OPERATIONAL (shifting) | WIDTH × DEPTH | HIGH × HIGH | LOW RISK |
| **Pharma Co** | MODERATE | COUNTDOWN | SETTLED | OPERATIONAL (settled) | LINEAR | HIGH × HIGH | LOW RISK |

**Use these archetypes as comparison anchors.** "This company most resembles [archetype] because..."

---

## Temporal Assessment

Scar tissue accumulates over time. Where is the company on the curve?

| Stage | Signal |
|---|---|
| **Pre-operational** | Building product, hasn't processed real-world feedback yet |
| **Early accumulation** | Operating but limited history. Knowledge is real but thin. |
| **Compounding** | History enriches new learning. Newcomers face interpretive disadvantage. |
| **Deep moat** | Years of shifting-system operation. Width × depth both significant. |

"The learning rate is set by the speed of the world, not the speed of the agent." — Even with AI, scar tissue can't be rushed.

---

## Why You Can't Simulate Scar Tissue

"Throw a thousand AI agents at the problem" doesn't work. A simulation that actually works wouldn't be a simulation — it would be the system. To simulate is to operate. The bottleneck is time, not intelligence. You cannot learn next year's regulation this year. The learning rate is set by the speed of the world, not the speed of the agent.

## Unbundling

Every company that bundled code with operational knowledge is splitting apart. Code goes to zero; what survives is scar tissue. For incumbents (Salesforce, Workday, ServiceNow): does operational knowledge survive independently when anyone can rebuild the product in a weekend?

## Vertical AI as Moat Ground

Vertical AI companies pick a shifting system and operate within it. Each customer workflow becomes a system action; each action generates scar tissue. Operating across hundreds of customers in the same environment means each customer's surprises compound with every other's. These aren't software products anymore. They're shared operational knowledge, packaged as services.
