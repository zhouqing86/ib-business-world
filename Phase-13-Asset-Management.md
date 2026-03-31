# Phase 13 — 资产管理与基金
# Phase 13 — Asset Management & Funds

> **学习目标 / Learning Objectives**  
> 掌握各类基金的结构与特点、投资组合管理核心指标，以及对冲基金常见策略。  
> Master fund structures and characteristics, core portfolio management metrics, and common hedge fund strategies.

---

## 13.1 基金类型 / Fund Types

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **Mutual Fund** | 共同基金 | 向众多散户投资者募集资金、由专业基金经理管理的开放式基金；通常每日以NAV定价申购赎回。Open-end fund pooling money from retail investors; managed professionally; priced daily at NAV; redeemable on demand. |
| **UCITS** | 欧盟可转让证券集体投资 | 欧盟标准化的零售基金结构（Undertakings for Collective Investment in Transferable Securities）；高流动性要求，每日可赎回；可在欧盟跨境分销。EU-regulated retail fund structure; high liquidity requirements; daily redemption; can be sold cross-border in EU (and widely in Asia). |
| **ETF (Exchange-Traded Fund)** | 交易所交易基金 | 在交易所上市交易的开放式基金，通常追踪指数；兼具基金分散投资和股票交易便利的优点；费率低廉。Open-end fund listed on exchange; typically index-tracking; combines diversification of a fund with tradability of a stock; low cost. |
| **Closed-End Fund / Investment Trust** | 封闭式基金 | 发行固定数量份额，在交易所上市交易；市价可能高于或低于NAV（溢价/折价交易）。Issues fixed number of shares, listed on exchange; market price may trade at premium or discount to NAV. |
| **Hedge Fund** | 对冲基金 | 面向合格投资者（专业投资者）的私募基金，通常使用杠杆、做空和衍生品，追求绝对回报；监管相对宽松，费用结构为"2和20"（2%管理费+20%业绩分成）。Private fund for qualified (professional/accredited) investors; uses leverage, shorting, and derivatives for absolute returns; typically "2 and 20" fee structure. |
| **Private Equity (PE)** | 私募股权 | 投资非上市公司股权，通常持有期限5-7年，通过IPO/并购退出实现收益；主要策略包括LBO、成长型投资、风险投资。Invests in private (unlisted) company equity; typical hold 5–7 years; exits via IPO/M&A; strategies include LBO, growth equity, VC. |
| **Venture Capital (VC)** | 风险投资 | PE的子类别：专注于早期（种子、A/B/C轮）高成长技术或科技驱动公司，高风险高回报。Subset of PE focused on early-stage (seed, Series A/B/C) high-growth companies; high risk, high potential return. |
| **Real Estate Fund** | 房地产基金 | 投资实体房产（直接投资）或房地产相关证券（REIT等）的基金。Fund investing in physical properties (direct) or real estate-related securities (REITs, etc.). |
| **REIT (Real Estate Investment Trust)** | 房地产投资信托基金 | 持有产收益房产并将大部分租金收入作为股息分配给投资者的上市基金；在香港备受欢迎（Link REIT等）。Listed fund owning income-producing real estate; distributes most rental income as dividends; popular in HK (e.g., Link REIT 823.HK). |
| **Infrastructure Fund** | 基础设施基金 | 投资于道路、港口、机场、公用事业等基础设施资产的基金；现金流稳定、与市场相关性低。Fund investing in roads, ports, airports, utilities; stable cash flows, low market correlation. |
| **SWF (Sovereign Wealth Fund)** | 主权财富基金 | 政府控制的投资基金，以外汇储备或自然资源收入为资本；著名SWF包括挪威政府养老基金（全球最大）、中国投资公司（CIC）、GIC（新加坡）、阿布扎比投资局（ADIA）。Government-owned investment fund capitalised by FX reserves or natural resource revenues; examples: Norway GPFG (world's largest), CIC (China), GIC (Singapore), ADIA (Abu Dhabi). |
| **Pension Fund** | 养老基金 | 为未来退休支付养老金而管理的长期资产池；是全球最大的机构投资者群体之一。Long-term pool of assets to fund future pension benefit payments; one of the largest institutional investor classes globally. |

---

## 13.2 基金结构术语 / Fund Structure Terms

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **LP (Limited Partner)** | 有限合伙人 | PE/对冲基金的出资方（投资者），仅以出资额为限承担责任，不参与基金管理。Fund investors in PE/hedge funds; liability limited to invested capital; do not manage the fund. |
| **GP (General Partner)** | 普通合伙人 | 基金管理人，对基金决策和运营负无限责任；承担管理费和业绩分成。Fund manager; has unlimited liability; earns management fee and carried interest. |
| **Management Fee** | 管理费 | 基金管理人按AUM的固定百分比（通常1-2%/年）收取的基础服务费用。Annual fee charged by fund manager as a percentage of AUM (typically 1–2% p.a.). |
| **Carried Interest (Carry)** | 业绩分成 / 附带权益 | GP从基金超额收益中获取的分成（通常20%）；仅在超越门槛收益率（Hurdle Rate）后才计算。GP's share of fund profits above the hurdle rate; typically 20%; the primary incentive for fund managers. |
| **Hurdle Rate (Preferred Return)** | 门槛收益率 / 优先回报率 | LP首先须获得的目标年化回报率（通常8%）；超过门槛后GP才参与业绩分成。Minimum annual return (typically 8%) that LPs must receive before the GP starts taking carried interest. |
| **High-Water Mark** | 最高水位线 | 基金历史上曾达到的最高NAV；只有新的盈利（突破高水位线的部分）才计提业绩分成；防止基金对从之前亏损中恢复的部分重复收分成。Highest NAV previously achieved; performance fees only charged on new profits above this level; prevents double-charging on recovered losses. |
| **Clawback** | 追回条款 | 若基金最终整体表现未达到约定收益率，GP须将已分配的业绩分成部分归还给LP的条款。Provision requiring GP to return previously received carried interest if the fund's overall performance falls below committed return. |
| **Vintage Year** | 年份 | PE基金首次对外投资（或募资完成）的年份，用于比较不同年份基金的业绩。Year a PE fund makes its first investment or closes; used to benchmark fund performance within the same vintage cohort. |
| **DPI (Distributions to Paid-In)** | 已分配与实缴资本比 | 基金已向LP分配的现金 / LP的实缴资本；衡量实际已实现回报。Cash distributed to LPs / LP paid-in capital; measures actual realised returns. |
| **TVPI (Total Value to Paid-In)** | 总价值与实缴资本比 | (已分配 + 剩余净值) / 实缴资本；综合衡量已实现和未实现的总回报。(Distributions + Residual NAV) / Paid-In Capital; measures total (realised + unrealised) returns. |
| **IRR (Internal Rate of Return)** | 内部收益率 | PE基金常用的回报衡量指标，考虑资金的时间价值和现金流时序。Most common PE return metric; accounts for timing of cash flows and time value of money. |

---

## 13.3 投资组合管理 / Portfolio Management

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **Asset Allocation** | 资产配置 | 在不同资产类别（股票、债券、现金、另类投资等）之间分配投资资金的决策过程。Decision of how to allocate capital across asset classes (equities, bonds, cash, alternatives). |
| **SAA (Strategic Asset Allocation)** | 战略性资产配置 | 基于长期风险/收益目标制定的资产配置中枢（锚定配置）；相对稳定，定期审视。Long-term target asset mix based on risk/return objectives; relatively stable; reviewed periodically. |
| **TAA (Tactical Asset Allocation)** | 战术性资产配置 | 在SAA基础上，根据短期市场预期进行的动态偏离（超配/低配）；寻求短期阿尔法。Short-term deviations from SAA based on near-term market views (overweight/underweight); aims to generate short-term alpha. |
| **Benchmark** | 基准 | 用于衡量投资组合业绩的参考指数（如MSCI World、Bloomberg Global Aggregate）。Reference index against which a portfolio's performance is measured (e.g., MSCI World, Bloomberg Global Agg). |
| **Alpha (α)** | 阿尔法 / 超额收益 | 投资组合回报率超出基准（经β调整后）的部分；主动管理的核心目标。Portfolio return in excess of the benchmark (after adjusting for beta); the primary goal of active management. |
| **Beta (β)** | 贝塔 / 市场风险系数 | 投资组合相对于市场（基准）波动的敏感度；β=1表示与市场同步波动。Portfolio's sensitivity to market (benchmark) moves; β=1 means same volatility as market. |
| **Tracking Error** | 跟踪误差 | 投资组合回报与基准回报之差的标准差；衡量主动管理程度和偏离基准的幅度。Standard deviation of the difference between portfolio and benchmark returns; measures degree of active positioning. |
| **Information Ratio (IR)** | 信息比率 | 超额收益（Alpha）/ 跟踪误差；衡量主动管理每单位跟踪误差带来的超额回报效率。Alpha / Tracking Error; measures active management efficiency (alpha generated per unit of tracking error). |
| **Sharpe Ratio** | 夏普比率 | (组合回报 − 无风险利率) / 组合标准差；衡量每单位总风险的超额风险溢价。(Return − Risk-free rate) / Standard deviation; measures excess return per unit of total risk. |
| **Sortino Ratio** | 索提诺比率 | (组合回报 − 目标收益率) / 下行标准差；只惩罚下行波动（负偏差），比夏普比率更关注风险保护。(Return − Target return) / Downside deviation; penalises only downside volatility; gives a better picture of downside risk management. |
| **Maximum Drawdown (MDD)** | 最大回撤 | 投资组合从历史最高点到随后最低点的最大跌幅；衡量投资者在最坏时期可能经历的最大亏损。Largest peak-to-trough decline in portfolio value; measures worst-case loss an investor could have experienced. |
| **Rebalancing** | 再平衡 | 定期将偏离目标配置的资产类别买回/卖出，使组合恢复至战略配置目标的操作。Buying/selling assets to restore allocation to target weights when market moves cause deviation from SAA. |

---

## 13.4 对冲基金策略 / Hedge Fund Strategies

| 策略 | 英文 | 说明 |
|------|------|------|
| **多空权益** | Long/Short Equity | 同时持有预期上涨的多头（Long）和预期下跌的空头（Short）股票，可对冲部分市场风险；净敞口可正可负。Simultaneously holds long positions in expected outperformers and short positions in expected underperformers; partial hedge against market moves. |
| **市场中性** | Market Neutral | 严格控制净市场敞口接近零；通过精选个股的多空组合获取阿尔法，消除市场Beta风险。Maintains net market exposure near zero; seeks alpha purely from stock selection; eliminates market beta. |
| **全球宏观** | Global Macro | 基于对宏观经济趋势（利率、汇率、大宗商品、权益大势）的判断进行跨资产类别的方向性交易；索罗斯的量子基金是典型代表。Directional trading across asset classes based on macroeconomic forecasts (rates, FX, commodities, equities); Soros's Quantum Fund is the classic example. |
| **CTA / 管理期货** | Managed Futures / CTA | 通过期货合约在大宗商品、货币、利率、股指等市场进行趋势跟踪（Trend Following）策略；牛市熊市均可获利。Systematic trend-following using futures across commodities, FX, rates, and equity indices; can profit in both bull and bear markets. |
| **事件驱动** | Event-Driven | 围绕企业特定事件（并购、重组、破产、分拆等）进行投资。Invests around specific corporate events: M&A, restructurings, distressed situations, spinoffs. |
| **并购套利** | Merger Arbitrage | 收购宣布后，买入目标公司股票（通常按略低于收购价交易）、做空收购方股票，锁定套利价差。After M&A announcement, buys target and shorts acquirer; earns the spread between market price and deal price. |
| **困境债** | Distressed Investing | 以折价购买面临财务困境（破产重组）的公司债券或贷款，期望在重组后获取价值恢复的收益。Buys bonds or loans of financially distressed companies at deep discounts; profits if company value recovers through restructuring. |
| **固收套利** | Fixed Income Arbitrage | 利用固定收益市场中同类证券（国债、掉期、回购）间的相对价值错误定价获利；通常使用高杠杆。Exploits pricing discrepancies in fixed income markets (gov bonds, swaps); typically uses high leverage to amplify small spreads. |
| **统计套利** | Statistical Arbitrage (Stat Arb) | 利用历史统计规律和数量模型识别相关证券间的短暂价格偏差并进行快速交易获利；通常是高频或中频策略。Uses quantitative models to identify and exploit short-term pricing deviations among related securities; often HFT or medium-frequency. |
| **相对价值** | Relative Value | 广义策略：在相关联的证券间（如可转债与股票、新旧债券之间）识别和利用相对定价错误。Broad strategy: identifying and exploiting relative mispricing between related securities (e.g., CB vs. equity, on-the-run vs. off-the-run bonds). |

---

*上一阶段 / Prev: [Phase 12 — 投资银行与资本市场](Phase-12-Investment-Banking.md)*  
*下一阶段 / Next: [Phase 14 — 高级交易与金融科技](Phase-14-Advanced-Trading.md)*
