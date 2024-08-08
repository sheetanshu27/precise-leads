# Email Service Provider Finder(MX record)

Overview

This project provides a tool for identifying email service providers by querying MX (Mail Exchange) records for a given domain. It is designed to help with email validation and service provider identification efficiently.

# Features

MX Record Lookup: Retrieve MX records for a given domain.
Email Service Provider Identification: Determine the email service provider based on MX record data.
Enhanced Performance: Improved speed by processing 60 rows of data at a time.
Extended Provider List: Includes a comprehensive list of email service providers.

# Tools Used
Node.js: For running the script and performing network requests.
dns Module: To query MX records.

# Code workflow
 MXLookup Function:

Queries MX records for a domain.
Identifies the email service provider based on MX record data.
Returns "Google Apps" for Google domains, "Office 365" for Outlook domains, and "Other" for all others. Returns "ERROR" if the query fails.
getMXLookupResult Function:

Applies MXLookup to each domain in the input list.
Returns the list of email service providers for the domains.
getRawMXRecord Function:

Retrieves raw MX records for a domain.
Returns the raw MX record data or "ERROR" if the query fails.
processDomains Function:

Fetches domains from the 'Sheet222' sheet.
Processes domains in batches of 60.
Updates the 'ProcessedDomains' sheet with domains, email service providers, and raw MX records.
Sets a trigger to re-run the process if more domains need processing.
Deletes the trigger if all domains are processed.
clearAllTriggers Function (used within processDomains):

Deletes all triggers associated with the project.
