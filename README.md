# Candidate Email Automation System

## About the Project

This project automates the initial candidate communication process using Python, Google Forms, Google Sheets, and Gmail SMTP. It monitors candidate registrations and sends application confirmation emails automatically.

## Features

- **Automated Monitoring:** Checks Google Sheets for new candidate registrations every 30 seconds.
- **Email Validation:** Validates candidate email addresses before sending emails.
- **Required Field Validation:** Checks that candidate names and job roles are provided.
- **Duplicate Detection:** Detects duplicate email addresses and skips duplicate confirmation emails.
- **Automated Emails:** Sends application confirmation emails to eligible candidates.
- **Status Tracking:** Updates each candidate's email status in Google Sheets.

## Technologies Used

- Python
- Jupyter Notebook
- Google Forms
- Google Sheets API
- Gmail SMTP
- `gspread`
- `google-auth`
- `python-dotenv`

## Project Workflow

1. A candidate submits the Google Form.
2. The candidate's information is saved in Google Sheets.
3. The Python notebook checks for new registrations.
4. Candidate details and email addresses are validated.
5. Duplicate email addresses are detected.
6. A confirmation email is sent to eligible candidates.
7. The email status is updated in Google Sheets.

## Project Structure

```text
Email-Automation/
├── Email_Automation_Agent.ipynb
├── requirements.txt
├── README.md
└── .gitignore
```

## Installation and Setup

1. Clone or download this repository.
2. Create and activate a Python virtual environment.
3. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```
4. Configure Google Sheets authentication and Gmail credentials securely.
5. Open `Email_Automation_Agent.ipynb` in Jupyter Notebook.
6. Run the notebook cells in order.

## Email Statuses

- `Sent` — Confirmation email was accepted by Gmail SMTP.
- `Failed` — Email sending failed.
- `Invalid Email` — The email address did not pass validation.
- `Duplicate Email` — The email address was identified as a duplicate.
- `Missing Details` — Required candidate information is missing.

## Security

- Never upload `.env`, `credentials.json`, or `token.json`.
- Never publish Gmail app passwords, API keys, or other secrets.
- Avoid publishing real candidate information or private spreadsheet data.

## Current Limitations

- The notebook must remain running to monitor new submissions.
- The project has not yet been deployed to a cloud platform.
- Duplicate detection skips duplicate emails but does not delete duplicate spreadsheet rows.

## Future Enhancements

- Add improved logging and retry handling.
- Improve duplicate prevention and reliability.
- Integrate the Gmail API.
- Deploy the automation to a cloud platform.
