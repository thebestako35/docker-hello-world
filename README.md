docker-hello-world
==================

An updated image from the tutumcloud/docker-hello-world repo. This is a very basic Hello World image that we use to test the Automated build of the Dockerfile and the auto deployment of the updated container via Tutum.


Usage
-----

To create the image `dev3l/docker-hello-world`, execute the following command on the docker-hello-world folder:

	docker build -t dev3l/docker-hello-world .

You can now push your new image to the registry:

	sudo docker push dev3l/docker-hello-world


Running your Hello World docker image
-------------------------------------

Start your image:

	sudo docker run -d -p 80 dev3l/docker-hello-world

It will print the new container ID (like `d35bf1374e88`). Get the allocated external port:

	sudo docker port d35bf1374e88 80

It will print the allocated port (like 4751). Test your deployment:

	curl http://localhost:4751/


Editing the Hello World File
----------------------------
I've moved the application / logo to the /app directory. Inside of this directory you can edit the index.php file to customize the Hello World message and/or change the logo to your own.
