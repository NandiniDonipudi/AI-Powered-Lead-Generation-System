# Architecture

## Platform Components
| Component | Purpose |
|---|---|
| Salesforce Developer Org | Sandbox where all configuration happens |
| Object Manager | Modify the Lead object, create custom fields |
| Lightning App Builder | Assemble the "Lead Generation App" UI |
| Flow Builder | Build the declarative Record-Triggered Flow |
| Prompt Builder | Construct the AI prompt sent to Agentforce |
| Agentforce (Einstein GPT) | Generates lead summaries and insights |

## Data Flow
1. A Lead record is created or updated (manually, via web form, or import).
2. The Record-Triggered Flow fires on create/update.
3. The Flow evaluates `Industry_Type__c`, Company, Lead Source, and `Engagement_Level__c`.
4. The Flow computes `Lead_Score__c` (0–100) using the scoring rules in `Automation/Lead_Scoring_Flow.md`.
5. The Flow invokes the Prompt Template (see `AI-Integration/Prompt_Template.md`).
6. Agentforce returns a natural-language summary, which is written to `AI_Summary__c`.
7. The sales rep sees the score and summary directly on the Lead record and prioritizes outreach accordingly.

## System Diagram (textual)
```
Lead Created/Updated
        │
        ▼
Record-Triggered Flow ──► Score Lead_Score__c
        │
        ▼
Prompt Template ──► Agentforce (Einstein GPT)
        │
        ▼
AI_Summary__c populated
        │
        ▼
Sales Rep sees score + summary on Lead
```

## Related Docs
- Field definitions: `../Data-Model/Lead_Custom_Fields.md`
- Flow logic: `../Automation/Lead_Scoring_Flow.md`
- AI configuration: `../AI-Integration/Prompt_Template.md`
- Security model: `../Security/Profiles_and_Roles.md`
