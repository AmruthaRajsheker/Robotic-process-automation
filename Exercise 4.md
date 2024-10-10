# Exercise 4: Read and Write Excel Data (UI Path)



## Aim:
To create an automation that reads data from an Excel file and writes it to another Excel file using UI Path.



## Equipment Required:
1. A computer with Windows OS.
2. UI Path Studio installed.
3. An Excel file with sample data to read from.



## Theory:
Excel is commonly used in automation for data storage and manipulation. UI Path provides **Excel activities** that allow seamless interaction with Excel files for reading, writing, and processing data. 

- **Read Range Activity**: This activity reads the data from a specified range or worksheet in an Excel file and stores it in a data table.
- **Write Range Activity**: This activity writes data from a data table to an Excel file in a specified range or worksheet.



## Procedure:

>#### 1. **Reading Data from Excel**
#### Step 1: Open UI Path Studio
- Launch UI Path Studio and create a new project (e.g., "ReadWriteExcel").

#### Step 2: Set Up Excel Read Workflow
- Open **Main.xaml** and start by adding a **Sequence** activity.
- In the **Activities** panel, search for **Excel Application Scope**.
- Drag and drop the **Excel Application Scope** activity inside the sequence. 
- In the **WorkbookPath** field, provide the path to the Excel file (e.g., `C:\path\to\your\sourcefile.xlsx`).

#### Step 3: Read Excel Data
- Inside the **Excel Application Scope**, add a **Read Range** activity to read data from the Excel sheet.
- Specify the worksheet name (e.g., `"Sheet1"`) and leave the range as empty to read all data.
- Store the output in a **DataTable** variable (e.g., `inputDataTable`).



>#### 2. **Writing Data to Another Excel File**
#### Step 4: Set Up Excel Write Workflow
- Add another **Excel Application Scope** activity after reading the data.
- Provide the path for a new or existing Excel file where the data will be written (e.g., `C:\path\to\your\targetfile.xlsx`).

#### Step 5: Write Data to Excel
- Inside the **Excel Application Scope**, add a **Write Range** activity.
- Set the **DataTable** property to the variable containing the data read from the previous file (i.e., `inputDataTable`).
- Specify the worksheet name (e.g., `"Sheet1"`), and leave the starting cell as `"A1"`.



>#### 3. **Save and Run**
#### Step 6: Save the Workflow
- Save the workflow by clicking the save icon or pressing `Ctrl + S`.

#### Step 7: Run the Automation
- Run the automation to read data from the source Excel file and write it to the target Excel file.



## Output:
1. **Input Excel File**: The original Excel file's data is read and stored in the DataTable.
2. **Output Excel File**: A new or existing Excel file is populated with the data from the input Excel file.



## Result:
The automation successfully reads data from one Excel file and writes it to another, demonstrating data manipulation using **Read Range** and **Write Range** activities in UI Path.



Let me know if you'd like more details or clarifications on this assignment!
