# Email and Phone Finder from LeadMagic

Overview
This project provides tools for finding email addresses and phone numbers using LeadMagic. It includes two extensions designed to streamline and enhance the lead generation and contact discovery process.

# Features
Email Finder Extension: Extracts email addresses from LeadMagic data.
Phone Number Finder Extension: Extracts phone numbers from LeadMagic data.

# Extensions
Email Finder Extension:
Utilizes LeadMagic’s API to search for and extract email addresses from leads.

Phone Number Finder Extension:
Uses LeadMagic’s API to search for and extract phone numbers from leads.

# Tools Used
LeadMagic API: For extracting email addresses and phone numbers.
Node.js: For executing the scripts and processing data.
Google Sheets / Excel (if applicable): For storing and managing the extracted data.

# Work flow of Emali finder
Initialize: Set the API endpoint and key for LeadMagic.
Setup Sheet: Access the active Google Sheets and set column headers.
Retrieve Data: Get the data range from the sheet.
Iterate Rows: Loop through each row of data starting from the second row.
Fetch Email: Send a POST request to the LeadMagic API with the current row's data.
Handle Response: Check if the response status is 200 (OK); log and set an error if not.
Parse Data: Extract the email from the API response.
Update Sheet: Write the found email or an error message back to the sheet.
Log Results: Log any errors or the found email in the script's log.
Error Handling: Catch and log any exceptions that occur during the API request.