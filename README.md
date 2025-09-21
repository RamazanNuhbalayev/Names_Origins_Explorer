# Names & Origins Explorer 🇦🇿→🇬🇧

*A data-driven look at personal names in Azerbaijan, broken down by **gender** and **linguistic origin***

---

## 1 What Is This Project?

Many parents, teachers and policymakers ask:

*“Which letters start the most female names?”*
*“How many male names follow Turkic vowel-harmony, hinting at native origin?”*

This notebook answers such questions with **16 k+ Azerbaijani first names**, visualising trends in a few clicks.

---

## 2 Key Insights (at a glance)

| Metric                                       | Count      |
| -------------------------------------------- | ---------- |
| Total unique names                           | **16 233** |
| Male names                                   | **9 246**  |
| Female names                                 | **6 987**  |
| Names obeying vowel harmony (native-leaning) | **7 261**  |
| Names breaking harmony (likely borrowings)   | **8 972**  |

These figures come directly from the cleaned dataset in the study.

---

## 3 How the Analysis Works — Plain English

1. **Collect & Clean**

   * Names were scraped from public dictionaries, deduplicated and tagged by gender.
2. **Detect Origin Clues**

   * A simple function checks Turkic *vowel harmony*; names that follow it are flagged as “native-style”.
3. **Visualise**

   * Matplotlib line charts compare counts by starting letter, gender and harmony status.
4. **Summarise**

   * The notebook prints bullet-point findings so non-coders can read results without touching Python.

---

## 4 For Data Scientists

```bash
# Optional virtual environment
python -m venv venv && source venv/bin/activate   # Win: venv\Scripts\activate

# Install pinned dependencies
pip install pandas matplotlib openpyxl

# Launch
jupyter notebook  # Open Names_Origins_Explorer.ipynb
```

*Tech stack:* **Python · Pandas · Matplotlib · BeautifulSoup (scraping)**

### 4.1 Notebook Workflow

1. Read `Names Final.xlsx` → DataFrame.
2. Apply *vowel\_harmony(name)* → boolean flag.
3. Group by first letter & gender; compute counts.
4. Plot side-by-side charts (male vs female, native vs borrowed).
5. Print min/max highlights per letter.

---

## 5 Road-Map

* [ ] Publish interactive Plotly dashboard
* [ ] Add nationality tags beyond vowel harmony
* [ ] Automate monthly updates with new registry data

Contributions welcome — fork, branch, PR! 🚀

---

## 6 Author & Contact

Created by **Ramazan Nuhbalayev**.
Connect on LinkedIn or open an issue for questions.

> *Whether you’re choosing a baby name or modelling linguistic trends, this notebook gives you the numbers behind the narrative.*
