# Alpine Quality — Documentation for First Medical Health Plan

A curated documentation set for First Medical Health Plan (Plan Vital / Medicaid),
covering the Alpine Quality digital HEDIS® measurement and quality-operations platform.

> **Data note:** The live demo runs entirely on **synthetic data — no PHI**. Real member
> data enters only at the pilot stage, under a signed BAA and a HIPAA-compliant environment
> (see the Pilot Prerequisites document below).

---

## Live application

The operational tooling and audit documentation are best viewed in the running app:

**🔗 https://alpine-quality.vercel.app**  · demo login `qdirector` / `alpine2026`

Inside the app:
- **SOP Library** — 12 Standard Operating Procedures, one for every operational process
  (data ingestion, validation, measure calculation & certification, care-gap closure,
  member outreach, chart chase/MRRV, supplemental data & PSV, submission, access control,
  audit review, regulatory updates, audit response). Each cites its regulatory basis and is
  printable.
- **NCQA Audit Binder** — the audit documentation package assembled live from system data:
  IS Standards 1–7 evidence, SOP index, measure-certification results, and compliance posture.
  One-click Print/PDF.
- **Regulatory Monitor** — tracks new NCQA/CMS/ASES changes with impact assessments and a
  compliance calendar.
- **User Guide** — step-by-step instructions for daily and administrative users.

---

## Documents in this folder

| Document | What it covers |
|---|---|
| [FMHP Compliance Obligations](FMHP_Compliance_Obligations.md) | One-page summary of First Medical's binding HEDIS/quality reporting obligations, cadence, financial exposure (HCIP withhold), and audit/certification requirements. |
| [PR HEDIS Requirements Library](PR_HEDIS_Requirements_Library.md) | The laws, regulations, and NCQA specifications that govern HEDIS reporting for Plan Vital, with authoritative source links. |
| [Pilot Prerequisites & Plan](Pilot_Prerequisites_and_Plan.md) | The concrete next step after the demo: prerequisites (BAA, NCQA license, data extract), scope, plan, and success criteria for running First Medical's real data through a focused measure set. |

## One-page summary

- [presentation/leave-behind.html](presentation/leave-behind.html) — a printable one-page
  overview of Alpine Quality (open in any browser, print to PDF).

---

*Alpine Quality · Digital HEDIS engine for Plan Vital / Medicaid. HEDIS® is a registered
trademark of NCQA.*
