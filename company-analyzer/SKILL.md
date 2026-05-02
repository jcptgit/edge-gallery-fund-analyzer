---
name: company-analyzer
description: Analyze any public company by name or ticker symbol. Returns stock price, company profile, financial statements (income, revenue, net income), market cap, sector, CEO, and key financial ratios using Financial Modeling Prep API.
metadata:
  require-secret: true
  require-secret-description: "API Key de Financial Modeling Prep (gratuita). Regístrate en https://financialmodelingprep.com/register y copia tu API key."
  homepage: https://github.com/jcptgit/edge-gallery-fund-analyzer
---

# Company Analyzer

Get a comprehensive financial report for any publicly traded company. Search by company name or ticker symbol and receive stock price, profile data, and income statement analysis.

## Examples

* "Analyze Apple"
* "Give me the financials for MSFT"
* "Company report for Tesla"
* "How is NVIDIA doing?"
* "Busca información de Amazon"
* "Analiza la empresa Inditex"

## Instructions

When the user asks about a specific company (by name or ticker symbol), you MUST call the `run_js` tool with the following exact parameters:

- data: A JSON string with the following field:
  - query: String. The company name or ticker symbol to look up.

After receiving the result from the tool, format the response as a clear, professional financial report. Respond in the SAME LANGUAGE as the user's original message.

### Response Format

Use this template to present the data:

**🏢 Company Profile**
- Name, ticker symbol, exchange
- Sector, industry, CEO
- Number of employees, headquarters country
- Brief company description

**📈 Stock Price & Market Data**
- Current price, price change (amount and %)
- Day range (low — high), 52-week range
- Market capitalization
- Average volume, beta
- Last dividend, earnings announcement

**💹 Income Statement (Latest Annual)**
- Revenue and revenue growth
- Gross profit and gross margin
- Operating income and operating margin
- Net income and net margin
- Earnings per share (EPS)
- EBITDA

**📊 Income Statement (Latest Quarter)**
- Same metrics as annual but for the most recent quarter

### Important Rules

1. If the search returns multiple companies, use the first result (best match).
2. If no company is found, tell the user clearly and suggest checking the spelling or trying the ticker symbol.
3. DO NOT invent or fabricate any financial data. Only use data returned by the tool.
4. If some data fields are not available, show "N/A" rather than making up values.
5. If the user asks to compare multiple companies, call the tool once per company and present a comparison table.
6. Always include a disclaimer: "Data provided by Financial Modeling Prep. Not financial advice."
