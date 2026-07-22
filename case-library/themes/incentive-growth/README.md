# Incentive System Cases

> Cross-company evidence on monetary rewards, marketplace subsidies, product-aligned referrals, progress protection, gamification, and structural business-model alignment.

**[English](README.md)｜[简体中文](README.zh.md)**

For definitions, economics, incrementality, post-incentive retention, fraud, cannibalization, governance, and diagnosis, see [Incentive Systems](../../../handbook/incentive-growth/README.md).

## Capability Matrix

| Company | Incentive mechanism | Target behavior or alignment | Durability test | Primary risk |
| --- | --- | --- | --- | --- |
| [ByteDance](../../companies/bytedance/README.md) | Cash, coins, coupons, referral rewards, Lite products | Acquisition, repeated activity, referral, and portfolio movement | Retained behavior after rewards and incremental portfolio value | Fraud, contaminated signals, cannibalization, and subsidy dependence |
| [Uber](../../companies/uber/README.md) | Driver and rider incentives, local guarantees, promotions | Build supply, demand, utilization, and local liquidity | Supply, demand, and transaction quality after tapering | Permanent subsidy, local imbalance, weak supplier economics, and adverse selection |
| [Dropbox](../../companies/dropbox/README.md) | Product-capacity reward, including double-sided storage | Qualified referral and deeper product use | Recipient activation, retention, and continued storage value | Low-quality invitations, abuse, serving cost, and organic displacement |
| [Duolingo](../../companies/duolingo/README.md) | Streaks, milestones, status, reminders, and progress recovery | Repeated learning practice and habit continuity | Meaningful practice and return without coercive dependence | Point farming, notification fatigue, loss aversion, and learning-quality drift |
| [Ramp](../../companies/ramp/README.md) | Structural business-model alignment around customer savings | Make company growth credible when customers spend and operate more efficiently | Realized savings, trust, adoption, and durable economics | Alignment claims without measured savings or hidden revenue conflicts |

These cases represent different incentive layers. ByteDance and Uber use transferable economic value; Dropbox grants product value; Duolingo uses behavioral and protective mechanisms; Ramp is a structural alignment case rather than a reward campaign.

## Case 1: ByteDance - Monetary Rewards, Lite Products, and Risk

The ByteDance account separates cash, virtual coins, coupons, referral rewards, and portfolio-wide benefits. These mechanisms have different recipients, costs, withdrawal rules, and behavioral effects.

```text
Segment and target behavior
-> reward eligibility and delivery
-> acquisition, activity, or referral response
-> product value and retained behavior
-> fraud, cannibalization, and margin checks
-> continue, isolate, taper, or stop
```

Lite products make portfolio effects visible. A subsidized version can reach a distinct segment or device constraint, but it can also move existing users from a healthier product without adding value. Rewarded behavior must be labeled so recommendation and personalization systems do not mistake payment-driven activity for natural preference.

**Primary boundary:** internal figures, thresholds, and system descriptions come mainly from a former participant's retrospective account and are not transferable benchmarks.

## Case 2: Uber - Incentives as Temporary Liquidity Coordination

Uber's marketplace case treats incentives as one input to local supply and demand formation. Driver availability, rider demand, utilization, pickup time, fulfillment, participant economics, and retention interact inside a geography and time window.

```text
Local liquidity constraint
-> targeted supply or demand incentive
-> availability and transaction lift
-> participant value and utilization
-> taper incentive
-> retained local liquidity and economics
```

The incentive should target the constrained side and transition rather than maximize aggregate registrations. A market that cannot provide sufficient demand frequency or supplier economics without permanent subsidy may have a structural model problem.

**Primary boundary:** Uber's capital, labor pool, city operations, regulation, scale, and historical incentive levels do not form a universal marketplace launch template.

## Case 3: Dropbox - Product-Aligned Double-Sided Referral

Dropbox's early referral example rewarded additional storage, connecting the benefit directly to the product's core value. The mechanism could reward sender and recipient while allowing the recipient to experience the product rather than receive unrelated cash.

```text
Activated user values storage and synchronization
-> invites a qualified recipient
-> recipient activates and uses the product
-> product capacity is granted
-> both sides continue receiving storage value
```

Product alignment does not remove economic questions. Storage has serving cost, referred users can be low quality, and some recipients would have joined organically. Evaluate recipient activation, retention, reward cost, abuse, and marginal performance at scale.

**Primary boundary:** public referral accounts are simplified and do not provide complete experiment designs, cohort economics, baselines, or counterfactual results.

## Case 4: Duolingo - Progress Protection and Meaningful Habit

Duolingo's streak system combines daily state, visible progress, milestones, reminders, celebration, recovery through Streak Freeze, and paid feature boundaries. The incentive is partly status and partly protection from losing accumulated progress.

```text
Meaningful learning action
-> visible progress and streak state
-> reminder, milestone, or recovery
-> return to learning action
-> learning value and durable habit
```

The transferable mechanism is not the streak count itself. It is the connection between clear progress, limited recovery, repeated product value, and experimentation. Guardrails should cover learning quality, notification fatigue, coercion, and monetizing fear of loss.

**Primary boundary:** Duolingo is a high-frequency learning product with a recognizable brand and large experiment program. The same mechanic may be inappropriate for low-frequency or high-stakes products.

## Case 5: Ramp - Structural Incentive Alignment

Ramp's stated differentiation is to help customers save money and operate finance more efficiently, contrasting with financial models that benefit primarily when customers spend more or carry balances.

This is not a referral reward or customer promotion. It is an incentive-design question at the business-model level:

```text
Customer saves money or operating time
-> product creates measurable value
-> adoption and trust increase
-> company grows through delivered customer outcome
```

The alignment is credible only when pricing, revenue, product behavior, and measurement support the promise. Track realized savings, customer outcomes, margin, retention, and any revenue mechanism that could recreate the conflict.

**Primary boundary:** a stated customer-savings proposition does not by itself prove realized savings, causal growth contribution, or complete alignment across every product and revenue stream.

## Cross-Company Patterns

### Align the Reward With the Value Mechanism

- Dropbox rewards storage with storage capacity.
- Duolingo uses progress and recovery around repeated learning.
- Uber pays to coordinate supply and demand where local liquidity is constrained.
- ByteDance distinguishes reward types according to behavior, segment, and product role.
- Ramp frames the business model around a customer-savings outcome.

Alignment improves plausibility but does not establish incrementality, durability, or positive economics.

### Use Different Durability Tests

| Mechanism | Durability question |
| --- | --- |
| Cash or coins | Does behavior remain after payout declines or stops? |
| Marketplace subsidy | Does local liquidity, quality, and participant economics survive tapering? |
| Product capacity | Do referred recipients activate, retain, and continue valuing the product? |
| Progress protection | Does the user return to meaningful action rather than protect a counter alone? |
| Structural alignment | Is customer value realized and economically connected to company growth? |

### Measure the Whole System

An incentive can improve its target metric while harming another product, participant side, channel, cohort, or long-term motivation. Review customer-level, marketplace-level, and portfolio-level outcomes together.

### Design Risk Before Scale

ByteDance emphasizes anti-abuse and audience isolation; Uber requires local and cross-side economics; Dropbox needs referral validation and cost controls; Duolingo needs ethical motivation and learning-quality guardrails; Ramp needs transparent outcome and revenue measurement.

## Transfer Matrix

| Situation | Start with | Avoid |
| --- | --- | --- |
| Product value is unproven | Customer research, activation, and retention evidence | Paying users to compensate for weak value |
| Referral could carry qualified value | Recipient value, sender eligibility, activation, retention, and abuse controls | Optimizing invitation count alone |
| Marketplace cannot coordinate a local launch | Hard-side diagnosis, smallest viable network, bounded subsidy, and taper test | Uniform incentives across cities and times |
| Valuable habit is vulnerable to occasional misses | Clear progress, limited recovery, and value-linked return | Coercive loss, excessive reminders, or point farming |
| Multiple products share users | Customer-level holdouts and portfolio contribution | Evaluating the promoted product in isolation |
| Business model claims customer alignment | Realized customer outcome, revenue logic, and conflict audit | Treating positioning as economic proof |

## Related People

- [Xu Hongliang](../../people/xu-hongliang/README.md): cash, coins, coupons, Lite products, referrals, risk, audience isolation, and cannibalization.
- [Andrew Chen](../../people/andrew-chen/README.md): marketplace supply, local liquidity, subsidy boundaries, referrals, and post-incentive economics.
- [Sean Ellis](../../people/sean-ellis/README.md): Dropbox activation, must-have value, and product-aligned referral growth.
- [Luis von Ahn](../../people/luis-von-ahn/README.md): mission-aligned freemium, ethical motivation, visible progress, and learning value.
- [Jackson Shuttleworth](../../people/jackson-shuttleworth/README.md): streak design, recovery, notifications, milestones, experimentation, and retention.
- [Eric Glyman](../../people/eric-glyman/README.md): customer savings and business-model incentive alignment.

## Evidence and Limits

- Evidence relies mainly on participant interviews, talks, and practitioner analysis rather than complete internal experiment, cohort, cost, or fraud records.
- Practices span different company periods and do not represent every current program.
- Company scale, category, regulation, product frequency, data, risk capacity, and participant economics limit transfer.
- Reported growth, revenue, customer, experiment-volume, or savings claims are not used as causal proof.
- Company outcomes cannot be attributed to one incentive, team, or practitioner.
