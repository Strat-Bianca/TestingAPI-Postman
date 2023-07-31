# Testing API with Postman

You need to read the API documentation. 

We're using Simple Books API whose documentation can be found in the resources section of this link: https://github.com/vdespa/introduction-to-postman-course/blob/main/simple-books-api.md

# Endpoints

GET Method - get some data/request;

The API: https://simple-books-api.glitch.me


## List of books ##

GET /books

Returns a list of books.
 
 2 optional query parameters:
- type: fiction or non-fiction;
- limit: a number between 1 and 20.
  
I also create a variable for the URL link.

Status 200 - standard response for successful HTTP requests.

![GET list of books (2)](https://github.com/Strat-Bianca/TestingAPI-Postman/assets/119669189/b082479e-f322-47fe-b118-4e01d07d2d67)


## Get a single book ##
GET /books/:bookId

Retrieve detailed information about a book with a specific Id. (bookId = 3)


![GET a single book](https://github.com/Strat-Bianca/TestingAPI-Postman/assets/119669189/eafbb0ca-7588-4e3f-9c46-cd125a91caa7)

## Submit an order ##
POST /orders

Allows you to submit a new order, we are sending some data. 

Requires authentication. 
Authorization: Bearer <YOUR TOKEN> we register ourself with an API client.

The request body needs to be in JSON format and include the following properties:

- bookId - Integer - (Required)
- customerName - String - (Required)
  
 The response body will contain the order Id.

![POST order a book](https://github.com/Strat-Bianca/TestingAPI-Postman/assets/119669189/3199d6bc-28da-4885-b4ed-b7cf8c13ab1d)

## Get all orders ##
GET /orders 

Allows you to view all orders. Requires authentication.

![GET all books order](https://github.com/Strat-Bianca/TestingAPI-Postman/assets/119669189/b1e5649d-02b6-493d-b7d8-40c9dd4e5dc4)

## Get an order ##
GET /orders/:orderId

Allows you to view an existing order. Requires authentication.

![GET an order](https://github.com/Strat-Bianca/TestingAPI-Postman/assets/119669189/e07bcb2b-42cc-4642-836e-a916515fbb44)

## Update an order ##
PATCH /orders/:orderId

Update an existing order. Requires authentication.

The request body needs to be in JSON format and allows you to update the following properties:

- customerName - String

![PATCH update-order](https://github.com/Strat-Bianca/TestingAPI-Postman/assets/119669189/49efc6ba-e0aa-45e8-89b0-dacf40713290)

## Delete an order ##
DELETE /orders/:orderId

Delete an existing order. Requires authentication. --- Authorization: Bearer <YOUR TOKEN>

The request body needs to be empty.



## API Authentication ##
To submit or view an order, you need to register your API client.

POST /api-clients/

The request body needs to be in JSON format and include the following properties:

clientName - "Postman"
clientEmail - "strat.bianca@yahoo.com"

![POST register API client](https://github.com/Strat-Bianca/TestingAPI-Postman/assets/119669189/6d26d22b-c170-4ab8-a329-c8341cc3f1f6)

![POST register API client-2](https://github.com/Strat-Bianca/TestingAPI-Postman/assets/119669189/8fbc5df0-7adb-4991-846d-71e97d433559)

