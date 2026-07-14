# AI-Powered Lead Generation System

Salesforce-based lead scoring and qualification system that combines native automation (Flow) with Agentforce (Einstein GPT) to score leads and generate AI-written summaries for sales reps.

## Project Snapshot
| | |
|---|---|
| **Platform** | Salesforce Developer Edition |
| **Duration** | ~4 hours |
| **Audience** | University students / Salesforce beginners |
| **AI Engine** | Agentforce (Einstein GPT) via Prompt Builder |

## Repository Structure
```
AI-Powered-Lead-Generation-System/
├── README.md
├── .gitignore
├── Documentation/
│   ├── Project_Report.docx        # Full formal report
│   ├── Architecture.md            # Platform components + data flow
│   ├── Implementation_Roadmap.md  # 4-hour phased build plan
│   └── Success_Criteria.md        # Definition of "done"
├── Data-Model/
│   └── Lead_Custom_Fields.md      # Field-level spec for the Lead object
├── Security/
│   ├── Profiles_and_Roles.md      # Role hierarchy + profile permissions
│   └── Test_Users.md              # Test user accounts
├── Automation/
│   └── Lead_Scoring_Flow.md       # Record-Triggered Flow logic
├── AI-Integration/
│   └── Prompt_Template.md         # Prompt Builder config + AI Summary flow
├── Testing/
│   └── Test_Plan_and_Results.md   # QA strategy + test case log
└── Screenshots/
    ├── 01_Org_Setup/
    ├── 02_Lead_Customization/
    ├── 03_Lightning_App/
    ├── 04_Security_Model/
    ├── 05_Automation_Flow/
    ├── 06_AI_Integration/
    ├── 07_Testing/
    └── 08_Final_Submission/
```

## Core Features
- Custom Lead fields: `Lead_Score__c`, `AI_Summary__c`, `Industry_Type__c`, `Engagement_Level__c`
- Validation rules enforcing required/well-formatted Email and Company
- Dedicated "Lead Generation App" (Lightning App) with Leads, Reports, Dashboards tabs
- Role hierarchy: Sales Director → Sales Manager → Sales Representative
- Record-Triggered Flow that scores leads and invokes the AI prompt on create/update
- Agentforce-generated natural-language lead summaries via Prompt Builder

## Where to Look
- **Want the formal write-up?** → `Documentation/Project_Report.docx`
- **Want the technical spec for one piece (fields, flow, security, AI)?** → matching folder above
- **Want proof it works?** → `Testing/Test_Plan_and_Results.md` and `Screenshots/07_Testing/`

## Status
This README and the docs in this repo describe the system as designed in the project plan. Fill in the ✅/⬜ status markers in each doc and add your screenshots as you complete each phase — a repo that matches what's actually live in your org is worth more to a reviewer than one padded with placeholders.

## Team
**Institution:** ADITYA University – AP

| Name | 
|---|---|---|
| Nandini Donipudi |
| Naga Pushpa Latha Ravula | 
|Navya Kusunuri |
|Venkatesh Bachina|
|Harshith Sai Thonda| 


