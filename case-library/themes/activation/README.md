# Activation

> Activation is the first reliable evidence that a new user has received meaningful product value. It is a behavioral hypothesis that must predict later value, not the completion of signup or onboarding.

**[English](README.md)｜[简体中文](README.zh.md)**

## Definition and Boundaries

Activation answers a specific question: **has this new user experienced enough value to make continued use more likely?** The answer usually requires an observable value event, a time window, and evidence that the event is associated with downstream retention or another durable outcome.

Activation is related to, but different from:

| Concept | What it measures | Why it is not activation by itself |
| --- | --- | --- |
| Signup | Account creation or entry | Access does not prove value was received. |
| Onboarding completion | Progress through a designed flow | A user can finish the interface without reaching a useful outcome. |
| Engagement | Frequency or volume of activity | Activity can be shallow, accidental, or disconnected from value. |
| Retention | Continued value over time | Retention validates activation but occurs later in the journey. |

There is no universal activation event. A collaboration product may require a useful artifact and another participant; a consumer utility may activate when it completes one important job; a marketplace must consider value on both sides.

## Activation Model

Activation can be analyzed as four connected stages rather than one binary event.

| Stage | Question | Evidence | Typical failure |
| --- | --- | --- | --- |
| **1. User intent** | What job brought the user here? | Entry source, stated use case, role, imported context | The product sends different intents through one generic path. |
| **2. First value** | Did the user complete a meaningful job? | A successful value event, not an interface event | The flow optimizes setup steps instead of customer outcomes. |
| **3. Value reinforcement** | Did the user deepen, repeat, or share the value? | A second use, richer output, collaboration, saved state | The first success is isolated and creates no reason to return. |
| **4. Retention validation** | Does the proposed activation event predict durable value? | Cohort retention, expansion, or repeated job completion | A convenient early event is mistaken for a causal milestone. |

The model does not require every product to expose four separate screens or events. It requires the measurement system to distinguish acquisition intent, first success, reinforcement, and downstream validation.

## Metric Tree

A single activation rate cannot explain why users succeed or fail. Use a metric tree in which each layer answers a different decision question.

```text
Durable customer value
└── Retained activation
    ├── Activation outcome
    │   ├── Activation rate
    │   └── Time to first value
    ├── Process diagnostics
    │   ├── Step conversion
    │   ├── Abandonment point
    │   └── Time between steps
    ├── Activation quality
    │   ├── Value depth / breadth
    │   ├── Repeat value
    │   └── Collaboration or downstream use
    └── Guardrails
        ├── Errors and failed jobs
        ├── Support burden
        └── Retention, trust, and economic impact
```

- **Outcome metrics** show whether users reached the proposed value milestone.
- **Process metrics** locate friction but do not prove value.
- **Quality metrics** distinguish superficial completion from meaningful success.
- **Guardrails** prevent a local conversion gain from damaging trust, product quality, retention, or economics.

## Metric Dictionary

Before publishing any activation metric, define the eligible population, starting event, qualifying value event, observation window, exclusions, and owner. Changing any of these creates a different metric.

| Metric | Definition and formula | Window and useful cuts | Interpretation |
| --- | --- | --- | --- |
| **Activation rate** | `users completing the value event within W / eligible new users starting in the cohort` | First session, 24 hours, 7 days; source, intent, use case, role, device, market | Primary outcome. The denominator must not silently exclude users who encountered friction. |
| **Time to first value (TTFV)** | `timestamp of first value event - activation start timestamp`; report median and percentiles | Same cohort horizon as activation; intent, source, device, product complexity | A faster result is useful only when the event represents real value. A median alone can hide a long tail. |
| **Step conversion** | `users completing step n / users eligible for step n` | Per session and cohort; path, device, experiment variant | Diagnostic measure. High flow completion can coexist with weak activation. |
| **Step abandonment** | `eligible users who stop before step n+1 / users reaching step n` | Session timeout plus a defined return window; path and error state | Identifies where progress stops, not why. Combine with errors, qualitative evidence, and intent. |
| **Retained activation** | `activated users repeating the value event in period R / activated users eligible to return` | Match product frequency: day, week, or month; activation path and cohort | Quality outcome. The return period should reflect the natural usage cycle. |
| **Activation-to-retention lift** | `retention rate of activated users - retention rate of comparable non-activated users` | Fixed retention horizon; compare within source, intent, and cohort | Validates predictive usefulness, not causality. Selection effects require experiments or stronger causal designs. |
| **Value depth / breadth** | Product-specific amount or range of value after first success, such as useful objects, completed jobs, features serving the same job, or collaborators | Early window plus downstream cohort; use case and account type | Quality diagnostic. More activity is not automatically more value. |
| **Error rate** | `failed attempts / total attempts at the relevant job` | By step, platform, integration, locale, and version | Guardrail and diagnostic. Define whether retries count as attempts. |
| **Support burden** | `activation-related contacts or assisted sessions / eligible new users` | Cohort and release window; issue type and segment | A conversion gain that requires disproportionate human support may not scale. |

### Worked Example

Suppose 1,000 eligible new workspaces begin during one week. Within seven days, 420 create a useful project and complete the first target workflow:

```text
7-day activation rate = 420 / 1,000 = 42%
```

If 210 of those 420 repeat the workflow in week four, retained activation is:

```text
week-4 retained activation = 210 / 420 = 50%
```

These numbers are not benchmarks. They become useful only when compared across cohorts and segments, and when the value event has been validated against durable customer outcomes.

## Segmentation and Cohort Analysis

Aggregate activation often changes because the user mix changed, not because the product improved. Start with acquisition cohorts and split only on dimensions that can change interpretation or action:

| Dimension | Question it helps answer |
| --- | --- |
| Source or campaign | Did expectations set before entry match the product experience? |
| Intent or use case | Are users with different jobs being forced through the same path? |
| Role or account type | Does the person activating have authority, data, or collaborators required for value? |
| Device, platform, or version | Is friction caused by the experience or technical reliability? |
| Market, language, or locale | Do content, integrations, and value assumptions transfer? |
| New vs. invited or returning user | Are fundamentally different starting contexts mixed together? |

Compare cohorts on the same eligibility rules and maturity window. A seven-day activation rate should not compare a fully matured cohort with users acquired yesterday. Report both absolute volume and rate so that a small high-performing segment does not dominate the narrative.

## Diagnosing Activation Problems

Observed patterns narrow the search; they do not establish root cause. Each pattern should lead to a specific check and next action.

| Observed pattern | Plausible questions | Check next | Possible action |
| --- | --- | --- | --- |
| High signup, low first-step start | Expectation mismatch, unclear entry point, missing prerequisites | Source-by-intent cohorts, entry-page behavior, short user interviews | Align acquisition promise, prefill context, or route by intent. |
| High onboarding completion, low value-event completion | Flow rewards interface completion rather than the user job | Compare wizard steps with successful retained-user paths | Remove nonessential setup and bring the value-producing action forward. |
| Strong first value, slow TTFV | Too many dependencies, imports, permissions, or decisions | TTFV percentiles by step, role, platform, and error | Use templates, progressive setup, defaults, or asynchronous preparation. |
| High activation, low retained activation | Weak activation definition, low-quality success, no repeated value | Retention by activation depth, interviews, repeat-job behavior | Raise or redefine the value threshold and design reinforcement. |
| Strong aggregate rate, weak key segment | Mix shift or a path that serves only the dominant use case | Segment by source, intent, role, market, and device | Build a distinct path only when needs and product behavior differ. |
| Improved conversion, rising errors or support | Friction was hidden or shifted downstream | Error taxonomy, support contacts, cancellations, trust signals | Roll back, constrain exposure, or redesign with guardrails. |

## Experiment and Validation Method

1. **State the value hypothesis.** Describe the customer job and the behavior that signals meaningful completion.
2. **Fix the measurement contract.** Record eligibility, numerator, denominator, start event, window, exclusions, segments, and guardrails before reading results.
3. **Validate prediction.** Compare mature cohorts to test whether the event precedes stronger retention, repeated value, expansion, or another durable outcome.
4. **Locate the constraint.** Use process metrics and qualitative evidence to identify where and why the value path breaks.
5. **Change one mechanism.** Test a clearer promise, reduced prerequisite, template, default, guided action, or reinforcement mechanism tied to the diagnosis.
6. **Read the full tree.** Evaluate activation, quality, retained activation, errors, support, trust, and economic guardrails together.
7. **Revalidate over time.** Product changes and acquisition mix can weaken an activation definition that once predicted retention.

An A/B test can estimate the effect of an intervention, but it does not rescue a weak value definition. Conversely, a strong observational relationship between an early event and retention may be predictive while still reflecting user selection rather than causal impact.

## Cross-Company Evidence

| Company or person | Activation lens | What transfers | Boundary |
| --- | --- | --- | --- |
| [Airtable](../../companies/airtable/README.md) | Segmented onboarding, templates, first useful workflows, and later collaboration signals | Connect the entry path to user intent and validate early success against downstream team behavior | Workflow complexity and collaborative adoption differ from simpler or single-player products. |
| [Facebook / Meta](../../companies/facebook/README.md) | Friend connections and the Magic Moment as hypotheses for early network value | Search for an observable behavior that represents the product's core value and test it against retention | A connection threshold from a social network is not a universal activation rule. |
| [Sean Ellis](../../people/sean-ellis/README.md) | Must-have value, Aha Moments, and activation as the bridge from acquisition to retention | Learn from retained users, define value before optimizing the funnel, and prioritize the largest constraint | Interview language and correlation need behavioral and cohort validation. |

The shared pattern is not a specific event. It is the sequence of defining customer value, observing an early proxy, reducing the constraint, and validating the proxy against durable behavior.

## Operating Method

Use this compact specification for each product or meaningful use case:

```text
User and intent:
Customer job:
Eligible population:
Activation start event:
First-value event:
Observation window:
Value-reinforcement signal:
Retention-validation horizon:
Primary segments:
Quality metrics:
Guardrails:
Decision owner:
Current evidence and confidence:
```

Review the specification whenever the product, target customer, acquisition mix, or natural usage frequency changes. If one activation definition cannot explain materially different jobs, keep separate definitions instead of averaging incompatible paths.

## What Not to Copy Directly

- Do not copy another product's Aha Moment, event threshold, or time window.
- Do not promote signup, wizard completion, tooltip dismissal, or an invitation sent to activation without evidence of received value.
- Do not optimize activation rate while ignoring retained activation, errors, trust, support, or unit economics.
- Do not interpret activation-to-retention correlation as causal proof without accounting for selection and confounding.
- Do not add segments that produce interesting charts but no different decision or product path.

## Evidence and Limits

- Company evidence relies mainly on participant interviews and public material, not complete internal causal evaluation.
- Activation events and thresholds are product-, segment-, and time-dependent hypotheses.
- Company scale, market, product frequency, regulation, and data capability limit direct transfer.
- Publisher growth, revenue, valuation, customer-count, and user-count claims are not used to prove individual methods.
