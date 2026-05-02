# 📊 AI Edge Gallery — Financial Skills

A collection of [AI Edge Gallery](https://github.com/google-ai-edge/gallery) skills for financial analysis using [Financial Modeling Prep](https://financialmodelingprep.com) API.

## 🎯 Available Skills

### 1. Fund Analyzer
Analyze investment funds and ETFs by their **ISIN code**. Get performance data, risk metrics, top holdings, sector/country weightings, and fees.

**Install URL:** `https://jcptgit.github.io/edge-gallery-fund-analyzer/fund-analyzer/`

**Features:**
- 🔍 ISIN Lookup — Search any fund by its ISIN
- 📈 Performance Data — Current price, changes, 52-week range, beta
- 🏢 Top Holdings — Top 10 portfolio positions with weight %
- 🏗️ Sector Weightings — Sector allocation breakdown
- 🌍 Country Weightings — Geographic allocation breakdown

**Usage:** `Analyze ISIN IE00B4L5Y983`

---

### 2. Company Analyzer
Get a comprehensive financial report for any publicly traded company. Search by **company name or ticker symbol**.

**Install URL:** `https://jcptgit.github.io/edge-gallery-fund-analyzer/company-analyzer/`

**Features:**
- 🏢 Company Profile — Name, sector, industry, CEO, employees, website
- 📈 Real-time Stock Quote — Price, change, day/52-week range, P/E, EPS
- 💹 Income Statement — Revenue, net income, margins, EBITDA (5 years)
- 📊 Year-over-Year Growth — Revenue & net income growth trends

**Usage:** `Analyze Apple` or `Give me the financials for MSFT`

---

## 📋 Prerequisites

Both skills require a **free API key** from [Financial Modeling Prep](https://financialmodelingprep.com/register):

1. Go to [financialmodelingprep.com/register](https://financialmodelingprep.com/register)
2. Create a free account
3. Copy your API key from the dashboard
4. Each skill will prompt you to enter this key when first used

> **Free tier**: 250 API calls/day — more than enough for personal use.

## 📱 Installation in AI Edge Gallery

### From URL (Recommended)
1. Open AI Edge Gallery → Agent Skills → Skills chip
2. Tap (+) → **Load skill from URL**
3. Enter the URL of the skill you want to install (see above)

### Local Import
1. Download this repository
2. Push the skill folder to your Android device:
   ```bash
   adb push fund-analyzer/ /sdcard/Download/
   adb push company-analyzer/ /sdcard/Download/
   ```
3. Open AI Edge Gallery → Agent Skills → Skills chip
4. Tap (+) → **Import local skill**
5. Select the skill folder

## 💬 Usage Examples

### Fund Analyzer
- `Analyze ISIN US9229087690`
- `Give me the data for IE00B4L5Y983`
- `Fund report for LU0996182563`

### Company Analyzer
- `Analyze Apple`
- `Give me the financials for MSFT`
- `Company report for Tesla`
- `How is NVIDIA doing?`
- `Analiza la empresa Amazon`

## 📄 License

MIT License

## ⚠️ Disclaimer

Data provided by [Financial Modeling Prep](https://financialmodelingprep.com). This tool is for informational purposes only and does not constitute financial advice.
