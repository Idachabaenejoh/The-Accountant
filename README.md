# The Accountant — UX Prototype v3.0

A static, standalone user-experience simulation of The Accountant personal financial application. **No real bank or wallet API, no account access, no server data storage, no real transfers, no authentication, no actual AI service.**

## Safety

- Sample company/account activity is fictional.
- The displayed `DEMO-ONLY-0001` receiving number is deliberately invalid. **Never send real money to it.**
- No financial account number, bank login, personal identifier, credentials or approval documents should be entered into this public demo.
- This app is a UX prototype, NOT a secure financial service or production-ready ledger.
- Client-side rules can be bypassed. Real transfers, bank connections and approval controls require an authenticated, audited backend and an appropriately authorized bank/payment provider.
- The site is marked noindex for crawlers, but **noindex is not access control**. The Vercel demo URL may be accessible to anyone who has the link.

## Deploy to Vercel via GitHub

1. This GitHub repository is currently **public**. Commit only fictional demonstration source; never commit real financial records, account details, API secrets, or personal data.
2. The static demo was initially deployed at https://the-accountant-demo.vercel.app/. Set up a Git-connected Vercel project for automatic deployments.
3. Choose framework **Other**. Leave Build Command and Output Directory at defaults/unset; the project is plain static HTML and JavaScript without a build step.
4. Deploy. Verify the Vercel-provided HTTPS URL on both phone and desktop.
5. Do not promote it as a real banking product or collect real financial information.

The separate linked company accounts here are demo read-only sample feeds. A real bank link cannot be inferred from a transaction on this demo.

## Mobile acceptance checklist

- Open the HTTPS Vercel URL directly in iPhone Safari and Android Chrome.
- Overview displays balance, activities and copyable **demo** receiving details without overflow.
- Receive opens an account-details modal with clear demo labeling; Escape/close dismisses it.
- Payments: prepare, review and authorize a simulated payout; wallet balance changes only on simulated provider settlement.
- New incoming payment appears in overall wallet after provider confirmation; Accountant prompts for bookkeeping.
- Accounts opens separate Personal and Business sample account activities, without transfer authorization from read-only company accounts.
- My Plan works manually and AI Accountant is available across pages.
- Reload resets client-only simulation. This is expected, not durable storage.

## Next-stage backend research (not implemented)

Research account data aggregation/bank transaction feeds with explicit consent and permitted access; compare Nigerian wallet/collection and payout provider APIs, fees, KYC/legal eligibility, webhooks, virtual accounts, settlement, reconciliation, and transaction signing. Make no assumptions about bank API access or wallet account issuance before written provider confirmation.