# Foundation™ Team Training & Scenarios Guide

## 🎓 Training Your Team to Build Foundations

### Training Program Overview

**Week 1: Foundation Basics (Non-Technical)**
- Understanding the four agents
- Reading and interpreting agent responses
- Basic file structure navigation
- When to update what data

**Week 2: Research & Data Collection**
- Using web search effectively
- Identifying quality sources
- Formatting data for agents
- Creating comprehensive overviews

**Week 3: Client Implementation**
- Running discovery sessions
- Customizing agent prompts
- Building industry-specific knowledge
- Delivering value quickly

---

## 👥 Role-Based Training Paths

### For Project Managers
**Focus:** Client communication and project flow

**Day 1 Training:**
1. Understanding the Foundation value proposition
2. The four agents and their business roles
3. Reading the config file
4. Running basic agent queries

**Practice Scenario:**
```
A client asks: "How quickly can you show us value?"
Task: Use @NAVIGATOR to identify their biggest operational pain point from public data
Time: 15 minutes
Success: Identify one specific, measurable improvement opportunity
```

### For Research Analysts
**Focus:** Data collection and organization

**Day 1 Training:**
1. Web search techniques for business intelligence
2. Organizing information by agent domain
3. Writing clear, structured markdown files
4. Understanding data freshness

**Practice Scenario:**
```
Client: Regional manufacturing company
Task: Build complete competitor analysis for ATLAS
Time: 45 minutes
Success: 5 competitors with strengths/weaknesses documented
```

### For Technical VAs
**Focus:** System setup and maintenance

**Day 1 Training:**
1. GitHub basics (clone, commit, push)
2. File structure and naming conventions
3. YAML headers and agent scope
4. Setting up automated updates

**Practice Scenario:**
```
Task: Set up a new Foundation from template
Modify config for "ABC Corp"
Create company overview
Test all four agents
Time: 2 hours
```

---

## 🎮 Hands-On Training Scenarios

### Scenario 1: The Skeptical CEO
**Setup:** CEO thinks AI is just hype

**Your Mission:**
1. Use public data to build Foundation (30 min)
2. Have each agent identify one specific opportunity
3. Calculate potential ROI for each suggestion
4. Present as unified strategic plan

**Test Queries:**
```
@ATLAS What strategic move would give us immediate competitive advantage?
@NAVIGATOR Which process improvement would save the most money?
@MAESTRO What's the one system integration that would have biggest impact?
@CATALYST How do we get buy-in for this change?
```

**Success Metrics:**
- Each agent provides specific, actionable recommendation
- ROI calculations are realistic
- Recommendations align with each other

### Scenario 2: The Data-Hungry CFO
**Setup:** CFO wants everything quantified

**Your Mission:**
1. Focus on NAVIGATOR's operational metrics
2. Find industry benchmarks for comparison
3. Identify top 3 cost-saving opportunities
4. Create measurement framework

**Key Files to Create:**
```
NAVIGATOR/ops_metrics/
├── industry_benchmarks.md
├── cost_analysis.md
├── roi_projections.md
└── kpi_dashboard.md
```

**Success Metrics:**
- All recommendations include numbers
- Benchmarks are from credible sources
- ROI timeline is clear (30, 60, 90 days)

### Scenario 3: The Worried IT Director
**Setup:** Concerned about security and integration

**Your Mission:**
1. MAESTRO focuses on current tech assessment
2. Identify integration points (not replacements)
3. Address security concerns explicitly
4. Create phased technical roadmap

**Critical Questions to Answer:**
```
@MAESTRO How does this integrate with our existing systems?
@MAESTRO What security measures protect our data?
@MAESTRO Can we start small and expand?
@CATALYST How do we train our team on this?
```

### Scenario 4: The Burned Sales VP
**Setup:** Previous AI project failed spectacularly

**Your Mission:**
1. CATALYST identifies what went wrong before
2. NAVIGATOR shows quick operational wins
3. ATLAS provides competitive pressure context
4. MAESTRO keeps it simple initially

**Rebuild Trust Approach:**
```
@CATALYST What typically causes AI projects to fail?
@NAVIGATOR What's the smallest change with biggest impact?
@ATLAS What happens if we don't adopt AI?
@MAESTRO What's the simplest first step?
```

---

## 🔧 Troubleshooting Common Issues

### "I Don't Know What Data to Add"

**Solution Framework:**
1. Start with the company website
2. Check their latest news/blog
3. Look at job postings (reveals pain points)
4. Read customer reviews
5. Check competitor websites

**Minimum Viable Foundation:**
- Company overview (from website)
- 3 competitors (from Google)
- Industry trends (from news)
- Basic tech stack (from job posts)

### "The Agents Sound Generic"

**Diagnosis Prompts:**
```
@ATLAS Do you have access to the company overview file?
@ATLAS What industry is this company in?
@ATLAS What are their main products?
```

**Fixes:**
1. Check file has correct YAML header
2. Ensure agent_scope includes agent name
3. Add more specific industry context
4. Include actual company data, not just templates

### "Client Wants Different Agents"

**Customization Examples:**

**For Retail Client:**
- ATLAS → Market & Consumer Trends
- NAVIGATOR → Store Operations & Inventory
- MAESTRO → E-commerce & POS Systems
- CATALYST → Customer Experience

**For Healthcare Client:**
- ATLAS → Healthcare Policy & Competition
- NAVIGATOR → Patient Flow & Clinical Operations
- MAESTRO → EMR & Medical Systems
- CATALYST → Staff Training & Compliance

**Update agent prompts to reflect focus:**
```markdown
# In ATLAS.md for healthcare:
You are ATLAS, the Strategic Intelligence Officer for [CLIENT_NAME], 
specializing in healthcare market dynamics, regulatory changes, 
and competitive positioning in the medical sector.
```

### "How Do I Know It's Working?"

**Foundation Health Check:**

Level 1 - Basic Function:
```
@ATLAS What does this company do?
@NAVIGATOR What are their main operations?
@MAESTRO What technology do they use?
@CATALYST What's their reputation?
```

Level 2 - Integrated Intelligence:
```
@ATLAS @NAVIGATOR What's our biggest opportunity?
@MAESTRO @CATALYST How do we implement it?
```

Level 3 - Strategic Value:
```
@ATLAS If we had $1M to invest, where should it go?
@NAVIGATOR How would we measure success?
@MAESTRO What would we need to build?
@CATALYST How long until full adoption?
```

---

## 📚 Quick Reference Training Cards

### Card 1: The Foundation Formula
```
Public Data + Industry Context + Agent Intelligence = Business Insights
```

### Card 2: The Update Cycle
```
Weekly: News & Sentiment (CATALYST)
Bi-Weekly: Competitive Intel (ATLAS)
Monthly: Operations & Tech (NAVIGATOR/MAESTRO)
Quarterly: Full Review (ALL)
```

### Card 3: The Value Chain
```
Research (2 hrs) → Setup (1 hr) → Testing (30 min) → Client Demo (15 min)
Total Time Investment: ~4 hours
Client Value Delivered: Months of consulting work
```

### Card 4: The Quality Check
```
✓ Each agent answers specifically (not generically)
✓ Recommendations reference actual company data
✓ Agents build on each other's insights
✓ Clear next steps are identified
```

---

## 🎯 Certification Checklist

Before someone is certified to build Foundations:

### Knowledge Check:
- [ ] Can explain what each agent does in business terms
- [ ] Knows which agent to ask for what information
- [ ] Understands the file structure purpose
- [ ] Can write proper YAML headers

### Skill Check:
- [ ] Can set up a Foundation in under 4 hours
- [ ] Can use web search to populate agent knowledge
- [ ] Can test agent responses for quality
- [ ] Can identify when updates are needed

### Delivery Check:
- [ ] Can demo a Foundation to a client
- [ ] Can answer common objections
- [ ] Can customize for different industries
- [ ] Can train client team on usage

---

## 💡 Training Tips from the Field

1. **Start with Your Own Company**
   - Less pressure
   - You know what's right/wrong
   - Good for demos later

2. **Use Real Companies for Practice**
   - Public companies have more data
   - B2B companies are easier than B2C
   - Avoid stealth mode startups

3. **Time Yourself**
   - First Foundation: 6-8 hours
   - Second: 4-5 hours
   - Third: 2-3 hours
   - Goal: 2 hours for basic setup

4. **Common Beginner Mistakes**
   - Too much data (information overload)
   - Too generic (not company-specific)
   - Wrong agent boundaries (mixing domains)
   - Forgetting to test responses

5. **Build a Swipe File**
   - Save good prompts that worked
   - Keep templates for common industries
   - Document successful customizations
   - Share wins with team

Remember: Every Foundation gets easier. The goal is not perfection but a working system that delivers value. Your fourth Foundation will be 10x better than your first!