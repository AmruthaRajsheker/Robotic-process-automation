## Exercise 9: Keyboard Automation - Simulate Keystrokes (UI Path)

### Aim:
To create an automation that simulates typing and keyboard shortcuts in a desktop application (Notepad) using UI Path.

### Equipment Required:
1. A computer with Windows OS.
2. UI Path Studio installed.
3. Notepad application installed on the computer.

### Theory:
Keyboard automation involves simulating keystrokes to interact with applications. UI Path provides activities to send keystrokes to applications, which can be useful for automating tasks in desktop environments.

**Key UI Path Activities**:
- **Start Process**: This activity launches an application (e.g., Notepad).
- **Type Into**: This activity simulates typing text into an active application.
- **Send Hotkey**: This activity simulates pressing keyboard shortcuts (e.g., Ctrl+C, Ctrl+V).

### Procedure:

>#### 1. **Open UI Path and Create a New Project**
#### Step 1: Open UI Path Studio
- Launch UI Path Studio and create a new project (e.g., "KeyboardAutomation").

>#### 2. **Open Notepad**
#### Step 2: Use the Start Process Activity
- Use the **Start Process** activity to launch Notepad.
  - Set the **FileName** property to `notepad.exe`.

>#### 3. **Simulate Typing**
#### Step 3: Use the Type Into Activity
- After the **Start Process** activity, add a **Type Into** activity to simulate typing.
  - Set the **Text** property to the text you want to type (e.g., `"Hello, this is a test of keyboard automation."`).
  - Ensure the **SimulateType** property is checked to simulate the keystrokes.

>#### 4. **Use Keyboard Shortcuts**
#### Step 4: Simulate Keyboard Shortcuts
- After typing the text, add a **Send Hotkey** activity to perform keyboard shortcuts.
  - To copy the text, set the **Key** property to `Ctrl + C`.
  - To paste the text in Notepad (after moving the cursor or opening a new file), add another **Send Hotkey** activity and set the **Key** property to `Ctrl + V`.

>#### 5. **Save and Run the Workflow**
#### Step 5: Save the Workflow
- Save the workflow by clicking the save icon or pressing `Ctrl + S`.

#### Step 6: Run the Automation
- Run the automation to launch Notepad, simulate typing the text, and perform the keyboard shortcuts.

### Main.Xaml

![image](https://github.com/user-attachments/assets/47750006-8553-45bb-9efa-832cffe975e8)

![image](https://github.com/user-attachments/assets/59a012e0-7421-41f3-ade1-3766d20fec1a)


### Output:
1. **Notepad Content**: The specified text will be typed into Notepad.
2. **Keyboard Shortcuts**: The text will be copied and pasted as specified by the keyboard shortcuts.


![image](https://github.com/user-attachments/assets/52ea3ec5-2b55-41dd-a0b6-3bdfa31590e7)


### Result:
The automation successfully simulates typing and keyboard shortcuts in Notepad, demonstrating the use of **Start Process**, **Type Into**, and **Send Hotkey** activities in UI Path.
