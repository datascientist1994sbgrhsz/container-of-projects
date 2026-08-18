# US resident mortality

Unofficial static compilation of **incommensurable** U.S. resident mortality series. One file: `index.html`. Cutoff **18 August 2026**. No build step. No CDN.

**Not** an FBI, CDC, or NCHS product.

## Constructs

| Symbol | What it is | What it is not |
| --- | --- | --- |
| **D** | NVSS resident deaths (1933–2024 registered; 2025 provisional; 1900–32 national estimates) | UN WPP |
| **P** | Midyear Census population (thousands) | |
| **CDR** | D / P × 10⁵ | NCHS year-2000 **AA** |
| **AA** | Age-adjusted to the year-2000 U.S. standard | CDR |
| **UCR** | Police-reported murder / nonnegligent manslaughter | NVSS homicide (ICD) |
| **X40–Y14** | Drug-poisoning *underlying* cause (ICD-8/9/10; breaks 1979, 1999) | T40.4 mentions |
| **T40.4** | Multiple-cause mention, synthetic opioids other than methadone | A partition of all-drug |
| **U07.1** | COVID-19 *involving* (any mention), 2020– | *Underlying*-only |
| **XA** | Excess vs a U.S. expected baseline (OWID / RGA family) | A CDC year-total |
| **XB** | Excess vs other high-income countries (Bor et al., *JAMA Health Forum* 2025) | XA |

Do not add series. A missing residual is **not** zero. 2025 has **no** CDC publication that states “0 excess deaths.”

Hashes: `#method`, `#src`, `#murder`, `#od`, `#covid`, `#y/2020`. Language persists in the browser (EN HU RO DE ES). Year notes stay in English.

## Legal

- **Software** (HTML/CSS/JS and arrangement): MIT. See `LICENSE`.
- **U.S. federal statistical releases**: generally public domain (17 U.S.C. § 105). Cite the agency.
- **Non-federal sources** (journal articles, OWID, RGA): remain their owners’. Citation is not a license to republish those works.
- **Trademarks** identify sources only. No endorsement. No advice. No warranty.
- **Scope:** mortality series only. No private names. No party or administration pages.

Written to stay inside GitHub’s [Acceptable Use Policies](https://docs.github.com/en/site-policy/acceptable-use-policies/github-acceptable-use-policies). GitHub still decides enforcement.

If you fork, do not add local paths, account names, API keys, or unpublished files.

## Deploy

Publish this folder (or the parent repository root, which redirects here) with GitHub Pages: Settings → Pages → Deploy from a branch → `main`.
