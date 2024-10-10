## Exercise 10: Email Automation - Send Email (UI Path)

### Aim:
To create an automation that sends an email from a Gmail account using UI Path.

### Equipment Required:
1. A computer with Windows OS.
2. UI Path Studio installed.
3. An active Gmail account.
4. Internet access.

### Theory:
Email automation involves sending emails programmatically using automation tools like UI Path. The **Send SMTP Mail Message** activity in UI Path can be used to send emails through an SMTP server (like Gmail). To send emails using Gmail, you need to configure SMTP settings and ensure that less secure apps are allowed in your Gmail account settings (or use OAuth2 for enhanced security).

**Key UI Path Activities**:
- **Send SMTP Mail Message**: This activity allows you to send an email through an SMTP server.

### Procedure:

>#### 1. **Open UI Path and Create a New Project**
#### Step 1: Open UI Path Studio
- Launch UI Path Studio and create a new project (e.g., "EmailAutomation").

>#### 2. **Set Up Variables**
#### Step 2: Define Variables
- Define the following variables:
  - `smtpServer` (String): SMTP server for Gmail (e.g., `"smtp.gmail.com"`).
  - `port` (Int32): Port number for Gmail (usually `587` for TLS).
  - `emailFrom` (String): Your Gmail address (e.g., `"your_email@gmail.com"`).
  - `emailTo` (String): Recipient's email address (e.g., `"recipient@example.com"`).
  - `emailSubject` (String): Subject of the email (e.g., `"Test Email from UiPath"`).
  - `emailBody` (String): Body of the email (e.g., `"This is a test email sent from UiPath automation."`).
  - `password` (String): Your Gmail password or App Password if 2FA is enabled.

>#### 3. **Send Email**
#### Step 3: Use the Send SMTP Mail Message Activity
- Drag and drop the **Send SMTP Mail Message** activity into the workflow.
- Configure the properties:
  - **SMTP Server**: Set to `smtpServer`.
  - **Port**: Set to `port`.
  - **Email From**: Set to `emailFrom`.
  - **Email To**: Set to `emailTo`.
  - **Subject**: Set to `emailSubject`.
  - **Body**: Set to `emailBody`.
  - **User**: Set to `emailFrom`.
  - **Password**: Set to `password`.
  - **Enable SSL**: Check this option to ensure secure sending.

>#### 4. **Save and Run the Workflow**
#### Step 4: Save the Workflow
- Save the workflow by clicking the save icon or pressing `Ctrl + S`.

#### Step 5: Run the Automation
- Run the automation to send the email from your Gmail account to the specified recipient.

### Output:
1. **Email Sent**: An email will be sent to the recipient's email address with the specified subject and body.

### Result:
The automation successfully sends an email from a Gmail account using UI Path, demonstrating the use of the **Send SMTP Mail Message** activity for email automation.
