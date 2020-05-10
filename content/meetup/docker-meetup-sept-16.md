Title: Docker Meetup Sept-16
Date: 2016-09-29 14:40
Author: amolkahat
Category: Pythonpune
Tags: meetup, docker
Slug: docker-meetup-sept-16
Status: published

[PythonPune](http://meetup.com/PythonPune/) was announced the Docker meetup on the September 18. This meetup was hosted by [Suraj Deshmukh](https://twitter.com/surajd_). He works for the Red Hat in Banglore. He works on Project Atomic.

The meetup was started at 10:30. Around 40-50 people was there. As usual [Chandan Kumar](https://twitter.com/ciypro) gave little bit introduction about the speaker. After the Chandan's talk Suraj started with his introduction. Then he started with Docker introduction.

**What is Docker?**

Docker is light weight container/virtualization platform. It is application packaging and delivering mechanism. <!--more-->

**Why Docker?**

-   Docker is very light weight container virtualization platform.
-   Build once and run anywhere.
-   It reduces the time for developing an application and putting it on production.
-   Lighter than Virtual Machine.
-   Less start up time.
-   Less container size.
-   Can deploy many containers on single host.
-   Easy to use.

**Docker Components:**

Docker has 4 main components:

-   **Image : **It is a template used to launch container.
-   **Container : **Container holds everything which needed to run an application.
-   **Registry : **It stores and serves up the actual image assets, and it delegate the authentication to index.
-   **Index : **It is front end of registry. It manages user accounts, permission, search, tagging, all that nice stuff that's in the public web interface.

**Installation :**

-   \# dnf install -f docker
-   \# systemctl start docker
-   \# systemctl enable docker

**Docker Commands :**

-   **docker info :** To check the docker installation information.
-   **docker search \<image\> :** To search docker images with image name.
-   **docker pull \<image\> :** To pull / download the image.
-   **docker images :** To list images in the system.
-   **docker ps (-a) :**  To list all the docker processes. Using -a option you can see all the recently stopped process.
-   **docker run -i -t \<image\> /bin/bash:** To run the docker container and start its bash command.** **
-   **docker commit :  **To store your docker container as an images.
-   **docker logs \<ID\> : **To look in to the logs of container.
-   **docker kill \<ID\> : **To kill the docker container.

After all this commands Suraj explains docker files. Using docker files you can build many images at a time.

This was very nice session of the docker. Thanks Suraj for docker talk. Thanks PythonPune for arranging the meetup.
