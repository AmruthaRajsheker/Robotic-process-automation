## Exercise 7: Read and Extract Text from PDF (UI Path)

### Aim:
To create an automation that extracts text from a PDF file and saves it to a text file using UI Path.

### Equipment Required:
1. A computer with Windows OS.
2. UI Path Studio installed.
3. A PDF file containing text to be extracted.

### Theory:
Extracting text from PDF files is a common automation task that can be accomplished using UI Path's PDF activities. UI Path provides a set of activities designed to handle PDF documents, allowing users to read and manipulate text data effectively.

**Key UI Path Activities**:
- **Read PDF Text**: This activity reads the text from a PDF file and stores it in a string variable.
- **Write Text File**: This activity writes the extracted text to a text file.

### Procedure:

>#### 1. **Open UI Path and Create a New Project**
#### Step 1: Open UI Path Studio
- Launch UI Path Studio and create a new project (e.g., "ExtractTextFromPDF").

>#### 2. **Set Up Variables**
#### Step 2: Define Variables
- Define the following variables:
  - `pdfFilePath` (String): Path of the PDF file to be read (e.g., `C:\path\to\your\file.pdf`).
  - `outputFilePath` (String): Path of the text file where the extracted text will be saved (e.g., `C:\path\to\your\output.txt`).
  - `extractedText` (String): To hold the text extracted from the PDF.

>#### 3. **Read Text from PDF**
#### Step 3: Use the Read PDF Text Activity
- Use the **Read PDF Text** activity and set the **FileName** property to `pdfFilePath`.
- Create an output variable for the activity and assign it to `extractedText`.

>#### 4. **Write Extracted Text to Text File**
#### Step 4: Use the Write Text File Activity
- After the **Read PDF Text** activity, add a **Write Text File** activity.
- In the **Properties** panel, set the **FileName** property to `outputFilePath`.
- Set the **Text** property to `extractedText` to save the extracted text to the specified text file.

>#### 5. **Save and Run the Workflow**
#### Step 5: Save the Workflow
- Save the workflow by clicking the save icon or pressing `Ctrl + S`.

#### Step 6: Run the Automation
- Run the automation to extract text from the PDF file and save it to the specified text file.

### Main.xaml
![image](https://github.com/user-attachments/assets/fa437259-8a68-4249-8a8a-5f976bb2d249)


### Output:
1. **Extracted Text**: The text content from the PDF file will be stored in the `extractedText` variable.

![image](https://github.com/user-attachments/assets/bb1d696c-7a28-4f1e-a848-6944d61b0c53)

   
2. **Text File**: The extracted text will be saved as a text file at the specified location.

![image](https://github.com/user-attachments/assets/542f6f3b-a25a-4175-a8f4-3bfa4a030d54)


### Result:
The automation successfully extracts text from a PDF file and saves it to a text file, demonstrating the use of **Read PDF Text** and **Write Text File** activities in UI Path.
