# 📊 Fund Analyzer — AI Edge Gallery Skill

An [AI Edge Gallery](https://github.com/google-ai-edge/gallery) skill that analyzes investment funds and ETFs by their **ISIN code**. Get comprehensive financial reports including performance data, risk metrics, top holdings, sector/country weightings, and fees.

## 🚀 Features

- 🔍 **ISIN Lookup** — Search any fund by its International Securities Identification Number
- 📈 **Performance Data** — Current price, changes, 52-week range, beta
- 🏢 **Top Holdings** — Top 10 portfolio positions with weight percentages
- 🏗️ **Sector Weightings** — Sector allocation breakdown
- 🌍 **Country Weightings** — Geographic allocation breakdown
- 💰 **Fund Info** — Market cap, volume, dividends, IPO date

## 📋 Prerequisites

This skill requires a **free API key** from [Financial Modeling Prep](https://financialmodelingprep.com/register):

1. Go to [financialmodelingprep.com/register](https://financialmodelingprep.com/register)
2. Create a free account
3. Copy your API key from the dashboard
4. The skill will prompt you to enter this key when first used

> **Free tier**: 250 API calls/day — more than enough for personal use.

## 📱 Installation in AI Edge Gallery

### Option 1: From URL (Recommended)
1. Open AI Edge Gallery → Agent Skills → Skills chip
2. Tap (+) → **Load skill from URL**
3. Enter: `https://jcptgit.github.io/edge-gallery-fund-analyzer/fund-analyzer/`

### Option 2: Local Import
1. Download this repository
2. Push the `fund-analyzer/` folder to your Android device:
   ```bash
   adb push fund-analyzer/ /sdcard/Download/
   ```
3. Open AI Edge Gallery → Agent Skills → Skills chip
4. Tap (+) → **Import local skill**
5. Select the `fund-analyzer` folder

## 💬 Usage Examples

Once installed, simply type in the chat:

- `Analyze ISIN US9229087690`
- `Give me the data for IE00B4L5Y983`
- `Fund report for LU0996182563`

## ⚙️ How It Works

```
User provides ISIN → LLM detects ISIN pattern → Calls run_js tool
  → index.html receives ISIN + API key
  → Queries FMP API (search-isin → profile → holdings → sectors → countries)
  → Returns formatted report → LLM presents it to the user
```

## 📄 License

MIT License

## ⚠️ Disclaimer

Data provided by [Financial Modeling Prep](https://financialmodelingprep.com). This tool is for informational purposes only and does not constitute financial advice.
