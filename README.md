# Docker Compose for PostgreSQL and Keycloak

[![Docker](https://img.shields.io/badge/Docker-v20.10.12-blue?logo=docker)](https://docs.docker.com/get-docker/)
[![Docker Compose](https://img.shields.io/badge/Docker%20Compose-v1.29.2-blue?logo=docker-compose)](https://docs.docker.com/compose/install/)

This repository contains a Docker Compose configuration for running PostgreSQL and Keycloak services.

## Prerequisites

- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Required Docker Images Versions

Below is a table listing the required versions for the Docker images used in this project:

| Service    | Image                       | Version |
| ---------- | --------------------------- | ------- |
| PostgreSQL | `postgres`                  | 15      |
| Keycloak   | `quay.io/keycloak/keycloak` | 23.0    |

## Configure `.env.template` File

This project includes a `.env.template` file that serves as a template for configuring your PostgreSQL and Keycloak environment. To customize your environment, follow these steps:

1. **Copy the Template:**

   - Open the `.env.template` file.
   - Copy its content.

2. **Create a New `.env` File:**

   - Create a new file in the project root directory named `.env`.
   - Paste the copied content into the new `.env` file.

3. **Configure Variables:**

   - Review each environment variable in the `.env` file.
   - Replace the placeholder values with your desired configurations.
   - Ensure to set appropriate values for PostgreSQL user, password, and database, as well as Keycloak admin credentials and other configurations.
   - **NOTE**: The values on the template are used for use keycloak on your local machine

4. **Save Changes:**

   - Save the changes made to the `.env` file.

5. **Run the Services:**

   - After configuring the `.env` file, run the Docker services using the following command:
     ```bash
     docker-compose up -d
     ```

6. **Access Keycloak:**

   - Once the services are up, access Keycloak by navigating to [http://localhost:8083/](http://localhost:8083/) in your web browser.
   - Use the configured admin credentials to log in to the Keycloak Admin Console.

Feel free to tailor the configurations in the `.env` file to meet your specific needs, you can search for more information in the documentation [https://www.keycloak.org/server/all-config](https://www.keycloak.org/server/all-config)
