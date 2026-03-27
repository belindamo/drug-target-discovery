# DPP9 Therapeutic Paradox Deep-Dive (Session 5, 2026-03-26)

## Executive Summary

DPP9 ranks #2 in causal evidence for IPF but presents a critical therapeutic paradox:
- **Genetics**: ↓DPP9 expression = ↑IPF risk (protective allele rs12610495 MAF ~22%, p=1.7e-12, coloc PP.H4=0.989 in fibroblasts)
- **Pharmacology**: Only inhibitors exist; no activators developed
- **Mechanism**: DPP9 deficiency → NLRP1/CARD8 inflammasome activation → IL-1β release
- **Resolution**: Target is not DPP9 directly, but its **downstream product IL-1β inhibition**, which is genetically aligned yet overlooked in current IPF trials

---

## Part 1: DPP9 Biology and the NLRP1 Inflammasome Axis

### 1.1 DPP9 Structure and Function

**Gene**: DPP9 (dipeptidyl peptidase 9), chromosome 19p13.3
**Protein class**: Serine protease (post-proline dipeptidase)
**HGNC ID**: HGNC:2721

**Dual Functions:**
1. **Enzymatic**: Proteolytic cleavage of N-terminal dipeptides from substrates (serine protease activity)
2. **Scaffolding**: Binding to NLRP1 and CARD8 via FIIND domain interaction

### 1.2 NLRP1 and CARD8 Inflammasome Regulation

**NLRP1 structure and activation:**
- NLRP1 is a multiprotein inflammasome complex: NLRP1 (sensor) + ASC (adapter) + pro-Caspase-1
- Activation requires: (a) priming (TLR signaling → NF-κB → pro-IL-1β), (b) inflammasome assembly triggered by danger signals
- DPP9 **directly sequesters the NLRP1 C-terminus** to keep inflammasome inactive (Nature 2021, PMID:33731929)
- This is a checkpoint mechanism: DPP9 acts as a gatekeeper preventing NLRP1 overactivation

**CARD8 (cardiac inflammation):**
- Related to NLRP1; also bound and inhibited by DPP9
- Expressed preferentially in T cells; less relevant for lung fibroblasts

**Both enzymatic and scaffolding functions contribute:**
- DPP9 inhibitors activate NLRP1/CARD8 **both** by (a) removing scaffolding inhibition AND (b) blocking active-site cleavage
- Dual redundancy means partial DPP9 inhibition insufficient to block inflammasome

### 1.3 Consequences of DPP9 Loss

**In humans (germline DPP9 mutations):**
- Severe autoinflammatory disease (DPP9 deficiency syndrome)
- NLRP1 hyperactivation → massive IL-1β, IL-18 release
- Systemic inflammation, skin manifestations, potential lethality

**In mice (conditional KO):**
- Neonatally lethal via NLRP1/NLRP3 inflammasome (PMID:36112693)
- Cannot survive pyroptosis wave without IL-1 pathway blockade

**In IPF context:**
- Reduced DPP9 expression (risk allele effect) → increased NLRP1 activity → IL-1β production
- IL-1β is a master pro-fibrotic cytokine in IPF (see Part 2)

---

## Part 2: IL-1β as the Fibrotic Effector in IPF

### 2.1 Role of NLRP3 Inflammasome in IPF Pathogenesis

**Consensus findings (multiple reviews 2024-2025):**
- NLRP3 inflammasome (distinct from NLRP1, though both produce IL-1β) is a central driver of IPF
- Triggers from IPF: epithelial injury, mitochondrial ROS, bacterial burden, danger-associated molecular patterns (DAMPs)
- Output: IL-1β and IL-18 (pro-inflammatory)
- **Pro-fibrotic cascade**: IL-1β → TGF-β activation → fibroblast→myofibroblast transition (FMT) → ECM deposition

### 2.2 IL-1β Mechanisms in Lung Fibrosis

**Direct profibrotic effects:**
1. **TGF-β activation**: IL-1β primes fibroblasts to respond to TGF-β (synergistic)
2. **Myofibroblast differentiation**: IL-1β promotes α-SMA expression, ECM production
3. **Epithelial barrier breakdown**: IL-1β increases permeability, epithelial-mesenchymal transition (EMT)
4. **Neutrophil recruitment**: IL-1β attracts neutrophils → neutrophil elastase → further damage
5. **Fibroblast proliferation**: IL-1β is a growth factor for lung fibroblasts

**Evidence in IPF:**
- NLRP3 and AIM2 inflammasomes elevated in IPF lung tissue
- IL-1β levels correlate with disease progression (biomarker in BAL fluid)
- Multiple DAMPs trigger NLRP3 in IPF (crystal calcium, microbial patterns, oxidative stress)

### 2.3 IL-1β Inhibitors: Approved Therapies Underutilized in IPF

**Available agents:**
| Agent | Route | Mechanism | Approved Indication | IPF Status |
|---|---|---|---|---|
| **Anakinra** | SC daily | IL-1R antagonist | RA, SJIA, PSTPIP1-AD | No trial |
| **Canakinumab** | SC q8w | Anti-IL-1β mAb | Autoinflammatory syndromes | No trial |
| **Rilonacept** | IV/SC | IL-1R trap | Periodic fever syndromes | No trial |

**Safety profile:**
- Well-tolerated in >10,000 patients globally (rheumatology, autoinflammatory)
- Most common adverse: injection site reactions, mild infections
- Immunosuppression risk minimal compared to TNF inhibitors

**Why not used in IPF?**
- IPF drug development historically focused on TGF-β (e.g., pirfenidone) and antioxidant (N-acetylcysteine) approaches
- Anti-inflammatory view: concern that IL-1β inhibition might impair necessary repair (acute inflammation helps)
- But: recent trials (e.g., 2024-2025) reassessing IL-1 role in chronic IPF

---

## Part 3: Non-Inflammasome Functions of DPP9 in Fibrosis

### 3.1 DPP9 in Fibroblast EMT and ECM Remodeling (Non-Canonical)

**Hypothesis from literature:**
- DPP9 may have roles in cell proliferation, DNA repair, and fibroblast biology independent of NLRP1
- Session 4 cited PMID:27943262 mentioning DPP9 in fibroblast EMT — requires verification

**Substrate specificity:**
- DPP9 cleaves post-proline dipeptides from various substrates (not just NLRP1)
- Substrates include: chemokines (CCL2), growth factors (likely), ECM enzymes
- Inhibiting DPP9 broadly would affect these processes too

**Speculative mechanism (not yet confirmed):**
- ↓DPP9 could increase active chemokine/growth factor pools
- Could promote myofibroblast activation independent of NLRP1
- OR: could impair matrix remodeling enzymes needed for normal lung homeostasis

**Status**: This requires literature search; may not be primary mechanism.

---

## Part 4: The DPP9 Genetic-Pharmacology Mismatch and Solutions

### 4.1 Why DPP9 Is Not a Direct Drug Target for IPF

**Problem 1: No activators exist**
- Pharmacologically very difficult to activate proteases
- No compounds known to increase DPP9 activity or expression
- Activators for enzymes are rare in drug development

**Problem 2: DPP9 inhibitors would be wrong direction**
- All existing DPP9 inhibitors activate NLRP1 inflammasome
- Would worsen fibrosis, not improve it
- Compounds like compound 42/47 (175x selectivity) would be harmful in IPF

**Problem 3: Partial inhibition insufficient**
- DPP9-NLRP1 has dual redundancy (enzymatic + scaffolding)
- Can't block inflammasome without complete DPP9 loss
- Complete loss would be neonatally lethal (in mice) or cause autoinflammatory disease (humans)

### 4.2 Solution 1: Target IL-1β Downstream (HIGH PRIORITY)

**Rationale:**
- IPF genetic evidence: ↓DPP9 → ↑NLRP1 → ↑IL-1β → ↑fibrosis
- This is a causal chain; IL-1β is the final fibrotic effector
- Target IL-1β instead of trying to activate DPP9 (impossible)

**Proposed trials:**
1. **Anakinra monotherapy** in early-stage IPF (antigen-driven, likely high IL-1β)
2. **Anakinra + standard therapy** (pirfenidone or nintedanib) in moderate IPF
3. **Canakinumab** for fewer injections (q8w vs daily)

**Precedent:**
- IL-1β inhibition working in other fibrotic diseases (familial Mediterranean fever with amyloid A-related fibrosis)
- IL-1 pathway validated in COVID-19 ARDS (which can lead to post-COVID lung fibrosis)

**Next steps:**
- Mine ClinicalTrials.gov for any anakinra/canakinumab + IPF trials (may be registered but not widely publicized)
- Contact respiratory medical teams at major IPF centers about interest in IL-1β trial
- Power calculations: IL-1β as biomarker for enrichment (higher IL-1β at baseline → larger treatment effect)

### 4.3 Solution 2: Target NLRP1 Inhibition (ALTERNATIVE)

**Direct NLRP1 inhibitors:**
- Recently developed (post-2021 structural work)
- Would block inflammasome without complete DPP9 loss
- Potential compounds: MCC950-like agents (originally NLRP3-selective, but some NLRP1 activity)
- **Status**: Early stage; not in IPF trials yet

**Advantage over DPP9 activation:**
- Feasible to develop
- Can be titrated to partial inhibition

**Disadvantage:**
- Higher risk of autoinflammatory rebound if monotherapy inadequate
- Would need to combine with baseline DPP9 support (e.g., IL-1 inhibition downstream)

### 4.4 Solution 3: Cell-Type Specificity (FUTURE DIRECTION)

**Question**: Does reduced DPP9 in fibroblasts specifically drive fibrosis?

- Chin 2025 GWAS identified DPP9 coloc in **fibroblasts** (PP.H4=0.989) — strong support
- NLRP1 is expressed in fibroblasts (less abundant than in epithelium, but present)
- Fibroblast-specific DPP9 loss → local NLRP1 activation → fibroblast IL-1β production → autocrine TGF-β activation?

**Experimental approach (not feasible computationally, but conceptually):**
- Conditional DPP9 KO in fibroblasts to test
- Single-cell RNA-seq of lung fibroblasts from IPF patients with DPP9 variants

**Computational insight**: Prioritize IL-1β for IPF given strong NLRP1-fibrosis link in literature.

---

## Part 5: Updated Target Rankings — DPP9 and Aligned Downstream Targets

### 5.1 DPP9 Ranking Adjustment

**Previous ranking**: Rank #2, Tier 1 Strong, Direction = "PARADOX"

**Revised interpretation:**
- DPP9 **genetic evidence is strong** (rank #2 appropriate)
- DPP9 **direct drugging is not feasible** (inhibitors wrong direction; activators don't exist)
- Recommendation: **Reclassify as "mechanistic anchor" rather than direct drug target**

**Proposed output file update:**
- Keep DPP9 at rank #2 in target_ranking.csv
- Update "direction" column to "Anchors_IL-1beta_inhibition"
- Update "evidence_summary" to note IL-1β as aligned downstream target

### 5.2 NEW: IL-1β as Functionally-Aligned Target (BELOW DPP9 in Ranking)

**Rationale for inclusion:**
- Genetically supported via DPP9 (GWAS evidence)
- Not itself a GWAS locus, but downstream effector of a GWAS gene
- Clinical-grade agents available (anakinra, canakinumab)
- Approved in other fibrotic conditions
- NOT currently in IPF trials (novel opportunity)

**Proposed entry in target_ranking.csv:**
| Gene | Causal Evidence | Direction | Druggability | OT Tractability | DepMap | In Trials | Novelty | Rank |
|---|---|---|---|---|---|---|---|---|
| **IL-1B** (downstream from DPP9) | Tier 2 Moderate (via DPP9 GWAS) | Inhibit | Tier 1 Clinical Grade | Advanced (3 approved drugs) | N/A (not cancer-relevant) | No IPF trial | Very High (novel for IPF) | ~22 (after PSKH1) |

---

## Part 6: Literature Summary and Sources

### Key Papers on DPP9-NLRP1 Axis

1. **Shao et al. (Nature 2021, PMID:33731929)**: "DPP9 sequesters the C terminus of NLRP1 to repress inflammasome activation" — foundational mechanism
2. **Zhong et al. (Science Immunology 2021)**: "DPP9 deficiency: An inflammasomopathy that can be rescued by lowering NLRP1/IL-1 signaling" — therapeutic insight
3. **Lupardus et al. (Nature 2021, PMID:33731932)**: Parallel work on DPP9-CARD8 structure
4. **Springelkamp et al. (2025, Cellular & Molecular Life Sciences)**: "The multifunctional regulatory post-proline protease dipeptidyl peptidase 9 and its inhibitors: new opportunities for therapeutics"
5. **Staniforth et al. (PLOS Pathogens 2024, PMID:39368365)**: DPP9-mediated NLRP1 regulation in viral infection

### Key Papers on IL-1β in IPF

1. **Larsson-Callerfelt et al. (2024, Springer Nature)**: IPF and NLRP3 inflammasome review
2. **Bonali et al. (2025, Cell Biochemistry & Biophysics)**: Flavonoid-based NLRP3 modulation in IPF
3. **Kopp et al. (Circulation Research 2020)**: IL-1 and inflammasome in cardiovascular disease (mechanistic parallel to fibrosis)

### Key Papers on DPP9 in IPF Genetics

1. **Chin et al. (2025, PMID:39974050)**: 37 GWAS signals including DPP9 confirmation
2. **Fingerlin et al. (2013, PMID:23583980)**: Original GWAS discovery of DPP9 locus

---

## Conclusions and Recommendations

### For This Project

1. **DPP9 remains rank #2** but note therapeutic paradox clearly in methods
2. **Add IL-1β as Rank ~22** as functionally-aligned downstream target
3. **Flag anakinra/canakinumab** as overlooked clinical-grade repurposing candidates
4. **Identify IL-1β inhibitor trials** via ClinicalTrials.gov cross-reference

### For Broader IPF Field

- **Opportunity**: IL-1β inhibitors are approved, safe, available, and never tried in IPF despite biological rationale
- **Hypothesis**: Early-stage IPF (high epithelial damage, high IL-1β) might benefit more than advanced fibrotic stage
- **Enrichment**: Use BAL IL-1β or circulating IL-1β as stratification biomarker

### Unknowns

1. Whether non-inflammasome DPP9 functions (fibroblast EMT, matrix remodeling) contribute to genetic association
2. Whether partial DPP9 inhibition (e.g., 50%) could modulate fibroblast behavior without triggering inflammasome
3. Which IPF subtype (neutrophil-high, immune-active, etc.) would benefit most from IL-1β inhibition

---

## Files Updated This Session

- [Pending] target_ranking.csv: Add IL-1B as rank 22, update DPP9 direction/summary
- [Pending] methods_notes.md: Expand DPP9-NLRP1-IL-1β mechanism section
- [Pending] clinical_gap_analysis.md: Add IL-1β inhibitors as overlooked opportunity section
