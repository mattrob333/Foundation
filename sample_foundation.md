# Sample Foundation™ Data Files

## shared_context/company_overview.md

```markdown
---
title: "Company Overview - Global Parts Manufacturing Inc."
source: "Crunchbase, Website, LinkedIn"
owner: "intel@tier4.ai"
agent_scope: ["ATLAS", "NAVIGATOR", "MAESTRO", "CATALYST"]
created: "2025-01-20"
tags: ["company", "public", "overview"]
---

# Global Parts Manufacturing Inc.

## Company Snapshot
- **Founded**: 2010
- **Headquarters**: Detroit, Michigan
- **Employees**: 450 (350 production, 100 office)
- **Revenue**: $150M (2024)
- **Growth Rate**: 12% YoY
- **Market Position**: #3 in Midwest aftermarket parts

## Value Proposition
"Precision parts delivered faster than OEM at 30% less cost"

## Product Lines
1. **Engine Components** (40% of revenue)
   - Pistons, rings, bearings
   - 2-day delivery guarantee
   
2. **Transmission Parts** (35% of revenue)
   - Gears, synchronizers, clutches
   - 99.2% quality rating

3. **Suspension Systems** (25% of revenue)
   - Struts, springs, control arms
   - Newest product line (2022)

## Key Differentiators
- Proprietary quick-manufacturing process
- Industry-leading 2-day delivery
- ISO 9001:2015 certified
- Direct-to-installer model

## Leadership Team
- **CEO**: Michael Chen (LinkedIn: /in/michaelchen-gpm)
- **COO**: Sarah Johnson (15 years automotive experience)
- **CFO**: David Park (Former Tesla Finance)
- **CTO**: Lisa Rodriguez (Pioneer in additive manufacturing)

## Recent Milestones
- 2024 Q3: Launched AI-powered inventory prediction
- 2024 Q2: Opened third manufacturing facility
- 2024 Q1: Achieved B Corp certification
```

## ATLAS/market_landscape/key_trends_2025.md

```markdown
---
title: "Automotive Aftermarket Trends 2025"
source: "IBISWorld, McKinsey Automotive, Google Trends"
owner: "intel@tier4.ai"
agent_scope: ["ATLAS"]
created: "2025-01-20"
updated: "2025-01-20"
tags: ["market", "trends", "public"]
---

# Key Market Trends - Automotive Aftermarket 2025

## 1. EV Transition Impact 🔋
- **Trend**: 35% of new vehicles are EVs/Hybrids
- **Impact**: Traditional parts demand shifting
- **Opportunity**: EV-specific components market growing 78% YoY
- **Action**: Develop EV parts line by Q3 2025

## 2. Digital-First Purchasing 💻
- **Trend**: 67% of installers order parts online
- **Impact**: Physical distributors losing market share
- **Opportunity**: Direct-to-installer e-commerce
- **Competitor**: RockAuto growing 45% YoY

## 3. Predictive Maintenance AI 🤖
- **Trend**: Smart diagnostics predicting part failures
- **Impact**: Shift from reactive to proactive replacement
- **Opportunity**: Partner with diagnostic platforms
- **Market Size**: $2.3B by 2027

## 4. Supply Chain Localization 🏭
- **Trend**: "Near-shoring" post-COVID
- **Impact**: Advantage for domestic manufacturers
- **Opportunity**: "Made in USA" premium pricing
- **Risk**: Material costs up 23%

## 5. Sustainability Mandates ♻️
- **Trend**: California requiring 50% recycled materials
- **Impact**: New compliance requirements by 2026
- **Opportunity**: First-mover in green parts
- **Investment Needed**: $2-3M for recycling tech

## Strategic Implications
1. **Immediate** (Q1 2025): Launch e-commerce platform
2. **Short-term** (Q2-Q3): Develop EV parts capability
3. **Medium-term** (Q4): Implement predictive analytics
4. **Long-term** (2026): Recycling technology integration
```

## NAVIGATOR/ops_metrics/kpi_snapshot_public.md

```markdown
---
title: "Public KPI Intelligence"
source: "Industry reports, Glassdoor, SimilarWeb, LinkedIn"
owner: "intel@tier4.ai"
agent_scope: ["NAVIGATOR"]
created: "2025-01-20"
tags: ["kpi", "metrics", "public", "benchmark"]
---

# Operational KPI Intelligence

## Website Performance (SimilarWeb)
- **Monthly Visits**: 45,000
- **Bounce Rate**: 38% (Industry avg: 45%)
- **Avg Session**: 3:24 minutes
- **Conversion Rate**: ~2.5% (estimated)

## Employee Metrics (Glassdoor/LinkedIn)
- **Glassdoor Rating**: 4.2/5 (87 reviews)
- **Employee Growth**: +15% YoY
- **Open Positions**: 12 (8 production, 4 tech)
- **Key Complaint**: "Outdated inventory system"

## Industry Benchmarks
| Metric | GPM Inc. | Industry Avg | Leader |
|--------|----------|--------------|---------|
| Delivery Time | 2 days | 5 days | 1 day |
| Defect Rate | 0.8% | 2.1% | 0.3% |
| Inventory Turns | 12x | 8x | 15x |
| EBITDA Margin | ~18% | 15% | 22% |

## Customer Indicators
- **Google Reviews**: 4.6★ (312 reviews)
- **Common Praise**: "Fast shipping"
- **Common Complaint**: "Limited EV parts"
- **NPS Score**: Estimated 45-50

## Operational Opportunities
1. **Inventory System**: 3+ hours daily wasted (per Glassdoor)
2. **Website Conversion**: Below industry 3.5% benchmark
3. **Delivery Speed**: Could charge premium for 1-day
4. **EV Parts Gap**: Missing fastest-growing segment
```

## MAESTRO/tech_stack/public_tech_stack.md

```markdown
---
title: "Technology Stack Analysis"
source: "BuiltWith, Job postings, Website analysis"
owner: "intel@tier4.ai"
agent_scope: ["MAESTRO"]
created: "2025-01-20"
tags: ["technology", "systems", "public"]
---

# Current Technology Stack

## Core Systems (Identified)
### ERP/Finance
- **System**: NetSuite (confirmed via job posting)
- **Version**: Likely 2022.2 or newer
- **Gaps**: No AI/ML modules active

### CRM/Sales
- **System**: Salesforce (Sales Cloud)
- **Integrations**: Mailchimp (marketing)
- **Gap**: No Service Cloud for support

### E-commerce
- **Platform**: WooCommerce (WordPress)
- **Hosting**: AWS (us-east-1)
- **Performance**: 3.2s load time (needs optimization)

### Manufacturing Systems
- **MES**: Custom-built (job posting mentions "proprietary MES")
- **Age**: Likely 5+ years (seeking modernization)
- **Integration**: Manual data transfer (major bottleneck)

## Development Stack
- **Frontend**: React (website), jQuery (legacy)
- **Backend**: Node.js, some Python scripts
- **Database**: MySQL (primary), MongoDB (analytics)
- **Cloud**: AWS (partial migration from on-prem)

## Analytics & Monitoring
- **Web**: Google Analytics 4
- **Infrastructure**: Basic CloudWatch
- **Business Intelligence**: Excel-based (!)

## Identified Tech Debt
1. **No API between MES and NetSuite** (manual daily uploads)
2. **13 different Excel-based reports** (from job description)
3. **No unified data warehouse**
4. **Limited automation** (seeking RPA developer)

## Automation Opportunities
- **Priority 1**: MES-NetSuite integration ($300K annual savings)
- **Priority 2**: Automated reporting dashboard ($150K savings)
- **Priority 3**: Predictive inventory AI ($500K impact)
- **Priority 4**: Customer service chatbot ($200K savings)
```

## CATALYST/sentiment/news_mentions.md

```markdown
---
title: "Recent News & Sentiment Analysis"
source: "Google News, Industry publications, Social media"
owner: "intel@tier4.ai"
agent_scope: ["CATALYST"]
created: "2025-01-20"
tags: ["sentiment", "news", "public", "reputation"]
---

# News & Sentiment Tracking

## Recent News Coverage

### Positive Mentions 📈
1. **Detroit Business Journal** (Jan 15, 2025)
   - "GPM Inc leads in 2-day delivery promise"
   - Highlighted as local success story
   - CEO quoted on growth plans

2. **Automotive Aftermarket News** (Jan 8, 2025)
   - Featured in "Top 10 Innovators"
   - Praised quick-manufacturing process
   - Mentioned B Corp certification

3. **LinkedIn Viral Post** (Jan 5, 2025)
   - Employee shared culture story
   - 15K likes, 500+ comments
   - Theme: "Company that cares"

### Neutral/Concerning Mentions 📊
1. **Industry Week** (Dec 20, 2024)
   - "Mid-size manufacturers face EV transition"
   - GPM mentioned as "adapting slowly"
   - Highlighted market pressures

2. **Reddit r/AutoRepair** (Ongoing)
   - Mixed reviews on parts quality
   - Praise for speed, concerns on EV options
   - Competitors mentioned frequently

## Social Sentiment Analysis
- **LinkedIn**: 89% positive (great employer brand)
- **Twitter/X**: 76% positive (delivery speed praised)
- **Reddit**: 65% positive (quality debates)
- **Facebook**: 81% positive (local community support)

## Key Themes
### Strengths in Public Perception
- ✅ Fast delivery is signature differentiator
- ✅ Employee satisfaction visible externally
- ✅ B Corp status resonates with younger demos
- ✅ "David vs Goliath" story appeals

### Perception Gaps to Address
- ❌ Limited EV expertise perception
- ❌ "Traditional" vs innovative image
- ❌ Price concerns among budget installers
- ❌ Tech capabilities underappreciated

## Change Management Implications
1. **Build on**: Employee advocacy program
2. **Address**: EV transition narrative
3. **Amplify**: Innovation stories
4. **Prepare for**: AI implementation announcement
```

## README.md

```markdown
# Foundation™ - Global Parts Manufacturing Inc.

This repository contains the Foundation™ intelligence system for Global Parts Manufacturing Inc.

## 🤖 Your AI Executive Team

- **ATLAS** - Strategic Intelligence Officer
- **NAVIGATOR** - Operations Excellence Officer  
- **MAESTRO** - Technology Integration Officer
- **CATALYST** - Change & Adoption Officer

## 📁 Repository Structure

```
├── .agents/          → AI Executive system prompts
├── shared_context/   → Company-wide intelligence
├── ATLAS/           → Strategic market intelligence
├── NAVIGATOR/       → Operational metrics and processes
├── MAESTRO/         → Technology and integration data
├── CATALYST/        → Change management and sentiment
├── .scripts/        → Automation and update scripts
└── .workflows/      → GitHub Actions for continuous updates
```

## 🚀 Quick Start

### For AI IDEs (Cursor/Windsurf)

1. Clone this repository
2. Open in Cursor or Windsurf
3. Use @ mentions to reference agents:
   - `@ATLAS` - For strategic questions
   - `@NAVIGATOR` - For operational insights
   - `@MAESTRO` - For technical recommendations
   - `@CATALYST` - For change management

### Example Queries

```
@ATLAS What market opportunity should we pursue next?
@NAVIGATOR What's our biggest operational bottleneck?
@MAESTRO Which system integration would save us the most money?
@CATALYST How do we get the team excited about AI?
```

## 📊 Intelligence Status

| Agent | Public Data | Internal Data | Last Updated |
|-------|------------|---------------|--------------|
| Shared Context | 14/14 ✓ | 0/5 | 2025-01-20 |
| ATLAS | 8/8 ✓ | 0/3 | 2025-01-20 |
| NAVIGATOR | 3/3 ✓ | 0/3 | 2025-01-20 |
| MAESTRO | 4/4 ✓ | 0/3 | 2025-01-20 |
| CATALYST | 2/2 ✓ | 0/3 | 2025-01-20 |

## 🔄 Automated Updates

- **Daily**: Market news, competitor updates
- **Weekly**: Performance metrics, sentiment analysis
- **Monthly**: Strategic reviews, trend analysis

## 🔐 Security

- All internal data is encrypted
- Access controls via GitHub permissions
- Audit trail maintained for all changes

---

*Powered by Tier 4 Intelligence*
```