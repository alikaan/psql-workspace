# PostgreSQL and Python Workspace

This repository provides a setup for creating a PostgreSQL database and a pgAdmin instance using Docker Compose. This setup allows you to easily manage your PostgreSQL databases and interact with them using Python.

## Prerequisites

- Docker
- Docker Compose

## Getting Started

### Step 1: Start the Services

To start the PostgreSQL and pgAdmin services, run the following command:

```sh
docker-compose up -d
```


This command will start the services in detached mode.

### Step 2: Access pgAdmin

Once the services are up and running, you can access pgAdmin by navigating to http://localhost:5050 in your web browser. Use the following credentials log in:

 - Email: admin@admin.com
 - Password: pgadmin

### Step 3: Connect to PostgreSQL

<vscode_annotation details='%5B%7B%22title%22%3A%22hardcoded-credentials%22%2C%22description%22%3A%22Embedding%20credentials%20in%20source%20code%20risks%20unauthorized%20access%22%7D%5D'>In</vscode_annotation> pgAdmin, you can create a new server connection using the following details:

 - Host: psql-db
 - Port: 5432
 - Username: postgres
 - Password: postgres

### Using PostgreSQL in Python

The repository includes an example Python script (example/PostgreSQL+and+Python.py) that demonstrates how to connect to the PostgreSQL database using the psycopg2 library.

### Step 1: Install psycopg2

First, install the psycopg2 library using 

```sh
pip install psycopg2
```

### Step 2: Run the Python Script

You can run the example script to interact with the PostgreSQL database:

```sh
python example/PostgreSQL+and+Python.py
```

The script demonstrates how to:

 - Create a connection to the PostgreSQL database
 - Execute SQL queries
 - Fetch results from the database
 - Insert data into the database

### Stopping the Services

To stop the PostgreSQL and pgAdmin services, run the following command:

```sh
docker-compose down
```

This command will stop and remove the containers.

### Additional Information

For more information on using PostgreSQL with Python, refer to the Psycopg2 documentation.

### License
This project is licensed under the MIT License. 