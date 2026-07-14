# Pokemon TCG (9G) Sealed Box Investment Analysis

Power BI analysis evaluating which Scarlet & Violet sealed booster boxes have the strongest long-term value potential — based on measurable market data rather than subjective opinions about art or Pokemon popularity.

## Goal

Determine which 9th generation (Scarlet & Violet) sealed boxes are worth buying for long-term holding (2–3 years), using only measurable market signals.

## Approach

The market already prices in Pokemon popularity and illustration quality — so no artificial multipliers are used. Instead, the model measures set structure: how much the cards inside are worth, how concentrated the set is on rare illustrations, and whether it contains Pokemon that stay popular regardless of time or competitive relevance.

## Metrics

| Metric | What it measures |
|---|---|
| `EV_set` | Expected value of cards in one pack (Σ price × pull rate) |
| `SIR_FA_Count` / `Concentration` | Count and share of rare-illustration cards (SIR, Ultra Rare, Hyper Rare, Illustration Rare) |
| `Anchor_SIR_Count` / `Concentration` | Count and share of cards featuring "eternally popular" Pokemon among rare illustrations and across the whole set |
| `Set_Age_Months` | Set age in months since release |
| `Reprint_Risk` | Risk level combining print status and age |

## Key finding

Cards featuring Anchor Pokemon (Charizard, Pikachu, the Eevee line, Mew, and others) sell for **10.9x more by median price** than non-anchor cards of the same rarity tier — confirmed empirically from real market data, not assumed.

Full results and reasoning: [`docs/analysis_results_en.md`](docs/analysis_results_en.md)

## Repository structure

```
data/processed/      — cleaned data used by the Power BI model
scripts/scraping/    — pull rate collection from CardCodex
scripts/processing/  — merging and cleaning raw data
powerbi/             — the .pbix dashboard file
```

## Data sources

- Card prices, rarities, pull rates: [CardCodex](https://cardcodex.com)
- Release dates and print status: [Bulbapedia](https://bulbapedia.bulbagarden.net)

## Disclaimer

This is a personal data analysis project, not financial advice. Sealed collectible pricing is speculative and past patterns don't guarantee future results.
