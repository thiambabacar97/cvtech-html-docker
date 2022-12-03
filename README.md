= Angular NGINX Docker example

An example project demostrating deployment of angular application in nginx using docker.

== How to run

* Clone the project.
+
[source,shell]
----
$git clone https://github.com/thiambabacar97/cvtech-BT-angular-docker.git
----

* Go to project directory
+
[source,shell]
----
$cd cvtech-BT-angular-docker
----

* Initialize the project
+
[source,shell]
----
$yarn
----

* Build the project
+
[source,shell]
----
$ng build --prod
----

=== Deploy using docker command

* Build the image
+
[source,shell]
----
$docker build -t cvtech-angular:production --build-arg build_env=production .
----

* Create and start the container as daemon
+
[source,shell]
----
$docker run --name cvtech-angular -p 8080:80 -d cvtech-angular
----

=== Verify

Open browser and use docker server URL to access the application. for example if docker is running on localhost url shall be `http://localhost:8080`

== Useful command

* List images
+
[source,shell]
----
$ docker images
----

* List running containers
+
[source,shell]
----
$ docker ps
----

* List all containers both running and stopped
+
[source,shell]
----
$ docker ps -a
----

* Remove container
+
[source,shell]
----
$ docker rm kp-container
----
NOTE: use `-f` to remove running containers `docker rm -f kp-container`

* Remove image
+
[source,shell]
----
$ docker rmi angular-nginx-docker
----

* Remove containers and images using docker-compose
+
[source,shell]
----
$ docker-compose down --rmi all
----

== Useful Links

https://hub.docker.com/_/nginx[NGINX dockerhub] for more info on configuring nginx settings using nginx.conf files etc.
