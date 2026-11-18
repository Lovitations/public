---
name: seating-plan
description: Drafts a wedding seating plan from the guest list, the tables and the couple's wishes: who must sit together, who must not, where the family and children go. Returns a table-by-table plan and the trade-offs it made. Use for "help with our seating plan", "who sits where", "tafelschikking bruiloft", "distribución de mesas boda", "Sitzplan Hochzeit".
---

# Seating Plan

A seating plan is a puzzle with a few hard rules (these two never at one
table, grandma near the exit) and many soft wishes. The couple needs a first
draft that obeys every hard rule and says openly which wishes it could not
meet. Two ways to get it wrong: a neat plan that quietly breaks one hard rule,
and seating a plus-one away from the person they came with.

## Ground rules

- Only people who are coming, for the meal being seated. Ask if RSVPs are not
  in yet.
- Hard rules are never broken. If they cannot all be met, say which ones clash
  instead of picking one.
- Couples and plus-ones sit together unless the couple says otherwise.
- Answer in the language the user writes in. The example below is in English.

## When to use

"Help us with the seating plan", "who should sit with whom", "we have 8 round
tables of 10", "tafelschikking maken", "wie zet ik naast oma", "distribuir las
mesas", "Sitzordnung".

## Steps

1. **Collect:** the guests who are coming (with households), the tables (number,
   shape, seats each), the head table or sweetheart table.
2. **Ask for the rules** in one message: who must sit together, who must not,
   who needs to be near the exit or away from the speakers, where the children
   go, mixed or by group.
3. **Group first**: households, then friend groups, family branches,
   colleagues. Keep groups whole where they fit.
4. **Fill the tables**, starting with the tables closest to the couple, then
   the hard rules, then the wishes.
5. **Check** every hard rule against the result, and every table against its
   seat count.
6. **Report** the plan table by table, then the trade-offs and the empty seats.

## Output format

```markdown
## Table 1 (family Emma, 10/10)
Mother and father Smit, Lisa + Joris, grandma Smit (near exit), ...

## Table 2 (friends Daan, 9/10)
...

**Hard rules:** all met. Uncle Peter and Marco at tables 3 and 7.
**Wishes not met:** the university friends are split over tables 4 and 5 (12 people, 10 seats).
**Empty seats:** table 2 (1), table 6 (2).
```

## Limits

- The plan is a first draft; only the couple knows the family politics.
- It does not draw the floor plan of the venue.
