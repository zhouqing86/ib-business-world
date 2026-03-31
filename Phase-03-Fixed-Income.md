# Phase 03 — 固定收益与货币市场
# Phase 03 — Fixed Income & Money Markets

> **学习目标 / Learning Objectives**  
> 掌握债券的基本要素、定价与收益率计算、利率基准，以及货币市场工具。  
> Master bond fundamentals, pricing and yield calculations, rate benchmarks, and money market instruments.

---

## 3.1 债券基础 / Bond Basics

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **Bond** | 债券 | 发行人（政府/企业）向投资者借款并承诺定期支付利息、到期偿还本金的债务工具。A debt instrument where the issuer borrows money and promises to pay periodic interest (coupon) and repay principal at maturity. |
| **Issuer** | 发行人 | 发行债券筹资的主体，可以是政府、国际机构或企业。Entity that issues the bond to raise funds — government, supranational, or corporate. |
| **Face Value / Par Value** | 面值 | 债券到期时偿还给持有人的本金金额，通常为1,000美元或100元。Principal amount repaid at maturity; typically USD 1,000 or par 100. |
| **Coupon** | 票息 | 发行人按期（通常每半年或每年）支付给持有人的利息金额。Periodic interest payment made by the issuer to bondholders; typically semi-annual or annual. |
| **Coupon Rate** | 票息率 | 票息占面值的年化百分比。Annual coupon amount as a percentage of face value. |
| **Maturity Date** | 到期日 | 发行人须偿还面值的最终日期。Date on which the issuer repays the face value. |
| **Tenor** | 期限 | 从发行到到期的时间长度（例如：2年、5年、10年、30年）。Time from issuance to maturity (e.g., 2Y, 5Y, 10Y, 30Y). |
| **Accrued Interest** | 应计利息 | 上次付息日至结算日之间已累积但尚未支付的利息。Interest accumulated since the last coupon payment date up to the settlement date. |
| **Clean Price** | 净价 | 不含应计利息的债券报价价格。Bond price excluding accrued interest; the quoted price. |
| **Dirty Price / Full Price** | 全价 | 净价加上应计利息，即实际成交价格。Clean price plus accrued interest; the actual amount paid. Dirty Price = Clean Price + Accrued Interest |
| **ISIN** | 国际证券识别码 | 12位字母数字代码，全球唯一标识证券。12-character alphanumeric code uniquely identifying a security globally. |
| **CUSIP** | 美国证券识别码 | 9位字符代码，用于识别在美国和加拿大发行的证券。9-character code identifying securities issued in the US and Canada. |

---

## 3.2 债券类型 / Types of Bonds

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **Government Bond / Sovereign Bond** | 国债/主权债 | 由国家政府发行，信用风险最低；美国国债称Treasuries，英国称Gilts，日本称JGBs，中国称CGBs。Issued by national governments; lowest credit risk. US: Treasuries; UK: Gilts; Japan: JGBs; China: CGBs. |
| **Corporate Bond** | 企业债 | 由公司发行，收益率高于同期政府债，反映额外信用风险。Issued by companies; higher yield than government bonds to compensate for credit risk. |
| **Municipal Bond (Muni)** | 市政债券 | 由地方政府发行，在美国通常享有税收优惠。Issued by local governments; often tax-exempt in the US. |
| **Convertible Bond (CB)** | 可转换债券 | 持有人可在特定条件下将债券转换为发行人股票。Bondholder has the right to convert the bond into shares of the issuer under specified conditions. |
| **Zero-Coupon Bond** | 零息债券 | 不支付定期票息，以低于面值的折价发行，到期偿还面值。No periodic coupon; issued at a discount to face value, redeemed at par at maturity. |
| **Floating Rate Note (FRN)** | 浮息票据 | 票息随参考利率（如SOFR、HIBOR）浮动调整，降低利率风险。Coupon adjusts periodically based on a reference rate (SOFR, HIBOR); reduces interest rate risk. |
| **Inflation-Linked Bond / TIPS** | 通胀挂钩债券 | 本金和票息与通胀指数挂钩，保护实际购买力。Principal and/or coupon linked to an inflation index (e.g., CPI); protects real purchasing power. |
| **Covered Bond** | 担保债券 | 由资产池（通常是抵押贷款或公共贷款）双重担保，信用质量高。Backed by a pool of assets (mortgages/public loans) on the issuer's balance sheet; dual recourse. |
| **Subordinated Debt** | 次级债务 | 清偿顺序低于优先债，收益率更高，常见于银行资本结构。Ranks below senior debt in liquidation; higher yield; common in bank capital structures (AT1, Tier 2). |
| **Perpetual Bond** | 永续债 | 无固定到期日，持续支付票息，发行人可选择性赎回。No fixed maturity; pays coupon indefinitely; issuer may have call options. |
| **Green Bond** | 绿色债券 | 募集资金专用于环保或气候相关项目。Proceeds earmarked for environmentally sustainable or climate-related projects. |
| **AT1 Bond** | 额外一级资本债 | 银行发行的混合资本工具，在资本充足率触发时可转股或核销。Hybrid capital instrument issued by banks; can be converted to equity or written down when CET1 ratio falls below trigger. |

---

## 3.3 收益率与定价 / Yield & Pricing

| 英文 | 中文 | 说明 / Description |
|------|------|--------------------|
| **Yield to Maturity (YTM)** | 到期收益率 | 将债券未来所有现金流折现至当前价格的折现率；持有至到期的年化回报率。The discount rate that equates the present value of all future cash flows to the current price; annualised return if held to maturity. |
| **Yield to Call (YTC)** | 赎回收益率 | 债券在第一个赎回日被赎回时的预期收益率。Expected yield if the bond is called at the first call date. |
| **Current Yield** | 当期收益率 | 年票息收入除以债券当前市场价格。Annual coupon divided by current market price. |
| **Yield Curve** | 收益率曲线 | 同一信用质量债券在不同期限下的收益率连成的曲线。Graph plotting yields of bonds with the same credit quality across different maturities. |
| **Normal Yield Curve** | 正常（上斜）收益率曲线 | 长期利率高于短期利率，经济扩张期常见。Long-term rates higher than short-term; typical in economic expansions. |
| **Inverted Yield Curve** | 倒挂收益率曲线 | 短期利率高于长期利率，通常预示经济衰退。Short-term rates higher than long-term; often signals recession. |
| **Credit Spread** | 信用利差 | 企业债收益率与同期限无风险国债收益率之差，反映信用风险溢价。Difference between a corporate bond's yield and a risk-free government benchmark; reflects credit risk. |
| **Z-Spread** | Z利差 | 在整条收益率曲线上加一个固定利差，使债券现金流现值等于市场价格。A constant spread added to the entire spot rate curve so that discounted cash flows equal market price. |
| **OAS (Option-Adjusted Spread)** | 期权调整利差 | 剔除嵌入期权价值后的利差，反映纯信用和流动性风险溢价。Spread after removing the value of any embedded options; reflects pure credit and liquidity premium. |
| **Duration (Macaulay)** | 麦考利久期 | 债券所有现金流按现值加权平均的到期时间，单位为年。Weighted average time to receive all cash flows, discounted at YTM; measured in years. |
| **Modified Duration** | 修正久期 | 衡量债券价格对收益率变化的敏感度，利率上升1%，价格下跌约Modified Duration%。Measures price sensitivity to yield changes: price change % ≈ −Modified Duration × yield change. |
| **Convexity** | 凸性 | 修正久期线性近似的误差修正项；凸性越高，利率下降时价格上升越多，利率上升时价格下降越少。Second-order price sensitivity; higher convexity is beneficial: larger price gains when rates fall, smaller losses when rates rise. |
| **DV01 / PVBP** | 基点价值 | 收益率变化1个基点（0.01%）时债券价格的绝对变动金额。Absolute change in bond price for a 1 basis point move in yield. DV01 = Modified Duration × Price × 0.0001 |

---

## 3.4 利率基准 / Interest Rate Benchmarks

| 基准 | 全称 | 地区 | 说明 |
|------|------|------|------|
| **LIBOR** | London Interbank Offered Rate | 全球（已退出） | 曾是全球最重要的基准利率，已于2023年6月正式停用，各地已转向RFR替代基准。Once the world's most important benchmark rate; discontinued in June 2023; replaced by RFRs. |
| **SOFR** | Secured Overnight Financing Rate | 美国 | 美国LIBOR替代基准，基于美国国债回购市场实际成交利率，每日发布。US LIBOR replacement; based on actual US Treasury repo transactions; published daily by NY Fed. |
| **SONIA** | Sterling Overnight Index Average | 英国 | 英镑LIBOR替代基准，基于银行间无担保隔夜贷款实际利率。UK LIBOR replacement; based on actual unsecured overnight sterling transactions. |
| **HIBOR** | Hong Kong Interbank Offered Rate | 香港 | 香港银行间拆借利率，由香港银行公会制定，含O/N至12个月多个期限。HK interbank offered rate set by the HKAB; tenors from O/N to 12 months. |
| **HONIA** | HKD Overnight Index Average | 香港 | 香港的LIBOR替代基准，基于实际隔夜港元交易。HK's alternative reference rate; based on actual overnight HKD transactions. |
| **SHIBOR** | Shanghai Interbank Offered Rate | 中国 | 上海银行间同业拆借利率，由中国人民银行主导，含O/N至1年期限。China's interbank offered rate; overseen by PBOC; O/N to 1-year tenors. |
| **EURIBOR** | Euro Interbank Offered Rate | 欧元区 | 欧元区银行间拆借利率，仍在使用（经过改革）。Euro area interbank offered rate; still in use following reforms. |
| **Fed Funds Rate** | Federal Funds Rate | 美联储 | 美国联邦基金目标利率，全球最重要的政策利率，影响全球资产定价。The Fed's target policy rate; the most influential policy rate globally. |
| **Prime Rate** | 最优惠利率 | 美国/香港 | 商业银行向最优质借款人提供的基准贷款利率，香港最优惠利率(P)与HK按揭利率挂钩。Benchmark lending rate offered by commercial banks to top-rated borrowers. In HK, linked to mortgage rates. |

---

## 3.5 货币市场工具 / Money Market Instruments

| 英文 | 中文 | 期限 | 说明 / Description |
|------|------|------|--------------------|
| **T-Bill (Treasury Bill)** | 短期国库券 | 4周至52周 | 政府发行的短期折价债务工具，无票息，以折价发行到期按面值兑付。Short-term government discount securities; no coupon; issued at discount, redeemed at par. |
| **Commercial Paper (CP)** | 商业票据 | 1天至270天 | 大型信用优良企业发行的短期无担保债务工具。Short-term unsecured debt issued by large, creditworthy corporations. |
| **Certificate of Deposit (CD)** | 存款证 | 1天至数年 | 银行发行的定期存款凭证，可在二级市场交易（可转让存款证NCD）。Time deposit receipt issued by a bank; negotiable CDs can be traded in the secondary market. |
| **Repo (Repurchase Agreement)** | 回购协议 | 隔夜至数月 | 一方以证券作抵押借入资金，并约定在未来某日以约定价格买回证券。A party sells securities and agrees to repurchase them at a higher price on a future date; effectively a collateralised loan. |
| **Reverse Repo** | 逆回购 | 隔夜至数月 | Repo的对立面：买入证券并约定未来卖回，相当于以证券为担保的贷款。Mirror of repo: buying securities with agreement to resell; lending cash against collateral. |
| **O/N (Overnight)** | 隔夜 | 1天 | 起息日为今天，到期日为下一个工作日。Value today, matures next business day. |
| **T/N (Tom/Next)** | 明日隔夜 | 1天 | 起息日为明天（T+1），到期日为后天（T+2）。Value tomorrow (T+1), matures the day after (T+2). |
| **S/N (Spot/Next)** | 即期次日 | 1天 | 起息日为即期（T+2），到期日为T+3。Value spot (T+2), matures T+3. |

---

*上一阶段 / Prev: [Phase 02 — 金融市场与参与者](Phase-02-Financial-Markets.md)*  
*下一阶段 / Next: [Phase 04 — 权益市场](Phase-04-Equity-Markets.md)*
