# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

Python learning/portfolio project: a port of the Yastık6 price shield (`PriceShieldValidator` + `AlertTracker`, from `../Yastık6/backend/Yastık6.Api/`) guided by a Python course. The roadmap is in `docs/PLAN.md`.

`course-material/` holds copyrighted course PDFs. It is gitignored and local only. Read it for context, but never commit it or copy long passages into tracked files.

## Working agreement

- The user is learning for an exam on units 1-4 (variables/types, data structures, conditionals). Until stage 3 in `docs/PLAN.md` is done, use only what units 1-4 cover: no loops, functions beyond simple ones, classes, or pandas in the user's code.
- The user writes the code. Explain, review, and write tests or hints; don't write the solution unless asked.
- Never touch `../Yastık6-Server.key`.

## Commands

- Env: `source .venv/bin/activate` (Python 3.9; src layout, package `yastik6p`)
- Tests: `pytest` (single test: `pytest tests/test_x.py -k name`)
- IDE is Spyder 6; interpreter is `.venv/bin/python` (needs `spyder-kernels` 3.1.x, already installed).
