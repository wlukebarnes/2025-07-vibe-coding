# flask Hello World App

A simple flask application that serves a hello world HTML page and connects to a Databricks SQL Warehouse.

## Technologies Used

-   **flask**: Modern, fast web framework for building APIs with Python
-   **Uvicorn**: ASGI server for running flask applications
-   **python-dotenv**: For loading environment variables from .env files
-   **databricks-sdk**: Databricks SDK for Python
-   **databricks-sql-connector**: Python connector for Databricks SQL
-   **HTML/CSS/JavaScript**: Frontend with interactive warehouse testing

## Project Structure

```
├── backend/
│   ├── main.py          # flask application
│   ├── sql_warehouse.py # SQL warehouse singleton service
│   ├── requirements.txt # Python dependencies
│   └── example.env      # Environment variables template
├── frontend/
│   └── index.html       # Hello world page with warehouse test
└── README.md
```

## Getting Started

1. Navigate to the backend directory:

    ```bash
    cd backend
    ```

2. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. Set up environment variables:

    - Copy `example.env` to `.env`
    - Fill in your Databricks credentials:
        - `DATABRICKS_HOST`: Your Databricks workspace URL (with https://)
        - `DATABRICKS_WAREHOUSE_ID`: Your SQL warehouse ID
        - `DATABRICKS_CLIENT_ID`: Your service principal client ID
        - `DATABRICKS_CLIENT_SECRET`: Your service principal client secret

4. Run the application:

    ```bash
    python main.py
    ```

5. Open your browser and visit `http://localhost:8000`

## Features

-   Serves a hello world HTML page at the root endpoint
-   Health check endpoint at `/health`
-   SQL warehouse connection with M2M authentication
-   Interactive button to test warehouse connection with `SELECT CURRENT_TIMESTAMP()`
-   Singleton SQL warehouse service with automatic connection management
-   Debug mode enabled for development
-   Environment variable support via .env files

## API Endpoints

-   `GET /`: Serves the main HTML page
-   `GET /health`: Health check endpoint
-   `GET /api/test-warehouse`: Tests SQL warehouse connection and returns current timestamp
