# Movie Review API

This project is a RESTful API for managing movie reviews. It is built using Java and MongoDB as a NoSQL database.

## Features

- Create, read, update, and delete movie reviews
- Get a list of all movies
- Search for movies by title, genre, or release year
- Get detailed information about a movie, including its reviews

## Technologies Used

- Java 11
- MongoDB 4.2
- Spring Boot 2.5.4
- Maven 3.8.3

## Installation

1. Clone the repository:

git clone https://github.com/waliyani09/movies.git


2. Install MongoDB and start the server:

sudo service mongod start


3. Navigate to the project directory and build the project:

cd movie-review-api
mvn clean install


4. Run the application:

mvn spring-boot:run


## Usage

### Endpoints

The following endpoints are available:

| Endpoint                  | Description                            |
|---------------------------|----------------------------------------|
| `GET /movies`             | Get a list of all movies               |
| `GET /movies/{id}`        | Get detailed information about a movie |
| `POST /movies`            | Create a new movie                      |
| `PUT /movies/{id}`        | Update an existing movie               |
| `DELETE /movies/{id}`     | Delete a movie                          |
| `GET /reviews`            | Get a list of all reviews              |
| `GET /reviews/{id}`       | Get detailed information about a review|
| `POST /reviews`           | Create a new review                     |
| `PUT /reviews/{id}`       | Update an existing review              |
| `DELETE /reviews/{id}`    | Delete a review                         |
| `GET /movies/search`      | Search for movies by title, genre, or release year |
| `GET /movies/{id}/reviews`| Get all reviews for a specific movie |


