# Reqres-API-Testing
Performed API testing on Reqres mock API using Postman. 
Tested multiple HTTP methods (GET, POST, PUT, DELETE) and implemented automated validation of responses using Postman scripts.
This is the website https://reqres.in/
==================================>


1-LIST USERS 
endpoint==> /api/users?page=2  Response=200 Method=>GET
Test cases:

a-Checking response time is less than 500ms(Ensure the API responds within an acceptable time frame.)

b-Check status code is 200

c-Check that the total pages is equal to 2

d-Check Data Types(Validate that specific fields in the response have the correct data types.)

e-Check if Data Array is Not Empty(Confirm that the data array is not empty and contains user records.)

f-Check Specific Fields in the Response (Validate the expected fields in each user object (e.g.,id, email, first_name, last_name).)

g-Validate Email Format(Check if each user's email is in the correct format.)

h-Verify the Avatar URL is Reachable(Ensure the avatar URLs are valid and return an OK response.)

i-Check the Support Text and URL(Validate that the support section contains the correct URL and text.)

j-Verify Pagination Logic(Validate that the page number is correct and matches the total_pages logic.)

k-Check Unique Email IDs(Ensure all users in the data array have unique email IDs (helps to ensure data integrity).)

l- Check if All Users Have Avatars(Confirm each user has a valid avatar URL.)

m-Test for the Correct HTTP Method(Verify that the correct HTTP method is used for the request (in this case, it should be a GET request).)

n-Validate Pagination Fields(Ensure that page, per_page, total, and total_pages fields are consistent and correctly calculated.)

o-Verify Length of data Array(Check if the number of users returned in the data array matches the per_page value.)

p-Check for Missing or Null Fields(Ensure there are no null or missing values for critical fields such as id, email, first_name, last_name, and avatar.)

q-Check that number of page is equal to 2

========================================================================================================================================================

2-SINGLE USER 

endpoint==> /api/users/2  Response=200   Method=>GET

Test cases:
a-Checking response time is less than 500ms(Ensure the API responds within an acceptable time frame.)
b-Check status code is 200
c-Check the Support Text and URL(Validate that the support section contains the correct URL and text.)
d-Check Content-Type Header(Ensure the response is in JSON format by validating the Content-Type header.)
e-Check Specific Fields Exist(Confirm that the required fields exist in both the data and support objects.)
f- Check if ID Matches the Expected Value(If you expect a specific id value, you can test that it matches.)
g-Check for Null or Empty Fields(Ensure that none of the important fields in the data object are null or empty.)
h-Check Avatar URL Format(Confirm that the avatar field contains a valid URL.)
i-Validate Email Format(Ensure the email field has a valid format.)
j-Check Field Data Types(Verify that the data fields have the correct types.)

========================================================================================================================================================
3-SINGLE USER NOT FOUND
endpoint==> /api/users/23  Response=404   Method=>GET
Test cases:
a-Checking response time is less than 500ms(Ensure the API responds within an acceptable time frame.)
b-Check status code is 404
c-Check Response Body is Empty(Ensure the response body is an empty object ({})).
d-Check Content-Type Header(Ensure the response is in JSON format by validating the Content-Type header.)
e-Check Response Body is Not Null(Even though the body is empty, it should not be null. You can check that it returns an empty object instead of null or something else.)
f-Check no additional data fields are present.

========================================================================================================================================================
4-List <resource>
endpoint==> /api/unknown  Response=200   Method=>GET
Test cases:
a-Checking response time is less than 500ms(Ensure the API responds within an acceptable time frame.)
b-Check status code is 200
c-Check that total pages is equal to 2
d-Check Data Types(Validate that specific fields in the response have the correct data types.)
e-Check for Missing or Null Fields(Ensure there are no null or missing values for critical fields such as id,name, year, color and pantone_value.)
f-Check Specific Fields in the Response (Validate the presence of expected fields in each user object (e.g.id,name, year, color and pantone_value.)
g-Validate data type(Check if data is in the correct type'array'.)
h-Check the data is not empty
i-Check the Support Text and URL(Validate that the support section contains the correct URL and text.)
j-Verify Pagination Logic(Validate that the page number is correct and that it matches the total_pages logic.)
k-Test for the Correct HTTP Method(Verify that the correct HTTP method is used for the request (in this case, it should be a GET request).)
l-Validate Pagination Fields(Ensure that page, per_page, total, and total_pages fields are consistent and correctly calculated.) 
m-Verify correct number of users per page
n-Check the data field types
o-Check Unique IDs in Data Array(Ensure that all id values in the data array are unique.)
p-Check Color Format(Ensure that the color field in each object has a valid hex format (i.e., it starts with # and is followed by 6 characters).)
q-Check Content-Type Header(Validate that the Content-Type header is set to application/json.)
r-Ensure No Duplicate Pantone Values(Ensure that the pantone_value is unique across all items in the data array.)
s-Check Per Page Value(Ensure that the number of items per page is 6.)
t-Check Total Items(Validate that the total number of items is 12.)

========================================================================================================================================================
5-SINGLE <RESOURCE> 
endpoint==> /api/unknown/2  Response=200   Method=>GET
Test cases:
a-Checking response time is less than 500ms(Ensure the API responds within an acceptable time frame.)
b-Check status code is 200
c-Check the Support Text and URL(Validate that the support section contains the correct URL and text.)
d-Check Content-Type Header(Ensure the response is in JSON format by validating the Content-Type header.)
e-Check Specific Fields Exist(Confirm that the required fields exist in both the data and support objects.)
f- Check if ID Matches the Expected Value(If you expect a specific id value, you can test that it matches.)
g-Check for Null or Empty Fields(Ensure that none of the important fields in the data object are null or empty.)
h-Check Field Data Types(Verify that the data fields have the correct types.)

========================================================================================================================================================
6-SINGLE <RESOURCE> NOT FOUND
endpoint==> /api/unknown/23  Response=404   Method=>GET
Test cases:
a-Checking response time is less than 500ms(Ensure the API responds within an acceptable time frame.)
b-Check status code is 404
c-Check Response Body is Empty(Ensure the response body is an empty object ({})).
d-Check Content-Type Header(Ensure the response is in JSON format by validating the Content-Type header.)
e-Check Response Body is Not Null(Even though the body is empty, it should not be null. You can check that it returns an empty object instead of null or something else.)
f-Check no additional data fields are present

========================================================================================================================================================
7-CREATE
endpoint==> /api/users  Response=201   Method=>POST
Test cases:
a-Checking response time is less than 500ms(Ensure the API responds within an acceptable time frame.)
b-Check status code is 201
c- Verify that the response body contains the correct data, including the name, job, id, and createdAt fields.
d-Verify that the fields have the correct data types
e-Check Content-Type Header(Ensure the response is in JSON format by validating the Content-Type header.)
f-Validate that the createdAt field is in ISO 8601 format
g-Check Name in request matchs the response
h-Check Job in request matchs the response
i-Check createdAt in response matches the time in computer

=======================================================================================================================================================
8-UPDATE
endpoint==> /api/users/2  Response=200   Method=>PUT
Test cases:
a-Checking response time is less than 500ms(Ensure the API responds within an acceptable time frame.)
b-Check status code is 200
c- Verify that the response body contains the correct data, including the id, and updatedAt fields.
d-Verify that the fields have the correct data types
e-Check Content-Type Header(Ensure the response is in JSON format by validating the Content-Type header.)
f-Validate that the createdAt field is in ISO 8601 format
g-Check Name in request matchs the response
h-Check Job in request matchs the response
i-Check createdAt in response matches the time in computer

=======================================================================================================================================================
9-UPDATE
endpoint==> /api/users/2  Response=200   Method=>PATCH
Test cases:
a-Checking response time is less than 500ms(Ensure the API responds within an acceptable time frame.)
b-Check status code is 200
c- Verify that the response body contains the correct data, including  id, and updatedAt fields.
d-Verify that the fields have the correct data types
e-Check Content-Type Header(Ensure the response is in JSON format by validating the Content-Type header.)
f-Validate that the createdAt field is in ISO 8601 format
g-Check Name in request matchs the response
h-Check Job in request matchs the response
i-Check createdAt in response matches the time in computer

=======================================================================================================================================================
10-DELETE
endpoint==> /api/users/2  Response=204   Method=>DELETE
Test cases:
a-Checking response time is less than 500ms(Ensure the API responds within an acceptable time frame.)
b-Check status code is 200
c- Verify that the response body empty.
d-Check Content-Length Header(Ensure the response is 0 by validating the Content-Length header.)

=======================================================================================================================================================
11-REGISTER-SUCCESSFUL
endpoint==> /api/register  Response=200   Method=>POST
Test cases:
a-Checking response time is less than 500ms(Ensure the API responds within an acceptable time frame.)
b-Check status code is 200
c- Verify that the response body contains the correct data, including the  id, and token fields.
d-Verify that the fields have the correct data types in response.
e-Check Content-Type Header(Ensure the response is in JSON format by validating the Content-Type header.)
f-Check required fields of data in request (email,password)
g-Check the data field types in request
h-Check the correct format of email

========================================================================================================================
12-REGISTER-UNSUCCESSFUL
endpoint==> /api/register  Response=400   Method=>POST
Test cases:
a-Checking response time is less than 500ms(Ensure the API responds within an acceptable time frame.)
b-Check status code is 400
c- Verify that the response body contains error message.
d-Check Content-Type Header(Ensure the response is in JSON format by validating the Content-Type header.)
e-Check required fields of data in request (email)
f-Check the data field types in request
g-Check the correct format of email

========================================================================================================================
13-LOGIN-SUCCESSFUL
endpoint==> /api/login  Response=200   Method=>POST
Test cases:
a-Checking response time is less than 500ms(Ensure the API responds within an acceptable time frame.)
b-Check status code is 200
c- Verify that the response body contains the correct data, including the token field.
d-Verify that the fields have the correct data types
e-Check Content-Type Header(Ensure the response is in JSON format by validating the Content-Type header.)
f-Check required fields of data in request (email,password)
g-Check the data field types in request
h-Check the correct format of email

========================================================================================================================
14-LOGIN-UNSUCCESSFUL
endpoint==> /api/login  Response=400   Method=>POST
Test cases:
a-Checking response time is less than 500ms(Ensure the API responds within an acceptable time frame.)
b-Check status code is 400
c- Verify that the response body contains error message.
d-Check Content-Type Header(Ensure the response is in JSON format by validating the Content-Type header.)
e-Check required fields of data in request (email)
f-Check the data field types in request
g-Check the correct format of email

========================================================================================================================
15-DELAYED RESPONSE
endpoint==> /api/users?delay=3  Response=200 Method=>GET
Test cases:
a-Checking response time is less than 3500ms(Ensure the API responds within an acceptable time frame.)
b-Check status code is 200
c-Check that total pages is equal to 2
d-Check Data Types(Validate that specific fields in the response have the correct data types.)
e-Check if Data Array is Not Empty(Confirm that the data array is not empty and contains user records.)
f-Check Specific Fields in the Response (Validate the presence of expected fields in each user object (e.g.,id, email, first_name, last_name).)
g-Validate Email Format(Check if each user's email is in the correct format.)
h-Verify the Avatar URL is Reachable(Ensure the avatar URLs are valid and return a OK response.)
i-Check the Support Text and URL(Validate that the support section contains the correct URL and text.)
j-Verify Pagination Logic(Validate that the page number is correct and that it matches the total_pages logic.)
k-Check Unique Email IDs(Ensure all users in the data array have unique email IDs (helps to ensure data integrity).)
l- Check if All Users Have Avatars(Confirm that each user has a valid avatar URL.)
m-Test for the Correct HTTP Method(Verify that the correct HTTP method is used for the request (in this case, it should be a GET request).)
n-Validate Pagination Fields(Ensure that page, per_page, total, and total_pages fields are consistent and correctly calculated.)
o-Verify Length of data Array(Check if the number of users returned in the data array matches the per_page value.)
p-Check for Missing or Null Fields(Ensure there are no null or missing values for critical fields such as id, email, first_name, last_name, and avatar.)
q-Check that number of page is equal to 1

========================================================================================================================================================

using newman run the collection 
