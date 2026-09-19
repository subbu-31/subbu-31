# Subhash Sadacharam

Quantitative research on Indian index options — NIFTY 50, weekly expiries, short premium.
I build the data pipeline, test the idea adversarially, and publish the result whether or
not it worked. Most of what's below is a null.

M.Tech, AI & ML (BITS Pilani, WILP) · QuantInsti EPAT · [LinkedIn](https://www.linkedin.com/in/subhash-sadacharam)

---

## Research

**[vix-forward-range](https://github.com/subbu-31/vix-forward-range)** — Does today's India
VIX close predict tomorrow's NIFTY range? Over 1,402 sessions, r = 0.469 and it survives
HAC errors, a block bootstrap and a locked holdout — but a *five-day-old* VIX print scores
0.389 against the same target, so most of it is a slow regime read, not a fresh daily
signal. R² = 0.22. Clone and run it: both raw series are committed, no broker account
needed.

**[nifty-short-premium-lab](https://github.com/subbu-31/nifty-short-premium-lab)** — 71
weeks of real NIFTY options against a retail options-selling playbook. 4 confirmed, 9 null,
3 retracted — including three strategy variants I built myself and then killed. The
backwardation-fade spread looked real at p = 0.018 full-sample and was carried entirely by
the first eight months.

**[donchian-option-overlay](https://github.com/subbu-31/donchian-option-overlay)** — A
falsification study of the breakout signal every retail options group uses as a timing
device. It carries no tradeable edge on NIFTY weeklies. What does survive is narrower: the
channel's *width* forecasts the size of the next move, not its direction. Includes a
clean-room re-implementation that imports nothing from the main library, and a deliberate
look-ahead probe to prove the pipeline isn't leaking.

**[nifty-oi-repositioning](https://github.com/subbu-31/nifty-oi-repositioning)** — Open
interest repositioning around intraday structural breaks is strongly associated with break
direction, and the association is *reactive, not predictive*: a real-time signal locked on
2025 parameters does not survive a 2026 out-of-sample test.

## Tools

**[greeks-surface-lab](https://github.com/subbu-31/greeks-surface-lab)** — A
dependency-free Black-Scholes solver, a Greek-based P&L attribution engine, and a 3D
explorer driven by real NIFTY option-chain prints. Every Greek — including vanna, charm and
volga — is cross-checked against finite differences of the pricer itself; `mypy --strict`.

**[credit-spread-pipeline](https://github.com/subbu-31/credit-spread-pipeline)** — A
BPS/BCS research pipeline built around one constraint: enforced non-overtrading. One
decision per session, hard caps, no re-entries, enforced in `risk.py` rather than left to
discipline. Point-in-time correctness is tested, not assumed.

## Other

**[esco-onet-semantic-alignment](https://github.com/subbu-31/esco-onet-semantic-alignment)**
— M.Tech dissertation. Embedding-based alignment of the ESCO and O\*NET occupational
taxonomies, with dominance-gap and entropy diagnostics routing each occupation to
accept / review / ambiguous.

---

*Market data used in this research comes from licensed sources and is not redistributed.
Where a repository can ship its own data or a synthetic fixture, it does — see each
README's reproducibility note.*
