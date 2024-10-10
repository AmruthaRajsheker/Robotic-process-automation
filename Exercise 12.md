## Exercise 12: Automate an Unattended Robot Using Orchestrator (UI Path)

### Aim:
To create and deploy an automation process for an unattended robot using UiPath Orchestrator.

### Equipment Required:
1. A computer with Windows OS.
2. UiPath Studio installed.
3. UiPath Orchestrator account and access.
4. UiPath Robot installed on the machine intended for unattended execution.
5. Basic knowledge of creating processes in UiPath Studio.

### Theory:
UiPath Orchestrator is a web-based application that enables users to deploy, monitor, and manage UiPath robots in an enterprise environment. Unattended robots can run processes without human intervention, which is particularly useful for handling repetitive tasks and processing large volumes of work. The steps to automate an unattended robot include creating a process in UiPath Studio, publishing it to Orchestrator, and configuring the robot settings.

### Procedure:

>#### 1. **Create a New Project in UiPath Studio**
#### Step 1: Open UiPath Studio
- Launch UiPath Studio and create a new project (e.g., "UnattendedRobotProcess").

>#### 2. **Design the Automation Workflow**
#### Step 2: Build the Automation
- Design the automation workflow in UiPath Studio according to the task you want the unattended robot to perform (e.g., data entry, report generation, etc.).

>#### 3. **Publish the Project to Orchestrator**
#### Step 3: Publish the Process
- Once the workflow is complete and tested, publish it to UiPath Orchestrator.
  - Click on the **Publish** button in UiPath Studio.
  - Select the appropriate Orchestrator URL and the folder where you want to publish the process.
  
>#### 4. **Set Up UiPath Orchestrator**
#### Step 4: Log in to UiPath Orchestrator
- Open a web browser and navigate to your UiPath Orchestrator URL.
- Log in with your credentials.

#### Step 5: Create a New Process
- Navigate to the **Processes** section in Orchestrator.
- Click on **+ Add** to create a new process.
- Select the package you published earlier and configure any necessary settings (e.g., description, version).

>#### 5. **Create and Configure an Unattended Robot**
#### Step 6: Configure Robot
- Navigate to the **Robots** section in Orchestrator.
- Click on **+ Add** to create a new unattended robot.
- Fill in the required details:
  - Name of the robot
  - Type (Unattended)
  - Machine on which the robot is installed
  - Domain and Username (for logging into the machine)
- Save the robot configuration.

>#### 6. **Create a Trigger for the Process**
#### Step 7: Set Up a Trigger
- Navigate to the **Triggers** section in Orchestrator.
- Click on **+ Add** to create a new trigger.
- Select the process you created earlier and configure the trigger settings (e.g., start time, recurrence).
  
>#### 7. **Test the Unattended Robot**
#### Step 8: Start the Trigger
- Ensure that the unattended robot is running on the designated machine.
- Manually start the trigger if necessary to test the automation.
- Monitor the process execution through the Orchestrator dashboard.

>#### 8. **Monitor and Manage the Robot**
#### Step 9: Check Logs and Alerts
- After the trigger executes, monitor the logs in Orchestrator for any errors or alerts.
- Adjust the process or robot settings as needed based on performance and outcomes.

### Output:
1. **Process Execution**: The unattended robot will execute the defined process as scheduled.
2. **Logs and Alerts**: Execution logs will be available in Orchestrator for monitoring performance.

### Result:
The automation successfully sets up an unattended robot process using UiPath Orchestrator, demonstrating the ability to manage and deploy automated workflows in an enterprise environment.
