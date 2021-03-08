# MessageBoardAPI

1) Architectural style  - Domain-Driven-Design (Model, Repository , AppService)

2) Design Pattern - Dependency Injection

3) In-memory solution - Microsoft.EntityFrameworkCore.InMemory

4) Open api specification - Swagger

5) Used  LINQ for Data Operation

6) Used dynamic object and Newtonsoft to process JSON data.

7) Unit Test - xUnit Test Project Template


8)Message CURD operation has been define with four different operation


a) GetByID Message

URL -/api/Message/GetById<Use the same messageID as you get it in response of saving a data>  
HTTP Verb - GET
Header
Key-UserID
Value-monosrizdutta@gmail.com (Sample data)


b) Get All Message

URL -/api/Message/GetAllMessages 
HTTP Verb - GET
Header
Key-UserID
Value-monosrizdutta@gmail.com (Sample data)
---------------------------------------------------
c) Save a New Message

URL -/api/Message/Create 
HTTP Verb - POST
Header
Key-UserID
Value-monosrizdutta@gmail.com (Sample data)

Body (Sample Data)

{
  
    "subject": "Status",
    "text": "What is the project status?"
    
}
----------------------------------------------------
d) Update a New Message (Only Owner can update the message- - Based on Header Value)

URL -/api/Message/Update 
HTTP Verb - PUT
Header
Key-UserID
Value-monosrizdutta@gmail.com (Sample data)

Body (Sample Data)

{
  "messageID": "Use the same messageID as you get it in response of saving a data",
   "subject": Status",
   "text": "IS the task1 completed?"
    
}
------------------------------------------------------
e) delete a New Message (Only Owner can delete the message- Based on Header Value)

URL -/api/Message/Delete/<Use the same messageID as you get it in response of saving a data> 
HTTP Verb - DELETE
Header
Key-UserID
Value-monosrizdutta@gmail.com (Sample data)
