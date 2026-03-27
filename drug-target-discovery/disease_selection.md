# Disease Selection: Idiopathic Pulmonary Fibrosis (IPF)

## Decision

**Selected disease: Idiopathic Pulmonary Fibrosis (IPF)**

## Rationale

### 1. Severe Unmet Medical Need

IPF is a chronic, progressive, irreversible fibrotic lung disease with a **median survival of 3-5 years** from diagnosis. Before October 2025, only two approved anti-fibrotic drugs existed:

- **Pirfenidone** (Esbriet; approved 2014) — slows FVC decline ~50% but does not halt or reverse disease
- **Nintedanib** (Ofev; approved 2014) — similarly slows progression

In October 2025, **nerandomilast** (Jascayd; PDE4B inhibitor) became the first new IPF approval in a decade. Despite this advance, **none of the three approved drugs were discovered through genetic evidence**, and all only slow disease progression without halting or reversing fibrosis. Lung transplant remains the only curative option.

### 2. Exceptional GWAS Data Quality and Depth

IPF has one of the best-characterized common-variant genetic architectures among fibrotic/rare diseases:

| Study | Year | Cases / Controls | Novel Loci | Total Signals | Journal | PMID |

|---|---|---|---|---|---|---|

| Fingerlin et al. | 2013 | 1,616 / 4,683 | 7 | 10 | Nature Genetics | 23583980 |

| Allen et al. | 2017 | 2,760 / 8,561 | 1 (AKAP13) | ~11 | Lancet Respir Med | 29066090 |

| Allen et al. | 2020 | 2,668 / 8,591 (disc.) | 3 (KIF15, MAD1L1, DEPTOR) | 14 | AJRCCM | 31710517 |

| Allen et al. | 2022 | 4,125 / 20,464 | 5 (KNL1, NPRL3, RTEL1, STMN3, 10q25) | 23 | Thorax | 35688625 |

| Partanen et al. (GBMI) | 2022 | 11,160 / 1,364,410 | 7 (GPR157, FKBP5, FUT6, etc.) | 25 | Cell Genomics | 36777997 |

Cumulative: **>25 independent genome-wide significant loci** spanning diverse biological pathways.

The **MUC5B promoter variant rs35705950** (OR ~4-5) is one of the largest-effect common variants known in any complex disease and serves as a strong internal positive control for pipeline validation.

### 3. Clear Tissue Relevance for Computational Analysis

IPF is a **lung-specific disease**, making analytical priorities clear:

- **GTEx v8 lung tissue**: 515 samples with RNA-seq, enabling robust TWAS/S-PrediXcan
- **IPF-specific lung eQTLs**: Borie et al. 2022 (234 IPF + 188 control lung samples; PMID: 35816432)
- **Single-cell lung eQTLs**: Nature Genetics 2024 (66 PF + 48 control donors; 38 cell types)
- **eQTLGen Consortium**: Blood eQTLs for MR instruments (~31,000 samples)

This tissue clarity contrasts sharply with brain disorders (depression, ALS) where relevant cell types are heterogeneous and tissue access is limited.

### 4. Well-Characterized Biology with Druggable Pathways

Known IPF susceptibility pathways from GWAS include:

- **Telomere maintenance**: TERT, TERC, OBFC1/STN1, RTEL1
- **Mucociliary defense**: MUC5B, TOLLIP, FUT6, ATP11A
- **Epithelial barrier / cell-cell adhesion**: DSP, DPP9
- **mTOR signaling**: DEPTOR, NPRL3
- **Spindle assembly / cell division**: KIF15, KNL1, MAD1L1
- **Rho-GTPase / profibrotic signaling**: AKAP13, FAM13A

Several of these map to classically druggable protein families (kinases, peptidases, GPCRs, phosphodiesterases).

### 5. Comparison with Other Candidate Diseases

| Criterion | IPF | TRD | ALS | PCOS |

|---|---|---|---|---|

| GWS loci | >25 | ~1-2 (TRD-specific) | 15 | ~15 |

| Largest GWAS N (cases) | 11,160 | ~2,000 (TRD) | 29,612 | ~5,200 |

| Tissue clarity | Lung (GTEx) | Brain (limited) | Motor neuron (limited) | Ovary/adrenal (limited) |

| Approved drugs | 3 (modest efficacy) | 1 (esketamine) | 3-4 (marginal) | Symptomatic only |

| Genetic-to-drug gap | **Largest** | MDD loci ≠ TRD | Heterogeneous | Moderate |

| TWAS/eQTL feasibility | Excellent | Moderate | Poor | Moderate |

**IPF wins on**: tissue specificity, GWAS depth per locus, clarity of pathobiology, largest gap between genetic evidence and current therapeutics, and feasibility of TWAS/coloc/MR pipeline.

### 6. Validation Opportunity

The MUC5B locus provides an unambiguous positive control. If the pipeline correctly ranks MUC5B as a top causal gene with strong colocalization (PP.H4 = 1.00 in published data) and appropriate therapeutic directionality, it validates the entire methodology and lends credibility to novel target discoveries.

## Conclusion

IPF is the optimal disease for this causal drug target discovery pipeline. It offers: deep GWAS data, clean tissue context, a verified positive control (MUC5B), limited existing therapeutics, and an active clinical pipeline against which novel genetic targets can be benchmarked.