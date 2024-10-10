## Exercise 5: Web Scraping Data (UI Path)



### Aim:
To create an automation that scrapes data from a website and saves it to a CSV file using UI Path.



### Equipment Required:
1. A computer with Windows OS.
2. UI Path Studio installed.
3. Internet access to access a website for scraping data.



## Theory:
**Web scraping** is a technique used to extract data from websites. UI Path provides web scraping capabilities that allow users to automatically gather structured data from web pages. Once scraped, this data can be saved in various formats such as CSV, Excel, or databases.

**Key UI Path Activities**:
1. **Data Scraping Wizard**: This built-in tool allows you to easily select the structured data on a webpage and scrape it.
2. **Write CSV Activity**: After scraping the data, it can be written to a CSV file using the **Write CSV** activity.



### Procedure:

>#### 1. **Open UI Path and Create a New Project**
#### Step 1: Open UI Path Studio
- Launch UI Path Studio and create a new project (e.g., "WebScrapingProject").



>#### 2. **Design the Workflow**
#### Step 2: Open the Browser for Scraping
- In the **Activities** panel, search for the **Open Browser** activity.
- Drag and drop it into the sequence.
- In the **Properties** panel, provide the URL of the website you want to scrape data from (e.g., a shopping site, job listings, or any site with structured data).
  Example:
  ```https://example.com```

#### Step 3: Use the Data Scraping Wizard
- Inside the **Open Browser** activity, search for **Data Scraping**.
- Drag and drop the **Data Scraping** wizard into the **Do** section of **Open Browser**.
- Click **Next** on the wizard and select the structured data (e.g., product names, prices, job titles) from the web page that you want to scrape.
- After configuring the selection, the wizard will generate a **DataTable** that holds the scraped data. Name this DataTable as `scrapedData`.



>#### 3. **Save Data to CSV**
#### Step 4: Write Scraped Data to CSV
- After the **Data Scraping** activity, add a **Write CSV** activity.
- In the **Properties** panel, specify the **File Path** for the CSV file (e.g., `C:\path\to\your\output.csv`).
- Set the **DataTable** property to `scrapedData` to save the scraped data into the CSV file.



>#### 4. **Save and Run the Workflow**
#### Step 5: Save the Workflow
- Save the workflow by clicking the save icon or pressing `Ctrl + S`.

#### Step 6: Run the Automation
- Run the automation to launch the browser, scrape the data, and save it to the specified CSV file.



### Output:
1. **Web Scraped Data**: The selected structured data from the website will be stored in a **DataTable**.
2. **CSV File**: The scraped data will be saved as a CSV file at the specified location.


### Result:
The automation successfully scrapes structured data from a website and saves it to a CSV file, demonstrating the use of Data Scraping and Write CSV activities in UI Path.


## Result:
The automation successfully scrapes structured data from a website and saves it to a CSV file, demonstrating the use of **Data Scraping** and **Write CSV** activities in UI Path.



