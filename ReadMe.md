### containerization-journey

Main aim of this project is to run everything in a container.

- [x] Jenkins setup
- [x] Gitlab setup
- [x] MailHog setup

#### Notes

|server |Ports   |
|------:|-------:|
|MailHog| 8003   |
|Jenkins| 8002   |
|GitLab | 8001   |

#### Getting started

-build and start container

`docker-compose up --build`

or for detached mode

`docker-compose up --build -d`

- start container 

`docker-compose up`

- stop container

`docker-compose down`

- for troubleshooting 

*e.g Navigating container directories*

`docker exec -it container_name /bin/bash`

e.g `docker exec -it jenkins_web /bin/bash`



