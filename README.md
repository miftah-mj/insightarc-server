# InsightArc Server

This is the server-side application for the InsightArc project. It provides APIs for managing users, publishers, articles, and more.

## Table of Contents

-   [Installation](#installation)
-   [Configuration](#configuration)
-   [Running the Server](#running-the-server)
-   [API Endpoints](#api-endpoints)
    -   [Users API](#users-api)
    -   [Publishers API](#publishers-api)
    -   [Articles API](#articles-api)
-   [Authentication](#authentication)
-   [Error Handling](#error-handling)

## Installation

1. Clone the repository:

    ```sh
    git clone https://github.com/yourusername/insightarc-server.git
    cd insightarc-server
    ```

2. Install dependencies:
    ```sh
    npm install
    ```

## Configuration

Create a [.env](http://_vscodecontentref_/1) file in the root directory and add the following environment variables:

```env
PORT=5000
MONGODB_URI=your_mongodb_uri
TOKEN_SECRET=your_jwt_secret
IMGBB_API_KEY=your_imgbb_api_key
```

## Running the Server

To start the server, use the following command:

```sh
npm start
```

The server will start on the port specified in the `.env` file.

## API Endpoints

### Users API

-   `GET /api/users` - Get all users
-   `POST /api/users` - Create a new user
-   `GET /api/users/:id` - Get a user by ID
-   `PUT /api/users/:id` - Update a user by ID
-   `DELETE /api/users/:id` - Delete a user by ID

### Publishers API

-   `GET /api/publishers` - Get all publishers
-   `POST /api/publishers` - Create a new publisher
-   `GET /api/publishers/:id` - Get a publisher by ID
-   `PUT /api/publishers/:id` - Update a publisher by ID
-   `DELETE /api/publishers/:id` - Delete a publisher by ID

### Articles API

-   `GET /api/articles` - Get all articles
-   `POST /api/articles` - Create a new article
-   `GET /api/articles/:id` - Get an article by ID
-   `PUT /api/articles/:id` - Update an article by ID
-   `DELETE /api/articles/:id` - Delete an article by ID

## Authentication

The server uses JWT (JSON Web Tokens) for authentication. Make sure to set the `TOKEN_SECRET` environment variable in your `.env` file.

## Error Handling

The server includes error handling middleware to manage errors and send appropriate responses.
