# Skill Registry｜总控调用矩阵

| 阶段 | 主Skill | 辅助Skill |
|---|---|---|
| 项目诊断 | workflow | proposal |
| 总体方案 | solution-architecture | energy-project |
| 光伏 | photovoltaic | 8760-energy-simulation |
| 储能 | storage | 8760-energy-simulation |
| 光储充 | ev-charging | photovoltaic / storage |
| 污水厂 | wastewater | photovoltaic / storage |
| 路灯 | streetlight | energy-project |
| 停车场 | parking | ev-charging / storage |
| 零碳园区 | zero-carbon-park | energy-project |
| 低碳城市 | low-carbon-city | project-portfolio |
| 数据中心 | data-center-cooling | 8760-energy-simulation |
| VPP | vpp | vpp-electricity-market |
| 电力交易 | electricity-trading | vpp |
| EPC | epc-cost | epc-cost-engine |
| 财务 | financial-modeling | cashflow-engine |
| 审计 | financial-model-audit | financial-audit |
| 交付 | deliverables | document-engineering / visual-design |

## 调用规则
1. 总控先读取项目输入和已有数据。
2. 按项目类型加载行业Skill。
3. 技术规模确定后才进入BOM和EPC。
4. EPC与8760模型必须共享同一技术规模。
5. 收益必须来自8760/交易/运营模型，不得凭总投资比例直接生成。
6. 财务指标必须来自年度现金流。
7. 财务审计必须独立复核关键指标。
8. Word、Excel、PPT必须引用同一最终数据版本。
