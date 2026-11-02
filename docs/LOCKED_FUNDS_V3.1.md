# The Accountant — Locked Funds Experiment (v3.1)

**Status:** Prototype implemented and browser-tested; user acceptance and real backend feasibility **pending**. This is not a banking control in production.

## Goal

Protect an amount of personally verified cleared money already allocated to an approved budget, without creating any separate wallet or changing the established Overview → Payments → Accounts → My Plan → AI Accountant architecture.

## Demonstration rule

1. Receive a fictional incoming payment and simulate provider confirmation with sample personal-ownership evidence.
2. Approve a plan in My Plan.
3. Under **My Plan → Locked money**, choose an approved category, a purpose, an amount within its currently available budget, and explicitly confirm the lock.
4. The locked amount remains included in wallet cash and within its original budget, but is **excluded from available spending**. A payment draft, a standing allowance, or an AI-suggested payment cannot spend it. Editing allocations cannot reduce the category below funds already paid, reserved, or locked.
5. **Request unlock** starts a 24-hour delay. Money remains locked for the whole period; the user can cancel the release request.
6. After the delay, the user must choose **Release this money**. It becomes available again only within the original approved budget.
7. **Advance demo clock by 24 hours** exists solely for testing the waiting period and does not automatically release funds.

## Accountability boundaries

- **Confirmed in browser tests:** a lock reduces spendable budget without reducing cash; an over-budget protected payment is blocked even after acknowledgement; editing a budget cannot reassign a lock; requesting release alone does not unlock it; release requires waiting period + explicit confirmation; the full flow works on narrow mobile widths.
- **Not implemented:** backend or financial institution restrictions, real wallet holds, authenticated identity or override policies, durable ledger, verified time, cross-device enforcement, real AI. The demo state resets on reload and can be altered via browser developer tools.
- **Working product decision:** a 24-hour delayed-release lock is a candidate for user testing, **not final approved backend architecture**. Fixed-date locks, emergency release policy, dispute processes, interest implications, and which licensed provider can honor restrictions are still open.

## Real-world provider requirements (to research next)

A future lock must be enforced server-side against cleared and user-owned balances at payment authorization and execution, not merely in the UI. It requires an auditable ledger, immutable lock and release events, authenticated release requests, idempotent payouts, synchronization across devices, a trustworthy clock, and a provider commitment if bank-level ringfencing is claimed. A budget-level software lock must be accurately described as software enforcement, not a bank custody restriction.
