# Exercise 1 - Hello World: Display a Message Box 

## Aim:
To develop a simple automation script in UI Path that displays a "Hello World" message using a Message Box activity.

## Equipment Required:
1. A computer with Windows OS.
2. UI Path Studio installed.
3. Basic knowledge of UI Path Studio activities and workflow creation.

## Theory:
UI Path is an RPA (Robotic Process Automation) tool that allows automation of repetitive tasks. The Message Box activity in UI Path is used to display a pop-up dialog containing a message. This is one of the simplest ways to demonstrate UI Path's functionality. It helps in building user interfaces for automations that require interaction.

The **Message Box** activity halts the execution of the automation until the user closes the dialog box, making it a great tool for debugging and basic workflows.

## Procedure:
1. **Open UI Path Studio**: Launch UI Path Studio from your computer.
2. **Create a New Project**: 
   - Click on the 'New Project' button.
   - Select 'Process' from the list and name the project (e.g., "HelloWorld").
   - Click 'Create.'
3. **Create Workflow**: 
   - In the Designer panel, open the **Main.xaml** file.
   - In the Activities panel (left side), search for "Message Box."
   - Drag and drop the **Message Box** activity onto the workflow design canvas.
4. **Configure Message Box**: 
   - In the **Message Box** properties panel, set the **Message** field to `"Hello, World!"`.
   - This can be done by typing the string inside the quotes or setting it from a variable.
5. **Save the Workflow**: 
   - Save your workflow by clicking the save icon or pressing `Ctrl + S`.
6. **Run the Project**: 
   - Click on the 'Run' button in the ribbon at the top.
   - The Message Box with "Hello, World!" will appear.
   - After clicking 'OK,' the automation will end.

## Output:
- A pop-up message box displaying the text "Hello, World!".
- The automation successfully halts at the message box until the user clicks "OK."

## Result:
The "Hello, World!" automation script was successfully created in UI Path, demonstrating the use of the Message Box activity to display a message. This basic exercise serves as a foundation for building more complex UI Path workflows.

