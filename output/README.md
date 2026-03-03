# Output Artifacts

本目录存放 `demo/` 对应场景的可视化输出，用于展示 HydroAgent-OS 的结果可解释性与工程可复核性。

## 目录结构

```text
output/
├─ demo_1/
├─ demo_2/
├─ demo_3/
├─ demo_4/
├─ demo_5/
├─ demo_6/
└─ demo_7/
```

## 文件类型说明

- `green_ampt_*.png`  
  Green-Ampt 下渗-净雨过程图，展示入渗与产流分配。

- `nash_hydrograph_*.png`  
  Nash 汇流过程图，展示降雨/净雨与出口流量关系。

- `muskingum_routing_*.png`  
  Muskingum 河道演算入流-出流对比图，含削峰与滞时特征。

- `rainfall_runoff_*.png`  
  综合过程图（降雨 + 净雨 + 流量），用于链式任务一图总览。

- `flood_frequency_*.png`  
  洪水频率分析图（P-III），用于设计洪水读取与外推判断。

- `reservoir_routing_*.png`  
  水库调洪过程图，关注最高库水位、最大下泄、削峰率等。

## 当前样例概览（来自本仓库快照）

| Folder | Representative Outputs |
|---|---|
| `demo_1/` | `green_ampt`, `nash_hydrograph`, `muskingum_routing`, `rainfall_runoff` |
| `demo_2/` | `nash_hydrograph`, `muskingum_routing`, `rainfall_runoff` |
| `demo_3/` | `nash_hydrograph` |
| `demo_4/` | `nash_hydrograph`, `muskingum_routing`, `rainfall_runoff` |
| `demo_5/` | `nash_hydrograph`, `muskingum_routing`, `rainfall_runoff` |
| `demo_6/` | `flood_frequency`, `reservoir_routing` |
| `demo_7/` | `green_ampt`, `nash_hydrograph`, `rainfall_runoff` |

## 结果解读建议

1. 先看图形是否与场景机理一致（如降雨峰后流量峰是否滞后）。
2. 再看关键指标（峰值、峰现时刻、削峰率、拟合优度）。
3. 最后结合 `demo/demo_x.md` 的解释文本，确认边界条件与风险提示是否充分。

## 与评测报告的关系

- 本目录是“可视化证据”。
- 量化精度请结合主仓库 `eval/tool_precision/reports/` 中的 `.md/.json` 报告。

## 公开边界说明

本目录仅用于能力展示，不包含私有模型权重、内部策略、生产配置与任何敏感信息。
