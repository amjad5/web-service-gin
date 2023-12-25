# Album Web Service

This repository contains a simple web service for managing record albums. The service is built using the [Gin](https://github.com/gin-gonic/gin) web framework in Go.

## Endpoints

### Get All Albums

- **Endpoint:** `/albums`
- **HTTP Method:** GET
- **Description:** Retrieve information about all record albums.
- **Response:** Returns a JSON array containing details about each album.

### Get Album by ID

- **Endpoint:** `/albums/:id`
- **HTTP Method:** GET
- **Description:** Retrieve information about a specific record album based on its ID.
- **Parameters:**
  - `id` (string): The unique identifier of the album.
- **Response:**
  - If the album is found, returns a JSON object with album details.
  - If the album is not found, returns a JSON object with a "message" field indicating that the album was not found.

### Add a New Album

- **Endpoint:** `/albums`
- **HTTP Method:** POST
- **Description:** Add a new record album to the collection.
- **Request Body:** Expects a JSON object with the following fields:
  - `title` (string): Title of the album.
  - `artist` (string): Artist or band name.
  - `price` (float64): Price of the album.
- **Response:**
  - If the album is successfully added, returns a JSON object with the details of the new album.
  - If there is an error in the request or validation, an appropriate HTTP status code is returned.

## Example Usage

### Get All Albums

```bash
curl http://localhost:8080/albums
```

### Get Album by ID
```bash
curl http://localhost:8080/albums/1
```
### Add a New Album
```bash
curl -X POST -H "Content-Type: application/json" -d '{"title":"New Album","artist":"New Artist","price":29.99}' http://localhost:8080/albums
```

## Running the Service
To run the web service locally, ensure you have Go installed and execute the following commands:
```
go get -u github.com/gin-gonic/gin
go run main.go
```
The service will be accessible at http://localhost:8080.

Feel free to explore the code and provide any feedback. If you have questions or suggestions, please create an issue.

Happy coding! 🎶🚀
