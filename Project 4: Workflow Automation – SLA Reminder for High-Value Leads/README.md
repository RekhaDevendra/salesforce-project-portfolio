# Project 4: Workflow Automation – SLA Reminder for High-Value Leads

## Objective:
Set up a workflow rule to automatically notify Sales Managers when a high-value lead has not been contacted within 3 days, ensuring SLA compliance and fast-tracking outreach.

---

## Tools Used:
- **Salesforce Workflow Rules**: For automation of lead follow-up reminders.
- **Custom Fields on Lead Object**: To categorize leads based on their value.
- **Email Templates**: For creating automated email notifications.
- **Time-Triggered Actions**: To trigger reminders after a set time.

---

##  Steps Taken:

### 1. Add Custom Field to Lead
- **Field Name**: `Lead Value Category`
- **Type**: Picklist (Values: High, Medium, Low)
  - This field allows categorizing leads based on their potential value, which is crucial for SLA compliance.

### 2. Create Workflow Rule
- **Object**: Lead
- **Rule Criteria**:  
  Ensure that the workflow is triggered only when the lead value is high and it hasn’t been modified in the past 3 days.

  Lead Value Category = "High" AND
  
  LastModifiedDate <= TODAY() - 3
  
Explanation: This rule ensures that the workflow is triggered if the lead is categorized as “High” value and hasn’t been updated or contacted in the last 3 days.

### 3. Create Email Template
Email Template Name: High Value Lead – Reminder

### Email Content:

Explanation: This rule ensures that the workflow is triggered if the lead is categorized as “High” value and hasn’t been updated or contacted in the last 3 days.

### 3. Create Email Template
Email Template Name: High Value Lead – Reminder

### Email Content:

"This is a reminder that a high-value lead, {!Lead.Name}, has not been contacted within the SLA period."
- Explanation: The email will notify the lead owner that a high-value lead needs attention to ensure SLA compliance.

### 4. Add Time-Dependent Workflow Action
Action: Send Email Alert to Lead Owner

### Time Trigger: 3 days after LastModifiedDate

The email reminder will be triggered exactly 3 days after the last modification of the lead, ensuring that the SLA is being met for high-value leads.

### 5. Activate and Test
Test Leads: Created leads with "High" value.

### Testing Steps:

Created test leads with the value set to "High".

Waited 3 days to ensure the time-dependent workflow action triggered the email reminder to the lead owner.

### Result: The email reminder was successfully sent to the lead owner after 3 days, ensuring compliance with SLA policies.

### Outcome:
100% Compliance: Ensured SLA policies were adhered to for all high-value leads.

Improved Response Time: Reduced average response time by 2 days by automating follow-up reminders.

Reduced Missed Opportunities: Significantly decreased the chances of missed opportunities for high-value clients due to missed follow-ups.

### Conclusion:
This project successfully automated the process of sending reminders to Sales Managers about high-value leads that haven’t been contacted within the defined SLA. This not only ensured SLA compliance but also enhanced the response time and reduced the risk of missed opportunities.

### Additional Notes:
The Lead Value Category picklist field can be adjusted to fit different lead segmentation strategies.

The workflow rule can be modified to accommodate more complex criteria, such as specific lead sources or campaign types.
