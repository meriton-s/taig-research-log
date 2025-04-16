# Paper: Open Problems in Technical AI Governance  
Link: https://arxiv.org/pdf/2407.14981

---

## What's it for

This paper can help to:  
(a) identify areas where intervention is needed,  
(b) evaluate the effectiveness of potential governance actions,  
(c) expand the governance toolbox by designing mechanisms for enforcement, incentives, or compliance.

---

## Key points

### AI Governance & TAIG

- **AI governance** = the processes and structures through which decisions about AI are made, implemented, and enforced.
- **TAIG** = technical tools and analyses that support effective AI governance.

---

### How TAIG contributes to AI governance:

 **Identifying**  
Mapping technical properties of AI systems to social and political concerns, to identify where governance intervention is needed.  
*Example:* Monitoring progress in AI video generation could help predict deepfake risks and prompt earlier policy response.

 **Informing**  
Providing decision-makers with better models, measurements, and explanations, so they can compare and choose governance strategies more effectively.  
*Example:* Better risk models could support more targeted regulation for specific harms.

 **Enhancing**  
Designing technical tools that support enforcement, incentivization, or compliance with governance decisions.  
*Example:* Robust evaluation methods for black-box models could make third-party audits more reliable.

---

## 2D Taxonomy

TAIG is structured along two axes:

 **Capacities** (How to do X)  
A set of technical tools and capabilities that enable stakeholders to analyze and influence AI systems.

**Targets** (What to govern)  
Core components of AI systems — data, compute, models, deployment — that governance efforts aim to affect.

Each capacity can be applied to each target.

### TAIG Capacities (Part of 2D Taxonomy)

Each "capacity" is a type of technical ability that helps governance efforts do their job better.

---

## Capacity: Assessment

**Description:**  
The ability to evaluate AI systems, involving both technical analyses and consideration of broader societal impacts.

**Why it matters for governance:**  
Enables the identification and understanding of system capabilities and risks, allowing for more targeted governance intervention.

**Comment (in plain words):**  
This is about figuring out what an AI system actually does and what it could lead to. Without assessment, you can’t spot risks or control anything.

---

## Capacity: Access

**Description:**  
The ability to interact with AI systems, including model internals, as well as obtain relevant data and information while avoiding unacceptable privacy costs.

**Why it matters for governance:**  
Enables external research and assessment of AI systems, and aids in fairly distributing the benefits of AI across society.

**Comment:**  
Access means being able to look inside the model. Without that, even the smartest experts can’t tell whether it’s working safely.

---

## Capacity: Verification

**Description:**  
The ability of developers or third parties to verify claims made about AI systems’ development, behaviors, capabilities, and safety.

**Why it matters for governance:**  
Establishes trust in AI systems and confirms compliance with regulatory requirements.

**Comment:**  
If someone says “our AI is safe,” it’s nice to be able to check that. Verification means you don’t have to take their word for it — you get proof.

---

## Capacity: Security

**Description:**  
The development and implementation of measures to protect AI system components from unauthorized access, use, or tampering.

**Why it matters for governance:**  
Ensures the integrity, confidentiality, and availability of AI systems and guards against misuse.

**Comment:**  
Without security, AIs can get hacked, faked, or misused. It’s the bare minimum if we want them to do what they’re supposed to do.

---

## Capacity: Operationalization

**Description:**  
The translation of ethical principles, legal requirements, and governance objectives into concrete technical strategies, procedures, or standards.

**Why it matters for governance:**  
Bridges the gap between abstract principles and the practical implementation of regulatory requirements.

**Comment:**  
Stuff like “AI should be fair” doesn’t mean anything unless it can be turned into code. Operationalization means turning rules into real systems.

---

## Capacity: Ecosystem Monitoring

**Description:**  
Understanding and studying the evolving landscape of AI development and application, and associated impacts.

**Why it matters for governance:**  
Enables informed decision-making, anticipation of future challenges, and identification of key leverage points for effective governance interventions.

**Comment:**  
It’s not enough to monitor one model — you need to see the whole picture: who’s building what, how AI is changing society, and where new problems might show up. It’s like radar — without it, you’re flying blind.

---
### TAIG Targets (Part of 2D Taxonomy)

Each "target" is a component of AI systems that governance efforts might want to influence or regulate.

---

## Target: Data

**Description:**  
The pretraining, fine-tuning, retrieval, and evaluation datasets on which AI systems are trained and benchmarked.

**Why it matters for governance:**  
Data defines what an AI learns. Biased, poor-quality, or unsafe data can lead to dangerous outcomes. Controlling and auditing data is key to ensuring responsible development.

**Comment (in plain words):**  
Garbage in — garbage out. If we don’t control what the model trains on, we don’t control what it does.

---

## Target: Compute

**Description:**  
Computational and hardware resources required to develop and deploy AI systems.

**Why it matters for governance:**  
Compute is a gatekeeper. Tracking who has access to large-scale compute helps monitor the development of frontier models and manage proliferation risks.

**Comment:**  
AI doesn’t appear out of nowhere. It needs powerful hardware. Whoever controls compute, controls who can train what.

---

## Target: Models and Algorithms

**Description:**  
Core components of AI systems, consisting of software for training and inference, their theoretical underpinnings, model architectures, and learned parameters.

**Why it matters for governance:**  
These are the “brains” of AI. Governing how they’re built, shared, and modified is central to ensuring safety and accountability.

**Comment:**  
This *is* the AI — its algorithms, architecture, and what it has learned. If we want to govern AI, we need to understand and check what's inside.

---

## Target: Deployment

**Description:**  
The use of AI systems in real-world settings, including user interactions, and the resulting outputs, actions, and impacts.

**Why it matters for governance:**  
Even safe-looking models can cause harm when deployed at scale. Governance must track not just design, but real-world effects.

**Comment:**  
It’s not just how the model is built — it’s how it’s used. Even good models can do harm if deployed carelessly.

## 3.1 Assessment
- assessment is key to ai governance — helps catch risks early  
- real-world examples: red-teaming (bletchley), eval sharing (white house eo)  
- goal: detect harm, ensure safety, robustness, fairness  
- problem: evals for foundation models are still messy and expensive  
- some standards exist (nist, uk safety institute), but core issues remain

### my thoughts

- current evals tell us what a model *can* do — not what it *can’t*  
- but safety guarantees depend on knowing what a model is **incapable** of doing  
- no existing benchmark directly tells us “this behavior is impossible”  
- still, benchmarks and red-team demos are valuable — we should do more of them  
- seems worth thinking about how to move from observed behavior to bounds on unobserved behavior  
- might be worth framing as: what’s the tightest safe assumption we can extract from a noisy eval

### related research questions (from the paper)

- how to scale detection of problematic data to trillions of tokens?  
- how to automate license collection + validation?  
- how to flag harmful data without direct access to full dataset?  
- how to detect contamination of training data?  
- how to remove harmful data without leaking info about what was removed?  
- what reporting standards (license + metadata) are useful?  
- what infra do researchers need to audit huge datasets?  
- how to measure persistent bias at scale?  
- how to tell if a dataset is fit for training?  
- how does bad data affect downstream behavior?  
- can we trace specific behavior back to specific data?

## 3.4.1 — downstream impact

### summary

- model performance in isolation ≠ real-world impact  
- we need ways to evaluate ai systems *in use*, not just in test conditions  
- policymaker decisions depend on having that real-world picture  
- current proxies (e.g. fairness metrics) miss actual societal effects  
- hard to test across languages, contexts, cultures — takes time and coordination  
- early taxonomies exist but we don’t have good methods yet  
- real impact eval needs nuance, interdisciplinarity, inclusion

### proposed problem:  
how can we reliably predict and measure the real-world, downstream societal impacts of AI systems — including harm, inequality, and cultural shifts — given the complexity, scale, and interdisciplinary nature of these effects?

### my thoughts

it’s really hard to predict downstream impact — and not just because we don’t try hard enough  
if we frame it as a technical problem with a full solution, it becomes intractable — we’d need a full model of society  
and we don’t have that. nowhere close

so what might be doable instead?  
borrow ideas from fields that deal with complex systems under uncertainty — like medicine  
we don’t try to predict a person’s entire medical future at age 5 based on their DNA  
instead we do annual checkups — catch early signs, look for patterns

maybe we can do the same here:  
look at ai systems already deployed, figure out what impacts we’re already seeing  
for example — youtube amplified flat-earth content → built filter bubbles → boosted antivax memes → possibly worsened pandemic outcomes  
each step needs fact-checking, but this is the kind of pattern we might want to trace and generalize

once we have the pattern, we can ask:  
- what could have warned us?  
- how would we notice a similar thing happening elsewhere?  
- what would help avoid it?  
not “better metrics” in general — if youtube had a metric that worked for this, they’d probably use it  
maybe we need wrapper systems that don’t purely optimize engagement but also avoid failure modes, without hurting the platform’s bottom line

### idea stub (to move to ideas.md)

evaluate deployed ai systems by analyzing past harm patterns, tracing influence paths (like content → belief → behavior), and identifying early-warning signs  
borrow from public health / epidemiology mindset: regular monitoring, early detection, targeted intervention

---

