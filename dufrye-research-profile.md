# Personal Research Profile — Dustin Frye
### Pre-filled template for `/interview-me` in clo-author
*Paste this at the start of every `/interview-me` session.
Fill in the [PROJECT-SPECIFIC] block at the bottom before pasting.*

---

## How to Use This Template

1. Fill in the **[PROJECT-SPECIFIC]** block at the bottom
2. Launch Claude Code from your project folder: `cd [project folder] && claude`
3. Run `/interview-me`
4. When Claude asks its first question, paste this entire document
5. Claude will write `.claude/rules/domain-profile.md` from this automatically

---

## Researcher Profile

**Name:** Dustin Frye
**Title:** Assistant Professor, Department of Agricultural and Applied Economics,
University of Wisconsin–Madison
**Affiliations:** NBER Research Economist; Faculty Affiliate, Institute for Research
on Poverty; Faculty Affiliate, La Follette School of Public Affairs
**PhD:** University of Colorado Boulder (Economics). Fields: Urban Economics,
Development Economics, Economic History

**Research program:** My research spans urban economics, economic history, and
development economics, with a unifying focus on how public policy, infrastructure,
and institutions shape long-run economic development and spatial outcomes. I work
across three interconnected areas:

1. **Transportation infrastructure:** Effects of highway and railroad networks on
   employment concentration, land development, and spatial economic structure
   (interstate highways, railroad abandonment, market integration)

2. **Urban environmental economics:** Long-run consequences of urban infrastructure
   decisions, particularly lead water pipes and childhood exposure to environmental
   toxins, on labor market outcomes and intergenerational mobility

3. **Native American economic history:** Property rights, governance, and
   development on American Indian reservations — land allotment, federal oversight,
   self-governance, blood quantum, and the long-run legacy of federal Indian policy

A defining feature of my work is **original data construction and digitization** —
assembling new historical datasets from census microdata, land patents, infrastructure
maps, mortality records, BIA records, and administrative sources, often requiring
archival research and digitization of previously unused records.

**Published in:** Review of Economics and Statistics, Journal of Political Economy:
Microeconomics, Public Choice, AEA Papers and Proceedings

**Grants:** NSF (# 2017946), USDA Hatch, Campbell Fellow (Hoover Institution)

---

## Identification & Econometrics

**Primary identification strategies:**
- Difference-in-differences (including staggered adoption / heterogeneous treatment)
- Instrumental variables (network theory instruments, historical plans, chemical
  interactions, geographic instruments)
- Event study designs
- Regression discontinuity (narrowly determined elections, geographic boundaries)

**Typical instruments I use:**
- Historic military/planning maps combined with network theory algorithms to predict
  highway/railroad construction timing and location
- Proposed-but-never-built highway segments from 1920s interstate plans as
  counterfactual locations
- Chemical properties of local water supply interacted with lead pipe adoption
- Voting thresholds and close elections for governance discontinuities

**Standard errors:**
- Default: cluster at the treatment unit
- Spatial data: Conley spatial HAC when cross-sectional dependence is a concern
- Varies by paper depending on data structure and identification design

**Robustness expectations:**
- Always report pre-trends tests for DiD and event study designs
- For staggered DiD, use modern estimators robust to heterogeneous treatment effects
  (Callaway-Sant'Anna, Sun-Abraham, de Chaisemartin-D'Haultfoeuille) — never
  vanilla TWFE without justification
- IV: always report first-stage F-statistics, reduced form, and weak instrument tests
- Spatial papers: discuss MAUP and modifiable unit concerns where relevant
- Fine-grained fixed effects (neighbor comparisons, grid-cell level) preferred where
  data permit

**Spatial methods:** Comfortable with fine-grained spatial analysis at grid-cell
(1km x 1km) level; satellite imagery for land use outcomes; GIS-based construction
of treatment variables from infrastructure maps

---

## Data Sources & Construction

**Commonly used:**
- Full count historical US Censuses (1900–1940) including Native American populations
- Bureau of Indian Affairs annual reports and administrative records
- Bureau of Land Management land patent records
- Satellite imagery and remote sensing (land cover, NLCD, nighttime lights)
- Census and ACS (decennial, 5-year estimates)
- Property and real estate records (transactions, assessments, parcel data)
- Historical infrastructure maps (highway plans, railroad networks)
- Mortality records and vital statistics

**Data construction approach:**
- Original digitization and archival research is central to my work, not incidental
- Probabilistic record linkage across historical sources (e.g., Indian Census Rolls
  to full-count Census) is a standard part of my toolkit
- Raw data is never modified — all cleaning happens in scripts
- Raw data lives outside the project folder in a shared Dropbox location
- Derived/intermediate data lives in `data/derived/` within the project folder
- All scripts use dynamic path globals — never hardcoded absolute paths
  - Stata: source `globals.do` first every session
  - R: source `paths.R` at top of every script
  - Python: import `config.py` at top of every script

---

## Software Stack

| Task | Tool |
|------|------|
| Primary analysis, regressions, data cleaning | Stata (StataNow SE 19.5) |
| Figures, visualization, spatial plots | R |
| Data construction, large-scale processing, ML | Python / Anaconda |
| Exploratory analysis, prototyping | Jupyter notebooks |
| GIS / spatial analysis | ArcGIS, QGIS, GRASS |
| Writing | LaTeX (via Overleaf, synced to Dropbox) |

---

## Target Journals & Writing Style

**Journal targeting strategy:** Paper-dependent. I aim for the highest appropriate
venue given the scope and contribution. I do not pre-constrain to a tier.

**Journals I publish in and target:**
- Top 5: AER, JPE, QJE, Review of Economic Studies, Econometrica
- Strong applied: Review of Economics and Statistics, AEJ: Applied Economics,
  AEJ: Economic Policy
- Field: Journal of Urban Economics, Journal of Public Economics, Journal of
  Economic History, Explorations in Economic History, Journal of Labor Economics,
  JAERE, Journal of Human Resources, Journal of Political Economy: Microeconomics
- Others as appropriate: Public Choice, Land Economics, Transport Geography

**Writing style:** Varies by paper and venue. I adjust register and level of
formalism to the audience. Across all venues I prioritize:
- Building economic intuition clearly before introducing formal apparatus
- Careful institutional detail — the setting and mechanism matter, not just the
  estimate
- Honest, direct treatment of identification threats and limitations
- Precise, unadorned prose — no overselling, no hedging

**Referee I write for:** A technically sophisticated, skeptical referee who will
probe the identification strategy, the instrument's validity, and the external
relevance of the setting. I anticipate and address the toughest objections directly
in the paper rather than leaving them for the response letter.

---

## Quality Standards

- Pre-trends must be shown, tested, and discussed for any DiD or event study
- Staggered DiD must use heterogeneous-treatment-robust estimators
- Tables: always include sample sizes, fixed effects indicators, and clustering info
- Figures: publication-ready from R — no Stata default graphics in final papers
- Code must be reproducible end-to-end from raw data with a single master script
- Every analysis file must begin with globals/path setup
- Data construction and analysis scripts are separated — never mix them

---

## [PROJECT-SPECIFIC] — Fill in before pasting

**Project title / working title:**
[FILL IN]

**One-sentence description:**
[FILL IN — what is the question, what is the setting, what is the identifying variation]

**Current state of the project:**
[FILL IN — e.g., data under construction / analysis underway / paper drafted / R&R]

**Primary dataset(s) for this project:**
[FILL IN]

**Identification strategy for this project:**
[FILL IN — be specific about the instrument or design and why it is valid here]

**Target journal(s) for this project:**
[FILL IN]

**Key open questions or concerns:**
[FILL IN — what are you most uncertain about, what do you want Claude to flag]

**Project file locations:**
- Scripts: [FILL IN — e.g., empirics[projectname]/]
- LaTeX: /Users/dufrye/Dropbox (Personal)/Apps/Overleaf/[ProjectName]/
- Derived data: data/derived/
- Raw data: [FILL IN — path within Dropbox]
- Outputs: output/
