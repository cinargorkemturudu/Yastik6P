# Yastık6P

A Python port of the **price shield** from Yastık6, a price-tracking
backend. The shield rejects bad price data (zero prices, sudden 40% jumps) and accepts a
big move once several readings agree on the new level.

Built as a learning project alongside a Python course, so it grows in stages: plain functions,
then a class, then a replay of price history in pandas.

> Work in progress. See [docs/PLAN.md](docs/PLAN.md) for the roadmap.

## Setup

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -e ".[dev]"
pytest
```
