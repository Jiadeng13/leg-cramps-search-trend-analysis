# Leg Cramps — Consumer Search Trend Analysis

How consumers search for leg-cramp relief, classified by intent.
Personal care category research · Google Colab / Python

## Overview
Shoppers rarely search by brand — they search by problem. This project
combines **Google Keyword Planner** data with **Amazon search terms** for
the leg-cramp category and classifies every keyword by consumer intent, to
show what shoppers actually look for and where the demand sits.

## Classification categories
Each search term is assigned to one intent category:
**Symptom · Variants/Types · Function/Benefit · User · Format · Brand ·
Ingredient · Claim · Other**

## Key finding — monthly searches by category
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

## Data
- `data/Keyword_Stats_Leg_Cramps_V1_08142026.csv` — Google Keyword Planner
  export (Aug 14, 2026): ~7,100 leg-cramp-related keywords with average
  monthly searches, competition level/index, top-of-page bid ranges, and
  monthly search volumes for Aug 2024 – Jul 2026.
- Amazon search-term data (combined in the analysis notebook).

## Tools
Python · pandas · matplotlib / seaborn · Google Colab (Drive-mounted data)

## Contents
| File | What it is |
|---|---|
| `data/Keyword_Stats_Leg_Cramps_V1_08142026.csv` | Keyword Planner dataset |
| `Leg_Cramps_V2.ipynb` | Classification + aggregation + charts (to be added) |
