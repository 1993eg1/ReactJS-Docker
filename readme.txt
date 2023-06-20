Interfacing with the Docker container:
# you can view the servers web page at [server ip address]:3000 #
# my favorite way of working with the container after it is running is the use sshfs and mount my-app
to a folder so that i can use a text editor to edit files #
# you could also use scp or a text editor on the docker server if you wished #
# your web app is found at /home/[username]/ReactJS-Docker/my-app

Commands:

Build file
# move to folder that the docker file is stored in #
$ docker build -t reactjs .

Start image:
$ docker run -d -p 3000:3000 reactjs

Find container ID:
$ docker ps

Copy default app files down from image:
$ docker cp [container ID]:/app/my-app /home/[username]/ReactJS-Docker/my-app

Stop Docker container:
$ docker stop [container name]
# if you do not know the name of the docker container you can use the docker ps command #

Start the image with docker compose:
# this will make a link from the host to the container #
# move to the file that docker-compose.yaml is stored in #
# edit [user name] in the docker compose file to your user name
$ docker compose up -d
