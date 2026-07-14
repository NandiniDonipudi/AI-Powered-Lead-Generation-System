# Implementation Roadmap (4-Hour Plan)

| Phase | Time | Activities | Status |
|---|---|---|---|
| 1. Org Setup | 15 min | Create Developer Org, enable Agentforce and Flow | ⬜ |
| 2. Lead Customization | 30 min | Add custom fields, validation rules, update page layouts | ⬜ |
| 3. Lightning App & Tabs | 20 min | Build the app, add Leads tab, configure navigation | ⬜ |
| 4. Security Model | 30 min | Create profiles, roles, and test users | ⬜ |
| 5. Automation (Flow) | 45 min | Design and activate the Record-Triggered Flow with scoring logic | ⬜ |
| 6. AI Integration | 45 min | Configure Prompt Builder, link to Agentforce, map to AI Summary field | ⬜ |
| 7. Testing | 30 min | Create sample leads, verify scoring, validate AI output | ⬜ |
| 8. GitHub & Documentation | 45 min | Initialize repository, commit changes, write README and project report | ⬜ |
| 9. Final Review & Submission | 20 min | Verify checklist, package artifacts, submit | ⬜ |

Mark each phase ✅ as you complete it in your actual org, and drop the corresponding screenshots into the matching `Screenshots/0N_.../` folder. Commit after each phase for a clean, incremental commit history (see `Prerequisites` below for the git commands).

## Prerequisites
- Valid Salesforce Developer Edition account (free)
- Basic familiarity with Salesforce Setup / Object Manager
- GitHub account (free)
- Git installed locally (recommended, not required — GitHub's web UI works too)
- Modern browser (Chrome/Firefox recommended)

## Salesforce Features to Enable
- Agentforce (Einstein GPT) — must be enabled in your org
- Flows — native, no extra license required
- Prompt Builder — requires permission to access

## Suggested Commit Cadence
```bash
git add Data-Model/ Screenshots/02_Lead_Customization/
git commit -m "Phase 2: add custom Lead fields and validation rule"

git add Security/ Screenshots/04_Security_Model/
git commit -m "Phase 4: add role hierarchy, profiles, and test users"

git add Automation/ Screenshots/05_Automation_Flow/
git commit -m "Phase 5: build and activate lead scoring flow"

git add AI-Integration/ Screenshots/06_AI_Integration/
git commit -m "Phase 6: configure Prompt Builder and AI Summary field"

git add Testing/ Screenshots/07_Testing/
git commit -m "Phase 7: end-to-end test results"
```
