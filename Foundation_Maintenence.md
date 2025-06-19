# Foundation™ Maintenance & Update Guide

## 🔄 When and How to Update Your Foundation

### Understanding Data Freshness

Different types of data age at different rates:

| Data Type | Update Frequency | Signs It's Stale |
|-----------|-----------------|------------------|
| Company Overview | Quarterly | New leadership, merger, rebrand |
| Market Trends | Monthly | Season change, major events |
| Competitor Intel | Bi-weekly | New product launches, pricing |
| Tech Stack | Monthly | Job posting changes |
| News/Sentiment | Weekly | No recent mentions |
| Financial Data | Quarterly | Earnings releases |

### How to Check for Stale Data

**Quick Staleness Check Prompt:**
```
@ATLAS @NAVIGATOR @MAESTRO @CATALYST Review your knowledge bases and identify any data older than [30/60/90] days that might need updating. List specific files and why they might be outdated.
```

### The Update Process

#### Step 1: Weekly Review (Every Monday)
Run this check with your agents:
```
@CATALYST What major events happened with the company last week that we should document?
@ATLAS Any competitor moves or market changes we should capture?
@NAVIGATOR Any new performance data or metrics available?
@MAESTRO Any technology changes or new integrations announced?
```

#### Step 2: Update Specific Files
For each item identified, update the specific file:

**Example Update Prompt:**
```
@Web Search for [Company Name] news in the last 7 days. Update the CATALYST/sentiment/news_mentions.md file with any significant developments.
```

#### Step 3: Mark Updates in Files
Always update the header when you modify a file:
```yaml
---
title: "Market Analysis"
source: "Industry reports, news"
owner: "intel@tier4.ai"
agent_scope: ["ATLAS"]
created: "2025-01-20"
updated: "2025-01-27"  # ADD THIS LINE
tags: ["market", "analysis", "current"]
---
```

---

## 🎯 Strategic Update Order

Update agents in this specific order and here's why:

### 1. CATALYST First (External Signals)
- Monitors news, sentiment, changes
- Alerts other agents to investigate
- Most time-sensitive information

**Update Prompt:**
```
@Web @CATALYST Search for any news, reviews, or mentions of [Company Name] in the last week. What's changed?
```

### 2. ATLAS Second (Strategic Impact)
- Assesses if external changes affect strategy
- Updates market positioning
- Identifies new opportunities/threats

**Update Prompt:**
```
@Web @ATLAS Based on CATALYST's findings, are there any strategic implications? Check for competitor responses or market shifts.
```

### 3. NAVIGATOR Third (Operational Adjustments)
- Determines operational impact
- Updates KPIs if needed
- Adjusts process recommendations

**Update Prompt:**
```
@NAVIGATOR Given the strategic updates from ATLAS, what operational metrics or processes need attention?
```

### 4. MAESTRO Last (Technical Implementation)
- Plans technical responses
- Updates integration priorities
- Adjusts automation roadmap

**Update Prompt:**
```
@MAESTRO Based on all updates, what technical changes or new integrations should we prioritize?
```

---

## 📊 Creating Data Feeds

### RSS Feed Setup for Automatic Monitoring

Create `.scripts/rss_feeds.json`:
```json
{
  "company_news": {
    "google_news": "https://news.google.com/rss/search?q=[Company+Name]",
    "industry_news": "https://news.google.com/rss/search?q=[Industry]+news",
    "competitor_news": "https://news.google.com/rss/search?q=[Competitor+Name]"
  },
  "update_frequency": "daily",
  "agents_to_notify": ["CATALYST", "ATLAS"]
}
```

### Setting Up Google Alerts
1. Go to google.com/alerts
2. Create alerts for:
   - "[Company Name]" news
   - "[Company Name]" AND "[Industry]"
   - "[Main Competitor]" AND "announcement"
   - "[Industry]" AND "AI" AND "automation"

3. Set delivery to weekly digest
4. Add RSS feed URLs to your monitoring

---

## 🔍 Quality Control Checklist

### Before Each Update Session:
- [ ] Check last update dates in file headers
- [ ] Review any GitHub issues or reminders
- [ ] Have company website open for reference
- [ ] Clear 30 minutes uninterrupted time

### During Updates:
- [ ] Start with CATALYST for external signals
- [ ] Follow the strategic update order
- [ ] Cross-reference multiple sources
- [ ] Mark [UNCONFIRMED] for uncertain data
- [ ] Update the `updated:` date in headers

### After Updates:
- [ ] Test agents with current event questions
- [ ] Save all modified files
- [ ] Create note about major changes
- [ ] Set reminder for next update

---

## 🚨 Red Flags That Require Immediate Updates

Update immediately if you discover:

1. **Leadership Changes**
   - New CEO/CFO/CTO
   - Major departures
   - Board changes

2. **Strategic Shifts**
   - Merger or acquisition
   - New product line
   - Market exit/entry
   - Major partnership

3. **Crisis Events**
   - Security breach
   - Major lawsuit
   - Regulatory action
   - PR crisis

4. **Competitive Disruption**
   - New major competitor
   - Disruptive technology
   - Price war
   - Market consolidation

**Emergency Update Prompt:**
```
@Web Search for breaking news about [Company Name] regarding [specific event]. Update all relevant agent knowledge bases with implications.
```

---

## 📈 Measuring Foundation Health

### Weekly Health Check:
```
@ATLAS How current is your strategic intelligence (rate 1-10)?
@NAVIGATOR Are your KPIs and metrics up to date (rate 1-10)?
@MAESTRO Is your technical knowledge current (rate 1-10)?
@CATALYST How fresh is your sentiment data (rate 1-10)?
```

Scores below 7 indicate update needed.

### Monthly Deep Dive:
```
@ATLAS @NAVIGATOR @MAESTRO @CATALYST Each identify:
1. Your most outdated piece of intelligence
2. The highest priority update needed
3. Any data you need but don't have
```

---

## 🔄 Automated Update Scripts

### Simple Update Reminder Script

Create `.scripts/check_updates.py`:
```python
import os
import datetime
from pathlib import Path

def check_file_age(directory):
    old_files = []
    for file_path in Path(directory).rglob('*.md'):
        # Check file modification time
        mod_time = datetime.datetime.fromtimestamp(os.path.getmtime(file_path))
        age_days = (datetime.datetime.now() - mod_time).days
        
        if age_days > 30:
            old_files.append({
                'file': file_path,
                'age_days': age_days,
                'agent': file_path.parts[0]
            })
    
    return old_files

# Check each agent's files
for agent in ['ATLAS', 'NAVIGATOR', 'MAESTRO', 'CATALYST']:
    old = check_file_age(agent)
    if old:
        print(f"\n{agent} has {len(old)} files older than 30 days:")
        for file in old:
            print(f"  - {file['file']}: {file['age_days']} days old")
```

---

## 💡 Pro Tips for Efficient Updates

1. **Batch Similar Updates**
   - Update all competitor files together
   - Update all metrics at once
   - Group news/sentiment updates

2. **Use Templates for Consistency**
   ```markdown
   ## Update: [Date]
   ### What Changed:
   - [Bullet points of changes]
   ### Impact:
   - [How this affects our recommendations]
   ### Source:
   - [Links to sources]
   ```

3. **Create Update Aliases**
   Save common update prompts as snippets:
   - "Weekly news check"
   - "Competitor update"
   - "Metrics refresh"
   - "Tech stack scan"

4. **Version Important Changes**
   For major updates, note the version:
   ```yaml
   # In file header
   version: "2.0"  # Major strategy shift
   version_notes: "Added EV market analysis after pivot announcement"
   ```

Remember: A Foundation with 80% current data that's actively used is infinitely more valuable than one with 100% perfect data that's never updated!