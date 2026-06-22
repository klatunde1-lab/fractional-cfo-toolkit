# Fractional CFO Toolkit: 3-Statement Model + Expense Audit

A reusable Excel-based financial intelligence system for small and mid-sized businesses. Combines a fully-linked 3-statement model, unit economics analysis, and an automated expense leakage audit, with an AI layer that turns model outputs into CFO-level strategic briefs.

## Overview

This toolkit does what a fractional CFO does for an SMB: take raw business drivers and turn them into a complete financial picture plus actionable strategy. It demonstrates:

- **3-Statement Financial Modeling**: A driver-based Income Statement, Balance Sheet, and Cash Flow Statement that fully link and balance — change any assumption and all three statements recalculate while the balance sheet stays balanced.
- **Unit Economics**: Churn-driven LTV, CAC, LTV:CAC ratio, and payback period, all linked to the same assumptions that drive the model.
- **Automated Expense Audit**: Rule-based anomaly detection that flags duplicate vendors, high recurring costs, and spending spikes across a transaction dataset, then quantifies recoverable savings.
- **AI Integration Layer**: A documented prompt library that feeds structured model outputs to an LLM, generating institutional-grade CFO briefs, expense audits, and scenario interpretations.

## Sample Business & Key Findings

The toolkit is pre-loaded with a sample boutique fitness studio (a subscription business) to demonstrate functionality. Replace the blue input cells with any business's figures to model it.

Headline results from the sample:

| Metric | Value |
|--------|-------|
| Year 1 Revenue | $393,042 |
| Year 3 Revenue | $643,256 |
| Year 1 Net Income | ($103,752) |
| Year 3 Net Income | $95,423 |
| Year 3 EBITDA Margin | 22.5% |
| LTV : CAC | 13.75x |
| Year 1 Ending Cash | ($26,260) |
| Audit Savings Identified | $30,730 |

**What the model surfaces:**
- The business inflects from a Year 1 net loss to Year 3 profitability — a textbook operating-leverage curve as a growing member base scales against a fixed cost base.
- Year 1 cash goes negative (ending at ‑$26,260), flagging a funding need to bridge to profitability — the kind of liquidity insight the model exists to catch.
- An LTV:CAC of 13.75x indicates highly marketing-efficient customer acquisition.
- The expense audit flagged recurring waste with ~$30,730 in recoverable annual savings.

## How It Works

### 1. Assumptions (the control panel)
Every input lives in one place as a blue, editable cell. Revenue drivers (member count, churn, fee), cost drivers (fixed vs. variable), working capital (DSO/DPO), and capital/depreciation. Nothing downstream is hardcoded.

### 2. The 3-Statement Model
- **Income Statement** — built on a monthly member waterfall for Year 1 (beginning + new − churned), then annual for Years 2–3. Revenue flows through to EBITDA, EBIT, and net income.
- **Balance Sheet** — assets, liabilities, equity, with a CHECK row confirming Assets = Liabilities + Equity in every period.
- **Cash Flow Statement** — reconciles accrual net income to actual cash via depreciation add-backs and working-capital changes, producing the ending cash that links back to the balance sheet.

The three statements connect through three bridges: net income → retained earnings, ending cash → balance sheet cash, and CapEx/depreciation → PP&E.

### 3. Unit Economics
Member lifespan derived from churn (1 ÷ churn rate), profit-based LTV, CAC, LTV:CAC, and payback — all linked live to the assumptions.

### 4. Expense Leakage Audit
Transaction data is imported via Power Query (or pasted), then rule-based formulas flag anomalies automatically across the full dataset. A summary block quantifies total flagged spend and recoverable savings.

### 5. AI Analysis Layer
An "AI Feed" tab consolidates model outputs, unit economics, and audit results into a structured block. A documented prompt library (CFO Strategist, Expense Auditor, Scenario Translator) turns that feed into written executive deliverables. A sample AI-generated CFO brief is included.

## Files

| File | Description |
|------|-------------|
| `Fractional_CFO_Toolkit.xlsx` | The full workbook: Dashboard, 3-statement model, unit economics, audit, AI feed, prompt library |
| `leakage_sample_data.csv` | Sample transaction data for the expense audit |
| `Sample_CFO_Brief.pdf` | Example AI-generated executive brief from the model outputs |
| `/screenshots` | Dashboard and model visuals |

## How to Use It for Your Own Business

1. Open the workbook and go to the **Assumptions** tab.
2. Replace the blue cells with your business's figures.
3. All statements, unit economics, and the dashboard update automatically.
4. For the audit, load your transaction export into the Leakage Audit tab.
5. Copy the AI Feed block into the included prompts to generate your own CFO brief.

## Tools & Skills Demonstrated

- 3-statement financial modeling (linked, balancing)
- Driver-based forecasting and scenario sensitivity
- Unit economics (LTV/CAC, churn, payback)
- Excel: advanced formulas, Power Query (ETL), anomaly detection logic, dashboard design
- AI-augmented financial analysis (structured LLM prompting)

## Author

**Karsten Latunde**  
UC Berkeley, Economics | Class of 2026  
[LinkedIn](https://linkedin.com/in/karstenlatunde)