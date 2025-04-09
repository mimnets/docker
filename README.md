# How I learn basic docker commands as a beginner in 2025
I was afraid of Docker, thought it was very difficult to understand and more difficult to use. But I was wrong, after long try now I am bit confident.</br>
In this GitHub repositories I will discuss and take notes about my learnings of docker, so that I can return back and have a look if I need to.</br>
All of learning about docker!

# I learn and practice this basic docker commands
- Docker Basic Commands - [The most basic docker commands for beginners in 2025](https://monirulmimnets.blogspot.com/2025/04/the-most-basic-docker-commands-for.html)
- Docker Tag - [What is the correct Docker tag used to download or pull a specific version of software from Docker Hub repositories?](https://monirulmimnets.blogspot.com/2025/04/what-is-correct-docker-tag-used-to.html)
- Docker STDIN - docker run -i : stands for interactive mode, docker run -t: stands for terminal mode for prompt. Together - docker run -it
- Docker PORT Mapping - docker run -p 80:5000 kodekloud/webapp : Here p stand for port mapping with internal port 5000 to external port 80
- Docker Volume Mapping - docker run -v /opt/datadirL/var/lib/mysql mysql: With volume mapping parameter -v it defines and stor the data into local storage at /opt/datadir and docker image internal storage at /var/lib/mysql folders path. If we dittach, delete or remove the image our saved and modified data will be available for later use at local storage.
- Inspect a Docker Container - docker inspect blissful_hopper : We can inspect a docker contianer to learn or know the more details about the container by it's name or ID.
- Attached to a Docker Contianer - docker attach upbeat_hodgkin : By the attach command we can switch to the docker contianer prompt or inside the running container to insturct or give command.
- Finally Docker Exit - By this docker exit command we can logout or take exit from inside the docker contaner. 

