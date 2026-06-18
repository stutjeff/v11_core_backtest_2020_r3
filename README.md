# V11-Core 2020 COVID Backtest R7.1

測試 R7.1 在 2020 COVID 急殺急彈環境中，是否仍能啟動快速回攻通道。

## Files

- `v11_core_2020_backtest.py`
- `requirements.txt`
- `.github/workflows/run-v11-core-2020-backtest.yml`

## Run locally

```bash
pip install -r requirements.txt
python v11_core_2020_backtest.py
```

## GitHub Actions

Go to **Actions → Run V11-Core 2020 COVID Backtest R7.1 → Run workflow**.

Outputs:

- `output/v11_core_2020_weekly_modes.csv`
- `output/v11_core_2020_switch_log.csv`
- `output/v11_core_2020_summary.md`

## R7.1 logic

R7.1 = R5-fixed + medium repair lane.

- Slow bear / valuation compression: keep R3-style defensive confirmation.
- True panic: allow R4-style fast release only when fast panic regime is confirmed.
- Medium correction: allow 514 → 452 only after medium repair confirmation, not direct 433.


## R7.1 update

R7.1 tightens the medium repair lane. In R6, a 7/9 count could release 514 to 452 even when market momentum was still weak. R7.1 requires momentum repair, QQQ/SOXX 60D repair, credit 60D repair, VIX cooling, score cooling, and positive QQQ 20D return. The goal is to keep the 2018 repair benefit while blocking 2022-style bear-market rallies.


## R7.1 微調

加入信用危機底部防亂跳條件：若 total_score >= 75 或 credit_proxy_score >= 12，即使 V 型快速回攻訊號出現，也暫不允許 514 → 452。
