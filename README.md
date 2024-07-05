# Social Network API

## Description
This project is a social network API built using Express.js for routing, a MongoDB database, and the Mongoose ODM. Users can share their thoughts, react to friends’ thoughts, and create a friend list. This API is designed to handle large amounts of unstructured data efficiently.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
  - [Users](#users)
  - [Thoughts](#thoughts)
- [Walkthrough Video](#walkthrough-video)
- [Technologies Used](#technologies-used)


## Installation
To set up this project locally, follow these steps:

1. Clone the repository:
    ```bash
   git clone https://github.com/github-cedsim/social-network-api.git
2. Navigate to the project directory:
    ```bash
   cd social-network-api
3. Install the dependencies:
    ```bash
    npm install
4. Start the server:
    ```bash
    npm start

## Usage
After starting the server, you can interact with the API using Insomnia, Postman, or any other API client. The base URL for all endpoints is http://localhost:3001.

API Endpoints
The following endpoints are available for interacting with the API:

Users

Create a New User

URL: http://localhost:3001/api/users
Method: POST
Body (JSON):
json

{
  "username": "user1",
  "email": "user1@example.com"
}

Get All Users

URL: http://localhost:3001/api/users
Method: GET
Get a Single User by ID

URL: http://localhost:3001/api/users/:userId
Method: GET
Update a User by ID

URL: http://localhost:3001/api/users/:userId
Method: PUT
Body (JSON):
json

{
  "username": "updatedUser",
  "email": "updatedUser@example.com"
}
Delete a User by ID

URL: http://localhost:3001/api/users/:userId
Method: DELETE
Add a Friend to a User's Friend List

URL: http://localhost:3001/api/users/:userId/friends/:friendId
Method: POST
Remove a Friend from a User's Friend List

URL: http://localhost:3001/api/users/:userId/friends/:friendId
Method: DELETE
Thoughts
Create a New Thought

URL: http://localhost:3001/api/thoughts
Method: POST
Body (JSON):
json

{
  "thoughtText": "This is a new thought",
  "username": "user1",
  "userId": "user1Id"
}
Get All Thoughts

URL: http://localhost:3001/api/thoughts
Method: GET
Get a Single Thought by ID

URL: http://localhost:3001/api/thoughts/:thoughtId
Method: GET
Update a Thought by ID

URL: http://localhost:3001/api/thoughts/:thoughtId
Method: PUT
Body (JSON):
json

{
  "thoughtText": "Updated thought text"
}

Delete a Thought by ID

URL: http://localhost:3001/api/thoughts/:thoughtId
Method: DELETE
Create a Reaction to a Thought

URL: http://localhost:3001/api/thoughts/:thoughtId/reactions
Method: POST
Body (JSON):
json

{
  "reactionBody": "This is a reaction",
  "username": "user2"
}

Remove a Reaction from a Thought

URL: http://localhost:3001/api/thoughts/:thoughtId/reactions/:reactionId
Method: DELETE

## Walkthrough Video
A walkthrough video demonstrating the functionality of the application can be found here. The video shows: https://drive.google.com/file/d/14Jt8b2NMrDTAzz6UU3p-rsRMpP5Kw4lL/view?usp=drive_link

How to start the application's server.
GET routes for all users and all thoughts being tested in Insomnia.
GET routes for a single user and a single thought being tested in Insomnia.
POST, PUT, and DELETE routes for users and thoughts being tested in Insomnia.
POST and DELETE routes for a user’s friend list being tested in Insomnia.
POST and DELETE routes for reactions to thoughts being tested in Insomnia.

## Technologies Used
Node.js
Express.js
MongoDB
Mongoose
Insomnia (for API testing)

