# NameGame Spring Boot Backend

This application's purpose is to learn and experiment with Java while collaborating on the AspiringX NameGame app project.

## How to Set Up

1. Clone repo locally.

2. Get the `.env` file from the AspiringX shared drive or (optionally copy `.env.example`) and fill out empty fields.
**NOTE:** The default database setup is MySQL running on `localhost:3306` for development purposes but can be updated via the `.env` file values.
**NOTE:** The **JWT** requires a 256 bit hex secret key in order to create tokens, one can be created online or with a tool but a dev one will be included in the `.env` file.

3. To create the default dev MySQL database run the following commands from the project's root folder:
CREATE the database container `docker compose -f src/main/resources/docker-dev-db.yaml up -d`
STOP the database container `docker compose -f src/main/resources/docker-dev-db.yaml down`

5. (*Optional*) Connect to the database with a third party app such as DBeaver or MySQL Workbench and verify the **namegame** database has been created. 
**NOTE:** The JPA dependency will populate the schema when the app is started and delete it when stopped. (This behavior can be updated to only verify the schema if necessary.)

6. Run the **NameGameApplication** file to start the app. (This should create the users table in the database.)

7. Download the postman collection from the AspiringX shared drive to test the JWT register, authenticate and demo end points.
