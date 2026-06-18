# V11-Core 2020 COVID Crash Event Backtest R4

這是「全球市場雷達 V11」的 2020 COVID 崩盤事件型回測 R4 版。

目標不是預測疫情第一擊，而是驗證：

1. 第一擊後，資金撤退是否能讓 V11 從 452 切到 514。
2. 急殺後如果市場快速 V 型反彈，是否能比 R3 更快解除防守。
3. 解除防守後，是否能等確認再從 452 進入 433。

## R4 與 R3 差異

R3 在 2022 慢熊很穩，但在 2020 急殺急彈中太晚解除防守。

R4 保留 R3 的正常嚴格 R 模式，同時新增「V 型急殺後快速回攻通道」。

快速回攻通道條件：

- 近 90 日曾出現 VIX > 40
- 近 90 日總風險分數曾 > 85
- VIX 自高點回落超過 40%
- QQQ 站回 20 日線
- SOXX 站回 20 日線
- HYG/LQD 站回 20 日線
- QQQ 20 日報酬轉正

符合 5 項以上：514 → 452。

之後若快速反攻條件繼續成立，連續 2 週後：452 → 433。

## 執行方式

```bash
pip install -r requirements.txt
python v11_core_2020_backtest.py
```

輸出：

- output/v11_core_2020_weekly_modes.csv
- output/v11_core_2020_switch_log.csv
- output/v11_core_2020_summary.md
