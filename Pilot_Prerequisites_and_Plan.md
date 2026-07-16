# FMHP Pilot — Prerequisites & Plan

_The concrete next step after the demo. Purpose: run First Medical's **real data** through a
focused measure set, under proper controls, and prove rates that match (or beat) their current
reporting — so the pilot decision is grounded, not aspirational._

## The boundary (say this plainly, always)
| Stage | What it is | Data | Status |
|---|---|---|---|
| **Demo** (today) | Proof the engine runs NCQA's logic on the measure shapes | Synthetic, no PHI | ✅ done |
| **Pilot** (this plan) | Real FMHP data → wedge measures → validated rates + gap lists | **Real PHI, under a BAA** | ⏳ proposed |
| **Production** | Certified, submitted, ongoing, full measure set | Real PHI, hosted | future |

The demo is **not** a compliance system. The pilot is where real data first enters — and only with the prerequisites below.

## Prerequisites (all required before any real data moves)
1. **Business Associate Agreement (BAA) + secure environment.** FMHP's data is PHI. Nothing starts
   until a signed BAA and a HIPAA-compliant, access-controlled environment exist. The demo repo has
   *never* held PHI — that line holds until this is in place.
2. **NCQA DCS license** for the target Measurement Year — the licensed digital measure packages for
   the pilot set (paid, per-measure, per-year). Free public packages are demo-only.
3. **Data extract from FMHP** (their MHK "Member-360" feeds or equivalent): enrollment/eligibility,
   medical claims + diagnoses, pharmacy (NDC), lab (LOINC), provider/specialty. A defined layout +
   a data dictionary.
4. **Agreed wedge measure set** — 3–5 ASES-scrutinized measures that have digital packages available
   (e.g. **BCS, COL, HbA1c/diabetes**, and CCS once its Pap mapping is finalized). CAHPS is **out**
   (survey-based; needs a survey vendor).
5. **UMLS license** (free) for value-set refresh from VSAC where needed.

## Scope
- **In:** ingest FMHP's real feeds → FHIR; run the wedge measures; validate/reconcile the load;
  produce rates, patient-level detail (PLD), and care-gap pursuit lists; compare to FMHP's current
  (MHK) rates for the same period.
- **Out (this pilot):** NCQA **Measure Certification** (a separate, parallel track — required before
  results are *reportable*), full 40+ measure set, CAHPS, production hosting, IDSS submission to NCQA.

## Plan
1. **Setup** — BAA, secure environment, DCS license, agree wedge set + data layout.
2. **Ingest & map** — build/harden the Member-360 → FHIR mapping for FMHP's *actual* formats and code
   sets. *(This is the bulk of the effort — the CCS Pap issue is a preview: each measure's data must
   map exactly.)*
3. **Validate & reconcile** — row counts, referential integrity, dedup, load report (auditable).
4. **Run measures** — execute the licensed packages on the real population; compute rates + PLD.
5. **Gap closure** — produce prospective per-PCP pursuit lists for the wedge measures.
6. **Compare & report** — diff Alpine's rates vs FMHP's current reported rates for the same MY;
   deliver a findings report + go/no-go recommendation.

## Success criteria
- Alpine's wedge-measure rates **reconcile with FMHP's current reported rates** (same population,
  same MY) — proving correctness on real data.
- A working **gap-closure list** with a quantified improvement opportunity on the ASES-scored measures.
- A clear-eyed **effort estimate** for the full production build (all measures + certification).

## Risks / notes
- **Data mapping is the real work**, not the engine — expect the extract quality and code-set mapping
  to drive the timeline (and to need FMHP data-team collaboration).
- **Certification gates go-live** — matching rates in the pilot is necessary but not sufficient to
  *report*; plan the certification track in parallel.
- **Start focused** — keep the pilot small and fixed-scope, prove value on the wedge measures first,
  then expand to the full measure set and production.
