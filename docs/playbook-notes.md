# GRC AI Playbook — Field Notes

Running log of what worked, what failed, and what required human correction. One dated entry per day. New entries appended at the bottom.

---

# Banking GRC AI Playbook - Working Notes

This is a running log of what I learn while building the toolkit. Honest 
notes, not polished writing. Will be consolidated into the published 
Playbook on Day 12.

---

## Day 1 - 2026-05-19

### Where AI helped today
- Scaffolded the repo folder structure from a single prompt
- Drafted the NIST CSF 2.0 overview in roughly five minutes. From scratch, this would have taken me 90 minutes of writing and another 30 minutes of formatting
- README v0.1 came out coherent and usable on the first pass. I edited 
  the "why this exists" section in my own voice but the rest held up
- Markdown formatting was clean, no manual cleanup


### Where AI failed or hallucinated
- Got the C-SCRM history wrong. Claimed it was a single subcategory in 
  CSF 1.1. The truth is it was a full category (ID.SC) under Identify 
  with five subcategories. Caught it during review because I have ten 
  years of GRC experience. A junior practitioner would have missed it 
  and shipped a credibility-damaging error.
- Made an unverified claim that NIST published a CSF 2.0 to FFIEC CAT 
  crosswalk. Could not confirm the source. Likely the FFIEC published 
  their own mapping, not NIST. References section is fixed.
- Cited an FFIEC CAT sunset announcement date of March 2024 without a 
  primary source. Only the August 31, 2025 effective date is verified. 
  Replaced the announcement date claim with the verified effective date

### Prompt patterns that worked
- Specifying exact structure ("section 1 covers X, section 2 covers Y")
- Naming the audience ("for a banking GRC practitioner who already 
  knows the basics")
- Banning marketing language explicitly ("no fluff, no buzzwords, plain 
  professional English")
- Pointing to a specific file path for the output
- Telling it to add citations at the end of any factual document

### Anti-patterns and traps
- Trusting AI on regulatory specifics without verification. Same trap as approving a junior analyst's first draft of a board pack without  reading it. You sign it, you own it. The examiner does not care that AI wrote it. 
- Not keeping the primary source documents (NIST CSF 2.0 PDF, official 
  publications) open in tabs while prompting. Made it harder to spot 
  the C-SCRM error in real time. Tomorrow I will open the source docs 
  before I start prompting

### Validation steps I had to do manually
- Cross-checked the C-SCRM CSF 1.1 structure against NIST and third 
  party sources before accepting the overview as final
- Will need to verify every NIST subcategory ID I cite in the mapping 
  engine module starting Day 3
- Decision for the rest of the project: any regulatory claim, framework identifier, date, or numeric count goes through manual verification against an authoritative source before it lands in a committed file.

### Banking-specific gaps in AI output
- AI did not anchor on the US banking context naturally. It treated 
  CSF 2.0 as a general framework adoption story. I had to keep 
  redirecting it to the examiner angle and the FFIEC CAT transition.
- The default vocabulary was generic GRC and cloud-vendor flavored. 
  Banking has its own language. I will need to feed this vocabulary explicitly in every banking-relevant prompt for the rest of the project.

### My reflection
AI behaves like a fast, confident junior analyst with broad knowledge 
and zero accountability. Senior judgment has to sit on top of it. The 
risk is not that AI is wrong. The risk is that AI sounds right when 
it is wrong. In a regulated industry, that gap is exactly where 
examination findings come from.

For this project to be credible, my QA layer has to be visible in 
the final Playbook. Not just what AI produced, but what I caught 
and corrected. That is the differentiator. Anyone can paste a prompt. 
Showing the corrections is what proves the practitioner is in charge 
of the AI, not the other way around.

### Day 1 time breakdown (rough)
- Setup, Git, GitHub, repo, environment fixes: 2 hours
- Claude Code prompting and content generation: 1.5 hours
- Manual review, verification, edits: 1 hour
- Playbook notes (this file): 30 minutes
Total: 5 hours

---

## Day 2 - 2026-05-21

### Where AI failed or hallucinated

Block 3 surfaced three categories of AI error in framework descriptions:

1. **Specific dates wrong** (PCI DSS v4.0.1 publication; v4.0 retirement). Pattern: AI guesses dates when uncertain rather than flagging uncertainty.

2. **Imprecise regulatory vocabulary** ("mandatory" for SOC 2 Security). Pattern: AI doesn't distinguish regulatory mandate from voluntary scope selection. Senior practitioners do.

3. **Structural errors on niche frameworks** (CRI Profile: wrong version, missed Extend function, made unsupported universal claims). Pattern: AI quality drops sharply on frameworks with smaller training-data footprint. CRI Profile is well-documented publicly but less prominent than NIST CSF or PCI DSS.

**Mitigation:** For any framework less prominent than the top-tier standards (NIST CSF, ISO 27001, PCI DSS, SOC 2), assume AI output requires line-by-line source verification before commit. Build the verification step into the prompt itself by requiring source citations at the end of every factual claim.

**Specific examples from Block 3:**

- **Date precision:** PCI DSS v4.0.1 publication came back as March 2024; the correct date is June 11, 2024. CRI Profile version came back as 2.0; current version is 2.2. AI guesses confidently rather than flagging uncertainty.

- **Regulatory vocabulary:** SOC 2 Security is not mandatory. SOC 2 is voluntary; Security is the only universally included Trust Services Category *when the engagement happens*. The word "mandatory" is technically wrong and a senior reviewer catches it instantly.

- **Universal and negative claims:** AI wrote "every CSF 2.0 subcategory maps to CRI" and "the inverse does not occur" with no source. Asserting universals and asserting negatives are both red flags when reviewing AI output on any framework.

**Senior practitioner takeaway:** AI quality drops sharply on frameworks with smaller training-data footprint. For banking GRC, the widely-documented standards (NIST CSF, PCI DSS, SOC 2, ISO 27001) get a light review. The banking-specific material (CRI Profile, FFIEC handbooks, OCC bulletins, SR letters, NYDFS 500, GLBA Safeguards) gets line-by-line verification against primary sources. This is exactly where ten years of practitioner experience earns its keep. AI does the typing. The practitioner does the judgment.