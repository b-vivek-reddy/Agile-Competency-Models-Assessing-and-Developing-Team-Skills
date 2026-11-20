# Agile-Competency-Models-Assessing-and-Developing-Team-Skills
IEEE Research Paper on Agile Competency Models: Assessing and  Developing Team Skills


> A conceptual term paper proposing the **Agile Competency Model (ACM)**, a team-level framework for assessing and developing the skills agile teams need.

**Author:** Bujunuri Vivek <br>
**Affiliation:** School of Computer Science and Engineering, Lovely Professional University, Phagwara, India <br>
**Contact:** vivekreddy8541@gmail.com<br>
**Overleaf:** [agile_competency_model_IEEE_paper_vivek](https://www.overleaf.com/project/6ae6dd2951a7ed93c6899b04/share#24a32d520ce78561b0169a825d56390c3689cded36110e9c)<br>
**Paper:** [`agile_term_paper_vivek.pdf`](./agile_term_paper_vivek.pdf)<br>

**Keywords:** agile software development · competency model · team skills · skill assessment · team development · behavioral software engineering · psychological safety

---

## Overview

Agile practices are everywhere, but many teams still can't say which skills they need, how to check that those skills exist, or how to grow them deliberately.

- **Certification** checks that people know the terminology.
- **Maturity models** record which practices have been adopted.
- Neither captures the *behaviors* through which agile teams create value.

The ACM fills this gap with a behavior-focused model that treats the **team** as the unit of analysis and comes with a practical way to assess and develop it.

> **Status:** The ACM is a **conceptual proposal, not a validated instrument.** It was built from a synthesis of the agile, teamwork, competence, and psychometric literatures. No real team has used it yet. The paper provides a staged plan for validating it.

## Research Questions

| # | Question |
|---|----------|
| RQ1 | Which competency dimensions and proficiency levels can describe agile team capability in observable terms? |
| RQ2 | How can evidence for these competencies be gathered and combined while limiting bias and misuse? |
| RQ3 | How can assessment results be turned into team-owned development actions that fit routines agile teams already have? |

## Contributions

1. The **ACM**: six dimensions in three clusters, with four proficiency levels.
2. An **evidence-weighted assessment procedure** with team-profile measures that expose coverage gaps and single points of expertise.
3. A **four-step development cycle** built on retrospectives, pairing, and communities of practice.
4. A **worked example** and a **staged validation plan**.

---

## The Model

### Design principles

Behavioral · Team-centric · Framework-neutral · Developmental (not for appraisal) · Parsimonious (workable in a single workshop)

### Six dimensions in three clusters

| Cluster | Dimension | Focus |
|---------|-----------|-------|
| **Craft** | D1 Engineering craft | Test automation, refactoring, code review, technical debt |
| | D2 Delivery flow and quality | Small batches, CI/CD, definition of done, production feedback |
| **Collaboration** | D3 Communication and coordination | Information sharing, cross-role communication, dependencies, conflict handling |
| | D4 Shared leadership and ownership | Collective ownership, shared decisions, backup behavior, mentoring |
| **Direction** | D5 Value and customer insight | User feedback, value-based prioritization, outcome goals, experimentation |
| | D6 Learning and adaptation | Retro follow-through, small experiments, knowledge sharing, responding to change |

Each dimension has **4 competencies (24 in total)**. Some are *individual* (rated per member, e.g. test automation) and some are *collective* (rated once for the team, e.g. definition of done), which avoids averaging individual scores to describe a group property.

### Four proficiency levels

| Level | Name | Description |
|-------|------|-------------|
| L1 | Emerging | Occasional, usually prompted; relies on individual initiative |
| L2 | Consistent | Regular and unprompted in routine situations |
| L3 | Adaptive | Tailored to context; handles exceptions; helps others |
| L4 | Influential | Shapes practice beyond the team: norms, tools, or training |

Levels describe consistency and reach, **not seniority**. Every competency gets behaviorally anchored descriptors at each level.

---

## Assessment Framework

### Four evidence sources

| Source | Contributes | Main bias | Default weight |
|--------|-------------|-----------|----------------|
| Self-rating | Intent and context | Over/under-rating | 0.15 |
| Peer rating | Day-to-day view | Friendship effects, fear | 0.30 |
| Artifact indicators | Traces of work | Gaming, context | 0.30 |
| Observation / retrospectives | Behavior in events | Observer effect | 0.25 |

### Combining evidence

For member *i* and competency *c*, the provisional level is a weighted mean over available sources:

```
L̂_ic = Σ(w_s · r_ics) / Σ(w_s)
```

Self–peer divergence `Δ = r_self − r_peer` is flagged for discussion when `|Δ| ≥ 1`.
This estimate is only a **starting point**; the final level is agreed in a facilitated **~90-minute calibration session**.

### Team profile measures (per dimension)

Each member's dimension level is the **lower median** of their calibrated competency levels.

| Measure | Meaning |
|---------|---------|
| **Coverage** `C_d` | Fraction of members at L2 or above |
| **Depth** `D_d` | Fraction of members at L3 or above |
| **Redundancy** `E_d` | Count of members at L3 or above |

**Flags (working values, to be tuned in pilots):**
- `E_d ≤ 1` → single point of expertise
- `C_d < 0.75` → needs attention

### Governance and ethics

- The team owns its profile.
- Individual ratings are visible only to the facilitator and the member concerned.
- Profiles stay separate from performance appraisal and compensation.
- Reassess on a fixed cadence (every 3–6 months).
- Introduce assessment only where psychological safety exists or is being built.

---

## Development Cycle

1. **Prioritize**: the team picks one or two dimensions to improve.
2. **Choose interventions**: activities just beyond current ability, with task-focused feedback (e.g. pairing/mobbing, WIP limits, rotating facilitators, story mapping, experiment backlog).
3. **Embed in the workflow**: learning actions go on the backlog with protected capacity (starting point: 10–15%).
4. **Reassess**: after 1–2 quarters, revisit only the targeted competencies.

---

## Worked Example (Illustrative, Invented Data)

A hypothetical six-person team with several recent failed releases produced this profile:

| Dim. | L1 | L2 | L3 | L4 | C_d | D_d | Flag |
|------|----|----|----|----|-----|-----|------|
| D1 | 1 | 3 | 2 | 0 | 0.83 | 0.33 | – |
| D2 | 2 | 3 | 1 | 0 | 0.67 | 0.17 | E ≤ 1, C < 0.75 |
| D3 | 0 | 2 | 3 | 1 | 1.00 | 0.67 | – |
| D4 | 3 | 2 | 1 | 0 | 0.50 | 0.17 | E ≤ 1, C < 0.75 |
| D5 | 2 | 2 | 2 | 0 | 0.67 | 0.33 | C < 0.75 |
| D6 | 1 | 2 | 2 | 1 | 0.83 | 0.50 | – |

**Decision:** The team targets **D2** (WIP limits, fortnightly pipeline review) and **D4** (rotating release lead, cross-training pairs), with **D5** as a candidate for the next cycle. The behavioral outcome: *"any two members can run a release without outside help."*

---

## Validation Plan

| Stage | Method | Statistic |
|-------|--------|-----------|
| Content | Delphi panel of coaches and practitioners | Lawshe's CVR per item |
| Reliability | Questionnaire pilot; paired raters | Cronbach's α, ICC, weighted κ |
| Structure | Exploratory then confirmatory factor analysis | Fit indices, loadings |
| Criterion | Relate profiles to delivery metrics and team-effectiveness scales | Multilevel regression |
| Consequences | Longitudinal action research | Profile change, team experience |

## Limitations and Threats to Validity

- **Conceptual status:** untested on real teams; dimensions are not claimed to be exhaustive or independent.
- **Rating bias:** self-rating inflation, peer friendship effects, common-method variance.
- **Metric gaming:** artifact indicators are evidence for discussion, never scores.
- **Small samples:** `C_d`, `D_d`, `E_d` jump in large steps in teams of 5–9; they are descriptive only.
- **Context and culture:** indicators may need adapting (distributed teams, safety-critical domains).
- **Misuse:** the biggest risk is using profiles for appraisal, which would destroy candor.

## Future Work

- Expert review of the competency set
- Questionnaire development and psychometric testing
- Pilots with industrial and student teams to calibrate weights and thresholds
- Tooling that derives profiles from repository and delivery data
- Longitudinal studies linking competency growth to team performance and well-being
- Cross-team competencies for scaled agile settings

---

## Citation

```bibtex
@misc{vivek_acm,
  author = {Bujunuri Vivek},
  title  = {Agile Competency Models: Assessing and Developing Team Skills},
  note   = {IEEE research paper, School of Computer Science and Engineering, Lovely Professional University}
}
```

## License

*Add a license of your choice (e.g. CC BY 4.0 for the paper) here.*
