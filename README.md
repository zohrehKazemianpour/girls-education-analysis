# Girls' Education — Messaging Gap Analysis

> 📓 **[View the rendered notebook on nbviewer](https://nbviewer.org/github/zohrehKazemianpour/girls-education-analysis/blob/main/analysis.ipynb)**

This project looks at why girls drop out of secondary school in sub-Saharan Africa, and whether NGO communications actually address the reasons families give.

The central question: **is there a gap between what families say causes dropout and what NGOs talk about?**

## What's in the notebook

1. **Enrolment trends** — World Bank data on girls' secondary enrolment across Nigeria, Sierra Leone, Ghana, Ethiopia and Mali (2000–2022)
2. **NGO theme analysis** — 20 NGO communications documents scored against 6 themes using TF-IDF
3. **The messaging gap** — side-by-side comparison of family survey responses vs. NGO communications, with gap annotations in percentage points

## Data sources

- [World Bank](https://data.worldbank.org/indicator/SE.SEC.ENRR.FE) — Girls' secondary school enrolment (SE.SEC.ENRR.FE)
- [UNICEF — Out of School Children Study, Sierra Leone 2021](https://www.unicef.org/sierraleone/media/1186/file/Out-Of-School%20Children%20Study%20Sierra%20Leone.pdf) (Table 9, survey data)
- UNICEF Sierra Leone — NGO communications corpus (20 paragraphs drawn from the sources below)

### NGO corpus sources

| Source                                                                      | URL                                                                                                                                                                                            |
| --------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| UNICEF Sierra Leone — Education programme page                              | [unicef.org/sierraleone/education](https://www.unicef.org/sierraleone/education)                                                                                                               |
| UNICEF — Out of School Children Study Sierra Leone                          | [unicef.org/sierraleone/reports/out-school-children-study-sierra-leone](https://www.unicef.org/sierraleone/reports/out-school-children-study-sierra-leone)                                     |
| UNICEF Sierra Leone — Situation Analysis of Children and Adolescents        | [unicef.org/sierraleone/reports/situation-analysis-children-and-adolescents-sierra-leone](https://www.unicef.org/sierraleone/reports/situation-analysis-children-and-adolescents-sierra-leone) |
| UNICEF Sierra Leone — National Seminar on Inclusive Education press release | [unicef.org/sierraleone/press-centre](https://www.unicef.org/sierraleone/press-centre)                                                                                                         |
| UNICEF Sierra Leone — 2023 Annual Report                                    | [unicef.org/sierraleone/reports/unicef-sierra-leone-2023-annual-report](https://www.unicef.org/sierraleone/reports/unicef-sierra-leone-2023-annual-report)                                     |

## How to run

```bash
# Create and activate a virtual environment
python -m venv .venv
source .venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Open the notebook
jupyter notebook analysis.ipynb
```

## Files

| File                  | Description               |
| --------------------- | ------------------------- |
| `analysis.ipynb`      | Main notebook             |
| `girls_enrolment.csv` | World Bank enrolment data |
| `ngo_corpus.csv`      | NGO communications corpus |
| `requirements.txt`    | Python dependencies       |
| `*.png`               | Exported charts           |

## Next steps

- Replace keyword-based themes with a full topic modelling pipeline (LDA or NMF)
- Add spaCy for entity recognition across the NGO corpus
- Build an interactive dashboard (Streamlit or Dash)
