# Security Model — Profiles & Roles

## Role Hierarchy
```
Sales Director (Top)
└── Sales Manager
    └── Sales Representative
```

## Profiles
| Profile | Access |
|---|---|
| **Sales Rep** | View, create, and edit their own leads; limited reporting access |
| **Sales Manager** | View all leads in the hierarchy; access to dashboards and reports; can approve/delete records |

## Setup Steps
1. Setup → Roles → set up the hierarchy above (Sales Director → Sales Manager → Sales Representative)
2. Setup → Profiles → clone Standard User profile twice → rename to "Sales Rep Profile" and "Sales Manager Profile"
3. Adjust object/field permissions per the access table above
4. Assign each profile its matching role when creating users

Screenshots for this phase: `../Screenshots/04_Security_Model/`
