# All-Hands Meeting Transcript Processing Checklist

## 🎯 Purpose
This checklist helps process meeting transcripts to extract Foundation-worthy information while discarding noise. Load this into an AI with your transcript and say: "Process this meeting transcript using the Foundation checklist."

---

## 📋 Pre-Processing Setup

**Meeting Information:**
- Date: _______________
- Duration: ___________
- Key Attendees: _________________
- Meeting Purpose: _______________

**Have Ready:**
- [ ] Meeting transcript or recording
- [ ] Access to Foundation repository
- [ ] List of current company initiatives
- [ ] Previous meeting's action items

---

## 🔍 Step 1: Initial Transcript Scan

First, identify and mark these categories in the transcript:

```
[S] = Strategic (ATLAS)
[O] = Operational (NAVIGATOR)  
[T] = Technical (MAESTRO)
[C] = Cultural/Change (CATALYST)
[X] = Discard (not Foundation-worthy)
[?] = Unclear (needs verification)
```

---

## 📊 Step 2: Categorization Criteria

### [S] STRATEGIC - Goes to ATLAS
✅ **Include if it's about:**
- Market expansion or contraction
- New products/services launching
- Competitive moves or responses
- Partnerships or acquisitions
- Long-term goals (1+ years out)
- Major investment decisions
- Industry trends discussed
- Board-level decisions

❌ **Exclude if it's:**
- Just an idea with no commitment
- Personal opinions about strategy
- Speculation about competitors

**Qualifying Questions:**
- Will this affect company direction?
- Is there budget allocated?
- Did leadership commit to this?

### [O] OPERATIONAL - Goes to NAVIGATOR
✅ **Include if it's about:**
- KPI changes or new metrics
- Process improvements implemented
- Cost savings initiatives
- Revenue targets or sales goals
- Efficiency improvements
- Resource allocation changes
- Department restructuring
- Performance benchmarks

❌ **Exclude if it's:**
- One-time operational issues
- Individual performance
- Daily task assignments
- Routine status updates

**Qualifying Questions:**
- Does this change how we measure success?
- Will this affect multiple teams?
- Is this a new standard going forward?

### [T] TECHNICAL - Goes to MAESTRO
✅ **Include if it's about:**
- New systems being adopted
- Integration projects approved
- Security policy changes
- Technical stack decisions
- Automation initiatives
- Data management changes
- Infrastructure updates
- AI/ML implementations

❌ **Exclude if it's:**
- Bug fixes or minor updates
- Individual technical tasks
- Routine maintenance
- Personal tool preferences

**Qualifying Questions:**
- Does this affect our technical architecture?
- Will multiple systems need to change?
- Is there a significant budget involved?

### [C] CULTURAL/CHANGE - Goes to CATALYST
✅ **Include if it's about:**
- Leadership changes
- New company policies
- Cultural initiatives
- Training programs launching
- Communication changes
- Employee engagement initiatives
- Change management plans
- Team morale indicators

❌ **Exclude if it's:**
- Individual HR issues
- One-time events
- Personal announcements
- Office logistics

**Qualifying Questions:**
- Does this affect how people work?
- Will this require behavior change?
- Does everyone need to know this?

### [X] DISCARD - Not Foundation-Worthy
Always exclude:
- Meeting logistics ("next meeting is...")
- Personal updates ("Bob's on vacation")
- Routine acknowledgments ("good job team")
- Speculation or rumors
- Off-topic discussions
- Individual task assignments
- Temporary situations

---

## 🔄 Step 3: Processing Workflow

### A. First Pass - Mark Everything
Read through transcript and add tags:
```
Example:
"CEO: We're officially entering the Canadian market next quarter [S] 
and Jim will be leading the expansion [C]. The coffee machine 
is broken [X] but we've allocated $2M for the initiative [S]."
```

### B. Second Pass - Extract Tagged Items
Create temporary lists:

**Strategic Items [S]:**
1. ______________________
2. ______________________

**Operational Items [O]:**
1. ______________________
2. ______________________

**Technical Items [T]:**
1. ______________________
2. ______________________

**Cultural Items [C]:**
1. ______________________
2. ______________________

**Needs Verification [?]:**
1. ______________________
2. ______________________

### C. Third Pass - Apply Quality Filters

For each item, ask:

**The 3-Month Test**
- [ ] Will this matter in 3 months?
- [ ] If no → Discard

**The New Employee Test**
- [ ] Would a new employee need to know this?
- [ ] If no → Discard

**The Decision Test**
- [ ] Is this a decision or just discussion?
- [ ] If just discussion → Buffer for 1 week

**The Scope Test**
- [ ] Does this affect multiple people/departments?
- [ ] If no → Likely discard

---

## 📝 Step 4: Format for Foundation

### Template for Each Item:

```markdown
## Update: [Date] All-Hands Meeting

### What Changed:
- [Concise description of the decision/change]

### Impact:
- [How this affects operations/strategy/etc.]

### Effective Date:
- [When this takes effect]

### Source:
- All-Hands Meeting [Date]
- Announced by: [Name/Title]
```

---

## 🎯 Step 5: Final Checklist

Before adding to Foundation:

- [ ] Is the information factual (not speculation)?
- [ ] Has it been confirmed by leadership?
- [ ] Is it formatted clearly?
- [ ] Is it in the right agent folder?
- [ ] Does it have proper YAML headers?
- [ ] Have you removed any personal/confidential info?
- [ ] Is the language professional and neutral?

---

## 💾 Step 6: Implementation

### For Each Approved Item:

1. **Navigate to correct folder:**
   - Strategic → `ATLAS/strategic_plans/`
   - Operational → `NAVIGATOR/ops_metrics/`
   - Technical → `MAESTRO/workflow_opportunities/`
   - Cultural → `CATALYST/change_assets/`

2. **Update or create file:**
   - If updating: Add date header
   - If new: Create with proper template

3. **Save with clear commit message:**
   ```
   git commit -m "Added Q1 strategic initiatives from Jan 27 all-hands"
   ```

---

## 🤖 AI Processing Prompt

To use this checklist with AI:

```
I have a meeting transcript that needs to be processed for our Foundation knowledge base. Please:

1. Tag each item as [S]trategic, [O]perational, [T]echnical, [C]ultural, or [X]discard
2. Apply the quality filters (3-month test, new employee test, etc.)
3. Format the qualifying items using the template
4. Tell me which folder each item should go in
5. Flag anything that needs verification

Here's the transcript: [PASTE TRANSCRIPT]
```

---

## 📊 Quick Reference Card

| Type | Agent | Key Question | Folder |
|------|-------|--------------|---------|
| Strategic | ATLAS | "Does this change our direction?" | `/ATLAS/strategic_plans/` |
| Operational | NAVIGATOR | "Does this change how we operate?" | `/NAVIGATOR/ops_metrics/` |
| Technical | MAESTRO | "Does this change our systems?" | `/MAESTRO/workflow_opportunities/` |
| Cultural | CATALYST | "Does this change our culture?" | `/CATALYST/change_assets/` |

---

## 🚫 Red Flags - Never Add These

- Anything marked "confidential" or "do not share"
- Personal employee information
- Unconfirmed rumors or speculation
- Complaints or negative feedback about individuals
- Specific salary information
- Legal matters under discussion
- Information about potential layoffs

Remember: When in doubt, leave it out. It's better to have less high-quality information than more low-quality information.