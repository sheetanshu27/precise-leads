# Waterfall Enrichment Extension

The Waterfall Enrichment extension is designed to enrich lead emails by utilizing multiple tools such as LeadMagic, UseArtemis, Tomba, and BounceBan,nimbler. It follows a waterfall approach where if one tool fails to find the email, the next tool in line is used until the email is successfully retrieved. The retrieved email is then validated using BounceBan to determine its validity.

## Features

- **Email Enrichment:** The extension enriches lead emails using LeadMagic, UseArtemis, and Tomba APIs.
- **Fallback Mechanism:** If one tool fails to find the email, the extension automatically switches to the next available tool until the email is found.
- **Email Validation:** After retrieving the email, BounceBan is used to validate its deliverability and ensure it is a valid email address.

## Workflow

The workflow of the Waterfall Enrichment extension follows these steps:

1. **Input Data:** Receive input data such as lead's first name, last name, and company domain.
2. **Tool Selection:**
   - Try LeadMagic API first to find the email based on the provided information.
   - If LeadMagic does not return a valid email, switch to UseArtemis to attempt email retrieval.
   - If UseArtemis also fails, use Tomba as a fallback option to find the email.
     If UseArtemis also fails, use nimbler as a fallback option to find the email.
3. **Email Validation:** Once an email is successfully retrieved,reeon,Leadmagic BounceBan API is used to validate the email's deliverability and check if it's a valid email address.



## Code Explanation

The Waterfall Enrichment extension script (`waterfall-enrichment.js`) performs the following steps:

1. **Retrieve Records:** Fetch records from the specified table (`Waterfall Enrichment`) using the `selectRecordsAsync` method.

2. **API Key Setup:**
   - `emailValidationApiKey`: API key for email validation using BounceBan.

3. **Enrichment Workflow:**
   - Iterate through each record to extract necessary data such as email, website, first name, and last name.
   - Use LeadMagic API (`https://api.leadmagic.io/email-finder`) to find emails based on first name, last name, and company domain.
   -If LeadMagic does not return a valid email, fallback to UseArtemis API (`https://api.useartemis.co/enrich/email`).
    If UseArtemis also fails, use Tomba API (`https://api.tomba.io/v1/email-finder`) .
    If tomba also fails, use nimbler API (`'https://api.mysalesapplication.com/api/v1/contacts/search'`) as a final fallback option.

4. **Email Validation:**
   - Validate retrieved emails using BounceBan API (`https://api.bounceban.com/v1/verify/single`) to determine deliverability.
   - Update the record in the table with the retrieved email and its validation status (`valid` or `invalid`).


