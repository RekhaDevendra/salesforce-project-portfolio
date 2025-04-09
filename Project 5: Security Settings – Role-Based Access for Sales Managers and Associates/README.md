# Project 3: Security Settings – Role-Based Access for Sales Managers and Associates

##  Objective:
Set up security rules ensuring different levels of data access based on role—so Sales Managers can edit all leads, but Sales Associates can only edit leads assigned to them.

---

##  Tools Used:
- **Profiles**: Used to define the level of access for different users.
- **Roles**: Used to establish a hierarchy of data access within the organization.
- **Organization-Wide Defaults (OWD)**: Configured to set the default access level for all records.
- **Sharing Rules**: Configured to allow access to records based on roles and criteria.
- **Permission Sets**: For additional access beyond profiles when needed.

---

##  Steps Taken:

### 1. Set Organization-Wide Defaults
- **Object**: Lead
- **Access Level**: **Private**
  - By setting the OWD for the Lead object to **Private**, only the record owner (and users with specific permissions) can view and edit their leads.

### 2. Create Roles
- **Sales Manager Role**: 
  - Can view and edit all leads in the system.
  - Inherits access to records owned by Sales Associates.
- **Sales Associate Role**: 
  - Can only view and edit leads assigned to them.

### 3. Assign Role Hierarchy
- **Manager > Associate**: 
  - Sales Managers will inherit access to all records owned by Sales Associates in the system, which is necessary for oversight and reporting.

### 4. Configure Profiles
- **Sales Manager Profile**: 
  - **Edit All Leads**: Provides the ability to view, edit, and delete all leads across the system.
  - **Access to Reports & Dashboards**: Ensures that Managers can access reporting and analytic tools to make informed decisions.
  
- **Sales Associate Profile**: 
  - **Read/Edit Own Leads Only**: Limits the Associate's ability to view and edit only the leads they are assigned to.
  - **View-Only Permissions for Accounts**: Sales Associates can view account details but cannot make changes to them.

### 5. Create Sharing Rules
- **Rule**: Share all leads owned by Sales Associates with their Managers.
  - Ensures that Sales Managers can always access and edit their associates’ leads for performance tracking, auditing, and support.

### 6. Test Scenarios
- **Test Users**: 
  - Created a **Sales Manager** user with full access to all leads.
  - Created a **Sales Associate** user with restricted access, limited to only their assigned leads.
  - **Verification**: Ensured that Sales Managers can view/edit all leads, while Sales Associates can only view/edit their own leads.

---

##  Outcome:
- **Data Confidentiality**: Ensured that sensitive lead data is only accessible to authorized users.
- **Prevention of Record Overwriting**: Minimized the risk of accidental data overwriting by restricting Sales Associates’ access to their own records only.
- **Improved Compliance**: Established strong internal controls and compliance by adhering to role-based access and data security best practices.

---

##  Additional Notes:
- The **Organization-Wide Defaults (OWD)** setting of **Private** ensures the security of lead data, making it essential for controlling data access within the company.
- **Role Hierarchy** ensures that managers have access to the records of those below them, enabling efficient oversight.
- **Sharing Rules** are critical for maintaining flexibility in data access while adhering to the principle of least privilege.

