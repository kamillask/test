# Test Plan
**Author**: Group 5

## 1 Testing Strategy

### 1.1 Overall strategy

Our testing strategy for the Reminder App will encompass multiple levels of testing to ensure that each component functions correctly both in isolation and in conjunction with other components. The testing levels will include:

- Unit Testing: Individual components will be tested to ensure that they perform as expected. This will include testing classes, methods, and functions for the core functionality such as list creation, reminder instantiation, alert setup, and system acknowledgment.

- Integration Testing: After unit testing, we will perform integration tests to verify that the components work together. This will involve testing the interactions between the 'New Reminder List' creation feature, 'Individual Reminder' creation feature, 'Alert Repeat' function, and the acknowledgment signals.

- System Testing: The entire application will be subjected to system testing to ensure that it meets the requirements specified in the sequence behavioral description. This will test the end-to-end functionality of the app, including user interaction flows and system responses.

- Regression Testing: Whenever a new feature is added or an existing feature is modified, regression tests will be performed to ensure that the change has not adversely affected the existing functionality.

The testing will be carried out iteratively, with each release cycle going through the unit, integration, system, and regression tests as needed. The testing team will include software testers for manual testing and software developers for automated test script creation.


### 1.2 Test Selection

The selection of test cases will be based on both black-box and white-box testing techniques:
* Black-box Testing: Test cases will be derived from the software requirements and specifications without considering the internal workings of the application. This will include:

    * Functional Testing: To verify that each function of the software application behaves as specified in the sequence behavioral description.

    * Non-functional Testing: To assess the application’s performance, usability, reliability, and responsiveness.

* White-box Testing: Test cases will be based on the internal structure of the application. This will include:

    * Path Testing: To ensure all possible paths through the code are executed at least once.

    * Statement and Branch Coverage: To ensure that all possible branches in the code have been tested and that every statement in the code has been executed.

Both techniques will be employed at different testing levels. For example, unit testing will lean more towards white-box testing, while system testing will primarily utilize black-box testing.

Then we will proceed to define specific test cases based on the features and behaviors described.


### 1.3 Adequacy Criterion

**Code Coverage:** Aiming for at least 80% code coverage for unit tests.

**Requirements:** Coverage; make sure all the functional requirements are covered by one test case for system testing.


### 1.4 Bug Tracking

We will use the [Bug Tracking System] tool for bug and enhancement tracking. All bugs and issues discovered during testing will be recorded and tracked through this system until solved.

### 1.5 Technology

**JUnit:** The testing framework for writing and running repeatable tests in Java, used for unit-level testing.

**AndroidJUniRunner:** The default test runner on Android which supports both JUnit4 and JUnit3 tests.

**Android Profiler:** Integrated into Android Studio, it provides real-time statistics for CPU usage to see the performance.

**Crashlytics:** Real-time reporting is critical for monitoring the app stability.


## 2 Test Cases

### 2.1 Unit Testing

#### 2.1.1 Reminder List Creation

* Test Case ID: TC_ULC_01

    * Objective: To verify that the application allows the creation of a new reminder list.

    * Test Steps:

            1. Navigate to the 'Create New List' feature.

            2. Enter a valid list name.

            3. Submit the request to create a new list.

            4. Expected Result: A new reminder list is created with the given name.

            5. Actual Result: [To be filled during testing]

#### 2.1.2 Individual Reminder Creation

* Test Case ID: TC_UIR_01

    * Objective: To verify that individual reminders can be added to the list.

    * Test Steps:

            1. Select an existing reminder list.

            2. Use the 'Add Reminder' feature to create a new reminder with valid details.

            3. Submit the reminder details.

            4. Expected Result: The new reminder is added to the selected list.

            5. Actual Result: [To be filled during testing]

#### 2.1.3 Alert Repeat Function
 
* Test Case ID: TC_UAR_01

    * Objective: To verify that the alert repeat function sets up recurring reminders correctly.

    * Test Steps:

            1. Create a new reminder or select an existing one.

            2. Access the 'Alert Repeat' settings.

            3. Configure a repeat interval and save the settings.

            4. Expected Result: The reminder is set to repeat at the specified interval.

            5. Actual Result: [To be filled during testing]


### 2.2 Integration Testing

#### 2.2.1 Reminder List and Reminder Integration

* Test Case ID: TC_ILRI_01

    * Objective: To test the integration between reminder list creation and individual reminder addition.

    * Test Steps:

            1. Create a new reminder list.

            2. Add a new reminder to the created list.

            3. Check if the reminder is correctly associated with the list.

            4. Expected Result: The reminder is correctly added to the newly created list.

            5. Actual Result: [To be filled during testing]

#### 2.2.2 System Acknowledgment upon Reminder Creation

* Test Case ID: TC_ISA_01

    * Objective: To verify that the system provides acknowledgment upon successful creation of a reminder.

    * Test Steps:

            1. Create a new reminder.

            2. Observe the system's response after the reminder is created.

            3. Expected Result: The system generates an acknowledgment signal.

            4. Actual Result: [To be filled during testing]


### 2.3 System Testing

#### 2.3.1 Complete Application Workflow

* Test Case ID: TC_SAW_01

    * Objective: To verify the complete workflow of creating a reminder list, adding reminders, setting alerts, and receiving acknowledgments.

    * Test Steps:

            1. Start the application.

            2. Create a new reminder list.

            3. Add multiple reminders with varying types and alert settings.

            4. Verify that acknowledgments are received and alerts are set correctly.

            5. Expected Result: The application performs the complete workflow seamlessly, with correct acknowledgments and alerts.

            6. Actual Result: [To be filled during testing]

#### 2.3.2 Alert Functionality and Responsiveness

* Test Case ID: TC_SAF_01

    * Objective: To assess the functionality and responsiveness of the alert system.

    * Test Steps:

            1. Set a reminder with an alert.

            2. Trigger the alert by reaching the set time or location.

            3. Observe the system's alert notification.

            4. Expected Result: The system promptly displays the alert notification at the appropriate time or location.

            5. Actual Result: [To be filled during testing]


### 2.4 Regression Testing

#### 2.4.1 Post-Update Application Behavior

* Test Case ID: TC_RAB_01

    * Objective: To ensure that updates have not adversely affected existing functionality.

    * Test Steps:

            1. Repeat all previously passed test cases after an update is applied.

            2. Expected Result: All features work as expected, as in the previous version.

            3. Actual Result: [To be filled during testing]

|Test Case ID|Purpose   |Steps   |Expected Result   |Actual Result   |Pass/Fail   |Comments   |
|---|---|---|---|---|---|---|
|TC01   |Validate user login   |1.Enter username and password. <br />2. Click login   |Successful login and dashboard displayed   |   |   |   |
|TC02   |Check reminder creation   |1.Navigate to reminders. <br />2. Create a new reminder   |New reminder is added to the list   |   |   |   |
|TC03   |Check Invalid Login   |1.Open app. <br />2. Enter invalid username and password   |Error message displayed   |   |   |Error message should be clear and helpful.   |
|TC04   |Test Reminder Notification   |1.Create a reminder with an alert. <br />2. Wait for the alert time   |Notification is received at the correct time   |   |   |Test with phone locked and unlocked.   |

