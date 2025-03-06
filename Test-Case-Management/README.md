# Objective

This document primarily serves as a guide to a team's approach to test case management in TestRail. It aims to outline a hierarchical structure for clear and organized testing efforts, as test case management is a crucial part of the software testing process, ensuring that testing activities are well-organized, traceable, and aligned with project goals.

Secondarily, it highlights best practices and offers a potential implementation reference for other teams seeking to establish or improve their test case organization, particularly within TestRail.

## Context:

Previously, test cases were categorized by Location in UI, Feature/Specific Action, Project, and APIs. While this allows for UI and Feature Focus, it brought up issues with duplication & inconsistency, scattered coverage, increased test case maintenance effort, and added confusion and complexity.

## Test Suites:
This is organized using TestRail, a web-based test case management tool used by QA engineers, developers, and team leads to manage, track, and organize testing efforts.

* **&lt;projectName>** currently uses two Suites for test case management: 

* **&lt;projectName Test suite URL>** 

* **&lt;projectName Automation Test Suite URL>** 


# Core Principles

* **Clarity:** The structure should be clear, easy to understand, and provide a logical flow for organizing test cases.

* **Maintainability:** The structure should be easy to maintain and update as the project evolves and new features are added.

* **Reusability:** The structure should promote the reusability of test cases and test components across different areas of the application.

* **Scalability:** The structure should be scalable to accommodate a growing number of test cases and functionalities.

# Hierarchical Structure

* **Why this new structure?**

When starting with broad categories and drilling down into more specific areas; this structure helps organize test cases by allowing for a logical flow and making it easier to locate and manage test cases. I’ve found this approach is helpful for large or complex projects where a clear and well-defined structure is essential for efficient test management.

This approach has several advantages over alternative structures like organizing by feature or location in UI:

* **Clarity and organization:** This structure provides a clear and logical flow, making it easier to understand the relationships between different test areas and locate specific test cases.

* **Maintainability:** As the project evolves and new features or functionalities are added, a hierarchical structure is easier to maintain and update.

* **Scalability:** The structure provides a flexible framework that can be easily expanded to incorporate new test cases and/or functionalities as your project evolves.

* **Reduced redundancy:** By grouping related tests together, using a hierarchical structure helps to avoid redundancy while ensuring test cases are not duplicated across different sections.

* **Better collaboration:** This structure also facilitates collaboration between different teams and stakeholders by providing a shared understanding of the test organization. This can be particularly helpful when there are transitions of feature or service ownership between teams, as the structure helps maintain clarity and avoid confusion.

# Section Descriptions

Each section in the project hierarchy should have a description that explains its purpose and scope. This helps testers and stakeholders understand the organization of the test suite and locate relevant test cases.

**Example Section Descriptions:**

* **Functional Area 1:** This section contains tests related to the core functionality of [Functional Area 1], such as [list key functionalities]. Make sure that test data is created and maintained to accurately reflect the data flows and dependencies within this functional area.

* **Feature 1:** This section focuses on testing [Feature 1] within [Functional Area 1]. It includes tests for [list key aspects of the feature]. Consider including the specific test data requirements for this feature, including any necessary data setup or cleanup following test completion.

* **Test Type 1 (e.g., Functional Tests):** These tests validate the core functionality of [Feature 1], ensuring that it meets the specified requirements.

*Note: Sometimes certain test types require having a dedicated section within a specific feature, while others may not, and instead only live in the Non-Functional test section.*

* *Example:* 
    * ***Compatibility Tests***
        * ***Within a Feature:*** These tests verify the compatibility of [Feature 1] with different browsers, devices, and operating systems.
        * ***Non-Functional Tests:*** These general tests assess the overall compatibility of the application across different environments.

The new structure consolidates tests by Test Type and Feature and is divided into several main categories: Authentication/Authorization Tests, User Management, UAT Tests, API Testing, and Tools. 

*Note: Considering the complexity and the number of test cases involved with IAM and login (e.g. MFA, biometrics, step-up authentication, SSO, etc); we use separate categories for these features for better organization, scalability, and focus.*

# Testing Types to Consider

Currently in our Suite we use the following to ensure comprehensive test coverage:

* ***UI Tests:*** Evaluating the usability and visual aspects of the system’s login interface, including form elements, error messages, and responsiveness.
* ***Database Tests:*** Focus on the Data integrity, validation, and persistence concerning the feature being tested.
* ***Functional Tests:*** These tests validate the core functionality of the feature 
* ***Backend Tests:*** These tests evaluate the server-side logic and security mechanisms related to the feature.
* ***Compatibility Tests:*** Checks the compatibility of the system with different hardware, operating systems, browsers, and other software components. This includes Browser and Device tests.
* ***General:*** Ensure the application works correctly across different browsers, devices, and operating systems. Some teams user browserstack for this testing. If interested let me know.
* ***Feature-Specific:*** Test compatibility within specific features where it is a major concern.
* ***API Tests:*** These tests validate the login functionality exposed through APIs for toastweb, including API endpoints, data formats, and security measures.
* ***Usability Testing:*** Evaluate the user-friendliness and ease of use of the application.
* ***Accessibility Testing:*** Ensure the application/feature is accessible to users with disabilities.

*UAT tests are to be written following the e2e User Journey, following BDD when able.*

*Other testing types you may consider for your team might include:*
* *Performance Testing: Assess the performance and scalability of the application under different load conditions*
* *Security Testing: Identify vulnerabilities and security risks in the application*
* *Localization Testing: Verify the application/feature is adapted for different languages and regions*

# Test Case Creation

Test cases are written based on functional requirements, user stories, and acceptance criteria. Each test case is designed to verify a specific aspect of the feature or functionality, ensuring that all edge cases are accounted for and that the product meets the desired quality standards.

## Test Case Naming Conventions

The naming convention should include information about the feature, scenario, and expected result. They should be easy to identify and understand. The following guidelines are often used. 

* ***Start with "Verify":*** Beginning the test case title with the word "Verify" indicates that it is a test case designed to verify a specific functionality or behavior.
* ***Describe the Goal:*** Use clear and concise language when describing the goal of the test case in the title. Action-oriented language can then be used to indicate what the test case will be verifying.
* ***Be Specific:*** Use specific and unambiguous language to avoid any confusion about the test case's objective. Include relevant details like the specific conditions or actions involved in the test.

*In instances where the test is specifically covering the functionality of a platform is indicating only the general platform being tested can be helpful. For example, if you had a case like Verify push notification on app open (mobile), it would be beneficial to use mobile in the title, and within the test steps you would then be able to list the specific platforms (e.g. Android, iOS).*

### The following fields should be filled out for each test:

* ***Dedicated Project:*** Each team should have a dedicated TestRail project to manage their test cases.
* ***Test Case Fields:*** Include the following fields in each TestRail test case:
* ***Test Type:*** (e.g., Functional, Integration, Other, Performance, Regression, Security)
* ***Priority:*** (e.g., Critical, High, Medium, Low, Do not test)
* ***Owner:*** (Individual)
* ***Services Covered:*** (List the services involved in the test case)
* ***Line of Business:*** (Specify the area of the business the test case relates to)
* ***Jira Ticket:*** If applicable, link the relevant Jira ticket(s) to the test case for traceability. (This is reflected in the Jira ticket when used)
* ***Preconditions:*** List all preconditions needed to execute the test case. This can include links (to confluence or other test cases), data setup instructions, devices needed to run the test case, etc.
*Optional*
* *Automation Candidates: When considering automation for your test cases you can use the following fields. (Some teams may have a separate automation suite, but should your team not want to do that, this is how you could implement using this structure.)*
* *"Ready for Automation" Checkbox: Select this to mark test cases that are good candidates for automation. This helps identify and prioritize test cases for automation.*
* *"Automated" Checkbox: Select this checkbox, and uncheck “Ready for Automation” once you test case is automated.*
* *Framework Used: If a test case is automated, specify the automation framework used (e.g., Proof - (Selenium or Appium), Playwright, Postman). This helps track automation progress and identify which frameworks are being used for different types of tests.*

### Example IAM Test Case Title with naming breakdown, test type, and location:

* ***Verify Account Lockout until Password Reset***
    * ***Naming Breakdown:*** Verify indicates that this is a test case, Account Lockout specifies the feature being tested, Password reset describes the condition for the account remaining locked. 
    * ***Test Type:*** Functional
          * ***Focus on Functionality:*** It verifies the core functionality of the account lockout feature, specifically how it behaves in relation to the password reset process.
          * ***Workflow Validation:**** It tests a specific workflow or sequence of actions (account lockout, password reset, account unlock)
          * ***Black-box Perspective:*** It tests the system's behavior without requiring knowledge of the internal implementation details. It focuses on the inputs (failed login attempts, password reset) and the expected outputs (account locked, account unlocked).
    * ***Structure:***
      * ***Example Structure:***

Identity & Access Management 

    ├── Authentication and Authorization Tests
    │   ├── Web
    │   │   ├── Login Tests
    │   │   │   └── Functional Tests
    │   │   │   	└── Account Lockout
    │   │   │   		└── Failed Login Flow
    │   │   │   		└── Account Password Reset Flow
    │   │   │   			└── Verify Account Lockout until Password Reset
 
# Test Execution and Reporting

Using TestRails integration with Jira to visibility.

* ***Create and Link Test Runs:*** For each Jira ticket, create a corresponding test run in TestRail and link it to the ticket. This for wider visibility for your team and makes it easier to track testing progress for each ticket.
* ***Assign Test Cases:*** Assign specific test cases to the test run, ensuring that all relevant tests are executed for the given ticket or feature.
* ***Execute Tests:*** Execute the test cases within the test run, marking the test result, and providing detailed results and any relevant attachments or comments.
* ***Close Test Runs:*** Once all tests within a test run are completed, close the run in TestRail to indicate that testing is finished for that particular ticket or feature. This helps maintain a clean and organized testing history.

# Continuous Improvement

Regularly review and update the test case management hierarchy as the project evolves and new features or functionalities are added. This maintenance will help with keeping your cases relevant, and organized.

# Adapting the Template

While this structure provides a general framework for organizing test cases, feel free to adapt it to your specific needs. This could look like:

* Adding or removing sections to reflect the specific features and functionalities of your application.
* Customizing section descriptions to better describe the purpose and scope of each section.
* Changing the test case naming convention to fit your project's needs or preferences.
* Integrating the test case management hierarchy with your existing testing tools, processes, and workflows.
