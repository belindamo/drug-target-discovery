# DPP9 Therapeutic Paradox: A Deep Dive into the NLRP1 Inflammasome Axis and Fibrotic Biology

*Session 5 (2026-03-26) — Comprehensive mechanistic analysis*

---

## 1. The Core Paradox

DPP9 presents the most intellectually challenging target in the IPF pipeline:

- **Genetics says**: ↓DPP9 expression = ↑IPF risk (GWAS p=1.7e-12; fibroblast-specific coloc PP.H4=0.989)
- **Pharmacology says**: Only **inhibitors** exist (no activators) — and DPP9 inhibition activates the NLRP1 inflammasome, which drives pyroptosis and IL-1β release
- **In vivo says**: DPP9 KO is neonatally lethal (100% before weaning; PMID: 36112693)

This paradox — genetics pointing to DPP9 as protective but only inhibitors available — requires molecular-level resolution.

---

## 2. DPP9 Molecular Functions: Three Distinct Mechanisms

### 2.1 Inflammasome Regulation (NLRP1 + CARD8)

DPP9 represses inflammasome activation through two synergistic mechanisms (Nature 2021, PMID: 33731929 + 33731932):

1. **Scaffolding function**: Full-length NLRP1 and DPP9 form a 2:1 ternary complex. The ZU5 domain of NLRP1 is required for complex assembly. This complex sequesters the NLRP1 C-terminal UPA-CARD fragment, preventing higher-order oligomerization (ASC speck formation → caspase-1 activation → pyroptosis).

2. **Enzymatic function**: The N-terminus of the NLRP1 C-terminal fragment inserts into the DPP9 active site. DPP9 cleaves pro-NLRP1, and this catalytic activity contributes to keeping NLRP1 inactive. Val-boroPro (VbP) disrupts this interaction by occupying the active site.

**Key insight for the paradox**: Both scaffolding AND catalysis are required for full NLRP1 suppression. Therefore:
- **Genetic reduction of DPP9 expression** → less DPP9 protein → less scaffolding AND less catalysis → NLRP1 inflammasome activation → pyroptosis → inflammation → fibrosis
- **Pharmacological inhibition of DPP9** → blocks catalytic activity but **scaffolding is preserved** (DPP9 protein is still present, just enzymatically dead)

This distinction is critical: **expression loss ≠ enzymatic inhibition**. The genetic risk (reduced expression) removes the entire DPP9 protein, including its scaffolding function. An inhibitor only blocks the active site.

### 2.2 CARD8 Inflammasome Regulation

DPP9 also suppresses the CARD8 inflammasome, but through a **different mechanism** (ACS Chem Biol 2019, PMID: 31479242):

- DPP9's **enzymatic activity** (not protein binding) inhibits CARD8 activation
- This means DPP9 inhibitors WILL activate CARD8, regardless of scaffolding

Functional studies with selective compound 42 (2023–2025):
- Cpd-42 and cpd-6a induced **dose-dependent lytic cell death** in myeloid leukemia cell lines
- Both activated the **CARD8 inflammasome** (not NLRP1 in those cells)
- Affected monocytes, macrophages, dendritic cells; activated T cells least sensitive
- Notable: **No concurrent increase in IL-1β or IL-18 secretion** with CARD8-mediated pyroptosis

This last point is potentially important for the fibrosis application: CARD8-mediated cell death may be less inflammatory than NLRP1-mediated cell death.

### 2.3 Non-Inflammasome Functions

DPP9 has several inflammasome-independent roles:

| Function | Mechanism | Reference |
|---|---|---|
| **EMT regulation** | DPP9 knockdown → ↑E-cadherin, ↑MUC1, ↓vimentin, ↓S100A4, ↓SNAIL in NSCLC cells | PMID: 27943262 |
| **Cell migration** | DPP9 siRNA inhibits proliferation, migration, invasion in lung cancer | PMID: 27943262 |
| **Akt pathway** | DPP9 overexpression inhibits EGF-mediated Akt activation; induces apoptosis | Frontiers Pharmacol 2022 |
| **DNA repair** | DPP9 regulates BRCA2 concentration for homologous recombination | CMLS 2025 review |
| **N-degron pathway** | Removes N-terminal dipeptides (targets AK2, Syk for degradation) | CMLS 2025 review |
| **B cell signaling** | Destabilizes Syk kinase → regulates BCR responses | CMLS 2025 review |

**Critical for IPF**: The EMT connection is directly relevant. In NSCLC cells (PMID: 27943262):
- DPP9 **overexpression** → ↓E-cadherin, ↑vimentin (promotes EMT)
- DPP9 **knockdown** → ↑E-cadherin, ↓vimentin (inhibits EMT)

This creates a SECOND paradox: in cancer cells, DPP9 appears to PROMOTE EMT. If the same holds in fibroblasts, then DPP9 reduction (the IPF risk allele) should INHIBIT EMT — which is protective, not harmful. This contradicts the GWAS direction.

**Resolution**: The EMT data comes from cancer cells with fundamentally different signaling contexts. In fibroblasts, DPP9's primary protective role may be inflammasome suppression, not EMT regulation. The FAP-DPP9 axis in OSCC also shows that DPP9 overexpression reverses FAP-induced EMT — suggesting the DPP9-EMT relationship is cell-type and context-dependent.

---

## 3. The KEAP1-DPP9 Redox Axis: A New Dimension

A landmark 2024 study (JBC, PMID: 39615677) revealed an entirely new regulatory layer:

### 3.1 Mechanism
- The redox sensor **KEAP1** binds DPP9 in an **inactive (unfolded) conformation**
- KEAP1 stabilizes this non-native DPP9 fold
- Inactive DPP9 **reciprocally inhibits** KEAP1's ability to bind and degrade **NRF2**
- Result: DPP9 unfolding → NRF2 stabilization → antioxidant gene expression

### 3.2 Key Details
- **C844 on DPP9** is required for KEAP1 binding
- DPP9-KEAP1 binding is triggered by conditions that force DPP9 out of its native dimer (new protein expression, chemical denaturation)
- The physiological trigger is **unknown** — but likely stress-related

### 3.3 Implications for IPF

This connects DPP9 to **oxidative stress**, a well-established driver of IPF:

1. **In healthy lung**: DPP9 exists as an active dimer → suppresses NLRP1 → prevents inflammation
2. **Under oxidative stress**: Some DPP9 unfolds → binds KEAP1 → frees NRF2 → antioxidant response. This is a protective stress sensor.
3. **In IPF risk allele carriers**: Less DPP9 protein → less capacity for both NLRP1 suppression AND KEAP1 sequestration → impaired antioxidant response + enhanced inflammasome activation

This model predicts that DPP9 loss has a **double hit** on fibrosis:
- ↑Inflammasome activation → IL-1β → inflammatory cascade
- ↓NRF2 antioxidant response → oxidative damage → epithelial injury

### 3.4 Connection to Cancer
A 2023 study (PMID: 37713596) showed that in clear cell renal cell carcinoma:
- DPP9 binds KEAP1 via a conserved **ESGE motif**
- DPP9 competes with NRF2 for KEAP1 binding (enzyme-independent)
- DPP9 overexpression → NRF2 stabilization → suppresses ferroptosis → promotes cancer

This is consistent but reversed: in cancer, DPP9 overexpression is bad (promotes survival); in IPF, DPP9 reduction is bad (loses antioxidant protection).

---

## 4. In Vivo Evidence: DPP Inhibitors in Fibrosis Models

### 4.1 Talabostat (PT100) in Bleomycin Model (2017, PMID: 28506908)

Talabostat is a **non-selective** pan-DPP inhibitor (DPP4, FAP, DPP8/9):
- Bleomycin-challenged mice treated with PT100 showed **significantly less fibrosis** than vehicle-treated controls
- Fibrotic lesions did not progress in PT100-treated animals
- **However**: No effect on type I collagen mRNA
- **Caveat**: PT100 inhibits FAP (fibroblast activation protein) which may drive the antifibrotic effect, not DPP8/9

### 4.2 Talabostat in Systemic Sclerosis Fibroblasts (2024–2025)

- TGF-β-stimulated SSc fibroblasts treated with talabostat showed **attenuation of pro-fibrotic genes**
- **Concentration-dependent inhibition** of activated fibroblast viability
- **Suppressed fibroblast migration**
- **Inhibited myofibroblast differentiation, activation, and migration**

### 4.3 DPP9-Specific In Vivo Fibrosis Data

**No published study** (as of March 2026) has tested a **DPP9-selective inhibitor** in a pulmonary fibrosis model. This is a critical gap in the field.

### 4.4 DPP Inhibitor and Asthma
The 2025 CMLS review notes that DPP inhibitor treatment showed **partial protection against asthma** and reduced collagen deposition — suggesting anti-fibrotic potential in the lung.

### 4.5 Hepatocyte-Specific DPP9 KO (2025)
A conditional KO study showed:
- DPP9 loss in hepatocytes is **benign** (no lethality)
- No differences in fibrosis or steatosis in DPP9-KO livers
- But: **increased active caspase-1** (inflammasome activation confirmed)
- Tolerable in liver suggests tissue-specific DPP9 modulation may be safe

---

## 5. Resolving the Therapeutic Paradox: Five Possible Strategies

### Strategy 1: Downstream Anti-IL-1β Therapy (Genetically Aligned)

**Rationale**: If ↓DPP9 → ↑NLRP1 → ↑IL-1β → fibrosis, then blocking IL-1β directly addresses the genetic mechanism.

| Drug | Target | Status | Notes |
|---|---|---|---|
| Anakinra | IL-1R antagonist | Approved (RA) | Short half-life; would need inhaled formulation |
| Canakinumab | Anti-IL-1β mAb | Approved (CAPS, gout) | CANTOS showed CV benefit; monthly SC injection |
| Rilonacept | IL-1 trap | Approved (pericarditis) | Weekly SC injection |

**Evidence**: DPP9-deficient mice rescued by single-allele deletion of IL-1R (Sci Immunol 2021, PMID: abi4611). This proves that even **partial** IL-1 pathway blockade is sufficient to rescue DPP9 loss-of-function.

**Assessment**: ★★★★★ — Most genetically aligned strategy. Clinical-grade drugs exist. Anti-IL-1β in IPF has not been tested.

### Strategy 2: Partial DPP9 Enzymatic Inhibition

**Rationale**: Low-dose, partial inhibition might avoid catastrophic inflammasome activation while gaining anti-fibrotic benefits through FAP/DPP4 cross-inhibition or fibroblast modulation.

**Evidence**:
- Talabostat showed antifibrotic effects in bleomycin model
- SSc fibroblast data shows dose-dependent anti-fibrotic activity
- Hepatocyte-specific KO is benign despite inflammasome activation

**Risks**:
- Dose window may be extremely narrow
- CARD8 activation is purely dose-dependent (no scaffolding protection)
- Neonatal lethality of full KO suggests low margin

**Assessment**: ★★☆☆☆ — Theoretically possible but high risk. Needs DPP9-selective inhibitor tested in fibrosis models first.

### Strategy 3: DPP9 Expression Enhancement (Gene Therapy/ASO)

**Rationale**: Since the genetic risk is ↓expression, increasing DPP9 expression is the most direct correction.

**Approaches**:
- CRISPRa targeting DPP9 promoter in lung fibroblasts
- Inhaled mRNA encoding DPP9 (like COVID vaccines)
- Antisense oligonucleotide targeting DPP9 regulatory elements to enhance transcription

**Assessment**: ★★★☆☆ — Scientifically ideal but technically challenging. No existing tools; would require de novo development.

### Strategy 4: NLRP1-Specific Inhibition

**Rationale**: Block the downstream inflammasome sensor directly, rather than modulating DPP9.

**Status**:
- No approved NLRP1 inhibitors exist
- NLRP3 inhibitors (dapansutrile, MCC950) are in development for other diseases
- NLRP1 is structurally distinct from NLRP3; different inhibitor chemistry needed

**Assessment**: ★★☆☆☆ — Promising concept but no clinical-grade molecules.

### Strategy 5: NRF2 Activation (KEAP1 Disruption)

**Rationale**: If DPP9 loss impairs the KEAP1-NRF2 antioxidant axis, directly activating NRF2 may compensate.

| Drug | Mechanism | Status |
|---|---|---|
| Dimethyl fumarate (Tecfidera) | NRF2 activator | Approved (MS) |
| Bardoxolone | Potent NRF2 activator | Failed Phase 3 (kidney) — safety concerns |
| Sulforaphane | Dietary NRF2 activator | Supplements available |

**Evidence**: NRF2 activation is antifibrotic in multiple organ systems. Dimethyl fumarate has been proposed for fibrotic diseases.

**Assessment**: ★★★☆☆ — Addresses one arm of the DPP9 paradox (redox). Clinical-grade drugs exist. But does not address inflammasome arm.

---

## 6. Integrated Therapeutic Model

The optimal strategy may combine approaches:

```
DPP9 genetic risk (↓expression)
    │
    ├── ↑NLRP1/CARD8 inflammasome ──→ Anti-IL-1β (anakinra/canakinumab)  [Strategy 1]
    │       ↓
    │   ↑IL-1β, ↑pyroptosis
    │       ↓
    │   Inflammatory cascade → Fibrosis
    │
    └── ↓KEAP1 sequestration ──────→ NRF2 activator (dimethyl fumarate)  [Strategy 5]
            ↓
        ↓NRF2 antioxidant response
            ↓
        Oxidative damage → Epithelial injury → Fibrosis
```

**Recommended first-line approach**: Anti-IL-1β therapy (anakinra or canakinumab) in IPF patients genotyped for rs12610495-G (DPP9 risk allele). This would be the first genotype-stratified IPF trial.

---

## 7. Key Unanswered Questions

1. **Does DPP9 enzymatic inhibition activate NLRP1 in lung fibroblasts specifically?** — The fibroblast-specific coloc (PP.H4=0.989) suggests fibroblasts are the key cell type, but inflammasome activation has been studied primarily in myeloid cells.

2. **What is the physiological trigger for DPP9 unfolding and KEAP1 binding?** — The 2024 JBC paper identified the interaction but not the endogenous stimulus.

3. **Does the DPP9-NLRP1 axis explain the IPF-COVID overlap?** — Both diseases share the DPP9 risk locus. COVID-19 involves massive inflammasome activation. The shared mechanism may be NLRP1/CARD8 activation in the lung.

4. **Can tissue-specific DPP9 modulation be achieved?** — Hepatocyte KO is tolerable; what about fibroblast-specific KO?

5. **What is the relative contribution of inflammasome vs. non-inflammasome DPP9 functions to IPF risk?** — The EMT, Akt, and KEAP1 pathways may be quantitatively more important than inflammasome activation in fibroblasts.

---

## 8. Summary Assessment

| Criterion | Assessment |
|---|---|
| Genetic evidence strength | ★★★★★ (GWAS p=1.7e-12; fibroblast coloc PP.H4=0.989) |
| Mechanistic understanding | ★★★★☆ (inflammasome + EMT + redox; cell-type specificity unclear) |
| Druggability | ★★★★☆ (selective nanomolar inhibitors exist; wrong direction for genetics) |
| Therapeutic clarity | ★★☆☆☆ (paradox partially resolved; downstream IL-1β blockade is aligned) |
| Clinical readiness | ★★★☆☆ (anti-IL-1β drugs are approved for other indications) |
| Novelty for IPF | ★★★★★ (no anti-IL-1β trial in IPF; genotype-stratified trial would be first) |

**Bottom line**: DPP9 is not a conventional drug target where you simply inhibit or activate. It is a **genetic signpost** pointing to the IL-1β/inflammasome pathway AND the NRF2/oxidative stress pathway as causal in IPF. The therapeutic value of DPP9 lies in identifying the **downstream pathways** it controls, not in directly modulating DPP9 itself.

---

*Sources: Nature 2021 (PMID: 33731929, 33731932); JBC 2024 (PMID: 39615677); J Med Chem 2023 (PMID: 37721854); CMLS 2025 DPP9 review (PMC12037458); Sci Immunol 2021 (PMID: abi4611); PMID: 27943262 (NSCLC EMT); PMID: 28506908 (PT100 bleomycin); PMID: 37713596 (ccRCC KEAP1); eBioMedicine 2025 (IPF-COVID shared aetiology)*
