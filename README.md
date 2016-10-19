Automated build of phpPgAdmin with Docker
===========

[![Docker Repository on Quay](https://quay.io/repository/lups/phppgadmin/status "Docker Repository on Quay")](https://quay.io/repository/lups/phppgadmin)

### Apache and Postgres environment variables
Apache and Postgres will make of the following environment variables.

	POSTGRES_HOST=localhost
	POSTGRES_PORT=5432
	POSTGRES_DEFAULTDB=defaultdb

### Use the pre built image
The pre built image can be downloaded using docker directly. After that you do not need to use this command again, you will have the image on your machine.

	$ docker pull lups/phppgadmin


### Build the docker image by yourself
If you prefer you can easily build the docker image by yourself. After this the image is ready for use on your machine and can be used for multiple starts.

	$ docker build -t lups/phppgadmin .


### Start the container
The container has all pre requisites set up to run phpPgAdmin. Specify all needed environment variables.

	$ docker run -i -d -p 80 -e POSTGRES_HOST=localhost -e POSTGRES_PORT=5432 -v /etc/localtime:/etc/localtime lups/phppgadmin

Trying the browser on url http://localhost..