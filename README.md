# Testing API with Postman - CRUD

You need to read the API documentation. 

We're using Simple Books API whose documentation can be found in the resources section of this link: https://github.com/vdespa/introduction-to-postman-course/blob/main/simple-books-api.md

# Endpoints

GET Method - get some data/request;

The API: https://simple-books-api.glitch.me


## 1. List of books ## GET

GET /books

Returns a list of books.
 
 2 optional query parameters:
- type: fiction or non-fiction;
- limit: a number between 1 and 20.
  
I also create a variable for the URL link {{baseURL}}. 

Status 200 - standard response for successful HTTP requests.

![GET list of books (2)](https://github.com/Strat-Bianca/TestingAPI-Postman/assets/119669189/b082479e-f322-47fe-b118-4e01d07d2d67)


## 2. Get a single book ## GET
GET /books/:bookId

Retrieve detailed information about a book with a specific Id. (bookId = 3)

Status 200 - standard response for successful HTTP requests.


![GET a single book](https://github.com/Strat-Bianca/TestingAPI-Postman/assets/119669189/eafbb0ca-7588-4e3f-9c46-cd125a91caa7)

## 3. Submit an order ## POST
POST /orders

We identify a book that we want to order, allows you to submit a new order, we are sending some data. 

Requires authentication.
Authorization: Bearer Tooken -  we register ourself with an API client.

The request body needs to be in JSON format and include the following properties:

- bookId - Integer - (Required)
- customerName - String - (Required)
  
 The response body will contain the order Id.
 
"201 Created" is a standard response status code that indicates a successful creation of a new resource on the server.

![POST order a book](https://github.com/Strat-Bianca/TestingAPI-Postman/assets/119669189/3199d6bc-28da-4885-b4ed-b7cf8c13ab1d)

## 4. Get all orders ## GET
GET /orders 

Allows you to view all orders. Requires authentication.

Status 200 - standard response for successful HTTP requests.


![GET all books order](https://github.com/Strat-Bianca/TestingAPI-Postman/assets/119669189/b1e5649d-02b6-493d-b7d8-40c9dd4e5dc4)

## 5. Get an order ##  GET
GET /orders/:orderId

Allows you to view an existing order. Requires authentication.

Status 200 - standard response for successful HTTP requests.

![GET an order](https://github.com/Strat-Bianca/TestingAPI-Postman/assets/119669189/e07bcb2b-42cc-4642-836e-a916515fbb44)

## 6. Update an order ## PATCH
PATCH /orders/:orderId

Update an existing order. Requires authentication.

The request body needs to be in JSON format and allows you to update the following properties:

- customerName - String

Status 204 - the server successfully performs the requested action, but there is no new information to be sent back to the client.

![PATCH](https://github.com/Strat-Bianca/TestingAPI-Postman/assets/119669189/2e76842f-d7ba-4121-a12a-fc39090a5ef3)


## 7. Delete an order ## DELETE
DELETE /orders/:orderId

DELETE method to remove a specific book from the collection by sending a DELETE request to the API endpoint representing that book.
Delete an existing order. Requires authentication. 

Authorization: Bearer Token

The request body needs to be empty.

![PATCH update-order](https://github.com/Strat-Bianca/TestingAPI-Postman/assets/119669189/49efc6ba-e0aa-45e8-89b0-dacf40713290)


## 8. API Authentication ## POST
To submit or view an order, you need to register your API client.

POST /api-clients/

The request body needs to be in JSON format and include the following properties:

clientName - "Postman"

clientEmail - "strat.bianca@yahoo.com"
 
   # 1.1  ![POST register API client](https://github.com/Strat-Bianca/TestingAPI-Postman/assets/119669189/6d26d22b-c170-4ab8-a329-c8341cc3f1f6)

   #  1.2  ![POST register API client-2](https://github.com/Strat-Bianca/TestingAPI-Postman/assets/119669189/8fbc5df0-7adb-4991-846d-71e97d433559)

