# Leg Cramps — Consumer Search Trend Analysis

How consumers search for leg-cramp relief, classified by intent.
Personal care category research · Google Colab / Python

## Objective
Understand the demand structure of the leg-cramp category: what shoppers
actually search for, which intents drive the volume, and which brands win
the clicks. The notebook classifies **Google Keyword Planner** keywords and
**Amazon search terms** into consumer-intent categories, then aggregates
demand by category, concept, and brand.

## Method
1. **Load** the Google Keyword Planner export (~7,100 keywords, monthly
   search volumes Aug 2024 – Jul 2026) and Amazon search-term reports
   (Search Frequency Rank, Search Term, Top Clicked Brands #1–3) from
   Google Drive in Colab.
2. **Classify with an LLM** — unique search terms are sent to the OpenAI API
   (GPT-5) and assigned to intent categories; terms with multiple
   categories are split into one row per category (explode).
3. **Aggregate Google demand** — total monthly searches per category
   (bar chart).
4. **Amazon analysis** — merge classifications back to the search-term
   data, count Top Clicked Brand occurrences, and compute the average
   Search Frequency Rank per term within each category; top-20 tables and
   bar charts per category.
5. **Concept grouping** — a custom regex-based `group_keyword_concept`
   function rolls individual keywords up into concepts, and high-volume
   concepts are aggregated and charted.

## Classification categories
**Symptom · Variants/Types · Function/Benefit · User · Format · Brand ·
Ingredient · Claim · Other**

## Key finding — monthly searches by category (Google)
| Category | Monthly searches |
|---|---|
| Symptom | 10,886,550 |
| Variants/Types | 1,492,800 |
| Function/Benefit | 1,276,100 |
| User | 435,050 |
| Format | 216,750 |
| Brand | 120,100 |
| Other | 65,050 |
| Ingredient | 33,300 |
| Claim | 23,200 |

Symptom language ("leg cramps," "restless legs," "foot cramp") outweighs
brand searches ~90-to-1 — demand is problem-led, not brand-led.

## Tools & packages
- **Python in Google Colab** (Drive-mounted data: `google.colab.drive`)
- **OpenAI API (GPT-5)** — LLM classification of search terms
- **pandas** — loading, combining, merging, aggregation
- **matplotlib + seaborn** — bar charts and tables
- **re (regex)** — rule-based keyword-to-concept grouping
- The same pipeline is reused across personal-care categories
  (ear wax and nasal spray runs are referenced in the notebook).

## Contents
| File | What it is |
|---|---|
| `Leg_Cramps_V2_08192026.ipynb` | Full analysis notebook (163 cells) |
| `data/Keyword_Stats_Leg_Cramps_V1_08142026.csv` | Google Keyword Planner dataset |
