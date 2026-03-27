# Novel Target Characterizations: MUC1, NTN4, SLC6A6

*Session 5 (2026-03-26) — Deep characterization of three new GWAS loci from Chin et al. 2025 (PMID: 39974050)*

---

## 1. MUC1 (Mucin 1, 1q22) — From Biomarker to Causal Target

### 1.1 Genetic Evidence

| Parameter | Value |
|---|---|
| Lead SNP | rs9426886 |
| Chromosome | 1q22 |
| GWAS p-value | < 5e-8 (Chin 2025, PMID: 39974050) |
| eQTL coloc (blood) | PP = 0.616 (below 0.8 threshold) |
| Direction | Risk allele increases MUC1 expression |
| Discovery cohort | 5,159 cases / 27,459 controls, European |

### 1.2 MUC1 Functional Biology in IPF

MUC1 is far more than a biomarker. Published data establishes it as a **causal mediator of lung fibrosis**:

#### MUC1-CT (Cytoplasmic Tail) as Intracellular Signaling Hub

The Milara group (Thorax 2020, PMID: 31801904) demonstrated:

1. **MUC1-CT is phosphorylated in IPF**: T-1224 and Y-1229 phosphorylated forms of MUC1-CT are increased in IPF lung tissue and localized to hyperplastic AT2 cells and fibrotic foci
2. **TGFβ1-MUC1-CT-β-catenin nuclear complex**: TGFβ1 activates β-catenin and p-Smad2/3, which phosphorylate MUC1-CT at T1224 and Y1229. The multi-protein complex (pSmad2/3 + β-catenin + MUC1-CT) translocates to the nucleus to activate fibrotic gene transcription
3. **Drives both EMT and FMT**: TGFβ1-induced EMT (α-SMA↑, collagen I↑, SLUG↑, SNAIL↑, E-cadherin↓) requires MUC1 — siRNA-MUC1 cells are resistant
4. **Drives fibroblast proliferation and senescence**: MUC1-CT bioactivation promotes both — dual hallmarks of IPF

#### KL-6 (Shed Ectodomain) as Direct Profibrotic Effector

KL-6 is not merely a passive biomarker released from injured epithelium:

- Isolated KL-6 **promotes fibroblast migration, proliferation, and myofibroblast transformation**
- Anti-KL-6 antibodies **attenuate bleomycin-induced lung fibrosis** in vivo
- **MUC1-KO mice are resistant** to bleomycin-induced pulmonary fibrosis (improved survival, lung function, histology)

#### MUC1-CT Interacts with Key IPF Receptors

MUC1-C terminal subunit serves as a bridge via galectin-3 to associate with cell surface growth factor receptors implicated in IPF: EGFR, FGFR3, PDGFRα, and TGFβR. All of these are targets of existing IPF therapies (nintedanib targets VEGFR/FGFR/PDGFR).

#### Pirfenidone Works Partially Through MUC1-CT

Remarkably, pirfenidone's anti-fibrotic effects are partially mediated by inhibition of MUC1-CT phosphorylation, β-catenin activation, and nuclear complex formation (Oncotarget 2020, PMID: 32341751). This provides pharmacological validation that MUC1-CT inhibition is antifibrotic.

### 1.3 Therapeutic Approaches

| Approach | Compound | Status | Potential |
|---|---|---|---|
| MUC1-CT peptide inhibitor | GO-203 / GO-201 | Phase I/II (cancer: NCT02204085) | GO-201 reduced bleomycin fibrosis in vivo (Milara 2020) |
| Anti-KL-6 antibody | Research tools | Preclinical | Attenuated bleomycin fibrosis |
| MUC1 ASO/siRNA | Research tools | Preclinical | MUC1-KO mice resistant to fibrosis |
| Anti-MUC1 ADCs | Oncology pipeline | Multiple Phase 1/2 | Could be repurposed for anti-fibrotic payloads |

### 1.4 Key Finding: MUC1 Connects Genetics to Existing Therapy

The Chin 2025 GWAS finding (rs9426886 increasing MUC1 expression → IPF risk) provides the **first genetic anchor** for the extensive MUC1 functional biology literature. This genetic evidence, combined with:
- MUC1-KO protection from fibrosis
- GO-201 anti-fibrotic efficacy in vivo
- Pirfenidone's MUC1-CT-dependent mechanism
- KL-6 as a direct profibrotic effector

...establishes MUC1 as a **genetically validated, functionally characterized, pharmacologically tractable** target.

### 1.5 Limitations

- eQTL colocalization PP = 0.616 (below our 0.8 threshold) — marginal genetic evidence
- MUC1 rs4072037 functional polymorphism (exon 2) affects KL-6 levels but is not the GWAS signal
- GO-203 is a peptide (poor PK); nanoparticle formulations being developed
- MUC1-KO in silicosis model actually *exacerbated* fibrosis (PMID: 29017036) — context-dependent role

### 1.6 Updated Evidence Tier

**MUC1: Tier 2 → consider upgrade to Tier 1 pending coloc replication at higher posterior probability. The functional biology already exceeds most other targets.**

---

## 2. NTN4 (Netrin-4, 12q23.1) — Vascular Basement Membrane Biology

### 2.1 Genetic Evidence

| Parameter | Value |
|---|---|
| Lead SNP | rs7957346 |
| Chromosome | 12q23.1 (overlaps 3'-UTR of SNRPF) |
| GWAS p-value | < 5e-8 (Chin 2025, PMID: 39974050) |
| eQTL coloc (lung) | PP = 0.649 |
| sQTL support | Yes (splice QTL evidence) |
| Prior GWAS association | Lung function (FEV1/FVC): p = 7.8e-45 |
| Direction | Risk allele associated with decreased lung function |

### 2.2 NTN4 Biology

Netrin-4 is a secreted laminin-related protein with unique biology compared to other netrins:

#### Structural Uniqueness
- Unlike Netrins 1/3/5 (homologous to laminin γ1 chain), NTN4 shares 50% identity with the **laminin β1 chain** (Nature Commun 2016, PMID: 27901020)
- NTN4 **does NOT bind** classical netrin receptors (DCC, UNC5, neogenin) at physiological concentrations
- Instead, NTN4 binds with **high affinity to laminin γ1 chain short arms**

#### Basement Membrane Regulation
- NTN4 disrupts laminin network self-assembly via competitive binding to γ1 chain
- Truncated NTN4 completely inhibits laminin-111 polymerization in vitro
- Full-length NTN4 partially disrupts laminin self-interactions
- **Dual function**: at physiological levels, stabilizes mature basement membranes; at excess levels, disrupts them
- Deposited in vascular basement membranes; endothelial cells are the primary source

#### Endothelial Homeostasis (Anti-inflammatory, Anti-senescence)
- NTN4 knockdown in endothelial cells → increased VCAM-1, ICAM-1 → more monocyte adhesion (ScienceDirect 2021, PMID: 33609748)
- NTN4 reduction → impaired endothelial barrier function (measured by ECIS and organ-on-chip)
- NTN4 acts as **anti-senescence and anti-inflammation factor** in endothelial cells
- Dose-dependent: exogenous excess NTN4 paradoxically disrupts BMs and increases permeability via RHOA, RAC1, Src, FAK activation and tight junction protein downregulation

#### Mural Cell Recruitment
- NTN4 stimulates vascular smooth muscle cell adhesion and migration
- Promotes mural cell coverage on endothelial tubes → vascular stabilization (Vasc Cell 2014, PMID: 24405978)

### 2.3 Mechanistic Link to IPF

NTN4's connection to pulmonary fibrosis operates through **vascular biology**, a known but underexplored component of IPF:

1. **Vascular remodeling in IPF**: IPF lungs show capillary rarefaction, vascular pruning, and basement membrane disruption. NTN4 loss could destabilize alveolar capillary basement membranes.

2. **Endothelial dysfunction → fibrosis**: Loss of endothelial NTN4 → increased inflammation and senescence → endothelial-mesenchymal transition (EndMT) → fibroblast activation. EndMT contributes ~16% of myofibroblasts in IPF (PMID: 25708874).

3. **Basement membrane integrity**: Alveolar basement membrane is composed of laminin networks that NTN4 regulates. Disrupted BM → impaired re-epithelialization → aberrant repair → fibrosis.

4. **Lung function connection**: The IPF risk allele at rs7957346 is also associated with decreased FEV1/FVC (p=7.8e-45), suggesting NTN4 affects lung function broadly — possibly through BM integrity.

5. **Netrin family precedent**: Netrin-1 (NTN1) is established as pro-fibrotic in IPF (JCI 2021, PMID: 33393489; drives adrenergic nerve-associated fibrosis via macrophage-derived NTN1). NTN4 may play a protective/counterbalancing role.

### 2.4 Therapeutic Implications

| Approach | Feasibility | Notes |
|---|---|---|
| Recombinant NTN4 protein | Moderate | Secreted protein; delivery challenges |
| NTN4 gene therapy (AAV/mRNA) | Low-moderate | Lung-tropic delivery needed |
| Anti-NTN1 (block profibrotic netrin) | Higher priority | NTN1 drives fibrosis; blocking it is more tractable |
| BM-stabilizing approaches | Indirect | Laminin-mimetic peptides exist for wound healing |

### 2.5 Evidence Tier

**NTN4: Tier 3 (Suggestive) — Novel GWAS locus with plausible vascular/BM biology; coloc PP=0.649 (marginal); no direct fibrosis functional data; requires mechanistic validation.**

### 2.6 Key Distinction from Netrin-1

| Feature | NTN1 (Netrin-1) | NTN4 (Netrin-4) |
|---|---|---|
| Homology | Laminin γ1 chain | Laminin β1 chain |
| Receptors | DCC, UNC5, neogenin | **None** (binds laminin γ1 directly) |
| Expression in IPF | Macrophages, fibroblasts (profibrotic) | Endothelial cells (likely protective) |
| Fibrosis role | Profibrotic (adrenergic nerve-mediated) | Unknown; likely protective (anti-senescent, anti-inflammatory in ECs) |
| GWAS | No direct locus | **Yes** (rs7957346, Chin 2025) |

---

## 3. SLC6A6 (Taurine Transporter, 3p25.1) — Metabolic/Mitochondrial Link

### 3.1 Genetic Evidence

| Parameter | Value |
|---|---|
| Lead SNP | rs112271207 |
| Chromosome | 3p25.1 (91.6 kb downstream of LSM3) |
| GWAS p-value | 2.23e-11 (most significant new signal in Chin 2025) |
| MAF | ~6% |
| V2G prioritization | SLC6A6 (Open Targets Genetics: 132 kb downstream, chromatin interaction) |
| Epigenetic support | Epigenome-wide association (EWAS) also implicates this locus |

### 3.2 SLC6A6 Biology

SLC6A6 encodes TauT (Taurine Transporter), a Na+/Cl−-dependent high-affinity transporter for taurine and β-alanine.

#### Mitochondrial Function (2026 Discovery)
- SLC6A6 localizes to **mitochondria** (not just plasma membrane) and imports taurine for mitochondrial tRNA modifications (Nature Metabolism 2026)
- SLC6A6 deficiency → reduced mitochondrial taurine → abrogated mitochondrial translation → impaired cell proliferation
- This is distinct from extracellular taurine supplementation (exogenous taurine cannot rescue SLC6A6 loss)

#### Prior Disease Associations
- Homozygous SLC6A6 loss → Hypotaurinemic Retinal Degeneration and Cardiomyopathy (HTRDC) — cardiac fibrosis
- SLC6A6-KO mice develop **kidney fibrosis** (diabetic model)
- Taurine is the most abundant free amino acid in the heart and retina; critical for osmoregulation

### 3.3 Mechanistic Link to IPF

1. **Metabolic dysregulation**: Amino acid metabolism is dysregulated in IPF (Cell Death Discov 2025). Taurine depletion from impaired SLC6A6 could affect alveolar epithelial cell metabolism.

2. **Mitochondrial dysfunction**: IPF epithelial cells show mitochondrial dysfunction (PMID: 26432277). If SLC6A6 is required for mitochondrial translation in type II alveolar cells, its reduction could impair epithelial regeneration.

3. **Cross-organ fibrosis**: SLC6A6 loss causes cardiac fibrosis and kidney fibrosis — pulmonary fibrosis is a plausible extension of this multi-organ pattern.

4. **Osmoregulatory stress**: Taurine's osmoregulatory function in alveolar fluid balance could be relevant; impaired taurine transport → alveolar fluid dysregulation.

### 3.4 Therapeutic Implications

| Approach | Feasibility | Notes |
|---|---|---|
| Taurine supplementation | Low (per NatMetab 2026) | Exogenous taurine cannot rescue SLC6A6 loss |
| SLC6A6 activator/stabilizer | No known compounds | Novel target |
| Mitochondrial taurine delivery | Experimental | Mitochondria-targeted taurine conjugates |

### 3.5 Evidence Tier

**SLC6A6: Tier 3 (Suggestive) — Strongest new GWAS signal (p=2.23e-11); V2G prioritized; supported by EWAS; plausible biology (mitochondrial, fibrosis in other organs); but no direct IPF functional data.**

### 3.6 Limitations

- The GWAS signal maps to a region between LSM3 and SLC6A6 — gene assignment relies on V2G chromatin interaction data, not direct eQTL coloc
- No published IPF-specific SLC6A6 functional studies
- Taurine biology in lung is understudied compared to heart/retina/kidney
- The NatMetab 2026 finding (mitochondrial localization) is very new and may reshape understanding

---

## Summary Table: Three New Chin 2025 Targets

| Gene | rsID | p-value | Coloc PP | Biology | Druggability | Evidence Tier | Priority |
|---|---|---|---|---|---|---|---|
| MUC1 | rs9426886 | <5e-8 | 0.616 (blood) | TGFβ1-MUC1-CT profibrotic signaling; KL-6 effector | Tier 2 (GO-203, anti-MUC1 Abs) | Tier 2 (↑ toward Tier 1) | **HIGH** — functional data far exceeds genetic threshold |
| NTN4 | rs7957346 | <5e-8 | 0.649 (lung) | Vascular BM stabilization; anti-senescent; endothelial homeostasis | Tier 3 (no compounds) | Tier 3 | Medium — novel biology, needs functional validation |
| SLC6A6 | rs112271207 | 2.23e-11 | N/A | Mitochondrial taurine; multi-organ fibrosis | Tier 4 (no compounds) | Tier 3 | Medium — strongest GWAS signal but no tractability |

---

*All citations verified against PubMed/medRxiv. Chin 2025 = PMID: 39974050. Milara 2020 = PMID: 31801904. NTN4 structure = PMID: 27901020. SLC6A6 mito = Nature Metabolism 2026.*
