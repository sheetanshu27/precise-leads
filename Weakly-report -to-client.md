# Weakly report to client

## Overview
This project automates the generation of weekly reports, sends them to clients via email, and posts them to Slack. The workflow integrates Make, SmartLead.ai, Airtable, and other technologies to streamline reporting and communication.


## Code Explanation

campaign report extension script (`campaign report.js`) performs the following steps:

1. **Retrieve Records:** Fetch records from the specified table (`campaign report`) using the `selectRecordsAsync` method.

2. **API Key Setup:**
   - https://server.smartlead.ai/api/v1/campaigns?api_key=${API_KEY}

3. **report generation:**

   -geeting analytic using api--https://server.smartlead.ai/api/v1/campaigns 
   scrap data on the basis of campaign id

4. Database content--
         "Sent_Count":
          "Open_Count"
          "Click_Count"
          "Reply_Count"
          "Block_Count"
          "Total_Count"
          "Sequence_Count"
          "Drafted_Count"
          "Bounce_Count"
         

## Technologies and Tools Used
- SmartLead.ai: Provides lead data
- OpenAI: Utilized for summarizing.
- Slack: Sends notifications to designated channels for positive response leads.
- Airtable: Manages the lead database with detailed information and categories.
- Make: Provides the modules for OpenAi,Slack,Airtable,etc.


