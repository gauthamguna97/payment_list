# Payments Data Dashboard
  - TechStack - `React, Redux, TypeScript`
  - Functionalities
    - `Table` for list of payments
    - `Search Bar` to filter the payments
    - `Add Payment` popup for adding a transaction
    - `Sortable Table` based on columns (sender, receiver, currency)

## Running Code
  - Client
    - `cd client`
    - `npm install`
    - `npm start`
    - localhost:3000 to view the code

  - Server
    - `cd server`
    - `npm install`
    - `npm start`

## API's Usage

  - Used `GET /payments` endpoint that produces payments data.
  - Used `POST /payments` endpoint that allows you to record a new payment on the server.
  - Used `GET /users` endpoint to add only valid users in a transaction


## Detailed Implementions

### Tech Stack:
 - I used React along with Redux for client Side state management.
 - Used TypeScript to write type checked code and bug free code.

### List of Payments
  - I used a simple table to populate list of transactions
  - `GET /payments` API is called periodically to add payments
  - Redux is used to maintain the historical transactions

### Search Payments
  - Added a simple search bar to filter Payments
  - Payments are filtered based on sender name, receiver name and currency type

### Add Payment
  - Added a simple popup form to display payments
  - Used `GET /users` to validate users while adding in the form
  - Added a autocomplete search list while adding sender or receiver
  - Added ERROR checks for an invalid data entry (Eg: Invalid Users, same sender and receiver)
  - Used `POST /payments` to record payment in server.
  - Handled HTTP status codes according to requirements

