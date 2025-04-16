# What's this
raw ideas on what to do as a research project in TAIG

## idea: downstream impact monitoring via harm pattern tracing
**source:** Open Problems in Technical AI Governance, section 3.4.1  
**date:** 2025-04-16

**proposed problem**
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

**what's the idea:**  
instead of trying to predict all downstream effects in advance (which is intractable) we could try to evaluate deployed ai systems by analyzing past harm patterns, tracing influence paths (like content → belief → behavior), and identifying early-warning signs  
borrow from public health / epidemiology mindset: regular monitoring, early detection, targeted intervention

**why it might matter:**  
it’s more realistic than full prediction, and still gives policymakers something actionable. it also creates space for partial interventions that don’t depend on solving society.

**what I'd need to figure out:**  
- how to trace influence paths from AI systems to societal outcomes  
- how to detect early signals of problematic dynamics  
- how to package this insight into governance-relevant outputs

**possible next steps:**  
- [ ] sanity-check it with someone  
- [ ] see if anyone’s done similar work  
- [ ] review concrete cases of harm amplification (e.g. recommendation systems)  
- [ ] try a toy version / write a sketch  
- [ ] sketch out taxonomy of harm propagation patterns  
- [ ] identify intervention points (tech or policy level)
