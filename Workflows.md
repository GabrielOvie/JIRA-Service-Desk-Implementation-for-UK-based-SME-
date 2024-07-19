# JIRA Service Desk Workflows

This document outlines the custom workflows created for our JIRA Service Desk implementation.

## 1. IT Support Workflow

![IT Support Workflow](images/it-support-workflow.png)

### Stages:
1. Open
2. In Progress
3. Awaiting Information
4. Resolved
5. Closed

### Transitions:
- Open → In Progress: Support agent picks up the ticket
- In Progress → Awaiting Information: More info needed from user
- Awaiting Information → In Progress: User provides information
- In Progress → Resolved: Issue is fixed
- Resolved → Closed: User confirms resolution
- Resolved → In Progress: Issue recurs or resolution unsatisfactory
- loop again

