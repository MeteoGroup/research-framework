# Framework to develop minimum viable product (MVP)

This project is an empty framework for research products to come.
The advised approach is to setup using Docker.

First install or update to the latest version of [Docker](https://docs.docker.com/engine/installation/)

### Setup using Docker:

#### Step 1
  Note: Skip this step for linux machines
  Create a docker machine

    docker-machine create -d virtualbox dev
    eval "$(docker-machine env dev)"

  'dev' is the name of the machine created
#### Step 2
  Build the containers

    docker-compose build

#### Step 3
  Start the services

    docker-compose up -d

#### Step 4
  Create database

    docker-compose run --rm web /usr/local/bin/python create_db.py

#### Step 5
  Shut down services

    docker-compose stop

### Tools used:

    python3
    flask
    postgres
    docker
    nginx

### Debugging the application:

  Create python virtual environment

      pyvenv <virtualenv-name>
      source <virutalenv-name>/bin/activate
      cd web
      pip install -r requirements.txt
      flask run

  Use python debugger as usual

      import pdb; pdb.set_trace()

### Adding new python libraries

  Add a new line in requirements.txt file with library name and version
  e.g.,

      Flask==0.11.1
