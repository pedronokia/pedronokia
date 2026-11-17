# Pedro Leite

Python developer from Brazil. I build data-heavy tools, and then I check whether their
signals actually hold up.

### What I've built

- **[Lodout](https://lodout.com)** ([code](https://github.com/pedronokia/lodout)): a live
  website that gives CS2 skins an explainable 0–100 score from public Steam Market data,
  and shows why. A background worker collects prices within Steam's rate limits, so page
  visits never hit Steam. Steam sign-in turns your inventory into a portfolio after fees,
  with resale and buy-order targets. 1,575 tests, 92% coverage, screenshot checks on every
  deploy. *Python, Flask, SQLite, httpx, Docker, GitHub Actions.*
- **[blockguard](https://github.com/pedronokia/blockguard)**: a small circuit breaker for
  rate limits the server imposes on you, published on
  [PyPI](https://pypi.org/project/blockguard/). No dependencies, tested in CI on Python
  3.9 to 3.13.

### How I work

- **Measure before believing.** A daily backtest replays Lodout's score without lookahead,
  split by item into calibration and confirmation sets. It showed the momentum factor
  worked backwards, caught two bugs that were inflating results, and flags it when a score
  band stops holding up.
- **Treat outside limits as design constraints.** Steam's rate limits shaped the
  collector: one worker, a circuit breaker after the first 429, a market-wide crawl paced
  over a day. Steam's terms are why the site never asks for a password, cookie or API key.
- **Tests that run offline.** All network access goes through one mock point, so the
  suite runs without internet, locally and in CI.

**Tools:** Python, Flask, SQLite, pytest, Playwright, httpx, Docker, Git, GitHub Actions.
