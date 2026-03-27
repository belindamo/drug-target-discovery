# DPP9 Therapeutic Strategy Deep-Dive: Resolving the Paradox

*Session 5 (2026-03-26) — Comprehensive analysis of the DPP9–NLRP1–CARD8 inflammasome axis, partial inhibition window, and therapeutic alternatives*

---

## 1. The DPP9 Paradox Restated

DPP9 sits at the intersection of IPF's strongest genetic-pharmacological disconnect:

| Evidence Layer | Finding | Implication |
|---|---|---|
| GWAS | rs12610495 (19p13.3) p=1.7e-12 | Strong causal locus |
| Coloc (fibroblasts) | PP.H4 = 0.989 (rs2277732) | Fibroblast-specific causal variant |
| Coloc (IPF cases) | PP.H4 = 0.874 (rs12462642) | Validated in disease tissue |
| Direction | Risk allele → **decreased** DPP9 expression | Lower DPP9 = more disease |
| Available compounds | Cpd 42/47 — DPP9 **inhibitors** (175x selective, Ki ~nM) | Only inhibitors exist — **wrong direction** |
| Global KO | Neonatal lethal via NLRP1 inflammasome | Complete loss intolerable |

**The core paradox**: Genetics says "increase DPP9 activity to reduce IPF risk," but only inhibitors exist. Directly activating a protease is pharmacologically impractical. How do we therapeutically exploit this biology?

---

## 2. DPP9's Dual Mechanism of NLRP1/CARD8 Suppression

DPP9 keeps NLRP1 and CARD8 inflammasomes inactive through **two independent mechanisms** (Nature 2021, PMID: 33731929 + 33731932):

### 2a. Enzymatic Activity (Protease)
- DPP9 cleaves nascent N-terminal fragments of NLRP1 after its autoproteolytic FIIND domain processing
- This removes the activating signal before it can nucleate an inflammasome
- Demonstrated by: DPP9 S759A catalytic-dead mutant only partially rescues NLRP1 activation in DPP8/9-null cells (ACS Chem Biol 2019, PMID: 31525884)

### 2b. Scaffolding / Sequestration (Non-enzymatic)
- DPP9 physically sequesters the NLRP1/CARD8 C-terminal fragment in a ternary complex
- Cryo-EM structure shows: full-length NLRP1 + C-terminal fragment + DPP9 dimer (Nature 2021, PMID: 33731929)
- This prevents the C-terminal UPA-CARD fragment from forming ASC specks → no pyroptosis
- Demonstrated by: catalytic-dead DPP9 still partially suppresses inflammasome

### Key Insight for Therapy
The **graded nature** of these two mechanisms is critical. Partial pharmacological DPP9 inhibition (blocking enzymatic activity while preserving scaffolding) would produce a **graded, not binary** inflammasome response. This is the conceptual basis for a therapeutic window.

---

## 3. Evidence That Tissue-Specific Partial DPP9 Loss Is Tolerable

### 3a. Global DPP9 KO: Lethal
- DPP9-null mice die within 24 hours of birth (PMID: 36112693)
- Driven almost entirely by NLRP1 inflammasomopathy
- Rescued by removing a single copy of *Nlrp1a/b/c*, *Asc*, *Gsdmd*, or *Il-1r* (but NOT *Il-18*) — Sci Immunol 2021, PMID: 34652968
- This proves: the lethal phenotype is IL-1β-dependent, not IL-18-dependent

### 3b. Hepatocyte-Specific DPP9 KO: **Tolerated**
- Albumin-Cre × DPP9-floxed mice: viable, normal lifespan (ScienceDirect 2025; ASCO 2025 abstract)
- Phenotype: reduced liver/adipose mass, lower fasting glucose, some cleaved caspase-1
- **Critically**: no pyroptosis, no overt inflammation, no NLRP1-driven pathology
- Suggests: tissue-specific DPP9 reduction is tolerable, and NLRP1 activation was a "minor mechanism" in hepatocytes
- Alternative mechanisms predominated: **autophagy** (all 4 markers elevated) and **p53 tumor suppression**

### 3c. Implications for Lung
- The hepatocyte data suggests that partial DPP9 inhibition in a tissue-specific manner may be tolerable
- However, lung fibroblasts (where IPF DPP9 coloc signal is strongest) may behave differently
- NLRP1 expression varies by cell type: high in keratinocytes, moderate in monocytes/macrophages, variable in fibroblasts
- **Unanswered question**: What is NLRP1 expression in IPF fibroblasts specifically?

---

## 4. DPP9's Non-Inflammasome Functions in Fibrosis

The inflammasome is not the only pathway. DPP9 has fibrosis-relevant functions independent of NLRP1/CARD8:

### 4a. FAP-DPP9 Interaction and EMT
- FAP (Fibroblast Activation Protein) physically interacts with DPP9 intracellularly (PMID: 32273729)
- FAP overexpression **downregulates DPP9** → promotes EMT (epithelial-mesenchymal transition)
- DPP9 overexpression **reverses** FAP-induced proliferation, migration, invasion, and EMT
- This is a **non-enzymatic interaction** — independent of DPP9 protease activity
- **IPF relevance**: FAP is a hallmark marker of activated myofibroblasts (the key effector cell in IPF fibrosis). GLIS3 CRISPR screen identified FAP as a direct transcriptional target (Nature 2026). The FAP-DPP9 axis directly connects DPP9 genetics to fibroblast activation.

### 4b. Cell Adhesion and Migration
- The IPF risk allele (rs12610495-G) reduces DPP9 expression in fibroblasts
- Context-specific eQTL study (medRxiv 2024) linked this to "impaired cell adhesion and migration affecting lung tissue repair"
- Lower DPP9 → impaired fibroblast wound healing → aberrant repair → fibrosis
- This is mechanistically distinct from inflammasome activation

### 4c. Autophagy Regulation
- Hepatocyte DPP9-KO showed increased autophagy markers (4/4 markers elevated)
- Autophagy dysregulation is a known feature of IPF (PMID: 36853800 — sirolimus trial)
- DPP9-mTOR connection: DPP9 may regulate autophagy via mTOR-independent mechanisms
- Convergence with our DEPTOR/NPRL3 mTOR pathway findings

---

## 5. Therapeutic Strategy Options

Given the paradox, there are **four viable approaches** to exploit DPP9 biology:

### Strategy A: Downstream Anti-IL-1β (Genetically Aligned)

**Rationale**: If reduced DPP9 → increased NLRP1 activation → increased IL-1β → fibrosis, then blocking IL-1β is the genetically aligned intervention.

| Drug | Status | IPF Data |
|---|---|---|
| Anakinra (IL-1Ra) | Approved (RA) | No IPF trial; COVID-19 lung data (PMID: 33377883) |
| Canakinumab (anti-IL-1β mAb) | Approved (CAPS, gout) | CANTOS showed CV benefit + cancer reduction (PMID: 28845751); NO IPF trial |
| Rilonacept (IL-1 trap) | Approved (CAPS, pericarditis) | No IPF trial |

**Strength**: Existing approved drugs; genetically aligned direction (block IL-1β excess from NLRP1 de-repression)
**Weakness**: IL-1β blockade is immunosuppressive; IPF patients already infection-prone; may not address non-inflammasome DPP9 functions
**Evidence level**: Strong genetic + mechanistic; no direct IPF clinical data
**Recommendation**: **Anakinra proof-of-concept trial in IPF is warranted** — lowest-risk path to test the genetic hypothesis

### Strategy B: DPP9 Gene Therapy / mRNA (Restore Expression)

**Rationale**: The genetics say "more DPP9 is protective." Deliver DPP9 directly to the lung.

| Approach | Feasibility |
|---|---|
| AAV-DPP9 lung delivery | Technically possible; lung-tropic AAVs exist (AAV6.2, AAV5) |
| LNP-mDPP9 mRNA (inhaled) | IPF-relevant inhaled LNP platform exists (SPL5B uses this for MUC5B) |
| CRISPR activation (CRISPRa) | Targeting DPP9 promoter to boost expression; preclinical |

**Strength**: Directly addresses the genetic deficiency
**Weakness**: No existing clinical-grade DPP9 gene therapy; would require de novo development; delivery to fibroblasts (not epithelium) is the target cell
**Evidence level**: Theoretical; no preclinical data
**Recommendation**: Long-term option; not immediately actionable

### Strategy C: Partial DPP9 Inhibition for Non-Inflammasome Effects

**Rationale**: The hepatocyte-specific KO data suggests tissue-specific DPP9 reduction is tolerable. If the anti-fibrotic benefit comes primarily from **non-inflammasome** pathways (EMT reversal, autophagy modulation), partial inhibition might paradoxically help by triggering compensatory mechanisms.

**This is speculative and should NOT be pursued** without significantly more preclinical data. The direction is wrong per genetics.

### Strategy D: Target the FAP-DPP9 Axis

**Rationale**: FAP downregulates DPP9 non-enzymatically, promoting EMT. FAP inhibitors could indirectly restore DPP9 function in fibroblasts.

| Drug | Status | Notes |
|---|---|---|
| 177Lu-FAP-2286 (radioligand) | Phase 1/2 (cancer) | Too toxic for IPF |
| FAP-targeted CAR-T | Phase 1 (cardiac fibrosis) | Tao et al. Science 2024; PMID: 38096411 |
| Small-molecule FAP inhibitors | Tool compounds | Talabostat (Val-boroPro) activates CARD8 — counterproductive |

**Strength**: Addresses the non-inflammasome mechanism; FAP is well-validated in fibrosis
**Weakness**: FAP is DPP family member — selectivity issues; FAP inhibitors may cross-react with DPP9
**Evidence level**: Moderate genetic + mechanistic; indirect path
**Recommendation**: Monitor cardiac fibrosis CAR-T data; consider FAP biology in IPF context

---

## 6. Revised Therapeutic Recommendation

### Primary recommendation: **Anti-IL-1β therapy (Strategy A)**

The strongest genetically-aligned, immediately actionable intervention is:

> **Anakinra (recombinant IL-1 receptor antagonist) proof-of-concept trial in IPF**

Supporting evidence chain:
1. rs12610495-G decreases DPP9 expression in fibroblasts (PP.H4=0.989)
2. Decreased DPP9 → de-repressed NLRP1 inflammasome → increased IL-1β
3. Global DPP9-KO lethality is rescued by removing one copy of *Il-1r* (not *Il-18*)
4. IL-1β drives fibroblast activation and collagen deposition in pulmonary fibrosis
5. Anakinra is FDA-approved, safe (>20 years of clinical use), and has COVID-19 lung data showing anti-inflammatory benefit

### Secondary recommendation: **NLRP1-specific inhibitors**

Unlike pan-inflammasome blockers, NLRP1-specific inhibitors would precisely target the de-repressed inflammasome without affecting NLRP3 (which may have protective functions in tissue repair):

- NLRP1 is the specific inflammasome activated by DPP9 loss
- No NLRP1-specific inhibitors are currently approved, but academic programs exist
- This would be more selective than IL-1β blockade

### Tertiary recommendation: **Monitor FAP-targeted approaches**

FAP-directed therapies in cardiac fibrosis (CAR-T, small molecules) should be monitored for applicability to IPF via the FAP-DPP9 axis.

---

## 7. Updated DPP9 Target Profile

| Parameter | Value | Source |
|---|---|---|
| Gene | DPP9 (19p13.3) | HGNC:20823 |
| GWAS p-value | 1.7e-12 | PMID:23583980 |
| Causal evidence tier | Tier 1 (Strong) | GWAS + coloc + eQTL |
| Colocalization (fibroblasts) | PP.H4 = 0.989 | Context-specific eQTL 2024 |
| Genetic direction | ↓DPP9 → ↑IPF risk | Risk allele decreases expression |
| Therapeutic direction | **Activate DPP9** (or block downstream IL-1β) | Genetics-aligned |
| Direct druggability | Paradox: only inhibitors exist | Cpd 42/47 (JMedChem 2023) |
| Downstream druggability | **Tier 1**: anakinra/canakinumab (approved) | Anti-IL-1β is aligned |
| DepMap safety | Not essential (0.3% dependent) | DepMap 25Q3 |
| Cross-ancestry | Moderate (EUR only, EAS untested) | Global allele 12.9–28.8% |
| Key biology | Dual NLRP1/CARD8 repressor + FAP-EMT axis + autophagy | Multiple pathways |
| Key risk | Complete DPP9 inhibition lethal (NLRP1 inflammasomopathy) | PMID: 36112693 |
| Key opportunity | Anti-IL-1β repurposing; genetically aligned; immediately actionable | Novel for IPF |

---

## 8. Open Questions

1. **What is NLRP1 expression in IPF fibroblasts?** Cell-type-specific NLRP1/CARD8 expression data in IPF lung scRNA-seq would clarify whether the inflammasome axis is active in the key effector cell.
2. **Does the FAP-DPP9 interaction occur in IPF fibroblasts?** This non-enzymatic pathway could be the primary mechanism, independent of inflammasome.
3. **Can partial DPP9 activation be achieved pharmacologically?** Allosteric activators, protein stabilizers, or CRISPRa approaches could bypass the inhibitor-only problem.
4. **IL-18 vs IL-1β in IPF**: Global DPP9-KO rescue experiments show IL-1R (not IL-18) drives lethality. But does IL-18 contribute to fibrosis specifically?
5. **What fraction of DPP9's IPF effect is inflammasome-dependent vs independent?** The hepatocyte KO data suggests non-inflammasome mechanisms may predominate in some tissues.

---

*This analysis integrates data from Nature (2021), Science Immunology (2021), J Med Chem (2023), ChemMedChem (2025), ScienceDirect (2025), ACS Chem Biol (2019), and the context-specific eQTL study (medRxiv 2024). All cited PMIDs verified.*
