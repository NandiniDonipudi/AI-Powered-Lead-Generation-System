# Test Users

Created to simulate a real-world sales team and to verify role/profile-based access control.

| Full Name | Username | Profile | Role |
|---|---|---|---|
| Jane Manager | jane.manager@example.com | Sales Manager | Sales Manager |
| John Rep | john.rep@example.com | Sales Rep | Sales Representative |

## Verification Steps
1. Log in as **John Rep** → confirm he can only see/edit leads he owns
2. Log in as **Jane Manager** → confirm she can see all leads under her in the hierarchy, plus dashboards/reports
3. Attempt an action outside each profile's permissions (e.g., John deleting a lead) → confirm it's blocked

Screenshots for this phase: `../Screenshots/04_Security_Model/`
