# HydroAgent-OS-Demo

<p align="center">
  <b>Public Capability Showcase for HydroAgent OS</b><br/>
  <sub>用公开 Demo 与结果证据展示水文数字人的专业能力</sub>
</p>


<p align="center">
  <a href="https://github.com/losnleger/HydroAgent-OS"><img alt="Main Repo" src="https://img.shields.io/badge/Main%20Repo-HydroAgent--OS-0A66C2"></a>
  <img alt="Demo Cases" src="https://img.shields.io/badge/Demo%20Cases-7-16A34A">
  <img alt="Output Figures" src="https://img.shields.io/badge/Output%20Folders-7-0EA5E9">
  <img alt="Tool Regression" src="https://img.shields.io/badge/Regression-27%2F27%20PASS-22C55E">
</p>


## What This Repository Is

`HydroAgent-OS-Demo` is the public-facing showcase repository of **HydroAgent OS**.

It is designed for readers who want to quickly understand:

- what hydrology/hydraulics tasks HydroAgent OS can solve,
- how the interaction and model orchestration works,
- what outputs and evidence are produced in real cases.

This repository focuses on **capability evidence**, not proprietary implementation.

## Highlights

- Covers runoff generation, hydrograph routing, hydraulic structures, flood frequency, and reservoir routing
- Includes full dialogue-style demos for real engineering scenarios
- Provides visual outputs and report artifacts for reproducibility
- Anchored by measurable benchmark evidence from the main repository

## Repository Structure

```text
HydroAgent-OS-Demo/
├─ demo/
│  ├─ demo_1.md
│  ├─ demo_2.md
│  ├─ ...
│  └─ README.md
├─ output/
│  ├─ demo_1/
│  ├─ demo_2/
│  ├─ ...
│  └─ README.md
└─ README.md
```

## Demo Coverage

| Demo        | Scenario Focus                                      | Key Capability           |
| ----------- | --------------------------------------------------- | ------------------------ |
| `demo_1.md` | 半干旱流域完整链路（Green-Ampt + Nash + Muskingum） | 产汇流链式建模与参数确认 |
| `demo_2.md` | SCS-CN + Muskingum + 堰闸能力约束                   | 建筑物瓶颈识别与风险解释 |
| `demo_3.md` | 汇流计算 + 堰闸参数追问与泄流分析                   | 缺参追问与工程解释       |
| `demo_4.md` | 湿润区链式计算与方案对比（A/B）                     | 决策分支与结果对照       |
| `demo_5.md` | 多轮深度会话与参数迭代修正                          | 可追溯参数推断流程       |
| `demo_6.md` | 堰流计算 + P-III 频率分析 + 水库调洪                | 多任务跨域协同           |
| `demo_7.md` | 运行模式切换 + Green-Ampt/Nash计算                  | 交互控制与流程稳定性     |

## Output Artifacts

Each `output/demo_x/` folder contains representative visual artifacts such as:

- `green_ampt_*.png`: infiltration-runoff partition process
- `nash_hydrograph_*.png`: rainfall-runoff hydrograph
- `muskingum_routing_*.png`: inflow-outflow routing comparison
- `flood_frequency_*.png`: P-III frequency curve
- `reservoir_routing_*.png`: reservoir flood routing process
- `rainfall_runoff_*.png`: composite rainfall-net-rainfall-flow figure

## Proven Evidence (from Main Repo)

Reference project: https://github.com/losnleger/HydroAgent-OS

As of **2026-03-03**:

- Tool precision regression: **27 cases / 67 checks / 0 failed / PASS**
- Multi-event calibration benchmark:
  - Nash train/val robustness score: **87.58 (A)**
  - SCS+Nash+Muskingum train/val robustness score: **90.45 (A)**

## How To Read This Repo Efficiently

1. Start with `demo/README.md` to pick a scenario by task type.
2. Open the corresponding `demo/demo_x.md` to inspect full dialogue and reasoning traces.
3. Cross-check figures in `output/demo_x/`.
4. If needed, verify benchmark reports in the main repo (`eval/tool_precision/reports/`).

## Relationship with HydroAgent-OS

- **HydroAgent-OS (main repo)**: architecture, runtime, tools, benchmark pipeline
- **HydroAgent-OS-Demo (this repo)**: curated demos and outputs for public presentation

This dual-repo strategy keeps proprietary engineering assets private while making capability evaluation transparent.

## Contact

- Main project: https://github.com/losnleger/HydroAgent-OS
- Author: Losn
- Email: losnleger@gmail.com

