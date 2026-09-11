# Northstar Market

A complete e-commerce starter built with Node.js, Express, MongoDB, Mongoose, and a responsive vanilla JavaScript storefront.

## Requirements

- Node.js 18+
- MongoDB running locally, or a MongoDB Atlas connection string

## Setup

1. Install dependencies:

   ```bash
   npm install
   ```

2. Update `.env` if needed:

   ```env
   PORT=3000
   MONGODB_URI=mongodb://127.0.0.1:27017/northstar-market
   ```

3. Add sample products:

   ```bash
   npm run seed
   ```

4. Start the app:

   ```bash
   npm start
   ```

Open http://localhost:3000.

## API

- `GET /api/products?search=&category=` list products
- `GET /api/products/:id` get one product
- `POST /api/products` create a product
- `PUT /api/products/:id` update a product
- `DELETE /api/products/:id` delete a product
- `GET /api/cart/:userId` view a cart
- `POST /api/cart` add `{ userId, productId, quantity }`
- `PATCH /api/cart/:userId/items/:productId` update `{ quantity }`
- `DELETE /api/cart/:userId/items/:productId` remove an item
- `POST /api/orders` place an order with `{ userId, shippingAddress }`
- `GET /api/orders/user/:userId` view order history
- `GET /api/orders/:userId/:orderId` view one order

The browser creates a guest user ID in localStorage, so the shopping flow works without authentication. Add authentication later by replacing that ID with the authenticated user's ID.
