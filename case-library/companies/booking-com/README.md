# Booking.com

> An experimentation-system case centered on decentralized product decisions, self-service infrastructure, shared methodology, parallel tests, and organizational learning.

**[English](README.md)｜[简体中文](README.zh.md)**

## Growth Context

Booking.com developed online experimentation as a broad product-development capability rather than a centralized analytics service. Lukas Vermeer describes responsibility spanning infrastructure and tools, methodology and metrics, training, and culture.

The case demonstrates how an organization can increase decision throughput while maintaining common quality controls. Public talks do not establish the incremental business impact of the experimentation system or document every current Booking.com practice.

## Decentralized Experimentation System

```text
Product team owns customer problem and hypothesis
-> shared platform manages assignment, exposure, and analysis
-> shared methods and metrics protect comparability
-> training enables local judgment
-> evidence changes the product decision
-> documentation becomes reusable organizational learning
```

Decentralization is not the absence of standards. The system separates reusable controls from decisions that remain close to product context.

| Layer | Reusable capability | Failure to avoid |
| --- | --- | --- |
| Infrastructure | Assignment, exposure, event data, analysis, and diagnostics | Every team creates incompatible pipelines |
| Methodology | Design standards, uncertainty, quality checks, and interpretation | Self-service produces confident but invalid conclusions |
| Metrics | Shared definitions, outcome metrics, diagnostics, and guardrails | Teams choose favorable measures after seeing results |
| Training | Practical competence across product and technical roles | Knowledge remains concentrated in specialists |
| Culture | Permission to challenge intuition and stop weak ideas | Experiments become confirmation theater |

## Concurrent Experiments

High experiment throughput requires some tests to overlap. Blanket mutual exclusion protects against hypothetical interactions by imposing a certain capacity cost.

| Situation | Response |
| --- | --- |
| Independent mechanisms and surfaces | Allow overlap and retain exposure records |
| Shared page or scarce resource | Assess conflict and monitor important combinations |
| Treatments directly invalidate each other | Use mutual exclusion or a combined design |
| Unexpected heterogeneous result | Check concurrent exposure and plausible interaction mechanisms |
| High-risk or irreversible consequence | Apply stronger isolation and review |

Interaction analysis should follow a plausible mechanism and decision consequence. Searching every treatment combination can create its own multiple-testing and interpretation problems.

## Growth Infrastructure Lessons

- Make the standard trustworthy workflow self-service.
- Centralize reusable platform reliability and metric governance, not every product decision.
- Build automation after recurring work and failure modes are visible.
- Preserve assignment, exposure, analysis, and decision documentation so results remain auditable.
- Measure whether evidence changes decisions, not only how many tests launch.
- Develop infrastructure, methodology, training, and culture as one system.

## Transfer Boundaries

- Small organizations may lack the traffic or experiment volume that justifies Booking.com-scale infrastructure.
- Decentralization requires sufficient statistical and product judgment in local teams.
- Marketplace interference, repeated exposure, seasonality, and shared inventory can require designs beyond individual randomization.
- High experiment velocity cannot compensate for weak strategy, customer understanding, or product value.
- The appropriate level of platform investment depends on current constraints, not another company's scale.

## Related Themes and People

- [Experimentation](../../themes/experimentation/README.md)
- [Growth Infrastructure](../../themes/growth-infrastructure/README.md)
- [Metrics & Measurement](../../themes/metrics-and-measurement/README.md)
- [Growth Organization](../../themes/growth-organization/README.md)
- [Lukas Vermeer](../../people/lukas-vermeer/README.md)
- [Ronny Kohavi](../../people/ronny-kohavi/README.md)

## Sources

1. Lukas Vermeer, [Online Experiments at Booking.com](https://www.youtube.com/watch?v=4e_rBd96iGA).
2. Lukas Vermeer, [Democratizing Online Experiments at Booking.com](https://www.youtube.com/watch?v=r57gd8CRxDA).
3. Lukas Vermeer, [Democratizing Online Controlled Experiments at Booking.com](https://www.youtube.com/watch?v=z81SxsmSfFo).
4. Lukas Vermeer et al., [A/B Testing at Scale: Accelerating Software Innovation](https://www.youtube.com/watch?v=RoJ_s7Bb4qM).
5. Lukas Vermeer, [Running Many Tests at Once: Interaction Avoidance and Detection](https://www.youtube.com/watch?v=J6gVJcvfr2Q).

## Evidence and Limits

- The case is based on public conference talks and interviews, not internal platform documentation or an independent causal evaluation.
- Talks from different dates may describe different stages of the system.
- No precise incremental revenue, conversion, retention, or innovation effect is claimed.
- Booking.com's results also reflect its product, marketplace, brand, operations, strategy, capital, timing, and teams.
