# **Workshop Plan: AI for Practical IT Data Analysis (Guided Follow-Along)**

**Objective:** To equip university IT staff with foundational AI prompting skills to automate data analysis and communication tasks through a hands-on, interactive session.

**Total Time:** 45 minutes + 30 minutes Q&A

**Tools for Demo:** ChatGPT-4 (or latest version with file analysis) / Copilot / University-provided AI

## **Materials Needed**

1.  **For the Facilitator:**
    *   Minimal presentation slides for the intro/outro.
    *   A prepared instance of the chosen AI tool.
    *   The sample `IT_support_tickets.csv` file.
    *   A text file with the exact prompts for easy copy-pasting.

2.  **For Participants (shared via a single link at the start):**
    *   The sample `IT_support_tickets.csv` file.
    *   A simple document (`workshop_prompts.txt`) with the key prompts.

---

## I. Introduction & Setup (Time: 5 Minutes)

*   **(1 min) Welcome & Framing:**
    *   **Facilitator Script:** "Good morning, everyone, and welcome. My name is Dr. Jie Tao, and I direct the AI & Tech Institute. Our goal today is simple: in the next 45 minutes, we're going to move past the hype and turn AI into a practical tool you can use today. We'll frame AI as a new colleague—a very fast, very capable junior analyst that thrives on clear instructions."

*   **(2 mins) The "Guided Follow-Along" & Materials:**
    *   **Facilitator Script:** "This is designed to be a **guided follow-along** session. I encourage you to open your favorite AI tool now—whether that's ChatGPT, Copilot, or the university's Clarity AI. We're going to work through a real-world problem together. To make it easy, I'm pasting a link in the chat. This link has the sample data file we'll use and a text file with the main prompts. Following along is optional, but it's the best way to learn, even if it's just to practice uploading a file. After this session, we'll email everyone a one-page guide with all the examples, including a bonus one."

*   **(2 mins) The Core Idea: Bad vs. Good Prompting:**
    *   **Facilitator Demo:** Quickly show a side-by-side comparison of a vague prompt (`Here is some ticket data. Tell me about it.`) and its messy output, versus a clear, structured prompt (`Act as an IT analyst. Profile the attached IT ticket data, identify the top 3 issue categories, and present your findings in a table.`) and its clean output.
    *   **Facilitator Script:** "This is the core idea for today. The quality of your output is a direct result of the quality of your input. Let's learn how to do that together."

---

## II. The Core Demo: A Guided Follow-Along (Time: 35 Minutes)

### **Part 1: Making Sense of the Mess (10 mins)**

*   **Facilitator Script:** "Okay, let's dive into our main scenario. Imagine you've been given a raw data export of IT support tickets. For everyone following along, this is your chance to try it in your own tool. Find the 'attach' or 'upload' button and select the `IT_support_tickets.csv` file."
*   **Action:** Upload the CSV file.
*   **Prompt 1 (Discovery):**
    ```
    Act as a senior IT analyst. Profile the attached spreadsheet named 'IT_support_tickets.csv'. Your task is to:
    1.  Identify all column headers and infer the data type for each.
    2.  Analyze the 'Description' column to identify and list the top 3 most common themes or issues mentioned by users.
    3.  Present this entire analysis as a concise, well-formatted summary.
    ```
*   **Facilitator Script:** "In seconds, we get a full profile of the file and a thematic analysis of unstructured text—something that's very hard to do with traditional tools."
*   **INTERACTION POINT (1 min):**
    *   **Facilitator Script:** "As you see, the AI identified three themes. **In the chat, what is one other question you could ask the AI right now to better understand this raw data?** Let's see some ideas."

### **Part 2: Precise Triage with Structured Prompting (15 mins)**

*   **Facilitator Script:** "Now let's find the most urgent problems using a framework called **R.A.F.T. - Role, Audience, Format, and Task**. Giving the AI these constraints is the key to getting reliable results. Let's build a prompt together."
*   **Prompt 2 (R.A.F.T. Extraction):**
    ```
    Excellent. Now, for your next task:
    - Your **Role** is an IT Service Desk Manager.
    - Your **Audience** is me, the Director of IT, who needs a clear, no-fluff view.
    - I need the output in a clean table **Format**.
    - Your **Task** is to extract all tickets that meet ALL criteria: Priority is 'High' OR 'Critical', Status is 'Open', AND Category is 'Network'.
    ```
*   **INTERACTION POINT (2 mins):**
    *   **Facilitator Script:** "We just used the **Format** 'Table'. This is incredibly useful, but it's not our only option. **In the chat, what are two other formats we could have requested for this exact same data?** Think about different uses." (e.g., JSON, a bulleted list, CSV).
*   **Marketing Weave-in Script:** "This R.A.F.T. technique is something we dive much deeper into during our full-day 'AI for Data Professionals' workshop at the Institute."

### **Part 3: From Data to Decision (10 mins)**

*   **Facilitator Script:** "This table is great, but it's still just data. The real value is turning data into a decision. We'll do this by continuing the conversation with the AI."
*   **Prompt 3 (Refinement & Calculation):**
    ```
    That's the exact data I needed. Now, please add a new column to that table called 'Days_Open' and calculate how many days each ticket has been open based on today's date, which is November 18, 2025.
    ```
*   **Prompt 3 (Optimized):**
    ```
    This is perfect. Now, please re-display the entire table of open, high-priority network tickets from your previous response. For each ticket, calculate the number of days it has been open, using November 18, 2025 as today's date. Place this new 'Days_Open' column immediately after the 'Status' column for better visibility.
    ```
*   **Facilitator Script:** "Perfect. Now for the final leap: from analysis to a strategic communication."
*   **Prompt 4 (Transformation & Communication):**
    ```
    Use this final table to draft a non-technical email memo to the CIO. The memo should:
    1.  Summarize that we have a significant number of critical, open network-related tickets.
    2.  Mention the average number of days these tickets have been open.
    3.  Recommend forming a priority task force to investigate the root cause.
    4.  The tone should be professional, data-driven, and solution-oriented.
    ```
*   **INTERACTION POINT (2 mins):**
*   **Facilitator Script:** "This email is for the CIO. But what if the audience was the IT team itself? **In the chat, what is one specific change you would ask the AI to make to the email's tone or content for an internal team audience?**"

### **Part 4: Review and Follow Up (if time allows):**
* **Self Review** Prompt:
   ```
   Act as a senior IT Service Desk Manager, review above draft for the email memo and suggest areas for improvement.
   ```
* **Follow Up** Prompt
   ```
   Act as the Chief Information Officer, review the draft of the updated email memo and:
   1. Specify whether you will or will not support this recommendation.
   2. Help me (as the IT Service Desk Manager) prepare for a follow up meeting.
   ```

---

## III. Wrap-up & Next Steps (Time: 5 Minutes)

*   **(2 mins) Recap Key Takeaways:**
    *   **Facilitator Script:** "So let's recap the two key skills we practiced today: 1) Using a structured framework like R.A.F.T. to give clear instructions, and 2) Using a conversational, iterative approach to refine and transform the AI's output. This is how you turn the AI into a true work partner."

*   **(3 mins) Call to Action & Transition to Q&A:**
    *   **Facilitator Script:** "If you found this hands-on approach useful, the ideal next step is our upcoming workshop, 'Advanced AI for IT Automation,' which will be held in the spring. We'll be sending the registration link and the one-page prompt guide from today's session in a follow-up email."
    *   **Facilitator Script:** "Thank you for your time and your fantastic interaction. We now have 30 minutes for Q&A. Feel free to ask about the demo or any other questions you have about using AI in your work."
