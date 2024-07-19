# JIRA Service Desk Automation Rules

This document lists the automation rules implemented in our JIRA Service Desk.

## 1. Auto-assign Priority Based on Keywords

**Trigger:** Issue Created
**Conditions:** 
- Summary or description contains words like "urgent", "critical", "ASAP"
**Actions:** 
- Set priority to High
- Add comment: "Priority automatically set to High based on ticket content."

## 2. SLA Breach Notification

**Trigger:** SLA time remaining is 1 hour
**Conditions:**
- Issue is unresolved
**Actions:**
- Send email to support team lead
- Add comment: "SLA breach imminent. Please prioritize this ticket."

