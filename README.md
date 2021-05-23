Credit Card Processing

Write a small full stack application for a credit card provider. It should allow you to add new credit card accounts and view them as a list. The backend must be a RESTful API.

Requirements

Two REST Endpoints must be implemented
"Add" will create a new credit card for a given name, card number, and limit
oCard numbers should be validated using Luhn 10
oNew cards start with a £0 balance
ofor cards not compatible with Luhn 10, return an error
"Get all" returns all cards in the system

The endpoints should be given appropriate URLs and HTTP methods, according to RESTful design principles. There is no right and wrong answer here, but you may be asked to explain and justify your design, so give it some thought.

Validation

All input and output will be JSON
Credit card numbers may vary in length, up to 19 characters
Credit card numbers will always be numeric

Technical requirements

Create the RESTful API using Spring Boot and Use Maven/Gradle for dependency management
Create the endpoints use appropriate HTTP Methods and define the payloads, return codes and response structures
Write unit test cases, though please note that we’re looking for quality over quantity – coverage does not need to be high
Use an in-memory DB to store the information while the API is running, so that it can store the credit card information
Hand code the Luhn 10 check, don’t use a library

========================================

CreditCard POJO with 4 attributes 

private String cardUserName;
private Long cardNumber
private Date validTill;
private Long cardLimit = 0L;
private String cardType;


I have used Lombok, JAVA 11
I have developed one creditservice service, which has two methods
	- getAllCards()
	- saveCard(CC pojo) payload should be used while inserting new cc details.
	
	
Code includes :-

1. CC Service
2. Service Registry
3. API Gateway
4. Hystrix Dashboard
5. Cloud Config server
6. Zipkin and Sleuth


I have taken help of "start.spring.io" for generating the various modules and added all the required dependencies using the same.
The API development is done based on microservices design pattern, where I can do individual developments in the respective modules.

NOTE :-
I am currently working in my office network (CITIBANK), where its very strict to share the code and files.
I tried installing eclipse in my local laptop, but it took lot of time and i was unsuccessful in installing and setting up the environment for this assignment.
I have tested this code in postman in my citi network. 
I can explain each and every line of code, if you are unable to understand anything. 
As the time allotted to me was very less, i could not implement the Luhn 10 algorithm in my code, but it can be done in service layer also along with few more validations too. 