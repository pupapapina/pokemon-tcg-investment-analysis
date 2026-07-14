# Pokemon TCG (9G) Sealed Box Potential Analysis — Results

*Analysis based on data from 16 Scarlet & Violet sets, 3,387 cards after cleaning.*

> 💡 **Insight for 9G analysis:** Scarlet & Violet introduced a new secret rarity, **"Black White Rare"** (first appearing in Black Bolt / White Flare), with a very low pull rate (~0.2%). If a card of this type is mistakenly grouped under a broader category like "Rare" during data collection, its high price gets multiplied by a far higher probability, sharply distorting the entire set's `EV_set`. When working with new secret rarities in 9G, it's worth double-checking that every unique rarity in a set is correctly represented in the pull rates rather than collapsed into a neighboring category.

---

## 1. Empirical Confirmation of the Anchor Pokemon Hypothesis

This is the main finding of the analysis: the hypothesis that "eternally popular" Pokemon command a price premium is **confirmed by real market data**, with no artificial multipliers involved.

| Card group (SIR/FA) | Count | Median price | Average price |
|---|---|---|---|
| Anchor Pokemon | 32 | **$114.28** | $222.13 |
| Non-Anchor | 849 | $10.45 | $21.95 |

**Anchor cards cost 10.9x more by median** than regular SIR/FA cards of the same rarity tier. This isn't an assumption — it's what the market has already priced in.

**Top 10 most expensive Anchor SIR/FA cards across all 16 sets:**

| Set | Card | Rarity | Price |
|---|---|---|---|
| Prismatic Evolutions | Umbreon ex | SIR | $1,584.55 |
| Paldean Fates | Mew ex | SIR | $925.18 |
| Prismatic Evolutions | Sylveon ex | SIR | $468.46 |
| 151 | Charizard ex | SIR | $451.28 |
| Paldean Fates | Charizard ex | SIR | $334.85 |
| Surging Sparks | Pikachu ex | SIR | $331.68 |
| Prismatic Evolutions | Espeon ex | SIR | $330.44 |
| Prismatic Evolutions | Leafeon ex | SIR | $327.87 |
| Prismatic Evolutions | Vaporeon ex | SIR | $295.84 |
| Prismatic Evolutions | Glaceon ex | SIR | $286.42 |

Notably, **Prismatic Evolutions** dominates the top of the list — it's a set dedicated to Eevee's evolutions, containing six Anchor Pokemon at once (the Eevee line + Umbreon) in SIR format.

---

## 2. Full Comparative Metrics Table

| Set | EV_set | SIR/FA | SIR/FA % | Anchor SIR | Anchor % | Age (months) | In print |
|---|---|---|---|---|---|---|---|
| Paldean Fates | **$317.02** | 22 | 9.0% | 2 | 4.1% | 30 | No |
| Black Bolt | $277.82 | 84 | 48.8% | 0 | 0.0% | 12 | Yes |
| White Flare | $266.08 | 84 | 48.6% | 0 | 0.0% | 12 | Yes |
| 151 | $182.57 | 42 | 20.3% | **9** | 9.7% | 34 | No |
| Paldea Evolved | $152.88 | 86 | 30.8% | 0 | 1.1% | 37 | No |
| Prismatic Evolutions | $134.20 | 49 | 27.2% | **10** | **17.2%** | 18 | Yes |
| Paradox Rift | $87.78 | 84 | 31.6% | 3 | 1.9% | 32 | No |
| Temporal Forces | $83.90 | 56 | 25.7% | 1 | 1.4% | 28 | No |
| Destined Rivals | $80.79 | 62 | 25.4% | 0 | 0.0% | 14 | Yes |
| Scarlet & Violet Base | $77.48 | 60 | 23.3% | 0 | 0.4% | 40 | No |
| Twilight Masquerade | $69.10 | 59 | 26.1% | 1 | 1.8% | 26 | No |
| Shrouded Fable | $55.79 | 35 | 35.4% | 0 | 2.0% | 23 | No |
| Obsidian Flames | $54.27 | 33 | 14.3% | 3 | 3.0% | 35 | No |
| Surging Sparks | $53.53 | 61 | 24.2% | 3 | 2.8% | 20 | No |
| Stellar Crown | $50.43 | 33 | 18.9% | 0 | 2.9% | 22 | No |
| Journey Together | $40.89 | 31 | 16.3% | 0 | 0.5% | 16 | Yes |

---

## 3. Breakdown of the Strongest Candidates

### 🥇 151 — Best overall balance
Highest `Anchor_Concentration` (9.7%) among all sets that have already **gone out of print**. Nine SIR/FA cards featuring Charizard, Mew, and other Anchor Pokemon. Age 34 months — a reprint is unlikely. This is the safest pick from the perspective of the "eternally popular Pokemon" thesis.

### 🥈 Prismatic Evolutions — Highest Anchor concentration, but carries risk
The clear leader in `Anchor_Concentration` (17.2%) and `Anchor_SIR_Count` (10) — the set is literally built around the Eevee line. However, it's only 18 months old and is **still in print** — a moderate reprint risk under our `Reprint_Risk` logic. If no reprint happens soon, its long-term potential exceeds 151's.

### 🥉 Paldean Fates — Highest EV, but a narrow base
The highest `EV_set` ($317) of all sets. However, this is almost entirely due to a single card — Mew ex SIR at $925. `Anchor_Concentration` is only 4.1% — meaning the high EV rests on one rare card rather than a broad base of popular Pokemon. This is a higher concentration risk: if Mew ex's price drops, the set's entire EV collapses with it.

### ⚠️ Black Bolt / White Flare — An unusual finding
The highest `SIR_FA_Concentration` (48.8% and 48.6%) — nearly half of the set's rare cards are SIR/FA. But `Anchor_SIR_Count = 0` for both. Reason: these sets are themed around Generation 5 (Unova) — Snivy, Oshawott, Seismitoad, Zoroark, and so on. Not a single classic Anchor Pokemon (Charizard, Pikachu, Eevee) appears among the top rare cards.

This doesn't mean the sets are bad — Seismitoad IR already costs $216, showing that popularity can emerge outside the base Anchor list. But under the project's strict methodology (only time-tested Anchor Pokemon), these two sets don't get the long-term stability bonus. A notable takeaway: **the Anchor Pokemon list is worth revisiting** if you plan to include sets from other regions/generations.

---

## 4. Risks and Limitations of the Analysis

**Paldean Fates concentration risk.** The set's high EV depends partly on a single card (Mew ex, $925). This runs counter to the "don't put all your eggs in one basket" principle.

**Young sets still in print.** Prismatic Evolutions, Journey Together, Destined Rivals, Black Bolt, White Flare — all are still in print and under 18 months old. Under the project's methodology, this is an elevated reprint risk that could crash card prices.

**The Anchor Pokemon list is static.** It's built around classic favorites (mostly Kanto/Johto/Sinnoh). The data shows popularity can also emerge in other generations (Seismitoad, Volcarona from Black Bolt) — the list is worth revisiting periodically.

---

## 5. Bottom-Line Recommendation

If optimizing purely for **long-term stability** (the project's goal) — **151** is the safest choice: already out of print, high concentration of time-tested Anchor Pokemon, moderate age.

If you're willing to accept a **moderate reprint risk** for higher potential — **Prismatic Evolutions** has the strongest Anchor structure of all 16 sets.

**Paldean Fates** is only worth considering if you specifically believe in Mew ex's long-term value — otherwise, its high EV is a misleading metric built on a single card.
