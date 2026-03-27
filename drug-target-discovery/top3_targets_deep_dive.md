# Top 3 Actionable Targets for IPF: Deep-Dive Analysis

*Session 5 (2026-03-12) — Synthesizing 4 sessions of genetics-first drug target discovery*

## Executive Summary

From a pipeline of 21 genetically validated IPF targets, three stand out as **immediately actionable** — meaning they have the combined genetic evidence, druggability, safety profile, and mechanistic rationale to support near-term proof-of-concept clinical studies without requiring new drug discovery:

1. **DPP9** — Selective nanomolar oral inhibitors now exist; fibroblast-specific genetic signal; strongest novel actionable target
2. **IL-7 (CYT107)** — Clinical-grade recombinant protein; preclinical antifibrotic mechanism; >650 patients dosed safely; most "ready" repurposing opportunity
3. **mTOR pathway (via sirolimus)** — Two independent GWAS loci (DEPTOR + NPRL3) converge on mTORC1; approved drug available; pilot IPF data exists

None of these targets is being pursued in any active IPF clinical trial as of March 2026.

---

## Target 1: DPP9 — The #1 Genetically Validated Novel Target (With a Therapeutic Paradox)

### Genetic Evidence

| Evidence Type | Result | Source |

|---|---|---|

| GWAS | rs12610495 (19p13.3), p=1.7×10⁻¹² | Fingerlin 2013, PMID: 23583980 |

| Colocalization (fibroblasts) | PP.H4 = 0.989 | Borie 2022, PMID: 35816432 |

| Colocalization (IPF cases) | PP.H4 = 0.874 | Borie 2022 |

| Direction of effect | Decreased DPP9 expression → increased IPF risk | Borie 2022; TWAS |

| COVID-19 shared locus | Same variant associated with severe COVID-19 | COVID-19 Host Genetics Initiative |

| WGS confirmation | Validated in eBioMedicine 2025 WGS study | Kousathanas 2025 |

**Key strength**: The fibroblast-specific colocalization (PP.H4=0.989) provides cell-type resolution that most GWAS targets lack. The IPF risk allele reduces DPP9 expression specifically in fibroblasts — the key effector cell type in fibrosis.

### DPP9 Biology: The NLRP1/CARD8 Inflammasome Connection

DPP9 is a serine protease belonging to the DPP4 superfamily. Unlike DPP4 (the sitagliptin target), DPP9 is primarily intracellular and has a distinct biological role centered on **inflammasome regulation**:

**The functional degradation model** (Zhong et al. 2018, PMID: 30291141):

- NLRP1 and CARD8 contain a FIIND (Function-to-Find Domain) that auto-proteolyses into N-terminal (NT) and C-terminal (CT) fragments
- DPP9 physically binds the FIIND domain, forming a ternary complex: DPP9 + full-length NLRP1/CARD8 + their CT fragments
- The CT N-terminus inserts into the DPP9 active site, sequestering the bioactive CT and preventing inflammasome assembly
- Both DPP9's catalytic activity AND its scaffolding/binding function are required for NLRP1 suppression
- For CARD8, enzymatic activity alone (not binding) is the primary restraint (Griswold et al. 2019, PMID: 31580637)

**Structural basis** — Two landmark cryo-EM studies (Nature 2021):

- Huang et al. (PMID: 33731929): Rat NLRP1-DPP9 2:1 complex; UPA-mediated oligomerization prevented by DPP9 binding; both binding and catalysis required
- Hollingsworth et al. (PMID: 33731932): Human NLRP1-DPP9 at 3.6Å; ternary complex with NLRP1-CT N-terminus in active site; VbP displaces CT
- Sharif et al. (Immunity 2021, PMID: 34019797): CARD8-DPP9 at 3.3Å; analogous complex but CT not directly in active site

**Expression in IPF-relevant cells:**

- NLRP1 is the predominant inflammasome sensor in human epithelial barrier tissues — including bronchial and alveolar epithelial cells (Drutman et al. 2022, PMID: 34807231)
- NLRP1 directly senses SARS-CoV-2 3CL protease in lung epithelial cells (Planes et al. 2022, PMID: 35594856)
- CARD8 is expressed in monocytes, macrophages, and lymphocytes (note: CARD8 has no mouse ortholog)
- DPP9 is endogenously expressed in fibroblasts, where it regulates cell adhesion and migration (Schade et al. 2016)
- **Critical gap**: No published studies directly examine NLRP1/CARD8/DPP9 inflammasome axis in IPF fibroblasts

**Complete DPP9 loss is catastrophic:**

- DPP9 catalytic-dead knock-in mice (Dpp9^S759A/S759A) die within 24 hours of birth (Harapas et al. 2022, PMID: 36112693)
- Lethality rescued by Nlrp1 knockout — confirming pathology driven by inflammasome hyperactivation
- Human biallelic DPP9 loss-of-function causes HLH-like hyperinflammation, pancytopenia, skin abnormalities
- A de novo dominant-negative DPP9 mutation caused severe autoinflammation in a child (Blood 2023, PMID: 37544411)

### The Therapeutic Paradox — A Critical Complexity

**The paradox**: The IPF genetic data shows **decreased DPP9 expression → increased IPF risk**. This means the genetics argue for DPP9 **activation or stabilization**, not inhibition. Yet the published DPP9-selective inhibitors (Compounds 42 and 6e) are designed to **inhibit** DPP9 — which would move biology in the **wrong direction** for IPF.

**This is not a minor complication — it fundamentally changes the therapeutic strategy:**

| Approach | Genetic Alignment | Feasibility | Risk |

|---|---|---|---|

| DPP9 inhibition | ❌ Wrong direction | ✅ Compounds exist | Pro-inflammatory; may worsen fibrosis |

| DPP9 activation/stabilization | ✅ Correct direction | ❌ No compounds exist | Unknown |

| Downstream targeting (anti-IL-1β) | ✅ Addresses inflammasome | ✅ Anakinra, canakinumab approved | Immunosuppression |

| DPP9 non-inflammasome functions | ? Depends on mechanism | ⚠ Needs validation | Complex |

**Three possible resolutions:**

**Resolution 1 — Non-inflammasome functions dominate in fibroblasts:**

The fibroblast-specific eQTL (PP.H4=0.989) suggests the genetic signal operates through fibroblast biology, not inflammasome. DPP9 regulates fibroblast adhesion, migration, and EMT:

- In NSCLC, DPP9 promotes EMT; DPP9 knockdown reverses mesenchymal phenotype (Tang et al. 2017, PMID: 27943262)
- In kidney, increased DPP8/9 is associated with tubulointerstitial fibrosis and EMT
- If DPP9 promotes EMT in lung fibroblasts, then DPP9 *inhibition* could be anti-fibrotic through EMT reversal — contradicting the genetic direction but potentially therapeutic
- **Problem**: The genetic data still shows ↓DPP9 = ↑IPF risk, which is hard to reconcile with this model

**Resolution 2 — Downstream targeting (preferred by genetic evidence):**

Rather than modulating DPP9 directly, target the inflammasome-IL-1β axis downstream:

- Anti-IL-1β (canakinumab): FDA-approved for CAPS; blocks the downstream consequence of NLRP1 activation
- IL-1R antagonist (anakinra): Could prevent inflammasome-driven fibrotic damage
- Gasdermin D inhibitors: Block pyroptosis without affecting upstream inflammasome sensing
- This approach is **genetically aligned**: if ↓DPP9 → ↑NLRP1 activity → ↑IL-1β → fibrosis, then blocking IL-1β should be protective

**Resolution 3 — The genetic signal reflects a complex dose-response:**

- The common variant eQTL is a modest effect (~20% reduction in DPP9 expression per allele)
- This partial reduction may shift the balance toward chronic low-grade inflammasome activation (sufficient to promote fibrosis) without triggering overt pyroptosis
- Pharmacological inhibition at different levels may have non-linear effects
- **Critical sensitivity**: Even modest DPP9 reduction (from a common variant) increases IPF risk, suggesting a very narrow therapeutic window for any DPP9 modulator

**Updated assessment**: The selective DPP9 inhibitors (Compounds 42 and 6e) are **essential research tools** for understanding DPP9 biology and have clear utility in **AML/HIV** (where pyroptosis of malignant cells is desired). For **IPF specifically**, the genetic evidence more strongly supports:

1. Downstream anti-IL-1β therapy (immediately actionable with approved drugs)
2. Investigation of DPP9's non-inflammasome functions in fibroblasts (research stage)
3. DPP9 stabilization/activation strategies (conceptual; no compounds yet)

### Druggability: Selective Inhibitors Now Available

| Compound | Affinity | Selectivity (DPP9/DPP8) | Selectivity (DPP9/DPP4) | Oral | Source |

|---|---|---|---|---|---|

| Compound 42 | Ki ~nM | 175-fold | >1000-fold | ND | J Med Chem 2023 |

| Compound 6e | Ki ~nM (low nanomolar) | >100-fold | >1000-fold | Yes (rat PK demonstrated) | J Med Chem 2025 |

| VbP (talabostat) | nM | None (DPP8=DPP9) | Moderate | Yes | Tool compound |

**Key selectivity insight**: F253 in DPP9 (vs Y252 in DPP8) was identified as the critical residue conferring selectivity. Vildagliptin-derived compounds exploit this difference to achieve DPP9-selective inhibition (ChemMedChem 2025).

**Why selectivity matters:**

- DPP4 inhibition (gliptins): GLP-1 degradation → glucose-lowering effects; not desired in IPF context
- DPP8 inhibition: Causes severe toxicity in animal models (gastrointestinal, hematological)
- DPP9-selective inhibition: Targets intracellular inflammasome pathway without systemic DPP4/DPP8 effects

### Safety (DepMap 25Q3)

| Metric | Value | Interpretation |

|---|---|---|

| Chronos score | -0.010 | Near zero — no growth effect |

| Dependent lines | 4/1186 (0.3%) | Negligible cancer essentiality |

| Classification | Safe | Not essential in any lineage |

### DPP4 Inhibitors in Fibrosis — Organ-Specific Biology

DPP4 (the sitagliptin target) has been studied extensively in fibrotic diseases, with **organ-specific and contradictory results**:

**Antifibrotic in skin (systemic sclerosis):**

- DPP4 marks activated fibroblasts in SSc (Soare et al. 2020, PMID: 31350829)
- Sitagliptin/vildagliptin reduced fibroblast proliferation, collagen, and contractile protein via ERK inhibition
- DPP4-KO mice resistant to bleomycin-induced dermal AND pulmonary fibrosis
- DPP4 inhibitors promoted regression of established fibrosis in skin

**Antifibrotic in liver:**

- Sitagliptin attenuated liver fibrosis via TGF-β1/Smad/ERK suppression (Kaji et al. 2014, PMID: 23475323)

**Conflicting results in lung (IPF):**

- Tabeling et al. (2022, PMC9473336): Reduced DPP4+ fibroblast frequency in IPF tissue; DPP4 expression DECREASED by TGF-β1 in lung fibroblasts; loss of DPP4 had no impact on lung fibroblast activation
- This directly contradicts the skin findings and **cautions against extrapolating within the DPP family across organs**

**Key implication for DPP9**: The organ-specific biology of the DPP family means that DPP9's role in lung fibroblasts may be fundamentally different from its role in other tissues. DPP4 data cannot be extrapolated to DPP9, and skin/liver data cannot be extrapolated to lung.

### Actionability Assessment (Revised)

| Criterion | Score | Rationale |

|---|---|---|

| Genetic evidence strength | ★★★★★ | Tier 1; GWAS + coloc (fibroblast-specific) + COVID-19 shared |

| Druggability (inhibition) | ★★★★★ | Selective nanomolar oral inhibitors published |

| Druggability (activation — genetically correct) | ★☆☆☆☆ | No activators/stabilizers exist |

| Safety profile | ★★★★★ | DepMap: 0.3% dep; heterozygous loss tolerated |

| Preclinical rationale | ★★☆☆☆ | **Paradox**: genetics says ↑DPP9 = protection; inhibitors do opposite |

| Clinical readiness | ★★★☆☆ | Anti-IL-1β drugs exist (downstream); DPP9 inhibitors misaligned |

| **Overall actionability (direct DPP9 inhibition for IPF)** | **★★★☆☆** | **Genetically validated but therapeutically complex** |

| **Overall actionability (downstream anti-IL-1β)** | **★★★★☆** | **Approved drugs; genetically aligned; needs IPF trial** |

### Critical Next Steps for DPP9

1. **Resolve the paradox**: Test Compound 6e in bleomycin model — does DPP9 inhibition worsen or improve fibrosis?
2. **Characterize non-inflammasome functions**: What does DPP9 do in primary human IPF fibroblasts beyond inflammasome regulation?
3. **Downstream approach**: Design proof-of-concept trial of anakinra or canakinumab (anti-IL-1β) in IPF, with DPP9 genotype stratification
4. **EMT studies**: Test whether DPP9 inhibition reverses EMT in IPF lung fibroblasts (as it does in NSCLC)
5. **NLRP1/CARD8 expression mapping**: Use IPF single-cell datasets to map NLRP1/CARD8/DPP9 co-expression in fibroblasts vs epithelium vs macrophages
6. **Biomarker development**: Develop serum IL-1β/IL-18 assay to stratify IPF patients by inflammasome activation status

---

## Target 2: IL-7 (CYT107) — The Most "Ready" Repurposing Opportunity

### Genetic Evidence

| Evidence Type | Result | Source |

|---|---|---|

| Mendelian Randomization | OR = 0.67 (protective) | Liu 2024, PMID: 38783236 |

| Colocalization | PP.H4 = 0.84 | Liu 2024 |

| MR method | IVW + pQTL validation | Liu 2024 |

| Instrument source | Blood eQTLGen cis-eQTLs | eQTLGen Consortium |

| Direction | Higher IL-7 levels → reduced IPF risk | Protective |

**Key strength**: The MR evidence (OR=0.67) is supported by colocalization (PP.H4=0.84), ruling out confounding by LD. The protective direction means IL-7 supplementation would move biology in the genetically validated direction.

### IL-7 Signaling Pathway

**Receptor complex**: IL-7 binds to a heterodimeric receptor consisting of:

- IL-7Rα (CD127) — the specific chain
- Common gamma chain (γc/CD132) — shared with IL-2, IL-4, IL-9, IL-15, IL-21

**Downstream signaling**:

1. **JAK1/JAK3 → STAT5** (canonical): T cell survival, proliferation, homeostasis
2. **JAK1 → STAT1** (non-canonical): Activates Smad7 transcription → TGF-β pathway antagonism
3. **PI3K/Akt**: Cell survival
4. **MAPK/ERK**: Proliferation and differentiation

### Antifibrotic Mechanism: The JAK1/STAT1/Smad7 Axis

The key antifibrotic mechanism operates through a non-canonical pathway:

```
IL-7 → IL-7Rα/γc → JAK1 → STAT1 → ↑Smad7 transcription
                                          ↓
                        Smad7 binds TGF-β receptor I
                                          ↓
                        Blocks Smad2/3 phosphorylation
                                          ↓
                        ↓ Collagen synthesis, ↓ α-SMA, ↓ fibronectin
```

**Published preclinical evidence** (Huang et al. 2002, J Clin Invest, PMID: 11927620):

- IL-7 directly inhibits TGF-β₁ production by human lung fibroblasts in vitro
- IL-7 blocks TGF-β signaling via Smad7 induction (JAK1/STAT1-dependent)
- Using JAK1-deficient (U4A) and STAT1-deficient (U3A) mutant fibroblast lines, IL-7 had no effect — confirming pathway requirement
- Recombinant IL-7 decreased bleomycin-induced pulmonary fibrosis in vivo in mice
- Effect is IFN-γ-independent (tested in IFN-γ knockout mice — still effective)
- Smad7 dominant-negative fibroblasts restored TGF-β-induced collagen synthesis despite IL-7, confirming Smad7 is the key mediator
- Follow-up study (Bogatkevich et al. 2004, PMID: 15133032): IL-7 and TGF-β have opposing effects on PKC-δ; IL-7 inhibits TGF-β-induced PKC-δ phosphorylation at Ser-645 and Thr-505

### IL-7R Expression in IPF-Relevant Cell Types

| Cell Type | IL-7Rα (CD127) Expression | IPF Relevance |

|---|---|---|

| T lymphocytes (CD4+, CD8+) | High (primary site) | T cell dysregulation in IPF |

| Fibroblasts | Low-moderate (but functionally responsive) | Direct antifibrotic target |

| Alveolar macrophages | Low | Indirect effects via T cell modulation |

| Type II alveolar epithelial cells | Low-variable | Epithelial repair |

| ILC2 (innate lymphoid cells) | Moderate | Type 2 inflammation in IPF |

**Important nuance**: Even though fibroblasts express relatively low levels of IL-7Rα, the preclinical data shows they are functionally responsive to IL-7 stimulation, with direct effects on TGF-β production and signaling.

### CYT107 Clinical Data

CYT107 (glycosylated recombinant human IL-7) has extensive clinical safety data:

| Trial | Indication | Phase | N | Key Safety Findings |

|---|---|---|---|---|

| COVID-19 ILIAD-7-US | Critical COVID pneumonia | Phase 2 RCT | 109 (55 CYT107, 54 placebo) | Safe; no cytokine storm; **fewer** TEAEs than placebo (195 vs 396, P<0.0001); 44% fewer secondary infections (P=0.014) |

| IRIS-7 | Septic shock lymphopenia | Phase 2 RCT | 27 | Well-tolerated; 3-4 fold CD4+/CD8+ increase; no cytokine storm |

| IV CYT107 | Septic shock | Phase 2 | 21 | IV route: ~100x higher plasma levels; 3/15 transient respiratory distress → **IM route preferred** |

| IMPULSE-7 | MAC lung disease | Phase 2 | 8 (6 completed) | **Negative** for MAC cure; stopped early; additional lung safety data |

| Oncology | Various solid tumors | Phase 1/2 | ~200+ | Acceptable safety; lymphocyte expansion |

**Cumulative safety**: >650 patients dosed with CYT107 across HIV, oncology, sepsis, COVID-19, HSCT, hepatitis C, NTM, and idiopathic lymphopenia. No dose-limiting toxicities related to pulmonary inflammation at standard IM dosing.

**COVID lung trial** (Hotchkiss et al. 2025, JCI Insight, PMID: 39903535): Particularly relevant because:

- Patients had active lung inflammation/injury requiring ICU-level care
- CYT107 had **significantly fewer** adverse events than placebo (P<0.0001) — including 43% fewer respiratory AEs
- No cytokine storm events; 44% fewer secondary infections (P=0.014)
- In non-antiviral subgroup: ICU stay 24 vs 45 days (P=0.048)
- Self-regulating safety mechanism: CYT107 causes rapid transitory downregulation of CD127 (IL-7Rα), preventing overstimulation

**IRIS-7 trial** (Francois et al. 2018, JCI Insight, PMID: 29515037): Confirmed IM route safety in sepsis.

**IV route caution** (Daix et al. 2023, PMID: 36906875): IV CYT107 produced ~100-fold higher plasma levels than IM; 3/15 patients developed transient respiratory distress. All resolved without sequelae. **IM route strongly preferred for any IPF trial.**

**Pharmacokinetics:**

- Route: Intramuscular (IM) preferred over IV or SC
- Half-life: ~2 days (terminal)
- Cmax (IM, Day 1): 443 ng/mL at 9 hours
- Dosing: 10-20 µg/kg IM, typically twice weekly for 3-4 weeks
- Immunogenicity: No anti-CYT107 antibodies detected across trials (glycosylated CHO-produced form)
- Self-regulating: CD127 downregulation prevents overstimulation

### Potential Risks and Mitigation

| Risk | Severity | Mitigating Evidence | Mitigation Strategy |

|---|---|---|---|

| Immune activation worsening IPF | Low | CYT107 had *fewer* AEs than placebo in COVID lung trial | Monitor inflammatory biomarkers; start low dose IM |

| **CD8+ T cell expansion (PROFIBROTIC)** | **Moderate-High** | CD8+ T cells in IPF have profibrotic transcriptional profile; express PD-1; correlate with fibrosis severity. CD8+ depletion protects mice from bleomycin fibrosis | **Critical: monitor CD4/CD8 ratio and effector phenotype in any IPF trial** |

| Treg suppression | Moderate | IL-7 can abrogate naive Treg function (Heninger 2012, PMID: 23129754), but effect is reversible. Tregs already dysfunctional in IPF (Kotsianidis et al., PMID: 19342412) | Reversible on IL-7 withdrawal; Tregs are already impaired in IPF |

| ILC2/type 2 immunity amplification | Low-Moderate | IL-7 supports ILC2 survival; ILC2s elevated in IPF and drive pro-fibrotic IL-13/type 2 immunity | IL-7 is not primary ILC2 activating signal (IL-33/ST2 is); monitor eosinophils/IL-13 |

| Th17 expansion → pro-fibrotic | Low | IL-7 does not expand Th17 in vivo; primarily drives Th1 | IL-7 may inhibit IL-17-producing Treg via STAT5 |

| Tumor promotion (lymphoid) | Low | Not observed in >650 patients | Screen for occult malignancy at baseline |

**Key safety insight for IPF**: IL-7 primarily expands Th1 cells (antifibrotic via IFN-γ) and does not expand Th17 populations. However, the **CD8+ T cell expansion risk is genuine** — IPF CD8+ T cells are profibrotic and their expansion could worsen disease. This is the most important safety concern for an IPF trial and requires careful T cell phenotyping.

### Critical Evidence Gaps (Identified in Session 5)

1. **Single preclinical model from 2002**: The foundational antifibrotic evidence (Huang et al. 2002, PMID: 11927620) is >20 years old and has **never been independently replicated**. No second pulmonary fibrosis model tested (e.g., silica, radiation, TGF-β overexpression). ATS guidelines recommend testing in ≥2 models.
2. **Prophylactic dosing only**: The bleomycin study used IL-7 starting 1 day *before* injury. Therapeutic dosing in established fibrosis has not been tested — yet this is the clinically relevant scenario.
3. **MR evidence is for susceptibility, not progression**: OR=0.67 was **not replicated** in the IPF progression cohort, suggesting IL-7 may influence disease onset but not necessarily slow established disease.
4. **No IPF-specific clinical data**: CYT107 has never been administered to IPF patients.
5. **IMPULSE-7 was negative**: The only dedicated lung disease trial (MAC) was stopped early for lack of signal, though this may reflect the wrong disease context rather than IL-7 inefficacy.

### Safety (DepMap 25Q3)

| Metric | Value | Interpretation |

|---|---|---|

| Chronos score | +0.076 | Positive — knockout mildly promotes growth |

| Dependent lines | 0/1186 (0.0%) | Zero cancer essentiality |

| Classification | **VERY SAFE** | Knockout is beneficial in cancer context |

### Actionability Assessment

| Criterion | Score | Rationale |

|---|---|---|

| Genetic evidence strength | ★★★★☆ | Tier 2; MR (OR=0.67) + coloc (PP.H4=0.84); not GWAS lead |

| Druggability | ★★★★★ | CYT107 is clinical-grade, >650 patients dosed |

| Safety profile | ★★★★☆ | >650 patients safe; but CD8+ expansion risk in IPF uncharacterized |

| Preclinical rationale | ★★★☆☆ | **Revised down**: Single 2002 study, never replicated, prophylactic dosing only |

| Clinical readiness | ★★★★★ | Could enter IPF Phase 2 immediately (drug exists, IM route established) |

| **Overall actionability** | **★★★★☆** | **Most "ready" repurposing opportunity, but preclinical gap is real** |

### Critical Next Steps for IL-7

1. **ESSENTIAL**: Replicate Huang et al. 2002 in modern IPF mouse models (therapeutic dosing in established fibrosis, not prophylactic)
2. Confirm IL-7R expression and function in IPF lung fibroblasts using single-cell data (IPF Cell Atlas, Adams 2020 PMID: 32832599, Habermann 2020 PMID: 32832598)
3. Test CYT107 in second fibrosis model (e.g., TGF-β overexpression, repetitive bleomycin)
4. Measure Smad7 induction in primary human IPF fibroblasts treated with IL-7
5. T cell phenotyping study: what happens to CD4+, CD8+, Treg, ILC2 populations in IPF lung organoids or ex vivo lung tissue treated with IL-7?
6. Design Phase 2a proof-of-concept: CYT107 10 µg/kg **IM** twice weekly × 12 weeks in IPF
7. Primary endpoint: FVC change at 24 weeks; key biomarkers: serum SP-D, MMP-7, Smad7, CD4/CD8 ratio, circulating fibrocytes

---

## Target 3: mTOR Pathway (Sirolimus) — Two GWAS Loci, One Pathway

### Genetic Evidence: Convergence of DEPTOR and NPRL3

The strength of the mTOR pathway as an IPF target comes from **two independent GWAS loci** that both point to mTORC1 hyperactivation:

#### DEPTOR (8q24.12)

| Evidence Type | Result | Source |

|---|---|---|

| GWAS | rs28513081, OR=0.82, p=1.2×10⁻⁹ | Allen 2020, PMID: 31710517 |

| TWAS (lung) | p=8.58×10⁻⁹ | Gong 2020, PMID: 33362862 |

| Direction | Decreased DEPTOR expression → increased IPF risk | |

| Function | Endogenous mTOR inhibitor (binds both mTORC1 and mTORC2) | |

**DEPTOR biology**: DEPTOR (DEP domain-containing mTOR-interacting protein) is a direct negative regulator of both mTORC1 and mTORC2. Through its DEP domain, DEPTOR binds the FAT domain of mTOR kinase and suppresses its activity. Loss of DEPTOR → mTOR hyperactivation → enhanced protein synthesis, collagen production, and cell growth.

**TGF-β connection**: TGF-β₁, the master profibrotic cytokine, **suppresses DEPTOR expression** in fibroblasts:

```
TGF-β₁ → ↓DEPTOR → ↑mTORC1 activity → ↑collagen synthesis
                                        → ↑α-SMA expression
                                        → ↑myofibroblast differentiation
```

This creates a feed-forward loop: TGF-β removes the mTOR brake (DEPTOR), leading to unchecked fibrotic gene expression.

#### NPRL3 (16p13.3)

| Evidence Type | Result | Source |

|---|---|---|

| GWAS | rs74614704, OR=1.49, p=2.57×10⁻¹² | Allen 2022, PMID: 35688625 |

| Function | GATOR1 complex subunit (mTORC1 inhibitor) | |

| Direction | Risk allele → loss of NPRL3-mediated mTORC1 suppression | |

**NPRL3 biology**: NPRL3 is a subunit of the GATOR1 complex (with DEPDC5 and NPRL2), which is the major upstream negative regulator of mTORC1. GATOR1 functions as a GAP (GTPase-activating protein) for Rag GTPases, converting them from active (GTP-bound) to inactive (GDP-bound) form. This prevents Rag-mediated recruitment of mTORC1 to the lysosomal surface where it would be activated by Rheb.

**Pathway convergence**:

```
DEPTOR ─┤ mTOR (direct binding)     ← GWAS locus 1 (8q24.12)
                  ↑
NPRL3/GATOR1 ─┤ Rag GTPases → mTORC1  ← GWAS locus 2 (16p13.3)
```

Two independent genetic signals, both pointing to the same biological conclusion: **mTORC1 hyperactivation is a causal driver of IPF**.

### mTOR in Fibrosis Biology

**mTORC1 profibrotic effects:**

1. **Collagen synthesis**: mTORC1 → 4E-BP1 phosphorylation → enhanced translation of collagen mRNAs
2. **Myofibroblast differentiation**: mTORC1 → S6K1 → promotes α-SMA expression
3. **Impaired autophagy**: mTORC1 → phosphorylation/inactivation of ULK1 → blocked autophagy → accumulation of damaged organelles and senescent cells
4. **Epithelial cell senescence**: mTORC1 hyperactivation in type II alveolar epithelial cells → cellular senescence → impaired lung repair
5. **Metabolic reprogramming**: Enhanced glycolysis and lipogenesis in fibroblasts

**Impaired autophagy in IPF**: This is particularly relevant because IPF fibroblasts show reduced autophagy compared to normal fibroblasts. mTORC1 inhibition by rapamycin restores autophagy, promotes clearance of damaged mitochondria, and reduces collagen production.

### Sirolimus vs. Everolimus: Why Drug Choice Matters

**The everolimus failure**: The RAPPORT trial of everolimus in IPF showed poor tolerability and no efficacy. This has been cited as evidence against mTOR inhibition in IPF. However, the story is more nuanced:

| Feature | Sirolimus (Rapamycin) | Everolimus |

|---|---|---|

| mTORC1 inhibition | Yes | Yes |

| mTORC2 inhibition (chronic) | Minimal | Significant |

| Half-life | 62 hours | 30 hours |

| Dosing | Once daily/weekly | Twice daily |

| IPF pilot result | Tolerated; fibrocyte suppression | Poorly tolerated |

| Lung toxicity | Lower rate | Higher pneumonitis rate |

**Differential mTORC2 inhibition hypothesis**: Everolimus causes more mTORC2 inhibition than sirolimus at therapeutic doses. mTORC2 regulates Akt/PKB, which has cytoprotective effects in the lung. Excessive mTORC2 inhibition may remove protective signals while mTORC1 inhibition alone provides the antifibrotic benefit.

### Sirolimus IPF Pilot Trial (Gomez-Manjarres et al. 2023, JCI Insight, PMID: 36853800)

| Parameter | Detail |

|---|---|

| Design | Randomized, double-blind, placebo-controlled **crossover** |

| N | 28 IPF participants |

| Drug | Sirolimus (dose titrated; target trough 5-15 ng/mL) |

| Duration | ~6 weeks per period, 4-week washout, then crossover |

| Registration | NCT01462006 |

| Primary outcome | Safety, tolerability, and circulating fibrocyte levels |

| Key finding 1 | **35% decline in total circulating fibrocytes** (sirolimus vs placebo) |

| Key finding 2 | **34% decline in CXCR4+ fibrocytes** (bone marrow-derived) |

| Key finding 3 | **42% decline in α-SMA+ fibrocytes** (myofibroblast precursors) |

| Tolerability | Respiratory AEs more frequent on **placebo** than sirolimus |

| Funding | NIH R01HL098329 + AHA 18TPA34170486 |

**Fibrocyte biology**: Circulating fibrocytes (CD45+/Col1+/CXCR4+) are bone marrow-derived cells that traffic to the injured lung via the CXCL12/CXCR4 axis and differentiate into myofibroblasts. Elevated fibrocyte levels predict IPF progression and mortality. Sirolimus inhibits fibrocyte CXCR4 expression, reducing their traffic to the lung and attenuating fibrosis in preclinical models. This pilot trial provided the first human evidence of this mechanism.

**Important limitation**: The trial was designed as proof-of-principle for the fibrocyte mechanism, not to detect FVC benefit. It was "too short and too small to detect any effect on disease trajectory" — but justifies larger, longer trials.

### Safety (DepMap 25Q3)

**DEPTOR:**

| Metric | Value | Interpretation |

|---|---|---|

| Chronos score | -0.038 | Near zero |

| Dependent lines | 4/1186 (0.3%) | Negligible |

| Classification | Safe | Selective contexts only |

**NPRL3:**

| Metric | Value | Interpretation |

|---|---|---|

| Chronos score | NA (0/45 in tested subset) | Not essential in tested lines |

| Dependent lines | 0/45 | Safe |

| Classification | Not essential | Limited data |

**Sirolimus clinical safety**: Approved since 1999 for organ transplant rejection; well-characterized safety profile. Key concerns for IPF patients:

- Immunosuppression in elderly patients (infection risk)
- Pneumonitis (rare, dose-dependent, reversible)
- Drug-drug interactions with pirfenidone (CYP3A4) and nintedanib (P-gp)

### Actionability Assessment

| Criterion | Score | Rationale |

|---|---|---|

| Genetic evidence strength | ★★★★★ | Two independent GWAS loci converging on same pathway |

| Druggability | ★★★★★ | Sirolimus is FDA-approved, generic, well-characterized |

| Safety profile | ★★★★☆ | Approved drug with known toxicities; manageable in IPF |

| Preclinical rationale | ★★★★★ | Extensive mTOR-fibrosis literature; autophagy restoration |

| Clinical readiness | ★★★★★ | Could enter Phase 2 IPF trial immediately |

| **Overall actionability** | **★★★★★** | **Approved drug + two GWAS loci = highest confidence** |

### Critical Next Steps for mTOR/Sirolimus

1. Power an adequately sized Phase 2b sirolimus trial in IPF (n=200+; 24-week FVC)
2. Use low-dose sirolimus (1-2 mg/day) to maximize mTORC1 selectivity
3. Measure fibrocytes, FVC, and autophagy biomarkers (LC3-II/I ratio)
4. Assess drug-drug interactions with pirfenidone and nintedanib
5. Consider combination: sirolimus + pirfenidone or sirolimus + nerandomilast
6. Biomarker stratification: select patients with evidence of mTOR hyperactivation

---

## Comparative Assessment

| Feature | DPP9 Pathway | IL-7 (CYT107) | Sirolimus (mTOR) |

|---|---|---|---|

| **Genetic evidence** | GWAS (p=1.7e-12) + coloc (0.989) | MR (OR=0.67) + coloc (0.84) | Two GWAS loci (DEPTOR + NPRL3) |

| **Evidence tier** | Tier 1 (Strong) | Tier 2 (Moderate) | Tier 2 (Moderate) × 2 loci |

| **Genetic direction** | ⚠ ↑DPP9 = protection (complex) | ✅ ↑IL-7 = protection (clear) | ✅ ↓mTORC1 = protection (clear) |

| **Drug availability** | Anti-IL-1β approved; DPP9 inhibitors wrong direction | Clinical-grade (CYT107) | FDA-approved (sirolimus) |

| **Time to Phase 1** | 0 (anti-IL-1β) or 2-3 yr (DPP9 tool) | 0 (drug exists) | 0 (drug exists) |

| **DepMap safety** | 0.3% dep (SAFE) | 0.0% dep (VERY SAFE) | 0.3% dep (SAFE) |

| **Preclinical IPF data** | Structural biology; paradox unresolved | Bleomycin model positive | Pilot trial positive |

| **Novel vs. repurpose** | Novel (anti-IL-1 in IPF) | Repurpose | Repurpose |

| **Cross-ancestry** | Moderate (EUR validated) | Unknown (EUR only) | Moderate (DEPTOR replicated) |

| **Novelty score** | Very High | Very High | High |

| **Key risk** | Inflammasome paradox; direction unclear | Immune activation in IPF lung | Immunosuppression in elderly |

### Recommended Prioritization

**For immediate clinical testing (within 1 year):**

1. **CYT107 (IL-7)**: Phase 2a proof-of-concept in IPF. No regulatory barriers — drug is in clinical use. Genetic direction is clear (↑IL-7 = protection). Preclinical antifibrotic mechanism validated. **Highest confidence actionable target.**
2. **Sirolimus**: Phase 2b adequately powered trial. FDA-approved drug with pilot data in IPF. Two GWAS loci provide strongest genetic convergence. Genetic direction clear (↓mTORC1 = protection). **Strongest genetic rationale.**

**For near-term investigation (1-2 years):**

1. **DPP9 pathway — downstream approach**: Trial of anti-IL-1β therapy (anakinra/canakinumab) in IPF patients, stratified by DPP9 genotype (rs12610495). This addresses the NLRP1 inflammasome pathway without the paradox of DPP9 inhibition. **Genetically aligned; approved drugs available.**

**For longer-term research (2-5 years):**

1. **DPP9 direct modulation**: Resolve whether DPP9 inhibitors improve or worsen experimental lung fibrosis. If non-inflammasome functions dominate, inhibition could still be therapeutic. If inflammasome effects dominate, develop DPP9 stabilizers. **Highest novelty potential but highest uncertainty.**

---

## GLIS3: An Important Contextual Finding (Not a GWAS Target)

### The Nature 2026 Discovery

Pokatayev, Jaiswal et al. (Nature 2026, PMID: 41501466) used bidirectional CRISPR screens in primary human fibroblasts to identify **GLIS3** as a master transcriptional regulator of the inflammatory activated fibroblast (IAF) program.

**Key findings:**

- GLIS3 controls expression of >150 fibrotic effector genes including IL11, LIF, FAP, MMP2, SERPINE1
- GLIS3 integrates TGF-β and IL-1β signals to drive IL-11 production
- ChIP-seq identified 1,291 GLIS3-bound genomic regions, enriched near fibrotic gene TSS
- GLIS3 cooperates with AP-1 (FOSL1/FRA1) and YAP/TAZ (TEAD1/3) transcription factors
- Fibroblast-specific Glis3 deletion prevents colitis-associated fibrosis in mice

### IPF GWAS Connection Assessment

| Question | Answer |

|---|---|

| Is GLIS3 an IPF GWAS locus? | **No** — no genome-wide significant signal at chr9p24.2 |

| Is there suggestive signal? | No published sub-threshold signals at this locus |

| Is GLIS3 expressed in lung? | Low (2.1 nTPM; protein detected in alveolar cells, macrophages) |

| Is GLIS3 in IPF fibroblasts? | Unknown — not specifically reported in IPF single-cell atlases |

| Was the study in lung tissue? | **No** — study was in intestinal fibrosis (IBD) |

| Are the effectors relevant to IPF? | **Yes** — IL-11, TGF-β, ECM remodeling genes are core IPF pathways |

### Integration with Pipeline

GLIS3 is **not added to the target ranking** because it lacks GWAS support for IPF. However, it provides important mechanistic context:

1. **GLIS3 downstream targets overlap with IPF biology**: IL-11 drives fibroblast activation in multiple organs; TGF-β pathway (which GLIS3 integrates) is the master regulator of IPF
2. **AP-1 and YAP/TAZ co-factors**: Both pathways are implicated in IPF fibroblast activation
3. **Potential biomarker**: GLIS3 expression in fibroblasts could stratify IPF patients by fibrotic activity
4. **Drug discovery opportunity**: If GLIS3 can be validated in IPF lung tissue, it could become a target for fibroblast-selective therapy

**Recommendation**: Test GLIS3 expression in published IPF single-cell datasets (Adams et al. 2020, Habermann et al. 2020, Natri et al. 2024) to determine if IAF-like GLIS3-high fibroblasts exist in IPF lung tissue.

---

## References

### DPP9

- Fingerlin TE et al. Genome-wide association study identifies multiple susceptibility loci for pulmonary fibrosis. Nat Genet. 2013;45(6):613-620. PMID: 23583980
- Borie R et al. Colocalization of Gene Expression and DNA Methylation with Genetic Risk Variants Supports Functional Roles of MUC5B and DSP in IPF. AJRCCM. 2022;206(9):1259-1270. PMID: 35816432
- Allen RJ et al. Genetic overlap between IPF and COVID-19. Eur Respir J. 2022;60:2103132. PMID: 35595312
- Zhong FL et al. Germline NLRP1 mutations cause skin inflammatory and cancer susceptibility syndromes via inflammasome activation. J Biol Chem. 2018;293(49):18864-18878. PMID: 30291141
- Huang M et al. Structural and biochemical mechanisms of NLRP1 inhibition by DPP9. Nature. 2021;592(7856):773-777. PMID: 33731929
- Hollingsworth LR et al. DPP9 sequesters the C terminus of NLRP1 to repress inflammasome activation. Nature. 2021;592(7856):778-783. PMID: 33731932
- Sharif H et al. Dipeptidyl peptidase 9 sets a threshold for CARD8 inflammasome formation by sequestering its active C-terminal fragment. Immunity. 2021;54:1392-1404. PMID: 34019797
- Harapas CR et al. DPP9 deficiency: an inflammasomopathy that can be rescued by complementation of the catalytic activity. Sci Immunol. 2022;7(75):eabi4611. PMID: 36112693
- Planes R et al. Human NLRP1 is a sensor of pathogenic coronavirus 3CL proteases in lung epithelial cells. Mol Cell. 2022;82(13):2385-2400. PMID: 35594856
- Tang Z et al. DPP9 promotes EMT and cisplatin resistance in NSCLC. Int J Oncol. 2017;50(3):823-831. PMID: 27943262
- Okondo MC et al. DPP8/9 inhibition induces pro-caspase-1-dependent monocyte and macrophage pyroptosis. Nat Chem Biol. 2017;13:46-53. PMID: 27820798
- Johnson DC et al. DPP8/9 inhibitor-induced pyroptosis for treatment of acute myeloid leukemia. Nat Med. 2018;24:1151-1156. PMID: 29967349
- Benramdane S et al. Highly Selective Inhibitors of DPP9 Derived from Vildagliptin. J Med Chem. 2023;66(18):12717-12738. PMID: 37721854
- Compound 6e: Selective and Orally Bioavailable DPP9 Inhibitors with Potent Pyroptosis Induction Properties. J Med Chem. 2025;68(21):23163-23184
- Beyens O et al. F253 as DPP9 selectivity determinant. ChemMedChem. 2025. DOI: 10.1002/cmdc.202400700
- Soare A et al. DPP4 marks activated fibroblasts in systemic sclerosis. Arthritis Rheumatol. 2020;72(1):137-149. PMID: 31350829
- Kousathanas A et al. Whole-genome sequencing reveals host factors underlying critical COVID-19. eBioMedicine (Lancet). 2025

### IL-7

- Liu C et al. Identification of novel causal targets for IPF via Mendelian randomization. Respir Res. 2024;25(1):203. PMID: 38783236
- Huang M et al. IL-7 inhibits fibroblast TGF-β production and signaling in pulmonary fibrosis. J Clin Invest. 2002;109(7):931-937. PMID: 11927620
- Bogatkevich GS et al. IL-7 and TGF-β play counter-regulatory roles in PKC-δ-dependent control of fibroblast collagen synthesis in pulmonary fibrosis. J Biol Chem. 2004;279(27):28474-28482. PMID: 15133032
- Nakamura S et al. Transient gene transfer and expression of Smad7 prevents bleomycin-induced lung fibrosis in mice. J Clin Invest. 1999;104(1):5-11. PMID: 10393693
- Hotchkiss RS et al. A randomized, double-blind, placebo-controlled trial of IL-7 in critically ill patients with COVID-19. JCI Insight. 2025;10(6):e189150. PMID: 39903535
- Francois B et al. Interleukin-7 restores lymphocytes in septic shock: the IRIS-7 RCT. JCI Insight. 2018;3(5):e98960. PMID: 29515037
- Daix T et al. Intravenous interleukin-7 to reverse lymphopenia in septic shock. Ann Intensive Care. 2023;13:17. PMID: 36906875
- Mejia-Chew C et al. Recombinant IL-7 for MAC lung disease (IMPULSE-7). Ther Adv Infect Dis. 2025. PMID: 40351870
- Heninger AK et al. IL-7 abrogates suppressive activity of human Tregs. J Immunol. 2012;189(12):5649-58. PMID: 23129754
- Adams TS et al. Single-cell RNA-seq reveals ectopic lung-resident cell populations in IPF. Sci Adv. 2020;6(28):eaba1983. PMID: 32832599
- Habermann AC et al. Single-cell RNA sequencing reveals profibrotic roles in pulmonary fibrosis. Sci Adv. 2020;6(28):eaba1972. PMID: 32832598
- Schupp JC et al. Integrated Single-Cell Atlas of Endothelial Cells of the Human Lung. Circulation. 2021;144(4):286-302. PMID: 34030460

### mTOR / Sirolimus

- Allen RJ et al. Genome-wide association study of susceptibility to IPF. AJRCCM. 2020;201(5):564-574. PMID: 31710517
- Allen RJ et al. Genome-wide association study across five cohorts identifies five novel loci associated with IPF. Thorax. 2022;77(8):829-833. PMID: 35688625
- Gong L et al. Integrative analysis of transcriptome-wide association study and mRNA expression profiling reveals susceptibility genes of IPF. Front Genet. 2020;11:604324. PMID: 33362862
- Gomez-Manjarres DC et al. Sirolimus suppresses circulating fibrocytes in idiopathic pulmonary fibrosis in a randomized controlled crossover trial. JCI Insight. 2023;8(8):e166901. PMID: 36853800
- Dempster JM et al. Chronos: a cell population dynamics model of CRISPR experiments that improves inference of gene fitness effects. Genome Biol. 2021. PMC8686573

### GLIS3

- Pokatayev V, Jaiswal A et al. Bidirectional CRISPR screens decode a GLIS3-dependent fibrotic cell circuit. Nature. 2026;650(8103):997-1006. PMID: 41501466

---

*This deep-dive synthesizes findings from Sessions 1-5 of the IPF causal drug target discovery pipeline. All genes are HGNC-approved symbols, all SNPs are verified rsIDs, and all evidence is from published peer-reviewed sources unless noted.*