# ML Wizard Deployment and Testing Script
This repo contains a `docker-compose.yml` file which can be used to deploy a `del` build locally for testing.

Of course, the prerequisite for running the script is `Docker`.

## Reference Repos
- [Frontend](https://github.com/davutkulaksiz/ml-interface-wizard)
- [Backend](https://github.com/nikolaDrljaca/interface-wizard-backend)

## How to Run
After cloning this repository, navigate to the root directory.
Open a terminal and run: `docker compose up -d` 

## Containers
- `localhost:8000/docs`: Documentation for the backend application.
- `localhost:3000/home`: React application. 
- `localhost:8081/`: Mongo Express driver, allows access to the database.

## Testing
The React app can be accessed as mentioned above. This build showcases functionality related to the ML Interface Wizard part of the project.

So far, we have tested the application with two models with their accompanying `config.json`, `in_transformer.pkl.` and `out_transformer.pkl` files. Note that there is a disctintion between a models `config` and `metadata`. The `config` is used to generate the UI, while the metadata is saved on the backend to describe the model. This metadata is accessible from the backend application, refer to the `/docs`.

Here is the link to the models we used for testing so far:
[https://drive.google.com/drive/folders/1UdiVcG8DnMGcMooE5RqFBBIWO12pxfcd?usp=sharing](https://drive.google.com/drive/folders/1UdiVcG8DnMGcMooE5RqFBBIWO12pxfcd?usp=sharing)


## Note
The script pulls images for the `del2` builds. As new builds are available, the script will be updated accordingly. 

## Existing Issues
1. Sometimes refreshing the `frontend` application causes it to break and throw `404` errors. In this case it is sufficient to open a new tab and navigate to `localhost:3000/home`. This issue is being investigated. 

