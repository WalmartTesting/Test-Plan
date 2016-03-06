INTRODUCTION/TEST OBJECTIVE:
============================

The test objective is to determine if the developed software satisfies the business requirements. The main focus in this phase is to validate the following functionalities / Use cases:

1.  Number of seats available within the venue

2.  Hold the best available seats on behalf of a customer

3.  Reserve and commit a specific group of held seats for a customer

ASSUMPTIONS:
============

1.  Functional requirements are locked and there are no changes involved during the testing phase.

2.  *Ticket service software does not involve a GUI component or an API interface.*

3.  The level’s, price, rows and the seats in row remain constant as stated in the below table:

    <embed src="media/image1.emf" width="538" height="213" />

4.  The wait time to hold the reservation is set to be 5 minutes

5.  Email id of the customer is the unique identifier to the system.

6.  The customer can either login to discover, hold and reserve the seats or need to login at the point when they are ready to reserve the seats.

7.  Credit or Debit is the mode of payment

8.  Table structures to hold the customer details, status of seats are defined.

9.  STATUS will be the column that will hold the current status of the seats (FREE,HOLD,RESERVED)

ENVIRONMENT DETAILS:
====================

The software is developed using JAVA and Oracle or any other Data base as a backend.

ENTRANCE CRITERIA:
==================

-   Ticket Service software meets all the Hardware / Software requirements.

-   The final code is available for QA deployment before the initiation of testing cycle.

-   Unit testing have been conducted and results inspected.

-   Test data have been mapped to the scenarios designed.

SYSTEM TESTING:
===============

System testing will focus on testing the functional requirements through the test scenarios designed. Testing techniques are selected based on the scenarios concluded for the application and they encompass Active testing, Agile testing, Age testing, Assertion testing, All – pair testing, Basis path testing

TEST SCENARIO:
==============

UC001: Number of seats available within the venue

| Scenario ID | Scenario description                                                                                                                       |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| 1.          | Validate that the customer is given the choice to view the available seats across all levels or a specific seating level.                  |
| 1.          | Validate that the customer inputs a valid Level to view the seating details.                                                               |
| 1.          | Validate that the correct number of seats available are retrieved for a given seating level                                                |
| 1.          | Validate when 2 or more customers are accessing the same details, the seats held by one customer are not available for the other customer. |
| 1.          | TEST SCENARIO                                                                                                                              |

> UC002: Hold the best available seats on behalf of a customer

| Scenario ID | Scenario description                                                                                               |
|-------------|--------------------------------------------------------------------------------------------------------------------|
| 1.          | Validate that the customer chooses only the seats that are not already reserved or on hold.                        |
| 1.          | Validate that the customer is able to select more than 1 available seat across different rows and different levels |
| 1.          | Validate that the seats are held only during the ‘wait time’ and are released after the time expires.              |
| 1.          | TEST SCENARIO 2                                                                                                    |

UC003: Reserve and commit a specific group of held seats for a customer

| Scenario ID | Scenario description                                                                         |
|-------------|----------------------------------------------------------------------------------------------|
| 1.          | Validate that the customer’s email id is already available; if not request before reserving. |
| 1.          | Validate that the customer selects a valid payment option to reserve the seats.              |
| 1.          | Validate that the customer reserves the held seats within the ‘wait time’                    |
| 1.          | Validate that once the customer reserves the held seats, they are committed.                 |

TEST CASES:
===========

| Scenario ID | Test case ID | Test case Name                     | Test case Description                                                                                              | Test Step \#  | Test Description                                                                                    | Expected Result                                                                                                                           | Path Covered by Test Case |
|-------------|--------------|------------------------------------|--------------------------------------------------------------------------------------------------------------------|---------------|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|---------------------------|
| TSH001      | TCH001a      | Verify Seat Selection              | Validate that the customer chooses only the seats that are not already reserved or on hold.                        | Pre-condition | Seat details are displayed as per the customer’s choice of level                                    |                                                                                                                                           |                           |
|             |              |                                    |                                                                                                                    | Step 1        | Customer selects the seat number from the specific level which are available (not held or reserved) | The selected seats are put on hold for the customer.                                                                                      
                                                                                                                                                                                                                                                                                                                                                                                                                                                         
                                                                                                                                                                                                                                                                                                              The status is flipped from ‘Free’ to ‘Hold’ in the backend                                                                                 |                           |
|             | TCH001b      | Verify Seat Selection              | Validate that the customer chooses only the seats that are not already reserved or on hold.                        | Pre-condition | Seat details are displayed as per the customer’s choice of level                                    |                                                                                                                                           |                           |
|             |              |                                    |                                                                                                                    | Step 1        | Customer selects the seat number from the specific level which are held or reserved                 | Customer is informed that “The selected seats are either reserved or on hold”                                                             |                           |
| TSH002      | TCH002       | Verify Multiple selection of seats | Validate that the customer is able to select more than 1 available seat across different rows and different levels | Pre-condition | All the available seats are displayed for customer selection                                        |                                                                                                                                           |                           |
|             |              |                                    |                                                                                                                    | Step 1        | Customer chooses multiple seats across different rows and different level                           | The selected seats are put on Hold for the customer for a preset time before he confirms his reservation.                                 
                                                                                                                                                                                                                                                                                                                                                                                                                                                         
                                                                                                                                                                                                                                                                                                              The status is flipped from ‘Free’ to ‘Hold’ in the backend                                                                                 |                           |
| TSH003      | TCH003       | Wait time                          | Validate that the seats are held only during the ‘wait time’ and are released after the time expires.              | Pre-Condition | Customer has selected the available seats displayed from the list                                   |                                                                                                                                           |                           |
|             |              |                                    |                                                                                                                    | Step 1        | Customer has chosen multiple seats across different levels                                          | 1.  Customer is informed that the selected seats will be held for them for only 5 minutes                                                 
                                                                                                                                                                                                                                                                                                                                                                                                                                                         
                                                                                                                                                                                                                                                                                                              2.  The timer is set on from the moment the customer has selected the seats and their status remains ‘Hold’ for a wait time of 5 minutes.  
                                                                                                                                                                                                                                                                                                                                                                                                                                                         
                                                                                                                                                                                                                                                                                                              3.  Once 5 minutes are exhausted, the customer is informed to discover available seats again                                               
                                                                                                                                                                                                                                                                                                                                                                                                                                                         
                                                                                                                                                                                                                                                                                                              4.  The status in the backend flips back to ‘Free’                                                                                         |                           |

EXIT CRITERIA:
==============

TESTING TOOL SUGGESTED
======================

<img src="media/image2.png" width="405" height="659" />
