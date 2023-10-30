# Music Streaming API README

## Overview

The Music Streaming API is a RESTful service designed to enable users to manage songs, playlists, and user accounts. It offers endpoints for creating, reading, updating, and deleting songs and playlists, and provides features for user authentication and authorization.

## Table of Contents

- [Features](#features)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [API Endpoints](#api-endpoints)
- [Authentication](#authentication)
- [Pagination](#pagination)
- [Error Handling](#error-handling)
- [Deployment](#deployment)
- [Testing](#testing)
- [Contributing](#contributing)
- [License](#license)

## Features

- **User Management**:
  - User registration and login
  - User roles (Normal and Admin)

- **Song Management (Admin Only)**:
  - Create, Read, Update, and Delete songs

- **Playlist Management**:
  - Create, Read, Update, and Delete playlists
  - Add and remove songs from playlists
  - Pagination support

## Getting Started

### Prerequisites

To run the Music Streaming API, make sure you have the following prerequisites:

- Java Development Environment
- MySQL Database
- Maven or Gradle (for building and running the project)

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-repo/music-streaming-api.git
Navigate to the project directory:

bash
Copy code
cd music-streaming-api
Configure your MySQL database settings in src/main/resources/application.properties.

Build and run the application:

bash
Copy code
# Using Maven
mvn spring-boot:run

# Using Gradle
gradle bootRun
The API will be available at http://localhost:8080. You can customize the port in application.properties.

API Endpoints
User Endpoints:

POST /api/user/register - Register a new user
POST /api/user/login - User login
GET /api/user/profile - Retrieve user profile
Song Endpoints (Admin Only):

POST /api/song - Create a new song
GET /api/song/{id} - Get a song by ID
PUT /api/song/{id} - Update a song
DELETE /api/song/{id} - Delete a song
Playlist Endpoints:

POST /api/playlist - Create a new playlist
GET /api/playlist/{id} - Get a playlist by ID
PUT /api/playlist/{id} - Update a playlist
DELETE /api/playlist/{id} - Delete a playlist
GET /api/playlist/{id}/songs - Get songs in a playlist with pagination
Authentication
Authentication is required for certain endpoints. Use the /api/user/login endpoint to obtain an access token, which should be included in the Authorization header for authenticated requests.
Pagination
For endpoints that support pagination (e.g., a list of songs in a playlist), use query parameters page and size to control the number of items per page and the current page.
Error Handling
The API provides detailed error responses with appropriate HTTP status codes for various situations. Check the response status and body for error messages.
Deployment
Deploy the Music Streaming API on a web server or cloud platform, and configure your MySQL database connection.
Testing
You can test the API using tools like Postman or write unit tests for services and controllers.
Contributing
Contributions are welcome! If you wish to contribute to the project, please follow our Contribution Guidelines.

License
This project is licensed under the MIT License.
