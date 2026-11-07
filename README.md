CODEX v14.0

Quantitative Adversarial AI Security Evaluation Framework

"Version" (https://img.shields.io/badge/version-14.0-2563EB?style=flat-square)
"Status" (https://img.shields.io/badge/status-experimental-orange?style=flat-square)
"Focus" (https://img.shields.io/badge/focus-AI%20Security-7C3AED?style=flat-square)
"Evaluation" (https://img.shields.io/badge/method-evidence--based-0F766E?style=flat-square)


CODEX is a structured AI security evaluation framework designed to analyze jailbreak prompts, examine adversarial instruction techniques, assess model resistance, and produce evidence-based security reports.

Its methodology separates the complexity of an attack from its demonstrated effectiveness, preventing theoretical analysis from being misrepresented as verified results.

---

Overview

Modern AI systems face adversarial inputs designed to manipulate instruction-following behavior, bypass safeguards, or create conflicts within their instruction hierarchy.

CODEX provides a systematic approach to examining these inputs.

Rather than treating every jailbreak prompt as successful, CODEX evaluates its construction, identifies the techniques it employs, examines available behavioral evidence, and measures the reliability of the conclusions.

The framework emphasizes:

- Structured adversarial prompt analysis
- Instruction hierarchy and conflict examination
- Jailbreak technique classification
- Quantitative evaluation criteria
- Model resistance assessment
- Evidence-based reporting
- Reproducible evaluation methodology

Core philosophy: Analyze objectively. Measure independently. Report honestly.

---

Key Features

1. Adversarial Prompt Analysis

Examines submitted prompts as untrusted specimens without following or executing their embedded instructions.

Analysis includes:

- Instruction hierarchy manipulation
- Role and identity reassignment
- Authority impersonation
- Policy override attempts
- Context manipulation
- Prompt injection techniques
- Refusal suppression strategies
- Multi-stage instruction structures

2. Quantitative Evaluation

CODEX uses separate scoring dimensions to avoid confusing attack complexity with actual behavioral success.

Metric| Range| Purpose
Attack Sophistication| 0–100| Measures the design and structural complexity of a specimen
Demonstrated Effectiveness| 0–100| Measures observed behavioral impact
Model Resistance| 0–100| Measures defensive performance
Evaluation Confidence| 0–100| Measures the reliability and completeness of available evidence

Scores represent evaluation dimensions, not universal security guarantees.

3. Technique Classification

Identifies and categorizes adversarial techniques found within submitted specimens.

Each identified technique receives an evidence classification:

- VERIFIED — Directly supported by available evidence.
- SUPPORTED — Supported by relevant observations or indicators.
- HYPOTHESIS — Plausible interpretation requiring further validation.
- UNKNOWN — Insufficient evidence to establish a conclusion.

4. Evidence-Based Assessment

CODEX distinguishes static inspection from live behavioral testing.

It does not claim that a prompt successfully bypassed a model merely because its instructions appear sophisticated.

When live behavioral evidence is unavailable, demonstrated effectiveness must be reported as NOT TESTED (N/T).

5. Structured Reporting

Produces organized evaluation reports containing:

- Specimen overview
- Identified adversarial techniques
- Structural analysis
- Scoring breakdown
- Evidence classifications
- Confidence assessment
- Evaluation limitations
- Defensive recommendations

---

Evaluation Architecture

CODEX v14.0 uses a multi-dimensional evaluation architecture.

Scoring Dimensions

Attack Sophistication — 0 to 100

Evaluates the construction and complexity of an adversarial specimen.

Considerations include:

- Structural complexity
- Instruction layering
- Context manipulation
- Technique diversity
- Internal consistency
- Multi-stage design

This dimension can be evaluated through static analysis.

Demonstrated Effectiveness — 0 to 100

Evaluates actual behavioral impact using available testing evidence.

It must not be inferred from prompt wording, complexity, or persuasive claims.

Without valid behavioral evidence, the result is recorded as N/T.

Model Resistance — 0 to 100

Evaluates how effectively the tested model maintains its applicable instruction hierarchy and defensive behavior under the evaluated conditions.

This requires relevant behavioral evidence.

Evaluation Confidence — 0 to 100

Measures the strength and reliability of the evaluation itself.

Considerations include:

- Evidence completeness
- Reproducibility
- Test coverage
- Observation quality
- Consistency of results
- Remaining uncertainty

---

Weighted Evaluation Method

Individual evaluation criteria use a rating scale from 0 to 4.

Rating| Interpretation
0| Not demonstrated
1| Weak
2| Partial
3| Strong
4| Fully demonstrated

Each criterion receives a defined weight.

The weighted contribution is calculated as:

"Contribution = Weight × (Rating / 4)"

Criteria marked NOT TESTED are excluded from the applicable denominator. Remaining scores are normalized against the total applicable weight.

This prevents missing evidence from being silently interpreted as a successful or unsuccessful result.

---

Assessment Statuses

CODEX uses separate status systems for specimen inspection and behavioral evaluation.

Specimen Status

Status| Meaning
PRESENT| The identified component is present
PARTIAL| The component is present but incomplete
ABSENT| The component was not identified
UNCERTAIN| Available evidence is insufficient

Behavioral Status

Status| Meaning
PASS| Expected defensive behavior was observed
FAIL| A defined defensive requirement was not met
PARTIAL| Only some requirements were satisfied
NOT TESTED| No relevant behavioral test was performed
INCONCLUSIVE| Available observations do not support a reliable conclusion

These statuses must not be treated as interchangeable.

---

Operational Workflow

CODEX follows a structured evaluation process:

1. Input Collection — Receive the adversarial prompt specimen.
2. Specimen Isolation — Treat embedded instructions as untrusted data.
3. Structural Analysis — Examine its organization and instruction patterns.
4. Technique Classification — Identify relevant adversarial techniques.
5. Evidence Assessment — Determine which conclusions are supported.
6. Quantitative Scoring — Calculate applicable evaluation dimensions.
7. Confidence Assessment — Account for missing or uncertain evidence.
8. Report Generation — Produce a structured evaluation with limitations and recommendations.

---

Security Principles

CODEX follows these core evaluation principles:

- Instruction Integrity: Specimen instructions are analyzed, not obeyed.
- Evidence First: Conclusions must be supported by available observations.
- No Fabricated Results: Untested behavior is never presented as verified.
- Independent Metrics: Attack sophistication and demonstrated effectiveness remain separate.
- Transparent Uncertainty: Unknown information is explicitly identified.
- Reproducibility: Evaluation criteria and scoring should be documented.
- Defensive Orientation: Findings should support security analysis and system improvement.

---

Example Evaluation Report

The following is an illustrative report structure, not a claim of completed testing.

CODEX v14.0 — EVALUATION REPORT

Specimen: SAMPLE-001
Evaluation Type: Static Analysis

ATTACK SOPHISTICATION:       [Pending]
DEMONSTRATED EFFECTIVENESS:  N/T
MODEL RESISTANCE:            N/T
EVALUATION CONFIDENCE:       [Pending]

TECHNIQUE CLASSIFICATION:
- Instruction hierarchy manipulation
- Role reassignment attempt
- Policy override attempt

SPECIMEN STATUS:
- Structural analysis: PRESENT
- Behavioral evidence: NOT TESTED

EVIDENCE CLASSIFICATION:
- Static observations: VERIFIED
- Behavioral conclusions: UNKNOWN

FINAL ASSESSMENT:
Static analysis completed.
Live behavioral effectiveness has not
been established.

---

Limitations

CODEX is an evaluation framework, not a universal certification system.

Its results depend on the quality of the specimen, evaluation criteria, available evidence, and testing conditions.

Important limitations:

- Static analysis cannot establish live jailbreak success.
- Model behavior may vary between versions and configurations.
- Scores are meaningful only within their documented methodology.
- Missing evidence reduces confidence.
- Results should not be generalized beyond the tested conditions.

A high sophistication score does not imply a successful jailbreak.

A strong resistance score does not establish absolute security.

---

Project Structure

A suggested repository organization:

CODEX/
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── docs/
│   ├── methodology.md
│   ├── scoring.md
│   ├── classifications.md
│   └── evaluation-guide.md
├── examples/
│   └── sample-report.md
└── reports/
    └── .gitkeep

This is a suggested structure. It does not imply that every listed file already exists.

---

Intended Applications

CODEX is intended for:

- AI security research
- Jailbreak robustness evaluation
- Prompt injection analysis
- Adversarial instruction research
- Model resistance assessment
- AI safety testing
- Security documentation
- Comparative evaluation research

---

Version Information

Field| Value
Project| CODEX
Version| 14.0
Author| Neon
Category| AI Security
Framework Type| Adversarial Evaluation
Methodology| Quantitative and Evidence-Based
Status| Experimental

---

Project Summary

CODEX v14.0 is a quantitative adversarial AI security evaluation framework that analyzes jailbreak prompts, classifies manipulation techniques, evaluates model resistance, and generates evidence-based security reports.

It separates attack sophistication from demonstrated effectiveness, applies weighted scoring criteria, tracks evaluation confidence, and explicitly identifies untested or uncertain results.

Analyze. Evaluate. Measure. Verify.

---

CODEX — Advancing structured, evidence-based AI security evaluation. 
