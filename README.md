<div align="center">

# 📈 A股智能分析 · 个人实战定制版

[![GitHub stars](https://img.shields.io/github/stars/ljh1119999/ben-stock-prediction?style=social)](https://github.com/ljh1119999/ben-stock-prediction/stargazers)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?logo=docker&logoColor=white)](https://hub.docker.com/r/zhulinsen/daily_stock_analysis)

> 🤖 基于 [ZhuLinsen/daily_stock_analysis](https://github.com/ZhuLinsen/daily_stock_analysis) 深度定制增强版 — 不只是 fork，是个人实战交易工具箱。

</div>

## 🔥 与原版的区别

| 维度 | 原版 | 本定制版 |
|------|------|----------|
| **A股强化** | 通用A/H/美股覆盖 | 深度优化A股数据源、技术指标、资金流分析 |
| **AI 引擎** | 多模型可选 | 集成 **Hermes Agent** 全自动工作流，微信端实时交互 |
| **投资框架** | Agent策略问股 | 额外集成 **13位投资大师思维框架**（巴菲特/索罗斯/德鲁肯米勒/林奇…），每只股票多角度交叉验证 |
| **自动化** | GitHub Actions / Docker | Hermes Cron 定时调度 + 微信推送，A股交易时段全覆盖 |
| **决策输出** | 标准仪表盘 | 大师投票汇总（看多X/中性X/看空X）+ 综合结论 + 操作建议 |
| **数据联动** | 独立运行 | 与 [铝价预测系统](https://github.com/ljh1119999/aluminum-price-prediction) 共享分析框架 |

## ✨ 核心特性

### 🧠 Hermes Agent 深度集成

- **微信端交互**：通过微信直接触发分析、查询报告、调整参数
- **Cron 定时调度**：自动抓取 → 技术分析 → AI 决策 → 推送，全链路无需人工
- **自选股管理**：002837 英维克、603991 领先股份等，随时通过微信增删

### 🎯 13位投资大师思维框架

每只股票自动经过以下大师视角交叉验证：

| 看多阵营 | 中性阵营 | 看空阵营 |
|----------|----------|----------|
| 德鲁肯米勒（趋势跟踪） | 林奇（PEG估值） | 巴菲特（护城河+安全边际） |
| 索罗斯（反身性理论） | Tepper（极端机会） | 段永平（商业模式） |
| Wood（成长创新） | 马克斯（周期位置） | |
| Raschke（技术分析） | | |
| 梁文锋（量化信号） | | |

最终输出：**看多 X : 中性 X : 看空 X** 投票汇总 + 综合投资结论。

### 📊 A股专属增强

- 龙虎榜、融资融券、北向资金实时监控
- A股特有技术指标（筹码分布、量比、换手率深度分析）
- 涨跌停板风险预警

---

## 🚀 快速开始

### 本地运行

```bash
# 克隆项目
git clone https://github.com/ljh1119999/ben-stock-prediction.git && cd ben-stock-prediction

# 安装依赖
pip install -r requirements.txt

# 配置环境变量（参考 .env.example）
cp .env.example .env && vim .env

# 运行分析
python main.py --stocks 002837,603991 --force-run
```

### 常用命令

```bash
python main.py --debug              # 调试模式
python main.py --dry-run            # 干跑测试
python main.py --stocks 600519      # 指定股票
python main.py --market-review      # 大盘复盘
python main.py --serve-only         # 仅启动 Web 界面
```

---

## 📱 实际使用效果

本定制版通过 **Hermes Agent + 微信** 实现移动端实时交互：

- 📊 盘后自动推送每日分析报告（大师投票 + 技术面 + 基本面 + 操作建议）
- 💬 微信发送股票代码即可触发即时分析
- 🔔 关键价位突破自动预警

---

## 🙏 致谢

本项目基于 [ZhuLinsen/daily_stock_analysis](https://github.com/ZhuLinsen/daily_stock_analysis)（43K+ ⭐）深度定制，感谢原作者的杰出工作。

完整原版功能特性、Web界面、Docker部署等请参考 [原项目文档](https://github.com/ZhuLinsen/daily_stock_analysis)。

---

## 📄 License

[MIT License](LICENSE) © 2026

基于 [ZhuLinsen/daily_stock_analysis](https://github.com/ZhuLinsen/daily_stock_analysis) 二次开发。

## ⚠️ 免责声明

本项目仅供学习和研究使用，不构成任何投资建议。股市有风险，投资需谨慎。
