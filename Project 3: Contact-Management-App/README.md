# Contact Management App – Client Outreach Database for HR Services Team

To build a Contact Management App in Salesforce to track client contact information and enable seamless outreach for HR Services and CSSR teams.
This project involves the creation of a Contact Management App on Salesforce, where users can create, update, view, and delete contact records. The app utilizes Salesforce's robust object-oriented database structure to manage and store customer data efficiently. This is a basic yet essential component of CRM (Customer Relationship Management) systems.

### Key Features:
- **Create, Read, Update, Delete (CRUD) Operations** on Contact records
- Track and manage customer interactions, sales leads, and opportunities
- Custom fields and page layouts to suit business requirements
- Reports and dashboards to monitor contact information and engagement

### Objective:
To build a Salesforce app that allows sales teams to manage customer contact information effectively. This helps ensure that critical customer data is organized and accessible for follow-ups, relationship management, and reporting.

### Steps Taken:
1. **Data Model Creation**:
   - Created a custom **Contact** object to store basic information such as:
     - First Name, Last Name, Email, Phone Number, and Address
     - Created custom fields based on business needs (e.g., 'Lead Status', 'Preferred Contact Method')
   
2. **Page Layouts**:
   - Designed intuitive page layouts to display relevant information
   - Assigned layouts based on user profiles to ensure relevant data is displayed for different roles (e.g., Sales Representative vs. Sales Manager)

3. **Record Types**:
   - Set up multiple record types based on business processes (e.g., ‘Prospects’, ‘Customers’)
   - Custom fields were tailored to each record type to capture information specific to each category.

4. **Workflow Rules**:
   - Created workflow rules to trigger automatic actions when certain conditions were met:
     - 1) Send an email notification to the sales team when a new contact is created
     - 2) Automatically update the ‘Lead Status’ field when the contact becomes a ‘Customer’

5. **Validation Rules**:
   - Implemented validation rules to ensure accurate data entry, such as preventing users from leaving the email field empty or ensuring phone numbers meet specific format requirements.

6. **Reports and Dashboards**:
   - Built custom reports to track key performance indicators (KPIs) such as the number of active contacts and their lead status
   - Created a dashboard for sales managers to visualize contact distribution, sales performance, and lead conversion rates

### Tools/Features Used:
- **Salesforce Object Model**: Custom objects and fields
- **Salesforce Flow**: Automating processes within the app
- **Workflow Rules & Alerts**: Automating email notifications and updates
- **Reports & Dashboards**: Visualizing data and KPIs

### How This Relates to My Real-Time Work:
This project directly mirrors my work experience at [Previous Company], where I worked on building and optimizing Salesforce systems for data management. Specifically:
- I utilized similar **data models** for managing sales leads and contact information.
- I automated processes, ensuring timely reminders and accurate information flow to the sales team.
- My experience with custom objects, workflow automation, and reporting allowed me to provide the necessary tools for efficient customer management.

### Conclusion:
The **Contact Management App** is an essential part of CRM operations, ensuring that sales teams can effectively manage contacts and track critical customer data. This project showcases my ability to build customized Salesforce solutions that align with real-world business needs, improving both efficiency and accuracy.
