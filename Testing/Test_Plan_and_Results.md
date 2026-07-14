# Test Plan & Results

## QA Strategy
| Test Type | What it Verifies |
|---|---|
| Unit Testing | Manually create Lead records with varying inputs to verify scoring logic |
| Validation Testing | Attempt to save invalid records (empty email, incorrect format) and confirm error messages appear |
| AI Testing | Submit leads with different industries and observe the variety/quality of AI-generated summaries |
| Security Testing | Log in as Sales Rep vs. Sales Manager to confirm field visibility and access are correctly restricted |

## Test Case Log
| # | Test Case | Steps | Expected Result | Actual Result | Status |
|---|---|---|---|---|---|
| 1 | Create Lead with valid email | Create Lead, valid company email | Lead saves successfully | | ⬜ |
| 2 | Create Lead with personal email | Enter a Gmail/Yahoo/Hotmail/Outlook address | Validation error blocks save | | ⬜ |
| 3 | Lead scoring — high engagement | Create Lead with Engagement Level = High, Industry = Technology | `Lead_Score__c` reflects high weighting | | ⬜ |
| 4 | Lead scoring — low engagement | Create Lead with Engagement Level = Low, Industry = Other | `Lead_Score__c` reflects low weighting | | ⬜ |
| 5 | AI Summary generation | Save a Lead with all fields populated | `AI_Summary__c` is populated with a relevant, readable summary | | ⬜ |
| 6 | Sales Rep access | Log in as John Rep | Can only see/edit own leads | | ⬜ |
| 7 | Sales Manager access | Log in as Jane Manager | Can see all leads in hierarchy + dashboards | | ⬜ |

Fill in "Actual Result" and flip Status to ✅ Pass / ❌ Fail as you run each test in your org, then attach the corresponding screenshot to `../Screenshots/07_Testing/`.

## Minimum Bar for Submission
At least 3 test leads created and verified end-to-end (per the project's Deliverable Checklist), covering at minimum: one valid save, one validation failure, and one AI summary generation.
