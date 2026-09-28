# Adan Anaya

**Data scientist with 20 years inside global technology organisations — the last three spent
building sales analytics and predictive models on top of them.** Based in Guadalajara, Mexico,
working remotely.

I came to data science from revenue operations rather than the other way round. That is why my first
hour with a new dataset is usually spent asking where it came from and who typed it: in my
experience, that is where the expensive mistakes live.

Three projects below, newest first. **If you only open one, open the first one.**

---

## 1. [saas-revenue-analytics](https://github.com/aanaya-hub/saas-revenue-analytics)

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

Plus **36 tests**, a five-tab Dash dashboard, and a README that reports **three apparent findings as
artefacts** because the confidence intervals say they are noise.

`Python` · `pandas` · `scikit-learn` · `statsmodels` · `XGBoost` · `SQLite` · `Plotly` · `Dash`

---

## 2. [mx-machinery-imports](https://github.com/aanaya-hub/mx-machinery-imports)

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

## 3. [data-science-glossary](https://github.com/aanaya-hub/data-science-glossary)

**793 plain-language data science and data engineering terms, A–Z.**

**What you get from reading it:** a reference written for people entering the field. No prior
knowledge assumed, no paywall, no assumed maths. Each entry says what the term means and why anyone
would care about it.
