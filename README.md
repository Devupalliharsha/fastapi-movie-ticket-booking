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
