# Daily-Task-Reminder-Automation-with-n8n

## 📌 Workflow: Daily Task Reminder (n8n Automation)

This workflow automates the process of sending **daily task reminders via email** using **Google Sheets** and **Gmail** inside [n8n](https://n8n.io/).

### ⚙️ How It Works

1. **Interval Trigger**

   * Runs the workflow automatically at a set interval (e.g., every few minutes or hours).

2. **Google Sheets Node**

   * Reads tasks from a Google Sheet (columns: `Task`, `Status`, `Due Date`).
   * Sheet ID: `1rmkItFRGWjEYio4feXBI6DB81g5QirDMGnBRzX0Rv94`
   * Range: `A:C`

3. **Format Tasks (Function Node)**

   * Formats the tasks into a readable email body:

     ```
     • Task Name (Status: In Progress, Due: 2025-08-30)
     • Another Task (Status: Completed, Due: 2025-08-31)
     ```

4. **Send Email (Gmail Node)**

   * Sends the formatted task list to your Gmail inbox.
   * Subject: `Task for the DAY!`
   * Message:

     ```
     Hi! Here are your tasks for the day:

     [formatted task list]
     ```

### 🛠 Requirements

* **n8n** installed and running
* A connected **Google Sheets account** (OAuth2)
* A connected **Gmail account** (OAuth2)

### 🚀 Use Case

* Automatically receive a daily digest of tasks from Google Sheets in your inbox.
* Perfect for personal productivity or small team task tracking.
