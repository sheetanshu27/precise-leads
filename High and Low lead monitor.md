# High Bounce and Low Leads 

Overview
This project focuses on monitoring high bounce rates and low lead counts using the Make platform, SmartLead, and Slack. The system is designed to automate the process of scraping lead details, performing analytics, and notifying relevant stakeholders when certain thresholds are exceeded.

# Tools Used

SmartLead: Used for scraping lead details via API.
Make: Platform for automating workflows and performing analytics.
Slack: For notifications regarding bounce rate and lead count issues.

# Workflow
Data Collection:
Scrape lead details from SmartLead using its API.

Analytics:

Perform necessary analytics on the scraped data to monitor bounce rates and lead counts.
Comparison and Notifications:

Compare the bounce count with a predefined threshold (e.g., >3%).
If the bounce count exceeds the threshold, pause the process and send a notification to Slack.

