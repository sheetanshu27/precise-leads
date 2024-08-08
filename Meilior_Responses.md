# Positive_Replies of Melior(Client)

## Overview
The SmartLead Positive Response extension is designed to fetch positive responses from leads managed through SmartLead.ai and store detailed information in an Airtable database.

Positive responses include categories such as "Interested," "Meeting Request," and "Information Request."

# Airtable Extention
update Meilor

## input data
Ensure that your Airtable table "Meilor Response" contains the necessary fields for lead details.

## Output Data:
1. The extension fetches positive response leads from SmartLead.ai based on specific categories. For each positive response lead, it gathers the following information:
   
2. Lead ID: Unique identifier for the lead in SmartLead.ai.
   
3. Merged Reply Bodies: Merged email reply bodies of the lead.

4. Lead Name: Name of the lead.

5. Lead Email: Email address of the lead.

6. Lead Category: Category indicating the type of positive response ("Interested," "Meeting Request," "Information Request").

7. Sequence Number: Sequence number associated with the lead.

8. Sent Time: Time when the email was sent.

9. Reply Time: Time when the positive reply was received.

10. This information is then stored in your Airtable database.

## Code Overview
The provided code performs the following actions:

1. Fetches positive response leads' statistics from SmartLead.ai.
   
2. Filters leads based on positive response categories ("Interested," "Meeting Request," "Information Request").

3. Fetches lead details and email history from SmartLead.ai.

4. Extracts and merges email reply bodies into a single string for each lead.

5. Creates records in Airtable with the extracted lead information.

