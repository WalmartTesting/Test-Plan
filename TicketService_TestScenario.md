
Table of Contents
Introduction/Test objective:	1
Assumptions:	1
Environment Details:	1
Entrance Criteria:	1
System Testing:	2
Test Scenario:	2
Test cases:	4
Exit Criteria:	6
Testing tool suggested	6

INTRODUCTION/TEST OBJECTIVE:
The test objective is to determine if the developed software satisfies the business requirements. The main focus in this phase is to validate the following functionalities / Use cases:
UC001.	Number of seats available within the venue
UC002.	Hold the best available seats on behalf of a customer
UC003.	Reserve and commit a specific group of held seats for a customer

ASSUMPTIONS:
1.	Functional requirements are locked and there are no changes involved during the testing phase.
2.	Ticket service software does not involve a GUI component or an API interface.
3.	The level’s, price, rows and the seats in row remain constant as stated in the below table:
 
4.	The wait time to hold the reservation is set to be 5 minutes
5.	Email id of the customer is the unique identifier to the system.
6.	The customer can either login to discover, hold and reserve the seats or need to login at the point when they are ready to reserve the seats.
7.	Credit or Debit is the mode of payment
8.	Table structures to hold the customer details, status of seats are defined.
9.	STATUS will be the column that will hold the current status of the seats (FREE,HOLD,RESERVED)

ENVIRONMENT DETAILS:
The software is developed using JAVA and Oracle or any other Data base as a backend.

ENTRANCE CRITERIA:
•	Ticket Service software meets all the Hardware / Software requirements.
•	The final code is available for QA deployment before the initiation of testing cycle.
•	Unit testing have been conducted and results inspected.
•	Test data have been mapped to the scenarios designed.

SYSTEM TESTING:
System testing will focus on testing the functional requirements through the test scenarios designed. Testing techniques are selected based on the scenarios concluded for the application and they encompass Active testing, Agile testing, Age testing, Assertion testing, All – pair testing, Basis path testing

TEST SCENARIO:

UC001: Number of seats available within the venue

Scenario ID	Scenario description
TSD001.		Validate that the customer is given the choice to view the available seats across all levels or a specific seating level.
TSD002.		Validate that the customer inputs a valid Level to view the seating details.
TSD003.		Validate that the correct number of seats available are retrieved for a given seating level
TSD004.		Validate when 2 or more customers are accessing the same details, the seats held by one customer are not available for the             other customer.


UC002: Hold the best available seats on behalf of a customer

Scenario ID	Scenario description
TSH001.		Validate that the customer chooses only the seats that are not already reserved or on hold.
TSH002.		Validate that the customer is able to select more than 1 available seat across different rows and different levels
TSH003.		Validate that the seats are held only during the ‘wait time’ and are released after the time expires.

UC003: Reserve and commit a specific group of held seats for a customer

Scenario ID	Scenario description
TSR001.		Validate that the customer’s email id is already available; if not request before reserving.
TSR002.		Validate that the customer selects a valid payment option to reserve the seats.
TSR003.		Validate that the customer reserves the held seats within the ‘wait time’
TSR004.		Validate that once the customer reserves the held seats, they are committed.

TEST CASES:
Scenario ID	Test case ID	Test case Name	Test case Description	Test Step #	Test Description	Expected Result	Path Covered by Test Case

 
EXIT CRITERIA:

TESTING TOOL SUGGESTED
