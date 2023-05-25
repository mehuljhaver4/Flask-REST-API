# Flask-REST-API
This project is a Flask-based RESTful API for temperature monitoring. It allows users to create rooms, add temperature readings for each room, and retrieve the average temperature across all rooms.

## Prerequisites
Make sure you have the following dependencies installed:
* Python 3.x
* PostgreSQL
* psycopg2
* dotenv
* Flask

## Installation
#### Clone the repository:
git clone https://github.com/mehuljhaver4/Flask-REST-API.git

#### Change into the project directory:
cd flask-temperature-api

#### Install the dependencies:
pip install -r requirements.txt

## Configuration
Create a .env file in the project root directory.

#### Add the following variables to the .env file and provide appropriate values:
DATABASE_URL= your_postgresql_database_url

## API Endpoints
* Create Room
  * URL: /api/room
  * Method: POST

* Add Temperature Reading
  * URL: /api/temperature
  * Method: POST

* Get Global Average Temperature
  * URL: /api/average
  * Method: GET

## Database Schema
The API uses the following PostgreSQL tables:

* rooms
  *  Columns: id (SERIAL PRIMARY KEY), name (TEXT)
* temperatures
  * Columns: room_id (INTEGER), temperature (REAL), date (TIMESTAMP)
  * Foreign Key: room_id references rooms(id) ON DELETE CASCADE
