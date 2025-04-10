# Project 7: Customer Feedback Form – Salesforce Web-to-Lead

## Objective:
Create a Customer Feedback Form using Salesforce’s Web-to-Lead feature. This form captures customer responses and automatically generates a Lead record in Salesforce CRM, helping businesses track feedback and follow up efficiently.

---

## Tools Used:
- Salesforce (Lightning or Classic)
- Web-to-Lead
- Custom Lead Fields
- HTML
- Email Templates (Auto-response)

---

## Steps Taken:

### 1. Enabled Web-to-Lead
- Navigated to Setup → Web-to-Lead → Enabled
- Set a default Lead Creator (used if no assignment rule matches).

Save the settings.
---

### 2. Create Custom Lead Fields for Feedback
- To store customer responses, add custom fields on the Lead object:
- Field 1: Feedback_Rating (Type: Picklist; Values: Excellent, Good, Average, Poor)
- Field 2: Feedback_Comments (Type: Long Text Area)
- Field 3: Product_Used (Type: Text or Picklist)

Setup → Object Manager → Lead → Fields & Relationships → New

---

### 3. Generated Web-to-Lead Form
Setup → Web-to-Lead → Create Web-to-Lead Form

- Included: Name, Email, Company, Feedback Fields
- Deploy the Form: Sample HTML provided in `feedback-form.html`
- Embedded in external webpage

---

When customers submit the form, a new Lead is created in Salesforce instantly.
### 4. Auto-Response Rule
- Created auto-reply email template to thank users
- Triggered upon submission for customer engagement

---

### 5. Tested Submission
- Submitted test feedback form
- Verified new Lead was created with correct field mapping
- Checked if email response was received

---

### 6. Outcome:
- Seamless data collection from external users
- Auto-creates Salesforce Leads with relevant data
- Improves response time and customer experience
- No manual data entry required

---

## Optional Enhancements:
- Add reCAPTCHA for spam protection
- Lead assignment rules based on feedback
- Dashboard for visualizing feedback trends

---

## Files:
- `feedback-form.html` – Working HTML form ready for deployment
- `README.md` – Full project documentation

---

## Role: Salesforce Administrator

Built this project to simulate real-world Salesforce Web-to-Lead integrations. Gained hands-on experience in:
- CRM automation
- Customization
- Lead data mapping
- Form deployment
