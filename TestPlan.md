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



| Test Case ID | Purpose                                    | Steps                                                                                                  | Expected Result                        | Actual Result                                                       | Pass/Fail | Comments                          |
|--------------|--------------------------------------------|--------------------------------------------------------------------------------------------------------|----------------------------------------|---------------------------------------------------------------------|-----------|-----------------------------------|
| TC01         | Add ReminderList                           | 1. Click on the add button on the first screen. <br />2. Add a new list name                                | A new reminder list is created         | Is added                                                            | Pass      | May have to refresh the screen    |
| TC02         | Add reminder type                          | 1. Click on the add button Check if the new type is stored in the spinner. <br />2. Select the type                | A new reminder type is added           | Is added                                                            | Pass      | Works as expected                 |
| TC03         | Add a new Reminder                         | 1. Type the new reminder inside the edit text. <br />2. Click save button                                          | A new reminder name is added           | Is added                                                            | Pass      | Works as expected                 |
| TC04         | Add a new date                             | 1. Select a new date from the date picker <br />2. Click save button                                               | A new date is added                    | Is added                                                            | Pass      | Works as expected                 |
| TC05         | Add a new time                             | 1. Select a new time from the time picker <br />2. Click the save button.                                          | A new time is added                    | Is added                                                            | Pass      | Works as expected                 |
| TC06         | Display reminder list                      | Click on the plus icon. Type the name of the list Go back to the main screen                           | Reminder List added to the main screen | Is added                                                            | Pass      | Works as expected                 |
| TC07         | Deleting reminder list                     | On the main screen, where the reminder list is displayed, click on the three dots. Click delete.       | Is deleted                             | Is deleted                                                          | Pass      | Only deletes from screen          |
| TC08         | Deleting reminder list (Database)          | 1. On the main screen, where the reminder list is displayed, click on the three dots. 2. Click delete. | Is deleted                             | Not deleted                                                         | Fail      | Does not delete from the database |
| TC09         | Deleting reminder name and type            | The reminder name and type are displayed.  Click on the three dots and delete.                         | Is deleted                             | Is deleted                                                          | Pass      | Only deletes from screen          |
| TC10         | Deleting reminder name and type (Database) | The reminder name and type are displayed. Click on the three dots and delete.                          | Is deleted                             | Not deleted                                                         | Fail      | Does not delete from the database |
| TC11         | CheckOff reminder                          | On the list of reminders name screen, click on the checkbox. Check or uncheck                          | Uncheck the reminder                   | Unchecked                                                           | Pass      | Works as expected                 |
| TC12         | Adding reminderType to spinner             | On adding reminders screen, type a new reminder type. Click ‘add’ button.                              | Is added                               | Is added                                                            | Pass      | Added inside the database         |
| TC13         | Uncheck all reminders                      | 1 check all the reminders first. 2. And click the Uncheck All button.                                  | Uncheck all reminders                  | Unchecked                                                           | Pass      | Works as expected                 |
| TC14         | Edit reminderList                          | 1 Click the button on the right side of the list, then click edit                                      | Add or rename the list                 | After delete the reminder, then restart the app, it come back again | Fail      | Not implemented                   |
| TC15         | Edit reminder name and type                | 1 click the button on the right side of the reminder, then click edit                                  | Edit the name and type                 | After click edit, there is no response.                             | Fail      | Not implemented                   |
