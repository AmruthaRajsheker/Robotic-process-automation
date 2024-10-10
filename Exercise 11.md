## Exercise 11: API Integration and Data Processing (UI Path)

### Aim:
To create an automation that calls a REST API (e.g., Weather API), processes the JSON response, and writes the data to a database using UI Path.

### Equipment Required:
1. A computer with Windows OS.
2. UI Path Studio installed.
3. Internet access to call the REST API.
4. A database setup (e.g., SQL Server, MySQL) to write the data.

### Theory:
API integration allows applications to communicate and exchange data. UI Path can call REST APIs using the **HTTP Request** activity and process the JSON responses using built-in functionalities. Once the data is processed, it can be inserted into a database.

**Key UI Path Activities**:
- **HTTP Request**: This activity is used to send HTTP requests to a REST API and receive responses.
- **Deserialize JSON**: This activity converts the JSON response into a .NET object for easier data manipulation.
- **Database Activities**: Activities like **Execute Non Query** to write data into the database.

### Procedure:

>#### 1. **Open UI Path and Create a New Project**
#### Step 1: Open UI Path Studio
- Launch UI Path Studio and create a new project (e.g., "APIIntegration").

>#### 2. **Set Up Variables**
#### Step 2: Define Variables
- Define the following variables:
  - `apiUrl` (String): The URL of the REST API (e.g., `"https://api.openweathermap.org/data/2.5/weather?q=London&appid=YOUR_API_KEY"`).
  - `response` (String): To store the API response.
  - `jsonResponse` (JObject): To hold the deserialized JSON response.
  - `temperature` (Double): To store the temperature value extracted from the response.
  - `humidity` (Int32): To store the humidity value extracted from the response.
  - Database connection string (String): Connection string to the database (e.g., `"Server=your_server;Database=your_db;User Id=your_user;Password=your_password;"`).

>#### 3. **Call the REST API**
#### Step 3: Use the HTTP Request Activity
- Drag and drop the **HTTP Request** activity into the workflow.
- Configure the properties:
  - **Method**: Set to `GET`.
  - **Endpoint**: Set to `apiUrl`.
  - **Response**: Set to `response`.

>#### 4. **Process the JSON Response**
#### Step 4: Deserialize the JSON Response
- Use the **Deserialize JSON** activity to convert the `response` string into a JObject.
- Configure the properties:
  - **JsonString**: Set to `response`.
  - **Output**: Set to `jsonResponse`.

#### Step 5: Extract Data
- Use **Assign** activities to extract data from the JSON response:
  - `temperature = jsonResponse("main")("temp").Value(Of Double)()`
  - `humidity = jsonResponse("main")("humidity").Value(Of Int32)()`

>#### 5. **Write Data to Database**
#### Step 6: Use Database Activities
- Use the **Execute Non Query** activity to insert the data into the database.
- Configure the properties:
  - **Connection String**: Set to your database connection string.
  - **Sql**: Write an SQL command to insert the temperature and humidity values:
    ```sql
    INSERT INTO WeatherData (Temperature, Humidity) VALUES (@Temperature, @Humidity)
    ```
  - **Parameters**: Add parameters for `@Temperature` and `@Humidity`.

>#### 6. **Save and Run the Workflow**
#### Step 7: Save the Workflow
- Save the workflow by clicking the save icon or pressing `Ctrl + S`.

#### Step 8: Run the Automation
- Run the automation to call the API, process the response, and write the data to the database.

### Output:
1. **API Response**: The weather data will be retrieved from the API.
2. **Database Entry**: The temperature and humidity values will be stored in the specified database table.

### Result:
The automation successfully integrates with a REST API, processes the JSON response, and writes the extracted data to a database, demonstrating API integration and data processing in UI Path.
