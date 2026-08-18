# US resident mortality

Static compilation of incommensurable U.S. mortality series: **UCR murder**, **NVSS drug-poisoning**, **all-cause 1900–2025** (crude rates on charts), **COVID-19**, and **excess** (U.S.-expected and HIC-peer). One file: `index.html`.

Cutoff recorded in the page: **18 August 2026**. No build step. No CDN. No network after the file loads.

Open `index.html`, or publish this folder with GitHub Pages (Settings → Pages → Deploy from a branch → `main` / repository root). Shareable hashes: `#murder`, `#od`, `#covid`, `#y/2020`.

## What this is

An unofficial compilation and viewer. It is **not** an official FBI, CDC, or NCHS product. Figures are transcribed or reconstructed from public releases and named secondary sources listed on the Sources page (`#src`). Method notes live on `#method`.

Series are **not interchangeable**:

| Series | What it counts |
| --- | --- |
| FBI UCR murder | Police-reported murder / non-negligent manslaughter |
| CDC homicide | Death-certificate homicides (often higher than FBI murder) |
| CDC overdose | ICD-coded drug-poisoning deaths (coding breaks in 1979 and 1999) |
| COVID “involving” | U07.1 on the certificate — not the same as underlying-cause-only |
| Excess vs U.S. expected | Deaths above a U.S. baseline (OWID / CDC-style / RGA) |
| Excess vs high-income peers | Separate JAMA Health Forum estimates — not a CDC year-total |
| NCHS all-cause | Registered resident deaths 1933–2024; 2025 provisional; 1900–32 national estimates (registration incomplete) |
| All-cause charts | Crude rate per 100,000 (count ÷ midyear population), not NCHS age-adjusted |

Some rows are **provisional**, **rounded**, **rate-reconstructed**, or **12-month windows**, not calendar-year finals. The 2026 overdose figure on the page is the 12 months ending February 2026, not a 2026 calendar year-to-date. There is **no** official CDC “0 excess deaths” year-total for 2025 on this page.

## Legal

- **Software** (this HTML/CSS/JS and arrangement): MIT. See `LICENSE`.
- **U.S. federal statistical releases**: generally public domain in the United States (17 U.S.C. § 105). Cite the originating agency if you reuse them.
- **Non-federal sources** (for example journal articles, OWID presentations, RGA commentary): remain the property of their owners. This page cites selected published figures for reference. Republishing those works in full is not authorized here.
- **Trademarks** (FBI, CDC, and others) belong to their owners. Use here is identification only.
- **No endorsement.** Publication of a number is not a finding, verdict, or official statistic.
- **No advice.** Not legal, medical, actuarial, or law-enforcement advice.
- **No warranty.** Series are revised. Transcription and reconstruction can be wrong. Check primary sources before relying on a figure.
- **Sensitive content.** Pages discuss deaths as published statistical series. They do not name private individuals.

Scope is **mortality series only**: FBI murder, CDC overdose / synthetics, NCHS all-cause and COVID, and published excess-mortality estimates. No administrations, parties, border, or immigration pages.

This repository is written to stay inside GitHub’s [Acceptable Use Policies](https://docs.github.com/en/site-policy/acceptable-use-policies/github-acceptable-use-policies):

- No private personal information ([doxxing policy](https://docs.github.com/en/site-policy/acceptable-use-policies/github-doxxing-and-invasion-of-privacy)).
- No threats or graphic violence; mortality is shown as tables and charts, with an unofficial-compilation notice ([violence policy](https://docs.github.com/en/site-policy/acceptable-use-policies/github-threats-of-violence-and-gratuitously-violent-content)).
- Series are labeled as official, provisional, reconstructed, or third-party so they are not presented as a single CDC/FBI fact ([misinformation policy](https://docs.github.com/en/site-policy/acceptable-use-policies/github-misinformation-and-disinformation)).
- No malware, secrets, or unpublished local files.

GitHub still decides enforcement. This is not a guarantee.

If you fork this repository, do not add local paths, account names, API keys, or unpublished files.

## Deploy

From a clone of **this** repository (do not commit another machine’s home directory):

```bash
git add index.html LICENSE README.md .gitignore .nojekyll
git commit -m "US resident mortality"
git branch -M main
git remote add origin https://github.com/OWNER/REPO.git
git push -u origin main
```

Replace `OWNER/REPO` with the GitHub repository. Do not put personal filesystem paths in commits or this file.
