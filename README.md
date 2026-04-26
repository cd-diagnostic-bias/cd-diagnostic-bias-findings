# Celiac Disease Diagnostic Bias Research

**Version:** 1.4  
**Last Updated:** 2026-04-26  
**Status:** Pre-publication analysis (not peer-reviewed)

Systematic investigation of diagnostic biases in celiac disease detection, documenting how current diagnostic algorithms systematically miss significant patient populations.

---

## Where to Start

With 37 files, here's where to begin depending on your time and interest:

| Time | Goal | Start Here |
|------|------|------------|
| **10 min** | Core argument | [7.2 Guideline Critique](https://raw.githubusercontent.com/cd-diagnostic-bias/cd-diagnostic-bias-findings/main/7_2_guideline_critique_celiac_2026-02-12_FINAL_v2_minified.json) |
| **20 min** | Quantitative cascade | [7.1 Cascade Sensitivity](https://raw.githubusercontent.com/cd-diagnostic-bias/cd-diagnostic-bias-findings/main/7_1_cumulative_cascade_sensitivity_celiac_2026-02-11_FINAL_lean_minified.json) |
| **30 min** | Seronegative CD deep-dive | [3.1 SNCD Synthesis](https://raw.githubusercontent.com/cd-diagnostic-bias/cd-diagnostic-bias-findings/main/3.1_SNCD_final_synthesis_minified.json) + [8.3 Mucosal Deposits](https://raw.githubusercontent.com/cd-diagnostic-bias/cd-diagnostic-bias-findings/main/8.3_SNCD-Deposits-FINAL-v2_1_minified.json) |
| **Full review** | All topics | Start with [file_index.json](https://raw.githubusercontent.com/cd-diagnostic-bias/cd-diagnostic-bias-findings/main/file_index.json) |

For detailed instructions with all file URLs, see [CD_Research_Project_Instructions_v2.md](CD_Research_Project_Instructions_v2.md).

---

## Key Findings Summary

The widely cited ~93% sensitivity of IgA-tTG2 is derived from studies where only seropositive patients receive confirmatory biopsy. When corrected for this verification bias (Hujoel et al. 2021), sensitivity drops to **57.1% (95% CI: 35.4–76.4%)**.

| Finding | Statistic | Source File |
|---------|-----------|-------------|
| IgA-tTG2 sensitivity (bias-corrected) | **57%** (not 93%) | 1.1 |
| Marsh 3A pathologist agreement | **κ = 0.33** | 2.1 |
| Elderly CD patients undetected | **58%** | 3.6 |
| Black CD patients seronegative | **80%** | 3.7 |
| GFD followers lacking diagnosis | **72%** | 3.8 |
| CD patients with anti-tTG6 (neurological) | **40%** | 9.1 |

### Overlooked Populations

| Population | Estimated Miss Rate | Key File |
|------------|---------------------|----------|
| Marsh 3A | 60-80% | 2.4A1, 2.4B |
| DQ8-only genotype | 40-60% | 3.2 |
| Elderly (>60) | 58% | 3.6 |
| Non-white | 75-80% | 3.7 |
| Already on GFD | >90% | 3.8 |
| Neurological (tTG6+) | Unknown | 9.1 |

### Guideline Limitations

Analysis of ACG 2023, ESPGHAN 2020/2022, ESsCD 2025, and BSG 2024 guidelines reveals:

- Sensitivity claims not adjusted for verification bias
- Seronegative CD underestimated
- Neurological manifestations inadequately addressed
- Racial/ethnic disparities not considered
- No guidance for immunoglobulin-deficient patients

---

## Methodology

### How This Research Was Conducted

This research was conducted using **AI-assisted systematic literature review**:

- **Primary analysis:** Claude Opus 4.5/4.6 (Anthropic)
- **Adversarial peer review:** Grok 3.1 (xAI) and additional Claude instances
- **Literature source:** PubMed via API, with PMID verification
- **Cross-validation:** Multi-model consensus required for key findings

### What This Means

Each finding includes PMID citations verified against PubMed. The JSON files contain `verified_citations` and `pmid_verification_required` fields distinguishing confirmed from unverified references.

### What This Is NOT

- ❌ **Not a peer-reviewed publication** — This is a structured pre-publication analysis
- ❌ **Not original clinical research** — This synthesizes existing published literature
- ❌ **Not medical advice** — See Disclaimer below

This analysis is intended to surface diagnostic biases for further investigation by researchers and clinicians.

---

## Limitations

**Please read before using these findings:**

1. **Not peer-reviewed** — Findings should be verified against primary sources before citing in academic work

2. **AI-assisted synthesis may misinterpret studies** — PMID verification confirms the citation exists, not that the summary fully captures the source's conclusions or context

3. **Selection bias in topic coverage** — This analysis focuses on seronegative and missed presentations; some areas of CD diagnostics receive less coverage

4. **Reliance on limited evidence base** — Some findings rely on small studies or single research groups (e.g., Spanish IEL lymphogram work, Sheffield gluten ataxia data)

5. **Reference patient context** — Several files reference an anonymized "reference patient" (DQ8+, Marsh 3A, seronegative, low IgG1) that motivated certain research directions; this may introduce perspective bias

6. **Rapidly evolving field** — New guidelines (ESsCD 2025) and research may supersede some findings

---

## File Structure

All findings are in minified JSON format. While designed for machine consumption, each file contains an `executive_summary` field readable by humans.

### Sections

| Section | Topic | Files |
|---------|-------|-------|
| **1.x** | Verification Bias & Serology Accuracy | 3 |
| **2.x** | Biopsy Interpretation Biases | 6 |
| **3.x** | Overlooked Populations | 11 |
| **4.x** | Diagnostic Cascade Failures | 2 |
| **5.x** | Unproven Guideline Assumptions | 2 |
| **6.x** | Disease Spectrum & Alternatives | 3 |
| **7.x** | Synthesis (Cascade Sensitivity, Guideline Critique) | 2 |
| **8.x** | Monitoring & Classification | 5 |
| **9.x** | Extraintestinal Manifestations | 2 |
| **10.x** | Microbiome-Immune Pathogenesis | 1 |

**Total: 37 research files**

### File Index

For a structured index with descriptions and key findings, see:  
📄 **[file_index.json](https://raw.githubusercontent.com/cd-diagnostic-bias/cd-diagnostic-bias-findings/main/file_index.json)**

### Raw File Access

Files can be accessed directly via:
```
https://raw.githubusercontent.com/cd-diagnostic-bias/cd-diagnostic-bias-findings/main/FILENAME
```

---

## Usage

### For AI/LLM Integration

These files are optimized for machine consumption. In Claude or similar:

```
Fetch the file index:
https://raw.githubusercontent.com/cd-diagnostic-bias/cd-diagnostic-bias-findings/main/file_index.json

Then fetch specific topic files as needed using web_fetch.
```

See [CD_Research_Project_Instructions_v2.md](CD_Research_Project_Instructions_v2.md) for complete instructions with all explicit URLs.

### For Researchers

Each JSON file contains:

| Field | Description |
|-------|-------------|
| `executive_summary` | Brief human-readable overview |
| `key_findings` | Structured findings with evidence strength ratings |
| `biases_documented` | Identified methodological biases in the literature |
| `contradictory_studies` | Studies challenging the consensus |
| `research_gaps` | Areas needing further investigation |
| `recommendations` | Evidence-based suggestions |
| `key_citations` | PMIDs for primary sources |

### For Clinicians

Start with [7.2 Guideline Critique](https://raw.githubusercontent.com/cd-diagnostic-bias/cd-diagnostic-bias-findings/main/7_2_guideline_critique_celiac_2026-02-12_FINAL_v2_minified.json) for an overview of where current guidelines may fall short. The `executive_summary` and `clinical_implications` fields in each file are written for clinical relevance.

---

## Citation

### Citing Primary Sources

Each finding documents PMIDs. **Please cite the primary sources**, not this analysis. Example:

> Verification-bias-corrected IgA-tTG2 sensitivity: 57.1% (Hujoel et al. 2021, PMID: 33965987)

### Citing This Analysis

This analysis is unpublished and cannot be formally cited in academic work. If you wish to reference it informally:

> CD Diagnostic Bias Research Project (2026). Celiac Disease Diagnostic Bias Findings. GitHub repository. https://github.com/cd-diagnostic-bias/cd-diagnostic-bias-findings

---

## Disclaimer

This research is for **educational and research purposes only**.

- Clinical decisions should be made in consultation with qualified healthcare providers
- Individual patient circumstances vary and may not match patterns described here
- This analysis is not a substitute for professional medical judgment
- The authors are not liable for clinical decisions based on this content

---

## License

MIT License — see [LICENSE](LICENSE) file.

---

## Contributing

This is currently a closed research project. If you identify errors in citations or interpretations, please open an issue.

---

## Changelog

| Version | Date | Changes |
|---------|------|---------|
| 1.4 | 2026-04-26 | Added Section 10 (Microbiome); updated 3.2B, 8.3 filenames; added methodology and limitations |
| 1.0 | 2026-02-12 | Initial release with 36 files |
