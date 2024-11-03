# Exercise 3: Flow Sequence or Flow Chart Using Repeat, While, and Do-While Loops (UI Path)

## Aim:
To create an automation that demonstrates the usage of **Repeat**, **While**, and **Do-While** loops in UI Path through a Flow Sequence or Flow Chart.

## Equipment Required:
1. A computer with Windows OS.
2. UI Path Studio installed.
3. Basic knowledge of UI Path activities (Repeat, While, and Do-While loops).

## Theory:
In UI Path, loops are used to perform repetitive actions until a specified condition is met. The most commonly used loops are:

1. **Repeat**: Repeats a set of activities a specified number of times.
2. **While**: Executes a block of activities while a given condition is true.
3. **Do-While**: Similar to While, but ensures that the activities inside the loop execute at least once before checking the condition.

Each of these loops can be used to automate repetitive tasks and control the flow of the automation process.

## Procedure:

### 1. **Creating a Flow Sequence with Loops**:
#### Step 1: Open UI Path Studio
- Launch UI Path Studio and create a new project (e.g., "FlowWithLoops").

#### Step 2: Design the Flow
- Open **Main.xaml** and create a **Flow Chart** or **Flow Sequence** depending on your preference.
- Drag and drop the necessary activities for the three loops: Repeat, While, and Do-While.


>#### 1.1. **Using the Repeat Activity**

#### Step 3: Create the Repeat Loop
- Add a **Repeat Number of Times** activity to the Flow.
- Set the **Number of Repetitions** property to 5.
- Within the **Do** section of the Repeat activity, add a **Message Box** displaying `"Iteration X"` (where X is the iteration number). You can use a counter variable (`counter`) and increment it inside the loop.
  ```VB
  counter.ToString
  ```


>#### 1.2. **Using the While Loop**

#### Step 4: Create the While Loop
- Add a **While** activity in the sequence or flow.
- Define a condition for the loop (e.g., `counter < 5`).
- Inside the loop, use a **Message Box** activity to display `"In While Loop: Iteration " + counter.ToString`.
- Increment the counter by 1 at the end of each iteration.


>#### 1.3 **Using the Do-While Loop**

#### Step 5: Create the Do-While Loop
- Add a **Do While** activity to the Flow.
- Set the condition (e.g., `counter < 5`).
- In the **Do** section, use a **Message Box** to display the message `"In Do-While Loop: Iteration " + counter.ToString`.
- Increment the counter inside the loop.


### 2. **Connect the Loops in the Flow Chart**:
- In the **Flow Chart** or **Flow Sequence**, connect the Repeat, While, and Do-While activities logically.
- Ensure that they execute in sequence, starting from Repeat, followed by While, and finally Do-While.

#### Step 6: Save and Run
- Save the workflow by clicking on the save icon.
- Run the automation to see the loops in action.

## Main.xaml:

![image](https://github.com/user-attachments/assets/e940f9c0-0934-4c75-a630-9334c3dd6d70)

![image](https://github.com/user-attachments/assets/276a7e02-c0df-4d2a-a4c1-09d089bb7411)

![image](https://github.com/user-attachments/assets/2b5e59ed-f3c7-4eb1-a849-5323b1a49f8e)


## Output:
1. **For Repeat Loop**: 
   - A message box will appear 5 times displaying `"Iteration 1"`, `"Iteration 2"`, etc.
   
2. **For While Loop**:
   - A message box will display 5 times as long as the condition is true, showing `"In While Loop: Iteration 1"`, `"Iteration 2"`, and so on.

3. **For Do-While Loop**:
   - A message box will appear at least once and continue to display until the condition is false, showing `"In Do-While Loop: Iteration 1"`, `"Iteration 2"`, and so on.

![image](https://github.com/user-attachments/assets/216c41c9-73d1-4142-b371-2194c10496ed)


## Result:
The automation successfully demonstrates the use of **Repeat**, **While**, and **Do-While** loops, iterating over a series of actions and controlling the flow of execution based on conditions.

