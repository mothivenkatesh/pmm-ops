# Signzy MCC Classification & Onboarding Suite -- Step 1: Research Output

---

## 1. ICP & Market Research

### Ideal Customer Profile

**Company Type & Industry:**
- **Primary ICP:** RBI-licensed Payment Aggregators (PA-Online, PA-Physical, PA-Cross Border) that must onboard and classify merchants under correct MCCs as mandated by RBI Master Direction 2025. There are 50+ licensed PAs in India as of mid-2025, with the top 3 (Razorpay, PayU, Cashfree) controlling ~70-80% of new merchant onboarding volume.
- **Secondary ICP:** Acquiring banks (SBI, HDFC, ICICI, Axis, YES Bank etc.) that assign MCCs to merchants in card payment flows and bear ultimate regulatory liability for MCC accuracy. Approximately 20-25 major acquiring banks operate in India.
- **Tertiary ICP:** Large NBFCs and neobanks launching merchant acceptance / BaaS products that need compliant onboarding rails without building in-house.

**Size:**
- Payment Aggregators onboarding 10,000+ merchants/month (mid-market) to 500,000+/month (enterprise like Razorpay with 10M+ merchants).
- Acquiring banks processing 1M+ card transactions/month where MCC accuracy drives interchange economics, GST compliance, and dispute outcomes.

**Must-Have Criteria (Unit of Work):**
- The unit of work is a **single merchant onboarded and classified** -- meaning one KYC-verified, MCC-assigned, compliance-cleared merchant record. Signzy charges per successful onboarding/verification transaction (~65% of revenue is transaction-based).
- Must-haves: (a) RBI PA license or application in progress, (b) active merchant acquisition pipeline, (c) existing or planned digital onboarding flow, (d) regulatory obligation for MCC assignment and CDD.

**Buyer Persona:**
| Attribute | Detail |
|-----------|--------|
| Title | VP/Head of Compliance, Chief Risk Officer, Head of Merchant Onboarding, or Head of Product (Payments) |
| Pain | Manual MCC classification is error-prone, slow (days per merchant), and creates regulatory exposure. RBI Master Direction 2025 tightened CDD requirements and penalties for misclassification. Every wrongly classified merchant = GST liability risk + potential RBI audit flag + interchange leakage. |
| Decision Criteria | (1) Accuracy of automated MCC assignment, (2) RBI compliance coverage out-of-the-box, (3) API-first integration with existing onboarding stack, (4) Speed -- reduce merchant go-live from days to minutes, (5) Audit trail and reporting for regulatory submissions. |
| Budget Authority | Compliance/Risk head signs off on vendor; CTO/Head of Product approves technical integration. Deals typically need dual sign-off. |

**End User Persona:**
- **Merchant Onboarding Operations Analyst** -- runs 50-200 merchant applications/day through the system. Needs a clean dashboard, bulk processing, exception handling for edge-case MCCs, and one-click regulatory report generation.
- **Compliance Officer** -- reviews flagged merchants, validates MCC assignments against RBI/Visa/Mastercard/RuPay code tables, runs periodic re-classification audits.

**Current Way (What They Do Today):**
1. **Manual classification:** Ops teams cross-reference merchant business descriptions against a spreadsheet of ~800+ MCC codes. Senior analysts handle ambiguous cases. Takes 15-45 min per merchant for complex cases.
2. **Fragmented tooling:** Many PAs use one vendor for KYC (PAN/Aadhaar verification), another for bank account validation, and a third for business verification -- with MCC assignment done manually in between.
3. **Periodic audit panic:** Compliance teams run quarterly or annual MCC audits manually, often discovering hundreds of misclassified merchants that require retroactive correction and reporting to card networks.
4. **Rule-based scripts:** Some larger PAs have built internal rule engines mapping keywords to MCCs, but these break on edge cases (multi-category businesses, new business types) and require constant maintenance.

**Buying Triggers:**
1. **RBI Master Direction Sept 2025:** The consolidated PA Directions made MCC validation and CDD a hard compliance requirement with tighter enforcement. PAs that were previously informal about MCC assignment must now demonstrate systematic processes.
2. **RBI license grant or renewal:** New PA license recipients (9 approved in 2025 alone) need compliant onboarding infrastructure from day one.
3. **Merchant onboarding ban/lift:** RBI has historically suspended onboarding for non-compliant PAs (Razorpay and Cashfree experienced bans). The risk of onboarding suspension is a powerful motivator.
4. **Scale inflection:** When a PA crosses ~50K active merchants, manual MCC classification becomes operationally unsustainable.
5. **Card network audits:** Visa/Mastercard periodically audit MCC accuracy of acquirers. Failed audits lead to fines and remediation mandates.
6. **IPO/fundraise preparation:** Razorpay filed for IPO in Jan 2026. Investors and auditors demand demonstrable compliance infrastructure.

---

### ICP Scorecard (FletchPMM Methodology)

| Dimension | Score (1-10) | Evidence |
|-----------|:---:|----------|
| **Retention** | 8 | Once a PA integrates Signzy's onboarding + MCC APIs into their merchant acquisition flow, switching costs are very high (re-integration, re-validation of existing merchant base, compliance continuity risk). Signzy processes 10M+ onboardings/month across clients -- evidence of deep workflow embedding. 65% of revenue is transaction-based, meaning retention correlates with client growth. |
| **Access** | 7 | Compliance heads and onboarding product leads at PAs are identifiable and reachable through industry events (Global Fintech Fest, NASSCOM), RBI working groups, and NPCI forums. However, enterprise bank procurement cycles are slow (6-9 months). Signzy already serves 240+ FIs and 4 of India's largest banks, demonstrating established access channels. Mid-market PAs are more accessible. |
| **Sales Velocity** | 6 | Enterprise deals with banks take 6-9 months with POCs, security reviews, and procurement. Mid-market PA deals can close in 2-3 months given regulatory urgency. The Sept 2025 RBI directive created a time-bound compliance window that accelerates velocity. However, budget cycles at banks remain rigid. Signzy's no-code platform and 3-4 week deployment claim (vs. 6-month in-house builds) helps compress cycles. |
| **Activation** | 8 | Time-to-value is fast because MCC misclassification is a measurable, auditable problem. A PA can run their existing merchant base through Signzy's classification engine and immediately see the error rate delta. Signzy claims 99% success rate on onboarding and speed-to-market reduction from 6 months to 3-4 weeks. ROI is directly calculable: (manual ops cost saved) + (penalties avoided) + (interchange leakage recovered). |

**Composite ICP Score: 7.25/10** -- Strong ICP. Retention and Activation are the leading indicators. Sales Velocity is the constraint, particularly for bank segment.

---

### TAM Sizing (Triangulated)

#### Bottom-Up Estimate

| Segment | Count | Avg Annual Contract Value (ACV) | Segment TAM |
|---------|------:|------:|------:|
| Top-tier PAs (Razorpay, PayU, Cashfree, PhonePe, BillDesk etc.) | 10 | INR 3-5 Cr ($360-600K) -- high volume, enterprise pricing | INR 40 Cr ($4.8M) |
| Mid-tier licensed PAs | 40 | INR 50L-1.5Cr ($60-180K) -- growing merchant base | INR 40 Cr ($4.8M) |
| PA applicants / pre-license fintechs | ~50 | INR 20-50L ($24-60K) -- starting small | INR 17.5 Cr ($2.1M) |
| Acquiring banks (top 25) | 25 | INR 1-3 Cr ($120-360K) -- card-network MCC compliance | INR 50 Cr ($6M) |
| Large NBFCs with merchant acceptance | 30 | INR 30-75L ($36-90K) | INR 15 Cr ($1.8M) |
| **Total Bottom-Up TAM** | **~155 accounts** | | **INR 162.5 Cr (~$19.5M)** |

*Assumptions: ACV includes onboarding platform license + per-transaction MCC classification + compliance reporting modules. Based on Signzy's ~INR 111 Cr FY24 revenue across all products and ~$40-50M ARR run-rate in early 2026, the MCC/merchant onboarding vertical likely represents 25-35% of total revenue.*

#### Top-Down Estimate

- India digital merchant onboarding platform market: $1.4B globally in 2025, India estimated at 8-10% = ~$112-140M.
- Signzy's addressable slice (MCC classification + compliance onboarding for regulated entities, not full merchant onboarding platforms like Stripe): approximately 15-20% of the India portion = **$17-28M**.
- India e-KYC market alone is $26.3M (2024), growing at 20.3% CAGR. MCC classification is an adjacent vertical that piggybacks on this infrastructure.

#### Analogy Estimate

- Signzy's comparable in the US/EU is Sardine (fraud + onboarding compliance, raised $70M, valued ~$500M) and Alloy (identity + compliance orchestration, $235M raised). Both serve a similar "compliance infrastructure for fintechs" niche.
- India's regulated fintech ecosystem is roughly 1/5th the size of the US by revenue but growing faster. Applying a 1/5th ratio to Alloy's estimated ~$100M ARR suggests a ~$20M opportunity for the India leader.
- Cross-reference: Signzy at ~$40-50M ARR total, with MCC/onboarding at 25-35%, implies ~$10-17.5M current revenue from this vertical -- consistent with a ~$20M near-term TAM.

#### Triangulated TAM: ~$19-22M for India MCC Classification + Compliant Merchant Onboarding

#### SOM (Serviceable Obtainable Market -- Reachable NOW)

- Signzy already serves 240+ FIs. For the MCC vertical specifically:
  - **Existing clients upsell:** 40-60 current PA/bank clients who can be upsold the MCC classification module = INR 30-40 Cr ($3.6-4.8M)
  - **New logo acquisition:** 20-30 newly licensed or compliance-pressured PAs reachable in next 12 months = INR 10-20 Cr ($1.2-2.4M)
  - **SOM estimate: $4.8-7.2M in next 12 months**
- This assumes Signzy can convert 30-40% of the addressable base, which is realistic given their brand, existing relationships, and the regulatory tailwind from Sept 2025 RBI directions.

---

### Key Gaps to Validate

1. **MCC-specific product maturity:** Signzy's website prominently covers KYC/KYB/AML but MCC classification is mentioned only in blog content, not as a standalone product page. Need to validate: Is MCC classification a launched, GA product or still in development/beta? What is the actual classification accuracy rate vs. manual processes?

2. **Competitive positioning vs. IDfy:** IDfy has a dedicated "Merchant Onboarding" product page and explicitly targets PAs. How does Signzy's MCC engine compare on accuracy, coverage of India-specific MCC codes (especially RuPay codes), and pricing?

3. **PA buyer willingness to pay:** Many mid-tier PAs may view MCC classification as a feature within their existing KYC vendor relationship, not a standalone purchase. Need to validate whether Signzy sells MCC as a standalone module or only as part of a broader onboarding suite -- and whether PAs have separate budget for it.

4. **Actual enforcement intensity:** While RBI Master Direction 2025 tightened requirements, it is unclear how aggressively RBI is enforcing MCC accuracy specifically (vs. other PA compliance requirements like net worth, grievance redressal). Need to validate through conversations with PA compliance heads whether MCC is a "hair on fire" problem or a "nice to have."

5. **Build vs. buy dynamics:** Large PAs like Razorpay (10M+ merchants, IPO-bound) may prefer to build in-house MCC classification using their own data. Signzy's sweet spot may be the mid-tier PAs (50K-500K merchants) who lack engineering resources. This segmentation needs validation.

6. **International expansion leverage:** Signzy claims 180+ country coverage. Does the MCC product work for cross-border PAs (PA-CB category)? This could meaningfully expand TAM if validated.

7. **Revenue attribution:** Signzy's $40-50M ARR run-rate is across all products. The specific revenue contribution of MCC classification vs. broader KYC/KYB modules is not publicly broken out. Need internal data to size this accurately.

---

## Data Sources & References

- [Signzy MCC Guide](https://www.signzy.com/blogs/guide-on-merchant-category-code-mcc)
- [Signzy Digital Onboarding](https://www.signzy.com/digital-onboarding/)
- [Signzy Funding - Crunchbase](https://www.crunchbase.com/organization/signzy)
- [Signzy Financials - Tracxn](https://tracxn.com/d/companies/signzy/__FKmMW-C-ZqyWKlnCs2jeeZcdbBJFnHhjkB4fWlblLW4)
- [Signzy How It Works - Business Model Canvas](https://businessmodelcanvastemplate.com/blogs/how-it-works/signzy-how-it-works)
- [Signzy Empowers Payment Aggregators](https://www.signzy.com/blogs/how-signzy-empowers-payment-aggregators-in-a-licensed-landscape)
- [RBI PA Master Direction 2025 - AuthBridge Analysis](https://authbridge.com/blog/rbi-payment-aggregator-master-direction-2025/)
- [RBI PA Directions 2025 - India Corp Law](https://indiacorplaw.in/2025/10/09/decoding-rbis-overhaul-of-the-payment-aggregator-directions/)
- [RBI PA Directions - Lexology](https://www.lexology.com/library/detail.aspx?g=66e43cc2-d69d-42a3-87f8-2381a386ea89)
- [RBI PA Compliance Mandate - Mondaq](https://www.mondaq.com/india/financial-services/1706010/rbi-master-direction-2025-compliance-mandate-for-payment-aggregators-and-pa-p-deadline)
- [MCC Misuse Crackdown - LinkedIn](https://www.linkedin.com/pulse/rbis-crackdown-mcc-misuse-wake-up-call-fintechs-ram-rastogi--815ef)
- [India Payment Gateway Market - Mordor Intelligence](https://www.mordorintelligence.com/industry-reports/india-payment-gateway-market)
- [India e-KYC Market - IMARC](https://www.imarcgroup.com/india-e-kyc-market)
- [India Identity Verification Market - UnivDatos](https://univdatos.com/reports/india-identity-verification-market)
- [India KYC Industry - The Indian Eye](https://theindianeye.com/2025/10/02/indias-kyc-industry-builds-trust-in-digital-identity-verification/)
- [Digital Merchant Onboarding Market](https://www.marketreportanalytics.com/reports/digital-merchant-onboarding-platform-73341)
- [PayU PA License - Business Standard](https://www.business-standard.com/finance/news/payu-secures-final-rbi-approval-as-online-payment-aggregator-125051301470_1.html)
- [Razorpay Statistics 2026 - CoinLaw](https://coinlaw.io/razorpay-statistics/)
- [Signzy Competitors - HyperVerge](https://hyperverge.co/blog/signzy-competitors/)
- [IDfy Merchant Onboarding](https://www.idfy.com/identity-verification-solutions-by-idfy/merchant-onboarding/)
- [MCC India List - Open Money](https://open.money/blog/merchant-category-code-list-in-india/)
- [Signzy Capterra](https://www.capterra.com/p/10009382/Signzy/)
