# FastAPI Movie Ticket Booking System

## Overview

This project is a backend API for a Movie Ticket Booking System developed using FastAPI as part of the February 2026 Internship at Innomatics Research Labs.

The application simulates a real-world cinema booking workflow, including movie management, ticket booking, seat allocation, and advanced data operations such as search, filtering, sorting, and pagination.

---

## Features

### Movie Management

* Retrieve all movies with aggregate statistics
* Get movie details by ID
* Add new movies with validation
* Update ticket price and seat availability
* Delete movies with constraints (restricted if bookings exist)

### Booking System

* Create bookings with seat types:

  * Standard
  * Premium (1.5× pricing)
  * Recliner (2× pricing)
* Apply promotional codes:

  * SAVE10 (10% discount)
  * SAVE20 (20% discount)
* Automatic seat availability updates

### Seat Hold Workflow

* Temporarily hold seats before booking
* Confirm seat holds and convert them into bookings
* Release held seats and restore availability

### Data Operations

* Search movies and bookings
* Filter movies by genre, language, price, and seat availability
* Sort movies and bookings with validation
* Paginate results for movies and bookings
* Combined browsing endpoint (search + filter + sort + pagination)

---

## Tech Stack

* Python
* FastAPI
* Pydantic
* Uvicorn

---

## Running the Application

```bash
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python -m uvicorn main:app --reload
```

---

## API Documentation

Swagger UI is available at:

http://127.0.0.1:8000/docs

---

## API Endpoints

### General

```http
GET /
```

---

### Movies

```http
GET /movies
GET /movies/{movie_id}
GET /movies/summary
GET /movies/filter
GET /movies/search
GET /movies/sort
GET /movies/page
GET /movies/browse
```

---

### Bookings

```http
GET /bookings
POST /bookings
GET /bookings/active
GET /bookings/search
GET /bookings/sort
GET /bookings/page
```

---

### Movie Management (CRUD)

```http
POST /movies
PUT /movies/{movie_id}
DELETE /movies/{movie_id}
```

---

### Seat Hold Workflow

```http
POST /seat-hold
GET /seat-hold
POST /seat-confirm/{hold_id}
DELETE /seat-release/{hold_id}
```

---

## Endpoint Mapping

### General

| Method | Endpoint | Description               |
| ------ | -------- | ------------------------- |
| GET    | `/`      | Returns a welcome message |

---

### Movies

| Method | Endpoint             | Description                                                    |
| ------ | -------------------- | -------------------------------------------------------------- |
| GET    | `/movies`            | Retrieve all movies with total count and seat availability     |
| GET    | `/movies/{movie_id}` | Retrieve a specific movie by ID                                |
| GET    | `/movies/summary`    | Get summary statistics (pricing, genres, total seats)          |
| GET    | `/movies/filter`     | Filter movies by genre, language, price, and seat availability |
| GET    | `/movies/search`     | Search movies by keyword                                       |
| GET    | `/movies/sort`       | Sort movies by price, title, duration, or seats                |
| GET    | `/movies/page`       | Paginate movie results                                         |
| GET    | `/movies/browse`     | Combined search, filter, sort, and pagination                  |

---

### Bookings

| Method | Endpoint           | Description                              |
| ------ | ------------------ | ---------------------------------------- |
| GET    | `/bookings`        | Retrieve all bookings with total revenue |
| POST   | `/bookings`        | Create a new booking                     |
| GET    | `/bookings/active` | Retrieve active bookings                 |
| GET    | `/bookings/search` | Search bookings by customer name         |
| GET    | `/bookings/sort`   | Sort bookings by total cost or seats     |
| GET    | `/bookings/page`   | Paginate booking results                 |

---

### Movie Management (CRUD)

| Method | Endpoint             | Description                                   |
|--------|--------------------|-----------------------------------------------|
| GET    | `/movies`           | Retrieve all movies                           |
| GET    | `/movies/{movie_id}`| Retrieve a specific movie by ID               |
| POST   | `/movies`           | Add a new movie                               |
| PUT    | `/movies/{movie_id}`| Update ticket price or seat availability      |
| DELETE | `/movies/{movie_id}`| Delete a movie (restricted if bookings exist) |
---

### Seat Hold Workflow

| Method | Endpoint                  | Description                                 |
| ------ | ------------------------- | ------------------------------------------- |
| POST   | `/seat-hold`              | Temporarily hold seats                      |
| GET    | `/seat-hold`              | Retrieve all seat holds                     |
| POST   | `/seat-confirm/{hold_id}` | Confirm held seats and create booking       |
| DELETE | `/seat-release/{hold_id}` | Release held seats and restore availability |

---

## Project Structure

```
fastapi-final-project/
├── main.py
├── requirements.txt
├── README.md
├── screenshots/
```

---

## Screenshots

The following screenshots demonstrate the functionality of all implemented endpoints:

### Basic Endpoints

* Q1 – Home Endpoint
* Q2 – Get All Movies
* Q3 – Get Movie by ID (Valid / Invalid)
* Q4 – Get All Bookings
* Q5 – Movies Summary

### Validation and Helpers

* Q6 – Booking Validation Error (Pydantic)
* Q7 – Helper Functions Implementation

### Booking and Filtering

* Q8 – Create Booking and Seat Update
* Q9 – Booking with Promo Code
* Q10 – Filter Movies

### CRUD Operations

* Q11 – Add Movie (Success / Duplicate)
* Q12 – Update Movie (Valid / Invalid)
* Q13 – Delete Movie (Blocked / Success / Not Found)

### Seat Hold Workflow

* Q14 – Create and View Seat Hold
* Q15 – Confirm and Release Seat Hold

### Search, Sort, Pagination

* Q16 – Movie Search (Found / Not Found)
* Q17 – Sorting (Valid / Invalid Cases)
* Q18 – Pagination (Multiple Pages)
* Q19 – Booking Search, Sort, and Pagination
* Q20 – Combined Browse Endpoint

All screenshots are available in the `screenshots/` directory.

---

## Key Learnings

* Designing RESTful APIs using FastAPI
* Implementing data validation with Pydantic
* Managing state using in-memory data structures
* Building multi-step workflows (seat hold and confirmation)
* Implementing search, filtering, sorting, and pagination
* Structuring backend code for clarity and scalability

---

## Author

Devupalli Harsha Vardhan

---

## Acknowledgement

This project was developed as part of the FastAPI Internship program at Innomatics Research Labs (February 2026).
