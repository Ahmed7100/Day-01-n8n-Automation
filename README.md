# Day 01 — Client Intake → Project Setup

**Problem:**  
Manual project setup takes ~30–45 minutes per new client.

**Solution:**  
Automates the entire client onboarding process:
1. Client submits intake form (Typeform/Google Forms)
2. n8n Webhook triggers workflow
3. Creates project in Asana or Monday.com
4. Generates Google Drive folder structure
5. Sends personalized welcome email with next steps
6. Logs project info in Google Sheets/Airtable
7. Optional: Notifies team in Slack

**Workflow Nodes (high-level no-code steps):**
- Webhook (Trigger from form submission)
- Set / Extract node (normalize fields)
- Conditional node (validate required fields)
- Asana/Monday project creation
- Standard task creation (template tasks)
- Google Drive folder creation
- Permissions/share setup
- Email node (personalized welcome)
- Logging node (Google Sheets / Airtable)
- Slack notify (optional)

**Project & Folder Naming Convention:**  
`{ClientName}_{ProjectName}_{YYYYMMDD}`  
Subfolders: `00_Admin`, `01_Assets`, `02_Work-in-Progress`, `03_Final`, `04_Revisions`, `05_Archive`

**Standard Task Template (Asana/Monday):**
1. Kickoff meeting — schedule (PM)
2. Gather assets (Designer)
3. Create initial concepts / wireframes (Designer)
4. Internal review (Team Lead)
5. Client review & feedback (PM)
6. Revisions & approval (Designer)
7. Final delivery & handoff (PM)
8. Invoice & sign-off (Finance)

**Welcome Email (example placeholders):**  
- `{{client_name}}`  
- `{{project_name}}`  
- `{{pm_name}}`  
- `{{drive_link}}`  
- `{{project_link}}`  
- `{{kickoff_link}}`

**Deliverables:**
- Exported `workflow.json`
- README (this file)
- Demo screenshots
- Sample welcome email

**How to Test:**
1. Submit Typeform/Google Form
2. Confirm project creation in Asana/Monday
3. Confirm folder creation in Drive
4. Confirm welcome email sent with correct links
5. Verify logging in Google Sheets/Airtable

![alt text](<Screenshot 2025-10-04 222653.png>)