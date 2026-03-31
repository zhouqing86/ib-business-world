# Phase 08 — 交易执行与结算
# Phase 08 — Trading, Execution & Settlement

> **学习目标 / Learning Objectives**  
> 掌握订单类型、执行算法、交易生命周期、清算结算机制，以及金融行业核心报文协议（FIX/SWIFT）。  
> Master order types, execution algorithms, trade lifecycle, clearing & settlement, and key financial messaging protocols (FIX/SWIFT).

---

## 8.1 订单类型 / Order Types

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **Market Order** | 市价单 | 以当前最优市场价格立即成交的订单；确保成交但价格不确定。Order to execute immediately at the best available market price; guarantees fill but not price. |
| **Limit Order** | 限价单 | 指定不高于（买入）或不低于（卖出）的价格；若市价触及则成交，否则挂单等待。Buy at no more than / sell at no less than a specified price; may not fill if price is not reached. |
| **Stop Order** | 止损单 | 当价格触及止损价时自动转为市价单执行；用于限制亏损或保护利润。Becomes a market order when the stop price is reached; used to limit losses or protect profits. |
| **Stop-Limit Order** | 止损限价单 | 触及止损价时转为限价单（非市价单）；确保价格但可能不成交。Becomes a limit order (not market) when stop price is hit; ensures price but risks non-execution. |
| **IOC (Immediate or Cancel)** | 立即成交否则取消 | 尽量立即成交，未成交部分立即取消。Execute as much as possible immediately; cancel any unfilled portion. |
| **FOK (Fill or Kill)** | 全部成交否则取消 | 必须立即全部成交，否则整笔订单取消（不允许部分成交）。Must fill the entire order immediately; if not possible, cancel the whole order. |
| **GTC (Good Till Cancelled)** | 有效直至取消 | 订单在显式取消前持续有效（通常有上限天数）。Order remains active until explicitly cancelled (may have a maximum duration). |
| **GTD (Good Till Date)** | 有效至指定日期 | 订单在指定日期前有效，届时自动取消。Order remains active until a specified date, then auto-cancels. |
| **Iceberg Order** | 冰山订单 | 只向市场显示部分订单量（冰山一角），隐藏大额真实订量，减少市场冲击。Displays only a small portion of the total order size to the market; hides large true quantity to minimise market impact. |
| **Pegged Order** | 锚定订单 | 订单价格自动跟随某一市场参考价（如最优买卖价）动态调整。Order price automatically tracks a reference price (e.g., best bid/ask). |

---

## 8.2 执行算法 / Execution Algorithms

机构投资者在执行大额订单时使用算法，以减少市场冲击成本和执行偏差。  
Institutions use algorithms to execute large orders while minimising market impact and execution slippage.

| 缩写 | 全称 | 中文 | 说明 |
|------|------|------|------|
| **VWAP** | Volume-Weighted Average Price | 成交量加权平均价算法 | 将订单分散在交易日内，按历史成交量分布执行，力求接近全日VWAP价格。Splits order throughout the day proportional to historical volume distribution; aims to achieve day's VWAP. |
| **TWAP** | Time-Weighted Average Price | 时间加权平均价算法 | 将订单按时间等量均匀分散在指定时间段内执行，减少时机选择偏差。Splits order into equal slices over a specified time period; minimises timing bias. |
| **POV** | Percentage of Volume | 成交量百分比算法 | 以市场实时成交量的固定比例（如5-10%）跟随市场成交。Participates at a fixed percentage of real-time market volume (e.g., 5–10%). |
| **IS** | Implementation Shortfall | 执行缺口算法 | 以决策价格为基准，最小化实际执行价与决策价之间的总成本（含市场冲击和时机成本）。Minimises total execution cost vs. decision price; trades off market impact against timing risk. |
| **Arrival Price** | — | 到达价格算法 | 以订单到达时的市场价格为基准，快速执行以降低市价风险。Targets the market price when the order arrives; executes quickly to reduce adverse price movement. |
| **Dark Algo** | — | 暗池算法 | 优先在暗池中寻找流动性以减少信息泄露；仅在必要时转向公开市场。Seeks liquidity in dark pools first to minimise information leakage; falls back to lit markets. |

---

## 8.3 交易生命周期 / Trade Lifecycle

```
[1] 投资决策        →  [2] 订单生成     →  [3] 合规检查
    Investment           Order              Pre-trade
    Decision             Generation         Compliance

[4] 订单路由        →  [5] 撮合成交     →  [6] 交易确认
    Order Routing        Trade              Trade
    (OMS→Broker)         Matching           Confirmation

[7] 清算            →  [8] 结算         →  [9] 后台对账
    Clearing             Settlement         Reconciliation
    (CCP/bilateral)      (DvP T+1/T+2)      & Reporting
```

| 阶段 | 英文 | 说明 |
|------|------|------|
| **Pre-Trade** | 交易前 | 风控限额检查、合规审批、流动性评估、TCA预分析 |
| **Order Routing** | 订单路由 | OMS将订单发送至EMS，EMS进行智能路由到最优交易场所 |
| **Execution** | 执行 | 交易所/暗池撮合成交，生成成交回报（Fill Report） |
| **Affirmation** | 预确认 | 买方机构确认成交细节（在结算前的快速确认步骤） |
| **Confirmation** | 正式确认 | 买卖双方通过SWIFT/FIX确认交易条款以备结算 |
| **Clearing** | 清算 | CCP（中央对手方）介入，成为买方的卖方和卖方的买方，进行多边净额轧差 |
| **Novation** | 合同更替 | CCP清算时，原始双边合约替换为与CCP分别签立的两份合约 |
| **Settlement** | 结算 | 按DvP原则进行证券与资金的实际交割 |
| **STP (Straight-Through Processing)** | 直通处理 | 从订单到结算全程自动化，无需人工干预 |
| **Fail** | 交收失败 | 卖方未能按时交割证券或买方未能按时支付资金 |
| **Buy-In** | 强制买入 | 因交收失败，受损方有权从市场强制买入证券并向违约方追偿 |

---

## 8.4 清算与结算 / Clearing & Settlement

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **CCP (Central Counterparty)** | 中央对手方 | 清算时介入买卖双方之间，成为所有交易的统一对手方，大幅降低系统性信用风险。Interposes between buyer and seller; becomes the buyer to every seller and seller to every buyer; eliminates bilateral counterparty risk. |
| **DvP (Delivery versus Payment)** | 货银对付 | 证券交割与资金支付同步进行，确保两者同时完成，消除本金风险。Simultaneous exchange of securities and cash; eliminates principal risk (one leg failing while the other completes). |
| **FoP (Free of Payment)** | 非货银对付 | 证券单边转账，无对应的资金转移（例如内部户间的转账）。One-sided transfer of securities without a corresponding payment; e.g., internal transfers between accounts. |
| **T+1 / T+2 Settlement** | T+1/T+2结算 | 交易日后1天/2天结算；美国已于2024年迁移至T+1；香港股票为T+2。Settlement 1 or 2 business days after trade date. US equities moved to T+1 in 2024; HK equities settle T+2. |
| **DTCC** | 美国存托信托清算公司 | 美国股票和债券的中央结算机构，旗下包括NSCC（证券清算）和DTC（托管和结算）。US central clearing and settlement for equities and bonds; subsidiaries NSCC (clearing) and DTC (settlement/custody). |
| **Euroclear** | 欧洲清算行 | 总部位于比利时，是全球最大的证券结算系统之一，处理欧洲债券和股票结算。Belgium-based ICSDs; one of the world's largest securities settlement systems for Eurobonds and cross-border securities. |
| **Clearstream** | 清算流 | 德意志交易所旗下的国际中央证券存管机构，与Euroclear并列为欧洲两大ICSDs。Deutsche Börse subsidiary; another major ICSD alongside Euroclear. |
| **HKSCC** | 香港中央结算有限公司 | HKEX旗下子公司，负责香港上市证券的中央结算与托管，运营中央结算系统（CCASS）。HKEX subsidiary; clears and settles HK-listed securities via the Central Clearing and Settlement System (CCASS). |
| **ChinaClear** | 中国证券登记结算公司 | 负责A股、债券及基金等境内证券的登记、托管和结算服务。China's central securities depository and settlement body for A-shares, bonds, and mutual funds. |

---

## 8.5 金融报文协议 / Financial Messaging Protocols

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **FIX (Financial Information eXchange)** | 金融信息交换协议 | 证券行业广泛使用的电子交易报文标准，覆盖订单管理、执行报告、询价等；是EMS/OMS的核心通信协议。Industry-standard electronic messaging protocol for pre-trade, trade, and post-trade communications; backbone of EMS/OMS connectivity. |
| **SWIFT** | 环球银行间金融电信协会 | 全球银行间金融报文传输网络，负责跨行、跨境支付指令和确认的安全传输。Global secure messaging network for interbank financial communications; used for cross-border payments and confirmations. |
| **MT103** | — | SWIFT单笔客户汇款报文（国际电汇最常用类型）。SWIFT message for single customer credit transfer; the most common international wire transfer format. |
| **MT202** | — | SWIFT银行间资金转账报文，用于银行间清算支付。SWIFT interbank funds transfer message used for bank-to-bank clearing payments. |
| **MT300** | — | SWIFT外汇交易确认报文。SWIFT FX transaction confirmation message. |
| **MT571** | — | SWIFT证券资产负债报表（托管报文之一）。SWIFT securities statement of holdings; a custody message type. |
| **ISO 20022** | — | 新一代全球金融报文标准（XML格式），正逐步取代老式MT格式；更丰富的数据结构支持更智能的合规处理。Next-generation global financial messaging standard (XML-based); richer data structure; gradually replacing legacy MT messages globally. |
| **FpML (Financial Products Markup Language)** | 金融产品标记语言 | 专用于场外衍生品（利率掉期、CDS、期权等）的XML数据标准，用于交易确认和清算报告。XML-based messaging standard for OTC derivatives (IRS, CDS, options); used in trade confirmations and clearing reports. |

---

*上一阶段 / Prev: [Phase 07 — 风险管理](Phase-07-Risk-Management.md)*  
*下一阶段 / Next: [Phase 09 — Bloomberg终端与数据系统](Phase-09-Bloomberg.md)*
