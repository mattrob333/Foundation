# Foundation™ Complete Setup Guide - Non-Developer Edition

## 🎯 What This Guide Does
This guide walks you through setting up a Foundation™ - an AI-powered business intelligence system with four AI executives that understand a specific company. Load this entire document into Claude, ChatGPT, or Windsurf and say: "Walk me through setting up a Foundation for [Company Name]"

---

## 📋 Pre-Setup Checklist

Before starting, gather:
- [ ] Company name and website
- [ ] Your GitHub account (free at github.com)
- [ ] Windsurf or Cursor IDE installed
- [ ] 2-4 hours of uninterrupted time

---

## 🚀 PHASE 1: Initial Setup (30 minutes)

### Step 1.1: Get the Template
1. Go to the Foundation Template repository
2. Click the green "Code" button
3. Click "Download ZIP"
4. Extract the ZIP file to your computer
5. Rename the folder from `foundation-template` to `foundation-[company-name]`
   - Example: `foundation-tesla` or `foundation-acme-corp`

### Step 1.2: Open in Windsurf/Cursor
1. Open Windsurf or Cursor
2. Click "File" → "Open Folder"
3. Select your `foundation-[company-name]` folder
4. You should see the file structure on the left side

### Step 1.3: First File to Modify - Configuration
**ALWAYS START HERE:** `foundation.config.yaml`

1. Double-click `foundation.config.yaml` to open it
2. Replace the placeholder text:

```yaml
client:
  name: "[REPLACE WITH COMPANY NAME]"
  industry: "[REPLACE WITH INDUSTRY - e.g., Software, Manufacturing, Healthcare]"
  size: "[REPLACE WITH EMPLOYEE COUNT - e.g., 50-200]"
  website: "[REPLACE WITH WEBSITE - e.g., https://example.com]"
```

Example:
```yaml
client:
  name: "Acme Manufacturing Corp"
  industry: "Automotive Parts Manufacturing"
  size: "200-500"
  website: "https://acmemfg.com"
```

3. Save the file (Ctrl+S or Cmd+S)

---

## 🏢 PHASE 2: Company Overview (45 minutes)

### Step 2.1: Create Company Overview
**Second file to modify:** `shared_context/company_overview.md`

1. Open `shared_context/company_overview.md`
2. Delete `.gitkeep` file in this folder if it exists
3. Ask Windsurf with web search:

**EXACT PROMPT TO USE:**
```
@Web Search and create a comprehensive company overview for [Company Name] with website [Website URL]. 

Include:
1. Company snapshot (founded, HQ, employees, revenue if public)
2. Their main value proposition 
3. Products/services offered
4. Key differentiators
5. Leadership team (from LinkedIn)
6. Recent news or milestones

Format this as a markdown file following the template in company_overview.md
```

4. Review and refine the generated content
5. Save the file

### Step 2.2: Verify Agent Access
1. Test that agents can see the overview:
   ```
   @ATLAS Can you see the company overview? What's the company's main value proposition?
   ```
2. If the agent can't see it, check that `agent_scope: ["ATLAS", "NAVIGATOR", "MAESTRO", "CATALYST"]` is in the file header

---

## 🎯 PHASE 3: Strategic Intelligence with ATLAS (1 hour)

### Step 3.1: Market Landscape Research
**File:** `ATLAS/market_landscape/industry_analysis.md`

**EXACT PROMPT FOR WINDSURF:**
```
@Web Search the [Industry] industry and create an industry analysis for [Company Name]. Include:

1. Market size and growth rate
2. Key trends for 2025
3. Major challenges facing the industry
4. Regulatory changes or requirements
5. Technology disruptions affecting the industry
6. Strategic opportunities and threats

Save this in proper markdown format with YAML header for ATLAS agent access.
```

### Step 3.2: Competitor Analysis
**File:** `ATLAS/competitors/competitor_landscape.md`

**EXACT PROMPT:**
```
@Web Search for [Company Name]'s top 5 competitors. For each competitor include:

1. Company name and size
2. Their key strengths and weaknesses  
3. Their value proposition
4. Approximate pricing (if available)
5. Recent strategic moves or news

Also identify how [Company Name] differentiates from these competitors.
```

### Step 3.3: Test ATLAS Understanding
```
@ATLAS Based on the market landscape and competitor data, what are the top 3 strategic opportunities for this company?
```

---

## 📊 PHASE 4: Operational Intelligence with NAVIGATOR (45 minutes)

### Step 4.1: Public Performance Metrics
**File:** `NAVIGATOR/ops_metrics/public_kpis.md`

**EXACT PROMPT:**
```
@Web Search for operational metrics and KPIs for [Company Name]. Look for:

1. Website traffic data (SimilarWeb)
2. Employee satisfaction (Glassdoor ratings)
3. Customer reviews and ratings
4. Industry benchmark KPIs for [Industry]
5. Growth indicators (hiring trends, expansion news)

Format as a KPI dashboard with actual vs industry benchmark where possible.
```

### Step 4.2: Process Intelligence
**File:** `NAVIGATOR/process_docs/industry_best_practices.md`

**EXACT PROMPT:**
```
@Web Search for best practices in [Industry] operations. Include:

1. Typical core processes in this industry
2. Common operational bottlenecks
3. Industry-standard KPIs and metrics
4. Automation trends in [Industry]
5. Operational excellence examples

This helps NAVIGATOR understand what good operations look like in this industry.
```

---

## 🔧 PHASE 5: Technical Intelligence with MAESTRO (45 minutes)

### Step 5.1: Technology Stack Discovery
**File:** `MAESTRO/tech_stack/current_technology.md`

**EXACT PROMPT:**
```
@Web Search what technology [Company Name] uses. Check:

1. BuiltWith.com data for their website
2. Job postings for technology requirements
3. Their website footer for platform indicators
4. LinkedIn for technology skills their employees have
5. Any technical blog posts or case studies

Create a comprehensive tech stack overview including gaps and opportunities.
```

### Step 5.2: Integration Opportunities
**File:** `MAESTRO/workflow_opportunities/automation_candidates.md`

**EXACT PROMPT:**
```
Based on [Company Name]'s industry and size, identify:

1. Top 5 processes that could be automated
2. Common system integrations needed in [Industry]
3. AI/ML opportunities specific to their business
4. Estimated ROI for each automation opportunity
5. Quick wins vs long-term projects

Focus on practical, achievable automations for a [Size] company.
```

---

## 🚀 PHASE 6: Change Intelligence with CATALYST (30 minutes)

### Step 6.1: Sentiment Analysis
**File:** `CATALYST/sentiment/public_perception.md`

**EXACT PROMPT:**
```
@Web Search for sentiment about [Company Name]. Analyze:

1. Recent news articles (last 6 months)
2. Glassdoor reviews and themes
3. Customer reviews and feedback
4. Social media mentions
5. Industry forum discussions

Identify perception strengths and gaps that would affect AI adoption.
```

### Step 6.2: Change Readiness
**File:** `CATALYST/change_assets/readiness_assessment.md`

**CREATE THIS CONTENT:**
```markdown
# Change Readiness Assessment

## Industry Change Indicators
- How quickly does [Industry] typically adopt new technology?
- What's the typical employee tech-savviness?
- Common resistance points in this industry?

## Company-Specific Factors
- Recent technology implementations
- Employee demographics and tenure
- Leadership technology stance
- Current pain points that create urgency
```

---

## ✅ PHASE 7: Validation and Activation (30 minutes)

### Step 7.1: Test Each Agent

Run these test queries in order:

1. **Test ATLAS:**
   ```
   @ATLAS What's the biggest strategic opportunity for this company based on your market intelligence?
   ```

2. **Test NAVIGATOR:**
   ```
   @NAVIGATOR What operational improvements would have the highest impact?
   ```

3. **Test MAESTRO:**
   ```
   @MAESTRO What's the first system integration we should tackle?
   ```

4. **Test CATALYST:**
   ```
   @CATALYST What change management challenges should we prepare for?
   ```

### Step 7.2: Cross-Agent Intelligence Test
```
@ATLAS @NAVIGATOR @MAESTRO @CATALYST If this company wanted to grow revenue by 20% next year, what would each of you recommend as your top priority?
```

---

## 💾 PHASE 8: Saving and Version Control

### When to Save:
- ✅ After completing each major file
- ✅ When agents successfully answer questions
- ✅ Before taking any break
- ✅ After any significant updates

### How to Save:
1. In Windsurf: Ctrl+S (PC) or Cmd+S (Mac)
2. To save all files: Ctrl+K then S

### Setting Up Automated Updates:
**File:** `.github/workflows/weekly_update.yml`

```yaml
name: Weekly Intelligence Update
on:
  schedule:
    - cron: '0 9 * * 1'  # Every Monday 9 AM
    
jobs:
  remind:
    runs-on: ubuntu-latest
    steps:
      - name: Create Issue
        uses: actions/github-script@v6
        with:
          script: |
            github.rest.issues.create({
              owner: context.repo.owner,
              repo: context.repo.repo,
              title: 'Weekly Intelligence Update Needed',
              body: 'Time to update market intelligence and check for outdated data'
            })
```

---

## 📅 Ongoing Maintenance Schedule

### Daily (Optional):
- News mentions
- Competitor updates
- Market alerts

### Weekly (Recommended):
- KPI updates
- Sentiment analysis
- Technology news

### Monthly (Required):
- Full market landscape review
- Strategy adjustments
- New automation opportunities

### Quarterly:
- Complete Foundation review
- Agent prompt refinements
- ROI assessment

---

## 🚨 Common Issues and Solutions

### "Agent can't see the files"
- Check YAML header includes agent in `agent_scope`
- Ensure file is saved
- Try closing and reopening the file

### "Web search not working"
- Make sure you use @Web exactly as shown
- Include specific details in your search request
- Break complex searches into smaller parts

### "Don't know what data to add"
- Start with what you know
- Use the prompts exactly as provided
- Mark unknown items as [TODO] and continue

### "Overwhelmed by the amount of work"
- This is a 2-4 hour process
- Take breaks between phases
- Remember: 80% complete is better than 0%

---

## 🎯 Success Checklist

By the end, you should have:
- [ ] 1 config file updated
- [ ] 1 company overview file
- [ ] 3-4 files per agent (12-16 total)
- [ ] Each agent responding intelligently
- [ ] Cross-agent collaboration working
- [ ] Clear next steps identified

---

## 💬 Quick Reference Prompts

Copy these exactly when setting up:

**For Company Research:**
```
@Web Search for comprehensive information about [Company Name] including history, products, leadership, and recent news
```

**For Industry Analysis:**
```
@Web Search [Industry] industry analysis including market size, growth trends, major players, and 2025 outlook
```

**For Competitor Research:**
```
@Web Search top competitors to [Company Name] in the [Industry] space with their strengths and weaknesses
```

**For Technology Stack:**
```
@Web Search what technology and software [Company Name] uses based on BuiltWith, job postings, and public information
```

---

## 🎉 Completion Message

When done, test your Foundation with:
```
@ATLAS @NAVIGATOR @MAESTRO @CATALYST Please each give me your #1 insight about this company based on your current intelligence.
```

If each agent provides a relevant, specific insight, your Foundation is ready!

---

## 📞 Getting Help

If stuck at any step:
1. Copy the exact step you're on
2. Include any error messages
3. Share what you've tried
4. Ask: "I'm on Step [X.X] and [specific issue]. How do I proceed?"

Remember: The goal is a working Foundation, not perfection. You can always improve and add more data later!