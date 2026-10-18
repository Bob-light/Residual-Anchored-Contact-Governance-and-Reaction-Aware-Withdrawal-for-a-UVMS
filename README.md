# UVMS Research Concepts

[中文版](README.zh-CN.md) | English

A documentation-only companion for research on underwater vehicle–manipulator systems (UVMS). It presents the research motivation, conceptual comparisons, and non-core workflow pseudocode.

## Public scope

This directory contains written explanations and comment-only pseudocode. No experimental or simulated observations, result summaries, performance figures, raw trajectories, sample datasets, trained artifacts, exact inputs, or parameter configurations are supplied. The private simulator and control implementations remain outside this release.

The associated research concerns numerical simulation. This companion supplies no empirical evidence or claim of hardware validation, guaranteed recovery, or superiority of a method.

## Research ideas

Contact operation couples end-effector loading, vehicle motion, arm reaction, and actuation limits. The research considers how locally updated contact governance and coordinated withdrawal can be studied within a common evaluation framework. Only the problem and overall design logic are described; controller equations, gains, tuning rules, platform calibration, and implementation details are not supplied.

| Conceptual policy | Role in the comparison |
| --- | --- |
| Static | Fixed contact governance with an original withdrawal strategy |
| Recovery | Fixed contact governance with revised withdrawal coordination |
| Proposed | Locally updated contact governance with revised withdrawal coordination |

Recovery versus Static is intended to examine withdrawal coordination. Proposed versus Recovery is intended to examine governance while holding withdrawal coordination fixed. These are comparison definitions, not reported experimental findings.

## Directory guide

```text
README.md                       English introduction
README.zh-CN.md                 Chinese introduction
docs/METHODS.md                 Conceptual research and comparison logic
analysis/plot_results.py        Generic analysis and plotting pseudocode
examples/contact_demo.py        Generic contact-teaching pseudocode
tests/check_release.py          Documentation-release review pseudocode
RELEASE_CHECKS.md               Scope of the local inspection
RIGHTS.md                       Licensing status
```

Start with [METHODS.md](docs/METHODS.md), then read the pseudocode files. The `.py` extensions are retained for navigation; every nonblank line is a comment. These files have no imports, executable statements, numerical model constants, or entry points. There is no installation step, executable example, plotting program, or public automated checker.

The analysis outline concerns observations a reader might obtain independently; none are included here. The contact outline is a generic teaching concept and is not an implementation or validation of the private UVMS method. Anyone wishing to execute these outlines must independently supply an implementation and any required inputs.

## Availability and rights

This release is limited to concepts and pseudocode. It does not provide a dataset, complete reproduction package, or request-based access service. No repository identifier or publication status is claimed.

No reuse license has been selected; see [RIGHTS.md](RIGHTS.md). Author identities, email addresses, institutional logos, manuscript drafts, third-party full texts, and private working materials are omitted. Any future addition must be reviewed against this documentation-only scope before upload.
