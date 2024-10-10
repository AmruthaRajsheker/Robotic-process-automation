## Exercise 6: Copy and Rename Files (UI Path)

### Aim:
To create an automation that copies all files from a source folder to a destination folder and renames them by appending a timestamp to the file names.

### Equipment Required:
1. A computer with Windows OS.
2. UI Path Studio installed.
3. A source folder containing files to be copied.

### Theory:
File manipulation is a common task in automation. UI Path provides activities that allow users to perform various file operations, including copying and renaming files. In this exercise, we will use the following activities:

- **Copy File**: This activity is used to copy files from one location to another.
- **Get File Name**: This activity retrieves the name of the files in the specified directory.
- **Assign Activity**: This is used to create new file names by appending timestamps.

### Procedure:

>#### 1. **Open UI Path and Create a New Project**
#### Step 1: Open UI Path Studio
- Launch UI Path Studio and create a new project (e.g., "CopyRenameFiles").

>#### 2. **Set Up Variables**
#### Step 2: Define Variables
- Define the following variables:
  - `sourceFolder` (String): Path of the source folder (e.g., `C:\path\to\source\folder`).
  - `destinationFolder` (String): Path of the destination folder (e.g., `C:\path\to\destination\folder`).
  - `files` (Array of String): To hold the list of files in the source folder.
  - `timestamp` (String): To hold the current timestamp for renaming.

>#### 3. **Get List of Files**
#### Step 3: Retrieve Files from Source Folder
- Use the **Assign** activity to set `files` to `Directory.GetFiles(sourceFolder)`, which retrieves all files in the source folder.

>#### 4. **Copy and Rename Files**
#### Step 4: Loop Through Files
- Use a **For Each** activity to iterate through each file in the `files` array.
  - Inside the **For Each** activity:
    - Use the **Assign** activity to set the `timestamp` variable to the current date and time formatted as desired (e.g., `Now.ToString("yyyyMMdd_HHmmss")`).
    - Use another **Assign** activity to create the new file name by appending the timestamp to the original file name.
      ```VB
      newFileName = Path.GetFileNameWithoutExtension(file) + "_" + timestamp + Path.GetExtension(file)
      ```
    - Use the **Copy File** activity to copy the file to the destination folder with the new name.
      - Set the **Source** property to `file`.
      - Set the **Destination** property to `Path.Combine(destinationFolder, newFileName)`.

>#### 5. **Save and Run the Workflow**
#### Step 5: Save the Workflow
- Save the workflow by clicking the save icon or pressing `Ctrl + S`.

#### Step 6: Run the Automation
- Run the automation to copy all files from the source folder to the destination folder while renaming them with a timestamp.

### Output:
1. **Copied Files**: All files from the source folder will be copied to the destination folder.
2. **Renamed Files**: Each file will be renamed by appending the current timestamp to its original name.

### Result:
The automation successfully copies and renames files from a source folder to a destination folder, demonstrating the use of **Copy File**, **For Each**, and file manipulation techniques in UI Path.
