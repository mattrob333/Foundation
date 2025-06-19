# Foundation™ Repository Structure

```
tier4-foundation-[CLIENT_NAME]/
│
├── README.md                    # Foundation overview & setup instructions
├── .gitignore                   # Ignore sensitive files
├── foundation.config.yaml       # Client configuration
│
├── .agents/                     # Agent System Prompts
│   ├── ATLAS.md                # Strategic Intelligence Officer prompt
│   ├── NAVIGATOR.md            # Operations Excellence Officer prompt
│   ├── MAESTRO.md              # Technology Integration Officer prompt
│   └── CATALYST.md             # Change & Adoption Officer prompt
│
├── shared_context/             # Company-wide intelligence
│   ├── company_overview.md     # [✓] Public data
│   ├── org_chart.md           # [✓] LinkedIn data
│   ├── product_portfolio.md    # [✓] From website
│   ├── core_processes.md      # [ ] Internal - pending
│   └── revenue_breakdown.md    # [ ] Internal - pending
│
├── ATLAS/                      # Strategic Intelligence
│   ├── market_landscape/
│   │   ├── industry_value_chain.md      # [✓]
│   │   ├── key_trends_2025.md          # [✓]
│   │   └── regulation_watchlist.md      # [✓]
│   ├── competitors/
│   │   ├── top_competitors_list.md      # [✓]
│   │   └── feature_benchmarks.md        # [✓]
│   ├── finance/
│   │   ├── last_3_annual_reports.md     # [ ]
│   │   └── quarterly_earnings_summary.md # [ ]
│   └── strategic_plans/
│       └── board_strategy_deck.md        # [ ]
│
├── NAVIGATOR/                  # Operational Excellence
│   ├── ops_metrics/
│   │   ├── kpi_snapshot_public.md       # [✓]
│   │   └── internal_kpi_dashboard.md    # [ ]
│   ├── sales_marketing/
│   │   ├── public_pricing_scrape.md     # [✓]
│   │   └── CAC_LTV_report.md           # [ ]
│   └── process_docs/
│       └── SOP_library_index.md         # [ ]
│
├── MAESTRO/                    # Technology Integration
│   ├── tech_stack/
│   │   ├── public_tech_stack.md         # [✓]
│   │   └── system_architecture.md       # [ ]
│   ├── talent/
│   │   ├── hiring_trends.md             # [✓]
│   │   ├── skill_gap_heatmap.md        # [✓]
│   │   └── full_skills_matrix.md       # [ ]
│   └── workflow_opportunities/
│       └── automation_candidates.md      # [ ]
│
├── CATALYST/                   # Change Management
│   ├── sentiment/
│   │   ├── news_mentions.md             # [✓]
│   │   └── customer_reviews.md          # [✓]
│   ├── change_assets/
│   │   ├── change_management_plan.md    # [ ]
│   │   └── training_materials_index.md  # [ ]
│   └── performance/
│       └── adoption_metrics_dashboard.md # [ ]
│
├── .scripts/                   # Automation scripts
│   ├── collect_public_data.py  # Scrape public sources
│   ├── update_market_data.py   # RSS feeds, APIs
│   ├── generate_reports.py     # Weekly summaries
│   └── requirements.txt        # Python dependencies
│
├── .templates/                 # Document templates
│   ├── company_overview_template.md
│   ├── competitor_analysis_template.md
│   └── kpi_dashboard_template.md
│
└── .workflows/                 # GitHub Actions
    ├── daily_intelligence_update.yml
    ├── weekly_report_generation.yml
    └── data_quality_check.yml
```

## Agent System Prompts

### `.agents/ATLAS.md`
```markdown
---
agent: ATLAS
role: Strategic Intelligence Officer
version: 1.0
---

# ATLAS - Strategic Intelligence Officer

You are ATLAS, the Strategic Intelligence Officer for [CLIENT_NAME]. You operate at the 30,000-foot level, identifying market opportunities, competitive threats, and transformative strategies.

## Core Responsibilities
- Market trend analysis and forecasting
- Competitive intelligence gathering
- Strategic opportunity identification
- Risk assessment and mitigation strategies
- M&A target evaluation

## Knowledge Base Access
- Primary: `/ATLAS/` directory
- Secondary: `/shared_context/` for company overview
- Cross-reference: NAVIGATOR for operational feasibility

## Key Behaviors
1. Always think 2-3 years ahead
2. Connect disparate market signals
3. Identify non-obvious opportunities
4. Challenge status quo assumptions
5. Provide actionable strategic insights

## Output Format
- Executive summaries with clear recommendations
- Competitive positioning matrices
- Market opportunity assessments
- Strategic risk evaluations

@company_context: shared_context/company_overview.md
@market_data: ATLAS/market_landscape/
@competitors: ATLAS/competitors/
```

### `.agents/NAVIGATOR.md`
```markdown
---
agent: NAVIGATOR
role: Operations Excellence Officer
version: 1.0
---

# NAVIGATOR - Operations Excellence Officer

You are NAVIGATOR, the Operations Excellence Officer for [CLIENT_NAME]. You translate strategic vision into actionable plans, optimize performance, and track KPIs.

## Core Responsibilities
- Operational planning and optimization
- KPI definition and tracking
- Resource allocation strategies
- Process improvement identification
- Performance gap analysis

## Knowledge Base Access
- Primary: `/NAVIGATOR/` directory
- Secondary: `/shared_context/` for processes
- Cross-reference: ATLAS for strategic alignment

## Key Behaviors
1. Focus on measurable outcomes
2. Identify operational bottlenecks
3. Optimize resource utilization
4. Create actionable roadmaps
5. Track progress relentlessly

@operations: NAVIGATOR/ops_metrics/
@processes: shared_context/core_processes.md
@sales_data: NAVIGATOR/sales_marketing/
```

## Why This Works

### 1. **IDE Integration Benefits**
- Cursor/Windsurf can @ mention agent personas
- Agents can directly read/update their knowledge bases
- Web search can auto-update market intelligence
- Git tracks all changes and evolution

### 2. **Systematization Opportunities**
```python
# Example: collect_public_data.py
def initialize_foundation(company_name, website):
    # Scrape company website
    # Pull Crunchbase data
    # Analyze LinkedIn presence
    # Check BuiltWith for tech stack
    # Search news mentions
    # Generate initial files
```

### 3. **Training & Scaling**
- Create a "Foundation Template" repo
- Clone for each new client
- Run initialization scripts
- VA team can fill in public data
- Client provides internal data post-contract

### 4. **Continuous Intelligence**
- GitHub Actions update market data daily
- RSS feeds populate news mentions
- API integrations pull fresh metrics
- Agents learn from every update

## Implementation Steps

1. **Create Template Repository**
   - Set up base structure
   - Write agent system prompts
   - Create data collection scripts

2. **Build Initialization Process**
   - Input: Company name, website, industry
   - Output: Pre-populated Foundation with public data
   - Time: 2-4 hours automated + VA review

3. **IDE Configuration**
   - Create `.cursorrules` or `.windsurfrules`
   - Define agent personas as references
   - Set up auto-completion for file paths

4. **Client Onboarding Flow**
   ```
   1. Clone template → 2. Run initialization → 3. VA enhancement
   → 4. Client demo → 5. Add internal data → 6. Activate agents
   ```

This approach is incredibly scalable and could revolutionize how you deliver the Foundation™ service!