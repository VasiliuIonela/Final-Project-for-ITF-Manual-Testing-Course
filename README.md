# Final-Project-for-ITF-Manual-Testing-Course Guru99 Bank application
The scope of the final project for ITF Manual Tesing Course is to use all gained knowledge through the course and apply them in practice, using a live application.

Application under test: [guru99Bank](https://demo.guru99.com/V4/index.php).
 
 Documentation: [doc](https://docs.google.com/document/d/1rPW5DV82VJT6vtA1VDSrfxaCBuAduxW0zb1yfTh_VMk/edit).
 
 **The final project will be split into 2 sections:** [Testing section](https://github.com/VasiliuIonela/Final-Project-for-ITF-Manual-Testing-Course/blob/main/README.md#1-testing-section) **and** [SQL section](https://github.com/VasiliuIonela/Final-Project-for-ITF-Manual-Testing-Course/blob/main/README.md#2-sql-section).
 
 Tools used: JIRA, Zephyr Squad, mySQL.
 # Functional specifications
The below Story was created in JIRA and describes the functional specifications of the  role of Manager, for which the final project is performed upon.

As a Manager, I want to be able to access all customers account.

**Description:**
* The Manager account can be accessed after login.
* On the left you can see all the modules that Managers can access and edit.
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
 * 80% of requirements coverage has been achieved.
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
 * Project risks: the development team wont’t have the necessary training for these tasks, the database won’t support such a high volume of data, short deadline, not-compliance with the rules regulated in the banking field, sick personnel,few team members, misunderstanding of the requirements. 
 * Product risks: Security risk-data leak, low performance of the Guru99 bank application, not having requests for using such bank application, appplication may crash. 
 ### 1.1.6 Evaluating entry criteria
 The entry criteria defined in the Test Planning phase have been achieved and the test process can continue.
  ## 1.2 Test Monitorig and Control
 Periodic reports were generated to reflect the current status of the testing process, in case of major problems, control measures could be taken.
  ## 1.3 Test Analysis
 The testing process will be executed, based  on the requirements  sent by the client, for the account of Manager modules. The following **test conditions** were found:
 
 * Check if a user is able to login into Manager role, when valid data is entered.
 * Check if a user is able to login into Manager role, when invalid data is entered.
 * Check if a user can Logout form application.
 * Check if a user is able to access "reset" buton functionality.
 
 **When  module New Customer is selected:**

 * Check if a Manager is able to add a new customer when valid data is entered.
 *  Check if a Manager is able to add a new customer when invalid data is entered.
 *  Check if a Manager is able to add a new customer when fields are left in blank.
 *  Check if a Manager is able to add a new customer when special characters are entered into the fields.
 *   Check if a Manager is able to add a new customer when valid first character entered into fields is 'space'.
 *   Check if a Manager is able to add a new customer when characters are entered into 'Pin' field.
 * Check if a Manager is able to add a new customer when   less than 6 digites are entered into 'Pin' field.
 * Check if a Manager is able to add a new customer when   moere than 6 digites are entered into 'Pin' field.
 *  Check if a Manager is able to add a new customer when characters are entered into 'Telephone number' field.   
 *   Check if a Manager is able to use the reset button functionality.
 *   Check if a Manager is able to add a new customer when a date of birth in the future is entered into the specific field.
 
**When module Edit Customer is selected:** 
* Check if  a Manager is able to edit customer details when valid customer id is entered.
* Check if  a Manager is able to edit customer details when invalid customer id is entered.
* Check if  a Manager is able to edit customer details when field is left in blank.
* Check if  a Manager is able to edit customer details when characters are entered into the customer id field.

**When module Detele Customer is selected:**
* Check if a Manager is able to delete customer when valid customer id is entered and has no account.
* Check if a Manager is able to delete customer when valid customer id is entered and has an existing account.
*  Check if a Manager is able to delete customer when invalid customer id is entered.
*   Check if a Manager is able to delete customer when customer id is left in blank.

**When module New Account is selected:**
* Check is a Manager is able to add new account for an existing customer.
* Check is a Manager is able to add new account for a customer that doesn't exist.
* Check is a Manager is able to add new account when fields are left in blank.

**When module Edit Account is selected:**
* Check if a Manager is able to edit account details for an existing account.
* Check is a Manager is able to edit account details when invalid data is entered into the field.
*  Check is a Manager is able to edit account details when characters are entered into the field.

**When module Delete Account is selected:**
* Check if a Manager is able to delete an account for an existing customer by using a valid account number.
* Check if a Manager is able to delete an account for an existing customer by using an invalid account number.
* Check if a Manager is able to delete an account for an existing customer when field is left in blank.

**When module Deposit is selected:**
* Check if a manager is able to deposit money into any account, when valid data is entered.
* Check if a manager is able to deposit money into any account, when valid data is entered.
* Check if a manager is able to deposit money into any account, when fields are left in blank.

**When module Withdrawal is selected:**
* Check if a Manager is able to withdraw money from any account, when valid data is entered.
*  Check if a Manager is able to withdraw money from any account, when invalid data is entered.
* Check if a Manager is able to withdraw money from any account, when fields are left in blank.

**When module Fund Transfer is selected:**
* Check if a Manager is able to transfer funds from any source bank account to a destination account, when valid data is entered.
* Check if a Manager is able to transfer funds from any source bank account to a destination account, when invalid data is entered.


**When module Change Passsword is selected:**
* Check if a Manager is able to generate new password for his own account.
* Check if a Manager is able to change password for an existing account of a customer.

**When module Balance Enquiry is selected:**
* Check if a Manager is able to iew balance for a customer who came under supervision, by using valid account number.
* Check if a Manager is able to iew balance for a customer who came under supervision, by using invalid account number.
* Check if a Manager is able to iew balance for a customer who came under supervision, when field is left in blank.

**When module Mini Statement is selected:**
* Check if  a Manager is able to access last 5 transactions of any account when valid number account is entered.
* Check if  a Manager is able to access last 5 transactions of any account when invalid number account is entered.
*  Check if  a Manager is able to access last 5 transactions of any account when field is left in blank.

**When module Customized Statement is selected:**
* Check if a Manager is able to filter transactions in any account based on date, transaction value.
* Check if a Manager is able to display transactions in any account based on date, transaction value.


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
 
