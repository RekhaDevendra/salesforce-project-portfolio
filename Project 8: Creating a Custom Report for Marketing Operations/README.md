# Salesforce Project 8: Custom Report for Marketing Operations

## Objective  
Design and build a Salesforce custom report that empowers the Marketing Operations team to monitor lead generation, campaign ROI, and conversion metrics. This report provides actionable insights that streamline outreach strategies and improve performance tracking.

---

## Tools & Features Used  
- Salesforce Lightning Report Builder  
- Custom Report Types  
- Filters and Groupings  
- Summary Fields and Charts  
- Report Folders & Sharing  
- Scheduled Report Delivery  

---

## Steps Taken  

### 1. Stakeholder Requirement Gathering  
Collaborated with Marketing Ops to define key KPIs:
- Leads by Source  
- Conversion Rates  
- Campaign Performance  
- Region-wise Lead Trends  

### 2. Created Custom Fields  
Added necessary fields for segmentation:
- `Lead Source Category` (Picklist)  
- `Marketing Region` (Text)  
- `Campaign Cost` (Currency)

### 3. Built a Custom Report Type  
- **Primary Object**: Leads  
- **Related Object**: Campaigns  
- Deployed for full access to connected data

### 4. Report Development  
- Used grouping by `Marketing Region` and `Lead Source`  
- Summarized by Count and Conversion Rate  
- Filtered on:
  - Created Date: Last 30 Days  
  - Status: Open, Converted  
- Added charts:
  - Bar chart: Leads by Campaign  
  - Pie chart: Lead Source Breakdown  
  - Line chart: Monthly Conversion Trend

### 5. Report Sharing and Scheduling  
- Saved under: `/Marketing Reports/Monthly Analysis`  
- Shared with: Marketing Role & Team Leads  
- Scheduled for weekly Monday delivery

---

## Outcome  
- 25% faster insight retrieval for Marketing Ops  
- 100% adoption of report among campaign strategists  
- Supported improved segmentation and campaign ROI tracking  

---

## Role: Salesforce Administrator  
In this project, I enabled the Marketing team to become more data-driven by configuring reports, custom fields, and automation, demonstrating:

- Custom Report Building  
- User-Centric Design Thinking  
- Real-Time Insight Delivery  
