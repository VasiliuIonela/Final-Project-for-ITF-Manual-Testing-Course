# Final-Project-for-ITF-Manual-Testing-Course Guru99 Bank application
The scope of the final project for ITF Manual Tesing Course is to use all gained knowledge through the course and apply them in practice, using a live application.

Application under test: https://demo.guru99.com/V4/index.php
 
 Documentation: https://docs.google.com/document/d/1rPW5DV82VJT6vtA1VDSrfxaCBuAduxW0zb1yfTh_VMk/edit
 
 **The final project will be split into 2 sections:** [Testing section](https://github.com/VasiliuIonela/Final-Project-for-ITF-Manual-Testing-Course/blob/main/README.md#1-testing-section) **and** [SQL section](https://github.com/VasiliuIonela/Final-Project-for-ITF-Manual-Testing-Course/blob/main/README.md#2-sql-section).
 
 Tools used: JIRA, Zephyr Squad.
 # Functional specifications
The below Story was created in JIRA and describes the functional specifications of the  role of Manager, for which the final project is performed upon.

As a Manager, I want to be able to access all customers account.

**Description:**
* The Manager account can be accessed after login.
* On the left you can see all the modules that Manager can access and edit.
* A Manager can Add New Customer  by clicking on the New Customer module. He can also edit details like adress, email, telephone of a customer.
* A Manager can Edit Customer and Delete Customer by using Customer ID. A customer can be deleted only if he/she has  no active current or saving accounts.
* A Manager can Add new account for an existing Customer. Currently system provides 2 types of accounts: ***Saving*** and  ***Current***

A customer can have multiple saving accounts (one in his name , other in a joint name etc). He can have multiple current accounts for different companies he owns. Or he can have a multiple current and saving accounts.
* A Manager can add an edit account details for an existing account.
* A Manager can add a delete an account for a customer.
* A Manager can deposit money into any account. Usually done when cash is deposited at a bank branch.
* A Manager can withdraw money from any account. Usually done when cash is withdrawn at a bank branch.
* A Manager can transfer funds from any source bank account to destination account.
* A manager can change password of only his account. He cannot change passwords of his customers.
* A manager can view balance of all the customers who come under his supervision.
*  A manager can see mini-statement of any account. A Mini statement will show last 5 transactions of an account.
*  A manager can see Customized -statement of any account. A customized statement allows you to filter and display transactions in an account based on date, transaction value. 
 # 1 Testing section 
 ## 1.1 Test Planning
This Test Plan is designed to access and verify the functionalities of existing modules in the role of Manager, such as: the option of adding a new customer, but also to edit and delete a customer, the option of creating new account for a customer(this will automated generate a customer id which is used in other fields, as: edit and delete account), the option that creates a new account for one specified customer, by its customer id(which will automated generate an account no), the option of editing and deleting an account, by using the account number, the options that allow to deposit, withdraw and also transfer funds,  from  the Guru99 Bank Application. 

The plan identifies the items to be tested, the features to be tested, the types of testing to be performed, the personnel responsible for testing, the resources and schedule required to complete testing, and the risks associated with the plan. 
 ### 1.1.1 Roles asigned to the project and persons allocated
 * Project manager:
 * QA Lead:
 * QA Tester: Ionela Vasiliu
 ### 1.1.2 Entry criteria defined
* roles needed for the project are allocated.
* Initial project risks were detected and mitigated. 
* functional specifications are defined.

 ### 1.1.3 Exit criteria defined
 * A certain level of requirements coverage has been achieved.
 *  All tests have been executed.
* No high priority or severe bugs are left outstanding.
*  All resolved bugs have been re-tested and appoved bt the QA team.
* All high-risk areas have been fully tested, with only minor residual risks left outstanding.
* The schedule has been achieved. 
 ### 1.1.4 Test scope 
 * Tests in scope: The scope of this project is limited to the testing of the features in the succeeding sections of this document.
Functional testing  are in scope and needed to be tested.  Only web applications will be tested.
 * Tests out of scope: Non-functional testing like performance, security testing is beyond scope of this project.
No QA support for mobile application developed. Automation testing is beyond scope. 
 ### 1.1.5 Risks detected 
 * Project risks: the development team wont’t have the necessary training for these tasks, the database won’t support such a high volume of dates, short deadline, not-compliance with the rules regulated in the banking field, sick personnel, too little team members, too little team members, misunderstanding of the requirements. 
 * Product risks: Security risk-data leak, low performance of the Guru99 bank application, not having customer’s requests, appplication will crash. 
 ### 1.1.6 Evaluating entry criteria
 The entry criteria defined in the Test Planning phase have been achieved and the test process can continue.
  ## 1.2 Test Monitorig and Control
 Periodic reports were generated to reflect the current status of the testing process, in case of major problems, control measures could be taken.
  ## 1.3 Test Analysis
 The testing process will be executed, based  on the requirements  sent by the client, for the account of Manager modules. The following **test conditions** were found:
 * Check the login functionality when valid data is entered.
 * Check the login functionality when invalid user id or password is entered.
 * Check the reset button functionality.
 
 **When  module New Customer is selected:**
 * Check the Submit button functionality when valid data is entered.
 * Check the Submit button functionality when invalid data is entered.
 * Check the Submit button functionality when fileds are left in blank.
 * Check the system response when special characters are entered.
 * Check the system response when first character is 'space'.
 * Check the system response when characters are entered in 'Pin' field.
 * Check the system response when  less than 6 digits are entered in'Pin' field.
 * Check the system response when more than 6 digits are entered in ' Pin' field..
 * Check the system response when characters are entered in 'Telephone number' field.
 * Check the system response when less/more digits are entered in the 'Telephone number' field.
 * Check the Reset button functionality.
 * Check the system response when a date of birth in the future is entered.
 
**When module Edit Customer is selected:** 
* Check if the system   allows  to edit customer details by using its customer id.
* Check the Submit button functionality when valid customer id is entered.
* Check the Submit button functionality when field is left in blank.
* Check the Submit button functionalithy when characters are entered in customer id field.
**When module Detele Customer is selected:**
* Check the Submit button functionality when valid customer id is entered and has no account.
* Check the Submit button functionality when valid customer id is entered and has one or more accounts.
* Check the system response  when field ' Customer id' is left in blank.
* Check the system response when first character is 'space' in 'Customer id' field.
* Check the system response when invalid data is entered in 'Customer id' field.

**When module New Account is selected:**
* check if the system allows to add a new account for an existing customer.
* Check the Submit button functionality when valid data is entered.
*  Check the Submit button functionality when invalid data is entered.
*  Check the system response when 'Customer id' field is left in blank.
*  Check the system response when first character is'space' in 'Customer id' field.

**When module Edit Account is selected:**
* check if the system allows to edit account details for an existing account.
*  Check the Submit button functionality when valid number account is entered.
*  Check the Submit button functionality when field is left blank.
*  Check the Submit button functionality when invalid number account is entered.

**When module Delete Account is selected:**
* check if the system allows to delete an account for an existing customer.
*  Check the Submit button functionality when valid account number is entered.
*  Check the Submit button functionality when invalid number account is entered.
*  Check the system response when when field is left in blank.

**When module Deposit is selected:**
* Check if the system allows to deposit money into any account.
* Check the submit functionality when valid data is enetered.
* Check the submit functionality when invalid data is entered.
* Check the system response when fields are left in blank.

**When module Withdrawal is selected:**
* Check if the system allows to withdraw money from any account.
*  Check the submit functionality when valid data is enetered.
* Check the submit functionality when invalid data is entered.
*  Check the system response when fields are left in blank.

**When module Fund Transfer is selected:**///
* Check if the system allows to transfer funds from any source bank account to destination account.

**When module Change Passsword is selected:**///
*  check if the system allows to generate new password, only for own account.

**When module Balance Enquiry is selected:**
* Check if the system allows to view balance of all the customers who came under supervision.
* Check the system response when valid number account is entered.
* Check the system response when invalid number account is entered.
* Check the system response when field is left in blank.

**When module Mini Statement is selected:**
*  Check if the system allows to show last 5 transactions of any account.
*  Check the system response when valid number account is entered.
*  Check the system response when invalid number account is entered.
*  Check the system response when field is left in blank.

**When module Customized Statement is selected:**////
* Check if the system allows to filter and display transactions in any account based on date, transaction value. 
* Check the functionality of the button Logout.

 ## 1.4 Test Design
 Functional test cases were created in JIRA. Based on the analysis of the specifications, the test design techniques used for generating test case are:
 
 **Test cases:** 
 Test cases with steps can be viewes here: [test_cases](https://docs.google.com/spreadsheets/d/1ofxRgH47y4j9weSqSTBlmjeJh_g5X8Eg/edit#gid=349785068).
 ## 1.5 Test Implementation 
 The following elements are needed to be ready before the test execution phase begins:

* Testing environment is up and running:  https://demo.guru99.com/V4/index.php 
* Access to the testing environment is given: Username : mngr493941  | Password : YsYvyba
* Cycle summary was created
* Test cases were added to the cycle summary

 ## 1.6 Test Execution 
 * Test cases are executed on the created test Cycle summary:
 * Bugs have been created based on the failed tests. The complete bug reports can be found here:
 * Full regression testing is needed after the bugs are fixed.
 ## 1.7 Test Completion 
 One of the critical outcomes of the Test Completion phase is the test completion report. This report is the summary of all the testing efforts which execute during the testing process. The completion report is a crucial input to the stakeholders to determine the amount of testing accomplished. In addition to that, it also analyzes the unattended risks and issues. It helps them to make informed decisions about the software.

 # 2 SQL section
 
