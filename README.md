# V11-Core 2020 COVID Crash Event Backtest R3

這是 V11-Core R3 規則用於 **2020 COVID 崩盤** 的事件型回測。

目標：

1. 測試 COVID 第一擊後，資金撤退擴散時，V11 是否能從 452 切到 514。
2. 測試 2020 急殺急彈後，V11 是否能在資金回流時切到 433。
3. 觀察 R3 在 V 型反彈中是否太保守。

預設期間：

```text
2019-11-01 ～ 2020-12-31
```

使用 proxy：

```text
00662 proxy：QQQ
半導體：SOXX
信用利差 proxy：HYG/LQD
市場廣度：RSP/SPY、IWM/SPY、QQQ/RSP
防禦資產：SHY/SPY
波動：^VIX
```

執行：

```bash
pip install -r requirements.txt
python v11_core_2020_backtest.py
```

輸出：

```text
output/v11_core_2020_weekly_modes.csv
output/v11_core_2020_switch_log.csv
output/v11_core_2020_summary.md
```

判斷重點：

```text
2020-02～2020-03 是否切 514
2020-03～2020-04 是否維持防守，還是反應太慢
2020-04～2020-08 是否能在資金回流後解除防守或切 433
R3 是否過度保守，錯過 V 型反彈
```
