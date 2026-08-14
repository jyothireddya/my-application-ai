# Customer Order Service

Customer Order Service is a REST API used to create, retrieve, update, and cancel customer orders.

## Application Overview

The application provides order management capabilities for internal business applications.

## Technology Stack

- Node.js 20
- Express 4.18.3
- PostgreSQL
- Jest 29.7.0

## Entry Point

The main application entry point is:

`src/index.js`

## API Endpoints

- `GET /orders` — Retrieve customer orders
- `GET /orders/:id` — Retrieve a specific order
- `POST /orders` — Create a customer order
- `PUT /orders/:id` — Update a customer order
- `DELETE /orders/:id` — Cancel a customer order

## Environment Variables

The application requires:

- `PORT`
- `DATABASE_URL`
- `JWT_SECRET`

Secret values must be provided through the deployment environment and must not be committed to the repository.

## Database

The application uses PostgreSQL for persistent order data.

## Testing

Jest is used for automated testing.

## Build and Run

Install dependencies:

`npm install`

Start the application:

`npm start`

Run tests:

`npm test`
