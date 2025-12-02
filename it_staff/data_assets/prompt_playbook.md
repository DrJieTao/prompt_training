# The One-Page AI Prompt Playbook

This guide provides the core concepts and prompt examples from the "AI for Practical IT Data Analysis" workshop. Use these patterns to save time and get better, more consistent results from any modern AI tool.

## Core Concepts

*   **R.A.F.T. (Role, Audience, Format, Topic):** A framework to structure your prompts for clarity and precision. By telling the AI *who it is*, *who it's talking to*, *how to present the information*, and *what the subject is*, you dramatically improve the quality of its output.
*   **Iterative Refinement:** Treat AI as a conversation, not a search engine. The first answer is just the beginning. Ask follow-up questions to correct, change, calculate, or completely transform the previous response.

---

## Example 1: IT Ticketing Analysis (Workshop Demo)

**Scenario:** You have a raw spreadsheet of IT support tickets (`IT_support_tickets.csv`) and need to quickly understand the key issues, identify critical problems, and communicate your findings to leadership.

**Data Columns:** `Ticket_ID, Creation_Date, Status, Priority, Category, Assignee, User_Department, Description`

### Workflow Prompts:

**Prompt 1: Discovery & Thematic Analysis**
*   **Goal:** To get a high-level overview of an unfamiliar dataset and identify key themes in unstructured text.
```
Act as a senior IT analyst. Profile the attached spreadsheet named 'IT_support_tickets.csv'. Your task is to:
1.  Identify all column headers and infer the data type for each.
2.  Analyze the 'Description' column to identify and list the top 3 most common themes or issues mentioned by users.
3.  Present this entire analysis as a concise, well-formatted summary.
```

**Prompt 2: Precise Extraction with R.A.F.T.**
*   **Goal:** To filter the data for a specific, actionable subset of high-priority items.
```
Excellent. Now, for your next task:
- Your **Role** is an IT Service Desk Manager.
- Your **Audience** is me, the Director of IT.
- I need the output in a clean table **Format**.
- Your **Task** is to extract all tickets that meet ALL criteria: Priority is 'High' OR 'Critical', Status is 'Open', AND Category is 'Network'.
```

**Prompt 3: Refinement & Calculation**
*   **Goal:** To enrich the extracted data with a new calculation, making it more insightful.
```
This is perfect. 
Now, please re-display the entire table of open, high-priority network tickets from your previous response. 
For each ticket, calculate the number of days it has been open, using [TODAY'S DATE] as today's date. 
Place this new 'Days_Open' column immediately after the 'Status' column for better visibility.
```

**Prompt 4: Transformation & Communication**
*   **Goal:** To turn the final, analyzed data into a strategic, human-readable communication.
```
This is very insightful, thank you. Use this final table to draft a non-technical email memo to the CIO. 
The memo should:
1.  Summarize that we have a significant number of critical, open network-related tickets.
2.  Mention the average number of days these tickets have been open.
3.  Recommend forming a priority task force to investigate the root cause.
4.  The tone should be professional, data-driven, and solution-oriented.
```
---

## Example 2: Project Update Summary [Bonus]

**Scenario:** You have an export of tasks from a project management tool (`project_tasks.csv`) and need to quickly generate a status update for stakeholders.

**Data Columns:** `Task_ID, Task_Name, Assignee, Status, Due_Date, Blocker_Comment`

### Workflow Prompts:

**Prompt 1: Analysis & Summary**
*   **Goal:** To analyze structured project data and summarize it into key categories for a status report.
```
Act as a project manager. Your audience is the project steering committee. Analyze the attached 'project_tasks.csv' file and provide a summary in the following format:
- **Overall Progress:** A bulleted list showing the count of tasks by status (e.g., Not Started, In Progress, Completed).
- **Upcoming Deadlines:** A list of all tasks due in the next 7 days.
- **Critical Blockers:** A list of any tasks where the 'Blocker_Comment' field is not empty, including the task name and assignee.
```

**Prompt 2: Draft Communication**
*   **Goal:** To transform the summarized data into a professional stakeholder communication.
```
Based on that summary, draft a concise weekly project status update email to all stakeholders. 
The tone should be confident and clear. Include the key progress points and explicitly list the critical blockers and who is assigned to them, asking for their immediate attention.
```
