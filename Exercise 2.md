# Exercise 2: Welcome Message in Message Box with IF Condition and Switch Case (UI Path)

## Aim:
To create an automation that takes the user’s name as input and displays different messages based on conditions, using both **IF** condition and **Switch Case** activity.

## Equipment Required:
1. Computer with Windows OS.
2. UI Path Studio installed.
3. Basic knowledge of UI Path workflow activities (Input Dialog, IF condition, and Switch Case).

## Theory:
UI Path provides powerful control flow structures such as **IF** and **Switch Case** to manage decision-making processes within automation workflows.

- **IF Activity**: This activity executes one block of code if a condition is true and another block if the condition is false.
- **Switch Case Activity**: Allows multiple branches of execution based on different values of a variable. It's an efficient way to handle multiple possible inputs.

In this exercise, we will use **Input Dialog** to get the name from the user, followed by displaying appropriate welcome messages using **IF** and **Switch Case**.

## Procedure:

1. **Open UI Path Studio**: 
   - Start UI Path Studio and create a new process (e.g., "WelcomeMessage").

2. **Create Workflow**:
   - Open the **Main.xaml** file in the Designer panel.

3. **Input Dialog for Name**:
   - In the **Activities** panel, search for "Input Dialog."
   - Drag and drop the **Input Dialog** activity onto the design canvas.
   - Set the **Label** to `"Please enter your name:"` and store the user's input in a variable called `userName`.

4. **IF Condition for Name Check**:
   - Drag an **IF** activity below the **Input Dialog**.
   - Set the condition to:  
     ```userName.Equals("RAM", StringComparison.OrdinalIgnoreCase)```
   - In the **Then** section, drag a **Message Box** activity and set the message to `"Welcome Mr. Ramachandran!"`.
   - In the **Else** section, drag another **Message Box** and set the message to `"Welcome " + userName + "!"`.

5. **Switch Case for Multiple Names**:
   - Add a **Switch** activity below the IF section.
   - Set the **Expression** to `userName.ToLower()`.
   - Add different **Cases** such as `"ram"`, `"john"`, `"alice"`, etc. 
   - For each case, use a **Message Box** to display personalized messages like:
     - Case "ram": `"Hello Ramachandran, welcome back!"`
     - Case "john": `"Welcome Mr. John!"`
     - Case "alice": `"Welcome Ms. Alice!"`
   - In the **Default** section, display a general message like `"Welcome " + userName + "!"`.

6. **Save and Run**:
   - Save the workflow and run it to test various inputs such as "RAM," "John," "Alice," and any other name.

## Output:
1. **For IF Condition**:
   - If the user inputs "RAM", it will display:  
     `"Welcome Mr. Ramachandran!"`.
   - For any other name, it will display:  
     `"Welcome <Given Name>!"`.
   
2. **For Switch Case**:
   - Depending on the input, the workflow will display different personalized welcome messages for predefined names (like Ram, John, Alice) and a default message for other names.

## Result:
The automation successfully displayed appropriate welcome messages based on the user's input using both IF condition and Switch case activities. This demonstrates conditional logic and branching in UI Path workflows.
