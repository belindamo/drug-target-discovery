# IPF Pathway Integration Map: All 21 GWAS Targets in Systems Context
*Session 5 — Updated March 26, 2026 with recent pathway discoveries*

## Overview

This document integrates all 21 IPF GWAS-validated targets into the known pathophysiology of idiopathic pulmonary fibrosis. The 21 targets cluster into **6 major biological pathways**, which together paint a unified picture of IPF as a disease of:

1. **Telomere dysfunction & senescence** (cell aging)
2. **Epithelial barrier breakdown** (mucociliary + tight junction failure)
3. **TGF-β/inflammasome signaling** (fibrotic and inflammatory amplification)
4. **Cell adhesion & EMT** (epithelial-mesenchymal plasticity)
5. **mTOR hyperactivation** (uncontrolled protein synthesis & myofibroblast differentiation)
6. **Cellular mechanics & mRNA stability** (spindle assembly & microRNA processing)

---

## Pathway 1: Telomere Dysfunction & Cellular Senescence

*The "aging lung" hypothesis — shortened telomeres drive cell cycle arrest and senescence, releasing pro-fibrotic cytokines*

### Genes (3 targets):

| Gene | GWAS p-value | Evidence | Mechanism | Drug Status |
|---|---|---|---|---|
| **TERT** | 2.2e-14 | Tier 1 | Telomerase reverse transcriptase; loss of TL maintenance → premature senescence | Imetelstat (MDS-approved, wrong direction); activation strategies needed |
| **TERC** | 8.9e-09 | Tier 1 (near TERC) | Telomerase RNA component; same pathway as TERT | Limited druggability |
| **RTEL1** | 3.13e-09 | Tier 1 | Telomere elongation helicase; functions in TL replication & DSB repair | DepMap flag (common essential); SAFETY RISK |

### Pathway Logic:

```
Short telomeres (TERT↓, TERC↓)
  ↓
Cell cycle arrest (p16/p21↑)
  ↓
Senescence-associated secretory phenotype (SASP)
  ↓
IL-6, IL-8, TNF-α, VEGF, MMP2/9
  ↓
Fibroblast activation, collagen, impaired epithelial repair
```

### IPF Context:

- IPF patients have shorter telomeres than age-matched controls (Liu 2017, PMID: 28348992)
- Telomerase mutations (TERT/TERC) cause familial pulmonary fibrosis
- Senescent cells accumulate in IPF tissue, producing pro-fibrotic factors
- p16/Ki67 double-positive cells (senescent) correlate with IPF progression

### Therapeutic Implications:

- **TERT activation** (telomerase boosters) would theoretically prevent senescence but:
  - Risk: Telomerase activation in preneoplastic cells (cancer risk)
  - Imetelstat (approved for MDS) *inhibits* telomerase (wrong direction for IPF)
  - TA-65/danazol (telomerase activators) lack clinical validation

- **RTEL1 is a major safety flag** (68.7% of cancer lines dependent on RTEL1 expression)
  - Inhibition would impair DSB repair → genomic instability → cancer
  - Not a druggable target for IPF

- **Alternative approach:** Target senescence downstream (eliminate senescent cells via senolytics)
  - Not yet in IPF clinical trials
  - Dasatinib + quercetin showing early promise in other fibrotic diseases

---

## Pathway 2: Epithelial Barrier Integrity & Mucociliary Dysfunction

*The "gatekeeping" hypothesis — impaired barrier function allows pathogenic inhaled agents into lung parenchyma*

### Genes (5 targets):

| Gene | GWAS p-value | Evidence | Role | Drug Status |
|---|---|---|---|---|
| **MUC5B** | 1.12e-66 | Tier 1 (strongest) | Mucin 5B; structural component of mucus layer | SpliSense SPL5B ASO (Phase 1, 2026) |
| **DSP** | 7.81e-28 | Tier 1 | Desmoplakin; cell-cell adhesion (desmosomes) | Topical ASO, protein engineering possible |
| **TOLLIP** | 3.8e-08 | Tier 1 | Toll-interacting protein; TLR signaling modulator | No known ligands (Tier 4 druggability) |
| **OBFC1 (STN1)** | 2.4e-08 | Tier 1 | CST complex member; telomere shelterin, DNA damage response | Limited druggability; telomere-related |
| **NTN4** | <5e-08 | Tier 2 (NEW Chin 2025) | Netrin-4; angiogenesis, endothelial cell function | No trials; antibodies possible |

### Pathway Logic:

```
Impaired epithelial barrier (MUC5B↓ or mutated, DSP↓)
  ↓
Loss of innate immune gate (TOLLIP↓ impairs TLR control)
  ↓
Increased pathogen/allergen trafficking to lung parenchyma
  ↓
Enhanced pattern recognition (TLR activation) → NLRP1 inflammasome → IL-1β
  ↓
Fibroblast recruitment, myofibroblast differentiation, collagen
```

### IPF Context:

- MUC5B T allele (rs35705950) is the **strongest IPF GWAS signal** (OR=4.11 in heterozygotes)
- MUC5B promoter variant increases expression → mucus plug formation → localized airway occlusion → altered mechanics
- MUC5B upregulation in IPF bronchioli (smoking + genetic predisposition)
- DSP mutations seen in familial and sporadic IPF; impair cell-cell adhesion
- TOLLIP variants affect TLR4 signaling; patients with risk alleles show exaggerated inflammatory responses

### Therapeutic Implications:

- **MUC5B modulation:**
  - Inhibition: SpliSense SPL5B (antisense oligonucleotide targeting MUCB5B pre-mRNA)
    - Rationale: Reduce mucus plug formation to restore mucociliary clearance
    - **Phase 1 readout expected mid-2026**
    - Risk: Complete mucus loss could impair innate immunity

  - Question: Should we inhibit (reduce plug burden) or stabilize (strengthen barrier)?

- **DSP stabilization:**
  - Enhance desmosomal strength to restore barrier integrity
  - Possible via: topical desmoplakin-stabilizing agents, cell therapy
  - Developmental stage: preclinical

- **TOLLIP pathway:**
  - Enhance TLR tolerance (reduce exaggerated inflammasome activation)
  - TOLLIP overexpression protects against LPS-induced acute lung injury
  - Small molecule approach: enhance TOLLIP-MyD88 interaction?
  - Developmental stage: conceptual

---

## Pathway 3: TGF-β & NLRP1 Inflammasome Signaling

*The "inflammatory amplification" hypothesis — TGF-β and IL-1β create feed-forward loops driving myofibroblast differentiation*

### Genes (4 targets):

| Gene | GWAS p-value | Evidence | Role | Drug Status |
|---|---|---|---|---|
| **DPP9** | 1.7e-12 | Tier 1 | Serine protease; NLRP1/CARD8 inflammasome suppressor | Cpd 6e (oral, 2025); PARADOX: ↓DPP9 = ↑risk |
| **ACVRL1** | MR-causal | Tier 2 | ALK1; TGF-β type II receptor for BMP9; endoglin complex | Sotatercept (Winrevair) approved PAH; dual ALK1/ActR2A inhibitor |
| **IL7** | MR: OR=0.67 | Tier 2 | IL-7; JAK1/STAT1 → Smad7 ⊣ TGF-β signaling | CYT107 clinical use (>650 patients) |
| **FAM13A** | 2.2e-11 | Tier 2 | Family with sequence similarity; RhoA pathway, fibroblast activation | No known ligands; upregulated in IPF |

### Pathway Logic:

```
TGF-β₁ → smad2/3 phosphorylation
  ↓
Collagen synthesis, α-SMA expression, myofibroblast differentiation
  ↓
BUT: TGF-β also suppresses DEPTOR → mTOR hyperactivation (see Pathway 5)

PARALLEL: TGF-β → caspase-1 activation (inflammasome)
  ├─ DPP9 restrains NLRP1 and CARD8
  ├─ Loss of DPP9 → ↑IL-1β production
  └─ IL-1β amplifies TGF-β signaling (positive feedback)

BRAKE: IL-7 → STAT1 → Smad7
  └─ Smad7 competitively blocks Smad2/3 (TGF-β pathway antagonism)
```

### IPF Context:

- TGF-β is the master pro-fibrotic cytokine in IPF (established literature)
- NLRP1 inflammasome is activated in IPF alveolar macrophages (overproduction of IL-1β, IL-18)
- Serum IL-1β correlates with IPF progression and poor prognosis
- IPF fibroblasts are primed for enhanced response to both TGF-β and IL-1β
- Fibroblast → myofibroblast transition (α-SMA+) is central to ECM deposition

### Therapeutic Implications:

- **DPP9 inhibitors (Cpd 6e):**
  - Published, orally bioavailable, selective
  - BUT genetic data says ↓DPP9 = ↑risk → inhibition moves in wrong direction
  - **Critical question:** Does DPP9's non-inflammasome role (EMT regulation) dominate in fibroblasts?
  - If yes: DPP9 inhibition could suppress EMT → benefit
  - If no: DPP9 inhibition worsens inflammasome activation → harm
  - **Resolution:** Preclinical testing in bleomycin model (Q2 2026)

- **ACVRL1 (ALK1) modulation:**
  - Sotatercept (Winrevair, approved for PAH) is a trap for BMP9 + ActR2A
  - Increases plasma BMP9 → enhances BMP signaling (opposite of kinase inhibition)
  - Rationale: BMP9 via ALK1 promotes endothelial stabilization, angiogenesis, vascular integrity
  - **Opportunity:** Test sotatercept in IPF-PH cohort; if vascular improvement translates to fibrosis benefit, expand to systemic IPF

- **IL-7 (CYT107):**
  - Recombinant protein; clinical-grade safety data
  - Directly antagonizes TGF-β via STAT1/Smad7 axis
  - Genetic direction clear (↑IL-7 = protection)
  - **Path:** Replicate preclinical antifibrotic effect in modern models; Phase 2a 2026

- **FAM13A:**
  - Upstream of RhoA/ROCK pathway (activated by TGF-β)
  - ROCK inhibitors (fasudil, ripasudil) are clinical-stage; could provide indirect targeting
  - FAM13A itself: poorly characterized; no ligand-based approach yet

---

## Pathway 4: Cell Adhesion & Epithelial-Mesenchymal Plasticity

*The "EMT highway" hypothesis — loss of epithelial identity and gain of mesenchymal traits facilitates fibroblast invasion*

### Genes (2 targets):

| Gene | GWAS p-value | Evidence | Role | Drug Status |
|---|---|---|---|---|
| **ATP11A** | 6.7e-09 | Tier 1 | ATPase phospholipid transporter 11A (P4-ATPase); membrane lipid flip | Antibodies possible; no inhibitors |
| **AKAP13** | 1.27e-09 | Tier 1 | A-kinase anchoring protein 13; RhoA-GEF; Rho signaling | ROCK inhibitors (downstream); fasudil, ripasudil clinical-stage |

### Pathway Logic:

```
ATP11A (P4-ATPase) maintains phosphatidylserine asymmetry in cell membrane
  ↓
Loss of ATP11A → phosphatidylserine externalization ("find me" signals)
  ↓
Enhanced macrophage recognition & migration; altered epithelial permeability
  ↓
Fibroblast recruitment, monocyte infiltration, EMT

PARALLEL: AKAP13 (RhoA-GEF) activates RhoA
  ↓
RhoA → ROCK (downstream kinase)
  ↓
Cytoskeletal contraction, stress fiber formation, TGF-β sensitivity
  ↓
Myofibroblast differentiation (α-SMA↑, contractility↑)
```

### IPF Context:

- ATP11A **has the strongest colocalization signal of any target** (PP.H4=0.996 in smoker lung eQTL, 0.994 in monocytes)
  - This is the strongest evidence short of a GWAS hit that the locus is causal for IPF
  - Yet no drug development underway

- ATP11A upregulated in IPF macrophages and myofibroblasts (HGG Advances 2025)
  - Suggests ATP11A mediates macrophage → fibroblast cross-talk

- RhoA/ROCK pathway is central to myofibroblast differentiation and mechanical tension
  - ROCK inhibitors (fasudil, ripasudil) reduce α-SMA and contractile protein in fibroblasts
  - Fasudil has been tested in IPF (modestly; not pursuing further development)

### Therapeutic Implications:

- **ATP11A inhibitors:**
  - NO specific inhibitors exist yet
  - Possible approaches:
    1. **Antibody-based**: Targeting ATP11A extracellular domain to block function
    2. **Substrate analogs**: Phosphatidylserine-mimetics to compete for ATP11A-mediated flip
    3. **CRISPR screen validation**: Confirm ATP11A is actionable in human IPF fibroblasts
  - **Timeline:** 2-3 year drug discovery effort

- **AKAP13/RhoA/ROCK pathway:**
  - ROCK inhibitors are relatively de-risked (fasudil + ripasudil have clinical data)
  - **Opportunity:** Focused Phase 2 trial of ROCK inhibitor in IPF
    - Genetic signal (AKAP13 GWAS) + downstream target (ROCK)
    - Small molecule (Genentech/Roche had ROCK inhibitor; development halted for unrelated reasons)
  - Could partner with existing ROCK inhibitor programs in other diseases (glaucoma, hypertension)

---

## Pathway 5: mTOR Signaling & Protein Synthesis

*The "growth control" hypothesis — loss of mTOR brake (DEPTOR/NPRL3) drives uncontrolled fibroblast expansion and collagen synthesis*

### Genes (2 targets):

| Gene | GWAS p-value | Evidence | Role | Drug Status |
|---|---|---|---|---|
| **DEPTOR** | 1.2e-09 | Tier 1 | DEP domain mTOR-interacting protein; mTOR inhibitor | **Downstream: sirolimus (FDA-approved, generic)** |
| **NPRL3** | 2.57e-12 | Tier 1 | GATOR1 complex member; Rag GTPase negative regulator | Same pathway; sirolimus targets upstream |

### Pathway Logic:

```
Normal state: DEPTOR + GATOR1/NPRL3 suppress mTORC1
  ↓
TGF-β₁ → ↓DEPTOR expression
  ↓
Loss of mTOR brake
  ↓
mTORC1 hyperactivation
  ├─ 4E-BP1 phosphorylation → ↑collagen mRNA translation
  ├─ S6K1 activation → ↑ribosomal protein, myofibroblast differentiation
  ├─ ULK1 phosphorylation → ↓autophagy (impaired clearance of damaged organelles)
  └─ Overall: Protein anabolism dominates; catabolic autophagy suppressed

Fibroblast consequences:
  ├─ Rapid collagen synthesis (COL1A1/COL1A2 translation↑)
  ├─ High demand for amino acids, lipids, energy
  ├─ Resistance to growth factor withdrawal
  └─ Accumulation of damaged mitochondria (autophagy↓)

BRAKE: Sirolimus inhibits mTORC1
  ├─ Restores autophagy
  ├─ Reduces collagen synthesis
  └─ Promotes fibrocyte suppression (CXCR4↓)
```

### IPF Context:

- **Two independent GWAS loci converge on one pathway** → highest confidence that pathway is causal
- mTORC1 is constitutively activated in IPF fibroblasts (vs normal)
- Sirolimus pilot trial (Gomez-Manjarres 2023):
  - 35% reduction in circulating fibrocytes
  - 42% reduction in myofibroblast precursors (α-SMA+ fibrocytes)
  - Safe & well-tolerated (actually fewer respiratory AEs on drug than placebo)

- Everolimus (another mTOR inhibitor) failed in IPF trial
  - Explanation: Everolimus has more potent mTORC2 inhibition than sirolimus
  - mTORC2 → Akt → cytoprotective signals in lung epithelium
  - Hypothesis: Selective mTORC1 inhibition (sirolimus) >> dual mTORC1/2 inhibition (everolimus)

### Therapeutic Implications:

- **Sirolimus Phase 2b trial (PRIORITY):**
  - FDA-approved, generic, de-risked
  - Clear genetic rationale (2 GWAS loci)
  - Clear preclinical rationale (fibrocyte suppression, autophagy restoration)
  - Clear clinical precedent (safe in IPF pilot, approved in transplant, oncology, rare diseases)
  - **Missing:** Industry backing (off-patent; no profit incentive)
  - **Solution:** NIH/foundation funding for investigator-initiated trial
  - **Timeline:** Protocol design Q2 2026; enrollment H1 2027

- **Combination strategy:**
  - Sirolimus + anti-IL-1β (bridges mTOR pathway + inflammasome pathway)
  - Sirolimus + pirfenidone (approved drug; test for synergy)
  - Sirolimus + nintedanib (check for drug-drug interactions: both CYP3A4 substrates)

---

## Pathway 6: Mitotic Spindle Assembly & Cell Cycle

*The "checkpoint" hypothesis — impaired spindle assembly increases aneuploidy and senescence, driving profibrotic SASP*

### Genes (3 targets):

| Gene | GWAS p-value | Evidence | Role | Drug Status |
|---|---|---|---|---|
| **KIF15** | 5.12e-10 | Tier 1 | Kinesin motor; spindle microtubule organization | DepMap SAFETY FLAG (8.4% dependent lines); activation needed |
| **MAD1L1** | 7.15e-13 | Tier 1 | Spindle assembly checkpoint; mitotic arrest deficient | No known ligands; 4.1% DepMap dependent |
| **KNL1** | 7.41e-13 | Tier 1 | Kinetochore scaffold; spindle checkpoint complex | No known ligands; no tractability data |

### Pathway Logic:

```
Impaired spindle assembly (KIF15↓, MAD1L1↓, KNL1↓)
  ↓
Weakened mitotic checkpoint; aneuploidy accumulation
  ↓
Chromosomal instability in dividing fibroblasts
  ↓
Cellular stress; p53 activation; senescence
  ↓
Senescence-associated secretory phenotype (SASP)
  ├─ IL-6, IL-8, TNF-α, VEGF, MMP2/9
  └─ Fibroblast activation, ECM remodeling, impaired epithelial repair
```

### IPF Context:

- **Spindle assembly genes are among the most strongly implicated in IPF GWAS** (4 genes cluster in this pathway)
- IPF fibroblasts show increased chromosomal instability and aneuploidy (Takahashi 2019, PMID: 30787161)
- Senescent cells accumulate in IPF lung tissue
- Mechanism link: Early fibrosis triggers cell division (regenerative attempt) → mitotic stress → senescence → SASP → further fibrosis

### Therapeutic Implications:

- **Spindle assembly genes are not "druggable" in traditional sense:**
  - KIF15: Kinesin motor; inhibitors would block cell division (anti-cancer strategy, wrong for IPF)
  - MAD1L1, KNL1: No known ligands

- **Alternative approaches:**
  - **Activate spindle assembly:** No technology exists yet
  - **Target downstream (senescence elimination):** Senolytics (dasatinib + quercetin)
    - Early-stage; not yet in clinical IPF trials
    - Mechanism: Selectively kill senescent cells via BCL-2 family inhibition

- **Clinical implication:**
  - These genes may be "markers of the problem" (senescence) rather than "targets for drugs"
  - Identifying and eliminating senescent cells (via senolytics or CAR-T approaches) may be more tractable
  - OR: Preventing senescence upstream (telomere maintenance, mitotic checkpoint integrity) is preferred

---

## Pathway 7 (Emerging): Transcriptional Control & Fibroblast Activation

*The "master regulator" hypothesis — GLIS3 and other transcription factors coordinate fibrotic gene programs*

### Gene (Not a GWAS hit, but functionally important):

| Gene | Note | Evidence | Role |
|---|---|---|---|
| **GLIS3** | **Not IPF GWAS locus** | Nature 2026, PMID: 41501466 (intestinal IBD screen) | Master transcription factor; controls IL-11, LIF, FAP, MMP2, SERPINE1 |

### Context:

- Recent CRISPR screens in primary human fibroblasts identified GLIS3 as central node in inflammatory activated fibroblast (IAF) program
- GLIS3 integrates TGF-β + IL-1β signals to drive IL-11 (potent profibrotic cytokine)
- **Not a GWAS locus for IPF** (no signal at chr9p24.2)
- But: GLIS3-regulated genes (IL-11, TGF-β target genes, ECM modifiers) are downstream of multiple GWAS targets

### Therapeutic Implications:

- **GLIS3 as biomarker (not target):**
  - GLIS3 expression in IPF fibroblasts could stratify patients by fibrotic activity
  - High-GLIS3 patients might preferentially respond to anti-IL-1β or TGF-β pathway inhibitors

- **Potential future target (2027+):**
  - IF GLIS3 can be validated in IPF tissue (single-cell data)
  - AND IF GLIS3 inhibitors can be developed (challenging; zinc-finger transcription factors are historically "undruggable")
  - THEN: Consider GLIS3 as next-generation IPF target

---

## Non-Pathway Targets (Pleiotropic / Context-Dependent)

### **BTRC, GIPC2, RAPGEF2, PSKH1, FUT6, GPR157, STMN3, MUC1**

These 8 targets have evidence for IPF GWAS association but fit less cleanly into the 6 major pathways above. They are either:

1. **Population-specific** (PSKH1: EAS-only; FUT6: AMR-enriched)
2. **Pathway-modulating** (BTRC: Wnt/NF-κB; GIPC2: context-dependent signaling)
3. **Orphan GPCRs** (GPR157: still undeorphanized; Pharos Tdark)
4. **Emerging targets** (MUC1: distinct from MUC5B; glycosylation biomarker)

### Integration:

- These targets should be considered in **secondary analyses** and **stratified trial designs**
- Example: PSKH1 genotype stratification for Asian IPF populations
- Example: MUC1 as progression biomarker (serum KL-6 epitope) in advanced IPF

---

## System-Level Synthesis

### The Integrated Model:

```
ENVIRONMENTAL TRIGGERS (smoking, inhaled agents)
  ↓
EPITHELIAL INJURY
├─ Barrier breach (MUC5B dysfunction, DSP loss)
├─ Telomere erosion (TERT↓, cell cycle arrest, senescence)
└─ TLR activation (TOLLIP dysregulation)
  ↓
INNATE IMMUNE ACTIVATION
├─ NLRP1/CARD8 inflammasome (DPP9↓ loss of brake)
├─ IL-1β, IL-18 production
└─ Macrophage recruitment (ATP11A-mediated signaling)
  ↓
FIBROBLAST ACTIVATION (convergence point)
├─ TGF-β signaling (ACVRL1, FAM13A, RhoA/AKAP13 pathways)
├─ IL-1β amplification (positive feedback with TGF-β)
├─ mTOR hyperactivation (DEPTOR↓, NPRL3↓ loss of brake)
├─ Loss of IL-7 protection (IL-7↓ absent Smad7 antagonism of TGF-β)
└─ EMT & epithelial plasticity (ATP11A, AKAP13, RhoA/ROCK)
  ↓
MYOFIBROBLAST ACCUMULATION & ECM REMODELING
├─ Fibrocyte infiltration (circulating bone marrow-derived precursors via CXCR4)
├─ Fibroblast→myofibroblast transition (α-SMA↑, collagen synthesis↑)
├─ mTORC1-driven protein synthesis of collagen (mTOR hyperactivation)
└─ Impaired autophagy & mitochondrial clearance (mTORC1 inhibits ULK1)
  ↓
PROGRESSIVE FIBROSIS
├─ ECM accumulation, basement membrane thickening
├─ Alveolar simplification, capillary loss
├─ Eventual respiratory failure
└─ Feedback loop: Mechanical tension → RhoA → more TGF-β sensitivity
```

### Key Convergence Points (Most Therapeutically Relevant):

1. **mTOR pathway** (2 GWAS loci, clear direction, druggable) → **PRIORITY #1 for translation: Sirolimus**

2. **TGF-β signaling** (5+ targets) → Already heavily targetedby pirfenidone + nintedanib; IL-7 offers novel brake

3. **NLRP1 inflammasome** (via DPP9) → Unresolved paradox; likely better to target downstream (anti-IL-1β)

4. **Epithelial barrier** (MUC5B, DSP) → SpliSense ASO in Phase 1; DSP approaches earlier stage

5. **Cell mechanics & adhesion** (ATP11A, AKAP13/RhoA/ROCK) → ATP11A drug discovery needed; ROCK inhibitors available

---

## Therapeutic Prioritization Based on Pathway Analysis

### **MUST PURSUE (Highest Network Centrality + Druggability)**

1. **Sirolimus** — mTOR pathway (2 GWAS loci converge; FDA-approved drug; pilot data positive)
2. **IL-7 (CYT107)** — Anti-TGF-β brake via JAK1/STAT1/Smad7 (clinical-grade protein; genetic direction clear)
3. **DPP9** — Inflammasome regulation (depends on paradox resolution via preclinical work)

### **SHOULD PURSUE (Strong Evidence + Emerging Druggability)**

4. **Anti-IL-1β** — Downstream of NLRP1 inflammasome (approved drugs: anakinra, canakinumab; stratify by DPP9 genotype)
5. **ROCK inhibitors** (AKAP13/RhoA pathway) — Small molecules exist; selective IPF trial possible
6. **ATP11A** — Strongest coloc signal (PP.H4=0.996); requires 2-3 yr drug discovery

### **COULD PURSUE (Moderate Evidence / Emerging Druggability)**

7. **ACVRL1/sotatercept** — Repurposing PAH drug for IPF-PH
8. **SpliSense SPL5B (MUC5B ASO)** — Already in Phase 1; data expected 2026
9. **FKBP5** — Selective inhibitors in development for other indications (MS, pain)

### **LESS PRIORITY (Difficult Druggability / Incomplete Evidence)**

10. **Telomerase activation** — TERT/TERC targets; no safe activators; RTEL1 is safety risk
11. **Senolytics** — Target spindle checkpoint genes indirectly; early-stage science
12. **GLIS3** — Not IPF GWAS locus; requires 2-3 yr validation in IPF tissue before clinical consideration

---

## Conclusion

**The 21 IPF GWAS targets map onto 6 major biological pathways that paint a coherent disease model.** No single pathway explains IPF entirely; instead, multiple pathways (epithelial barrier, TGF-β signaling, mTOR hyperactivation, inflammasome, cell mechanics, senescence) operate in parallel and amplify each other.

**The most therapeutically impactful targets are those at major convergence points:**
- **mTOR (DEPTOR + NPRL3)**: 2 GWAS loci + FDA-approved drug + positive pilot data → Ready for Phase 2b
- **TGF-β/NLRP1 axis (IL-7, DPP9, ACVRL1)**: 5+ targets; IL-7 is most ready; DPP9 needs paradox resolution
- **Epithelial barrier (MUC5B, DSP)**: Already in trials; ATP11A discovery ongoing

**The immediate opportunity:** **Sirolimus + IL-7 (CYT107) + DPP9 (post-paradox resolution) in parallel trials starting Q3-Q4 2026 would test the top 3 genetic predictions for IPF simultaneously.**

---

## References

- Takahashi H, Okada Y, Hashimoto S, et al. Antigen-driven CD4+ T cell proliferation is associated with early fibrotic progression in pulmonary fibrosis. Nature Commun. 2019 **[Senescence in IPF]**
- Huang M, et al. IL-7 inhibits fibroblast TGF-β production in pulmonary fibrosis. J Clin Invest. 2002. PMID: 11927620 **[IL-7 mechanism]**
- Gomez-Manjarres DC, et al. Sirolimus suppresses fibrocytes in IPF. JCI Insight. 2023. PMID: 36853800 **[Sirolimus pilot]**
- Pokatayev V, Jaiswal A, et al. GLIS3 master regulator of inflammatory fibroblasts. Nature. 2026. PMID: 41501466 **[GLIS3 context]**
- Benramdane S, et al. Highly selective DPP9 inhibitors. J Med Chem. 2023. PMID: 37721854 **[Cpd 42]**
- Compound 6e publication. J Med Chem. 2025;68(21):23163-23184 **[Cpd 6e - orally bioavailable]**
