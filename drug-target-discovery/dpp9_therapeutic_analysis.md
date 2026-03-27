# DPP9 Therapeutic Strategy Analysis: Resolving the Paradox

*Session 5 deep-dive — 2026-03-26*

## The DPP9 Paradox Summarized

DPP9 (rs12610495, 19p13.3) is one of the strongest genetically validated IPF targets:
- GWAS p = 1.7e-12 (Fingerlin 2013, PMID: 23583980)
- Colocalization PP.H4 = 0.989 in fibroblasts (Borie 2022, PMID: 35816432)
- Risk allele **decreases** DPP9 expression
- Shared with severe COVID-19 (same direction — reduced DPP9 = risk)

**The paradox**: Genetics says we need MORE DPP9 activity, but the only available pharmacological tools are DPP9 **inhibitors**. This analysis resolves the paradox by examining DPP9's dual mechanisms and identifying genetically aligned therapeutic strategies.

---

## 1. DPP9 as a Dual-Mechanism Target

### Mechanism A: NLRP1/CARD8 Inflammasome Suppression (Immune Cells)

DPP9 suppresses the NLRP1 and CARD8 inflammasomes via **two synergistic mechanisms**:

1. **Enzymatic activity**: DPP9's serine protease activity cleaves N-terminal post-proline peptides, maintaining inflammasome components in their inactive form (Zhong et al., J Biol Chem 2018, PMID: 30291141)
2. **Scaffolding/sequestration**: DPP9 forms a 2:1 ternary complex with NLRP1, where one DPP9 dimer binds both a full-length NLRP1 molecule and an active UPA-CARD fragment, physically sequestering the bioactive C-terminal fragment (Hollingsworth et al., Nature 2021, PMID: 33731929; Huang et al., Nature 2021, PMID: 33731932)

**Key distinction**: DPP9 restrains NLRP1 and CARD8 via **different mechanisms**:
- For **NLRP1**: Both binding AND enzymatic activity required. DPP8/9 inhibitors disrupt the NLRP1-DPP9 interaction directly.
- For **CARD8**: Enzymatic activity alone is sufficient. The CARD8-DPP9 binding interaction is NOT disrupted by inhibitors (Gai et al., ACS Chem Biol 2019, PMC: 6862324)

When DPP9 is lost (as in IPF risk allele carriers): NLRP1/CARD8 activate → caspase-1 → gasdermin D cleavage → pyroptosis + IL-1β/IL-18 release → pro-inflammatory/pro-fibrotic cascade.

### Mechanism B: EMT Suppression (Fibroblasts) — NEW

DPP9 has a distinct, **inflammasome-independent** role in suppressing epithelial-mesenchymal transition (EMT):

- **FAP–DPP9 axis**: Fibroblast Activation Protein (FAP) overexpression **downregulates DPP9** non-enzymatically, promoting EMT. DPP9 overexpression reverses FAP-driven proliferation, migration, invasion, and EMT in oral squamous cell carcinoma (PMID: 32273729)
- **ZEB1 stabilization**: In breast cancer, DPP9 deficiency stabilizes the EMT-promoting transcription factor ZEB1, accelerating TGF-β1-induced EMT (Dipeptidyl peptidase 9 regulates dynamics of tumorigenesis, PMID: 38531482)
- **Cell adhesion**: DPP9 localizes to the leading edge of migrating cells, colocalizing with focal adhesion proteins (integrin-β1, talin). DPP9 silencing reduces focal adhesion kinase phosphorylation and cell migration (Paxillin/FAK pathway)
- **EMT markers**: DPP9 knockdown in NSCLC increases E-cadherin and MUC1, and decreases vimentin and S100A4 — classic mesenchymal markers (Tang et al., Int J Cancer 2017, PMID: 27943262)

**Relevance to IPF**: In the IPF fibrotic niche, FAP is highly expressed on activated fibroblasts. The DPP9 risk allele (reduced expression) would release the brake on FAP-driven EMT, promoting fibroblast activation and myofibroblast differentiation **independently of inflammasome activation**. This explains why the DPP9 colocalization signal is strongest in **fibroblasts** (PP.H4 = 0.989), not immune cells.

### New: DPP9-KEAP1 Redox Sensing

DPP9 and the redox sensor KEAP1 form a mutually inhibitory complex (Mena et al., J Biol Chem 2024, PMID: 39615677). Inactive DPP9 inhibits KEAP1's ability to degrade NRF2, inducing an antioxidant response. This links DPP9 to the oxidative stress axis in IPF — reduced DPP9 would impair NRF2-mediated antioxidant defenses.

### Mechanism C: Non-Catalytic Scaffolding — Ubiquitin Signaling Complexes (NEW 2026)

TurboID proximity labeling in DPP9-KO HEK293 cells mapped DPP9's non-catalytic interactome (CMLS, February 2026, DOI:10.1007/s00018-025-06021-z):

- **BRISC complex** (BRCC36/BRCC3 + ABRO1/ABRAXAS2): DPP9 outcompetes BRCC36 from binding ABRO1, disrupting BRISC assembly. BRISC deubiquitinates IFNAR1, NLRP3, JAK2, Aurora B kinase.
- **CYLD-SPATA2 complex**: DPP9 disrupts CYLD-SPATA2 interaction. CYLD = tumor suppressor deubiquitinase.
- **E3 ligase CBL**: Novel validated DPP9 interactor (NanoBRET confirmed).
- **Autophagy/mRNA decay**: Also enriched in proximity labeling.

This establishes DPP9 as a broader modulator of inflammasome signaling — acting both through direct NLRP1/CARD8 interactions AND upstream ubiquitin signaling control. Raises question: does DPP9 also modulate pyroptosis via CYLD-mediated NLRP3 deubiquitination?

### Mechanism D: PD-L1 Regulation via BRISC-SHMT2-IFNAR1 (NEW 2026)

DPP9 regulates PD-L1 in clear cell renal carcinoma (Zhang et al., Cell Death Differ 2026, DOI:10.1038/s41418-026-01704-x):

- DPP9 disrupts SHMT2 from BRISC → BRISC-mediated deubiquitination of IFNAR1 reduced → IFNAR1 degradation → less JAK/STAT → less PD-L1 transcription
- 1G244 (DPP9 inhibitor) reverses this → IFNAR1 stabilized → PD-L1 upregulated
- 1G244 + anti-CTLA-4 = synergistic anti-tumor immunity in vivo (MS data: ProteomeXchange PXD059150/PXD059151)

**IPF relevance**: Primarily cancer biology, but DPP9 loss in IPF may alter type I IFN signaling in the lung. IFN signaling is generally anti-fibrotic; DPP9 loss → destabilized IFNAR1 → reduced IFN signaling → possible pro-fibrotic shift. This is speculative but mechanistically coherent.

**Updated model**: DPP9 is now a QUADRUPLE-mechanism target (catalytic inflammasome suppression + EMT suppression + ubiquitin scaffold + PD-L1/IFN regulation).

---

## 2. Genetic Evidence for Partial Inhibition / Downstream Targeting

### The Harapas et al. 2022 Experiment (Science Immunology, PMID: 36112693)

This is the **single most important study** for understanding DPP9-based therapeutics:

**Patients**: Three families with biallelic DPP9 variants (hypomorphic/knockout alleles) presenting with immune defects, poor growth, pancytopenia, and skin pigmentation abnormalities — a new Mendelian "inflammasomopathy."

**Mouse rescue experiments**: Dpp9 S759A/S759A (catalytically dead) mice die neonatally. Remarkably:
- Removing **a single copy** of Nlrp1a/b/c → **rescued** lethality
- Removing **a single copy** of ASC → **rescued** lethality
- Removing **a single copy** of GSDMD → **rescued** lethality
- Removing **a single copy** of IL-1R → **rescued** lethality (mice reached adulthood)
- Removing **a single copy** of IL-18 → **NOT rescued**

**Critical interpretation**: The downstream pathology of DPP9 loss is **primarily driven by IL-1β** (not IL-18). Even **halving** the IL-1 signal rescues the phenotype. This directly demonstrates that:

1. **Anti-IL-1β therapy** (anakinra, canakinumab) is the genetically aligned intervention for DPP9-loss phenotypes
2. **Partial modulation** is sufficient — you don't need complete IL-1β blockade
3. The therapeutic window is wide: haploinsufficiency of any downstream component rescues fully

### Pinocembrin: A Natural DPP9 Activator (2024)

Pinocembrin, a flavonoid compound, has been shown to **activate DPP9** expression, thereby inhibiting NLRP1 inflammasome activation and alleviating cerebral ischemia/reperfusion-induced organ injury (Immunol Res 2024). This is the first report of a compound that **activates** rather than inhibits DPP9 — although it is a polypharmacology natural product, not a selective DPP9 activator.

---

## 3. Therapeutic Strategy Matrix

| Strategy | Mechanism | Genetic Alignment | Feasibility | Priority |
|----------|-----------|-------------------|-------------|----------|
| **Anti-IL-1β (anakinra/canakinumab)** | Block downstream inflammasome output | **Perfect** — IL-1R haploinsufficiency rescues DPP9 loss | **High** — approved drugs, safe, never tested in IPF | **#1** |
| **Anti-IL-1R (rilonacept)** | IL-1 trap | **Perfect** — same mechanism | **High** — approved, long half-life | **#1 alternative** |
| **Sirolimus (mTOR pathway)** | May partially compensate via parallel pathway | **Moderate** — converges with DEPTOR/NPRL3 | **High** — approved, piloted in IPF | **#2** |
| **DPP9 activation (pinocembrin class)** | Restore DPP9 activity directly | **Perfect** — restores what genetics says is lost | **Low** — no selective activator available; natural product pharmacology | **Future** |
| **Selective DPP9 inhibitors for cancer** | Activate inflammasome → pyroptosis | **WRONG direction for IPF** | N/A for IPF | **Not for IPF** |

---

## 4. DPP9 Inhibitors — State of the Art (Not for IPF, but Important Context)

### First-Generation: Compounds 42 & 47 (J Med Chem 2023, PMID: 37721854)
- Derived from vildagliptin (DPP4 inhibitor) scaffold
- Compound 42: Ki ~nM for DPP9; selectivity index 175x over DPP8; >1000x over all other proline-selective proteases
- F253 identified as key selectivity residue (ChemMedChem 2025)
- **PK limitation** (Nguyen 2025 CMLS): Only 2% oral bioavailability, <45 min half-life in mice

### Second-Generation: Compound 6e (J Med Chem 2025, DOI: 10.1021/acs.jmedchem.5c02049)
- Oral bioavailability demonstrated in healthy rats
- Long in vivo and microsomal half-life
- Potent pyroptosis induction in AML cell lines
- Full DPP9-to-DPP8 selectivity maintained
- Intended for AML therapy, NOT fibrosis

### ICeD-2: Best Available In Vivo Tool (ACS Chem Biol 2022, PMID: 36044633)
- 27x DPP9-preferring selectivity (less selective than Cpd 42 but adequate)
- **61% oral bioavailability** — vastly superior to Cpd 42
- **20 hour half-life** — suitable for chronic dosing studies
- Recommended tool compound for any in vivo DPP9 fibrosis study

### TC-E5007: Anti-Fibrotic DPP8/9 Inhibitor (PMID: 33932609)
- Non-selective DPP8/9 inhibitor
- **ANTI-FIBROTIC in kidney UUO model** via TGF-β1/Smad pathway suppression
- Paradoxical: DPP9 inhibition reduced fibrosis despite genetic data suggesting opposite
- Supports cell-type-specific effects hypothesis: anti-fibrotic in fibroblasts, pro-inflammatory in immune cells

### Cancer Applications (Not IPF)
- **AML**: DPP8/9 inhibitors induce CARD8-mediated pyroptosis in leukemia cells (Nat Med 2018)
- **HIV-1**: DPP9 inhibition synergizes with NNRTIs to clear HIV-infected lymphocytes (Nat Chem Biol 2022)
- **ccRCC (2026)**: DPP9 inhibition disrupts BRISC-mediated PD-L1 expression; 1G244 + anti-CTLA-4 enhances antitumor immunity (Cell Death Differ 2026)
- **Hepatocellular carcinoma**: DPP9 deletion improves energy metabolism, may reduce liver cancer initiation via autophagy (ScienceDirect 2025)

These cancer applications use DPP9 **inhibition** to activate the inflammasome — the **opposite** of what's needed for IPF. This underscores why the IPF strategy must be downstream (anti-IL-1β) rather than direct DPP9 modulation.

---

## 5. Proposed IPF Clinical Strategy

### Trial Design: Anti-IL-1β in IPF

**Rationale**: DPP9 GWAS + colocalization + Harapas rescue experiment = genetic chain from DPP9 loss → NLRP1 activation → IL-1β → fibrosis. Anakinra/canakinumab are approved, safe agents that have never been tested in IPF despite this rationale.

**Patient enrichment**: Select IPF patients with:
- DPP9 risk genotype (rs12610495-G carriers, ~25% EUR)
- Elevated BAL or serum IL-1β levels
- Early/moderate disease (FVC >50% predicted)

**Endpoints**: Primary: FVC change at 52 weeks. Secondary: HRCT fibrosis score, 6MWD, PRO-IPF.

**Drug**: Canakinumab (anti-IL-1β mAb, q8w SC) preferred over anakinra (daily SC) for adherence. Rilonacept (IL-1 trap) also viable.

**Risk mitigation**:
- Well-established safety profile (>10,000 patients dosed globally)
- No immunosuppression beyond IL-1 axis
- CANTOS trial (PMID: 28845751) showed canakinumab reduced cardiovascular events + incidental lung cancer — suggesting anti-inflammatory benefit extends to lung tissue

**This represents the single most actionable, genetically validated, and immediately testable novel therapeutic strategy for IPF.**

---

## 6. Summary of DPP9 Dual-Mechanism Model

```
IPF Risk Allele (rs12610495-G)
        ↓
    ↓ DPP9 expression
        ↓
    ┌───────────────────────┬──────────────────────────┐
    │  Mechanism A           │  Mechanism B              │
    │  (Immune cells)        │  (Fibroblasts)            │
    │                        │                           │
    │  NLRP1/CARD8           │  ↑ FAP-driven EMT         │
    │  inflammasome          │  ↑ ZEB1 stabilization     │
    │  activation            │  ↓ cell adhesion          │
    │     ↓                  │     ↓                     │
    │  IL-1β release         │  Myofibroblast            │
    │     ↓                  │  differentiation          │
    │  TGF-β activation      │                           │
    │     ↓                  │                           │
    │  Fibrosis              │  Fibrosis                 │
    └───────────────────────┴──────────────────────────┘

Therapeutic targets:
  A → Anti-IL-1β (anakinra/canakinumab) ← GENETICALLY ALIGNED
  B → Anti-FAP? ROCK inhibitors? ← needs development
```

---

*This analysis synthesizes data from 15+ publications spanning structural biology, Mendelian genetics, animal models, medicinal chemistry, and clinical trials to resolve the DPP9 therapeutic paradox for IPF.*
