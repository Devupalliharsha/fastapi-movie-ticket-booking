# FastAPI Final Project - Movie Ticket Booking

## Overview

This project is a backend API for a Movie Ticket Booking System developed using FastAPI as part of the Feb 2026 Internship at Innomatics Research Labs.
It demonstrates core backend development concepts including API design, validation, business logic, and workflow handling.

---

## Features

### Movie Management

* Retrieve all movies with aggregate data
* Get movie details by ID
* Add new movies with validation
* Update ticket price and seat availability
* Delete movies with validation (restricted if bookings exist)

### Booking System

* Create bookings with seat type pricing (standard, premium, recliner)
* Apply promo codes (SAVE10, SAVE20)
* Automatic seat availability updates

### Seat Hold Workflow

* Temporarily hold seats
* Confirm hold and convert to booking
* Release hold and restore seats

### Data Operations

* Search movies and bookings
* Filter movies by genre, language, price, and availability
* Sort movies and bookings with validation
* Pagination support for movies and bookings
* Combined browse endpoint (search, filter, sort, pagination)

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

Swagger UI:
http://127.0.0.1:8000/docs

---

## Project Structure

```
fastapi-final-project/
├── main.py
├── requirements.txt
├── README.md
```

---

## Author

Devupalli Harsha Vardhan

---

## Acknowledgement

Developed as part of the Innomatics Research Labs Internship (Feb 2026).
