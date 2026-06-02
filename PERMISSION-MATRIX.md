# Permission Matrix

## Roles

- System Administrator
- Case Manager
- Analyst
- Attorney or Counsel
- Supervisor or Reviewer
- Records Clerk
- Read-Only Stakeholder

## Access Matrix

|        Capability        | Admin |     Case Manager     |        Analyst       |       Counsel        | Supervisor |    Records Clerk     | Read Only |
| ------------------------ | ----- | -------------------- | -------------------- | -------------------- | ---------- | -------------------- | --------- |
| View all cases           | Yes   | Assigned / permitted | Assigned / permitted | Assigned / permitted | Team cases | Archival / permitted | Yes       |
| Create case              | Yes   | Yes                  | No                   | No                   | No         | No                   | No        |
| Edit case core fields    | Yes   | Yes                  | Limited              | Limited              | Limited    | No                   | No        |
| Update case status       | Yes   | Yes                  | No                   | Limited              | Yes        | No                   | No        |
| Assign tasks             | Yes   | Yes                  | Yes                  | No                   | Yes        | No                   | No        |
| Edit task status         | Yes   | Yes                  | Yes                  | Yes                  | Yes        | No                   | No        |
| Add notes                | Yes   | Yes                  | Yes                  | Yes                  | Yes        | Limited              | No        |
| View audit history       | Yes   | Yes                  | Yes                  | Yes                  | Yes        | Limited              | Yes       |
| Attach document metadata | Yes   | Yes                  | No                   | No                   | No         | Yes                  | No        |
| Manage users and roles   | Yes   | No                   | No                   | No                   | No         | No                   | No        |
| Manage system settings   | Yes   | No                   | No                   | No                   | No         | No                   | No        |

## Permission Rules

- access is granted by role and case assignment
- sensitive fields should be hidden or read-only where appropriate
- all privileged actions must be authenticated
- all significant changes should create audit records
- future policy-based restrictions should fit into the same model