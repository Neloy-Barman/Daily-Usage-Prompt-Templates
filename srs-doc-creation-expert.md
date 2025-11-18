# Software Requirements Specification Creation from project descriptions Prompt 

``````md
## CONTEXT
I want '<context>'. I have collected different overviews for the same project. There are some common functionalities in between them but some lack requirements or processes mentioned in others. I want each and every feature mentioned in different data and merge them all into a common `Software Requirements Specification` document. The document should contain all the details in depth that a developer should follow from starting till the delivery phase of the project. 

## PROJECT DESCRIPTION DATA
```md
<description_1>
```
```md
<description_2>
```

## TASK
You need to approach the provided project details step by step internally, understand and analyze the client needs, extract the features from all resources. Finally, generate a `SRS` document and return the content in `.md` file formation.

## RULES
- Add the following sections while generating the `SRS` documentation.
    - Project Title
    - Project Overview
    - Problem Statement
    - Tech stacks/ Tools to be used
    - Core Workflow 
    - Deliverables
- When descriptions conflict or overlap, prioritize the most detailed version and consolidate similar features.
- The `Title` of the project should be `Professional`, `Appealing`, `Eye-catching` and memorable while reflecting the project's core purpose.
- The `Project Overview` should contain a summarized version of the whole project that gives a clear understanding within a short time.
- The `Problem Statement` should have the following characteristics: - 
    - The Problem
    - How this solution solves the problem.
    - Why someone should consider using the project.
- Break down the `Core Workflow` into logical development phases such as Requirements, Design, Implementation, Testing, and Deployment.
- Describe each `Phase` of the workflow thoroughly. 
- Organize the content into logical sections and key concepts.
- Provide comprehensive but focused details covering all functional and non-functional requirements to make the `Development` phase easier for the `Developer`.
- Formatting:
    - Use Markdown headings, bold text, and lists where helpful.
    - In bullet/numbered lists only, make labels before the colon bold (e.g., **Environment:** Production).
- Writing style:
    - Sentences should be short, concise, easy, clean, and in a professional tone.
    - Be comprehensive yet concise; avoid repetition.
- In `Tech Stack / Tools`, prefer technologies mentioned in the provided descriptions. If you propose alternatives, mark them as **Recommendations** and justify briefly.
- Provide a clear understanding of the `Deliverables` to the client.
- Mention the specific list of items/artifacts/files to be `Delivered`. 
- Return me with the whole response as a `Markdown` within **4 Backticks**(````<generated_markdown_content>````).
- Strictly keep the generated content within **4 Backticks**.

## EXAMPLE
Use the example below for structure and level-of-detail only. Do not copy vendor names, tools, or constraints unless they are present in the provided descriptions.
```md
# AI-Powered Customer Feedback Automation

## Project Overview

This project automates Artisan Corner's customer feedback processing by replacing manual sorting with an intelligent AI-driven workflow. The solution uses n8n to connect Tally.so web forms with Hugging Face AI services for sentiment analysis and image recognition, Supabase for data storage, and Discord for team notifications. Key benefits include faster response times to urgent issues, reduced manual workload, consistent classification of all feedback, and valuable insights into customer sentiment trends through centralized data tracking.

---

## Problem Statement
Our current process is as follows:
1.  A customer fills out a web form with their name, email, a message, and an optional image upload (e.g., showing a damaged product).
2.  An email notification is sent to a general `support@artisancorner.example` inbox.
3.  A team member reads the email, manually determines if it's a positive review, a general question, or an urgent issue, and then forwards it to the correct department or adds it to a spreadsheet.

This manual process is slow, prone to error, and we are not effectively tracking sentiment or common issues over time.

---

## Tech Stack (Open to Alternatives if Justified)

To ensure this project is feasible and cost-effective, we want to use services with free tiers.

*   **Automation Platform:** **n8n** (You can use the free n8n Cloud tier or self-host).
*   **Web Form:** **Tally.so**. It's free, user-friendly, and has excellent webhook support. You will need to create the form yourself.
    *   *Fields:* Name (Text), Email (Email), Message (Text Area), Product Image (File Upload).
*   **Database:** **Supabase**. It provides a free PostgreSQL database which is perfect for our needs. You will need to design a simple table schema to store the submissions.
*   **AI Functionality (NLP & Image Recognition):** **Hugging Face Inference API**. It offers a generous free tier for accessing thousands of pre-trained models.
    *   *For NLP:* Use a popular `sentiment-analysis` model.
    *   *For Image Recognition:* Use an `object-detection` or `image-classification` model.
*   **Notifications:** **Discord**. It's free and easy to set up incoming webhooks for sending formatted messages to different channels.

---

## Core Workflow

We need an end-to-end n8n workflow that automates the entire process. Here is the step-by-step logic we envision:

1.  **Trigger: Web Form Submission**
    *   The workflow must start when a customer submits our "Customer Feedback Form". This form will send its data via a webhook.

2.  **AI Analysis (NLP) on the Message**
    *   The text from the customer's message should be sent to an AI service to perform two tasks:
        *   **Sentiment Analysis:** Determine if the message is `Positive`, `Negative`, or `Neutral`.
        *   **Keyword Extraction/Categorization:** Identify key topics like "shipping," "damage," "quality," "praise," or "question."

3.  **AI Analysis (Image Recognition) on the Uploaded Image**
    *   If a customer has uploaded an image, the workflow should send the image URL to an AI service to analyze its content.
    *   The primary goal is to identify if the image contains things like "broken pottery," "cracked wood," or "packaging," which would indicate a damaged product issue.

4.  **Data Consolidation & Storage**
    *   All the data—original form submission, sentiment score, text category, and image analysis tags—must be collected.
    *   This consolidated record should then be inserted as a new row into our database for future reporting and analysis.

5.  **Intelligent Routing (Decision Making)**
    *   Based on the AI analysis, the workflow needs to branch into different paths:
        *   **Path A (Urgent Issue):** If sentiment is `Negative` AND the image analysis detects "damage" or the text mentions "broken"/"damaged," send a high-priority, formatted notification to our internal `#support-urgent` channel.
        *   **Path B (Positive Feedback):** If sentiment is `Positive`, send a notification to our `#happy-customers` channel so the marketing team can see it.
        *   **Path C (General Inquiry):** For all other cases (e.g., `Neutral` sentiment, questions), send a standard notification to the `#general-inquiries` channel.

---

## Expected Deliverables
1.  A fully functional and tested n8n workflow JSON file.
2.  The SQL `CREATE TABLE` statement for the Supabase table schema you designed.
3.  Brief (1-2 page) documentation explaining:
    *   How to set up the credentials (API keys, webhook URLs).
    *   An overview of the workflow logic.
    *   The names of the Hugging Face models you used.
4.  A short screen recording (Loom or similar) demonstrating the workflow in action from form submission to Discord notification.
```

## RESPONSE RETURN FORMAT
````md
    <generated_markdown_content>
````
``````