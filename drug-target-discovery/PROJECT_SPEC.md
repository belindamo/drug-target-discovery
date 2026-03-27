# Causal Drug Target Discovery — Automated Pipeline

## Objective

Identify and rank novel causal drug targets for a poorly-understood disease using only publicly available data and computational (bioinformatics) methods. No wet-lab experiments.

## Disease Selection Criteria

Pick a disease with:

- Recent large-scale GWAS data publicly available
- Few approved drugs (high unmet medical need)
- Candidates: treatment-resistant depression, PCOS, idiopathic pulmonary fibrosis (IPF), ALS
- The agent should commit to ONE disease early and deepen analysis over time

## Pipeline Steps

### Step 1 — GWAS Summary Statistics

- Source: GWAS Catalog (EBI), OpenGWAS (MRC IEU), published Nature/Nature Genetics papers
- Collect genome-wide significant loci (p < 5e-8)
- Record: lead SNPs, effect alleles, betas/ORs, sample sizes

### Step 2 — TWAS (Transcriptome-Wide Association Study)

- Method: S-PrediXcan across GTEx v8 (54 tissues)
- Map GWAS loci to effector genes via genetically predicted expression
- Prioritize tissue-relevant models (e.g., lung for IPF, brain for depression)
- Record: gene, tissue, z-score, p-value, prediction R²

### Step 3 — Colocalization

- Method: coloc (Bayesian), eCAVIAR, or HyPrColoc
- Test whether GWAS and eQTL signals share a causal variant (not just LD)
- Filter criterion: PP.H4 > 0.8 (coloc) — removes ~50% false positives
- Record: gene, tissue, PP.H4, shared causal SNP

### Step 4 — Mendelian Randomization (MR)

- Method: IVW, MR-Egger, weighted median, MR-PRESSO
- Exposure: genetically predicted gene expression (cis-eQTLs as instruments)
- Outcome: disease risk
- Establish causal direction: gene expression → disease
- Record: gene, method, beta, SE, p-value, pleiotropy test results

### Step 5 — Therapeutic Directionality

- For each causal gene: does increased or decreased expression increase disease risk?
- Map to: should we INHIBIT or ACTIVATE the target?
- Cross-reference with known pharmacology where available

### Step 6 — Druggability Scoring

- Sources: ChEMBL, Open Targets Platform, DGIdb
- Score each target: has known ligands? Protein class (kinase, GPCR, ion channel, etc.)?
- Tier: Tier 1 (approved drug exists for other indication), Tier 2 (clinical-stage compounds), Tier 3 (tool compounds only), Tier 4 (no known ligands)

### Step 7 — Safety / Cancer Liability Check

- Source: DepMap (Broad Institute), CRISPR essentiality screens
- Flag targets where loss-of-function causes cancer cell lethality (potential oncology liability)
- Record: dependency score, selectivity

### Step 8 — Clinical Trial Cross-Reference

- Source: ClinicalTrials.gov, Open Targets
- Which genetically-supported targets are already in trials?
- Which are being MISSED by pharma? (novel opportunities)

## Output Artifacts (continuously updated)

- `disease_selection.md` — rationale for chosen disease
- `gwas_loci.csv` — curated GWAS hits
- `twas_results.csv` — S-PrediXcan gene-tissue associations
- `colocalization_results.csv` — colocalized genes (PP.H4 > 0.8)
- `mr_results.csv` — Mendelian randomization causal estimates
- `target_ranking.csv` — final ranked target list with evidence tiers
- `clinicalgapanalysis.md` — what's in trials vs. what genetics says
- `methods_notes.md` — detailed methods, tools, parameters, data versions

## Logging Structure

- `/workspace/research_log.md` — Master log at workspace root. Contains experiment overview paragraph and one-sentence-per-session bullet list. This is the single source of truth for project history.
- `/workspace/logs/sessionNYYYY-MM-DD.md` — Detailed log for each session. Includes full accomplishments, findings, limitations, and next steps. Linked from the research log.

## Data Constraints

- **Only public data**: GWAS Catalog, GTEx, eQTLGen, OpenTargets, ChEMBL, DepMap, ClinicalTrials.gov
- **Only published/peer-reviewed sources**: preference for Nature, Nature Genetics, Lancet, NEJM
- **No proprietary data, no API keys required beyond public endpoints**
- **All work must be reproducible from public sources**

## Quality Standards

- Every claim must cite a specific dataset version or publication (with DOI/PMID)
- Statistical thresholds must be explicit and justified
- Sensitivity analyses where possible (multiple MR methods, tissue comparisons)
- Limitations must be documented honestly