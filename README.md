# Framework to develop minimum viable product (MVP)



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


### Setup using Docker:

  Create a docker machine

    docker-machine create -d virtualbox dev
    eval "$(docker-machine env dev)"

  Build the containers

    docker-compose build

  Start the services

    docker-compose up -d

  Create database

    docker-compose run web /usr/local/bin/python create_db.py

  Should be able access the application here - http://192.168.99.100/
