# Celiac Disease Diagnostic Bias Research

Systematic investigation of diagnostic biases in celiac disease detection, documenting how current diagnostic algorithms systematically miss significant patient populations.

## Overview

This repository contains structured research findings from a comprehensive analysis of celiac disease (CD) diagnostic pathways. The research reveals that:

- **Verification bias** inflates reported IgA-tTG2 sensitivity from ~93% to an adjusted **57%**
- **Marsh 3A** (partial villous atrophy) has pathologist agreement of only **κ=0.33**
- **58%** of elderly CD patients remain undetected
- **80%** of Black CD patients are seronegative
- **72%** of people following a gluten-free diet lack formal CD diagnosis
- **40%** of newly diagnosed CD patients have anti-tTG6 (neurological) antibodies

## File Structure

All findings are in minified JSON format for efficient machine access.

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

## Quick Access

### File Index

Download `file_index.json` for a structured index of all files with descriptions and key findings.

### Raw File Access

Files can be accessed directly via:
```
https://raw.githubusercontent.com/cd-diagnostic-bias/cd-diagnostic-bias-findings/main/FILENAME
```

Example:
```
https://raw.githubusercontent.com/cd-diagnostic-bias/cd-diagnostic-bias-findings/main/1.1_research_verification_bias_v2_minified.json
```

## Key Findings Summary

### The Core Problem: Verification Bias

The widely cited ~93% sensitivity of IgA-tTG2 is derived from studies where only seropositive patients receive confirmatory biopsy. When corrected for this verification bias (Hujoel et al. 2021), sensitivity drops to **57.1% (95% CI: 35.4–76.4%)**.

### Overlooked Populations

| Population | Estimated Miss Rate | Key File |
|------------|--------------------| ---------|
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

## Usage

### For AI/LLM Integration

These files are designed for machine consumption. In Claude or similar:

```
Fetch the file index:
https://raw.githubusercontent.com/cd-diagnostic-bias/cd-diagnostic-bias-findings/main/file_index.json

Then fetch specific topic files as needed.
```

### For Researchers

Each JSON file contains:
- `executive_summary`: Brief overview
- `key_findings`: Structured findings with evidence strength
- `biases_documented`: Identified methodological biases
- `contradictory_studies`: Studies challenging consensus
- `research_gaps`: Identified areas needing investigation
- `recommendations`: Evidence-based suggestions

## Citation

If using these findings in research, please cite the underlying primary sources documented in each file's `key_citations` fields.

## License

MIT License - see LICENSE file.

## Disclaimer

This research is for educational and research purposes. Clinical decisions should be made in consultation with qualified healthcare providers and consideration of individual patient circumstances.
