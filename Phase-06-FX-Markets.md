# Phase 06 — 外汇市场
# Phase 06 — Foreign Exchange Markets

> **学习目标 / Learning Objectives**  
> 掌握外汇市场的报价惯例、主要产品类型、定价原理，以及人民币特有概念。  
> Master FX quoting conventions, major product types, pricing principles, and RMB-specific concepts.

---

## 6.1 外汇基础 / FX Basics

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **Base Currency** | 基础货币 | 货币对的第一个货币，报价以1单位基础货币等于多少报价货币表示。The first currency in a pair; the price expresses how much of the quote currency equals 1 unit of the base. E.g., in EUR/USD, EUR is base. |
| **Quote Currency (Terms Currency)** | 报价货币 | 货币对的第二个货币。The second currency in a pair. In EUR/USD, USD is the quote currency. |
| **Spot Rate** | 即期汇率 | 当前市场上两种货币的现时兑换汇率，通常T+2交割（USD/CAD为T+1，USD/RUB为T+1）。Current exchange rate for immediate delivery; conventionally settling T+2 (some pairs differ). |
| **Bid** | 买价 | 做市商愿意买入基础货币（卖出报价货币）的价格。Price at which the market maker buys the base currency. |
| **Ask / Offer** | 卖价 / 要价 | 做市商愿意卖出基础货币（买入报价货币）的价格。Price at which the market maker sells the base currency. |
| **Spread** | 买卖价差 | Ask − Bid；做市商的利润来源之一，流动性越好点差越窄。Ask minus Bid; a source of market-maker profit; tighter in liquid markets. |
| **Pip** | 点（最小变动单位） | 大多数货币对的最小报价单位（第四位小数，0.0001）；日元对为第二位小数（0.01）。Smallest price increment; 0.0001 for most pairs (4th decimal place); 0.01 for JPY pairs (2nd decimal). |
| **Big Figure** | 大整数位 | 汇率中不在日常报价中频繁引用的前几位数，例如EUR/USD=1.0825，大整数位为1.08。The whole number portion of the exchange rate not usually quoted in full. E.g., for 1.0825, "big figure" is 1.08. |
| **Major Pairs** | 主要货币对 | 以美元为一方的最常交易货币对，流动性最高；包括EUR/USD、GBP/USD、USD/JPY、USD/CHF、AUD/USD、USD/CAD、NZD/USD。Most liquid USD pairs: EUR/USD, GBP/USD, USD/JPY, USD/CHF, AUD/USD, USD/CAD, NZD/USD. |
| **Cross Rates** | 交叉汇率 | 不含美元的货币对，如EUR/GBP、EUR/JPY、AUD/JPY。These pairs do not involve USD: EUR/GBP, EUR/JPY, AUD/JPY, etc. |
| **Exotic Pairs** | 新兴市场货币对 | 新兴市场货币与主要货币的组合，流动性较低，点差较宽；如USD/TRY、USD/INR、USD/BRL。EM currencies paired with majors; lower liquidity, wider spreads. E.g., USD/TRY, USD/INR, USD/BRL. |

---

## 6.2 外汇产品 / FX Products

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **FX Spot** | 外汇即期 | 即时成交、T+2交割的外汇买卖（部分货币对交割日有所不同）。Immediate exchange of currencies; conventional value date T+2. |
| **FX Forward / Forward Outright** | 外汇远期 | 约定在未来特定日期以今天约定的汇率（远期汇率）进行外汇交割；常用于套期保值。Agreement to exchange currencies at a pre-agreed rate on a future date; commonly used for hedging. |
| **FX Swap** | 外汇掉期 | 同时进行一笔即期外汇交易和一笔方向相反的远期外汇交易；主要用于资金管理和展期。Simultaneous spot purchase and forward sale (or vice versa) of the same amount; primarily used for funding and rollover. |
| **NDF (Non-Deliverable Forward)** | 无本金交割远期 | 用于受资本管制的货币（如CNY、INR、KRW）的远期合约，到期只进行差价的美元现金结算，无实际本金交割。Forward on a restricted currency (CNY, INR, KRW); settled in USD based on the difference between NDF rate and fixing rate; no principal exchange. |
| **NDS (Non-Deliverable Swap)** | 无本金交割掉期 | 针对管制货币的外汇掉期，现金结算，不进行实际本金交换。Non-deliverable FX swap; cash-settled; no actual currency exchange. |
| **FX Option** | 外汇期权 | 买方获得在未来以特定汇率买入/卖出外汇的权利（非义务）；用于对冲汇率风险或投机。Right (not obligation) to buy/sell a currency pair at a pre-agreed rate by a certain date; used for hedging or speculation. |
| **Vanilla Option** | 普通期权 | 标准欧式或美式外汇期权。Standard European or American FX option. |
| **Risk Reversal** | 风险逆转 | 同时买入一个虚值认购期权、卖出一个虚值认沽期权（或反向组合）；反映市场对汇率方向的偏向。Buying an OTM call and selling an OTM put (or reversed); reflects market directional bias and skew. |
| **Straddle** | 跨式期权 | 同时买入相同行权价的认购和认沽期权；押注波动率上升，方向不限。Buying a call and put with the same strike; profits from large moves in either direction. |
| **Strangle** | 宽跨式期权 | 同时买入不同行权价（虚值）的认购和认沽期权；比Straddle费用低，但需要更大的价格变动获利。Buying OTM call and OTM put with different strikes; cheaper than straddle but requires larger move. |

---

## 6.3 外汇定价概念 / FX Pricing Concepts

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **Interest Rate Parity (IRP)** | 利率平价理论 | 两国利差决定远期汇率与即期汇率的关系：高息货币远期折价，低息货币远期升水。Interest rate differential determines the forward rate: high-rate currency trades at a forward discount; low-rate currency at a premium. |
| **Forward Rate** | 远期汇率 | 根据利率平价理论计算的未来交割汇率。Forward Rate = Spot × (1 + r_quote) / (1 + r_base) |
| **Forward Points / Swap Points** | 远期点数 / 掉期点 | 远期汇率与即期汇率之差（通常以点Pips表示）；由两国利率差决定。Difference between forward rate and spot rate (in pips); driven by interest rate differential. |
| **Premium / Discount** | 升水 / 贴水 | 若远期价格高于即期价格→升水；若低于→贴水。Forward > Spot → premium; Forward < Spot → discount. |
| **Purchasing Power Parity (PPP)** | 购买力平价 | 长期汇率理论：两国商品价格相同时的汇率水平；实际汇率若偏离PPP则存在均值回归压力。Long-run exchange rate theory: exchange rate should equalise prices of identical goods. Deviation from PPP creates mean-reversion pressure. |
| **Value Date** | 起息日 / 交割日 | 外汇交易中实际资金划拨的日期（Spot = T+2）。Date on which funds are transferred in an FX transaction. Spot = T+2 from trade date. |

---

## 6.4 人民币相关概念 / RMB-Specific Concepts

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **CNY** | 在岸人民币 | 在中国大陆境内流通和交易的人民币，受PBOC和SAFE严格管控，汇率在每日中间价±2%范围内波动。RMB traded within mainland China; tightly managed by PBOC; daily trading band ±2% vs. PBOC fixing. |
| **CNH** | 离岸人民币 | 在香港（及其他离岸中心如新加坡、伦敦）自由交易的人民币，由市场供需驱动，通常与CNY存在一定价差。RMB traded offshore (mainly Hong Kong, also Singapore/London); freely traded; rate may differ from CNY. |
| **USD/CNH** | 美元/离岸人民币 | 香港市场上美元兑离岸人民币的汇率，是目前全球最活跃的人民币汇率。USD vs. offshore RMB rate, traded in HK; most liquid RMB exchange rate globally. |
| **PBOC Fix / Central Parity Rate** | 中间价 | 中国人民银行每日上午公布的人民币兑美元参考汇率，在岸市场在此基础上±2%范围内交易。Daily reference rate set by PBOC each morning; onshore market trades within ±2% band. |
| **CFETS** | 中国外汇交易中心 | 隶属中国人民银行，负责运营银行间外汇市场、债券市场和货币市场的基础设施。China Foreign Exchange Trade System; PBOC-affiliated; operates interbank FX, bond, and money markets. |
| **CIPS** | 人民币跨境支付系统 | 人民币国际化的核心基础设施，提供跨境人民币清算结算，类似SWIFT。RMB cross-border payment infrastructure; supports RMB internationalisation; China's equivalent to SWIFT for RMB payments. |
| **CNY NDF** | 人民币无本金交割远期 | 在离岸市场以美元结算的人民币远期合约，在资本管制时代是主要的人民币汇率风险对冲工具（随CNH发展，使用有所减少）。USD-settled forward on CNY; historically the main offshore RMB hedging tool before CNH developed. |
| **Dim Sum Bond** | 点心债券 | 在香港市场以人民币（CNH）发行的债券，面向离岸人民币投资者。CNH-denominated bond issued in Hong Kong; named after the popular HK cuisine. |
| **Panda Bond** | 熊猫债券 | 外国机构在中国大陆境内市场以人民币发行的债券。RMB-denominated bond issued by a foreign entity in mainland China's domestic bond market. |

---

*上一阶段 / Prev: [Phase 05 — 衍生品与结构化产品](Phase-05-Derivatives.md)*  
*下一阶段 / Next: [Phase 07 — 风险管理](Phase-07-Risk-Management.md)*
