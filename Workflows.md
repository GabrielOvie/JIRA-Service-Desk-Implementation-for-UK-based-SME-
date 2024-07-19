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

## 2. Hardware Request Workflow

![Hardware Request Workflow](images/hardware-request-workflow.png)

### Stages:
1. Requested
2. Under Review
3. Approved
4. On Order
5. Delivered
6. Closed

### Transitions:
- Requested → Under Review: IT reviews the request
- Under Review → Approved: Request is approved
- Under Review → Closed: Request is denied
- Approved → On Order: Hardware is ordered
- On Order → Delivered: Hardware arrives and is prepared
- Delivered → Closed: User confirms receipt

## 3. User Onboarding Workflow

![User Onboarding Workflow](images/user-onboarding-workflow.png)

### Stages:
1. New Hire Reported
2. Account Creation
3. Hardware Preparation
4. Software Setup
5. Access Granted
6. Completed

### Transitions:
- New Hire Reported → Account Creation: HR provides necessary details
- Account Creation → Hardware Preparation: Accounts created, moving to hardware
- Hardware Preparation → Software Setup: Hardware ready, installing software
- Software Setup → Access Granted: Software installed, granting system access
- Access Granted → Completed: All tasks finished, ready for new hire

## 3. Auto-Categorize Hardware Requests

**Trigger:** Issue Created
**Conditions:** 
- Project is "IT Support"
- Issue Type is "Hardware Request"
- Summary or description contains keywords (e.g., "laptop", "monitor", "keyboard")
**Actions:** 
- Set Component based on detected keywords
- Add label "hardware-request"

## 4. Escalate Overdue High-Priority Issues

**Trigger:** Scheduled - Daily at 9:00 AM
**Conditions:**
- Issue is unresolved
- Priority is High or higher
- Created date is more than 2 days ago
  
*Actions:*
- Increase priority by one level (if not already Highest)
- Add comment: "This high-priority issue has been open for over 2 days and has been escalated."
- Send email notification to IT manager

## 5. Auto-Resolve Inactive Issues

**Trigger:** Scheduled - Weekly
**Conditions:**
- Status is "Awaiting Information"
- Last updated more than 7 days ago
  
*Actions:*
- Transition issue to "Resolved"
- Add comment: "This issue has been automatically resolved due to inactivity. Please reopen if the problem persists."
- Send email notification to the reporter

## 6. New Hire Onboarding Checklist

**Trigger:** Issue Created
**Conditions:**
- Project is "User Onboarding"
- Issue Type is "New Hire"
**Actions:**
- Create subtasks for each onboarding step (e.g., "Create Email Account", "Prepare Workstation", "Schedule Orientation")
- Assign subtasks to appropriate team members
- Set due dates for each subtask relative to the start date
