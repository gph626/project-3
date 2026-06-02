# Phase 1: Project Definition

## Objective

Define the product clearly before any implementation starts. This phase locks down who the system is for, what problems it solves, what data it must store, and what rules govern access and workflow.

## Phase 1 Outcome

By the end of this phase, the project should have:

- a defined user base
- a bounded feature scope
- a case data model outline
- a role and permission matrix
- a deployment direction
- a clear MVP target

## Target Users

Primary users:

- case managers
- analysts
- attorneys or counsel
- supervisors or reviewers
- records clerks

Secondary users:

- administrators
- auditors
- read-only stakeholders

## Core Problem Statement

The system will replace fragmented case tracking across spreadsheets, email, and manual status updates with a structured case management platform that supports secure workflows and traceable actions.

## MVP Scope

The first version should include only the essentials needed to prove the system works.

### Must-Have

- secure login
- role-based access control
- dashboard with high-level metrics
- searchable case registry
- case detail page
- tasks and deadlines
- audit trail
- basic document metadata
- create, update, and close case flows

### Nice-to-Have Later

- file uploads
- advanced reporting
- saved views
- notifications
- approval workflows
- retention rules
- exports

## Case Data Fields

Each case should have a stable core record.

### Required Fields

- case number
- title or subject
- status
- priority
- assigned unit
- assigned user
- reviewer or judge
- created date
- updated date
- due date
- summary

### Optional Fields

- external reference number
- tags
- related cases
- statutory or program category
- risk level
- confidentiality flag

## Workflow States

The system should use predictable case states.

Recommended states:

- Draft
- Open
- In Review
- Pending Action
- Monitoring
- Closed
- Archived

## Role and Permission Matrix

### System Administrator

Can:

- manage users
- manage roles
- manage lookup values
- edit system settings
- view all cases

### Case Manager

Can:

- create cases
- edit assigned cases
- assign tasks
- update case status
- add notes
- view audit history

### Analyst

Can:

- view assigned cases
- update case notes
- create task updates
- add supporting metadata

### Attorney or Counsel

Can:

- review case details
- update legal or decision-related notes
- manage case status within assigned authority

### Supervisor or Reviewer

Can:

- view team cases
- approve or reject status changes
- assign ownership
- monitor workload

### Records Clerk

Can:

- attach document metadata
- classify records
- update retention-related fields
- view archival status

### Read-Only Stakeholder

Can:

- view assigned or permitted cases
- inspect dashboards and reports
- not modify records

## Data Entities

Core entities for the application:

- users
- roles
- units or offices
- cases
- parties
- tasks
- documents
- notes
- events
- audit entries

## Key Relationships

- one user can own many cases
- one case can have many parties
- one case can have many tasks
- one case can have many documents
- one case can have many audit entries
- one unit can manage many cases

## Security Rules

Phase 1 should establish these assumptions:

- users only see cases they are allowed to access
- all important edits are written to audit history
- privileged actions require authentication
- sensitive fields are protected by role
- the system should support future policy-based restrictions

## Deployment Direction

Recommended deployment path:

- Next.js app frontend and server layer
- PostgreSQL database
- Prisma or Drizzle for schema access
- Auth.js for authentication
- Tailwind CSS for UI

## Design Direction

The interface should feel:

- government-appropriate
- restrained and professional
- information-dense but readable
- responsive on laptop and desktop
- accessible by keyboard and screen reader

## Phase 1 Deliverables

At the end of this phase, create these artifacts:

- a finalized README
- the feature scope list
- a permission matrix
- a data model sketch
- a page inventory
- a milestone roadmap

## Phase 1 Decisions To Confirm

Before moving into implementation, confirm:

1. Which user role is the first primary operator?
2. Which case statuses are required in version 1?
3. Is document upload part of MVP or a later phase?
4. Do supervisors need approval workflows from day one?
5. Will the first release be internal-only or publicly deployable?

## Recommended Phase 1 Decision

For a strong capstone build, the best default choices are:

- primary operator: case manager
- MVP statuses: Draft, Open, In Review, Pending Action, Closed
- document upload: later phase, but document metadata in MVP
- approvals: not in MVP unless required by your use case
- deployment: internal-style demo first, production-ready structure from the start

## Next Step

Phase 1 is finalized through these repository artifacts:

- [Feature scope](FEATURE-SCOPE.md)
- [Permission matrix](PERMISSION-MATRIX.md)
- [Data model sketch](DATA-MODEL-SKETCH.md)
- [Page inventory](PAGE-INVENTORY.md)
- [Milestone roadmap](MILESTONE-ROADMAP.md)

After Phase 1 is finalized, move to Phase 2 and create the actual app shell with:

- dashboard
- case registry
- case detail view
- task list
- audit trail
