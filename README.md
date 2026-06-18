# V11-Core 2020 COVID Backtest R7.2

R7.2 = R7 + credit-crisis-only anti-whipsaw gate.

Purpose:
- Keep 2020-style fast V-rebound behavior when the shock is a liquidity panic.
- Apply the 2008-style anti-whipsaw gate only when credit has suffered a deep/prolonged drawdown.

Run:
```bash
pip install -r requirements.txt
python v11_core_2020_backtest.py
```
