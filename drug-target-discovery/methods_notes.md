# Methods Notes — IPF Causal Drug Target Discovery Pipeline

## Pipeline Overview

This document tracks all methods, data sources, parameters, and software versions used in the IPF causal drug target discovery pipeline.

---

## Session 1 — GWAS Locus Curation & Pipeline Foundation

### Disease Selection

- **Disease:** Idiopathic Pulmonary Fibrosis (IPF)
- **ICD-10:** J84.112
- **Selection criteria:** Large GWAS data available, few approved drugs (pirfenidone, nintedanib, nerandomilast), clear tissue relevance (lung), strong genetic architecture

### GWAS Data Sources

All GWAS loci were curated from published peer-reviewed studies. No summary statistics were downloaded or re-analyzed; instead, lead SNP information was extracted from published tables and supplementary materials.

| Study | Journal | Year | PMID | Cases | Controls | Novel Loci | Total Loci |

|-------|---------|------|------|-------|----------|------------|------------|

| Seibold et al. | NEJM | 2011 | 21460842 | 83 families | — | 1 (MUC5B) | 1 |

| Fingerlin et al. | Nat Genet | 2013 | 23583980 | 1,616 | 4,683 | 7 | 10 |

| Noth et al. | JAMA | 2013 | 24429156 | 1,410 | 2,934 | 1 (TOLLIP) | — |

| Allen et al. | Lancet Respir Med | 2017 | 29066090 | 2,760 | 8,561 | 1 (AKAP13) | — |

| Allen et al. | AJRCCM | 2020 | 31710517 | 2,668 | 8,591 | 3 | 14 |

| Allen et al. | Thorax | 2022 | 35688625 | 4,125 | 20,464 | 5 (robust) | 23 |

| Partanen et al. | Cell Genomics | 2022 | 36777997 | 11,160 | 1,364,410 | 7 | 25 |

| Chin et al. | medRxiv (preprint) | 2025 | 39974050 | 5,159 | 27,459 | 3 (MUC1, SLC6A6, NTN4) | 37 |

### Genome Build

- **Reference assembly:** GRCh38.p14 (hg38) — primary coordinate system
- **All positions verified via:** NCBI dbSNP Build 157 (September 2024)
- **Note:** Some source studies reported GRCh37; positions in gwas_loci.csv have been standardized to GRCh38 per dbSNP

### Statistical Thresholds

| Analysis | Threshold | Justification |

|---|---|---|

| GWAS significance | p < 5 × 10⁻⁸ | Standard genome-wide significance |

| TWAS significance | Bonferroni-corrected (p < 3.35 × 10⁻⁶ for ~15K genes) | Accounts for multiple testing |

| Colocalization | PP.H4 > 0.8 (coloc) or CLPP > 0.5 (eCAVIAR) | Conservative for causal inference |

| MR significance | FDR < 0.05 | Multiple testing correction for genome-wide MR |

| MR pleiotropy | HEIDI p > 0.05 or MR-Egger intercept p > 0.05 | Rules out horizontal pleiotropy |

### Locus Curation Procedure

1. Identified all published IPF GWAS from PubMed/GWAS Catalog
2. Extracted lead (sentinel) SNP rsIDs from published tables
3. Verified each rsID in dbSNP to confirm GRCh38 position and alleles
4. Recorded effect allele, other allele, OR/beta, and p-value from the discovery publication
5. Annotated nearest gene (HGNC symbol), cytogenetic band, and biological pathway
6. Flagged which study first reported each locus at genome-wide significance

### Effect Size Notes

- Effect sizes (OR) reported from the largest available meta-analysis where the locus reached GWS
- MUC5B rs35705950: OR = 4.11 from Allen et al. 2017 (PMID: 29066090)
- Most common variant ORs range 1.08–1.49, typical for GWAS
- Exceptions: rs539683219 (PSKH1) OR = 3.20 (EAS-specific rare indel); rs41308092 (RTEL1) OR = 1.75 (low-frequency variant)

### Ancestry

- Most loci identified in European ancestry populations
- Partanen et al. 2022 was first multi-ancestry IPF GWAS (6 ancestries)
- rs539683219 (PSKH1) is EAS-specific (MAF ~2% in EAS, essentially absent in EUR)

---

## Session 1 — TWAS Evidence

### Data Sources

- **Primary**: Gao et al. 2020, Frontiers in Genetics (PMID: 33362862)
    - Method: FUSION (Gusev et al. 2016, PMID: 26854917)
- Expression weights: GTEx lung tissue and whole blood
    - GWAS input: Allen et al. 2020 (2,668 cases / 8,591 controls)
- Genes tested: 14,929
    - Bonferroni threshold: p < 3.35 × 10⁻⁶
- Result: 29 Bonferroni-significant genes

- **Alternative**: Li et al. 2025, J Translational Medicine (PMID: 40091050)
    - Method: OTTERS framework
- Expression weights: Plasma eQTL data
    - GWAS input: GBMI IPF + FinnGen replication
- Result: 6 essential genes (BRCA1, EZH1, FAM13A, SFR1, ANO9, CCDC200)

### Key TWAS Findings

- Top lung tissue hits: DSP (p=1.35e-29), MUC5B (p=1.09e-28), MAPT (p=9.60e-15), DEPTOR (p=8.58e-9)
- Top blood hit: TOLLIP (p=1.41e-15)
- Note: Some known IPF genes (e.g., TERT) not significant in TWAS — likely due to tissue-specific regulatory mechanisms not captured by lung bulk expression models

---

## Session 1 — Colocalization Evidence

### Data Sources

- **Primary**: Borie et al. 2022, AJRCCM (PMID: 35816432)
    - Method: eCAVIAR
- Tissue: Whole lung homogenate (234 IPF + 188 control)
    - Both eQTL and mQTL colocalization performed
- 10 IPF loci tested
    - Strong colocalization for MUC5B (CLPP=1.00 controls, 0.96 cases) and DSP (CLPP=1.00 controls, 0.66 cases)

- **GTEx-based**: Context-specific eQTL study
    - Method: coloc (Bayesian)
- MUC5B PP.H4 = 1.00 in GTEx lung
    - DPP9 colocalized in IPF cases

- **Single-cell**: Natri et al. 2024, Nature Genetics
    - 66 PF + 48 control donors; 38 cell types
- Cell-type-specific colocalization for MUC5B (epithelial), DSP (epithelial), KANSL1

### Colocalization Thresholds

- eCAVIAR: CLPP > 0.5 considered evidence of colocalization
- coloc: PP.H4 > 0.8 standard; > 0.6 used in single-cell context (lower power)

---

## Session 1 — Mendelian Randomization Evidence

### Data Sources

- **Liu et al. 2024**, Respiratory Research (PMID: 38783236)
    - Method: SMR + HEIDI, IVW, MR-Egger, weighted median
- Exposure: cis-eQTLs of druggable genes from eQTLGen Consortium
    - Outcome: IPF GWAS (International IPF Genetics Consortium)
- Result: 45 druggable genes at FDR < 0.05; IL-7 and ABCA2 colocalized (PP.H4 > 0.80)

- **Zhang et al. 2024**, Respiratory Research (PMID: 39425105)
    - Method: SMR with HEIDI
- Exposure: Plasma gene expression, DNA methylation, protein levels (pQTL)
    - Result: BTRC, RIPK4, LINC01252 significant; MUC5B/DSP validated

- **TGF-β MR study 2026**, Biochemical Genetics
    - SMR confirmed ACVRL1 causal link to IPF via eQTLGen + GTEx

### Instrument Selection

- cis-eQTLs within 1Mb (or 500kb) of gene TSS
- p < 5 × 10⁻⁸ for instrument strength
- LD clumping: r² < 0.001, window 10Mb

---

## Session 1 — Druggability and Clinical Assessment

### Druggability Sources

- ChEMBL (https://www.ebi.ac.uk/chembl/)
- Open Targets Platform (https://platform.opentargets.org/) — tractability assessments
- DGIdb (https://www.dgidb.org/)
- Finan et al. 2017 (PMID: 28356508) — druggable genome classification

### Druggability Tier System

| Tier | Definition |

|---|---|

| Tier 1 | Approved drug exists for any indication (repurposing possible) |

| Tier 2 | Clinical-stage compounds exist |

| Tier 3 | Tool compounds / preclinical ligands only |

| Tier 4 | No known small-molecule ligands |

### Safety Assessment

- **DepMap** (Cancer Dependency Map, Broad Institute): https://depmap.org/portal/
    - CRISPR (Chronos) gene effect scores
- Gene effect < -0.5 = likely essential in that cell line
    - Pan-essential genes flagged for safety
- TERT flagged as essential in many cancer lines

### Clinical Trial Sources

- ClinicalTrials.gov (https://clinicaltrials.gov/)
- Open Targets Platform
- Published trial results: FIBRONEER-IPF (NCT05321069), TETON-2, GENESIS-IPF
- Pulmonary Fibrosis Foundation updates

---

## Session 4 — Evidence Deepening & Cross-Validation

### New Data Sources Added

| Source | Type | Key Findings | Reference |

|---|---|---|---|

| Chin et al. 2025 GWAS | GWAS | 3 novel loci (MUC1, NTN4, SLC6A6); 5,159 clinically-diagnosed cases | medRxiv 2025 |

| Kousathanas et al. 2025 | GWAS (WGS) | Novel locus MCL1; rare variant ANGPTL7 (OR=28.8); shared IPF-COVID loci | eBioMedicine (Lancet) |

| FIBRONEER-IPF/ILD | Phase 3 results | Nerandomilast 68.8 mL FVC benefit; approved Oct 2025 | NEJM, PMID: 40387033 |

| TETON-2 | Phase 3 results | Inhaled treprostinil 95.6 mL FVC benefit | NEJM March 2026 |

| BEACON-IPF | Phase 2b/3 | Bexotegrast DISCONTINUED — safety signal | Pliant June 2025 |

| DPP9 selective inhibitors | Medicinal chemistry | Cpd 42 (175x DPP9/DPP8 selectivity); Cpd 6e (oral, nanomolar) | J Med Chem 2023, 2025 |

| IL-7 antifibrotic | Preclinical | IL-7 inhibits TGF-β via JAK1/STAT1/Smad7; reduces bleomycin fibrosis | PMC150933 |

| CYT107 COVID trial | Phase 2 RCT | Safe in 109 critically ill patients; no cytokine storm | JCI Insight 2025 |

| Sirolimus IPF pilot | Phase 2 crossover | Tolerated; suppressed circulating fibrocytes | JCI Insight 2023 |

| GPR157 biology | Basic science | Orphan GPCR; Gq-IP3-Ca2+ signaling; CSF-derived ligand | Sci Rep 2016, PMID: 27142930 |

| ATP11A scRNA | Single-cell | Upregulated in macrophages + myofibroblasts in IPF | HGG Advances 2025 |

| ACVRL1 MR | Causal inference | Confirmed causal link to IPF; ACVRL1+ EC altered communication | Biochem Genet 2026 |

| SAFit2 MS model | Pharmacology | FKBP51 inhibitor reduces neuroinflammation in EAE | J Neuroinflammation 2025 |

| Partanen 2022 multi-ancestry | Population genetics | 6/7 novel loci would be missed in EUR-only analysis | Cell Genomics, PMID: 36777997 |

| GLIS3 CRISPR screen | Functional genomics | Master fibrotic TF; bidirectional CRISPR screens in fibroblasts | Nature 2026 |

### Open Targets Platform Tractability Assessment

Queried via GraphQL API (api.platform.opentargets.org/api/v4/graphql) for all 15 key targets (March 2026 data). Four modalities assessed: Small Molecule (SM), Antibody (AB), PROTAC (PR), Other Clinical (OC).

**Tractability bucket system** (Open Targets Pipeline v2):

- SM: Approved > Advanced Clinical > Phase 1 > Structure+Ligand > HQ Ligand > HQ Pocket (DrugEBIlity≥0.7) > Med Pocket > Druggable Family
- AB: Approved > Advanced Clinical > Phase 1 > UniProt high conf > GO CC high conf > UniProt med conf > SigP/TMHMM > GO CC med conf > HPA loc
- PR: Approved > Advanced Clinical > Phase 1 > Literature > UniProt Ubiq > DB Ubiq > Half-life > SM Binder
- OC: Approved > Advanced Clinical > Phase 1

Key findings (total positive buckets across all modalities):

| Gene | SM | AB | PR | OC | Total | Notable |

|---|---|---|---|---|---|---|

| ACVRL1 | 5 | 4 | 1 | 0 | **10** | Most tractable; Advanced Clinical SM+AB (sotatercept) |

| FKBP5 | 3 | 0 | 4 | 0 | **7** | SM (SAFit2) + exceptional PROTAC potential (4 buckets) |

| RIPK4 | 2 | 2 | 3 | 0 | **7** | Kinase family; SM + strong PROTAC |

| DPP9 | 3 | 0 | 3 | 0 | **6** | SM (Structure+Ligand, HQ Ligand, Druggable Family) |

| TERT | 2 | 1 | 2 | 1 | **6** | Only gene with OC bucket (imetelstat, Advanced Clinical) |

| DSP | 2 | 2 | 2 | 0 | **6** | HQ druggable pocket (DrugEBIlity≥0.7) |

| DEPTOR | 1 | 1 | 3 | 0 | **5** | PROTAC-amenable (3 buckets) |

| ATP11A | 0 | 3 | 2 | 0 | **5** | AB only (membrane localization) |

| GPR157 | 0 | 3 | 0 | 0 | **3** | Pharos Tdark; no SM despite GPCR family |

| IL7 | 0 | 3 | 0 | 0 | **3** | Secreted cytokine; AB/recombinant only |

| MUC5B | 0 | 3 | 0 | 0 | **3** | Secreted mucin; AB/ASO modalities |

| NPRL3 | 1 | 0 | 1 | 0 | **2** | Minimal tractability |

| TOLLIP | 0 | 0 | 0 | 0 | **0** | No tractability across any modality |

| FAM13A | 0 | 0 | 0 | 0 | **0** | No tractability |

### DepMap Essentiality Assessment (25Q3 Release)

Chronos CRISPR gene effect scores obtained from DepMap Public 25Q3+Score, Chronos_Combined dataset via the DepMap Portal API (https://depmap.org/portal/api/). 1,186 cancer cell lines across 30+ lineages.

- **Data source**: DepMap Public 25Q3, Broad Institute (https://depmap.org/portal/)
- **Algorithm**: Chronos (Dempster et al. 2021, Genome Biology, PMC8686573)
- **API endpoints used**: GET /download/gene*dep*summary (classifications); POST /download/custom with datasetId=Chronos_Combined (raw scores)
- **Score interpretation**: 0 = no effect; -1 = median pan-essential gene effect
- **Dependency threshold**: Chronos < -0.5 (likely essential in that cell line)
- **Common essential definition**: Listed in CRISPRInferredCommonEssentials.csv (ADaM method, >50% dep across diverse lineages)
- **Strongly selective**: Identified by DepMap algorithm as essential in specific contexts

Key findings (all 21 pipeline targets scored):

| Safety Class | Genes | Chronos Range | % Dep Lines |

|---|---|---|---|

| COMMON ESSENTIAL | RTEL1 | -0.571 | 68.7% |

| Strongly Selective | TERT, KIF15, MAD1L1, BTRC, AKAP13 | -0.054 to -0.151 | 0.8–8.4% |

| Safe (low dependency) | DPP9, DSP, DEPTOR, ACVRL1, FAM13A, MUC5B, RIPK4, FUT6, GPR157, ATP11A | -0.052 to +0.027 | 0.0–0.6% |

| Very Safe (positive Chronos) | IL7, TOLLIP, FKBP5, PSKH1 | +0.076 to +0.155 | 0.0% |

| Limited data | NPRL3 | NA (0/45 in tested subset) | 0.0% |

**Critical corrections from real data:**

- RTEL1: Identified as common essential (68.7% dependent) — added to ranking at #21 with safety flag
- TERT: Reclassified from "common essential" to "strongly selective" (only 1.7% dependent lines); less risky than published literature review suggested

### Cross-Ancestry Generalizability Assessment

Based on Partanen et al. 2022 (GBMI), Mushiroda et al. 2008, Peljto et al. 2015, All of Us cohort 2025:

| Generalizability | Targets |

|---|---|

| HIGH (EUR + EAS + AMR) | TERT |

| MODERATE (EUR validated, some cross-ancestry data) | MUC5B, DPP9, FAM13A, KIF15 |

| LOW (ancestry-enriched) | GPR157 (EAS), FUT6 (AMR), RAPGEF2 (AFR) |

| VERY LOW (ancestry-specific) | PSKH1 (EAS-only) |

| UNKNOWN (EUR-only, no cross-ancestry data) | DSP, IL7, DEPTOR, TOLLIP, AKAP13, FKBP5, NPRL3, RIPK4, BTRC, ACVRL1, ATP11A, MAD1L1 |

---

## Session 5 (2026-03-26) — DPP9 Therapeutic Paradox and NTN4 Mechanism Resolution

### DPP9-NLRP1-IL-1β Mechanistic Pathway

**Literature sources (web search 2026-03-26):**
- Shao et al. Nature 2021 (PMID:33731929): DPP9 sequesters NLRP1 C-terminus to repress inflammasome
- Zhong et al. Science Immunology 2021 (PMID:34671425): DPP9 deficiency rescuable by IL-1 pathway lowering
- Lupardus et al. Nature 2021 (PMID:33731932): DPP9-CARD8 structural basis
- Staniforth et al. PLOS Pathogens 2024 (PMID:39368365): DPP9-NLRP1 in viral infection
- Spandidos/Nature Reviews 2025: DPP9 enzymatic and scaffolding functions in inflammation

**Mechanistic chain:**
1. DPP9 genetic risk allele (rs12610495, GWAS p=1.7e-12) reduces DPP9 expression
2. Low DPP9 → impaired NLRP1 repression (both enzymatic + scaffolding mechanisms impaired)
3. NLRP1 inflammasome activation → caspase-1 cleavage of pro-IL-1β
4. IL-1β release → TGF-β pathway priming + fibroblast myofibroblast differentiation
5. Sustained myofibroblast activation → progressive fibrosis

**Dual therapeutic implications:**
- **Direct targeting impossible**: DPP9 activation is pharmacologically unfeasible (serine protease activation rare in drug development)
- **Downstream targeting possible**: IL-1β inhibitors (anakinra, canakinumab, rilonacept) genetically aligned
- **Previously overlooked**: Despite IL-1 inhibitors being approved and safe agents (>10,000 patients dosed globally in autoimmune/autoinflammatory diseases), none tested in IPF

**NLRP3 vs NLRP1 distinction:**
- NLRP3 inflammasome also produces IL-1β in IPF pathogenesis (reviews 2024-2025)
- DPP9 specifically represses NLRP1 + CARD8 (structurally related)
- Both converge on IL-1β as final effector
- IL-1β inhibition would address both pathways simultaneously

**Clinical-grade IL-1 inhibitor options:**
| Agent | Mechanism | Route | Frequency | Indication (Approved) |
|---|---|---|---|---|
| Anakinra | IL-1R antagonist | SC | Daily | RA, SJIA, PSTPIP1-AD |
| Canakinumab | Anti-IL-1β mAb | SC | q8 weeks | Autoinflammatory syndromes |
| Rilonacept | IL-1 trap | SC/IV | Varies | Periodic fever |

**Trial design recommendations:**
- Enrich for high baseline IL-1β (BAL or plasma cytokine panel)
- Power calculation: assuming 30-40% of IPF patients have IL-1β-driven phenotype
- Biomarker endpoints: IL-1β, IL-18, pro-caspase-1, inflammasome-derived DNA
- Functional endpoints: FVC decline, patient-reported outcomes
- Safety monitoring: infection rates (expected increased due to IL-1 block); tuberculin status check

### NTN4 (Netrin-4) Paradox and Unresolved Mechanisms

**Literature sources (web search 2026-03-26):**
- Wang et al. International Journal of Molecular Medicine 2024: NTN4 promotes VE-cadherin in endothelial cells via NF-κB
- Xiang et al. ScienceDirect 2022: NTN4 anti-inflammatory and anti-senescence in endothelium
- Gu et al. MDPI 2024: NTN4 pro-inflammatory in synovial fibroblasts (OA context)
- Chin et al. medRxiv 2025 (PMID:39974050): NTN4 rs7957346 identified as IPF GWAS locus, coloc PP=0.649 in lung

**The Paradox:**
- GWAS direction: rs7957346 risk allele increases NTN4 expression (loss of protective allele)
- Endothelial biology consensus: Higher NTN4 → stronger VE-cadherin → lower permeability → anti-inflammatory
- Prediction: Increased NTN4 should be PROTECTIVE, not harmful
- Contradiction: GWAS says increased NTN4 = IPF risk

**Possible resolutions (pending functional studies):**
1. **IPF-specific NTN4 mechanism differs from endothelial paradigm**: In fibroblast-endothelial crosstalk during chronic inflammation + fibrosis, high NTN4 may promote pathological remodeling (requires single-cell RNA-seq validation)
2. **Fine-mapping issue**: rs7957346 may not be causal; linked variant in different gene; requires dense mapping
3. **Cell-type specificity**: NTN4 expressed by different cell types has different effects (endothelium vs epithelium vs fibroblast); single-cell studies needed
4. **NTN4 promotes excessive angiogenesis in IPF context**: Abnormal angiogenesis drives fibrotic niche; increased NTN4 might paradoxically promote this (requires IPF tissue studies)

**Status for ranking:**
- Rank 21 (Tier 2 Moderate, Direction = Unknown) is appropriate until paradox resolved
- Flag mechanistic uncertainty prominently in evidence summary
- Recommend: Low-priority target pending functional validation
- Next steps: Obtain IPF single-cell RNA-seq (IPF Cell Atlas, GLF cohort) to quantify NTN4 expression by cell type; search for NTN4 biology in lung fibroblasts specifically

---

### Session 5 Addendum — New Literature Sources and Analytical Methods

#### DPP9 Selective Inhibitor Chemistry (Updated)
- **Filippi et al. 2025**, J Med Chem 68(21):23163-23184 (DOI: 10.1021/acs.jmedchem.5c02049): Compound 6e — orally bioavailable, selective DPP9 inhibitor with potent pyroptosis induction. High oral bioavailability in rats; long in vivo and microsomal half-life. University of Antwerp.
- **Nguyen et al. 2025**, Cell Mol Life Sci 82:187 (PMC12037458): Comprehensive review of DPP9 biology and inhibitor development. Notes: 170x selectivity achieved; DPP9 KO neonatally lethal; no fully selective inhibitor in vivo yet.
- **Zhang et al. 2026**, Cell Death Differ (DOI: 10.1038/s41418-026-01704-x): DPP9 inhibition (1G244) reduces PD-L1 via BRISC-SHMT2-IFNAR1 axis in ccRCC. New non-inflammasome function.

#### MUC1-CT Functional Validation
- **Milara/Ballester et al. 2019**, Thorax (PMID: 31801904): MUC1-CT phosphorylation (T1224+Y1229) increased in IPF; GO-201 inhibitor reduces bleomycin fibrosis in vivo; MUC1-KO mice protected.
- **Ballester et al. 2020**, Oncotarget (PMID: 29456657): Pirfenidone anti-fibrotic effects partially mediated by MUC1-CT phosphorylation inhibition.
- **MUC1-CT signaling chain**: TGFβ1 → pSmad3 → pMUC1-CT (T1224+Y1229) → β-catenin nuclear complex → EMT + FMT + fibroblast proliferation + senescence

#### NTN4 Biology
- **Reuten et al. 2016**, Nat Commun (PMID: 27901020): Netrin-4 disrupts laminin networks via high-affinity γ1 chain binding; non-enzymatic BM disruption.
- **Xiang et al. 2021**, Int J Biochem Cell Biol (PMID: 33621610): NTN4 anti-senescence and anti-inflammatory in endothelial cells; loss → ↑VCAM-1, ↑ICAM-1, impaired barrier.
- **Ramkhelawon et al. 2021**, JCI (PMID: 33393489): Related family member Netrin-1 drives lung fibrosis via macrophage-adrenergic nerve remodeling.

#### Clinical Pipeline Updates
- **Deupirfenidone (LYT-100)**: PureTech/Celea ELEVATE-IPF Phase 2b positive (Dec 2024): FVC decline -21.5 mL (825mg TID); HR=0.439 progression; 98.5% posterior probability superiority vs placebo. Phase 3 SURPASS-IPF starting H1 2026.
- **TETON-1 status**: Fully enrolled January 2025; 598 patients; top-line H1 2026. TETON-2 positive (NEJM March 2026: 95.6 mL FVC benefit).

#### Pathway Network Analysis Method
Targets were grouped into biological clusters based on:
1. Shared molecular pathway membership (GO biological process, Reactome)
2. Physical or functional protein-protein interactions (STRING, IntAct)
3. Literature-derived causal relationships (manual curation from published studies)
4. Cross-referencing with the converging-pathways model of IPF pathogenesis (Chambers & Mercer, Eur Respir Rev 2024)

Seven clusters identified: (1) Host Defense/Mucin, (2) TGF-β/Cell Signaling, (3) mTOR, (4) Telomere Maintenance, (5) Spindle Assembly, (6) Vascular/Endothelial, (7) Immune Modulation. Cross-cluster connections mapped to TGF-β as central convergence node.

---

## Session 6 (2026-03-26) — Tissue-Specific DPP9 Biology, ADS032, MUC1 Functional Evidence, Pipeline Updates

### New Data Sources

| Source | Type | Key Findings | Reference |
|---|---|---|---|
| Kidney DPP8/9 fibrosis | In vivo + in vitro | DPP8/9 OVEREXPRESSED in CKD; TC-E5007 inhibitor ANTI-fibrotic in UUO via TGF-β1/Smad; OPPOSITE to lung | Pharmacol Res 2021, PMID: 33932609 |
| Kidney DPP8/9 mesangial | In vitro | DPP8/9 siRNA inhibits TGF-β1-induced Smad2/3+Akt phosphorylation in mesangial cells | Toxicol Appl Pharmacol 2024, PMID: 38458339 |
| Kidney DPP8/9 ferroptosis | snRNA-seq + in vivo | DPP8/9 promote tubular cell ferroptosis in AKI; TC-E5007 protects | Eur J Med Res 2025, PMID: new |
| DPP9 hepatocyte KO | Mouse model | Hepatocyte-specific DPP9 KO is BENIGN; improved metabolism; fewer tumors; ↑caspase-1/autophagy | BBA-Mol Basis Dis 2025, ScienceDirect |
| ADS032 dual inhibitor | Cell-based + in vivo | First dual NLRP1+NLRP3 inflammasome inhibitor; binds NACHT domains; reduces IL-1β; protects lung | CTI 2023, PMID: 37360982 |
| Pinocembrin DPP9 activator | In vivo MCAO/R | Pinocembrin ↑DPP9 expression → ↓NLRP1 → protects lung+intestine from ischemic injury | Immunol Res 2025, DOI: 10.1007/s12026-024-09580-8 |
| Compound 6e full pub | Med chem | Oral bioavailable DPP9-selective inhibitor; long t1/2; pyroptosis-inducing | J Med Chem 2025, 68(21):23163-23184 |
| DPP9 in ccRCC | Functional | DPP9→BRISC→PD-L1; 1G244 inhibitor reduces PD-L1 in ccRCC | Cell Death Differ 2026 |
| MUC1 KL-6 chemoattractant | Functional | Purified KL-6 is MORE POTENT fibroblast chemoattractant than PDGF or FGF | PMID: 16289035 |
| NTN4 BM disruption | Structural | NTN4 disrupts laminin networks non-enzymatically via high-affinity γ1 chain binding | Nat Commun 2016, PMID: 27901020 |
| NTN4 anti-senescence | Functional | NTN4 loss → endothelial senescence (↑CDKN1A/CDKN2A), inflammation (↑VCAM-1/ICAM-1) | PMID: 33652203 |
| NTN4 anti-angiogenic | Functional | NTN4 inhibits angiogenesis via neogenin/Unc5B co-receptor | PNAS 2008, PMID: 18719102 |
| Vixarelimab MOONSCAPE | Phase 2 trial | First OSMRβ-targeting in IPF; 149 pts Cohort 1; Genentech | NCT05785624 |
| ALOFT-IPF Phase 3 | Trial design | 2-cohort design; Cohort 2 ~1,125 pts; FVC 52 wks; completion Oct 2026 | NCT06003426 |
| Zelasudil Phase 2a | Clinical | First ROCK inhibitor in IPF; hold lifted Mar 2026; Redx Pharma | RXC007 |

### Key Analytical Insights (Session 6)

**1. Tissue-Specific DPP9 Paradox:**
The DPP9 paradox is NOT just about direction (inhibit vs. activate). It is fundamentally about tissue context:
- **Kidney:** DPP8/9 are pro-fibrotic. They promote EMT and ECM deposition via TGF-β1/Smad signaling in renal tubular epithelial cells. Inhibition (TC-E5007) is therapeutic.
- **Lung (IPF):** DPP9 is protective. Loss in fibroblasts triggers NLRP1 inflammasome. The IPF GWAS signal is fibroblast-specific (PP.H4=0.989).
- **Liver:** Hepatocyte-specific DPP9 KO is benign and may be anti-tumorigenic.
- **Implication:** DPP9 modulators cannot be used systemically — organ-specific delivery or downstream targeting required.

**2. ADS032 as Genetically-Aligned Inflammasome Inhibitor:**
ADS032 (Adiso Therapeutics) represents a next-generation approach that would bypass the DPP9 paradox entirely:
- Directly inhibits both NLRP1 and NLRP3 (the two inflammasomes relevant to IPF)
- Reduces IL-1β in human macrophages and bronchial epithelial cells
- In vivo lung protection (silicosis model, influenza A)
- Genetically aligned: DPP9 loss → NLRP1 de-repression → IL-1β; ADS032 blocks at NLRP1 level

**3. MUC1 KL-6 Functional Evidence Upgraded:**
KL-6 (MUC1 epitope) is not merely a biomarker — it is a functional driver:
- More potent fibroblast chemoattractant than PDGF or FGF (PMID: 16289035)
- Accelerates fibroblast proliferation AND inhibits apoptosis
- Anti-KL-6 monoclonal antibody counteracts both effects
- MUC1-CT phosphorylation drives nuclear complex formation with Smad3/β-catenin
- MUC1-KO mice are protected from fibrosis

### Session 5/6 Addendum — DPP9 KEAP1-NRF2 Redox Axis (New Mechanistic Layer)

**Source:** Tsiatsiani et al. 2024, J Biol Chem 301(1):108034 (PMID: 39615677)

DPP9 and KEAP1 form a mutually inhibitory complex:
1. KEAP1 binds DPP9 in inactive (unfolded) conformation via C844 residue
2. Inactive DPP9 reciprocally inhibits KEAP1 → prevents NRF2 degradation → antioxidant response
3. Physiological trigger for DPP9 unfolding is unknown (stress-related)
4. Implication: DPP9 loss (IPF risk allele) = DOUBLE HIT → ↑NLRP1 inflammasome + ↓NRF2 antioxidant defense

Related: Lin et al. 2023 (PMID: 37713596) showed DPP9 binds KEAP1 via conserved ESGE motif in ccRCC, competing with NRF2; enzyme-independent mechanism.

**Therapeutic implication**: NRF2 activators (dimethyl fumarate, approved for MS) could complement anti-IL-1β therapy by addressing the redox arm of DPP9 biology. Combination strategy: anakinra + dimethyl fumarate for DPP9-risk-allele IPF patients.

### Session 6 Continued — DPP9 Inhibitor PK Comparison and SLC6A6 Characterization

#### DPP9 Selective Inhibitor PK Comparison

| Compound | DPP9 IC₅₀ | DPP9/DPP8 Selectivity | Oral Bioavail | Half-life | Status | PMID |
|---|---|---|---|---|---|---|
| Cpd 42 | 3 nM | 175x | **2%** | **<45 min** | Tool only | 37721854 |
| ICeD-2 | ~1 nM | 27x | **61%** | **20 h** | Best in vivo | 36044633 |
| Cpd 6e | ~nM | ~170x | Oral active (rats) | Long | Best selective oral | JMedChem 2025 |

**Selectivity-bioavailability trade-off**: Most selective (Cpd 42, 175x) has worst PK (2% bioavail). Best PK (ICeD-2, 61%) has only 27x selectivity.

#### Nguyen 2025 CMLS — Counter-Intuitive DPP9 Biology
(DOI:10.1007/s00018-025-05719-4): DPP9 activity **increases** in colitis/asthma; DPP8/9 inhibitors paradoxically **reduce** inflammation in those models. Contradicts simple NLRP1 paradigm.

#### SLC6A6 (Taurine Transporter) — Added Rank 25
Chin 2025 GWAS locus 3p25.1 (rs112271207). No fibrosis evidence in literature. Cancer/immune roles emerging (NatMetab 2026, Cell 2024). Lowest priority.

---

## Session 6 continued (2026-03-26) — Cross-Ancestry Generalizability, IL-1β Trial Verification, MUC1 Pirfenidone Connection

### Cross-Ancestry Analysis Sources

| Source | Year | Journal | Key Finding | PMID/DOI |
|---|---|---|---|---|
| Park et al. (All of Us) | 2025 | AJRCCM | First non-European PF genetic analysis: 129 non-EUR IPF cases; MUC5B OR similar (3.21 vs 3.26) but allele depleted; TL-PRS diminished in non-EUR (1.16 vs 1.31) | PMC12410450 |
| Korean IPF cohort | 2026 | Respir Res | MUC5B rs35705950 very rare in Korean population; different genetic architecture | DOI: 10.1186/s12931-026-03504-w |
| Partanen et al. (GBMI) | 2022 | Cell Genomics | First multi-ancestry IPF meta-analysis: 11,160 cases, 6 ancestries; 7 novel loci; 6/7 would be missed EUR-only | PMID: 36777997 |
| Garman et al. | 2024 | AJRCCM | African-derived PVT1 variants associated with sarcoidosis-related pulmonary fibrosis | AJRCCM 2024 |

### Cross-Ancestry Generalizability Assessment (Session 6 Updated)

| Target | Cross-Ancestry Data | Effect Portability | Allele Frequency Note | Drug Development Implication |
|---|---|---|---|---|
| **TERT** | EUR+EAS+AMR validated; All of Us: rare variants equally enriched across ancestries | HIGH | Common variant rs2736100 present globally | Best target for global drug development |
| **MUC5B** | All of Us: OR_EUR=3.26, OR_nonEUR=3.21 (SIMILAR) | MODERATE effect, LOW prevalence | MAF 0.12 EUR IPF vs very rare in EAS (0.007) / AFR (0.02) | SPL5B ASO: effective but fewer patients in non-EUR |
| **DPP9** | EUR-only GWAS; rs12610495 G allele MAF 12.9-28.8% globally; no cross-ancestry IPF data | UNKNOWN | Present globally but untested for IPF effect | Anti-IL-1β strategy may be ancestry-neutral |
| **DSP** | Confirmed Chin 2025 EUR; no non-EUR data | UNKNOWN | - | EUR-centric evidence only |
| **IL7** | Blood eQTL from eQTLGen (EUR-dominated) | UNKNOWN | - | CYT107 is ancestry-neutral therapy |
| **DEPTOR/NPRL3** | EUR GWAS only | UNKNOWN | - | Sirolimus is ancestry-neutral |
| **FKBP5** | Multi-ancestry GBMI; modest signal | MODERATE | rs9380529 MAF varies | SAFit2 development ancestry-neutral |
| **MUC1** | New Chin 2025 EUR locus only | UNKNOWN | KL-6 biomarker validated globally | Need cross-ancestry GWAS validation |
| **GPR157** | GBMI: EAS-enriched signal | LOW (EAS-specific) | rs7549256 enriched in EAS | EAS-focused development |
| **PSKH1** | EAS-specific (MAF 2% EAS, absent EUR) | VERY LOW | rs539683219 EAS-only | EAS-only clinical development |
| **KIF15** | All of Us: rare variants enriched regardless of ancestry | MODERATE (rare variants) | Common variant EUR; rare variant global | Rare variant-driven, ancestry-neutral |

**Key insight from All of Us analysis**: The discordance between PRS portability (IPF-PRS works cross-ancestry, TL-PRS doesn't) suggests that non-telomere IPF pathways may be more universally relevant than telomere pathways for drug development in diverse populations.

### IL-1β Inhibitor Trial Verification (March 2026)

**ClinicalTrials.gov deep search conducted**: Searched "anakinra", "canakinumab", "rilonacept", "interleukin-1", "IL-1 receptor antagonist" crossed with "pulmonary fibrosis", "IPF", "interstitial lung disease".

**Result: CONFIRMED — No active trial of any IL-1 inhibitor in IPF as of March 2026.**

Relevant IL-1 inhibitor lung disease trials found:
- NCT03925194: Anakinra in cystic fibrosis (not IPF)
- COVID-19 ARDS trials (anakinra/canakinumab) — not fibrosis-specific
- No trial registered for IPF or fibrotic ILD

### Session 7 Addendum (2026-03-26) — DPP9 Structural Deep-Dive, Dalapati 2025 Published, MUC1 Expanded, NTN4 Receptor Biology, Pipeline Failures

#### DPP9-NLRP1 Structural Biology (cryo-EM)

**Landmark structures (companion Nature 2021 papers):**
- PDB **6X6A** / **6X6C**: Human NLRP1-DPP9 complex at 3.6 Å (Hollingsworth et al., Nature 2021, PMID: 33731932). 2:1 NLRP1:DPP9 ternary complex — one full-length NLRP1 (molecule A) + one CT fragment (molecule B) per DPP9 monomer. VbP displaces NLRP1-CT from active site in 6X6C.
- PDB **7CRW**: Rat NLRP1-DPP9 complex (Huang et al., Nature 2021, PMID: 33731929). Confirmed architecture. Autocleavage at FIIND F968/S969.
- Three interfaces: (I) ZU5_A–DPP9 (~1000 Å²), (II) UPA_B threads into DPP9 substrate tunnel (~1600 Å²), (III) UPA_A dimerizes UPA_B (~800 Å²).
- ZU5 steric clash on molecule B ensures only NT-degraded CT fragment can occupy second site — DPP9 acts as "bomb defuser" sequestering freed CT fragments.

**DPP9-S759A mutant**: Catalytically dead; Dpp9-S759A/S759A mice die within 24h of birth from NLRP1 inflammasome hyperactivation. Rescued by heterozygous deletion of Nlrp1a/b/c, Asc, Gsdmd, or Il-1r (but NOT Il-18). Confirms IL-1β as the pathogenic effector (Harapas et al., Science Immunology 2022, PMID: 36112693).

#### Dalapati et al. 2025 — Published DPP9 Fibroblast Colocalization

**Full citation:** Dalapati T et al. "Context-specific eQTLs provide deeper insight into causal genes underlying shared genetic architecture of COVID-19 and idiopathic pulmonary fibrosis." HGG Advances 6(2):100410 (2025). PMID: 39876559. DOI: 10.1016/j.xhgg.2025.100410.

**Key values (published, supersede preprint):**
- DPP9 coloc in fibroblasts: PP4 = **0.968** (preprint had reported 0.989)
- DPP9 coloc in IPF cases (Borie data): PP4 = 0.874
- DPP9 coloc in COVID-19: PP4 = 0.873
- DPP9 coloc in controls: PP4 = 0.661 (weaker — disease-specific effect)
- eQTL slope: rs12610495-G → DPP9 expression **-0.212** in IPF cases (p=0.0196); **-0.074** in controls (p=0.526, NS)
- Single-cell: DPP9 decreased in AT2 cells + monocytes; **increased in myofibroblasts** (key cell-type paradox)

#### MUC1 Expanded Evidence (Session 7)

**Milara et al. 2020 (Thorax, PMID: 31801904)** — Key mechanistic details:
- n=22 IPF vs n=21 controls; MUC1-CT phosphorylation at Thr41 (T1224) and Tyr46 (Y1229) significantly increased in IPF
- GO-201 (D-amino acid cell-penetrating peptide) reduced: TGF-β1-induced myofibroblast transition, senescence markers, proliferation in ATII cells AND lung fibroblasts
- MUC1-KO mice: quantitatively reduced collagen deposition, fibrotic histology after bleomycin
- Galectin-3 activates MUC1-CT independently of TGF-β1 (TGF-β1-independent pathway)

**Ballester et al. 2020 (Oncotarget, PMID: 32341751):**
- Pirfenidone mechanism: does NOT directly inhibit canonical SMAD3 or ERK1/2 phosphorylation
- Instead: inhibits TGF-β1-induced MUC1-CT phosphorylation at Thr41 + Tyr46
- Implication: pirfenidone's anti-fibrotic effect is PARTIALLY MUC1-CT-mediated

**DS-3939 ADC (Daiichi Sankyo):** ESMO 2025 Phase 1/2 results — 64 pts advanced solid tumors; 1 CR + 10 PRs. 7 ILD events, 1 death. Anti-TA-MUC1 ADC; cancer glycoepitope not relevant for IPF, but confirms MUC1 targeting is clinically feasible.

**KL-6 prognostic data:**
- ≥1000 U/mL: IPF progression HR=2.761 (p=0.040; SciRep 2022)
- ≥1200 U/mL: mortality in IPF+OSA HR=4.887 (p=0.039; ATS 2025)
- Rising KL-6 trajectory predicts acute exacerbation (Choe PLOS One 2025, PMID: 40446067)

#### NTN4 Receptor Biology Clarification

**Critical finding: NTN4 does NOT bind classical netrin-1 receptors (DCC, UNC5A-D).**
- Crystal structure at 3.1 Å (Reuten et al., Nat Commun 2016, PMID: 27901020) revealed unique features vs NTN1
- NTN4 binds **neogenin** directly (Lejmi et al., PNAS 2008, PMID: 18719102)
- UNC5B recruited indirectly via neogenin-UNC5B complex
- Primary molecular target: **laminin gamma-1 chain** (1:1, Kd nM; Schneiders JBC 2007, PMID: 17588941)
- NTN4 is 50% identical to laminin beta-1 (not gamma-1 like other netrins)
- Expression in aberrant basaloid cells (IPF-specific; Adams SciAdv 2020, PMID: 32832599) — these cells located at edges of myofibroblast foci

#### Pipeline Failures Without Genetic Support (2024-2025)

| Drug | Target | Phase | Failure Mode | Genetic Support |
|---|---|---|---|---|
| Bexotegrast (PLN-74809) | αvβ6/αvβ1 integrins | 2b/3 | Safety: DSMB stop (worsening IPF) | None |
| GB0139/Olitigaltin | Galectin-3 (inhaled) | 2b | Efficacy: no target engagement; FVC WORSE | None |
| Zinpentraxin alfa (PRM-151) | Pentraxin-2 | 3 | Futility: no efficacy (Roche $400M write-off) | None |

**Success without genetic support:** Nerandomilast (PDE4B; approved Oct 2025), Inhaled treprostinil (prostacyclin; TETON-2 positive)
**Failure rate of genetically unsupported IPF targets (recent):** 3/5 = 60%

#### Recessive Model GWAS (February 2026 preprint)

**Citation:** medRxiv DOI: 10.64898/2026.02.18.26345897v1
- Same cohort as Chin 2025 (5,159 cases / 27,459 controls)
- 5 novel signals under recessive model not found with additive GWAS
- **PMF1**: exonic variant; increased expression in airway basal cells of IPF patients
- **EPN3** (Epsin 3): exonic variant; endocytic adapter
- Demonstrates non-additive genetic effects contribute to IPF architecture

#### eBioMedicine 2025 — Common + Rare Variant Integration

**Novel findings:**
- rs16837903 at 1q21.2: OR=0.88, p=9.5×10⁻⁹ (protective; near MCL1, BCL-2 family)
- **ANGPTL7** rare variant burden: OR=28.8, p=6.7×10⁻⁸ (angiopoietin-like 7)
- Shared aetiology with severe COVID-19 confirmed at multiple loci

**Preclinical rationale exists but untranslated:**
- IL-1ra prevents AND reverses bleomycin-induced fibrosis in mice (ScienceDirect 1993)
- NLRP3/AIM2 inflammasome activation is consensus IPF driver (reviews 2024-2025)
- DPP9 GWAS provides genetic anchor for IL-1β pathway in IPF
- This translational gap represents the single most actionable finding of the entire pipeline

### MUC1-Pirfenidone Connection (PMID: 32341751)

**Ballester, Milara, Cortijo. Oncotarget 2020; 11(13):1306-1320.**

Key finding: Pirfenidone's antifibrotic mechanism involves MUC1-CT:
- Pirfenidone does NOT inhibit canonical TGF-β1/Smad3 or ERK1/2 phosphorylation
- Instead, pirfenidone SPECIFICALLY inhibits TGF-β1-induced MUC1-CT Thr1224/Tyr1229 phosphorylation
- This reduces β-catenin activation and nuclear complex formation (pSmad3/MUC1-CT/β-catenin)
- Consequently inhibits SBE (Smad Binding Element) transcriptional activation
- Inhibits EMT, FMT, fibroblast proliferation, and cell senescence

**Implication**: MUC1-CT inhibition is already validated clinically (pirfenidone partially works through this mechanism). More specific MUC1-CT inhibitors (GO-203) could be more effective than pirfenidone while retaining the same pathway.

---

## Session 5 (2026-03-26) — Deep-Dive Updates: DPP9 Structural Biology, MUC1 Cell-Type eQTLs, NTN4 Netrin Biology, Cross-Ancestry Allele Frequencies

### New Data Sources (Session 5 Deep-Dives)

| Source | Type | Key New Data | Citation |
|---|---|---|---|
| Sewald et al. 2025 | Chemistry | Covalent DPP8/9 inhibitors from sulphostin; time-dependent kinetics | Nat Commun 16:3201 |
| Wang et al. 2025 | Pharmacology | Pinocembrin is first DPP9 transcriptional activator; DPP9↑→NLRP1↓ in lung injury | Immunol Res 73:13 |
| Natri et al. 2024 | sc-eQTL | MUC1 eQTL colocalizes with IPF GWAS in AT2, tAT2, and AT1 cells across 3 GWAS | Nat Genet PMID:38548990 |
| Milara et al. 2020 | Functional | MUC1-CT bioactivation drives EMT/FMT; MUC1-KO protected; GO-201 antifibrotic | Thorax PMID:31801904 |
| Ballester et al. 2020 | Pharmacology | Pirfenidone works through MUC1-CT phosphorylation inhibition | Oncotarget PMID:32341751 |
| Zhang et al. 2021 | Meta-analysis | KL-6 pooled HR=2.05 mortality, 1.98 progression in ILD | Front Immunol PMID:34956179 |
| Adams et al. 2020 | sc-RNA-seq | Aberrant basaloid cells defined in IPF; NTN4 highly expressed there | Sci Adv PMID:32832599 |
| Gao/Peng et al. 2021 | In vivo | Macrophage NTN1 drives lung fibrosis via adrenergic remodeling | JCI PMID:33393489 |
| Ishikawa et al. 2023 | Clinical | Alpha-1 blocker terazosin improved IPF patient survival (observational) | Am J Physiol Lung PMID:36648147 |
| Zhao et al. 2026 | In vivo | NTN1 autocrine in HSCs drives liver fibrosis via UNC5B-Ca2+-SMAD2; LNP-siRNA therapeutic | Adv Sci PMID:41514498 |
| Park et al. 2025 | Cross-ancestry | All of Us: MUC5B OR~3.2 same effect across EUR/non-EUR; IPF-PRS portable | AJRCCM PMC12410450 |

### Cross-Ancestry Allele Frequency Methodology

Allele frequencies compiled from:
- 1000 Genomes Phase 3 (30X high-coverage sequencing)
- gnomAD v4 (joint genomes + exomes)
- ALFA (Allele Frequency Aggregator, NCBI)
- 38KJPN (Japanese reference panel; for EAS-specific variants)
- Published GWAS papers (for IPF-specific frequencies)

Population codes: EUR (European), EAS (East Asian), AFR (African/African American), SAS (South Asian), AMR (Admixed American/Latino)

### Pathway Network Analysis Methodology (Expanded)

Ten pathway clusters identified using:
1. Reactome pathway membership (release 87, March 2026)
2. KEGG pathway annotations (Release 111.0)
3. GO Biological Process terms
4. STRING database protein-protein interactions (v12.0, score ≥0.7)
5. BioGRID physical interactions (release 4.4)
6. Manual curation from published mechanistic studies

Specific protein-protein interactions documented:
- BTRC ubiquitinates RIPK4 through phosphodegron motif (PMID: 29435596)
- MUC1-CT directly binds β-catenin at SXXXXXSSL motif (PMID: 12618757)
- TERT is cofactor in β-catenin/BRG1 transcriptional complex (PMID: 22723415)
- DPP9 forms 2:1 ternary complex with NLRP1 (PDB: 6X6A, 6X6C, 7CRW)
- AKAP13 activates RhoA (RhoGEF activity); FAM13A inactivates RhoA (RhoGAP, PMID: 29239766)
- DPP9 binds KEAP1 via C844 (PMID: 39615677)

---

## Limitations

1. **No original computation performed**: All results extracted from published studies. Independent re-analysis would require downloading full summary statistics.
2. **Genome build inconsistency**: Some source positions in GRCh37; standardized to GRCh38 via dbSNP where possible.
3. **European ancestry bias**: Most GWAS in European populations. GBMI provides multi-ancestry data but power varies. African-ancestry (169 cases) and South Asian (51 cases) severely underpowered. All of Us (2025) provides 129 non-EUR IPF cases — largest non-EUR dataset but still underpowered for individual SNP analysis.
4. **TWAS tissue coverage**: GTEx lung (n=515) is good but may miss cell-type-specific effects.
5. **MR instrument tissue mismatch**: Blood eQTLs (eQTLGen) have higher power than lung eQTLs but may not reflect lung-specific regulation.
6. **Druggability tiers updated**: Open Targets GraphQL API queried March 2026; tractability buckets current as of OT 2025 release.
7. **DepMap scores from 25Q3 API**: Chronos gene effect scores obtained for all 21 targets from DepMap 25Q3 Chronos_Combined via API. NPRL3 had limited coverage (45 lines tested). Cancer cell line dependency may not directly predict normal tissue toxicity — DepMap data informs safety risk but does not replace in vivo toxicology.
8. **Some TWAS/MR p-values and effect sizes not fully extractable**: Several publications reported summary findings without complete per-gene tables in accessible format.
9. **New GWAS loci from preprints**: Chin et al. 2025 and recessive model GWAS 2026 are medRxiv preprints, not yet peer-reviewed.

---

## Data Access URLs

- GWAS Catalog: https://www.ebi.ac.uk/gwas/
- GTEx Portal: https://gtexportal.org/
- eQTLGen: https://eqtlgen.org/
- GBMI IPF summary stats: Zenodo doi:10.5281/zenodo.6993906
- DepMap: https://depmap.org/portal/
- ChEMBL: https://www.ebi.ac.uk/chembl/
- ClinicalTrials.gov: https://clinicaltrials.gov/
- Open Targets: https://platform.opentargets.org/

## Software Referenced (Not Directly Run)

- FUSION (TWAS): https://github.com/gusevlab/fusion_twas
- OTTERS (TWAS): https://github.com/daiqile/OTTERS
- coloc (R package): https://github.com/chr1swallace/coloc
- eCAVIAR: https://github.com/fhormoz/caviar
- SMR: https://yanglab.westlake.edu.cn/software/smr/
- GCTA-COJO: https://yanglab.westlake.edu.cn/software/gcta/