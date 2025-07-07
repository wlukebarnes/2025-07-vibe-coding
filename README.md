# Vibe Coding Demo App

A simple web application built with FastAPI and HTML to demonstrate iterative app development with Cursor.

## Purpose

This project serves as a demo for building web applications step-by-step using Cursor IDE. It demonstrates a basic FastAPI backend serving static HTML content.

## Technologies Used

-   **Backend**: FastAPI - A modern, fast web framework for building APIs with Python
-   **Frontend**: Static HTML with CSS styling
-   **Server**: Uvicorn - ASGI server for running FastAPI applications
-   **Environment**: python-dotenv for environment variable management

## Getting Started

1. Navigate to the backend directory:

    ```bash
    cd backend
    ```

2. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. Run the application:

    ```bash
    python main.py
    ```

4. Open your browser and visit `http://localhost:8000`

The application will serve a simple "Hello World" page from the frontend directory.

## Project Structure

```
├── backend/
│   ├── main.py              # FastAPI application
│   ├── requirements.txt     # Python dependencies
│   └── example.env          # Example environment file
├── frontend/
│   └── index.html           # Static HTML page
└── README.md               # This file
```
