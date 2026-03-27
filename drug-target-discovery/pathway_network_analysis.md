# Pathway-Level Network Analysis of IPF Drug Targets

*Session 5 (2026-03-26) — Clustering 25 targets by shared pathways to identify convergence points and pathway-level interventions*
*Updated with DPP9 KEAP1-NRF2 redox axis, MUC1-CT functional biology, NTN4 basement membrane mechanism, SPDL1 antagonistic pleiotropy*

---

## 1. Pathway Clusters

Analysis of all 21 ranked targets plus 3 new Chin 2025 loci reveals **six major pathway clusters** with significant overlap:

### Cluster 1: TGFβ / Smad / EMT Axis (7 targets)

The largest and most therapeutically actionable cluster. TGFβ signaling is the master driver of IPF fibrosis.

```
TGFβ1
├── ACVRL1 (ALK1, TGFβ type I receptor) ─── MR causal; sotatercept approved PAH
├── DSP (desmoplakin) ─── Cell-cell adhesion; EMT marker; TWAS #1
├── MUC1 (MUC1-CT) ─── TGFβ1→pSmad2/3→MUC1-CT→β-catenin nuclear complex
├── SMAD2 ─── UTMOST TWAS; canonical TGFβ effector
├── AKAP13 (RhoA-GEF) ─── TGFβ→RhoA→ROCK→EMT; confirmed 2025
├── FAM13A ─── RhoA pathway; upregulated in IPF (Wen 2025)
└── RIPK4 ─── MR OR=2.60; NF-κB but also TGFβ crosstalk
```

**Convergence point**: TGFβ receptor signaling → Smad2/3 activation
**Existing drugs at node**: Anti-TGFβ (fresolimumab, failed Phase 1 IPF); TRK-250 (TGFβ1 siRNA, Phase 1)
**Novel genetic angle**: ACVRL1 provides genetically-supported entry to TGFβ receptor modulation; MUC1-CT is downstream AND genetically validated

### Cluster 2: mTOR / Autophagy (3 targets + DPP9 connection)

Two independent GWAS loci converge on mTORC1 negative regulation:

```
mTORC1
├── DEPTOR ─── mTOR negative regulator; GWAS OR=0.82; TWAS p=8.58e-9
├── NPRL3 ─── GATOR1 complex (mTORC1 inhibitor); GWAS p=2.57e-12
├── DPP9 ─── Hepatocyte KO → autophagy (4/4 markers ↑); connects to mTOR
└── [Sirolimus] ─── mTORC1-selective inhibitor; fibrocyte suppression in pilot
```

**Convergence point**: mTORC1 hyperactivation → collagen synthesis + autophagy impairment
**Existing drugs at node**: Sirolimus (mTORC1 inhibitor); pilot IPF data (35% fibrocyte decline, PMID: 36853800)
**Key insight**: DEPTOR + NPRL3 = two independent genetic validators for mTOR pathway. DPP9 connects via autophagy.

### Cluster 3: Innate Immunity / Inflammasome (4 targets)

The DPP9-NLRP1-IL-1β axis sits at the center, with TOLLIP as an independent innate immunity node:

```
Inflammasome / Innate Immunity
├── DPP9 ─── NLRP1/CARD8 repressor; GWAS p=1.7e-12
│   ├── NLRP1 ─── Activated when DPP9 reduced
│   ├── IL-1β ─── Downstream effector; genetically aligned therapeutic target
│   └── [Anakinra/Canakinumab] ─── Approved anti-IL-1β
├── TOLLIP ─── TLR signaling inhibitor; GWAS p=3.8e-8; TWAS p=1.41e-15
├── ATP11A ─── TLR4 innate immune; coloc PP.H4=0.996 in smokers
└── IL7 ─── Adaptive → innate bridge; inhibits TGFβ via JAK1/STAT1/Smad7
```

**Convergence point**: IL-1β / innate immune activation → fibroblast activation
**Key link**: DPP9 loss → NLRP1 de-repression → IL-1β → fibrosis. TOLLIP independently modulates TLR signaling.
**NEW Session 5**: DPP9 also connects to oxidative stress via KEAP1-NRF2 axis (JBC 2024, PMID: 39615677). DPP9 unfolding → KEAP1 sequestration → NRF2 stabilization → antioxidant response. DPP9 loss = double hit: ↑inflammasome + ↓antioxidant defense. Rescued by single-allele IL-1R deletion (Sci Immunol 2021).
**Therapeutic strategy**: Anti-IL-1β (anakinra) addresses the DPP9 genetics; IL-7 (CYT107) counteracts fibroblast TGFβ response; NRF2 activators (dimethyl fumarate) address redox arm

### Cluster 4: Telomere Maintenance (3 targets)

IPF has the strongest telomere connection of any common disease:

```
Telomere Biology
├── TERT ─── Telomerase reverse transcriptase; GWAS p=2.2e-14
├── TERC (3q26.2) ─── Telomerase RNA component; GWAS p=8.9e-9
├── RTEL1 ─── Telomere helicase; GWAS OR=1.75
└── OBFC1/STN1 ─── CST complex; telomere replication
```

**Convergence point**: Telomere shortening → AT2 cell senescence → impaired re-epithelialization → fibrosis
**Existing drugs**: Imetelstat (TERT inhibitor — wrong direction); TA-65/danazol (mild TERT activation, weak)
**Challenge**: Telomerase activation needed but oncology risk; cross-ancestry validated (best generalizability)

### Cluster 5: Host Defense / Mucin (4 targets)

The largest IPF-specific pathway, centered on MUC5B:

```
Mucin / Host Defense
├── MUC5B ─── Strongest GWAS (OR=4.11); SPL5B ASO Phase 1 2026
├── MUC1 ─── NEW: rs9426886; TGFβ-MUC1-CT-β-catenin profibrotic; GO-203
├── FUT6 ─── Fucosyltransferase; mucin fucosylation; Lewis antigens
└── TOLLIP ─── Innate immunity at mucin locus (11p15.5, independent of MUC5B)
```

**Convergence point**: Mucociliary dysfunction → epithelial stress → ER stress → UPR → apoptosis/fibrosis
**MUC5B-MUC1 distinction**: MUC5B is secreted (extracellular mucus); MUC1 is transmembrane (intracellular signaling). Different biology, different therapeutic approaches.
**Key therapeutic**: SPL5B (inhaled ASO targeting MUC5B) + GO-203 (MUC1-CT peptide inhibitor) = dual mucin targeting

### Cluster 6: Spindle Assembly / Cell Division (4 targets)

Unexpectedly enriched pathway — cell division defects in a fibrotic disease:

```
Spindle / Mitosis
├── KIF15 ─── Kinesin motor; GWAS OR=1.58; decreased expression = risk
├── MAD1L1 ─── Spindle checkpoint; GWAS OR=1.28; decreased expression = risk
├── KNL1 ─── Kinetochore scaffold; GWAS p=7.41e-13
└── STMN3 ─── Stathmin 3; microtubule dynamics; GWAS p=1.09e-8
```

**Convergence point**: Mitotic stress → genomic instability → cellular senescence → fibrosis
**Hypothesis**: Fibroblast proliferative stress during wound healing leads to mitotic errors; cells with impaired spindle assembly senesce prematurely; SASP drives paracrine fibrosis
**NEW Session 5 — SPDL1 addition**: SPDL1 (Spindly; rare missense p.Arg20Gln, OR=2.87, combined p=2.2e-20) extends this cluster to 5 genes. SPDL1 shows **antagonistic pleiotropy**: IPF risk allele is cancer-PROTECTIVE (Koskela 2021 preprint). Proposed mechanism: SPDL1 gain-of-function → stricter SAC → more mitotic arrests → senescence → cancer protection + fibrosis. This is INDEPENDENT of telomere length, representing a novel non-telomeric senescence mechanism.
**Challenge**: All five targets require *activation* (decreased expression = risk); no small molecules; DepMap safety flag for KIF15

---

## 2. Vascular / Extracellular Matrix (Emerging Cluster)

New targets from Chin 2025 suggest an underappreciated vascular component:

```
Vascular / ECM
├── NTN4 ─── Endothelial basement membrane; anti-senescent; anti-inflammatory
├── ATP11A ─── Phospholipid flippase; TLR4 innate immune; membrane biology
├── ACVRL1 ─── Endothelial TGFβ receptor (ALK1); vascular remodeling
└── SLC6A6 ─── Mitochondrial taurine; multi-organ fibrosis
```

**Convergence point**: Alveolar capillary dysfunction → endothelial-mesenchymal transition (EndMT) → fibrosis
**Clinical relevance**: IPF patients with pulmonary hypertension (PH-IPF) have worse outcomes. Vascular targets may specifically benefit this subgroup.

---

## 3. Cross-Cluster Connections (Hub Genes)

Some targets participate in multiple clusters, making them particularly high-value:

| Gene | Clusters | Hub Score |
|---|---|---|
| **DPP9** | Inflammasome + mTOR/Autophagy + EMT (via FAP) | **3 clusters** |
| **MUC1** | Mucin/Host defense + TGFβ/EMT (via MUC1-CT) | **2 clusters** |
| **ACVRL1** | TGFβ + Vascular | **2 clusters** |
| **TOLLIP** | Innate immunity + Mucin/Host defense (11p15.5) | **2 clusters** |
| **IL7** | Innate immunity + TGFβ (anti-fibrotic via Smad7) | **2 clusters** |
| **ATP11A** | Innate immunity + Vascular | **2 clusters** |

**DPP9 emerges as the highest-connectivity hub**: participating in inflammasome signaling, mTOR/autophagy regulation, and EMT via the FAP-DPP9 axis. This multi-pathway engagement explains its strong GWAS signal and makes its downstream target (IL-1β) particularly attractive.

---

## 4. Pathway-Level Therapeutic Opportunities

### 4.1 Immediate (Approved drugs, genetically supported)

| Pathway | Intervention | Genetic Support | Readiness |
|---|---|---|---|
| Inflammasome/IL-1β | Anakinra (anti-IL-1Ra) | DPP9 GWAS + coloc | Phase 2-ready |
| IL-7/anti-TGFβ | CYT107 (recombinant IL-7) | MR OR=0.67 + coloc PP=0.84 | Phase 2-ready |
| mTOR | Sirolimus (mTORC1 inhibitor) | DEPTOR + NPRL3 GWAS | Pilot data exists |
| TGFβ receptor | Sotatercept (ALK1-Fc; repurpose from PAH) | ACVRL1 MR | Approved drug, new indication |

### 4.2 Near-term (Clinical-stage compounds, some genetic support)

| Pathway | Intervention | Genetic Support | Status |
|---|---|---|---|
| MUC5B | SPL5B (inhaled ASO) | MUC5B GWAS OR=4.11 | Phase 1 (mid-2026) |
| MUC1-CT | GO-203 (peptide inhibitor) | MUC1 GWAS + functional | Phase I (cancer) |
| ROCK (via AKAP13) | Fasudil/Ripasudil (repurpose) | AKAP13 GWAS | Approved (other indications) |
| FKBP51 | SAFit2 / next-gen | FKBP5 GWAS | Preclinical (expanding) |

### 4.3 Longer-term (Novel pathway nodes)

| Pathway | Target | Approach | Timeline |
|---|---|---|---|
| Vascular/BM | NTN4 | Recombinant protein or gene therapy | 5+ years |
| Mitochondrial | SLC6A6 | Novel compounds | 5+ years |
| FAP-DPP9 | FAP | Small molecule or CAR-T (cardiac fibrosis data) | 3-5 years |
| Telomere | TERT | Activation strategy (small molecule/gene therapy) | 5+ years |

---

## 5. Pathway Convergence Diagram (Text Representation)

```
                          IPF FIBROSIS
                              ↑
           ┌─────────────────┼─────────────────┐
           ↑                 ↑                  ↑
    FIBROBLAST          EPITHELIAL          ENDOTHELIAL
    ACTIVATION          INJURY/SENESCENCE    DYSFUNCTION
           ↑                 ↑                  ↑
    ┌──────┴──────┐   ┌──────┴──────┐   ┌──────┴──────┐
    │ TGFβ/Smad   │   │ Telomere    │   │ Vascular    │
    │ ACVRL1      │   │ TERT        │   │ NTN4        │
    │ DSP         │   │ TERC        │   │ ATP11A      │
    │ MUC1-CT     │   │ RTEL1       │   │ ACVRL1      │
    │ AKAP13/RhoA │   │ OBFC1       │   │ SLC6A6      │
    │ RIPK4/NF-κB │   │             │   │             │
    │ FAM13A      │   │ Mucin/UPR   │   │             │
    └──────┬──────┘   │ MUC5B       │   └──────┬──────┘
           │          │ MUC1        │          │
    ┌──────┴──────┐   │ FUT6        │   ┌──────┴──────┐
    │ Inflamm.    │   │ TOLLIP      │   │ Spindle     │
    │ DPP9→NLRP1  │   └──────┬──────┘   │ KIF15       │
    │ →IL-1β      │          │          │ MAD1L1      │
    │ TOLLIP/TLR  │   ┌──────┴──────┐   │ KNL1        │
    │ IL7/JAK1    │   │ mTOR/Auto   │   │ STMN3       │
    └─────────────┘   │ DEPTOR      │   └─────────────┘
                      │ NPRL3       │
                      │ (DPP9→auto) │
                      └─────────────┘
```

---

## 6. Key Insights

### 6.1 DPP9 is the Network Hub
DPP9 connects three pathway clusters (inflammasome, mTOR/autophagy, EMT via FAP). This multi-pathway engagement likely explains its relatively strong GWAS signal and suggests that therapeutic strategies targeting DPP9's downstream effects (anti-IL-1β) would address one of the most interconnected nodes in the IPF genetic architecture.

### 6.2 TGFβ is the Most Targeted Pathway — But Genetically Weakest
Seven targets connect to TGFβ signaling, but most (DSP, AKAP13, FAM13A) are downstream/peripheral. The strongest genetic entry is ACVRL1 (MR causal) and MUC1 (GWAS + functional). Direct anti-TGFβ has failed in IPF (fresolimumab), likely due to pleiotropic effects. **Genetically-informed pathway modulation** (e.g., ACVRL1-selective, MUC1-CT-targeted) may succeed where broad TGFβ blockade failed.

### 6.3 Mucin Cluster is IPF-Specific
The MUC5B/MUC1/FUT6/TOLLIP cluster is essentially unique to pulmonary fibrosis. It's not enriched in other fibrotic diseases. SPL5B (MUC5B ASO) represents the first genetically-targeted IPF therapy.

### 6.4 Spindle Cluster is Genuinely Surprising
Four GWAS loci pointing to cell division biology in a non-neoplastic disease. The most likely explanation is **mitotic stress → senescence → SASP → paracrine fibrosis**. This parallels the telomere cluster (telomere attrition → replicative senescence). Both converge on cellular senescence as a disease driver.

### 6.5 Vascular Cluster is Emerging
NTN4 and SLC6A6 (both Chin 2025) plus ATP11A and ACVRL1 suggest IPF has a stronger vascular component than appreciated. This aligns with the clinical observation that PH-IPF patients do poorly and that treprostinil (prostacyclin) showed the largest FVC benefit (95.6 mL) of any IPF trial.

---

---

## 7. Session 5 Deep-Dive Updates (2026-03-26)

### 7.1 DPP9 Ternary Complex Structural Biology

Cryo-EM structures (3.6Å) reveal the DPP9-NLRP1 inhibitory mechanism:
- **2:1 stoichiometry**: One autoinhibited NLRP1 + one active UPA-CARD fragment, both bound to a single DPP9 dimer (Huang et al. Nature 2021, PMID: 33731929; PDB 7CRW)
- **Both catalytic activity and physical scaffolding** required for NLRP1 suppression (Hollingsworth et al. Nature 2021, PMID: 33731932; PDB 6X6A/6X6C)
- Val-boroPro (VbP) displaces the NLRP1 C-terminus from DPP9's active site → releases UPA-CARD → ASC oligomerization → caspase-1 → pyroptosis
- **CARD8 threshold mechanism**: DPP9 also suppresses CARD8 inflammasome (Sharif et al. Immunity 2021, PMID: 34019797); for CARD8, enzymatic activity (not binding) is primary

**Key in vivo evidence**: Dpp9 S759A/S759A (catalytically dead) mice die within 24h. Rescue by single-allele deletion of Nlrp1, Asc, Gsdmd, or Il-1r (Harapas et al. Sci Immunol 2022, PMID: 36112693). This **steep threshold** means even partial downstream blockade (e.g., heterozygous IL-1R) can rescue.

### 7.2 DPP9 Non-Inflammasome Functions in Fibrosis

**Renal fibrosis** (directly relevant):
- DPP8/9 are **upregulated in CKD proximal tubule cells**; inhibitor TC-E5007 attenuates EMT + ECM in UUO model (Tang et al. Pharmacol Res 2021, PMID: 33932609)
- DPP8/9 inhibition reduces TGF-β1-induced collagen III/IV/fibronectin/MMP2 in glomerular mesangial cells (Jiang et al. Toxicol Lett 2024, PMID: 38458339)
- DPP8/9 promote ferroptosis in AKI; TC-E5007 protects (Eur J Med Res 2025)

**Critical context problem**: In kidney, DPP8/9 are **upregulated** in fibrotic tissue and inhibition is antifibrotic. In IPF, DPP9 expression is **decreased** by the risk allele. Whether DPP9 protein is upregulated in IPF fibroblasts/myofibroblasts (as suggested by scRNA showing DPP9 INCREASED in myofibroblasts) has not been directly measured.

### 7.3 DPP9-KEAP1-NRF2 Redox Connection

New finding: DPP9 and KEAP1 form a **mutually inhibitory complex** (Tsamouri et al. JBC 2025, PMID: 39615677):
- Non-dimeric DPP9 binds KEAP1 KELCH domain via C844
- Links DPP9 to intracellular redox sensing alongside thioredoxin-1
- DPP9 loss → reduced KEAP1 sequestration → more NRF2 degradation → impaired antioxidant defense
- Creates a **double-hit** in IPF: ↑inflammasome activation + ↓antioxidant capacity

### 7.4 Pinocembrin: First DPP9 Activator

Wang et al. (Immunol Res 2025) demonstrated pinocembrin upregulates DPP9 expression → suppresses NLRP1 inflammasome → protects against cerebral I/R-induced lung injury. DPP9 knockdown reversed protection. This is the **only published DPP9 activator** — proof-of-concept for the genetically-correct therapeutic direction.

### 7.5 Lung-Specific DPP9 Isoform

bioRxiv (July 2025): A lung-epithelium-specific DPP9 isoform (DPP9-AFE) with alternative first exon. The GWAS variant causes **p.Leu8Pro** missense in this isoform, predicted to disrupt α-helix. Both WT and mutant retain NLRP1 interaction, but the coding variant in a tissue-specific isoform may explain lung-specific disease.

### 7.6 MUC1 Comprehensive Biological Validation

MUC1 was promoted to Tier 1 based on:
1. **GWAS**: rs9426886, OR=1.162, p=1.53e-9 (Chin 2025, PMID: 39974050)
2. **Cell-type sc-eQTL**: MUC1 eQTL colocalizes in AT2, transitional AT2, and AT1 cells across 3 independent GWAS (Natri 2024, PMID: 38548990)
3. **Functional**: MUC1-CT bioactivation drives EMT/FMT via TGFβ1/pSMAD3/β-catenin nuclear complex (Milara 2020, PMID: 31801904)
4. **KO protection**: MUC1-knockout mice protected from bleomycin fibrosis
5. **Pharmacological**: GO-201 inhibits MUC1-CT nuclear translocation; reduces bleomycin fibrosis in vivo
6. **Drug mechanism**: Pirfenidone partially works through MUC1-CT inhibition (Ballester 2020, PMID: 32341751)
7. **Novel pathway**: ADAM17/MUC1-CT/EZH2 axis identified 2025 (Biochem Pharmacol)
8. **Biomarker**: KL-6 AUC=0.96 diagnostic; HR=2.05 mortality; enables theranostic strategy

**Dual role caveat**: MUC1 extracellular domain is anti-inflammatory (MUC1-KO worsens silicosis fibrosis, PMID: 28916165). Therapeutic approach must target **activated MUC1-CT** specifically.

### 7.7 NTN4: Novel Target at Intersection of Vascular Biology and Senescence

Key NTN4 biology for IPF:
- Highest tissue expression in lung (enrichment 26.6, GeneCards)
- Highly expressed in **aberrant basaloid cells** — IPF-specific population (Adams et al. Sci Adv 2020, PMID: 32832599)
- **Anti-senescence**: NTN4 knockdown increases CDKN1A (p21), CDKN2A (p16), SA-βgal in endothelial cells; rescued by exogenous NTN4 (PMID: 33636396)
- **Anti-inflammatory**: NTN4 silencing increases VCAM-1, ICAM-1, monocyte adhesion
- **Basement membrane**: Disrupts laminin networks non-enzymatically via laminin-γ1 binding (NatComm 2016, PMID: 27901020)
- **Receptor controversy**: Binds neogenin (not DCC/UNC5B directly; PMID: 18719102) vs. primary laminin interaction (crystal structure argues against classical netrin receptors; PMID: 27901020)
- **Family context**: NTN1 is profibrotic from macrophages but protective from epithelium (JCI 2021, PMID: 33393489; ATS 2025). Alpha-1 blocker terazosin improved IPF patient survival (observational; PMID: 36648147).

### 7.8 Cross-Ancestry Allele Frequency Table

| Gene | Lead SNP | Risk allele | EUR | EAS | AFR | SAS | AMR | Implication |
|---|---|---|---|---|---|---|---|---|
| MUC5B | rs35705950 | T | 10.7% | 0.8% | 0.3% | 8.3% | 5.6% | EUR-enriched; 50-fold EUR/AFR differential |
| TERT | rs2736100 | A | 49.5% | 58.0% | 53.4% | 39.4% | 59.7% | Universally common; best portability |
| DSP | rs2076295 | G | 41.4% | 47.1% | 51.2% | 31.3% | 42.1% | Common everywhere; good portability |
| DPP9 | rs12610495 | G | 29.9% | 15.4% | 12.8% | 18.2% | 20.9% | Present globally; lower in non-EUR |
| AKAP13 | rs62025270 | A | 22.1% | 0.2% | 11.7% | 16.0% | 12.0% | Essentially monomorphic in EAS |
| FKBP5 | rs9380529 | A | 52.3% | 32.3% | 11.9% | 57.4% | 36.8% | Very low in AFR |
| GPR157 | rs7549256 | C | 33.6% | 47.8% | 25.3% | 36.2% | 35.4% | EAS-enriched (highest MAF) |
| PSKH1 | rs539683219 | del | 0.0% | 2.2% | 0.0% | 0.0% | -- | EAS-exclusive |
| FAM13A | rs2609255 | G | 23.6% | 45.2% | 29.8% | 45.9% | 25.8% | Higher in EAS/SAS than EUR |

**All of Us 2025 (AJRCCM, PMC12410450)**: MUC5B rs35705950 effect size is conserved across ancestries (OR ~3.2 EUR and non-EUR). Non-telomere IPF-PRS shows portable effect sizes (OR 1.35 non-EUR vs 1.29 EUR), suggesting non-telomere pathways are better global drug targets.

**Key GBMI finding** (PMID: 36777997): 4/7 novel loci were driven by non-EUR ancestry. Case ascertainment explains 55.8% of heterogeneity; ancestry only 6.2%.

---

*Analysis integrates genetic data from 8 GWAS, 4 TWAS studies, coloc results, MR analyses, and published pathway databases (Reactome, KEGG, GO, STRING, BioGRID). All genes are HGNC symbols; all SNPs are real rsIDs. Updated Session 5 (2026-03-26).*
