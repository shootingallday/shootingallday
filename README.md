### Hi, I'm Jomar

Building tools for prop firm futures traders. Solo, technical founder.

---

#### Open source

**[propfirm-calc](https://github.com/shootingallday/propfirm-calc)**

[![PyPI](https://img.shields.io/pypi/v/propfirm-calc?color=2b7489&label=pypi)](https://pypi.org/project/propfirm-calc/)
[![Python](https://img.shields.io/badge/python-3.9%2B-blue)](https://pypi.org/project/propfirm-calc/)
[![License](https://img.shields.io/badge/license-MIT-green)](https://github.com/shootingallday/propfirm-calc/blob/main/LICENSE)
![Dependencies](https://img.shields.io/badge/dependencies-none-brightgreen)

Dependency-free Python math for funded accounts: trailing drawdown floor, the consistency
rule, payout eligibility. Three calculations most journals get subtly wrong.

```python
from propfirm_calc import drawdown_floor

# $50k account, $2k trailing limit. The floor follows your high-water mark up...
drawdown_floor(50_000, 2_000, peak_equity=51_000)   # 49_000  — still trailing

# ...until it locks at the starting balance. Now you can't blow above break-even.
drawdown_floor(50_000, 2_000, peak_equity=53_000)   # 50_000  — locked
```

No bundled firm data — you pass the numbers, so it works for any firm and doesn't go stale
when one of them changes its rules.

```bash
pip install propfirm-calc
```

---

#### Building

**PX Journals** — Trading journal for prop firm futures traders.

**Rewind** — Backtester for NQ and ES. Rust, from scratch.

**Market Order** — Execution engine.

**OrderFilled** — Self-copy trade copier. Your own accounts, one leader, per-account sizing.

**Clips** — Records your chart while you trade and cuts each closed trade into a vertical
clip.

---

#### Stack

<p>
  <img alt="TypeScript" src="https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white">
  <img alt="React" src="https://img.shields.io/badge/React-20232A?logo=react&logoColor=61DAFB">
  <img alt="Rust" src="https://img.shields.io/badge/Rust-000000?logo=rust&logoColor=white">
  <img alt="Python" src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white">
  <img alt="Node" src="https://img.shields.io/badge/Node-5FA04E?logo=nodedotjs&logoColor=white">
  <img alt="Postgres" src="https://img.shields.io/badge/Postgres-4169E1?logo=postgresql&logoColor=white">
  <img alt="Tailwind" src="https://img.shields.io/badge/Tailwind-06B6D4?logo=tailwindcss&logoColor=white">
  <img alt="Cloudflare" src="https://img.shields.io/badge/Cloudflare-F38020?logo=cloudflare&logoColor=white">
</p>

#### About

Prop firm futures trader. Built these because the existing options are multi-asset retail
products with prop firm support bolted on. Mine are the inverse — futures and prop firm rules
are the starting point, not an afterthought.

Most tools try to serve everyone. These serve one audience well.

#### Contact

`jomar@pxjournals.com`
