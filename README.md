# Yonathan Emmanuel

**Biomedical / analytical scientist · computational health · regulated software & data systems**

I build at the intersection of experimental science, quantitative analysis, biomedical data, and software engineering. This GitHub portfolio is intentionally composed of **non-proprietary reference implementations** that demonstrate how I approach scientific computation, quality systems, reproducibility, validation, and software intended for health or regulated environments.

## Core competency map

| Domain | Evidence |
|---|---|
| Analytical / bioanalytical science | analytical method validation, assay statistics, potency/curve analysis |
| Clinical laboratory quality | statistical QC, rule systems, traceable laboratory data-quality checks |
| Biomedical data engineering | longitudinal health data normalization, provenance, missingness, time-window logic |
| Machine learning | reproducible biomedical ML, leakage controls, deterministic experiments |
| Regulated software / SaMD | requirements traceability, risk controls, verification architecture, lifecycle discipline |
| Swift / health software | typed domain models, protocol-driven adapters, deterministic health-data aggregation |
| Scientific software engineering | tests, CI, packaging, auditability, explicit assumptions and failure modes |

## Flagship public repositories

### Regulated software & computational health
- **[`samd-engineering-reference`](https://github.com/biomir/samd-engineering-reference)**  
  Requirements → risk controls → verification traceability, lifecycle documentation, and automated traceability checks.

- **`swift-health-data-architecture`**  
  Swift package demonstrating domain-layer architecture for health data, deterministic aggregation, testable store abstractions, and an optional HealthKit adapter boundary.

- **`longitudinal-health-data-engineering`**  
  Synthetic wearable/health time-series pipeline covering normalization, provenance, timezone-aware daily aggregation, missingness, and data-quality summaries.

### Analytical / laboratory science
- **[`analytical-method-validation-python`](https://github.com/biomir/analytical-method-validation-python)**  
  Auditable precision, accuracy, linearity, LOD/LOQ, acceptance-rule logic, tests, and CI.

- **`bioanalytical-assay-statistics`**  
  4-parameter logistic assay modeling, EC50 estimation, inverse concentration estimation, fit diagnostics, and synthetic assay examples.

- **[`clinical-lab-qc-python`](https://github.com/biomir/clinical-lab-qc-python)**  
  Statistical QC and Westgard-style rule logic with explicit separation between signal detection and laboratory disposition.

- **`regulated-data-quality-engineering`**  
  Rule-based data quality, immutable audit results, and SQLite-backed QC evidence suitable for traceable regulated-data workflows.

### Biomedical ML
- **[`biomedical-ml-reproducibility`](https://github.com/biomir/biomedical-ml-reproducibility)**  
  Dataset/config hashing, deterministic seeds, manifest generation, leakage-safe example pipelines, and reproducibility checklists.

## Engineering principles

1. **Scientific claims must be traceable to assumptions and evidence.**
2. **Correct calculations are not equivalent to validated intended use.**
3. **Data provenance and failure modes are first-class design concerns.**
4. **Testing should include boundary conditions and misuse, not only nominal paths.**
5. **Regulated engineering is strongest when traceability is generated continuously rather than reconstructed at release.**
6. **Public demonstrations should prove capability without exposing confidential science, patient data, or proprietary implementation.**

## Public portfolio boundary

These repositories contain synthetic examples and generic engineering references. They do **not** contain proprietary BioMIR algorithms, private health data, confidential employer information, unpublished controlled methods, credentials, or regulated production records.

## Current development direction

The portfolio is being expanded toward deeper demonstrations of:

- advanced bioanalytical statistics and assay modeling
- longitudinal health / wearable data engineering
- Swift health-software architecture
- regulated data quality and provenance
- model evaluation, uncertainty, and validation controls
- release engineering, cybersecurity, and software lifecycle evidence

---

**GitHub:** [github.com/biomir](https://github.com/biomir)
