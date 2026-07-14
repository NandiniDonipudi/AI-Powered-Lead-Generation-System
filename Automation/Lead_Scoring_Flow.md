# Lead Scoring Flow (Record-Triggered)

## Trigger
- **Object:** Lead
- **Trigger:** On create and on update
- **Type:** Record-Triggered Flow (Salesforce Flow Builder)

## Logic
1. Evaluate `Industry_Type__c`, Company, Lead Source, and `Engagement_Level__c`.
2. Apply scoring rules (example weighting — adjust to your actual implementation):
   | Factor | Condition | Points |
   |---|---|---|
   | Engagement Level | High | +40 |
   | Engagement Level | Medium | +20 |
   | Engagement Level | Low | +5 |
   | Industry Type | Technology or Finance | +20 |
   | Industry Type | Other | +5 |
   | Company | Populated | +10 |
   | Lead Source | Web / Referral | +15 |
3. Sum the points into `Lead_Score__c` (capped at 100).
4. Call the Prompt Template action (see `../AI-Integration/Prompt_Template.md`) to generate the AI summary.
5. Update `AI_Summary__c` with the returned text.

## Build Steps in Flow Builder
1. Setup → Flows → New Flow → Record-Triggered Flow
2. Object: Lead; Trigger: "A record is created or updated"
3. Add decision elements / formula resource to compute `Lead_Score__c`
4. Add an "Update Records" element to write `Lead_Score__c`
5. Add an Action element to invoke the Prompt Template, mapping Lead fields as inputs
6. Add a second "Update Records" element to write the returned summary into `AI_Summary__c`
7. Activate the flow

Screenshots for this phase: `../Screenshots/05_Automation_Flow/`
