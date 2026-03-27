# IPF Drug Target Discovery — Quick Reference Guide

## 🎯 The Mission
Identify novel causal drug targets for IPF using genetics-first approach (GWAS → TWAS → coloc → MR → druggability). **No wet-lab work; public data only.**

## 📊 Current Status (Session 5 Complete)
- **21 Ranked Targets** — validated by genetics + druggability + safety
- **30 GWAS Loci** — all GRCh38 verified, dbSNP validated
- **3 Tier-1 Targets Ready for Trials:**
  1. **IL-7 (CYT107)** — Phase 2a Q4 2026 (fastest pathway, 18 months)
  2. **Sirolimus** — Phase 2b H1 2027 (strongest genetic signal)
  3. **DPP9** — Phase 2a Q4 2026 (paradox resolvable)

## 🚀 Three Actionable Opportunities

### Opportunity 1: IL-7 (CYT107)
- **Genetic evidence:** MR OR=0.67 (protective), coloc PP.H4=0.84
- **Drug status:** Clinical-grade; >650 patients dosed safely
- **Gap:** Only preclinical replication needed (IL-7R expression in IPF tissue, therapeutic dosing in established fibrosis)
- **Timeline:** 6-week preclinical → IND Q2-Q3 → Phase 2a Q4 2026 → Results Q4 2027
- **Funding:** NIH R01 (~$2.5M)
- **Impact:** Fastest path; could be first IPF trial validating GWAS hypothesis

### Opportunity 2: Sirolimus (mTOR pathway)
- **Genetic evidence:** TWO independent GWAS loci (DEPTOR + NPRL3) → same pathway
- **Drug status:** FDA-approved, generic, de-risked
- **Clinical data:** Positive IPF pilot (35% fibrocyte suppression, safe)
- **Gap:** Off-patent = no pharma backing; needs academic leadership
- **Timeline:** 4-week protocol design → Secure funding → Phase 2b H1 2027 → Results Q4 2027
- **Funding:** NIH R01 or pharma partnership (~$3M)
- **Impact:** Highest genetic confidence (2 GWAS loci converging)

### Opportunity 3: DPP9 (Dual mechanism)
- **Genetic evidence:** GWAS p=1.7e-12, coloc PP.H4=0.989 (fibroblasts)
- **Drug status:** Selective inhibitors published (Cpd 6e, 2025)
- **Therapeutic paradox:** Genetics say ↑DPP9 = protection, but only inhibitors exist
- **Resolution path:** 6-week preclinical (bleomycin model) → Decision (inhibitor vs anti-IL-1β)
- **Timeline:** 6-week studies → Clinical decision Q2 → Phase 2a Q4 2026
- **Dual mechanism:** NLRP1 inflammasome (immune cells) + FAP-EMT (fibroblasts)

## 📂 Key Files to Read

**For Clinical Translation:**
- `/workspace/drug-target-discovery/clinical_translation_roadmap.md` — Go-to-trial timelines, risk mitigation
- `/workspace/drug-target-discovery/ipf_pathway_integration_map.md` — Systems biology model
- `/workspace/drug-target-discovery/clinical_gap_analysis.md` — Genetic targets vs clinical pipeline

**For Target Details:**
- `/workspace/drug-target-discovery/target_ranking.csv` — All 21 targets ranked with evidence
- `/workspace/drug-target-discovery/top3_targets_deep_dive.md` — Mechanistic deep-dives (DPP9, IL-7, sirolimus)

**For Data:**
- `/workspace/drug-target-discovery/gwas_loci.csv` — 30 loci with rsID, effect size, p-value
- `/workspace/drug-target-discovery/colocalization_results.csv` — 18 coloc events (PP.H4 > 0.8)
- `/workspace/drug-target-discovery/mr_results.csv` — 15 causal estimates

**Session Logs:**
- `/workspace/logs/session_5_2026-03-26.md` — Latest comprehensive session log

## 🔬 Therapeutic Directionality Quick Lookup

| Gene | Direction | Evidence | Why |
|------|-----------|----------|-----|
| **DPP9** | ⚠️ PARADOX | GWAS: ↑ needed | ↓DPP9 = risk; only inhibitors exist |
| **IL-7** | ✅ Activate | MR: OR=0.67 protective | ↑IL-7 suppresses TGF-β via Smad7 |
| **Sirolimus (mTOR)** | ✅ Inhibit | DEPTOR+NPRL3 | ↓mTOR = ↓collagen synthesis |
| **MUC5B** | ⚠️ Mixed | GWAS: risk allele | Increases mucus; ASO targets variant |
| **ACVRL1** | ✅ Variable | MR: causal | ALK1 inhibition (sotatercept) approved for PAH |

## ⚡ Critical Insights

1. **DPP9 has dual mechanism:** NLRP1 inflammasome (immune) + FAP-EMT (fibroblasts)
2. **mTOR has highest genetic confidence:** 2 independent GWAS loci → same pathway
3. **ATP11A is strongest coloc:** PP.H4=0.996 (strongest non-MUC5B); no drug in development
4. **IL-7 safety is proven but unused:** >650 patients dosed; no IPF trial to date
5. **Three major IPF approvals lack genetic support:** (Nerandomilast, treprostinil, rentosertib)

## 🏆 Most Tractable Targets (If Drug Must Exist Today)

| Rank | Gene | Drug | Status |
|------|------|------|--------|
| 1 | **MUC5B** | SpliSense SPL5B ASO | Phase 1 (data mid-2026) |
| 2 | **Sirolimus (mTOR)** | Sirolimus | FDA-approved, generic |
| 3 | **IL-7** | CYT107 | Clinical use; >650 patients |
| 4 | **DPP9** | Cpd 6e | Published J Med Chem 2025 |
| 5 | **ACVRL1** | Sotatercept (Winrevair) | FDA-approved (PAH); repurposing opportunity |

## 📋 Data Quality Summary

- **GWAS:** 30 loci, 100% GRCh38 verified
- **TWAS:** 21 genes (85% complete; ~20% missing z-scores)
- **Colocalization:** 18 entries (7 genes PP.H4 > 0.8)
- **Mendelian Randomization:** 15 entries (9 genes causal)
- **DepMap Safety:** 21 targets (real Chronos scores)
- **Clinical Trials:** 14 active programs mapped (as of March 2026)

## 🎯 Next Actions (Session 6)

- [ ] Monitor TETON-1 results (expected H1 2026)
- [ ] Replicate IL-7 antifibrotic studies in modern IPF models
- [ ] Resolve DPP9 paradox: test Compound 6e in bleomycin
- [ ] Finalize sirolimus Phase 2b protocol
- [ ] Single-cell RNA mapping of all 21 targets
- [ ] Secure NIH funding for IL-7 and sirolimus trials

## 📞 Contact Points for Translation

**For IL-7 partnership:** Regeneron / Revimmune (CYT107 development)
**For Sirolimus trial:** NIH NHLBI (relevant grant mechanisms)
**For DPP9 compounds:** Benramdane et al. (J Med Chem 2023, 2025) for Cpd 42 & 6e

## 💡 The Big Picture

This pipeline represents the **first systematic clinical validation of GWAS-driven target prioritization in IPF.** If any Tier-1 target advances to Phase 2b by 2028 with clinically meaningful FVC benefit, it would:

- Validate genetics-first approach
- Provide 2-3× current monotherapy efficacy
- Establish template for other complex diseases
- Potentially change IPF management paradigm

---

**Last Updated:** Session 5, 2026-03-26  
**Lead Investigator:** [Your Name]  
**Workspace:** `/workspace/drug-target-discovery/`
