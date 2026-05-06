# Paper 12: C8 Clarification Note — Code & Data

**On the Status of Local Entropy-Current Extensions of the Gravitational Entropy Escrow Framework: A Clarification Note**

[![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.20041992-blue)](https://doi.org/10.5281/zenodo.20041992)
[![License: MIT](https://img.shields.io/badge/Code-MIT-green)](https://opensource.org/licenses/MIT)
[![License: CC BY 4.0](https://img.shields.io/badge/Data-CC_BY_4.0-lightgrey)](https://creativecommons.org/licenses/by/4.0/)
[![Track: Entropic Bounds](https://img.shields.io/badge/Track-2_·_Entropic_Bounds-8b5cf6)](https://windstorminstitute.org/#track2)

> **Track 2 of the Windstorm Institute — Entropic Bounds in Analog Systems.** Companion to the paper's *Code and Data Availability* section.

---

## Published paper

- **[Windstorm-Institute/c8-clarification-note](https://github.com/Windstorm-Institute/c8-clarification-note)** — paper PDF, article HTML, submission scaffolds
- **Website article:** [windstorminstitute.org/articles/c8-clarification-note.html](https://windstorminstitute.org/articles/c8-clarification-note.html)
- **Zenodo:** [10.5281/zenodo.20041992](https://doi.org/10.5281/zenodo.20041992)

## Contents

The paper's *Code and Data Availability* section references a single Python script, mirrored here:

| Script | Directory | What it does |
|--------|-----------|--------------|
| **[`c8_calculations_v0_3.py`](experiments/c8_calculations/c8_calculations_v0_3.py)** | `experiments/c8_calculations/` | Reproduces every numerical claim in the paper. Uses numerical evaluation, symbolic dimensional analysis (`sympy`), and explicit reality checks against published values for: the dark energy density `ε_Λ = 5.3 × 10⁻¹⁰ J/m³` (Planck 2018), the de Sitter horizon radius `R_dS ≈ 16 Gly`, and the Gibbons–Hawking entropy `S_GH ≈ 10¹²² k_B`. |

The script verifies six claims from the paper and prints them as it runs:

1. C8 is dimensionally a rate equation
2. C8 with `t = R/c` equals the Bekenstein bound (saturated)
3. At a Schwarzschild horizon: ratio = 1 exactly
4. At a de Sitter horizon: ratio = 1 exactly (with the energy density of Λ, not the mass density)
5. The choice `t = R/c` is post-hoc — other natural horizon time scales give wildly different answers
6. Therefore C8 *is* the saturated Bekenstein bound, not new dynamics

## Reproduction

```bash
pip install sympy
cd experiments/c8_calculations
python3 c8_calculations_v0_3.py
```

- **Python:** 3.8 or later
- **Dependencies:** `sympy` (no NumPy required — only `math` and `sympy`)
- **Total compute:** under 1 second
- **External data:** none; all reality-check values are hard-coded from the cited Planck 2018 / horizon-thermodynamics references

The script is also archived in version-locked form on **[Zenodo (10.5281/zenodo.20041992)](https://doi.org/10.5281/zenodo.20041992)**.

## Methodology context

The script is *also* the answer to "what does a reality-check-anchored numerical analysis look like" for the methodology lessons of the paper's §7. Three of the four large-language-model systems consulted during the multi-round adversarial review of C8 were confidently wrong at various points about dimensional conventions; the script encodes the published-value reality checks that ultimately resolved the disagreement.

If you are operating a multi-LLM adversarial-review pipeline on a quantitative physics question, the structure of `c8_calculations_v0_3.py` — symbolic dimensional analysis + numerical evaluation + comparison against three independent published values — is intended as a portable template.

---

## Discuss this code

- **Bug, reproduction failure, or unexpected output?** → [Open an Issue](../../issues)
- **Q&A — version compatibility, hardware, generalization to other inputs?** → [Start a Discussion](../../discussions)
- **Discuss the paper itself** → [Comments on the website article](https://windstorminstitute.org/articles/c8-clarification-note.html#comments) or [Issues on the Institute repo](https://github.com/Windstorm-Institute/c8-clarification-note/issues)

---

## The Windstorm Institute

### Track 1 — The Throughput Basin · 9 papers (Papers 1–9 globally; 1st through 9th in this track; arc complete)

| # | Paper | DOI |
|---|-------|-----|
| 1 | [The Fons Constraint](https://github.com/Windstorm-Institute/fons-constraint) | [10.5281/zenodo.19274048](https://doi.org/10.5281/zenodo.19274048) |
| 2 | [The Receiver-Limited Floor](https://github.com/Windstorm-Institute/receiver-limited-floor) | [10.5281/zenodo.19322973](https://doi.org/10.5281/zenodo.19322973) |
| 3 | [The Throughput Basin](https://github.com/Windstorm-Institute/throughput-basin) | [10.5281/zenodo.19323194](https://doi.org/10.5281/zenodo.19323194) |
| 4 | [The Serial Decoding Basin τ](https://github.com/Windstorm-Institute/serial-decoding-basin) | [10.5281/zenodo.19323423](https://doi.org/10.5281/zenodo.19323423) |
| 5 | [The Dissipative Decoder](https://github.com/Windstorm-Institute/dissipative-decoder) | [10.5281/zenodo.19433048](https://doi.org/10.5281/zenodo.19433048) |
| 6 | [The Inherited Constraint](https://github.com/Windstorm-Institute/inherited-constraint) | [10.5281/zenodo.19432911](https://doi.org/10.5281/zenodo.19432911) |
| 7 | [The Throughput Basin Origin](https://github.com/Windstorm-Institute/throughput-basin-origin) | [10.5281/zenodo.19498582](https://doi.org/10.5281/zenodo.19498582) |
| 8 | [The Vision Basin](https://github.com/Windstorm-Institute/vision-basin) | [10.5281/zenodo.19672827](https://doi.org/10.5281/zenodo.19672827) |
| 9 | [The Hardware Basin](https://github.com/Windstorm-Institute/hardware-basin) | [10.5281/zenodo.19672921](https://doi.org/10.5281/zenodo.19672921) |

### Track 2 — Entropic Bounds in Analog Systems · 4 papers (Papers 10–13 globally; 1st through 4th in this track; line of inquiry active)

| # | Paper | DOI |
|---|-------|-----|
| 10 | [Phonon Extraction Bound (BEC Analog Gravity)](https://github.com/Windstorm-Institute/phonon-extraction-bound) *(1st in track)* | [10.5281/zenodo.20014391](https://doi.org/10.5281/zenodo.20014391) |
| 11 | [Gravitational Entropy Escrow](https://github.com/Windstorm-Institute/gravitational-entropy-escrow) *(2nd in track)* | [10.5281/zenodo.20032023](https://doi.org/10.5281/zenodo.20032023) |
| 12 | [C8 Clarification Note](https://github.com/Windstorm-Institute/c8-clarification-note) *(this paper — 3rd in track; companion to Paper 11)* | [10.5281/zenodo.20041992](https://doi.org/10.5281/zenodo.20041992) |

| 13 | [Lattice QFT Test of the Static Escrow Postulate](https://github.com/Windstorm-Institute/lattice-qft-test) *(4th in track; supplement to Paper 11)* | [10.5281/zenodo.20043421](https://doi.org/10.5281/zenodo.20043421) |
**Website:** [windstorminstitute.org](https://windstorminstitute.org)

---

*Code: MIT License · Data: CC BY 4.0*
