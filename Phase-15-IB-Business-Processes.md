# Phase 15 — 投行核心业务流程详解
# Phase 15 — Investment Bank Core Business Process Flows

> **学习目标 / Learning Objectives**  
> 通过真实的端到端业务流程，了解投行各部门如何协作，以及哪些角色在流程的哪个环节负责什么。  
> Understand how IB divisions collaborate through real end-to-end workflows, and which roles are responsible at each stage.

---

## 15.1 投行部门与角色全景图 / IB Division & Role Overview

一家典型的投资银行由以下主要部门构成，各部门在业务流程中扮演不同角色：  
A typical investment bank is structured into the following key divisions, each playing distinct roles in business workflows:

```
┌─────────────────────────────────────────────────────────────────┐
│                   INVESTMENT BANK (投资银行)                     │
├──────────────────────────┬──────────────────────────────────────┤
│   FRONT OFFICE (前台)    │  MIDDLE OFFICE (中台)  BACK OFFICE   │
│                          │                        (后台)         │
│  IBD (投行部)            │  Risk Management       Operations     │
│  ├─ ECM                  │  (风险管理)             (运营)         │
│  ├─ DCM                  │                                       │
│  ├─ M&A                  │  Finance & Control     IT / Technology│
│  └─ Leveraged Finance    │  (财务控管)             (信息技术)     │
│                          │                                       │
│  Global Markets (全球市场)│  Compliance            Legal          │
│  ├─ Sales (销售)         │  (合规)                (法务)         │
│  ├─ Trading (交易)       │                                       │
│  └─ Structuring (结构)   │  Credit Risk           Product Control│
│                          │  (信用风险)            (产品控制)      │
│  Research (研究)         │                                       │
└──────────────────────────┴──────────────────────────────────────┘
```

### 核心角色描述 / Key Role Descriptions

| 角色 | 英文 | 所属部门 | 职责 |
|------|------|----------|------|
| **Coverage Banker** | 覆盖银行家 | IBD | 维系客户关系，挖掘并购/融资需求，是客户进入银行的第一联系人 |
| **ECM Originator** | ECM发行部 | IBD/ECM | 设计股权发行方案，协调路演、定价与承销；客户在联交所挂牌的主导者 |
| **DCM Originator** | DCM发行部 | IBD/DCM | 设计债券发行方案，安排路演和簿记，协调评级机构和律师事务所 |
| **M&A Banker** | 并购银行家 | IBD/M&A | 提供估值分析、交易结构建议，主导谈判和尽职调查过程 |
| **Syndicate Desk** | 银团/辛迪加台 | IBD-Markets接口 | 债券/股票发行定价指导，收集投资者订单（簿记），决定最终价格和分配 |
| **Sales (Salesperson)** | 销售 | Global Markets | 联络机构客户（买方），推介交易想法，传递交易请求给交易员 |
| **Trader** | 交易员 | Global Markets | 执行客户订单或自营交易，管理风险头寸；固收/FX/权益/衍生品等专项 |
| **Structurer** | 结构师 | Global Markets | 设计定制化衍生品和结构化产品，对定价和法律文件负责 |
| **Quant / Financial Engineer** | 量化/金融工程师 | Markets/Risk | 构建定价模型、风险模型、交易算法 |
| **Research Analyst** | 研究分析师 | Research | 发布公司、行业、宏观研究报告（卖方研究），支持销售和客户决策 |
| **Risk Manager** | 风险经理 | Middle Office | 监控交易台的风险敞口（Greeks、VaR、限额），审批超限交易 |
| **Product Controller** | 产品控制员 | Middle Office | 独立验证交易台的P&L，确认估值模型和市场数据的正确性 |
| **Operations / Settlement** | 运营/结算 | Back Office | 处理交易确认、清算、结算、托管，核对Nostro账户 |
| **Legal / Documentation** | 法务 | Support | 起草和审查ISDA协议、承销协议、债券条款文件 |
| **Compliance** | 合规 | Support | 监控员工合规行为，审批产品适当性，反洗钱（AML）监控 |

---

## 15.2 债券发行（DCM）完整流程 / Bond Issuance (DCM) End-to-End Process

### 场景 / Scenario
某香港上市中资房地产公司希望通过境外SPV发行一笔5年期美元高收益债券，融资5亿美元。  
*A HK-listed Chinese property company wants to issue USD 500mn 5-year offshore high-yield bonds via a Cayman SPV.*

---

### 阶段一：授权与准备 / Phase 1: Mandate & Preparation（约4-6周 / ~4-6 weeks）

```
客户CFO/Treasurer
       │
       ▼
[1] 邀请多家银行提交提案（RFP）
    Client issues RFP to multiple banks
       │
       ▼
[2] 银行Coverage Banker + DCM Originator 联合制作提案（Pitch Book）
    Coverage Banker + DCM Originator jointly prepare pitch book
    - 发行时机分析 / Market timing analysis
    - 可比发行人定价 / Comparable issuer pricing
    - 建议发行结构（Reg S / 144A）/ Suggested structure
    - 承销费（Underwriting fee）报价 / Fee proposal
       │
       ▼
[3] 客户授权主承销商（Bookrunner）和联席管理行（Co-managers）
    Client selects Bookrunner(s) and Co-managers → Mandate Letter signed
```

**参与角色 / Roles involved:**
- `Coverage Banker` → 维系客户关系，争取授权
- `DCM Originator` → 市场分析、定价建议、结构设计
- `Legal (External)` → 律师事务所（如国浩、Sullivan & Cromwell）起草授权文件

---

### 阶段二：法律架构与文件准备 / Phase 2: Legal Structure & Documentation（约3-4周 / ~3-4 weeks）

```
[4] 设立境外SPV（通常为开曼群岛公司）
    Set up offshore SPV (Cayman Islands)
    - 银行法务 + 外部律师协同
       │
       ▼
[5] 起草发行文件
    Draft offering documents
    - Offering Memorandum (OM) / 发行备忘录
    - Indenture（信托契约）/ 债券契约
    - Purchase Agreement（购买协议）
    - Keepwell Deed + EIPU（维好契约+股权收购承诺，适用中资主体）
       │
       ▼
[6] 与评级机构沟通（若申请评级）
    Rating agency process (Moody's / S&P / Fitch)
    - 管理层路演（Rating Agency Presentations）
    - 获取初步信用评级
       │
       ▼
[7] 路演材料准备
    Prepare investor presentation / roadshow materials
```

**参与角色 / Roles involved:**
- `DCM Originator` → 主导文件流程，协调各方
- `Legal (Internal & External)` → 起草和审查所有法律文件
- `Compliance` → 审批发行适当性，KYC/AML检查
- `Credit Risk` → 审批银行对发行人的承销风险敞口
- `Structurer` → 设计Keepwell/EIPU等增信结构（若适用）

---

### 阶段三：投资者教育与路演 / Phase 3: Investor Education & Roadshow（约1-2周 / ~1-2 weeks）

```
[8] 发布投资者路演（Investor Roadshow）
    - 亚洲（香港、新加坡）→ 欧洲（伦敦）→ 美国（纽约、波士顿）
    - 客户管理层 + DCM Originator + Sales共同出席
       │
       ▼
[9] 订单意向收集（IOI — Indication of Interest）
    Gauge investor demand; collect non-binding indications
    - 由Sales团队接触各自负责的机构投资者
    - Syndicate Desk汇总需求，更新定价指引
       │
       ▼
[10] 发布价格指引（IPT — Initial Price Thoughts）
     Syndicate issues IPT to market
     例：US Treasuries + 600-625 bps（参考基准利率加点）
```

**参与角色 / Roles involved:**
- `DCM Originator` → 带领路演，回答投资者问题
- `Sales (Fixed Income)` → 联络机构客户，收集订单意向
- `Syndicate Desk` → 汇总需求，更新定价指引，发布IPT
- `Research (Credit)` → 提供信用研究报告支持销售
- `Client Management (CFO/IR team)` → 参与路演演讲

---

### 阶段四：簿记与定价 / Phase 4: Bookbuilding & Pricing（1-2天 / 1-2 days）

```
[11] 正式开放簿记（Books Open），发布最终价格指引（FPT）
     Books officially open; Final Price Talk announced
       │
       ▼
[12] 机构投资者提交正式认购订单
     Institutional investors submit orders (size + price limit)
     - 典型认购登记：2-8亿美元/单一账户
       │
       ▼
[13] Syndicate Desk实时追踪簿记进度
     Syndicate tracks book in real time
     - "Books are X times covered"（认购覆盖X倍）
     - 分析订单质量（长线vs对冲基金，地区分布）
       │
       ▼
[14] 定价决策 Price Setting
     Syndicate + Client → 确定最终票息和发行价格
     例：4.5年年期，票息8.875%，发行价格99.5（收益率8.975%+15bps NIP）
       │
       ▼
[15] 宣布发行成功（Deal Announced）
     "PRICED: USD 500mn 5NC3 Senior Notes @ 8.875%"
```

**参与角色 / Roles involved:**
- `Syndicate Desk` → **核心角色**：簿记、定价决策、分配管理
- `Sales` → 维护投资者关系，推动订单提交
- `DCM Originator` → 建议定价，与客户沟通
- `Trader (Credit)` → 提供二级市场参考定价和流动性评估

---

### 阶段五：分配与结算 / Phase 5: Allocation & Settlement（T+5，约5个工作日 / ~5 business days）

```
[16] 份额分配（Allocation）
     Syndicate decides allocation among investors
     - 优先奖励长线基金（Asset Managers、Insurers）
     - 限制短线对冲基金（Hedge Funds）
       │
       ▼
[17] 确认书发送（Trade Confirmations sent）
     Operations sends trade confirmations via SWIFT/email
       │
       ▼
[18] 结算（Settlement）T+5
     DvP settlement via Euroclear/Clearstream
     - 债券割让给投资者（ISIN注册）
     - 发行人收到净募集资金（扣除承销费）
       │
       ▼
[19] 二级市场上市（Secondary Market Listing）
     Bond listed on HKEX / SGX / Euronext Dublin
     Trader开始做市（Market Making），提供流动性
```

**参与角色 / Roles involved:**
- `Syndicate Desk` → 分配管理，通知各投资者
- `Operations / Settlement` → 发送确认书，处理Euroclear结算，核对Nostro账户
- `Legal` → 签署购买协议，交割文件
- `Trader (Credit / HY Bond)` → 上市后承担做市义务
- `Product Control` → 验证发行P&L（承销费收入）

---

## 15.3 IPO流程 / IPO Process End-to-End

### 场景 / Scenario
一家中国新能源公司希望在香港联交所主板上市，融资10亿美元。  
*A Chinese new energy company seeks to list on HKEX Main Board, raising USD 1bn.*

```
阶段 / Phase          时间 / Timeline        核心角色 / Key Roles
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
1. 授权 Mandate       第1-2个月              Coverage Banker, ECM Originator
2. 上市前准备          第2-6个月              ECM, Legal (Capital Market), Auditor,
   Pre-deal Prep                             External Counsel, Sponsor
3. 监管申报            第6-9个月              Sponsor Banker (HKEX规定), Legal, 
   HKEX Filing (A1)                          Compliance, Accounting
4. 投资者教育          第9-10个月             ECM, Sales (Equity), Research Analyst
   Pre-deal Research                         (启动研究覆盖)
5. 路演 Roadshow       第10-11个月            ECM Originator, Sales, 
                                             客户高管团队（CEO/CFO）
6. 基石投资者锁定       路演期间               ECM, Coverage Banker
   Cornerstone Locking                      (锁定战略投资者，6个月禁售期)
7. 公开认购 Public IPO  第11个月               Syndicate, Sales, Retail Broker Network
8. 定价 Pricing        公开认购结束后          Syndicate Desk, ECM
9. 挂牌上市 Listing     定价后第5工作日         Operations, HKEX, HKSCC/CCASS
10. 绿鞋稳定 Stabilization 挂牌后30天          Stabilization Agent (通常主承销商)
```

### HKEX上市独特要求 / HKEX-Specific Requirements

| 要求 | 说明 |
|------|------|
| **保荐人制度 (Sponsor)** | HKEX要求至少1家授权保荐人（通常是主承销商的独立团队）对发行人作尽职调查，对招股书内容承担法律责任 |
| **基石投资者 (Cornerstone Investors)** | 香港IPO特有：承诺认购固定金额、6个月禁售；提升市场信心；基石投资者须在招股书中披露 |
| **H股架构** | 中资企业在香港上市通常采用H股（境外上市、境内注册）或红筹（境外注册、境外上市）架构 |
| **25%公众持股量** | 上市时公众持股须达发行后总股数25%（市值超400亿港元可降至15%） |

---

## 15.4 M&A并购交易流程 / M&A Deal Process

### 场景 / Scenario
日本电子企业A（买方）收购新加坡半导体公司B（卖方），交易价值约20亿美元。  
*Japanese electronics company A (buyer) acquires Singapore semiconductor company B (seller), deal value ~USD 2bn.*

```
阶段 / Phase                  双方顾问工作 / Both Sides' Activities
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
[买方顾问 Buy-side IB]                    [卖方顾问 Sell-side IB]
Coverage + M&A Banker                     Coverage + M&A Banker

1. 战略建议 Strategic Rationale
   - 协同效应分析 Synergy analysis       - 协助卖方制作信息备忘录 (IM)
   - 并购目标筛选 Target screening       - 组织拍卖流程（组织竞价）
   
2. 初步估值 Preliminary Valuation
   - DCF / EV/EBITDA / 可比交易 Comps   - 反驳买方报价（争取更高对价）
   - 协同效应加成 Synergy premium        - 公平意见书 Fairness Opinion

3. 初步报价 Initial Bid（非约束性）
   非约束性意向书 NBO (Non-Binding Offer)

4. 尽职调查 Due Diligence（约4-8周）
   ► 财务DD   接触CFO、审计报告             ► 虚拟数据室管理 VDR Setup
   ► 法律DD   合同、诉讼、知识产权
   ► 商业DD   市场份额、客户合同、技术护城河
   ► 税务DD   跨境税务结构、潜在税务负债

5. 最终报价 Final Bid（约束性）
   SPA草稿协商 SPA (Share Purchase Agreement) negotiation

6. 排他性谈判 Exclusivity（约2-4周）
   确认交割条件（监管批准、股东表决等）

7. 签约 Signing（SPA签署）
   宣布交易 Public Announcement

8. 交割前期 Pre-Closing（约3-6个月）
   反垄断审查（SAMR/EC/DOJ）
   监管批准、SAFE外汇审批（若涉及跨境资金）

9. 交割 Closing
   资金划付、股权过户、整合启动
```

### 各角色在M&A中的职责 / Role Responsibilities in M&A

| 角色 | 具体工作内容 |
|------|------------|
| **Coverage Banker** | 维系并购双方关系，推动项目启动；全程对客沟通 |
| **M&A Analyst/Associate** | 构建财务模型（DCF、LBO模型、增厚/摊薄分析）；制作投资委员会材料 |
| **M&A VP/Director** | 监督模型质量，主导DD沟通，协助SPA谈判 |
| **Capital Markets (ECM/DCM)** | 若收购方需要融资（股票增发或债务融资）：设计融资方案 |
| **Leveraged Finance** | 若LBO交易：设计TLB/HY Bond融资层 |
| **Legal (External)** | 起草SPA、股东协议、交割文件；反垄断申报 |
| **Risk / Credit** | 对银行自身参与（如保留融资敞口）进行信用审批 |
| **Compliance** | 内幕信息管控（信息壁垒 Chinese Wall），OFAC制裁筛查 |
| **Tax Advisor** | 优化交易税务结构（持股架构、预扣税等） |

---

## 15.5 交易台日常运营 / Trading Desk Daily Operations

### 一位固定收益（信用债）交易员的一天 / A Day in the Life of a Credit Trader

```
时间          活动
─────────────────────────────────────────────────────
06:30        阅读隔夜新闻、彭博快讯、内部研究晨报
             Read overnight news, Bloomberg alerts, morning research note

07:30        早会（Morning Meeting）
             - 研究分析师：重点行业/公司更新
             - 销售：客户询问、潜在大单
             - 交易员：头寸更新、回购资金成本（Repo cost）
             - 风险经理：前日VaR报告、重点敞口

08:30        亚洲市场开盘（香港时间）
             - 更新买卖价格（Price Refresh）— 向系统报价
             - 处理前日未了结订单
             - 回应新加坡/东京的销售询价

09:00-12:00  高峰交易时段
             - 销售传入客户询价（RFQ — Request for Quote）
               例：某对冲基金询价：卖5MM USD某A评级亚洲美元债
             - 交易员报出买卖价（做市）
             - 对冲风险：买入CDS或调整相关仓位
             - Bloomberg YAS 计算收益率/利差

12:00        午间头寸评估（Mark-to-Market）
             - Product Control确认中间价（Mid Price）
             - P&L初步核对

14:00-17:00  欧洲市场重叠时段（伦敦下午）
             - 处理欧洲销售传来的亚洲美元债询价
             - 新发行债券定价参与（若有新债路演）

17:30-18:00  收盘流程（EOD Process）
             - 向风控系统提交当日头寸
             - Product Control更新收盘价
             - 报告超限情况（Breach Report）— 若有

19:00-21:00  美国市场重叠时段（可选）
             - 处理纽约销售询价（亚洲美元债）
             - 监控美债/利率变动对亚洲债价格的影响
```

### 交易台风险管控流程 / Trading Desk Risk Control Flow

```
交易员下单
    │
    ▼
[Pre-Trade Check]  ── 风控网关（Risk Gateway）实时检查
    ├─ 头寸限额（Position Limit）是否超限
    ├─ Delta/DV01 敞口是否在限额内
    ├─ 交易对手信用额度（Credit Line）是否充足
    └─ 制裁名单（OFAC/UN）筛查
    │
    ▼（通过→执行）
[执行（Execution）]  ── 市场成交
    │
    ▼
[Post-Trade Processing]  ── Operations处理
    ├─ 成交确认（Trade Confirmation）发送给交易对手
    ├─ 清算指令发送（SWIFT MT300/MT202等）
    ├─ 结算追踪（T+2/T+3）
    └─ Nostro账户核对
    │
    ▼
[End-of-Day Valuation]  ── Product Control / Risk
    ├─ 独立估值（Independent Price Verification, IPV）
    ├─ P&L归因（P&L Attribution）
    └─ VaR计算更新
```

---

## 15.6 结构化产品销售流程 / Structured Product Sales Process

### 场景 / Scenario
香港私人银行客户（高净值）希望在某亚洲科技股上投资500万美元，同时寻求保本或增强收益。  
*HK private banking client (HNWI) wants USD 5mn exposure to an Asian tech stock, seeking principal protection or yield enhancement.*

```
[1] 需求发现（Needs Discovery）
    Private Banker / Relationship Manager ↔ 客户
    ─ 了解风险偏好（Risk Appetite）、投资期限（Tenor）、监管限制
    
[2] 结构设计（Structuring）
    Banker → Structuring Desk（结构部）
    ─ 结构师根据需求设计产品选项：
      方案A：Principal Protected Note (PPN) 保本票据（嵌入认购期权）
      方案B：Equity-Linked Note (ELN) 股权挂钩票据（收益增强，有可能交割股票）
      方案C：Autocallable 自动赎回结构（若股价维持，每季度获息并可能提前赎回）

[3] 内部定价（Internal Pricing）
    Structurer ↔ Trader（期权交易台）
    ─ 期权交易台按波动率曲面（Vol Surface）定价
    ─ 计算发行利润空间（Bid-Offer）
    ─ 进行风险审批（Risk approval for Greeks）

[4] 合规审批（Compliance Approval）
    ─ 产品适当性评估（Product Suitability Assessment）
    ─ 验证客户的专业投资者（PI）状态（香港SFC要求）
    
[5] 客户报价与确认（Quoting & Confirmation）
    Banker → 客户报价 → 客户确认（Term Sheet签署）
    
[6] 交易录入与确认（Trade Booking & Confirmation）
    Operations录入系统 → 发送ISDA确认书（Confirmation）
    
[7] 持续生命周期管理（Lifecycle Management）
    ─ 观察日（Observation Date）监控：Autocall是否触发
    ─ 保证金/抵押品管理（若客户用杠杆购买）
    ─ 到期事件处理（Expiry Event）：现金结算或股票交割
    ─ 向Operations发起结算指令
```

---

## 15.7 中台/后台如何支持前台 / How Middle & Back Office Support Front Office

| 流程 | 中台角色 | 后台角色 |
|------|----------|----------|
| **新交易录入** | Risk: 实时监控敞口变化；Product Control: 标记初始MTM | Operations: 核对交易细节与对手确认书 |
| **每日估值** | Product Control: 独立收盘价验证（IPV）；Risk: 更新VaR | Operations: 生成日终头寸报表；Finance: 更新P&L账 |
| **结算** | Risk: 确认结算前无信用事件 | Operations: 发送SWIFT指令；核对Nostro账户；处理交割失败（Fail）|
| **公司行动** | Product Control: 估值调整 | Operations: 处理股息、票息收付；更新持仓 |
| **监管报告** | Risk: 准备EMIR/MAS报告数据 | Operations: 向交易存储库（Trade Repository）提交报告 |
| **客户对账** | Product Control: 验证客户报表数据 | Operations: 发送月度对账单（Statement）给客户 |

---

*上一阶段 / Prev: [Phase 14 — 高级交易与金融科技](Phase-14-Advanced-Trading.md)*  
*下一阶段 / Next: [Phase 16 — UBS投资银行业务深度解析](Phase-16-UBS-Investment-Bank.md)*
