# ML Wizard Deployment and Testing Script
This repo contains a `docker-compose.yml` file which can be used to deploy a `del` build locally for testing.

Of course, the prerequisite for running the script is `Docker`.

## Reference Repos
- [Frontend]("https://github.com/davutkulaksiz/ml-interface-wizard")
- [Backend]("https://github.com/nikolaDrljaca/interface-wizard-backend")

## How to Run
After cloning this repository, navigate to the root directory.
Open a terminal and run: `docker compose up -d` 

## Containers
- `localhost:8000/docs`: Documentation for the backend application.
- `localhost:3000/home`: React application. 
- `localhost:8081/`: Mongo Express driver, allows access to the database.

## Note
The script pulls images for the `del2` builds. As new builds are available, the script will be updated accordingly. 