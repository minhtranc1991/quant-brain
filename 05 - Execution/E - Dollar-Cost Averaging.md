---
modified:
  - 2026-08-15
created: 2026-08-15
tags:
  - portfolio-management
  - status/needs-review
layer: execution
type: core
domain:
  - portfolio-management
  - investing
---
## 1. Definition

**Dollar-Cost Averaging** is the mechanism that turns a [[S - Passive Indexing]] (or any long-term accumulation) decision into a real order stream: investing a fixed dollar amount in a security or fund at regular intervals (e.g. monthly or quarterly) over an extended period, rather than investing the entire available sum as a single lump sum at one point in time.

## 2. Mechanics

- Because the invested dollar amount is fixed each period while the price per share fluctuates, more shares are automatically purchased when the price is low and fewer when the price is high — mechanically lowering the investor's average cost per share relative to the simple average of the period's prices, without requiring any market-timing judgment.
- The source's own numerical illustration: investing a fixed $1,000/year over 5 years in a volatile-but-flat scenario (market falls, rises sharply, falls again, ending exactly where it started) produced a $6,048 ending value (a $1,048 gain) purely from the automatic buy-low/buy-high-less-often mechanism, versus a smaller $5,915 ending value in a scenario where the market rose steadily and ended 40% higher — illustrating that dollar-cost averaging's benefit comes specifically from *volatility*, not from a rising market per se.

## 3. When it matters

- Building up an equity or bond position gradually through regular savings contributions (e.g. 401(k) or IRA payroll contributions), rather than as a response to a single lump sum becoming available.
- Warren Buffett's framing, quoted in the source: an investor who will be a *net saver/buyer* of stocks for years to come should logically prefer *lower* prices during the accumulation period (since they will be "buying hamburgers," not selling them) — dollar-cost averaging operationalizes this preference automatically.

## 4. Parameters

- Contribution amount: fixed dollar amount per period (not a fixed number of shares).
- Contribution frequency: regular interval, e.g. monthly or quarterly, sustained continuously including during market declines — the source stresses that interrupting contributions specifically during a downturn (when shares are cheapest) forfeits the technique's main benefit.

## 5. Strategy Context

- [[S - Passive Indexing]]

_(Execution → Strategy, `implements` — the inverse of the Strategy's own `executed_by` edge.)_

## 6. Pitfalls

- Does not eliminate the risk of equity investing or protect against a severe bear market (the source explicitly notes it "will not save your 401(k) plan from a devastating fall in value during a year such as 2008") — it only reduces the risk of committing an entire position at a single unfavorable price point.
- Requires sustained discipline: the technique's benefit depends on continuing contributions through downturns, which is psychologically difficult and precisely when loss aversion and herd behavior (see the vault's behavioral-finance Concepts) most strongly push investors to stop.
- In a steadily, monotonically rising market, dollar-cost averaging produces a *lower* total return than lump-sum investing would have, since later contributions buy fewer shares at higher prices — the technique trades away some expected return for reduced timing risk.
