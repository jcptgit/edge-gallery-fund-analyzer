---
name: fund-analyzer
description: Analyze investment funds and ETFs by ISIN code. Returns performance, risk metrics (alpha, beta, Sharpe), sector/country weightings, top holdings, and fees using Financial Modeling Prep API.
metadata:
  require-secret: true
  require-secret-description: "API Key de Financial Modeling Prep (gratuita). Regístrate en https://financialmodelingprep.com/register y copia tu API key."
  homepage: https://github.com/jcptgit/edge-gallery-fund-analyzer
---

# Fund Analyzer

Analyze any investment fund or ETF by its ISIN code. Get a comprehensive financial report including performance, risk metrics, holdings, and fees.

## Examples

* "Analyze ISIN LU0690375182"
* "Give me the data for IE00B4L5Y983"
* "Fund report for ES0110407097"
* "Analyze the fund with ISIN LU0996182563"

## Instructions

When the user provides an ISIN code (format: 2 uppercase letters followed by 10 alphanumeric characters, e.g., LU0690375182), you MUST call the `run_js` tool with the following exact parameters:

- data: A JSON string with the following field:
  - isin: String. The ISIN code to look up.

After receiving the result from the tool, format the response as a clear, professional financial report using the following structure. Respond in the SAME LANGUAGE as the user's original message.

### Response Format

Use this template to present the data:

**📋 Fund Profile**
- Name, currency, exchange, sector, industry
- Type (ETF/Mutual Fund)

**📈 Performance**
- Price, price change, 52-week range
- Year-to-date return, beta, volume

**🏢 Top Holdings** (if available)
- List the top 10 holdings with their portfolio weight percentage

**🏗️ Sector Weightings** (if available)
- Show sector breakdown with percentages

**🌍 Country Weightings** (if available)
- Show country/region breakdown with percentages

**💰 Fees & Info**
- Expense ratio (TER), NAV, total assets
- Average volume, market cap

**📊 Risk Metrics**
- Beta value and interpretation

### Important Rules

1. If the ISIN search returns no results, tell the user clearly that the fund was not found in the database and suggest checking the ISIN or trying a different one.
2. If some data fields are not available, show "N/A" rather than making up values.
3. DO NOT invent or fabricate any financial data. Only use data returned by the tool.
4. If the user asks to compare multiple funds, call the tool once per ISIN and present a comparison table.
5. Always include a disclaimer: "Data provided by Financial Modeling Prep. Not financial advice."
