# Study and code plan

Goal: pass the exam on units 1-4, and end up with a tested Python port of the Yastık6
price shield for the portfolio. Source to port: `PriceShieldValidator` and `AlertTracker`.

## The rules to port

1. **Zero-price shield:** reject a reading if ask <= 0 or bid <= 0.
2. **Flash-crash shield:** reject a reading that moves more than 40% from the last accepted ask.
3. **Re-anchor:** after 3 consecutive rejected readings within 5% of each other, accept the new level.
4. **Alert muting:** the same alert key is sent at most once per hour.

## Stages

| Stage | Course unit | Code | Exam work |
|---|---|---|---|
| 0 | 1 | Setup, venv, run tests in Spyder | Read unit 1, answer its review questions |
| 1 | 2 | Price type (Decimal vs float), conversions, percent change function | Unit 2 exercises |
| 2 | 3 | State in dicts: last accepted price, pending moves | Unit 3 exercises |
| 3 | 4 | The shield rules as `if/elif/else` | Unit 4 exercises |
| 4 | 5 | Replay a list of readings through the shield with loops | After the exam |
| 5 | 6 | Refactor into small tested functions | After the exam |
| 6 | 7 | `PriceShield` and `AlertTracker` classes | After the exam |
| 7 | 8 | Load readings from CSV into pandas, report rejections | After the exam |

Stages 1-3 are the exam stages. Do not start stage 4 until the exam is done.

## Workflow for each stage

1. **Read** the unit (about 1-2 sessions). Run every example in Spyder's console.
2. **Write the tests first.** Say what the code should do in a `pytest` test.
3. **Write the code yourself** in `src/yastik6p/`. Claude reviews it, it does not write it.
4. **Run `pytest`** until green.
5. **Do the unit's review questions** from memory, without the book.
6. **Commit** with a clear message, one stage per commit or more.
7. **Write 3-5 lines** in `docs/NOTES.md`: what you learned and what surprised you.
