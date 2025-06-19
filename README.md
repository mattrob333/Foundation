# Foundation™ Business Intelligence System

Welcome to the Foundation™ repository—a template for an AI-powered business intelligence system. This system leverages four specialized AI agents, each with their own knowledge domains, to provide strategic, operational, technical, and change management insights.

## How It Works
- **@ mention any agent** (e.g., `@ATLAS`, `@NAVIGATOR`, `@MAESTRO`, `@CATALYST`) in your IDE or workflow.
- Agents respond in character, referencing their system prompts and knowledge base.
- Each agent has access to their specific folders and can cross-reference shared context for richer insights.

## Directory Structure
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

## Agents
- **ATLAS**: Strategic Intelligence Officer
- **NAVIGATOR**: Operations Excellence Officer
- **MAESTRO**: Technology Integration Officer
- **CATALYST**: Change & Adoption Officer

## Example Usage
- `@ATLAS What market opportunities should we pursue based on the trends in your market_landscape folder?`
- `@NAVIGATOR What are our biggest operational bottlenecks according to the KPI data?`
- `@MAESTRO Which system integration would provide the highest ROI?`
- `@CATALYST How should we manage the change when implementing new AI systems?`

## Getting Started
1. Review the agent prompts in `.agents/` to understand their personalities and capabilities.
2. Populate the knowledge folders with your company data, or use the sample files provided.
3. Use @ mentions to interact with agents and get context-aware insights.

## Configuration
- Edit `foundation.config.yaml` in the root directory to set up your client profile and data sources.

For more details and sample data, see the files in `shared_context/`, `ATLAS/`, `NAVIGATOR/`, `MAESTRO/`, and `CATALYST/`.
