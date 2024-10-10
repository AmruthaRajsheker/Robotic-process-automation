## **Exercise 8: Basic Web Automation - Fill a Web Form (UI Path)**

### Aim:
To create an automation that fills a simple web form with user data and submits it using UI Path.

### Equipment Required:
1. A computer with Windows OS.
2. UI Path Studio installed.
3. Internet access to access the web form.
4. A web browser (e.g., Chrome, Firefox).

### Theory:
Web automation involves programmatically interacting with web applications to perform tasks such as filling out forms, clicking buttons, and submitting data. UI Path provides various activities to automate these interactions with web pages.

**Key UI Path Activities**:
- **Open Browser**: This activity opens a specified web page in a browser.
- **Type Into**: This activity simulates typing text into input fields.
- **Click**: This activity simulates a mouse click on buttons or links.
- **Set Web Attribute**: This can be used to set values for specific attributes of web elements.

### Procedure:

>#### 1. **Open UI Path and Create a New Project**
#### Step 1: Open UI Path Studio
- Launch UI Path Studio and create a new project (e.g., "WebFormAutomation").

>#### 2. **Set Up Variables**
#### Step 2: Define Variables
- Define the following variables to hold user data:
  - `userName` (String): User's name (e.g., `"John Doe"`).
  - `userEmail` (String): User's email (e.g., `"johndoe@example.com"`).
  - `userMessage` (String): User's message (e.g., `"Hello, I would like to know more about your services."`).

>#### 3. **Open the Web Form**
#### Step 3: Use the Open Browser Activity
- Use the **Open Browser** activity to navigate to the URL of the web form (e.g., `https://example.com/contact`).
- Choose the browser type (e.g., Chrome) in the Properties panel.

>#### 4. **Fill the Web Form**
#### Step 4: Use Type Into Activity
- Inside the **Do** section of the **Open Browser** activity:
  - Use the **Type Into** activity to fill the name field:
    - Set the **Selector** property to identify the name input field.
    - Set the **Text** property to `userName`.
  - Use another **Type Into** activity to fill the email field:
    - Set the **Selector** property to identify the email input field.
    - Set the **Text** property to `userEmail`.
  - Use another **Type Into** activity to fill the message field:
    - Set the **Selector** property to identify the message input field.
    - Set the **Text** property to `userMessage`.

>#### 5. **Submit the Form**
#### Step 5: Use the Click Activity
- After filling in the fields, add a **Click** activity to simulate clicking the submit button.
  - Set the **Selector** property to identify the submit button on the form.

>#### 6. **Save and Run the Workflow**
#### Step 6: Save the Workflow
- Save the workflow by clicking the save icon or pressing `Ctrl + S`.

#### Step 7: Run the Automation
- Run the automation to open the web form, fill it with user data, and submit the form.

### Output:
1. **Filled Form**: The web form will be filled with the specified user data.
2. **Form Submission**: The form will be submitted successfully, and the user will receive any confirmation displayed on the website.

### Result:
The automation successfully fills a simple web form with user data and submits it, demonstrating the use of **Open Browser**, **Type Into**, and **Click** activities in UI Path.
