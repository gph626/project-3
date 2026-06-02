# Data Model Sketch

## Core Entities

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

## Key Fields

### users

- id
- name
- email
- roleId
- unitId
- active
- createdAt

### roles

- id
- name
- description

### units

- id
- name
- code

### cases

- id
- caseNumber
- title
- status
- priority
- assignedUnitId
- assignedUserId
- reviewerId
- dueDate
- summary
- createdAt
- updatedAt

### parties

- id
- caseId
- name
- type
- contactInfo

### tasks

- id
- caseId
- title
- ownerId
- status
- dueDate
- priority

### documents

- id
- caseId
- fileName
- documentType
- metadata
- visibility
- createdAt

### notes

- id
- caseId
- authorId
- body
- createdAt

### events

- id
- caseId
- eventType
- payload
- createdById
- createdAt

### auditEntries

- id
- caseId
- actorId
- action
- beforeValue
- afterValue
- createdAt

## Relationships

- one user belongs to one role
- one user belongs to one unit
- one case belongs to one unit
- one case belongs to one assigned user
- one case can have many parties, tasks, documents, notes, events, and audit entries

## Notes

- keep case status as a controlled enum
- use audit entries for all sensitive changes
- keep document metadata in MVP even if file uploads come later
- design IDs and timestamps consistently from the start