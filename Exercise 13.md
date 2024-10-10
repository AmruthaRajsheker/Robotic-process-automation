## Exercise 13: Invoice Processing Automation Using OCR (UI Path)

### Aim:
To automate the extraction of data from invoice PDFs using Optical Character Recognition (OCR) and save the extracted data (Invoice Number, Date, and Total Amount) into an Excel file.

### Equipment Required:
1. A computer with Windows OS.
2. UI Path Studio installed.
3. Invoice PDF files for processing.
4. Excel application or library to handle Excel files.

### Theory:
Optical Character Recognition (OCR) is a technology that converts different types of documents, such as scanned paper documents, PDFs, or images captured by a digital camera, into editable and searchable data. In this exercise, we will use the following key activities:

- **Read PDF with OCR**: This activity allows us to extract text from PDF files using OCR capabilities.
- **Write Range**: This activity enables us to write data to an Excel file.
- **Regular Expressions (Regex)**: These can be used to extract specific pieces of information, such as Invoice Number, Date, and Total Amount, from the text obtained through OCR.

### Procedure:

>#### 1. **Open UI Path and Create a New Project**
#### Step 1: Open UI Path Studio
- Launch UI Path Studio and create a new project (e.g., "InvoiceProcessingAutomation").

>#### 2. **Set Up Variables**
#### Step 2: Define Variables
- Define the following variables:
  - `invoiceText` (String): To hold the extracted text from the invoice PDF.
  - `invoiceNumber` (String): To store the extracted invoice number.
  - `invoiceDate` (String): To store the extracted invoice date.
  - `totalAmount` (String): To store the extracted total amount.
  - `outputData` (DataTable): To hold the data for writing to Excel.

>#### 3. **Read PDF and Extract Text**
#### Step 3: Use Read PDF with OCR Activity
- Add a **Read PDF with OCR** activity to the workflow.
- In the **Properties** panel, set the **FileName** to the path of the invoice PDF.
- Store the output in the `invoiceText` variable.

>#### 4. **Extract Required Data Using Regex**
#### Step 4: Use Regex to Extract Data
- Use **Assign** activities to extract the required information from `invoiceText` using Regex patterns:
  - For Invoice Number:
    ```VB
    invoiceNumber = System.Text.RegularExpressions.Regex.Match(invoiceText, "Invoice Number:\s*(\w+)").Groups(1).Value
    ```
  - For Invoice Date:
    ```VB
    invoiceDate = System.Text.RegularExpressions.Regex.Match(invoiceText, "Invoice Date:\s*(\d{2}/\d{2}/\d{4})").Groups(1).Value
    ```
  - For Total Amount:
    ```VB
    totalAmount = System.Text.RegularExpressions.Regex.Match(invoiceText, "Total Amount:\s*\$(\d+\.\d{2})").Groups(1).Value
    ```

>#### 5. **Prepare Data for Excel**
#### Step 5: Create DataTable and Add Data
- Initialize `outputData` as a DataTable with columns (Invoice Number, Date, Total Amount).
- Use a **Add Data Row** activity to add a new row with the extracted values.

>#### 6. **Write Data to Excel**
#### Step 6: Write Data to Excel File
- Use the **Write Range** activity to write `outputData` to an Excel file.
- Specify the path for the Excel file (e.g., `C:\path\to\output.xlsx`).

>#### 7. **Save and Run the Workflow**
#### Step 7: Save the Workflow
- Save the workflow by clicking the save icon or pressing `Ctrl + S`.

#### Step 8: Run the Automation
- Run the automation to extract data from the invoice PDF and save it to the specified Excel file.

### Output:
1. **Extracted Data**: The data (Invoice Number, Date, Total Amount) extracted from the invoice PDF.
2. **Excel File**: The extracted data will be saved in an Excel file at the specified location.

### Result:
The automation successfully processes invoice PDFs using OCR to extract relevant data and saves it into an Excel file, demonstrating the use of OCR and data handling activities in UI Path.
