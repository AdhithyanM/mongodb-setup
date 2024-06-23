# MongoDB and Mongo Express Setup with Docker

This repository contains a Docker Compose configuration to set up MongoDB and Mongo Express. MongoDB is a NoSQL database, and Mongo Express is a web-based MongoDB admin interface written in Node.js, Express.js, and Bootstrap3.

## Getting Started

### Clone the Repository

First, clone this repository to your local machine:

```bash
git clone https://github.com/AdhithyanM/mongodb-setup.git
cd <repository-directory>
```

Replace `<repository-directory>` with the name of the directory where the repository will be cloned.

### Run the Docker Services

To start the MongoDB and Mongo Express services, run the following command:

```bash
docker-compose up -d
```

This command will start the services in detached mode.

### Stop the Docker Services

To stop the running services, use the following command:

```bash
docker-compose down
```

This will stop and remove the containers defined in the `docker-compose.yml` file.

## Working with MongoDB

### Access MongoDB via Mongo Express

Mongo Express provides a web-based interface to interact with MongoDB. Follow these steps to access it:

1. Open your web browser and go to [http://localhost:8080](http://localhost:8080).
2. Log in using the following credentials:
   - **Username**: root
   - **Password**: root

You can now use the Mongo Express UI to interact with your MongoDB instance.

### Connect to MongoDB Using MongoDB Compass

If you prefer to use MongoDB Compass, follow these steps to connect to the MongoDB instance running in Docker:

1. Open MongoDB Compass on your host machine.
2. Click on the "New Connection" button.
3. In the "Hostname" field, enter `localhost`.
4. In the "Port" field, enter `27017`.
5. Click "Connect".

You should now be connected to the MongoDB instance running in Docker.

## Notes

- The MongoDB data is stored in a named volume `mongo-data`, ensuring data persistence across container restarts.
- The Mongo Express UI is exposed on port 8080, and MongoDB is accessible on port 27017.

Feel free to modify the `docker-compose.yml` file to suit your needs.
