= Html/Css Docker example

An example project demostrating deployment of angular application in nginx using docker.

== How to run

* Clone the project.

----

$git clone <https://github.com/thiambabacar97/cvtech-BT-angular-docker.git>
----

* Go to project directory

=== Deploy using docker command

* Build the image

----

$docker build -t cvtech-html-csst
----

* Create and start the container as daemon

----

$ docker run --name cvtech-htmlcss -p 8081:80 -d cvtech-htmlcss
----

=== Verify

Open browser and use docker server URL to access the application. for example if docker is running on localhost url shall be `http://localhost:8081`

== Useful command

* List images

----

$ docker images
----

* List running containers

[source,shell]
----

$ docker ps
----

* List all containers both running and stopped

----

$ docker ps -a
----

* Remove container

----

$ docker rm kp-container
----

NOTE: use `-f` to remove running containers `docker rm -f kp-container`

* Remove image

----

$ docker rmi angular-nginx-docker
----

* Remove containers and images using docker-compose

----

$ docker-compose down --rmi all
----

== Useful Links

<https://hub.docker.com/_/nginx[NGINX> dockerhub] for more info on configuring nginx settings using nginx.conf files etc.
