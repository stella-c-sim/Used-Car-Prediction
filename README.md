# 📊 Used Car Prediction

**One-line summary:** What problem you solved and why it matters.

---

## 🧠 Business Problem
Explain this like you're talking to a stakeholder, not a data scientist.

- What decision needed to be made?
- Why was this a problem?
- What happens if nothing changes?

**Example:**  
Online payments were experiencing a decline in authorisation rates in certain countries, leading to lost revenue and customer friction.

---

## 📁 Data
- **Source:** (internal dataset / public dataset / Kaggle / etc.)
- **Time period:** Jan 2023 – Dec 2024
- **Grain:** Transaction-level
- **Rows:** ~2.5M
- **Target variable:** `IS_AUTHORISED`

### Key Features
| Feature | Description |
|------|------------|
| HAS_THREE_DS | Whether transaction required 3DS |
| issuer_country_name | Card issuer country |
| amount | Transaction amount |
| card_type | Debit / Credit |

---

## 🔍 Exploratory Data Analysis (EDA)

Key questions explored:
- How does authorisation rate differ by country?
- What is the impact of 3DS on approval rates?
- Are declines concentrated in certain segments?

### Example Insight
> France shows a **12–15pp lower auth rate** for 3DS transactions compared to non-3DS, suggesting over-application of 3DS.

📈 Example visual:

![Auth Rate by Country](../../Images/project-thumb.png)

---

## 🧪 Methodology
Steps taken:
1. Data cleaning and validation
2. Feature engineering (binning amounts, risk flags)
3. Segment-level analysis
4. Controlled experiment design (A/B test)

(Optional modeling section if applicable)

---

## 🧠 Key Findings
- 3DS reduces authorisation rate by **X pp** in low-risk French transactions
- Non-3DS routing + tokenisation recovers **~Y% lost approvals**
- Impact is largest on returning customers

---

## 📌 Recommendation
**Run a controlled A/B test in France** where:
- Low-risk transactions bypass 3DS
- Control group remains unchanged
- Monitor fraud and chargebacks

**Expected impact:**
- +X pp authorisation uplift
- +$Y monthly recovered revenue
- No significant fraud increase (hypothesis)

---

## 🛠 Tools Used
- Python (pandas, numpy, matplotlib, scikit-learn)
- SQL
- Jupyter Notebook

---

## 🔁 Reproducibility
```bash
pip install -r requirements.txt
