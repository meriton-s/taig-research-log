# What's this
raw ideas on what to do as a research project in TAIG

## project 1 — tracing ai impact on user behavior  
**source:** Open Problems in Technical AI Governance, section 8.1 + 8.2

goal:  
look for changes in user behavior on large platforms where ai has been embedded for a while  
especially in domains where changes actually matter socially (e.g. health, politics, belief formation)

steps:  
- gather behavioral data (if public) from socially significant platforms (e.g. youtube, tiktok)  
- map timelines of ai feature rollouts / notable events  
- check if any user behavior shifts match those events  
- if yes, apply causal inference tools to separate out other causes  
- if still yes, think from first principles: why does ai affect people that way?

**status**: sounds feasible but depends on data access + narrowing scope  
**priority**: high

---

## project 2 — forecast falsification  
**source:** Open Problems in Technical AI Governance, section 8.2

goal:  
start from popular ai impact forecasts (slow takeoff, socio-political disruption, etc) and ask:  
what kind of observations would *falsify* these scenarios?

steps:  
- collect widely cited forecasting papers or scenarios people actually plan around  
- extract their assumptions and implied predictions  
- figure out what real-world data would contradict those  
- search for signals that break (or match) expectations

**status**: depends on data access, mostly conceptual, can be started solo  
**priority**: medium

---

## project 3 — ai pervasiveness + misuse risk  
**source:** Open Problems in Technical AI Governance, section 8.1 + 3.4.1

goal:  
find out where ai is most embedded in ordinary people’s lives  
then analyze what kind of misuse risk that creates

steps:  
- scan recent work on ai adoption across life domains  
- identify sectors with high engagement + low visibility (e.g. productivity tools, translation, etc)  
- ask: what kinds of misuse are most plausible here?  
- maybe map to an infosec/system risk taxonomy (domestic misuse, social engineering, etc)  
- could recruit someone with stats background to help scan data faster (e.g. veronika’s students)

**status**: partially scouted, needs literature pass + risk framing  
**priority**: medium-high

---

## project 4 — when shutdown isn’t an option  
**source:** Open Problems in Technical AI Governance, section 7.2

goal:  
tackle the fact that “just turn it off” often isn’t feasible for deployed systems

notes:  
- O’Brien et al. have mapped governance-side responses (access limits, feature blocks, shutdowns etc)  
- question is: can we do anything at the system level itself?

core question:  
→ how to design AI systems with soft shutdown modes or fallback states?

**status**: no clear research plan yet. still feels above my current level.  
but the idea won’t leave me alone, so keeping it here.  
**priority**: low for now, but conceptually important

---

## high-level reasoning behind all this

it’s really hard to predict downstream impact — and not just because we don’t try hard enough  
if we frame it as a technical problem with a full solution, it becomes intractable — we’d need not only deep knowledge about AIs but also a full model of society  
and we don’t have that. nowhere close

so what might be doable instead?  
borrow ideas from fields that deal with complex systems under uncertainty — it is already happening in many ways but still a lot of things are to be done  
take medicine — we don’t try to predict a person’s entire medical future at age 5 based on their DNA  
instead we do annual checkups — catch early signs, look for patterns

maybe we can do the same here:  
look at ai systems already deployed, figure out what impacts we’re already seeing (check social studies about media from the last 2 years?)  
might be something like this:  
youtube amplified flat-earth content → built filter bubbles → boosted antivax memes → possibly worsened pandemic outcomes  
each step needs fact-checking, but this is the kind of pattern we might want to trace and generalize

once we have the pattern, we can ask:  
- what could have warned us?  
- how would we notice a similar thing happening elsewhere?  
- what would help avoid it?  
not “better metrics” in general — if youtube had a metric that worked for this, they’d probably use it  
maybe we need wrapper systems that don’t purely optimize engagement but also avoid failure modes, without hurting the platform’s bottom line

---

## for each project — things to figure out

- sanity-check it with someone with good first principle reasoning  
- check if it's already been done  
- determine + write down: how within this project am i going to trace influence paths from AI systems to societal outcomes  
- determine + write down: how to detect early signals of problematic dynamics  
- determine + write down: how to package this insight into governance-relevant outputs

