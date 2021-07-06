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

### Setting up Extended E-mail Notification(Jenkins)

*the following steps are used to setup email notifications*

- go to **configuration**
- under **Extended E-mail Notification**  enter ```SMTP server```  and ```SMTP port```
   
  in this case ```SMTP server``` = mail-server    and  ```SMTP port``` =  1025
  
  
**similar approach can be used in setting up** ```E-mail Notification```


#### Gitlab password reset


*use the following steps for gitlab password*

` docker exec -it` DOCKER_CONTAINER_ID `/bin/sh`

`gitlab-rails console -e production`

  `user = User.where(id: 1).first`

  `user.password = 'your secret'`
  
  `user.password_confirmation = 'your secret'`
  
  `user.save`
  
  `exit`








