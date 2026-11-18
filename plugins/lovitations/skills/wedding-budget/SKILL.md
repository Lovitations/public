---
name: wedding-budget
description: Builds or reviews a wedding budget from the couple's quotes, guest count and total amount: costs per category, cost per guest, what is fixed and what scales with guests, and where the plan runs over. Use for "make a wedding budget", "are we over budget", "trouwbudget opstellen", "wat kost onze bruiloft", "presupuesto de boda", "Hochzeitsbudget".
---

# Wedding Budget

Most wedding budgets go over in the same way: the guest count grows and the
costs that scale with it (catering, drinks, chairs, invitations) grow with it,
quietly. The budget has to show which costs are fixed and which scale, so the
couple can see what ten extra guests cost. Two ways to get it wrong: filling
gaps with "average" prices, and leaving out the small items that add up.

## Ground rules

- Amounts come from the couple's quotes and estimates. An amount the couple
  has not given stays empty and is listed as missing; never fill it with an
  average.
- Mark each line as quote, estimate or paid.
- Separate fixed costs from costs per guest.
- Answer in the language the user writes in, in the user's currency. The
  example below is in English.
- A spreadsheet the user shares is left as it is; a new version is saved as a
  new file.

## When to use

"Make a wedding budget", "how much does each extra guest cost", "where can we
save", "are we over", "trouwbudget maken", "kosten bruiloft op een rij",
"presupuesto de boda", "Hochzeitskosten planen".

## Steps

1. **Collect:** the total they want to spend, the guest count per part of the
   day, every quote and estimate they have, what is already paid.
2. **Sort into categories:** venue, catering and drinks, attire, rings, photo
   and video, music, flowers and styling, invitations and stationery,
   transport, hair and make-up, accommodation, other. Add a buffer line
   (the couple chooses the percentage).
3. **Split fixed and per guest**, and compute the cost per extra day and
   evening guest.
4. **Compare with the total**: over or under, per category and overall.
5. **Name what is missing**: categories with no amount yet, usually the small
   ones (tips, stationery, transport, alterations).
6. **Offer a file.** If this environment can run Python, offer a `.xlsx` with
   the guest counts as input cells and every total as a formula. Otherwise
   give a table. Do not write a file without the user saying yes.

## Output format

```markdown
| Category | Amount | Type | Status |
|---|---|---|---|
| Venue | 4,500 | fixed | quote |
| Dinner (62 × 85) | 5,270 | per day guest | quote |
| Party drinks (147 × 28) | 4,116 | per guest | estimate |
| Photographer | 2,200 | fixed | paid deposit 500 |
| Flowers | | | **missing** |

**Total:** 16,086 of 20,000 · **Buffer left:** 3,914
**Each extra day guest:** 113 · **each extra evening guest:** 28
**Missing:** flowers, rings, transport. These usually decide whether you stay under.
```

## Limits

- The budget is as good as the quotes in it.
- The skill does not compare suppliers or quote market prices.
