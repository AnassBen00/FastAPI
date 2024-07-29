# Project Overview

The goal of this project is to provide a practical example of using Apache Kafka within a FastAPI application. This project, helps understanding how to implement a messaging system using Kafka.
# Technologies Used

    FastAPI: A framework for building APIs with Python 3+.
    Apache Kafka: A distributed event streaming platform.
    Docker: For setting up the Kafka, Zookeeper, and Kafdrop instances.
    Postman: For testing the API endpoints.

# Prerequisites

Ensure you have the following installed on your machine:

    Python 3+
    Docker
    Postman

# Set up a virtual environment:

python -m venv venv
source venv/bin/activate  # On Windows use `.\venv\Scripts\activate`

Start Kafka, Zookeeper, and Kafdrop using Docker Compose:

docker-compose up -d

Run the FastAPI application:

uvicorn main:app --reload

# Usage

After starting the application, you can interact with the FastAPI endpoints to publish and consume messages from Kafka.

To test the message creation endpoint, use Postman to send a POST request to http://localhost:8000/create_message with the appropriate payload.

Method: POST

body: 
{
  "message": "Hello message 1"
}

