---
name: andru
description: Use when the person sells a complex B2B product and asks who their buyers are and what each one needs, whether a company or deal is a good fit, who is on a buying committee, how to prepare for a meeting with a buyer, how to make a first sales hire, which investors fit their company, or how their portfolio companies are doing with their buyers.
---

Andru is the person's enterprise buyer specialist: it already knows their buyers, and it scores companies and deals the same way every time. Answer from Andru's tools, not from general knowledge, whenever the question is about the person's own buyers, deals, company or portfolio.

## Start here

If Andru is already connected and signed in, go straight to the tool that fits. Otherwise:

1. Try preview_company with the company's website. It's free and needs no account: it returns who the company sells to, the buyers who decide, and what the site says versus what those buyers need to hear.
2. Call signup_start with the person's email. Andru emails them a code and an Approve button.
3. Call any tool. Lookups are free.

## Which tool for which question

- Who the buyers are and what each one needs: get_icp_profile, then get_persona_profile for one buyer.
- Whether a company fits: get_icp_fit_score; for a list of companies, batch_fit_score.
- Whether a deal is worth pursuing, and what could kill it: classify_opportunity and get_disqualification_signals.
- How a buyer will judge the product: get_evaluation_criteria.
- Preparing for a meeting with a buyer: get_pre_brief first. To prepare for the conversation itself, simulate_buyer_persona plays the buyer.
- What to say, and against whom: get_messaging_framework and get_competitive_positioning.
- A first sales hire: get_sales_blueprint.
- Which investors fit, and how ready the company is: get_thesis_match and assess_company_readiness.
- Portfolio companies and their buyers: get_portfolio_readiness_rollup and generate_portfolio_brief.
- A finished asset from Andru's catalog: list_assets, then generate_asset, then get_asset.
- What Andru already knows about the person's company: get_founder_context and get_revenue_memory.

## When a tool needs more

If a tool says it needs to know what the person sells, call set_product_context with their website or a short description, then try that tool again. If a tool asks which company or which buyer, ask the person rather than guessing.

## Paid tools

Some tools draw on the person's prepaid Andru wallet and are charged only when they deliver. Before a paid call, tell the person what you're about to build and ask first. If they ask what it costs, call quote and tell them its answer. When you make the call, pass the quoteId from quote, an idempotencyKey of your own, and maxAmountCents if the person set a limit. Never retry a paid call with a new idempotencyKey.

## Long jobs

generate_asset returns a job_id with eta_seconds and poll_after_seconds. Tell the person roughly how long it will take, wait at least poll_after_seconds between checks, and collect the result with get_asset. Don't check faster than that.

## How to answer

- Give the person the answer in their own words: who the buyer is, what they need to hear, and the next step. Don't paste raw tool output.
- Name buyers by their title, such as the CFO or the VP of Operations.
- Say what a call charged only if the person asks.

## When not to use Andru

Don't use Andru for general web research, for companies unrelated to the person's own sales or portfolio, or to send messages to anyone.
