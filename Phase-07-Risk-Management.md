# Phase 07 — 风险管理
# Phase 07 — Risk Management

> **学习目标 / Learning Objectives**  
> 理解银行面临的各类风险及其度量方法，掌握信用风险XVA体系、流动性监管框架和巴塞尔协议要求。  
> Understand the key risk types banks face, how they are measured, the XVA framework, liquidity regulation, and Basel capital requirements.

---

## 7.1 市场风险 / Market Risk

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **Market Risk** | 市场风险 | 因市场价格（利率、汇率、股价、大宗商品价格）不利变动导致损失的风险。Risk of loss due to adverse movements in market prices: interest rates, FX, equities, commodities. |
| **VaR (Value at Risk)** | 风险价值 | 在给定置信水平（如99%）和持有期（如1天/10天）内，投资组合可能遭受的最大损失估计。Estimated maximum loss of a portfolio at a given confidence level (e.g., 99%) over a specified holding period (1 day, 10 days). |
| **CVaR / Expected Shortfall (ES)** | 条件风险价值 / 预期损失 | VaR的改进：超出VaR阈值的损失的条件均值；监管逐渐从VaR转向ES（FRTB）。Improvement on VaR: average loss in the tail beyond the VaR threshold. Regulators increasingly prefer ES (FRTB). |
| **Stress Testing** | 压力测试 | 在极端但可能的市场情景下（如2008年金融危机、COVID冲击）评估组合损失。Evaluating portfolio losses under extreme but plausible scenarios (e.g., GFC 2008, COVID crash). |
| **Scenario Analysis** | 情景分析 | 模拟特定宏观/市场事件对投资组合的影响；通常与压力测试结合使用。Modelling the impact of specific macro/market events on a portfolio; often combined with stress testing. |
| **Greeks** | 希腊字母 | 期权/衍生品组合对价格、波动率、时间、利率变动的风险敏感度（见Phase 05）。Risk sensitivities of derivatives to changes in price, volatility, time, and rates (see Phase 05 for detail). |
| **DV01 / PV01** | 基点价值 | 利率上升1个基点（0.01%）时固定收益组合的盈亏变动。P&L change of a fixed income portfolio for a 1 bps rise in interest rates. |
| **FX Exposure** | 外汇敞口 | 因汇率变动可能导致损失的非本币资产/负债头寸。Net non-base-currency positions subject to FX rate movements. |
| **FRTB** | 交易账户基本审查 | 巴塞尔委员会对市场风险资本计算的重大改革，用ES取代VaR，并区分交易账户与银行账户。Fundamental Review of the Trading Book; Basel's major overhaul of market risk capital; replaces VaR with ES; distinguishes trading vs. banking book. |

---

## 7.2 信用风险 / Credit Risk

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **Credit Risk** | 信用风险 | 交易对手未能履行合同义务导致损失的风险。Risk of loss from a counterparty failing to meet its contractual obligations. |
| **Default** | 违约 | 借款人未能按期偿还本金或利息的事件。Failure of a borrower to make required principal or interest payments. |
| **PD (Probability of Default)** | 违约概率 | 在特定时间段内（通常1年）借款人发生违约的概率。Probability that a borrower will default within a specified period (typically 1 year). |
| **LGD (Loss Given Default)** | 违约损失率 | 违约发生后，实际损失占违约敞口的百分比（1 − 回收率）。Percentage of EAD that is lost after a default occurs; LGD = 1 − Recovery Rate. |
| **EAD (Exposure at Default)** | 违约时的风险敞口 | 违约发生时预计的未偿余额。The estimated outstanding amount at the time of default. |
| **Expected Loss (EL)** | 预期损失 | EL = PD × LGD × EAD；银行须对预期损失提取拨备。EL = PD × LGD × EAD; banks must provision for expected losses. |
| **Unexpected Loss (UL)** | 非预期损失 | 超出预期损失的波动性损失；由资本（而非拨备）来覆盖。Loss volatility beyond expected loss; covered by regulatory capital, not provisions. |
| **CVA (Credit Valuation Adjustment)** | 信用估值调整 | 衍生品公允价值中因交易对手违约风险而进行的调整（减值）；CVA = 无风险价值 − 含信用风险价值。Adjustment to derivative fair value to account for counterparty default risk. CVA = Risk-free value − Risky value. |
| **DVA (Debt Valuation Adjustment)** | 借方估值调整 | CVA的镜像：因本行自身信用变化对衍生品负债端的价值调整。Mirror of CVA: adjustment reflecting the bank's own credit risk on its derivative liabilities. |
| **FVA (Funding Valuation Adjustment)** | 资金估值调整 | 为无抵押衍生品头寸进行资金融通的成本或收益的调整。Adjustment for the funding cost/benefit of uncollateralised derivatives. |
| **KVA (Capital Valuation Adjustment)** | 资本估值调整 | 持有衍生品所需监管资本的机会成本调整。Adjustment for the opportunity cost of regulatory capital required for derivatives. |
| **XVA** | 估值调整集合 | CVA + DVA + FVA + KVA等各类调整的统称，是现代衍生品定价的重要组成部分。Collective term for all valuation adjustments (CVA, DVA, FVA, KVA, etc.); integral to modern derivatives pricing. |
| **Credit Rating** | 信用评级 | 独立评级机构对发行人偿债能力的评估；三大评级机构：穆迪（Moody's）、标普（S&P）、惠誉（Fitch）。Assessment of an issuer's creditworthiness by rating agencies: Moody's, S&P, Fitch. |
| **Investment Grade (IG)** | 投资级 | 信用评级为BBB−/Baa3及以上的债券，被认为违约风险低。Bonds rated BBB−/Baa3 or above; considered low default risk. |
| **High Yield (HY) / Junk** | 高收益 / 垃圾级 | 信用评级低于BBB−/Baa3的债券，违约风险较高，收益率也较高。Bonds rated below BBB−/Baa3; higher default risk; compensated by higher yields. |
| **Collateral** | 抵押品 | 为降低信用风险，交易对手提供的资产或现金担保。Assets or cash provided by a counterparty to mitigate credit risk. |
| **CSA (Credit Support Annex)** | 信用支持附件 | ISDA协议下的附件，规定衍生品交易双方互相交换抵押品的条款（保证金要求）。Annex to ISDA Master Agreement specifying collateral exchange terms between OTC derivatives counterparties. |
| **ISDA Master Agreement** | ISDA主协议 | 国际掉期和衍生品协会制定的场外衍生品交易标准合同框架，是全球OTC衍生品市场的法律基础。Standardised legal framework for OTC derivatives transactions published by ISDA; the legal backbone of the global OTC derivatives market. |

---

## 7.3 流动性风险 / Liquidity Risk

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **Market Liquidity Risk** | 市场流动性风险 | 在不显著影响市场价格的情况下无法迅速变现资产的风险。Risk of being unable to quickly sell assets without significantly moving prices. |
| **Funding Liquidity Risk** | 融资流动性风险 | 无法以合理成本及时获得足够资金以满足到期债务的风险。Risk of being unable to meet cash flow obligations at a reasonable cost in a timely manner. |
| **LCR (Liquidity Coverage Ratio)** | 流动性覆盖率 | 巴塞尔 III 核心流动性指标：HQLA / 30天净现金流出 ≥ 100%。确保银行在30天压力情景下的流动性充足。Basel III metric: HQLA / Net cash outflows over 30-day stress scenario ≥ 100%. |
| **NSFR (Net Stable Funding Ratio)** | 净稳定资金比例 | 可用稳定融资 / 所需稳定融资 ≥ 100%；确保银行有足够长期稳定资金覆盖资产。Available Stable Funding / Required Stable Funding ≥ 100%; ensures long-term stable funding. |
| **HQLA (High-Quality Liquid Assets)** | 优质流动资产 | 在压力情景下可迅速变现的资产：一级（现金、央行储备、主权债）和二级（高评级企业债、机构MBS）。Assets that can be quickly converted to cash in a stress scenario: Level 1 (cash, central bank reserves, sovereign bonds) and Level 2 (IG corporates, agency MBS). |
| **Run on the Bank** | 银行挤兑 | 大量存款人同时提款，可能耗尽银行流动性储备。Mass simultaneous withdrawal by depositors; can deplete a bank's liquidity reserves. |

---

## 7.4 操作风险 / Operational Risk

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **Operational Risk** | 操作风险 | 因内部流程失败、人为失误、系统故障或外部事件（欺诈、自然灾害）导致损失的风险。Risk of loss from failed internal processes, people, systems, or external events (fraud, natural disasters). |
| **Model Risk** | 模型风险 | 使用错误或不适当的金融模型进行估值或风险管理导致损失的风险。Risk of loss from using incorrect or inappropriate financial models for valuation or risk management. |
| **Settlement Risk** | 结算风险 | 一方已交付资产但对手方未能按时交割对应资产的风险。Risk that a counterparty delivers its side of a transaction but the other party fails to deliver. |
| **Herstatt Risk** | 赫斯塔特风险 | 跨时区外汇结算的时间错位风险（以1974年德国赫斯塔特银行倒闭事件命名）。Foreign exchange settlement risk arising from time-zone differences; named after the 1974 collapse of Germany's Herstatt Bank. |
| **Rogue Trader** | 流氓交易员 | 未授权地进行超规模或隐藏亏损的内部交易员（如巴林银行尼克·利森事件）。Unauthorised trading by a rogue employee concealing losses; historical examples: Nick Leeson (Barings), Jerome Kerviel (SocGen). |
| **Cyber Risk** | 网络安全风险 | 网络攻击、数据泄露等信息安全事件导致的操作损失。Risk of operational losses from cyberattacks, data breaches, or IT disruptions. |

---

## 7.5 监管资本框架 / Regulatory Capital Framework

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **Basel III / Basel IV** | 巴塞尔协议III/IV | 国际清算银行巴塞尔委员会发布的银行监管资本、流动性和杠杆的国际标准。International standards for bank capital adequacy, liquidity, and leverage, published by the Basel Committee on Banking Supervision (BIS). |
| **CET1 Ratio** | 核心一级资本充足率 | CET1资本 / RWA；巴塞尔III最低要求4.5%，加上资本保护缓冲2.5%，总计7%。CET1 capital / RWA; Basel III minimum 4.5% + 2.5% conservation buffer = 7%. |
| **Capital Conservation Buffer** | 资本保护缓冲 | 额外2.5% CET1要求，若不满足则限制股息和奖金分配。Extra 2.5% CET1 on top of minimum; restricts distributions if breached. |
| **Countercyclical Buffer (CCyB)** | 逆周期资本缓冲 | 监管机构在信贷繁荣期要求的额外资本（0-2.5%），以缓冲信贷周期风险。Regulators may require 0–2.5% additional CET1 during credit booms; released in downturns. |
| **G-SIB Surcharge** | 全球系统重要性银行附加资本 | 全球系统重要性银行须额外持有1-3.5% CET1资本，按系统重要性分组。Additional CET1 of 1–3.5% for Global Systemically Important Banks (G-SIBs); tiered by systemic importance. |
| **ICAAP** | 内部资本充足评估程序 | 银行评估自身全部风险（包括非Pillar 1风险）并确定所需资本水平的内部程序。Bank's internal process to assess all material risks and determine appropriate capital levels beyond Pillar 1 minimums. |
| **CCAR** | 综合资本分析与审查 | 美联储对大型美国银行进行的年度压力测试，评估其在经济下行情景下的资本充足性。Annual Fed stress test for large US banks; assesses capital adequacy under adverse economic scenarios. |

---

*上一阶段 / Prev: [Phase 06 — 外汇市场](Phase-06-FX-Markets.md)*  
*下一阶段 / Next: [Phase 08 — 交易执行与结算](Phase-08-Trading-Execution.md)*
