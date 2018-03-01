# mongo_syntax_solo_challenge
In this challenge, we’re going to practice basic Mongo syntax. This should help better solidify some concepts that were covered during lecture.

## Assumptions
* You are using the mongo shell or Robomongo
* You installed mongo via homebrew
* mongod is currently running on your computer

## Setup
Follow the instructions below before continuing with this challenge.

### Create your database
We are creating a database to hold a collection with at least 3 documents.

1. Open mongo shell
2. Type `use prime-orders` to create your database (or use an existing database)

### GitHub repo
Create a GitHub repo named “prime-solo-mongo”.
Create a file called “mongo.txt”. You will store your responses to the exercise questions here.

## Exercise
For each of the following questions

* Write a comment that specifies which question you are answering. Use JavaScript comment syntax.
* Write the Mongo query that answers the question, below that comment.

### Example question and answer
```
// 0. Create a collection named orders
db.createCollection('orders')
```

## Tasks
1. Create a collection named `orders`.
2. Insert at least 3 documents that represent an order. IMPORTANT: See section below for fields. Order dates should be: 2017-02-03, 2017-04-04, 2017-01-02
3. Find all orders and make them look pretty.
4. Find all orders with an `orderDate` that is after 1/31/2017.
5. Change the `orderTotal` from 2/3/2017 to 63 dollars (you do NOT have to ensure the lineItems' unitPrice * quantity add up to the orderTotal)
6. Add another `lineItem` to the order from 4/4/2017
7. Change the first `lineItem` in the order from 1/2/2017 to be for 2 'transistor radio's
8. Find orders with `lineItems` that have a quantity that is less than 10, but greater than 2. You will have to research $elemMatch

### order fields
Your orders need to have the following fields:

* orderDate -- see https://docs.mongodb.org/manual/reference/method/Date/
* orderTotal
* lineItems -- a sub-document (array) that can accommodate many line items with fields: unitPrice, quantity, productName