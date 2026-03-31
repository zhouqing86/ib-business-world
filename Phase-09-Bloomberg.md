# Phase 09 — Bloomberg终端与数据系统
# Phase 09 — Bloomberg Terminal & Data Systems

> **学习目标 / Learning Objectives**  
> 熟练操作Bloomberg终端的核心功能，掌握常用函数命令及重要数据字段，并了解其他主流金融数据平台。  
> Navigate the Bloomberg Terminal proficiently, master key function commands and data fields, and understand other major financial data platforms.

---

## 9.1 Bloomberg终端基础 / Bloomberg Terminal Basics

Bloomberg终端（彭博终端）是全球金融专业人士最广泛使用的实时数据、新闻和分析平台，每月订阅费约$2,000。  
The Bloomberg Terminal is the world's most widely used real-time financial data, news, and analytics platform, used by traders, analysts, and risk managers globally.

### 基本操作规则 / Basic Navigation Rules

| 概念 | 说明 |
|------|------|
| **Ticker格式** | `{证券代码} {资产类别黄键} <GO>` 例如：`AAPL US Equity <GO>` / `US5Y Govt <GO>` / `EURUSD Curncy <GO>` |
| **黄色功能键 (Yellow Keys)** | `Equity`（股票）/ `Corp`（企业债）/ `Govt`（政府债）/ `Curncy`（货币）/ `Comdty`（大宗商品）/ `Index`（指数）/ `Mtge`（抵押债）/ `Muni`（市政债） |
| **`<GO>`键** | 确认/搜索/执行命令 |
| **`<HELP>`键按两次** | 接通Bloomberg实时客服（24小时全球服务） |
| **`<MENU>`键** | 返回上级菜单 |
| **`<PAGE UP/DOWN>`** | 翻页查看更多内容 |
| **`BACK <GO>`** | 返回上一个界面 |
| **面板系统** | Bloomberg支持将屏幕分割为多个面板（Panel 1-4），每个面板可显示不同功能 |

---

## 9.2 常用Bloomberg功能命令 / Essential Bloomberg Functions

### 市场总览 / Market Overview

| 命令 | 功能 | 说明 |
|------|------|------|
| `WEI` | World Equity Indices | 全球主要权益指数一览表（涨跌幅、成交量等） |
| `WEIF` | World Equity Index Futures | 全球主要股指期货实时行情 |
| `FXC` | FX Currency Cross Rates | 全球主要货币交叉汇率矩阵，快速查看多对货币汇率 |
| `FX` | Foreign Exchange Rates | 外汇汇率总览面板 |
| `BTMM` | Bloomberg Treasury & Money Markets | 美国货币市场利率总览（Fed Funds、T-Bill、Repo等） |
| `IYC` | International Yield Curves | 全球多国收益率曲线比较 |
| `WCDM` | World Credit Default Swaps Monitor | 全球主权和企业CDS利差监控 |
| `WIRP` | World Interest Rate Probability | 美联储及各国央行下次加/降息概率（期货隐含概率） |

### 证券信息 / Security Information

| 命令 | 功能 | 说明 |
|------|------|------|
| `DES` | Description | 证券详细描述：发行人、ISIN、票息、到期日、评级等完整信息 |
| `GP` | Graph Price | 证券价格走势图（可调整时间范围和指标） |
| `GIP` | Intraday Graph Price | 日内价格走势图，支持分钟级别 |
| `HP` | Historical Price Table | 历史价格数据表格 |
| `ALLQ` | All Quotes | 来自多个交易商的实时买卖报价汇总（主要用于固收） |
| `QR` | Quote Recap | 报价差异比较 |

### 固定收益专用 / Fixed Income Specific

| 命令 | 功能 | 说明 |
|------|------|------|
| `YAS` | Yield & Spread Analysis | 债券收益率和利差分析：计算YTM、Z-Spread、OAS、Duration等 |
| `FWCV` | Forward Curve | 利率远期曲线，预测未来利率走势 |
| `SWPM` | Swap Manager | 利率掉期定价和分析工具，可计算固定端利率和NPV |
| `BVAL` | Bloomberg Valuation | Bloomberg独立估值服务，提供流动性较差债券的公允价值 |
| `SRCH` | Fixed Income Search | 按发行人、评级、期限、利率类型等条件筛选债券 |
| `BI` | Bloomberg Intelligence | 深度行业研究，含固收策略报告 |
| `CRVF` | Curve Finder | 收益率曲线查找和比较工具 |
| `RATC` | Ratings Changes | 评级变更历史记录 |

### 外汇专用 / FX Specific

| 命令 | 功能 | 说明 |
|------|------|------|
| `FXIP` | FX Information Page | 外汇市场综合信息：即期汇率、远期点数、波动率、期权定价 |
| `OVML` | Options Valuation | FX期权定价工具：Black-Scholes定价和Greeks计算 |
| `VOLC` | Volatility Curve | 外汇隐含波动率曲线，按期限展示 |
| `FRD` | Forward Rates | 外汇远期汇率计算器 |
| `FXO` | FX Options Monitor | 外汇期权市场监控，含风险逆转（RR）和蝶式价差（BF）报价 |

### 权益专用 / Equity Specific

| 命令 | 功能 | 说明 |
|------|------|------|
| `EQS` | Equity Screening | 股票筛选器，按PE、PB、ROE、市值等多维度筛选 |
| `RV` | Relative Value | 同行估值比较（EV/EBITDA、P/E等倍数对比） |
| `FA` | Financial Analysis | 详细财务报表分析（历史利润表、资产负债表、现金流量表） |
| `CF` | Corporate Filings | 公司监管申报文件（年报、季报、招股书等） |
| `ERN` | Earnings | 业绩发布数据和分析师预测汇总 |
| `ANR` | Analyst Recommendations | 卖方分析师评级和目标价汇总 |
| `DVD` | Dividend Analysis | 历史股息和预期股息数据 |
| `EVTS` | Events Calendar | 即将举行的投资者日、业绩发布、分析师会议等事件日历 |

### 新闻与研究 / News & Research

| 命令 | 功能 | 说明 |
|------|------|------|
| `TOP` | Top News | Bloomberg头条新闻，按市场分类（股票、债券、FX、大宗商品等） |
| `NI` | News Search | 全文新闻搜索，支持按主题、时间、地区筛选 |
| `NH` | News Headlines | 滚动新闻标题流 |
| `BN` | Bloomberg News | Bloomberg自营新闻团队报道 |
| `BRIEF` | Bloomberg Brief | 每日市场简报，含宏观、固收、FX等专项报告 |
| `ECOW` | Economic Calendar | 全球经济数据发布日历（CPI、GDP、Non-Farm Payrolls等） |

### 投资组合与风险 / Portfolio & Risk

| 命令 | 功能 | 说明 |
|------|------|------|
| `PORT` | Portfolio Analysis | 投资组合绩效归因、风险分析、因子暴露分析 |
| `PRTU` | Portfolio Upload | 将外部投资组合数据上传至Bloomberg进行分析 |
| `MARS` | Multi-Asset Risk System | 多资产类别的风险分析，计算VaR、压力测试 |
| `TRA` | Transaction Cost Analysis | 交易成本分析，评估执行质量 |

---

## 9.3 Bloomberg数据字段（API使用）/ Bloomberg Data Fields (BDP / BDH / BDS)

Bloomberg API提供三类数据函数：  
- **BDP（Bloomberg Data Point）**：单一实时/参考数据点  
- **BDH（Bloomberg Data History）**：历史时间序列数据  
- **BDS（Bloomberg Data Set）**：数据集（例如持仓列表、评级历史）

### 常用字段 / Frequently Used Fields

| 字段名 | 中文 | 说明 |
|--------|------|------|
| `PX_LAST` | 最新价 | 证券最近一次成交价格 |
| `PX_BID` | 买价 | 做市商买入报价 |
| `PX_ASK` | 卖价 | 做市商卖出报价 |
| `PX_MID` | 中间价 | (Bid + Ask) / 2 |
| `PX_OPEN` / `PX_HIGH` / `PX_LOW` | 开/高/低价 | 当日开盘、最高、最低价 |
| `VOLUME` | 成交量 | 当日累计成交量 |
| `YLD_YTM_MID` | 到期收益率（中间价） | 债券按中间价计算的YTM |
| `YLD_YTM_BID` / `YLD_YTM_ASK` | YTM买价/卖价 | 债券按买价/卖价计算的YTM |
| `Z_SPRD_MID` | Z利差（中间价） | 债券Z-Spread |
| `OAS_SPREAD_MID` | OAS（期权调整利差） | 含嵌入期权债券的利差 |
| `CPN` | 票息率 | 债券年化票息率（%） |
| `MATURITY` | 到期日 | 债券到期日期 |
| `AMT_OUTSTANDING` | 发行量/流通量 | 债券在外流通的面值总量 |
| `CRNCY` | 货币 | 证券的计价货币 |
| `ISSUER` | 发行人 | 发行人名称 |
| `RATING_MOODY` / `RATING_SP` / `RATING_FITCH` | 穆迪/标普/惠誉评级 | 三大评级机构评级 |
| `DUR_MID` | 久期 | 修正久期（按中间价计算） |
| `CONVEXITY_MID` | 凸性 | 债券凸性（按中间价计算） |
| `DAYS_TO_SETTLE` | 结算天数 | 交易到结算的工作日数 |
| `ACCRUED_INT` | 应计利息 | 每面值100的应计利息金额 |
| `NXT_CPN_DT` | 下次付息日 | 下一次票息支付日期 |
| `DELTA_MID_RT` | Delta（期权） | 期权Delta值 |
| `GAMMA_MID_RT` | Gamma（期权） | 期权Gamma值 |
| `THETA_MID_RT` | Theta（期权） | 期权每日时间价值衰减 |
| `VEGA_MID_RT` | Vega（期权） | 期权对波动率的敏感度 |
| `IVOL_MID` | 隐含波动率 | 期权隐含波动率 |

---

## 9.4 其他主流金融数据平台 / Other Major Financial Data Platforms

| 平台 | 说明 |
|------|------|
| **Refinitiv Eikon / LSEG Data** | 路透社/伦交所集团数据终端；Bloomberg的主要竞争对手，在新闻资讯和新兴市场数据方面有优势；FX和固收数据广泛覆盖。 |
| **FactSet** | 买方机构常用的数据分析和投资组合管理平台；擅长权益基本面数据、投资组合归因分析和财务建模。 |
| **IHS Markit / MarkIt** | 信用衍生品（CDS）、贷款定价和估值数据的重要来源；iBoxx债券指数的发布机构。 |
| **Tradeweb** | 主要机构固定收益电子交易平台（政府债、信用债、利率衍生品）；同时提供执行后数据和TCA。 |
| **MarketAxess** | 信用债（IG和HY企业债）的领先电子交易平台；提供Open Trading多边交易网络。 |
| **ICE Data Services** | 提供债券估值、参考数据和指数（ICE BofA债券指数）；在固收数据方面与Bloomberg竞争。 |
| **SIX Financial Information** | 瑞士SIX集团旗下金融数据服务商，专注于证券参考数据和企业行动数据。 |
| **MSCI Analytics** | 风险分析和因子模型（Barra），被资产管理公司和风险管理团队广泛使用。 |
| **Moody's Analytics** | 信用风险分析工具、经济数据和模型；与Bloomberg有数据整合。 |

---

*上一阶段 / Prev: [Phase 08 — 交易执行与结算](Phase-08-Trading-Execution.md)*  
*下一阶段 / Next: [Phase 10 — 香港与中国市场特有术语](Phase-10-HK-China-Terms.md)*
