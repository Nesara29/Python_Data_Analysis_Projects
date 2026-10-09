<h1 align="center">🐍 Python Data Analysis Projects</h1>

<p align="center">
18 hands-on projects that turn real-world datasets into answers and charts using <b>Python</b>, <b>pandas</b> and <b>matplotlib</b>.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.9%2B-3776AB?logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/pandas-data%20analysis-150458?logo=pandas&logoColor=white" alt="pandas">
  <img src="https://img.shields.io/badge/Matplotlib-visualization-11557c" alt="Matplotlib">
  <img src="https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white" alt="Jupyter">
  <img src="https://img.shields.io/badge/projects-18-brightgreen" alt="18 projects">
</p>

---

## 📖 About

This repository is a collection of 18 small data-analysis projects. Each folder has one Jupyter notebook, its CSV data, and its own README.

Topics range from coffee preferences and flight delays to whale heart rates, volcanoes and Mondrian paintings. Every project follows the same flow: **load data → clean → calculate → visualise → conclude**.

## 🧰 Language & Tools

| Item | What is used | Why |
|---|---|---|
| **Language** | Python 3.9+ (notebook kernel: Python 3.9.6) | Simple, readable, standard for data analysis |
| **Notebook format** | Jupyter Notebook (`.ipynb`) | Code, charts and explanation in one place |
| **Data handling** | `pandas` (all 18 projects) | Tables, filtering, grouping, merging, cleaning |
| **Visualisation** | `matplotlib` (imported in 11 projects) | Bar, line and scatter charts, custom shapes |
| **Data files** | CSV (and one TSV) | Plain-text tables, easy to load with `read_csv` |
| **Documentation** | Markdown | Clean display on GitHub |

> Only Python is used for the analysis. One dataset (flight delays) was originally extracted with the R package `anyflights`; the resulting CSV is included, no R code is.

## 🗂️ Projects at a Glance

✅ = guided walkthrough completed in the notebook  🧩 = starter notebook with open questions

| # | Project | Topic | Data size | Libraries | Status |
|---|---|---|---|---|---|
| 1 | [A Plant-Based Coffee Shop](./coffee-survey-project) | Which dairy and plant-based milks should a new coffee shop stock? | 1,170 rows | pandas, matplotlib | ✅ |
| 2 | [The Ocean's Deep-Diving Animals](./deepest-divers-project) | Which air-breathing animals dive the deepest, and how do you make a bar chart that tells a story? | 118 rows | pandas, matplotlib | ✅ |
| 3 | [Emoji Sentiment](./emoji-sentiment-project) | Are popular emojis linked to positive or negative feelings? | 751 rows | pandas | 🧩 |
| 4 | [What Is the First Day of the Week?](./first-day-of-week-project) | Do more countries and more people start the week on Sunday or Monday? | 257 rows (3 files) | pandas | 🧩 |
| 5 | [Flight Delays](./flight-delays-project) | How does the day of the week affect the chance of a delayed departure? | 5,000 rows | pandas, matplotlib | ✅ |
| 6 | [Is Granola Healthy?](./granola-healthy-project) | Where do the public and nutrition experts disagree about healthy food? | 40 foods | pandas, matplotlib | ✅ |
| 7 | [Jean Pockets](./jean-pockets-project) | Are women's jean pockets really smaller than men's? | 80 rows | pandas | 🧩 |
| 8 | [World's Largest Islands](./largest-islands-project) | Which are the biggest islands, by region and climate? | 100 rows | pandas, matplotlib | 🧩 |
| 9 | [Art as Data (Mondrian Paintings)](./mondrian-art-project) | Can a table of rectangles describe a painting, and can data help spot a fake? | 3,204 rectangles | pandas, matplotlib, matplotlib.patches | ✅ |
| 10 | [Naming Colors Across Languages](./naming-colors-project) | How do English, Spanish and Tsimane speakers name the same colors? | 80 rows | pandas, matplotlib | 🧩 |
| 11 | [People on Banknotes](./people-on-banknotes-project) | Whose faces appear on banknotes around the world? | 279 rows | pandas | 🧩 |
| 12 | [Skeletal Variation](./skeletal-variation-project) | How do human, mammal and bird skeletons compare, especially neck bones? | 206 + 302 + 81 rows | pandas | ✅ |
| 13 | [Solar Eclipses](./solar-eclipses-project) | How long do solar eclipses last, and when are the next ones? | 444 rows | pandas | 🧩 |
| 14 | [A Century of Top Songs](./top-songs-project) | Have number-one songs become longer or shorter over 100 years? | 101 rows | pandas, matplotlib | ✅ |
| 15 | [Typing Speeds](./typing-speeds-project) | What affects how fast people type? | 168,594 rows | pandas | 🧩 |
| 16 | [Volcano Eruptions](./volcanic-eruptions-project) | Which volcanoes have had the longest eruptions since 1800? | 3,724 + 1,281 rows | pandas, matplotlib | 🧩 |
| 17 | [Blue Whale Heart Rates](./whale-heart-rates-project) | How much does a blue whale's heart rate change during a dive? | 1,087 rows | pandas, matplotlib | 🧩 |
| 18 | [Our World Connected](./world-connected-project) | When did more than half of the world get online? | 35 + 125 rows | pandas, matplotlib | ✅ |

## 🧠 Skills Demonstrated

If you know SQL, these pandas operations will look familiar:

| SQL idea | pandas | Used in |
|---|---|---|
| `SELECT col1, col2` | `df[['col1','col2']]` | Coffee Survey, Granola |
| `WHERE` | `df.query('...')` | Skeletal Variation, Top Songs, Mondrian, World Connected |
| `GROUP BY` + `MAX / AVG / COUNT` | `groupby().max() / mean() / size()` | Deepest Divers, Flight Delays, Mondrian |
| `LEFT JOIN` | `merge(..., how='left')` | Granola, Mondrian, World Connected |
| `ORDER BY` | `sort_values()` | most projects |
| column alias (`AS`) | `rename()` | Coffee Survey |
| `DISTINCT` | `drop_duplicates()` | People on Banknotes |
| `IS NULL` / remove empty rows | `isna()` / `dropna()` | Coffee Survey, World Connected |
| calculated column | `eval()` | Flight Delays, Granola, Top Songs, World Connected |

Other skills: date and time handling (`to_datetime`, `strftime`), string splitting (`str.split`), type conversion (`astype`), and chart design (horizontal bars, sorted bars, reference bars, equality lines, labels on outliers, custom `matplotlib.patches`).

---

## 📚 Project Details

### 1. A Plant-Based Coffee Shop

**Folder:** [`coffee-survey-project`](./coffee-survey-project)  
**Status:** ✅ Guided walkthrough (complete)  
**Libraries:** pandas, matplotlib

**Question:** A new specialty coffee shop will serve only plant-based drinks. Using a coffee-lover survey, which dairy alternatives are most popular?

**Why these tools:** **pandas**: The survey is a table with 30 long, sentence-style column names. pandas can select, rename and clean columns in a few lines. Answers are stored as 1/0, so `mean() x 100` directly gives the percentage of people. **matplotlib**: A horizontal bar chart ranks the milk types so the winner is easy to see.

**Key results:**

- Whole milk is the most popular option overall.
- Oat milk is the most popular plant-based choice, so it is a good default for the shop.
- Percentages add up to more than 100% because people can choose more than one milk.

[➡ Full details](./coffee-survey-project/README.md)

---

### 2. The Ocean's Deep-Diving Animals

**Folder:** [`deepest-divers-project`](./deepest-divers-project)  
**Status:** ✅ Guided walkthrough (complete)  
**Libraries:** pandas, matplotlib

**Question:** How deep can penguins, seals, whales and other animals dive, and which categories go deepest?

**Why these tools:** **pandas**: `groupby()` finds the maximum depth per category in one line. **matplotlib**: The main goal of this project is chart design. matplotlib lets you control orientation, colours, grid lines and spines to turn a default chart into a clear one.

**Key results:**

- Penguins reach up to 564 m, much deeper than other seabirds (152 m).
- Only 3 animal categories dive deeper than the 730 m submarine reference.

[➡ Full details](./deepest-divers-project/README.md)

---

### 3. Emoji Sentiment

**Folder:** [`emoji-sentiment-project`](./emoji-sentiment-project)  
**Status:** 🧩 Starter (questions left to solve)  
**Libraries:** pandas

**Question:** Researchers labelled 1.6 million tweets in 13 European languages as positive (+1), negative (-1) or neutral (0). About 4% of the tweets contained emojis. Which emojis are positive and which are negative?

**Why these tools:** **pandas**: The task is data cleaning and new columns (`sentiment = pos - neg`, a `positive_flag`), which are core pandas operations. No chart is needed yet, so matplotlib is not imported.

**Open questions:** Remove unneeded columns and rename the rest in `snake_case`. | Add `sentiment` = % positive - % negative. | Add `positive_flag` = True when sentiment > 0.

[➡ Full details](./emoji-sentiment-project/README.md)

---

### 4. What Is the First Day of the Week?

**Folder:** [`first-day-of-week-project`](./first-day-of-week-project)  
**Status:** 🧩 Starter (questions left to solve)  
**Libraries:** pandas

**Question:** Compare the number of territories, the number of people, and the regions that start their week on Friday, Saturday, Sunday or Monday.

**Why these tools:** **pandas**: The answer needs three separate tables to be combined on the country code (`alpha3`). pandas `merge()` works like a SQL JOIN, so you can weight countries by population and group by region.

**Open questions:** How many territories start the week on Fri / Sat / Sun / Mon? | How many people start the week on each day? (needs a `merge`) | Which regions mostly start on Sunday or Monday, and which are split? (also a `merge`)

[➡ Full details](./first-day-of-week-project/README.md)

---

### 5. Flight Delays

**Folder:** [`flight-delays-project`](./flight-delays-project)  
**Status:** ✅ Guided walkthrough (complete)  
**Libraries:** pandas, matplotlib

**Question:** On which day of the week are departures from the world's busiest airport most often late?

**Why these tools:** **pandas**: Dates and times arrive as text. pandas can convert them (`to_datetime`), subtract them to get a delay, and group by weekday. Text cannot be subtracted, which is why the conversion is needed. **matplotlib**: A bar chart of % delayed per weekday shows the pattern at a glance.

**Key results:**

- Sunday has the highest percentage of delayed flights.
- Tuesday has the fewest late flights.

[➡ Full details](./flight-delays-project/README.md)

---

### 6. Is Granola Healthy?

**Folder:** [`granola-healthy-project`](./granola-healthy-project)  
**Status:** ✅ Guided walkthrough (complete)  
**Libraries:** pandas, matplotlib

**Question:** For 40 foods, how closely do the opinions of the public and the experts match, and which foods split them the most?

**Why these tools:** **pandas**: Two separate tables are cleaned in the same way and then combined with a left merge on `food`. **matplotlib**: The project is about better scatter plots for paired data: equality line, square axes, transparent dots and text labels on the outliers.

**Key results:**

- Both groups agree that apples are healthy (public 96%, experts 99%) and white bread is not (public 20%, experts 15%).
- The biggest disagreement is granola bar, a 43-point gap between the public and experts.

[➡ Full details](./granola-healthy-project/README.md)

---

### 7. Jean Pockets

**Folder:** [`jean-pockets-project`](./jean-pockets-project)  
**Status:** 🧩 Starter (questions left to solve)  
**Libraries:** pandas

**Question:** Compare pocket height and width (front and back, in cm) between men's and women's jeans and between styles.

**Why these tools:** **pandas**: The comparison is group averages (`groupby` by gender and style) on a small, clean table, which is exactly what pandas is good at.

**Open questions:** Average difference in front pocket height between women's and men's jeans. | Skinny vs straight: is there a difference inside the same gender? | Back pocket sizes: women vs men.

[➡ Full details](./jean-pockets-project/README.md)

---

### 8. World's Largest Islands

**Folder:** [`largest-islands-project`](./largest-islands-project)  
**Status:** 🧩 Starter (questions left to solve)  
**Libraries:** pandas, matplotlib

**Question:** Explore the 100 largest islands: the biggest in the tropics, the biggest per region, how area falls with rank, and which islands belong to more than one country.

**Why these tools:** **pandas**: Filtering (`climate == 'tropics'`), `groupby('region')` and string search (`countries.str.contains(',')`) are all pandas operations. **matplotlib**: Imported for the planned line graph of `area` against `rank`.

**Open questions:** 10 largest islands in the tropics. | Largest island in each `region`. | Line graph of `area` (y) vs `rank` (x).

[➡ Full details](./largest-islands-project/README.md)

---

### 9. Art as Data (Mondrian Paintings)

**Folder:** [`mondrian-art-project`](./mondrian-art-project)  
**Status:** ✅ Guided walkthrough (complete)  
**Libraries:** pandas, matplotlib, matplotlib.patches

**Question:** Mondrian's style moved towards simplicity. How can we measure complexity, how did it change over time, and does a suspect painting fit the pattern?

**Why these tools:** **pandas**: Paintings are stored as rows in a table. `query()`, `groupby()` and `merge()` turn rows into per-painting numbers. **matplotlib + patches**: `matplotlib.patches.Rectangle` draws each row as a coloured rectangle, so data becomes a picture again (function `draw_mondrian()`). A scatter plot then shows complexity over time.

**Key results:**

- Complexity increases after 1935, showing a change in style.
- The suspect 1926 painting is a clear outlier with much higher complexity than other paintings of that period, which suggests it could be a fake.

[➡ Full details](./mondrian-art-project/README.md)

---

### 10. Naming Colors Across Languages

**Folder:** [`naming-colors-project`](./naming-colors-project)  
**Status:** 🧩 Starter (questions left to solve)  
**Libraries:** pandas, matplotlib

**Question:** Participants saw 80 colour chips (evenly spaced in the Munsell array) and chose one of 11 colour words. What share of chips is called red, green, etc. in each language, and do the languages correlate?

**Why these tools:** **pandas**: Counting how often each colour name appears per language is a `value_counts()` / `groupby` task. Several tables can be combined with `merge`. **matplotlib**: Rectangles drawn on a grid reproduce the colour chart; later, bar and scatter plots compare languages.

**Open questions:** For each language, % of chips named each colour. | Horizontal bar chart per language. | Scatter plots to compare languages (e.g. English vs Tsimane), which needs `merge`.

[➡ Full details](./naming-colors-project/README.md)

---

### 11. People on Banknotes

**Folder:** [`people-on-banknotes-project`](./people-on-banknotes-project)  
**Status:** 🧩 Starter (questions left to solve)  
**Libraries:** pandas

**Question:** The data covers 241 people on banknotes from 38 countries. What are their genders, occupations and ages, and were they alive when first printed?

**Why these tools:** **pandas**: The notebook already uses `drop(columns=['value'])` and `drop_duplicates(subset='name')` so each person counts once. Questions like 'what % are female?' use `value_counts(normalize=True)`; country questions use `groupby` + median.

**Open questions:** Male vs female proportion. | Writers or politicians: which are more common? What % are musicians? | What % of banknotes were issued before the person's death? (look for negative or NaN in `first_death_diff`)

[➡ Full details](./people-on-banknotes-project/README.md)

---

### 12. Skeletal Variation

**Folder:** [`skeletal-variation-project`](./skeletal-variation-project)  
**Status:** ✅ Guided walkthrough (complete)  
**Libraries:** pandas (with pandas built-in plotting)

**Question:** Are there really more bones in hands and feet than anywhere else? How many bones does a baby have? Do all mammals have 7 neck vertebrae? What about birds?

**Why these tools:** **pandas**: Every question is a count, sum, sort or filter on a table (`value_counts`, `sum`, `sort_values`, `query`). The notebook needs no separate plotting library: pandas' own `.plot.bar()` makes the one chart (it uses matplotlib internally).

**Key results:**

- The claim is true: over 51% of human bones are in the hands and feet.
- Adults have 206 bones; infants have 305 before bones fuse.
- Giraffes also have 7 neck vertebrae. Among mammals only manatees and sloths differ.
- Birds vary much more: 13 is the most common count, 23 is the maximum (Mute swan).

[➡ Full details](./skeletal-variation-project/README.md)

---

### 13. Solar Eclipses

**Folder:** [`solar-eclipses-project`](./solar-eclipses-project)  
**Status:** 🧩 Starter (questions left to solve)  
**Libraries:** pandas

**Question:** What is the average duration of totality in a total solar eclipse, and when did the longest eclipse happen?

**Why these tools:** **pandas**: `duration` is stored as text like `06m29s` and `date` as text. pandas string methods (`str.replace`) and `to_datetime` convert them so you can sort and average them.

**Open questions:** When was the longest eclipse? The longest total eclipse? (convert duration to seconds) | Average duration of total solar eclipses. | Show the next 10 solar eclipses (convert date to datetime).

[➡ Full details](./solar-eclipses-project/README.md)

---

### 14. A Century of Top Songs

**Folder:** [`top-songs-project`](./top-songs-project)  
**Status:** ✅ Guided walkthrough (complete)  
**Libraries:** pandas, matplotlib

**Question:** What is the ideal length of a hit song and how did song durations change over time?

**Why these tools:** **pandas**: The key lesson is data types: a duration like `00:02:43` is text, so it cannot be plotted. pandas string split + type conversion turns it into numbers. **matplotlib**: A line chart of song length by year shows the trend and the spike.

**Key results:**

- The shortest number-one song is 'Sonny Boy' (1928).
- The longest is 'Hey Jude' by The Beatles (1968, 431 seconds), a sharp spike on the chart; durations are higher afterwards.

[➡ Full details](./top-songs-project/README.md)

---

### 15. Typing Speeds

**Folder:** [`typing-speeds-project`](./typing-speeds-project)  
**Status:** 🧩 Starter (questions left to solve)  
**Libraries:** pandas

**Question:** Using data from an online typing test (15 sentences each), compare typing speed (`AVG_WPM_15`) by finger count, rollover ratio and typing course.

**Why these tools:** **pandas**: This is the biggest file in the repo (168,594 rows). pandas filters and compares groups quickly, which is needed for the 'keep other variables constant' comparisons described in the ideas.

**Open questions:** Drop `PARTICIPANT_ID` and rename columns (`AVG_WPM_15` to `wpm`, `ROR` to `ror`, `HAS_TAKEN_TYPING_COURSE` to `course`). | Compare speed by number of fingers after filtering to similar age, layout, language, keyboard type and course; exclude error rate above 3%. | Rollover ratio: compare ROR <= 20% with ROR > 80%.

[➡ Full details](./typing-speeds-project/README.md)

---

### 16. Volcano Eruptions

**Folder:** [`volcanic-eruptions-project`](./volcanic-eruptions-project)  
**Status:** 🧩 Starter (questions left to solve)  
**Libraries:** pandas, matplotlib

**Question:** Which volcanoes were still erupting in December 2024, and which had the longest eruptions?

**Why these tools:** **pandas**: Dates like `07-1913` must be converted with `to_datetime`, durations calculated, and the eruption table joined with the volcano table through `volcano_id` (like a SQL JOIN). **matplotlib**: Imported for a future chart.

**Open questions:** Volcanoes erupting as of Dec 2024. | Volcanoes with the longest eruptions. | Hints: `pd.to_datetime`, merge the volcano table into eruptions, keep only needed columns before merging, `sort_values`.

[➡ Full details](./volcanic-eruptions-project/README.md)

---

### 17. Blue Whale Heart Rates

**Folder:** [`whale-heart-rates-project`](./whale-heart-rates-project)  
**Status:** 🧩 Starter (questions left to solve)  
**Libraries:** pandas, matplotlib

**Question:** Heart rate (beats per minute) is recorded through five dive phases: descent, lunge, filter, ascent and surface. How does it change, and is dive duration linked to the maximum heart rate at the surface afterwards?

**Why these tools:** **pandas**: Warm-up: `groupby('dive_phase')` average. Challenge: convert `timestamp` to datetime, find start and end per `dive_id`, compute duration in minutes, then merge two small tables. **matplotlib**: Scatter plot of dive duration vs maximum surface heart rate.

**Open questions:** Warm-up: average heart rate per dive phase. | Challenge: dive duration per `dive_id` (first descent to last ascent), maximum surface heart rate per dive, merge, scatter plot.

[➡ Full details](./whale-heart-rates-project/README.md)

---

### 18. Our World Connected

**Folder:** [`world-connected-project`](./world-connected-project)  
**Status:** ✅ Guided walkthrough (complete)  
**Libraries:** pandas, matplotlib

**Question:** What percentage of the world population used the Internet each year, and in which year did it pass 50%?

**Why these tools:** **pandas**: Two tables (users, population) share a `year` column, so a left `merge` combines them. `eval()` calculates the percentage and `query()` finds the crossing year. **matplotlib**: A line chart with a 50% reference line (`axhline`) shows the growth.

**Key results:**

- Internet users grew from 3 million in 1990 to over 100 million in 7 years.
- Less than 0.1% of the world used the Internet in 1990; over 65% by 2022.
- The first year above 50% was 2019.

[➡ Full details](./world-connected-project/README.md)

---

## 📁 Repository Structure

```text
python-data-analysis-projects/
├── README.md
├── requirements.txt
├── .gitignore
├── coffee-survey-project/
│   ├── README.md
│   ├── DATA_SOURCES.txt
│   ├── coffee-survey-project.ipynb
│   ├── coffee-survey-results.csv
│   └── coffee-survey-full-dataset.csv
├── deepest-divers-project/
├── emoji-sentiment-project/
├── first-day-of-week-project/
├── flight-delays-project/
├── granola-healthy-project/
├── jean-pockets-project/
├── largest-islands-project/
├── mondrian-art-project/
├── naming-colors-project/
├── people-on-banknotes-project/
├── skeletal-variation-project/
├── solar-eclipses-project/
├── top-songs-project/
├── typing-speeds-project/
├── volcanic-eruptions-project/
├── whale-heart-rates-project/
└── world-connected-project/
```

Every project folder has the same layout: one notebook, its data files, `README.md` and `DATA_SOURCES.txt`.

## ▶️ How to Run

```bash
# 1. Clone
git clone https://github.com/<your-username>/python-data-analysis-projects.git
cd python-data-analysis-projects

# 2. (Optional) virtual environment
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate

# 3. Install
pip install -r requirements.txt

# 4. Open any project
cd coffee-survey-project
jupyter notebook
```

**Google Colab:** each notebook has a commented cell at the top. Uncomment it, upload the CSV files from the same folder, then run all cells.

## 📚 Data Sources & Credits

| Project | Source |
|---|---|
| A Plant-Based Coffee Shop | The Great American Taste Test by James Hoffmann (anonymised survey data). |
| The Ocean's Deep-Diving Animals | Scientific papers listed per animal in `DATA_SOURCES.txt`. |
| Emoji Sentiment | Kralj Novak, P. et al. 'Sentiment of emojis', PLoS ONE 10(12), 2015. https://kt.ijs.si/data/Emoji_sentiment_ranking/index.html |
| What Is the First Day of the Week? | Unicode CLDR supplemental data (first day); UN population via gapminder.org; four regions from gapminder.org. |
| Flight Delays | Flight data extracted with the R package `anyflights` (336,434 ATL flights in 2023, 5,000 sampled). Passenger counts from TSA (tsa.gov/travel/passenger-volumes/2023). Only the resulting CSV files are in this repo; no R code is included. |
| Is Granola Healthy? | Quealy & Sanger-Katz, 'Is sushi healthy? What about granola?', The New York Times, 2016. |
| Jean Pockets | Diehm & Thomas, 'Someone clever once said Women were not allowed POCKETS', The Pudding, Aug 2018. https://pudding.cool/2018/08/pockets/ |
| World's Largest Islands | Visual Capitalist, 'Visualizing the World's 100 Biggest Islands' (2021); based on a map by David Garcia; areas from Britannica and Wikipedia. |
| Art as Data (Mondrian Paintings) | Images from the Mondrian catalogue raisonne (pietmondrian.rkdmonographs.nl). Features extracted with algorithms written by the course authors. |
| Naming Colors Across Languages | Gibson, E. et al. 'Color naming across languages reflects color use', PNAS 114(40), 2017 (Figure S6, Supporting Information). |
| People on Banknotes | The Pudding, 'Who's in Your Wallet?' (Arevalo et al., Apr 2022). https://pudding.cool/2022/04/banknotes/ |
| Skeletal Variation | Williams et al. 2019, Nature Ecology & Evolution (mammals); bird papers listed by DOI in `DATA_SOURCES.txt`. |
| Solar Eclipses | NASA, 'Solar Eclipses: Past and Future'. https://eclipse.gsfc.nasa.gov/solar.html |
| A Century of Top Songs | Durations looked up manually for the specific version that was popular when each song ranked #1. |
| Typing Speeds | Dhakal et al., 'Observations on typing from 136 million keystrokes', CHI 2018. https://userinterfaces.aalto.fi/136Mkeystrokes/ |
| Volcano Eruptions | Global Volcanism Program (2024), Volcanoes of the World v5.2.5, Smithsonian Institution. https://doi.org/10.5479/si.GVP.VOTW5-2024.5.2 |
| Blue Whale Heart Rates | Goldbogen et al., 'Extreme bradycardia and tachycardia in the world's largest animal', PNAS 116(50), 2019. https://purl.stanford.edu/zp260dk8787 |
| Our World Connected | Our World in Data (population: HYDE, Gapminder, UN WPP; Internet: Ritchie et al. 2023) and Statista. |

All datasets belong to their original authors. They are used here for learning and portfolio purposes. Please follow each source's own terms if you reuse the data.

## 📝 Notes

- `typing-speeds.csv` is the largest file (about 11 MB).
- `departures-check-point.tsv` in the flight-delays project is written by the notebook itself.
- Starter notebooks contain a `# YOUR CODE HERE` cell. Their questions are listed in each project README.

## 📄 License

Add your license here (for example MIT) and the name of the course or provider these project briefs came from.

## 👤 Author

**Your Name**  
GitHub: [@your-username](https://github.com/your-username) · LinkedIn: [your-profile](https://linkedin.com/in/your-profile)
