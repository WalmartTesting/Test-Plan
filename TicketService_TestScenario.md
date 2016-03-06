INTRODUCTION/TEST OBJECTIVE:
============================

The test objective is to determine if the developed software satisfies the business requirements. The main focus in this phase is to validate the following functionalities / Use cases:

1.  Number of seats available within the venue

2.  Hold the best available seats on behalf of a customer

3.  Reserve and commit a specific group of held seats for a customer

ASSUMPTIONS:
============

1.  Functional requirements are locked and there are no changes involved during the testing phase.

2.  Technical design review has been completed and approved.

3.  The level’s, price, rows and the seats in row remain constant as stated in the below table:

    <embed src="media/image1.emf" width="538" height="213" />

4.  The wait time to hold the reservation is set to be 5 minutes

5.  Email id of the customer is the unique identifier to the system.

6.  The customer can either login to discover, hold and reserve the seats or need to login at the point when they are ready to reserve the seats.

7.  Credit or Debit is the mode of payment

8.  Table structures to hold the customer details, status of seats are defined.

9.  ‘STATUS’ will be the column that will hold the current status of the seats (FREE,HOLD,RESERVED)

ENVIRONMENT DETAILS:
====================

The software is developed using JAVA and a RDBMS.

ENTRANCE CRITERIA:
==================

-   Ticket Service software meets all the Hardware / Software requirements.

-   The final code is available for QA deployment before the initiation of testing cycle.

-   Unit testing have been conducted and results inspected.

-   System test plan have been approved and signed off.

-   Test data have been mapped to the scenarios designed.

SYSTEM TESTING:
===============

System testing will focus on testing the functional requirements through the test scenarios designed. Testing techniques are selected based on the scenarios concluded for the application and they encompass Active testing, Agile testing, Age testing, Assertion testing, All – pair testing, Basis path testing.

<img src="media/image2.png" width="623" height="888" />

TEST SCENARIO:
==============

UC001: Number of seats available within the venue

| **Scenario ID** | **Scenario description**                                                                                                                |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| TSD001.              | Validate that the customer is given the choice to view the available seats across all levels or a specific seating level.               |
| TSD002.              | Validate that the customer inputs a valid Level to view the seating details.                                                            |
| TSD003.              | Validate that the correct number of seats available are retrieved for a given seating level                                             |
| TSD004.              | Validate when multiple customers are accessing the same details, the seats held by one customer are not available for another customer. |

> UC002: Hold the best available seats on behalf of a customer

| **Scenario ID** | **Scenario description**                                                                                         |
|-----------------|------------------------------------------------------------------------------------------------------------------|
| TSH001.              | Validate that the customer chooses only the seats that are not already reserved or on hold.                      |
| TSH002.              | Validate that the customer is able to select 1 or more available seat across different rows and different levels |
| TSH003.              | Validate that the seats are held only during the ‘wait time’ and are released after the time expires.            |

UC003: Reserve and commit a specific group of held seats for a customer

| **Scenario ID** | **Scenario description**                                                                                                                  |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| TSR001.              | Validate that the customer’s email id is already available; if not request before reserving.                                              |
| TSR002.              | Validate that the customer selects a valid payment option which should include the credit / debit number validation to reserve the seats. |
| TSR003.              | Validate that the customer reserves the held seats within the ‘wait time’ and the reservation is committed                                |

TEST CASES:
===========

| **Scenario ID**   | **Test case ID**   | **Test case Name**                 | **Test case Description**                                                                                                                  | **Test Step \#**   | **Test Description**                                                                                                   | **Expected Result**                                                                                                                                                                    | **Path covered**                  |
|-------------------|--------------------|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|


EXIT CRITERIA:
==============

-   All the functional requirements are tested successfully

-   All the defects logged during the testing phase have a fix and have been successfully retested and closed.

-   IT Evidence of the test scenarios are collected and inspected

-   Results are incorporated in to Test summary report

TESTING TOOL SUGGESTED
======================

Selenium is the suggested testing tool that can be used for automation testing as it’s adaptable to any changes that might be introduced in the requirements. Data driven / Module based framework would best suit this application.
