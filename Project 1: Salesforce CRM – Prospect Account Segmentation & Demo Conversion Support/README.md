# Project 2: Salesforce CRM – Prospect Account Segmentation & Demo Conversion Support

## Objective:
To segment prospect accounts by industry and engagement potential, helping sales teams prioritize outreach and increase demo conversions.

---

##  Tools Used:
- **Salesforce CRM**: Primary platform for managing account data and customizations.
- **LinkedIn Sales Navigator**: Used to gather verified account data such as company size, revenue, etc.
- **ZoomInfo**: Another tool for enriching account-level data.
- **Microsoft Excel**: Used for initial data analysis and planning.
- **Salesforce Reports & List Views**: For segmentation and reporting purposes.

---

##  Steps Taken:

### 1. Account Segmentation Strategy
- **Objective**: To segment prospect accounts into tiers based on certain factors like industry, company size, and engagement potential.
- **Data Analyzed**: Historical data of high-converting accounts.
- **Segmentation Criteria**:
  - **Company size**: Large, medium, small
  - **Industry relevance**: Based on target market
  - **Engagement history**: Prior interactions, emails opened, calls made
  - **Demo interest level**: Indications of interest in product demos.

- **Account Tiers**:
  - **Tier A (High Priority)**: High industry relevance, large companies, strong engagement history, high demo interest.
  - **Tier B (Medium Priority)**: Medium relevance and size, moderate engagement and demo interest.
  - **Tier C (Low Priority)**: Low engagement and demo interest, smaller companies.

---

### 2. Salesforce Customization

- **Custom Fields**: Created fields in the **Account Object** to capture segmentation data.
  - **Industry Category**: A picklist field to categorize accounts based on their industry.
  - **Engagement Score**: A calculated field to determine account engagement.
  - **Tier Ranking (A, B, C)**: Formula field to categorize accounts into one of the three tiers (A, B, C).

- **Formula for Engagement Score**:  
  The **Engagement Score** was calculated based on prior activities (e.g., emails opened, calls made, demo requests).  
  Formula:
  ```plaintext
  CASE(
    WHEN (LastActivityDate >= TODAY() - 30, 10, 0),
    WHEN (EmailsOpened > 5, 5, 0),
    WHEN (CallsMade > 10, 5, 0),
    ELSE 0
  )

 This formula awards points based on activities in the past 30 days.

### Tier Ranking Formula: Formula to categorize into Tier A, B, or C based on engagement score:

CASE(
  WHEN Engagement_Score__c > 15, 'A',
  WHEN Engagement_Score__c > 10, 'B',
  'C'
)

### 3. Integration with Prospecting Tools
Data Pull from LinkedIn Sales Navigator:

Gathered account-level information such as revenue, employee count, HQ location, and industry.

Used ZoomInfo to validate the account data.

### Updating Salesforce:

Enriched Salesforce records with the insights gathered from LinkedIn Sales Navigator and ZoomInfo.

Updated custom fields with company size, revenue, industry, and engagement data.

### 4. Demo Conversion Support
"High Potential Accounts" List View:

Created a Salesforce List View to highlight accounts with the highest engagement and tier ranking. This view automatically filtered and displayed Tier A accounts.

Sales Team Collaboration:

Regularly shared segmented lists with Business Development Representatives and Sales Reps.

Flagged accounts ready for demos and moved them swiftly through the sales funnel.

### 5. Training and Enablement
Weekly Syncs with Sales Team:

Conducted training sessions to demonstrate how to filter and prioritize leads using Salesforce views.

Shared best practices on how to approach different tiers of accounts.

### Outcome:
Improved Demo Conversion Rate: Increased conversion from outreach to demos by 20%.

Time Savings for Sales Reps: Reduced prospecting time by 25% due to clear account segmentation.

Sales Team Feedback: Sales reps rated the segmented lists as "highly actionable" for targeting high-potential prospects.

Streamlined Lead-to-Sales Process: Empowered the sales team to focus on high-value accounts and reduced manual filtering of leads.

### Conclusion:
This project successfully created a scalable system for prospect segmentation in Salesforce, helping the Sales team prioritize accounts based on engagement and potential. It enhanced collaboration between lead generation and sales conversion, leading to a more efficient process and improved results.

### Additional Notes:
The formula fields used to calculate Engagement Score and Tier Ranking can be adjusted as needed based on changes in sales strategy or customer behavior.

The segmented lists can be modified to include more complex criteria, such as geographic location or account-specific preferences, for further refinement.
