<h1>Movie Review API</h1>
This project is a RESTful API for managing movie reviews. It is built using Java and MongoDB as a NoSQL database.

Features
Create, read, update, and delete movie reviews
Get a list of all movies
Search for movies by title, genre, or release year
Get detailed information about a movie, including its reviews
Technologies Used
Java 11
MongoDB 4.2
Spring Boot 2.5.4
Maven 3.8.3
Installation
Clone the repository:
bash
Copy code
git clone https://github.com/your-username/movie-review-api.git
Install MongoDB and start the server:
sql
Copy code
sudo service mongod start
Navigate to the project directory and build the project:
bash
Copy code
cd movie-review-api
mvn clean install
Run the application:
Copy code
mvn spring-boot:run
Usage
Endpoints
The following endpoints are available:

Endpoint	Description
GET /movies	Get a list of all movies
GET /movies/{id}	Get detailed information about a movie
POST /movies	Create a new movie
PUT /movies/{id}	Update an existing movie
DELETE /movies/{id}	Delete a movie
GET /reviews	Get a list of all reviews
GET /reviews/{id}	Get detailed information about a review
POST /reviews	Create a new review
PUT /reviews/{id}	Update an existing review
DELETE /reviews/{id}	Delete a review
GET /movies/search	Search for movies by title, genre, or release year
GET /movies/{id}/reviews	Get all reviews for a specific movie
Request/Response Examples
Get a list of all movies
Request:

vbnet
Copy code
GET /movies HTTP/1.1
Host: localhost:8080
Response:

css
Copy code
HTTP/1.1 200 OK
Content-Type: application/json

[
    {
        "id": "1",
        "title": "The Shawshank Redemption",
        "genre": "Drama",
        "releaseYear": 1994
    },
    {
        "id": "2",
        "title": "The Godfather",
        "genre": "Drama",
        "releaseYear": 1972
    }
]
Get detailed information about a movie
Request:

vbnet
Copy code
GET /movies/1 HTTP/1.1
Host: localhost:8080
Response:

css
Copy code
HTTP/1.1 200 OK
Content-Type: application/json

{
    "id": "1",
    "title": "The Shawshank Redemption",
    "genre": "Drama",
    "releaseYear": 1994,
    "reviews": [
        {
            "id": "1",
            "username": "john_doe",
            "rating": 9,
            "comment": "This is a great movie!"
        },
        {
            "id": "2",
            "username": "jane_doe",
            "rating": 8,
            "comment": "I really enjoyed this movie."
        }
    ]
}
Create a new movie
Request:

Copy code
POST
