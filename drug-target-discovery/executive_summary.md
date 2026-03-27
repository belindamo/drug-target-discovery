# Genetics-First Drug Target Discovery for Idiopathic Pulmonary Fibrosis: Executive Summary

*Computational Genomics Pipeline — 10 Sessions, March 2026*

---

## Premise

Idiopathic pulmonary fibrosis (IPF) kills ~80% of patients within 5 years. Three drugs are approved (pirfenidone, nintedanib, nerandomilast) — none target genetically validated mechanisms. We asked: **what are the genetically causal drug targets for IPF, and is the pharmaceutical industry pursuing them?**

## Approach

We built a systematic pipeline using only published public data:

1. **GWAS locus curation** — 30 genome-wide significant loci from 7 studies (largest: Chin 2025, 5,159 cases)
2. **TWAS** — 22 gene-tissue associations (lung, blood; GTEx, eQTLGen)
3. **Colocalization** — 18 high-confidence colocalizations (PP.H4 > 0.8); strongest: ATP11A (0.996), DPP9 fibroblasts (0.989)
4. **Mendelian randomization** — 18 causal gene-disease links; multi-method with pleiotropy testing
5. **Druggability** — Open Targets tractability (up to 10 buckets), ChEMBL compounds, DepMap cancer essentiality (25Q3)
6. **Clinical gap analysis** — comparison against all active IPF trials (ClinicalTrials.gov March 2026)
7. **Mechanistic deep-dives** — DPP9/NLRP1/IL-1β, MUC1-CT, NTN4, mTOR, and 8-pathway network analysis
8. **Cross-ancestry assessment** — All of Us 2025 (129 non-EUR IPF cases), Korean cohort 2026, GBMI multi-ancestry

## Key Results

### The Gap Is Enormous

- **~83% of active IPF pipeline programs target genes without GWAS support**
- **≥15 genetically validated targets have no IPF trial**
- Of 25 ranked targets, 4 have immediately actionable drug repurposing opportunities

### Top 5 Actionable Findings

| # | Finding | Drug | Status | Evidence |
|---|---------|------|--------|----------|
| **1** | **IL-1β blockade is genetically aligned via DPP9→NLRP1 pathway but has NEVER been tested in IPF** | Anakinra / canakinumab (approved) | Zero IPF trials | DPP9 GWAS p=1.7e-12; coloc PP.H4=0.989 fibroblasts; DPP9 KO rescued by Il-1r hemizygosity (PMID:36112693); IL-1ra prevents + reverses murine fibrosis; 3 FDA-approved agents with >10,000 patient-years safety data |
| **2** | **Recombinant IL-7 (CYT107) has genetic, preclinical, and safety evidence for IPF** | CYT107 (clinical-grade) | Zero IPF trials | MR OR=0.67 protective; IL-7 inhibits fibroblast TGF-β via JAK1/STAT1/Smad7; reduces bleomycin fibrosis; >650 patients dosed safely; safe in COVID lung |
| **3** | **mTOR hyperactivation is implicated by TWO independent GWAS loci; sirolimus is the genetically correct drug** | Sirolimus (approved) | Pilot data exists | DEPTOR + NPRL3 GWAS; sirolimus pilot: 35% fibrocyte suppression (PMID:36853800); mTORC1-selective unlike failed everolimus |
| **4** | **MUC1-CT is a functional fibrotic driver, not just a biomarker; pirfenidone partially works through it** | GO-203 (MUC1-CT inhibitor) | Preclinical | MUC1 KO mice protected; GO-201 antifibrotic in vivo; pirfenidone inhibits MUC1-CT phosphorylation (PMID:32341751); GWAS locus (Chin 2025) |
| **5** | **MUC5B promoter variant (OR=4.11) is the strongest genetic risk factor; first targeted ASO entering Phase 1** | SPL5B inhaled ASO | Phase 1 (2026) | Strongest GWAS signal in IPF (rs35705950, p<1e-121); coloc PP.H4=1.00; platform validated by SPL84 CF success |

### The DPP9 Paradox — Resolved

DPP9 (rank #2) has the strongest combined genetic + druggability evidence but CANNOT be inhibited for IPF — inhibitors activate the NLRP1 inflammasome. The causal chain is:

**DPP9 loss → NLRP1 de-repression → caspase-1 activation → IL-1β release → TGF-β amplification → fibrosis**

The solution is to target IL-1β downstream. Three FDA-approved IL-1 inhibitors exist. None have been tested in IPF. This is the pipeline's single most impactful finding.

Additionally, DPP9 shows a tissue-specific paradox: in kidney, DPP8/9 are PRO-fibrotic via TGF-β/Smad (PMID:33932609), while in lung, DPP9 is PROTECTIVE via NLRP1 suppression. This means DPP8/9 inhibitors (TC-E5007) reduce kidney fibrosis but would WORSEN lung fibrosis — a critical safety consideration.

### 25 Targets in 8 Biological Modules

| Module | Targets | Key Druggable Intervention |
|--------|---------|---------------------------|
| Mucin / Epithelial | MUC5B, MUC1, TOLLIP, FUT6, ANO9 | SPL5B ASO, GO-203, anti-galectin-3 |
| TGF-β / Smad | ACVRL1, DSP, SMAD2, GREM1 | Sotatercept (FDA-approved PAH) |
| mTOR / Autophagy | DEPTOR, NPRL3 | Sirolimus |
| Telomere | TERT, TERC, RTEL1, OBFC1 | Danazol (weak); gene therapy (future) |
| Cell Adhesion / Rho | DSP, AKAP13, FAM13A | Zelasudil (ROCK2 inhibitor, Phase 2a IPF) |
| Spindle Assembly | KIF15, MAD1L1, KNL1, SPDL1 | Undruggable (activation needed) |
| Immune / Inflammasome | IL7, FKBP5, RIPK4, BTRC, DPP9→IL-1β | CYT107, SAFit2, anakinra/canakinumab |
| Vascular / Endothelial | ACVRL1, NTN4, ATP11A | Sotatercept, NTN4 agonists (novel) |

### Cross-Ancestry Portability

The All of Us analysis (2025, AJRCCM) revealed differential PRS portability:
- **Non-telomere IPF pathways are more portable** across ancestries (IPF-PRS: OR 1.35 non-EUR vs 1.29 EUR)
- **Telomere-length PRS is diminished** in non-Europeans (OR 1.16 vs 1.31)
- **MUC5B effect size is similar** across ancestries (OR ~3.2) but allele frequency is dramatically lower in non-EUR

**Implication**: Drug development targeting inflammasome (DPP9/IL-1β), mTOR (DEPTOR/NPRL3), and immune (IL-7) pathways may serve more diverse global populations than telomere-focused approaches.

## What Pharma Is Missing — And Why

| Opportunity | Why Overlooked | Why It Shouldn't Be |
|-------------|---------------|---------------------|
| Anti-IL-1β (anakinra) for IPF | PANTHER trial (2012) created lasting anti-inflammatory skepticism; TGF-β-centric paradigm dominates | PANTHER used broad immunosuppression, not targeted IL-1; DPP9 GWAS provides genetic anchor; approved drugs exist |
| CYT107 (IL-7) for IPF | IL-7 historically viewed as immune stimulant, not antifibrotic | New mechanism: JAK1/STAT1/Smad7 axis inhibits TGF-β in fibroblasts; preclinical efficacy proven |
| Sirolimus for IPF | Everolimus failed → "mTOR doesn't work" | Everolimus inhibits mTORC1+2; sirolimus is mTORC1-selective; TWO GWAS loci support mTORC1 |
| MUC1-CT inhibitors | MUC1 viewed as biomarker (KL-6), not target | KO mice protected; GO-201 antifibrotic in vivo; pirfenidone mechanism involves MUC1-CT |

## Proposed Proof-of-Concept Trials (No New Drug Development Required)

1. **Anakinra + SOC in IPF** — Phase 2a; enrich for high BAL IL-1β; stratify by DPP9 genotype; 12 weeks; FVC + biomarkers
2. **CYT107 + SOC in IPF** — Phase 2a; PK/PD in IPF lung; assess TGF-β pathway biomarkers; 16 weeks
3. **Sirolimus + SOC in IPF** — Phase 2b; powered for FVC at 52 weeks; biomarker: fibrocyte count, mTOR activity in PBMCs

## Limitations

- All findings are from published literature extraction — no original GWAS/TWAS computation
- European ancestry dominance in genetic data (>90% of GWAS)
- DepMap cancer cell line essentiality may not predict normal tissue toxicity
- Chin 2025 and some other sources are preprints pending peer review
- NTN4 direction paradox unresolved; requires functional studies

## Bottom Line

The IPF drug development pipeline is overwhelmingly pursuing targets without genetic support (~83%). Meanwhile, four immediately testable, genetically-grounded drug repurposing opportunities — anti-IL-1β, recombinant IL-7, sirolimus, and MUC1-CT inhibitors — remain untried. The most impactful finding is that IL-1β blockade (anakinra/canakinumab) is genetically aligned through DPP9→NLRP1 biology, supported by preclinical mouse data, and available in three FDA-approved formulations — yet has never been tested in IPF. A single proof-of-concept trial could close this gap.

---

*Pipeline: 30 GWAS loci → 22 TWAS → 18 colocalizations → 18 MR → 25 ranked targets → 8 pathway modules → 4 actionable drug repurposing candidates. All data public, all analyses computational, all citations traceable to DOI/PMID.*
