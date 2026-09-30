# Adan Anaya

**Data scientist with 20 years inside global technology organisations — the last three spent
building sales analytics and predictive models on top of them.** Based in Guadalajara, Mexico,
working remotely.

I came to data science from sales analytics revops rather than the other way round. That is why my first
hour with a new dataset is usually spent asking where it came from and who typed it: in my
experience, that is where the expensive mistakes live.

Four projects below, newest first. **If you only open one, open the first one.**

---

## 1. [saas-revenue-analytics](https://github.com/aanaya-hub/saas-revenue-analytics)

**Live demo: [saas-revenue-analytics.onrender.com](https://saas-revenue-analytics.onrender.com)** — a
Docker container on a free tier, so if it has been idle the first load takes about 15 seconds.

A fictional B2B SaaS business built from nothing: **200 customers over four months**, a star schema of
six tables, every file under 800 rows. The dataset is then deliberately broken in **eight documented
ways** — duplicated rows, impossible values, a broken foreign key — cleaned, and modelled three ways.

**What you get from reading it:** the whole pipeline in one place, from an empty folder to an
interactive dashboard.

- **Regression.** Monthly revenue turns out to be arithmetic, not a prediction problem — it *is*
  `seats × price × (1 − discount)`. So the model was re-aimed at customer sentiment instead.
- **Classification.** Churn, and the finding that matters: the library default threshold of 0.50
  costs **$53,700** against a threshold of 0.20. A missed churner is a lost account; a false alarm is
  one phone call.
- **Clustering.** There are no natural customer segments, and the project says so: HDBSCAN labels
  every customer as noise, and the segments you already had don't separate in feature space.

Plus **40 tests**, a five-tab Dash dashboard **deployed as a Docker container**, and a README that
reports **three apparent findings as artefacts** because the confidence intervals say they are noise.

`Python` · `pandas` · `scikit-learn` · `statsmodels` · `XGBoost` · `SQLite` · `Plotly` · `Dash`

---

## 2. [holding-360](https://github.com/aanaya-hub/holding-360)

**Live demo: [holding-360.onrender.com](https://holding-360.onrender.com/)** — also a Docker container
on a free tier, with the same cold-start caveat as the first project.

One owner, eighteen people and three sets of books — an importer, a sourcing-trip operator and a customs
agency in one warehouse. **Every figure is synthetic**, generated from a single seed, and the project
says so on every screen.

It does not start from a clean dataset. It starts from the folder a real business hands over:
CONTPAQi-style exports, a bank movement report and two hand-kept spreadsheets carrying **fourteen
documented defects**. The generator writes the clean world first, then writes the defective version
from it — and the notebook has to rediscover the findings from the damaged files alone.

**What you get from reading it:** a result measured twice, and a pipeline that shows where the two
measurements disagree.

- **Cash.** A trough of **MXN 2.80 M** against a period median of **10.74 M**, reconstructed from the
  payment stream and labelled as reconstructed.
- **The exchange rate moves margin, not pricing.** Correlation **0.39** and **MXN 1.31 M** of margin
  lost to the peso. In the dashboard the rate is a slider, and it **flips a decision**: at 17.0 the two
  "loss-making" SKUs contribute margin and should be kept; past roughly 18.5 they should be withdrawn.
- **A finding that only exists because the pipeline was built twice.** The bank export drops the ledger
  link on **38 movements**, so a reader working from the bank statement alone reports **MXN 2.74 M** of
  invoices as outstanding that were in fact paid.
- **Intercompany markup.** **MXN 2.51 M** eliminated on consolidation, **MXN 393 K** of it pure markup
  that would otherwise have overstated group revenue.

Plus a table model built around **one shared core** — each company differing only in its operational
flow table, with the remaining tables specified rather than built — **75 tests**, and a notebook that
reports the divergence between the raw and clean worlds instead of hiding it.

`Python` · `pandas` · `Plotly` · `Dash` · `SQLite` · `Docker` · `pytest`

---

## 3. [mx-machinery-imports](https://github.com/aanaya-hub/mx-machinery-imports)

A two-system operations export taken apart and put back together: **1,458 rows describing 1,440
shipments** of industrial machinery from China to Mexico. The two systems disagree with each other,
and finding out where is most of the work.

**What you get from reading it:** a cleaning job documented rather than performed silently.

- **20 defects found**, each with the decision taken and the reasoning behind it.
- Four date formats inside one column, and **1,765 ambiguous dates resolved without a single guess**.
- **22 shipments** whose declared customs tariff code contradicts the duty actually paid — worth
  **MXN 1.2 million** if the declarations are read literally.

It also publishes what it could **not** conclude: there is no supplier ranking, because the spread
between suppliers is smaller than the uncertainty within each one.

`Python` · `pandas` · `NumPy` · `SciPy` · `matplotlib` · `seaborn` · `SQLite` · Excel export

---

## 4. [data-science-glossary](https://github.com/aanaya-hub/data-science-glossary)

**793 plain-language data science and data engineering terms, A–Z.**

**What you get from reading it:** a reference written for people entering the field. No prior
knowledge assumed, no paywall, no assumed maths. Each entry says what the term means and why anyone
would care about it.

---

**Working in:** Python (pandas, NumPy, scikit-learn), SQL, matplotlib, seaborn, Plotly, Git<br>
**Certified:** IBM Data Science Professional Certificate, 2026<br>
**Looking for:** a fully remote data science or analytics role with modelling ownership

[LinkedIn](https://www.linkedin.com/in/adan-anaya-ds) · [aanaya8@proton.me](mailto:aanaya8@proton.me)
