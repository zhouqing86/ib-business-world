# Phase 05 — 衍生品与结构化产品
# Phase 05 — Derivatives & Structured Products

> **学习目标 / Learning Objectives**  
> 掌握期权、期货、掉期的核心概念，理解希腊字母风险指标，并熟悉常见结构化产品。  
> Master options, futures, and swaps; understand the Greeks; familiarise yourself with common structured products.

---

## 5.1 期权基础 / Options Basics

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **Call Option** | 认购期权 | 买入权利：持有人有权（非义务）在到期日前以行权价买入标的资产。Right to BUY the underlying asset at the strike price on or before expiry. |
| **Put Option** | 认沽期权 | 卖出权利：持有人有权（非义务）在到期日前以行权价卖出标的资产。Right to SELL the underlying asset at the strike price on or before expiry. |
| **Premium** | 期权费 / 权利金 | 买方为获得期权权利向卖方支付的价格。Price paid by the buyer to the seller for the option right. |
| **Strike Price / Exercise Price** | 行权价 | 期权合约约定的买入或卖出标的资产的价格。The price at which the option holder can buy or sell the underlying. |
| **Expiration Date** | 到期日 | 期权权利终止的最后日期。The last date on which the option can be exercised. |
| **American Style** | 美式期权 | 可在到期日前任意时间行权。Can be exercised at any time before expiry. |
| **European Style** | 欧式期权 | 只能在到期日当天行权（多数场外期权及指数期权为欧式）。Can only be exercised on the expiry date itself. Most OTC and index options are European-style. |
| **ITM (In-the-Money)** | 实值 | 立即行权有内在价值：认购期权标的价格 > 行权价；认沽期权标的价格 < 行权价。Has intrinsic value if exercised now: call — spot > strike; put — spot < strike. |
| **ATM (At-the-Money)** | 平值 | 标的价格约等于行权价，内在价值接近零。Spot price ≈ strike price; intrinsic value near zero. |
| **OTM (Out-of-the-Money)** | 虚值 | 立即行权无内在价值：认购期权标的价格 < 行权价；认沽期权标的价格 > 行权价。No intrinsic value if exercised now: call — spot < strike; put — spot > strike. |
| **Intrinsic Value** | 内在价值 | 期权若立即行权可实现的价值（若为负则取零）。Value if exercised immediately (floored at zero). |
| **Time Value** | 时间价值 | 期权费中超出内在价值的部分，反映在到期前价格有利变动的可能性。Premium in excess of intrinsic value; reflects potential for favourable price movement before expiry. |

---

## 5.2 期权希腊字母 / The Greeks

希腊字母是衡量期权价格对不同风险因素敏感度的关键指标，是期权交易员日常管理风险的核心工具。  
The Greeks measure how an option's price responds to different risk factors — essential tools for options risk management.

| 希腊字母 | 英文 | 含义 | 说明 |
|----------|------|------|------|
| **Δ Delta** | Delta | 期权价格对标的资产价格变动$1的敏感度 | 认购期权Delta在0到1之间；认沽期权Delta在-1到0之间。例如：Delta=0.5表示标的价格上涨$1，期权价格上涨约$0.50。Call delta: 0 to +1; Put delta: -1 to 0. Delta=0.5 means a $1 rise in spot → ~$0.50 rise in option price. |
| **Γ Gamma** | Gamma | Delta对标的资产价格变动$1的敏感度（Delta的变化速度） | Gamma越高，Delta变化越快，风险对冲需要越频繁调整。Higher Gamma means faster Delta change; requires more frequent rehedging. |
| **Θ Theta** | Theta | 时间价值每日衰减率（时间损耗） | 期权买方每过一天损失Theta的时间价值；卖方每日获收Theta。Option buyers lose Theta daily (time decay); sellers collect it. Usually expressed as $ per day. |
| **ν Vega** | Vega | 期权价格对隐含波动率变动1%的敏感度 | Vega总为正：波动率上升，多头期权增值（无论认购还是认沽）。Always positive: both calls and puts gain value when implied volatility rises. |
| **ρ Rho** | Rho | 期权价格对无风险利率变动1%的敏感度 | 对于长期期权影响较大；短期期权Rho通常可忽略。More significant for long-dated options; often negligible for short-dated ones. |
| **IV (Implied Volatility)** | 隐含波动率 | 从当前期权市场价格反推出的标的资产未来波动率预期 | IV高代表市场预期波动大（通常在不确定性高时上升）；VIX即为S&P 500的30天隐含波动率。High IV indicates market expects large moves; VIX is 30-day implied vol of S&P 500. |
| **HV (Historical Volatility)** | 历史波动率 | 标的资产过去实际价格波动的统计量（通常为年化标准差） | 用于与IV比较，判断期权是否被高估或低估。Compared with IV to assess whether options are over- or under-priced. |
| **Volatility Skew** | 波动率偏斜 | 不同行权价的隐含波动率不同所呈现的非对称形态 | 股票期权通常呈左偏（虚值认沽期权IV高于虚值认购期权），反映尾部风险保护需求。Equities typically show negative skew (higher IV for OTM puts); reflects demand for downside protection. |
| **Volatility Surface** | 波动率曲面 | 将不同行权价和不同到期日的隐含波动率三维展示的曲面 | 期权交易员用波动率曲面进行定价和风险管理。A 3D representation of IV across strikes and maturities; used for option pricing and risk management. |

---

## 5.3 期货与远期 / Futures & Forwards

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **Futures Contract** | 期货合约 | 在交易所标准化的协议，约定在未来特定日期以特定价格买卖资产；每日盯市结算（MTM）。Standardised exchange-traded agreement to buy/sell an asset at a set price on a future date; daily MTM settlement. |
| **Forward Contract** | 远期合约 | 买卖双方场外协商的定制化协议，约定在未来特定日期以约定价格交割；无需每日结算，到期一次性结算。OTC customised bilateral agreement; no daily settlement; settled at maturity. |
| **Mark-to-Market (Daily Settlement)** | 每日盯市结算 | 期货合约每日按结算价重估，盈亏每日通过保证金账户划拨。Daily revaluation of futures; gains/losses transferred via margin accounts each day. |
| **Initial Margin** | 初始保证金 | 开仓时须存入的最低保证金，作为履约担保。Minimum deposit required to open a futures position; serves as performance bond. |
| **Variation Margin / Maintenance Margin** | 变动保证金 | 当账户保证金因亏损低于维持保证金水平时，须追加的资金。Additional funds required when account equity falls below the maintenance margin level due to losses. |
| **Margin Call** | 追加保证金通知 | 当保证金账户余额不足时，交易所或经纪商要求客户补充保证金的通知。Demand from a broker/exchange to deposit additional funds when margin balance falls below required level. |
| **Rollover** | 移仓换月 | 在近月合约到期前，将持仓从近月移至远月合约，以维持头寸。Closing a near-month contract and opening a far-month contract to maintain a continuous position. |
| **Basis** | 基差 | 现货价格与期货价格之差（Basis = Spot − Futures）。Difference between spot price and futures price: Basis = Spot − Futures. |
| **Contango** | 正价差 | 远期价格高于现货价格，收益率曲线向上倾斜；长期滚动仓将承受负收益。Futures price > spot price; typically seen in storable commodities; creates negative roll yield for long positions. |
| **Backwardation** | 反价差 / 期货贴水 | 远期价格低于现货价格；近期供应紧张时常见。Futures price < spot price; often reflects near-term supply shortage. |

---

## 5.4 掉期 / Swaps

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **IRS (Interest Rate Swap)** | 利率互换 | 双方约定交换固定利率与浮动利率现金流，名义本金不交换；用于利率风险管理。Exchange of fixed-rate cash flows for floating-rate cash flows on a notional principal; used to manage interest rate risk. |
| **CCS (Cross-Currency Swap)** | 跨货币互换 | 双方交换不同货币的本金和利息；到期时以初始汇率换回本金；用于管理跨货币融资风险。Exchange of principal and interest payments in different currencies; principal re-exchanged at maturity. Used for cross-currency funding management. |
| **CDS (Credit Default Swap)** | 信用违约互换 | 信用保护买方向卖方支付CDS利差（保费），一旦参考实体发生信用事件，卖方补偿买方损失。Protection buyer pays a periodic spread (premium) to the seller; upon a credit event on the reference entity, seller compensates buyer. Like insurance on a bond. |
| **TRS (Total Return Swap)** | 总收益互换 | 一方支付资产的总回报（利息+资本利得/损失），另一方支付固定/浮动利率；无需实际持有资产。One party pays total return of an asset (coupons + price change); other pays fixed/floating rate; synthetic exposure without owning the asset. |
| **OIS (Overnight Index Swap)** | 隔夜指数互换 | 双方交换固定利率与隔夜参考利率（如SOFR、HONIA）复利累积的浮动利率。Exchange of fixed rate for the compounded overnight reference rate (SOFR, HONIA, etc.). Used as a proxy for risk-free rate. |
| **Fixed Leg** | 固定端 | 掉期中支付固定利率的一方所产生的现金流序列。The stream of fixed-rate payments in a swap. |
| **Floating Leg** | 浮动端 | 掉期中支付浮动利率（通常与SOFR/HIBOR挂钩）的一方所产生的现金流序列。The stream of floating-rate payments, typically linked to SOFR, HIBOR, etc. |
| **Swap Rate** | 掉期利率 | 使IRS公允价值为零时的固定利率水平；也是市场对未来浮动利率走势的预期体现。The fixed rate at which an IRS has zero fair value at inception; reflects market expectations for future floating rates. |
| **Swap Spread** | 掉期利差 | 掉期固定利率与同期限国债收益率之差；反映银行间信用风险溢价。Difference between the swap rate and the yield on a government bond of the same tenor; reflects interbank credit risk. |

---

## 5.5 结构化产品 / Structured Products

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **CDO (Collateralized Debt Obligation)** | 担保债务凭证 | 将不同信用质量的债务资产打包，分层（Tranche）发行；各档次承担不同级别的损失。Pool of debt assets tranched into different risk levels; lower tranches absorb losses first. |
| **CLO (Collateralized Loan Obligation)** | 担保贷款凭证 | 以企业贷款（通常是杠杆贷款）为资产池的CDO；CLO是后危机时代杠杆融资的主要工具。CDO backed by corporate loans (typically leveraged loans); the dominant leveraged finance vehicle post-GFC. |
| **ABS (Asset-Backed Security)** | 资产支持证券 | 以信用卡应收款、汽车贷款等消费类资产为抵押发行的证券。Security backed by pools of consumer assets such as credit card receivables, auto loans, student loans. |
| **MBS (Mortgage-Backed Security)** | 抵押支持证券 | 以住宅或商业抵押贷款为资产池发行的证券。Security backed by pools of mortgage loans (residential: RMBS; commercial: CMBS). |
| **CLN (Credit-Linked Note)** | 信用挂钩票据 | 将CDS嵌入债券的结构：投资者承担参考实体的信用风险，获取更高收益。Bond embedding a CDS; investor takes on credit risk of a reference entity in exchange for a higher yield. |
| **Principal Protected Note (PPN)** | 保本票据 | 到期保证偿还本金，同时提供与标的资产挂钩的额外收益；通过零息债券+期权构建。Guarantees return of principal at maturity while offering upside linked to an underlying; constructed via zero-coupon bond + option. |
| **Autocallable** | 自动赎回结构 | 若标的资产在观察日高于触发价，产品提前偿还本金并支付溢价；否则继续到到期日。If the underlying is above a trigger level on observation dates, the product redeems early at a premium; otherwise continues to maturity. |
| **Knock-In Option** | 敲入期权 | 标的资产价格触及障碍价格时期权才开始生效（激活）。Option that only becomes active (is "knocked in") when the underlying touches a barrier level. |
| **Knock-Out Option** | 敲出期权 | 标的资产价格触及障碍价格时期权立即失效（被敲出）。Option that ceases to exist (is "knocked out") when the underlying touches a barrier level. |

---

*上一阶段 / Prev: [Phase 04 — 权益市场](Phase-04-Equity-Markets.md)*  
*下一阶段 / Next: [Phase 06 — 外汇市场](Phase-06-FX-Markets.md)*
