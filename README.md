# Foundation™ Business Intelligence System

Welcome to the Foundation™ repository—a template for an AI-powered business intelligence system. This system leverages four specialized AI agents, each with their own knowledge domains, to provide strategic, operational, technical, and change management insights.

## 🚀 Quick Start (First Time Setup)

### Prerequisites
- GitHub account (free at github.com)
- Windsurf or Cursor IDE installed
- 2-4 hours for initial setup

### Step 1: Get This Template
```bash
# Clone this repository
git clone [repository-url] foundation-[company-name]
cd foundation-[company-name]

# Or download as ZIP and extract
```

### Step 2: Open in Your AI IDE
1. Open Windsurf or Cursor
2. File → Open Folder → Select your foundation folder
3. You should see the file structure on the left

### Step 3: Configure for Your Company (ALWAYS START HERE)
1. Open `foundation.config.yaml`
2. Replace all placeholder text with your company information:
```yaml
client:
  name: "Your Company Name"
  industry: "Your Industry"
  size: "50-200"  # Employee count
  website: "https://yourcompany.com"
```
3. Save the file (Ctrl+S or Cmd+S)

### Step 4: Create Company Overview
1. Open `shared_context/company_overview.md`
2. Delete the `.gitkeep` file in that folder
3. Use this exact prompt in Windsurf:
```
@Web Search and create a comprehensive company overview for [Company Name] with website [Website URL]. Include company snapshot, value proposition, products/services, differentiators, leadership team, and recent news.
```
4. Save the generated content

### Step 5: Test Your Agents
Try these commands in Windsurf:
```
@ATLAS Can you see the company overview? What's our main value proposition?
@NAVIGATOR What should be our top operational priorities?
@MAESTRO What technology improvements would have the most impact?
@CATALYST What change management challenges should we expect?
```

## 📁 Directory Structure
```
Foundation_Template/
├── .agents/                # System prompts for each AI agent
├── shared_context/         # Company-wide context files
├── ATLAS/                  # Strategic Intelligence (market, competition, finance)
├── NAVIGATOR/              # Operations Excellence (KPIs, sales, processes)
├── MAESTRO/                # Technology Integration (tech stack, talent, automation)
├── CATALYST/               # Change & Adoption (sentiment, change assets, performance)
├── .scripts/               # Automation scripts
├── .templates/             # Document templates
└── .workflows/             # Workflow automations
```

## 🤖 How It Works
- **@ mention any agent** (e.g., `@ATLAS`, `@NAVIGATOR`, `@MAESTRO`, `@CATALYST`) in your IDE or workflow.
- Agents respond in character, referencing their system prompts and knowledge base.
- Each agent has access to their specific folders and can cross-reference shared context for richer insights.

## 👥 Your AI Executive Team

### ATLAS - Strategic Intelligence Officer
- **Focus**: Market opportunities, competitive analysis, strategic planning
- **Ask About**: Market trends, competitors, growth opportunities, risks
- **Knowledge Base**: `/ATLAS/` folder

### NAVIGATOR - Operations Excellence Officer  
- **Focus**: KPIs, process optimization, operational efficiency
- **Ask About**: Bottlenecks, metrics, cost savings, performance
- **Knowledge Base**: `/NAVIGATOR/` folder

### MAESTRO - Technology Integration Officer
- **Focus**: Systems, integrations, automation opportunities
- **Ask About**: Tech stack, integrations, AI/ML opportunities, technical debt
- **Knowledge Base**: `/MAESTRO/` folder

### CATALYST - Change & Adoption Officer
- **Focus**: Change management, adoption strategies, team readiness
- **Ask About**: Resistance points, training needs, cultural fit, adoption tactics
- **Knowledge Base**: `/CATALYST/` folder

## 💬 Example Usage
```
@ATLAS What market opportunities should we pursue based on the trends in your market_landscape folder?
@NAVIGATOR What are our biggest operational bottlenecks according to the KPI data?
@MAESTRO Which system integration would provide the highest ROI?
@CATALYST How should we manage the change when implementing new AI systems?
```

## 📊 Populating with Real Data

### Recommended Order:
1. **CATALYST** first (gather external signals)
2. **ATLAS** second (strategic context)
3. **NAVIGATOR** third (operational details)
4. **MAESTRO** last (technical implementation)

### Quick Data Collection Prompts:

**For Market Intelligence (ATLAS):**
```
@Web Search the [Industry] industry trends, market size, growth rate, and key challenges for 2025. Save this in ATLAS/market_landscape/
```

**For Competitor Analysis (ATLAS):**
```
@Web Search for [Company Name]'s top 5 competitors with their strengths, weaknesses, and recent news.
```

**For Operational Metrics (NAVIGATOR):**
```
@Web Search for operational KPIs and benchmarks in the [Industry] industry. Include efficiency metrics and best practices.
```

**For Technology Stack (MAESTRO):**
```
@Web Search what technology [Company Name] uses based on BuiltWith, job postings, and public information.
```

## 🔧 Configuration
- Edit `foundation.config.yaml` in the root directory to set up your client profile and data sources
- Update agent prompts in `.agents/` folder if you need industry-specific customization
- All markdown files need proper YAML headers for agents to access them:

```yaml
---
title: "Document Title"
source: "Where this came from"
owner: "intel@tier4.ai"
agent_scope: ["ATLAS", "NAVIGATOR", "MAESTRO", "CATALYST"]
created: "2025-01-20"
tags: ["relevant", "tags"]
---
```

## 🔄 Maintenance
- **Daily**: News and competitor updates (optional)
- **Weekly**: Sentiment and market changes (recommended)
- **Monthly**: Full review of all data (required)
- Mark updated dates in file headers when you make changes

## ❓ Troubleshooting

**"Agent can't see the files"**
- Check the YAML header includes the agent name in `agent_scope`
- Make sure the file is saved
- Try closing and reopening the file

**"Agents sound generic"**
- Make sure you've added company-specific data to their folders
- Check that `foundation.config.yaml` has your company details
- Verify agents can access the company overview file

**"Web search not working"**
- Use `@Web` exactly as shown in the prompts
- Be specific in your search requests
- Break complex searches into smaller parts

## 📚 Additional Resources
For detailed guides, see:
- Setup Guide: `docs/setup-guide.md`
- Maintenance Guide: `docs/maintenance-guide.md`
- Training Guide: `docs/training-guide.md`

## 🎯 Success Checklist
- [ ] Config file has your company information
- [ ] Company overview file created and saved
- [ ] Each agent responds with company-specific insights
- [ ] At least 3-4 files populated per agent
- [ ] Cross-agent collaboration tested
- [ ] Next steps and opportunities identified

---

For more details and sample data, see the files in `shared_context/`, `ATLAS/`, `NAVIGATOR/`, `MAESTRO/`, and `CATALYST/`.

Remember: The goal is a working Foundation that delivers insights, not perfection. You can always add more data and refine agent responses over time!