# Project 9: Set Up a Custom Field for Lead Segmentation

## Objective
Create a Custom Field to support lead segmentation for a targeted marketing campaign. Ensure it's usable in Lead records, Marketing Reports, and List Views, and seamlessly integrated with automation rules.

---

## Tools & Features Used
- Salesforce Setup
- Object Manager (Lead)
- Field-Level Security
- Page Layouts
- Custom List Views
- Marketing Campaign Reports and Dashboards
- Automation Setup (Optional: Workflow / Process Builder / Flow)

---

## Steps Taken

### 1. Business Need
To enable targeted follow-up campaigns based on how leads engaged with the company — such as webinars, e-books, or paid ads — a custom field was required.

### 2. Create Custom Field
- **Object**: Lead
- **Field Type**: Picklist
- **Field Name**: `Engagement Source Type`
- **Picklist Values**:
  - Webinar
  - E-Book
  - Social Media
  - Referral
  - Event Booth
  - Paid Ad
  - Other

- *Path*: `Setup → Object Manager → Lead → Fields & Relationships → New`

- Set field-level security to be visible for Sales & Marketing profiles
- Added to Lead page layout and compact layout

### 3. Update Page Layout
- Placed field on the Lead detail page for visibility
- Mapped it in Lead Conversion settings (if applicable)

### 4. Create List View
**View Name**: "Webinar Leads – Q2"

**Filters**:
- Engagement Source Type = Webinar
- Created Date = Last 90 Days

-- Used by Marketing Ops for campaign targeting

### 5. Build a Custom Report
- **Report Type**: Leads
- **Group By**: Engagement Source Type
- **Chart**: Bar Chart – Lead Volume by Source Type

### 6. Marketing Automation
Created a Flow to automatically add:
- Leads with `Engagement Source Type = Webinar`
- and `Lead Status = New`  
→ into a Salesforce Campaign named **"Webinar Follow-Up - Q2"**

---

## Outcome
- Improved segmentation & personalization
- Enabled campaign-specific automation
- Increased lead follow-up efficiency
- Enabled clear source attribution in reports

## Role: Salesforce Admin – Marketing Automation Focus
I implemented this field as part of a broader lead nurturing initiative, ensuring it supports reporting, campaign automation, and lead quality insights.

---
