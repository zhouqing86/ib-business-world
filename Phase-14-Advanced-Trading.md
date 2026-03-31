# Phase 14 — 高级交易与金融科技
# Phase 14 — Advanced Trading & FinTech

> **学习目标 / Learning Objectives**  
> 掌握算法交易、高频交易、主经纪商服务、证券融资和回购的核心概念，了解主流交易系统架构，以及数字资产和央行数字货币的新兴术语。  
> Master algorithmic trading, HFT, prime brokerage, securities financing, core trading system architecture, and emerging digital asset/CBDC terminology.

---

## 14.1 算法与高频交易 / Algorithmic & High-Frequency Trading

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **Algorithmic Trading (Algo)** | 算法交易 | 使用计算机程序依据预设规则（时间、成交量、价格等）自动执行交易指令；减少人工干预和执行偏差。Using computer programs to execute trades automatically based on pre-defined rules (time, volume, price); reduces human intervention and execution slippage. |
| **HFT (High-Frequency Trading)** | 高频交易 | 以极低延迟（微秒级）大量快速买卖，日内持仓时间极短；通常依赖主机托管（Co-location）获取速度优势；占美国股市成交量约50%。Trading at extremely low latency (microseconds), high volume, very short holding periods; relies on co-location for speed advantage; ~50% of US equities volume. |
| **Co-location** | 主机托管 | 将交易服务器放置在交易所机房内，以最短物理距离获得最快网络延迟；HFT的核心基础设施。Placing trading servers inside exchange data centres; minimises physical distance and network latency; essential HFT infrastructure. |
| **Latency** | 延迟 | 从信号产生到指令送达交易所被执行之间的时间差；延迟越低竞争优势越大。Time lag from signal generation to order execution; lower latency = competitive advantage in HFT. |
| **Market Making (做市)** | 做市商业务 | 同时报出买价和卖价，为市场提供流动性；从买卖价差（Spread）中获利；需要对冲Delta和其他风险。Simultaneously quoting bid and ask prices to provide liquidity; profits from the bid-ask spread; requires hedging delta and other risks. |
| **Statistical Arbitrage (Stat Arb)** | 统计套利 | 基于历史统计规律，对相关资产的短暂价格偏差进行系统化交易；通常经市场中性设计。Systematically exploits short-term pricing deviations among related assets based on statistical patterns; usually market-neutral. |
| **Pairs Trading** | 配对交易 | 做多历史相关性高但暂时表现落后的股票，同时做空领先的股票；押注两者价差均值回归。Long the historically correlated stock that has underperformed; short the one that has outperformed; bets on mean reversion of the spread. |
| **Momentum Strategy** | 动量策略 | 买入近期表现强势（上升动量）的资产，空头近期弱势资产；趋势追踪的核心逻辑。Buy recent outperformers; short recent underperformers; core logic of trend-following. |
| **Mean Reversion** | 均值回归 | 资产价格偏离历史均值后倾向于回归均值的统计现象；是统计套利和配对交易的理论基础。Statistical tendency for asset prices to revert to their historical mean after deviating; foundational for stat arb and pairs trading. |
| **Backtesting** | 回测 | 用历史数据验证交易策略的历史表现；过拟合（Overfitting）是回测的主要风险。Testing a trading strategy against historical data to evaluate past performance; overfitting is a major risk. |

---

## 14.2 主经纪商服务 / Prime Brokerage

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **Prime Broker (PB)** | 主经纪商 | 为对冲基金提供一站式综合服务的大型投资银行部门；服务包括证券借贷、保证金融资、结算托管、风险报告等。Major investment bank division offering bundled services to hedge funds: securities lending, margin financing, settlement, custody, risk reporting. |
| **Securities Lending** | 证券借贷 | 证券持有人（通常是养老基金、长线基金）将证券出借给借券方（通常是做空者或PB），收取借券费；借券方提供现金或证券作为抵押品。Securities owner (pension/long-only fund) lends securities to borrower (short seller/PB) for a fee; borrower posts cash or securities as collateral. |
| **Short Selling** | 卖空 / 做空 | 借入证券后在市场卖出，预期价格下跌后以更低价格买回、归还借入证券并获取差价利润。Borrowing securities, selling them in the market, then buying them back at a lower price to return to the lender; profits from price decline. |
| **Margin Financing / Margin Lending** | 保证金融资 | PB向对冲基金提供贷款用于购买证券，以所购证券作为抵押；允许基金放大投资规模（杠杆）。PB provides loans to hedge funds to purchase securities, using those securities as collateral; enables funds to amplify investment size (leverage). |
| **Rehypothecation** | 再质押 | PB将客户（对冲基金）提交的抵押品再次用作自身的融资抵押；放大杠杆但增加系统性风险。PB using client's collateral as its own collateral for PB's financing needs; increases system leverage and systemic risk (major issue in 2008 GFC). |
| **Gross Leverage** | 总杠杆率 | (多头头寸总市值 + 空头头寸总市值) / 基金净资产值；衡量基金的全部市场敞口总量。(Long positions + Short positions) / Net Asset Value; measures total market exposure. |
| **Net Leverage** | 净杠杆率 | (多头头寸总市值 − 空头头寸总市值) / 基金净资产值；衡量基金的净方向性敞口。(Long positions − Short positions) / NAV; measures net directional exposure. |
| **Prime Brokerage Agreement (PBA)** | 主经纪商协议 | 对冲基金与PB签订的综合服务协议，规定融资条款、抵押品要求、保证金率等。Master agreement between hedge fund and PB governing financing terms, collateral requirements, margin rates, etc. |

---

## 14.3 回购与证券融资 / Repo & Securities Finance

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **Repo Rate** | 回购利率 | 回购交易中卖方（资金需求方）支付的隐含利率；等于(回购价 − 即期价) / 即期价 × 360/天数。Implied interest rate in a repo transaction; = (Repo price − Spot price) / Spot price × 360/days. |
| **GC Repo (General Collateral)** | 一般抵押品回购 | 以任何合格、标准化抵押品（通常为国债）进行的回购；利率接近无风险利率；用于一般短期资金管理。Repo using any eligible, standardised collateral (typically government bonds); rate close to risk-free; used for general short-term funding. |
| **Special Repo** | 特殊回购（特殊券回购） | 针对特定高需求债券（如被大量做空的在途国债）的回购；利率低于GC（借券需求方愿意接受更低的融资成本换取特定券）。Repo on a specific, high-demand bond (e.g., heavily shorted on-the-run Treasury); rate is below GC as the bond borrower accepts a lower funding rate to obtain the specific security. |
| **Haircut** | 折扣率（抵押品打折） | 抵押品市值与可获得资金之间的百分比差额；例如：5%折扣意味着100元市值债券只能融得95元现金；保护资金提供方免受抵押品价格下跌损失。Percentage difference between collateral market value and cash received; e.g., 5% haircut: USD100 bond → USD95 cash; protects cash lender from collateral price falls. |
| **Collateral Transformation** | 抵押品转换 | 机构将低质量抵押品（如公司债）换成高质量抵押品（HQLA，如国债）以满足CCP或监管要求；通常由银行作为中介。Converting lower-quality collateral (corporates) into higher-quality assets (HQLAs like govts) to meet CCP/regulatory margin requirements; banks act as intermediaries. |
| **Tri-Party Repo** | 三方回购 | 由第三方代理机构（如Euroclear、BNY Mellon）管理抵押品选择和转让的回购安排；简化操作流程。Repo where a third-party agent (e.g., Euroclear, BNY Mellon) manages collateral selection, allocation, and substitution; simplifies operations. |
| **Securities Finance** | 证券融资 | 证券借贷、回购/逆回购及其他以证券为基础的融资活动的统称。Collective term for securities lending, repo/reverse repo, and related collateralised financing activities. |

---

## 14.4 核心交易系统架构 / Core Trading System Architecture

| 缩写 | 全称 | 中文 | 说明 |
|------|------|------|------|
| **OMS** | Order Management System | 订单管理系统 | 管理交易指令全生命周期（从投资决策到执行再到分配）的系统；通常由资产管理公司使用（如Charles River、Aladdin）。Manages the full order lifecycle from investment decision through execution to allocation; used by asset managers (e.g., Charles River, BlackRock Aladdin). |
| **EMS** | Execution Management System | 执行管理系统 | 专注于交易执行的系统：与多家交易商/交易所连接、提供实时行情、执行算法；通常由交易台直接操作（如Fidessa、Bloomberg EMS）。Execution-focused system for real-time trading: connects to multiple brokers/exchanges, provides market data, runs algos; used at the trading desk (e.g., Fidessa). |
| **PMS** | Portfolio Management System | 投资组合管理系统 | 管理投资组合持仓、资产配置和绩效归因的系统。System managing portfolio positions, asset allocation, and performance attribution. |
| **TCA** | Transaction Cost Analysis | 交易成本分析 | 对比实际执行价格与基准价格（VWAP、到达价格等）评估交易执行质量；指导算法选择和经纪商评级。Measures execution quality by comparing actual fill prices to benchmarks (VWAP, arrival price, etc.); guides algo selection and broker evaluation. |
| **DMA** | Direct Market Access | 直接市场接入 | 允许机构客户直接向交易所提交订单（绕过经纪商交易台），得到更快的执行速度和更低成本。Allows institutional clients to submit orders directly to the exchange (bypassing broker trading desk) for faster execution and lower cost. |
| **SOR** | Smart Order Routing | 智能订单路由 | 在多个交易场所（交易所、暗池）中自动寻找最优价格和流动性，将订单路由至最佳目的地。Automatically routes orders to the venue(s) offering best price and liquidity across multiple exchanges and dark pools. |
| **FIX Engine** | FIX引擎 | 实现FIX协议通信的软件模块，是OMS、EMS与经纪商/交易所系统连接的标准接口。Software implementing FIX protocol messaging; standard connectivity interface between OMS/EMS and broker/exchange systems. |
| **Risk Gateway** | 风控网关 | 在订单发送到市场前进行实时风险检查的中间层系统（如持仓限额、暴露量检验、压力测试）。Pre-trade risk check layer that validates orders against risk limits (position limits, exposure checks) before they reach the market. |

---

## 14.5 ESG与可持续金融 / ESG & Sustainable Finance

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **ESG** | Environmental, Social, Governance | 环境、社会和公司治理 | 评估企业非财务风险和可持续发展能力的三大维度；正成为机构投资决策的重要因素。Three dimensions for assessing non-financial risks and sustainability of a company; increasingly important in institutional investment decisions. |
| **Green Bond** | 绿色债券 | 募集资金专项用于符合资质的环境/气候项目；须遵循国际资本市场协会（ICMA）绿色债券原则。Bond where proceeds are exclusively used for eligible environmental/climate projects; follows ICMA Green Bond Principles. |
| **Sustainability-Linked Bond (SLB)** | 可持续发展挂钩债券 | 债券的财务特征（票息）与发行人实现预设可持续发展绩效目标（SPTs）挂钩；若未达标则票息上调。Bond whose financial characteristics (coupon) are linked to the issuer's achievement of sustainability performance targets (SPTs); coupon steps up if targets are missed. |
| **Carbon Credit / Carbon Offset** | 碳信用 / 碳抵消 | 代表减少或消除一吨CO₂排放的可交易凭证；企业购买碳信用来抵消自身排放。Tradeable certificate representing a reduction or removal of one ton of CO₂; purchased by companies to offset their emissions. |
| **Taxonomy** | 分类标准 | 界定哪些经济活动被认定为"可持续"的监管框架（如欧盟绿色分类法EU Taxonomy）。Regulatory framework defining which economic activities qualify as "sustainable" (e.g., EU Taxonomy). |

---

## 14.6 数字资产与央行数字货币 / Digital Assets & CBDC

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **CBDC (Central Bank Digital Currency)** | 央行数字货币 | 由中央银行发行的法定数字货币；与加密货币不同，CBDC有主权信用背书；是现金的数字形式。Legal tender digital currency issued by a central bank; unlike crypto, backed by sovereign credit; digital form of physical cash. |
| **e-CNY (Digital RMB)** | 数字人民币 | 中国人民银行发行的零售型CBDC；通过商业银行向公众分发；已在上海、北京等多城市试点。Retail CBDC issued by PBOC; distributed to public via commercial banks; piloted in multiple Chinese cities. |
| **e-HKD** | 数字港元 | 香港金管局（HKMA）正在探索的零售型CBDC项目；目前处于研究和试验阶段。Retail CBDC being explored by HKMA; currently in research and pilot phase. |
| **mBridge** | 多边央行数字货币桥 | 由HKMA、PBOC、阿联酋中央银行、泰国银行共同开发的跨境批发型CBDC基础设施，旨在提升跨境支付效率；基于分布式账本技术（DLT）。Cross-border wholesale CBDC infrastructure jointly developed by HKMA, PBOC, UAE CB, and Bank of Thailand; aims to improve cross-border payment efficiency; DLT-based. |
| **Tokenisation of Assets** | 资产代币化 | 将传统金融资产（股票、债券、房产等）转化为区块链上的数字代币；提升流动性、降低结算成本、24/7交易。Converting traditional assets (equities, bonds, real estate) into digital tokens on a blockchain; improves liquidity, reduces settlement costs, enables 24/7 trading. |
| **DLT (Distributed Ledger Technology)** | 分布式账本技术 | 跨多个节点共享、复制和同步的数字记录系统；区块链是DLT的一种具体实现形式。Digital record-keeping system shared, replicated, and synchronised across multiple nodes; blockchain is one implementation of DLT. |
| **Smart Contract** | 智能合约 | 在区块链上自动执行的程序化合约；无需中介、在满足预设条件时自动触发条款执行。Self-executing contract code on blockchain; executes automatically when pre-defined conditions are met; eliminates intermediaries. |
| **DeFi (Decentralised Finance)** | 去中心化金融 | 基于区块链的金融应用生态：无需传统中介即可完成借贷、交易、衍生品等金融功能；目前主要依托以太坊生态。Blockchain-based financial applications enabling lending, trading, and derivatives without traditional intermediaries; primarily built on Ethereum. |
| **RegTech** | 监管科技 | 利用人工智能、大数据、区块链等技术提升合规效率和监管报告质量的科技解决方案。Technology solutions using AI, big data, and blockchain to improve compliance efficiency and regulatory reporting quality. |
| **Open Banking** | 开放银行 | 银行通过API向第三方（经授权的金融科技公司）开放客户账户数据（须客户授权）的数字生态系统；英国PSD2推动了全球开放银行发展。Banks opening customer account data to authorised third parties (fintechs) via APIs; driven by UK PSD2 and replicated globally; powers account aggregation, payments initiation, and personalised financial services. |

---

## 附录：资深交易员常用行语 / Appendix: Senior Trader Lingo

| 行语 | 中文 | 含义 |
|------|------|------|
| **"Hit the bid"** | 打买盘 | 以对方的买价成交（卖出）；通常表示急于出货。Selling at the buyer's quoted bid price; implies urgency to sell. |
| **"Lift the offer"** | 拿卖盘 | 以对方的卖价成交（买入）；表示急于建仓。Buying at the seller's ask price; implies urgency to buy. |
| **"Axe"** | 斧头 / 强烈意向 | 交易商/做市商对某证券有特别强烈的买入或卖出意向（通常有库存需要处理）。A dealer/market maker's strong directional interest in a security; often has inventory to move. |
| **"Paper"** | 客户单 | 来自于客户（机构投资者）的买卖订单（相对于做市商自营单）。Customer order flow from institutional investors (as opposed to dealer proprietary flow). |
| **"On the run"** | 最新发行券 | 最近发行的、流动性最好的同期限政府债券；相对的是"Off the run"（非当期券）。The most recently issued and most liquid government bond of a given maturity; opposite of "off-the-run". |
| **"Fly"** | 蝶式头寸 | 蝶式利差交易（Butterfly）的简称，涉及三个期限债券的组合多空头寸。Shorthand for a butterfly spread trade involving three maturity points on the yield curve. |
| **"Paying / Receiving"** | 付/收固定利率 | 在利率掉期中，"Paying"指付固定利率/收浮动，"Receiving"指收固定利率/付浮动。In IRS: "Paying" = paying fixed/receiving floating; "Receiving" = receiving fixed/paying floating. |
| **"Risk off / Risk on"** | 避险/风险偏好 | Risk off：市场情绪恶化，资金流向安全资产（美债、日元、黄金）；Risk on：市场情绪改善，资金流向风险资产（股票、高收益债、新兴市场）。Risk off: markets move to safe havens (USTs, JPY, gold); Risk on: markets favor risky assets (equities, HY bonds, EM). |
| **"Steepener / Flattener"** | 陡峭化/平坦化交易 | 收益率曲线陡峭化交易：期望长短端利差扩大；平坦化：期望利差收窄。Steepener: expects long-short spread to widen; Flattener: expects spread to narrow. |
| **"Vol"** | 波动率 | 期权市场对波动率（Volatility）的简称。Shorthand for volatility in options markets. |

---

*上一阶段 / Prev: [Phase 13 — 资产管理与基金](Phase-13-Asset-Management.md)*  
*返回大纲 / Back to: [Spec.md](Spec.md)*

---

**恭喜完成所有14个学习阶段！🎓**  
**Congratulations on completing all 14 learning phases!**

> 从银行基础概念到资深交易员视角，你已掌握了银行内部系统开发所需的完整金融术语体系。  
> From banking fundamentals to senior trader insights, you now have a comprehensive financial terminology framework for banking system development.
