# Pedro Leite

Python developer from Brazil. I build data-heavy tools, and then I check whether their
signals actually hold up.

### What I've built

- **[SkinVault](https://github.com/pedronokia/skinvault)**: a desktop and web app for the
  CS2 skin market. It tracks a portfolio after fees, gives items an explainable 0–100
  score, sends price alerts, and backtests every factor in that score. 2,394 tests.
  *Python, PyQt6, Flask.*
- **[blockguard](https://github.com/pedronokia/blockguard)**: a small circuit breaker for
  rate limits the server imposes on you, published on
  [PyPI](https://pypi.org/project/blockguard/). No dependencies, tested in CI on Python
  3.9 to 3.13.

### How I work

- **Measure before believing.** SkinVault's backtests showed its own momentum factor
  worked backwards, and caught two bugs that were inflating the results.
- **Treat outside limits as design constraints.** Rate limits shaped SkinVault's caching,
  and the Steam terms of service are why it never logs in.
- **Tests that run offline.** All network access goes through one mock point, so the
  suites run without internet, locally and in CI.

**Tools:** Python, PyQt6, Flask, pytest, httpx, Git, GitHub Actions.
