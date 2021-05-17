# airflow-example-repo

Example repository to test airflow integrations. Comes with a simple
test dag.

## setup

We'll run airflow using [Docker](https://www.docker.com/). First make sure you have Docker installed and have it running. Then run
the following commands:

1. `mkdir ./logs ./plugins`
2. `echo -e "AIRFLOW_UID=$(id -u)\nAIRFLOW_GID=0" > .env`
3. `docker-compose up airflow-init`
4. `docker-compose up` (Note, this may fail due an out of memory error. In that case, you can increase the container size in your Docker preferences. 4GB should be plenty.)

If you've done this correctly, airflow will be up and running and the UI
will be available at http://localhost:8080.
