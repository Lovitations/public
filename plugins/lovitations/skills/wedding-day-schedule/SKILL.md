---
name: wedding-day-schedule
description: Builds a minute-by-minute schedule for the wedding day from the fixed times the couple has, with travel time, buffers and who is responsible for each moment, plus a short version for guests. Use for "make a schedule for our wedding day", "timeline for the day", "draaiboek bruiloft", "dagplanning trouwdag", "cronograma del día de la boda", "Ablaufplan Hochzeit".
---

# Wedding Day Schedule

On the day, the couple should not be the ones keeping time. The schedule is
for the master of ceremonies, the suppliers and the families: what happens
when, where, and who makes sure it does. Two ways to get it wrong: a schedule
without travel time and buffers, and moments with nobody responsible.

## Ground rules

- Fixed times (ceremony, registrar, dinner, venue closing) come from the
  couple and are never moved without saying so.
- Travel time between places is stated as an estimate for the couple to
  check.
- Every block has an owner: a person or a supplier, never "someone".
- Answer in the language the user writes in, and follow local customs. The
  example below is in English.

## When to use

"Make a schedule for our day", "what time should the photographer come", "is
this timeline realistic", "draaiboek maken", "ceremoniemeester draaiboek",
"timing van onze trouwdag", "cronograma de boda", "Tagesablauf Hochzeit".

## Steps

1. **Collect the fixed points:** ceremony time and place, civil ceremony if
   separate, dinner, party, venue closing time, sunset if they want golden
   hour photos.
2. **Collect the moments** they want: getting ready, first look, photos,
   speeches, cake, first dance, evening snack, send-off.
3. **Collect the people**: master of ceremonies, photographer, video, DJ or
   band, caterer, hair and make-up, transport.
4. **Build the schedule** backwards from the fixed points: travel time, a
   buffer of 10 to 15 minutes before each fixed point, and longer for hair and
   make-up and for group photos.
5. **Flag what does not fit**: overlapping blocks, a photographer booked for
   fewer hours than the plan needs, speeches longer than the time between
   courses.
6. **Write two versions**: the full schedule for the team, and the short
   programme for guests.

## Output format

```markdown
| Time | What | Where | Who |
|---|---|---|---|
| 09:00 | Hair and make-up (2 people, 2.5 h) | Hotel | Studio Glow |
| 12:15 | Photographer arrives | Hotel | Lens & Liefde |
| 13:15 | Leave for the ceremony (15 min drive, check) | | Driver Ruben |
| 13:30 | Buffer | | |
| 14:00 | Ceremony | Oranjerie | Registrar, MC Sanne |

**Does not fit:** the photographer is booked until 21:00, first dance is at 21:15.

## For guests
14:00 Ceremony · 15:00 Drinks · 18:00 Dinner · 20:30 Party
```

## Limits

- Travel and preparation times are estimates; suppliers know their own.
- The skill plans; it does not book or confirm suppliers.
