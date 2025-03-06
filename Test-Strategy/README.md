

# Table of Contents

[TOC]

### Revision History

| **Date**   | **Revision #** | **Explanation of Changes** | **Author** |
|:----------------:|:--------------:|:--------------------------:|:----------:|
| Date: 03/06/2025 | 1              | Document creation          | catfrzl    |
| Date:            | 1.1            |                            |            |

## 1 Introduction 
This document aims to demonstrate what the ideal format for a Test Strategy should look like for Identity and Identity Platform-related features.

## 2 What Needs a Test Strategy: 
Any feature that has a broad impact, complex requirements, or significant risks should be accompanied by a detailed test strategy to ensure quality and proper functionality.

Examples of this include:

* **New or Complex Functionality:** When introducing new functionality or complex features that involve multiple components, interactions, or integration points.
  
* **High-Risk Impact:** When the feature has a significant impact on system stability, security, or critical user workflows. This includes features related to sensitive data, permissions, or regulatory compliance.
  
* **Regulatory or Compliance Requirements:** When the feature must meet specific legal, security, or compliance standards (e.g., GDPR, SOC2), which requires in-depth testing.

* **Change in System Behavior:** When a feature alters the system behavior in ways that could affect existing functionality, requiring validation to ensure compatibility and proper integration.

* **Long-Term Maintenance or Support:** When the feature will require ongoing testing and maintenance due to its importance or expected long-term use.

* **Cross-Team Collaboration:** When the feature requires coordination across multiple teams, departments, or systems, ensuring alignment on expectations and responsibilities.

* **Performance, Load, or Stress Considerations:** When performance or scalability is a concern, testing strategies should be designed to assess these aspects under various conditions.

## 3 When to Complete a Test Strategy: 
You should complete the Test Strategy during the *planning phase* of the Software Development Life Cycle (SDLC), ideally before development begins or as early as possible. 

Completing the test strategy in the *planning phase* ensures that testing is aligned with project goals, resource allocation, and risk management early on, allowing for smoother execution during the later stages of the SDLC.

## 4 Test Strategy as it relates to the SDLC

### 4.1 Requirements Gathering/ Analysis

During this phase, the test strategy should be drafted based on the project requirements and scope. The initial test strategy should outline the high-level testing goals, risks, key areas to test, and the overall approach for testing. This provides a framework to align testing efforts with business and technical objectives.

#### 4.1.1 Involved Team Members
* ***Product Owner:*** Provides clarity on the requirements, user stories, and acceptance criteria. Ensures the test strategy aligns with business goals.
* ***QA Engineer:*** Reviews requirements and helps define testable scenarios. Identifies high-risk areas for testing and provides input on possible test types.
* ***Developers:*** Contribute to the understanding of technical constraints and requirements from the development side, helping ensure test strategy feasibility.

#### 4.1.2 Key Activities
* Drafting high-level test strategy
* Identifying Key features, risks, and test requirements
* Aligning testing with user stories and acceptance criteria

#### 4.1.3 Artifacts
**Created:**
* *PRD (Product Requirements Document):* Created by the Product Owner and stakeholders to define the feature’s purpose, scope, and requirements. This serves as the foundation for all subsequent testing artifacts.
* *RFC (Request for Comments):* Created collaboratively by the Product Owner, developers, and other team members to document technical proposals, design decisions, or process changes. The RFC provides a clear reference for the technical aspects of the feature and informs the test plan.

### 4.2 Design
As the design is finalized, the test strategy should be updated with more specific details. This includes defining the testing environments, selecting appropriate tools, determining test data needs, and outlining the approach for integration, security, and performance testing. It ensures that testing activities are integrated into the design process.

#### 4.2.1 Involved Team Members
* ***Product Owner:*** Clarifies any outstanding requirements or features.
* ***QA Engineer:*** Refines the test strategy by detailing the test cases, tools, and environments, and ensuring the testing approach aligns with the system design.
* ***Developers:*** Provide insights into the technical implementation, dependencies, and design decisions that will influence the testing process.
* ***Engineering Manager:*** Ensures that cross-team collaboration occurs and any testing needs are properly accounted for.

#### 4.2.2 Key Activities
* Finalizing the test strategy.
* Defining test environments, tools, and frameworks.
* Detailing the test types (functional, integration, performance, etc.).

#### 4.2.3 Artifacts
**Created:**
*  *[Test Plan](Test-Plan):* Created by the QA Engineer based on the PRD and RFC. The test plan outlines the scope, objectives, resources, timelines, test environments, and types of tests to be executed. It becomes the blueprint for testing.

### 4.3 Development
By the time development begins, the test strategy should be fully defined and approved. The development and QA teams must align their activities, so test cases and automation scripts can be created while the feature is being developed. This ensures testing is prepared to start as soon as the development is complete.

#### 4.3.1 Involved Team Members
* ***Product Owner:*** Ensures that the product vision and user stories are clear and understood, supporting the development and testing alignment.
* ***QA Engineer:*** Develops detailed test cases, prepares automated tests (if applicable), and ensures testings align with the code being developed.
* ***Developers:*** Implement the features, fix bugs, and collaborate with QA to ensure code is testable and test environments are set up properly.
* ***Engineering Manager:*** Helps resolve any blockers, facilitating team collaboration between developers and QA engineers.
  
#### 4.3.2 Key Activities
* Writing and refining test cases.
* Preparing automation scripts (if applicable).
* Ensuring testing aligns with development progress.
  
#### 4.3.3 Artifacts
**Used:**
* *[Test Plan](Test-Plan):* Continues to guide the creation of detailed test cases and ensures alignment between development and testing efforts.


### 4.4 Testing (Verification and Validation)
In this phase, the test strategy is executed. Test cases are run according to the defined strategy, and testing activities such as functional, integration, and regression testing are performed. The strategy should guide test execution and tracking, ensuring that all defined requirements are verified and any defects are logged.

#### 4.4.1 Involved Team Members
* ***Product Owner:*** Reviews the deployment results and ensures that the features deployed align with the business requirements when needed.
* ***QA Engineer:*** Develops detailed test cases, prepares automated tests (if applicable), and ensures testings align with the code being developed.
* ***Developers:*** Implement the features, fix bugs, and collaborate with QA to ensure code is testable and test environments are set up properly.
* ***Engineering Manager:*** Ensures smooth collaboration during the deployment phase and removes any blockers.

#### 4.4.2 Key Activities
* Executing test cases for functional, integration, and regression testing.
* Logging and tracking defects.
* Validating fixes against requirements and acceptance criteria

#### 4.4.3 Artifacts
**Created:**
* *[Final Testing Summary Report](Final-Test-Summary-Report):* Created by the QA Engineer at the conclusion of the testing phase. This document summarizes testing activities, key findings, defect resolution, test coverage, and the overall readiness of the feature for deployment.

**Updated:**
* *[Test Plan](Test-Plan):* Updated as necessary to reflect changes in scope or testing progress.

### 4.5 Deployment
During deployment, the test strategy should be revisited for final validation. This includes performing user acceptance testing (UAT), smoke tests, or post-deployment validation to ensure the feature works as expected in the production environment. Any lessons learned from previous testing can be used to update the strategy for future deployments.

#### 4.5.1 Involved Team Members
* ***Product Owner:*** Ensures that the product vision and user stories are clear and understood, supporting the development and testing alignment.
* ***QA Engineer:*** Conducts post-deployment testing, including smoke tests, UAT (User Acceptance Testing), and ensures that no critical issues are introduced in production. 
* ***Developers:*** Monitor deployment for issues, address any post-deployment bugs, and help validate production stability.
* ***Engineering Manager:*** Helps resolve any blockers, facilitating team collaboration between developers and QA engineers.

#### 4.5.2 Key Activities
* Running post-deployment tests (smoke/UAT).
* Monitoring production environment behavior.
* Ensuring successful feature launch.

#### 4.5.3 Artifacts
**Used**
* *[Final Testing Summary Report](Final-Test-Summary-Report):* Presented to stakeholders to confirm testing completion and feature readiness for deployment.

### 4.6 Maintenance
Even after the feature is deployed, the test strategy may need to be updated for ongoing maintenance and future updates. Regression testing, performance monitoring, and support for any new features or patches should be part of the ongoing testing strategy. The strategy should be revisited to ensure continued alignment with evolving business and technical needs.

#### 4.6.1 Involved Team Members
* ***Product Owner:*** Determines if additional testing is needed for new user stories or bug fixes based on customer feedback.
* ***QA Engineer:*** Handles regression testing, monitors production performance, and ensures that any new updates or changes are adequately tested.
* ***Developers:*** Work with the QA engineer to address any bugs or issues identified in the maintenance phase and ensure that new code changes do not affect existing functionality.
* ***Engineering Manager:*** Facilitates continuous improvement and retrospective discussions to refine the testing process.

#### 4.6.2 Key Activities
* Regression testing for new updates.
* Monitoring system performance.
* Addressing bugs and feedback.
  
#### 4.6.3 Artifacts
**Updated**
* *[Test Plan](Test-Plan):* Modified to reflect changes for ongoing testing of new updates or patches.

* *[Final Testing Summary Report](Final-Test-Summary-Report)* Updated as needed for new features or patches.
