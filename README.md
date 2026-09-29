Auto Ticket Classification using ServiceNow Flow Designer

📌 Project Overview

This project automates the classification of IT support tickets using **ServiceNow Flow Designer**.

The system analyzes the ticket's **Short Description** and automatically assigns the appropriate **Category** and **Subcategory** based on predefined keywords. It also sends an email notification to the caller after the ticket is created.

🎯 Objectives

- Automatically classify IT support tickets.
- Reduce manual effort for IT agents.
- Improve ticket routing efficiency.
- Maintain structured and standardized ticket information.
- Implement a no-code and maintainable automation solution.

⚙️ Technologies Used

- ServiceNow
- Flow Designer
- Custom ServiceNow Table
- Update Sets
- Email Notifications

🔄 Project Workflow

1. Create an IT support ticket.
2. Flow Designer detects the newly created record.
3. The Short Description is analyzed for predefined keywords.
4. Category and Subcategory are automatically assigned.
5. An email notification is sent to the caller.
6. The result is validated through testing.

🗂️ Ticket Classification

| Keyword / Issue | Category | Subcategory |
|---|---|---|
| WiFi / Network | Network | Wi-Fi |
| Projector | Hardware | Projector |
| Password / Login | Access | Forgot Password |
| Slow / Hanging | Performance | Slow Computer |

🛠️ Main Components

Custom Table

A custom **Incident WorkFlow** table is used to store ticket records.

 Fields

- Number
- Caller
- Category
- Subcategory
- Short Description
- Description
- State
- Assigned Group
- Assigned to

 Category & Subcategory Dependency

The Subcategory options depend on the selected Category.

For example:

Network → Wi-Fi
Hardware → Projector  
Access → Forgot Password  
Performance → Slow Computer

🔁 Flow Designer Automation

The flow is named:

Auto Classify School IT Tickets

The flow is triggered when a new record is created and the Category is empty.

It then checks the Short Description and updates the Category and Subcategory according to the identified keyword.

After classification, an email notification is sent to the caller.

🧪 Testing

Test Case 1 — Wi-Fi Issue

**Short Description:**  
`WiFi not working in library`

Expected Result:
- Category → Network
- Subcategory → Wi-Fi
- Email notification → Sent

Test Case 2 — Projector Issue

Short Description:
`Projector not turning on`

Expected Result:
- Category → Hardware
- Subcategory → Projector
- Email notification → Sent

📦 Deployment

The completed ServiceNow Update Set was exported as an **XML file** for project deployment and sharing.

✅ Project Status

**Completed and tested in ServiceNow.**

👩‍💻 Project

**Auto Ticket Classification using ServiceNow Flow Designer**


